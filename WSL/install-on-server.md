---
title: Windows Server に Linux サブシステムをインストールする
description: Windows Server 上の Linux サブシステムのインストール手順です。
keywords: BashOnWindows, bash, wsl, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256395"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="a4f27-104">Windows Server インストール ガイド</span><span class="sxs-lookup"><span data-stu-id="a4f27-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="a4f27-105">Windows Server 2019 以降に適用されます</span><span class="sxs-lookup"><span data-stu-id="a4f27-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="a4f27-106">Microsoft は、[Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/) 上で Linux 用 Windows サブシステムを利用できるようになったことを //Build2017 で発表しました。</span><span class="sxs-lookup"><span data-stu-id="a4f27-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="a4f27-107">以下の手順では、Windows Server 1709 以降で Linux 用 Windows サブシステムを実行する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="a4f27-108">Linux 用 Windows サブシステム (WSL) を有効にする</span><span class="sxs-lookup"><span data-stu-id="a4f27-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="a4f27-109">Windows 上で Linux ディストリビューションを実行する前に、"Linux 用 Windows サブシステム" オプション機能を有効にして再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4f27-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="a4f27-110">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="a4f27-111">メッセージが表示されたら、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-111">Restart your computer when prompted.</span></span> <span data-ttu-id="a4f27-112">WSL から信頼できる実行環境を開始できるようにするには、**この再起動が必要**です。</span><span class="sxs-lookup"><span data-stu-id="a4f27-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="a4f27-113">Linux ディストリビューションをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="a4f27-113">Download a Linux distro</span></span>

<span data-ttu-id="a4f27-114">[これらの手順](install-manual.md)に従って、お気に入りの Linux ディストリビューションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a4f27-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="a4f27-115">Linux ディストリビューションを抽出してインストールする</span><span class="sxs-lookup"><span data-stu-id="a4f27-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="a4f27-116">ディストリビューションをダウンロードしたので、その内容を抽出し、手動でディストリビューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a4f27-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="a4f27-117">PowerShell を使用するなどして、`<distro>.appx` パッケージのコンテンツを抽出します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="a4f27-118">ディストリビューション ランチャーを実行します。インストールを完了するには、`<distro>.exe` という名前のターゲット フォルダーでディストリビューション ランチャー アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="a4f27-119">例: `ubuntu.exe` など。</span><span class="sxs-lookup"><span data-stu-id="a4f27-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server 上の展開された Ubuntu ディストリビューション](media/server-appx-expand.png)

    > <span data-ttu-id="a4f27-121">**トラブルシューティング**</span><span class="sxs-lookup"><span data-stu-id="a4f27-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="a4f27-122">**エラー 0x8007007e が発生してインストールに失敗しました**:このエラーは、システムで WSL がサポートされていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="a4f27-123">次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-123">Make sure that:</span></span>
    >   * <span data-ttu-id="a4f27-124">Windows ビルド 16215 以降を実行している。</span><span class="sxs-lookup"><span data-stu-id="a4f27-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="a4f27-125">[ビルドを確認してください](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="a4f27-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="a4f27-126">Windows Subsystem for Linux オプション コンポーネントが有効になっていて、コンピューターが再起動されている。</span><span class="sxs-lookup"><span data-stu-id="a4f27-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="a4f27-127">[WSL が有効になっていることを確認してください](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="a4f27-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="a4f27-128">たとえば、Powershell を使用して、Windows 環境の PATH (この例では `C:\Users\Administrator\Ubuntu`) にディストリビューション パスを追加します。</span><span class="sxs-lookup"><span data-stu-id="a4f27-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="a4f27-129">これで、「`<distro>.exe`」と入力して任意のパスからディストリビューションを起動できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a4f27-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="a4f27-130">たとえば次のようになります。`ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="a4f27-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="a4f27-131">Linux ディストリビューションがインストールされたので、ディストリビューションを使用する前に、一度[新しいディストリビューション インスタンスを初期化する](initialize-distro.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4f27-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
