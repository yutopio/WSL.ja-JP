---
title: Windows Server に Linux サブシステムをインストールする
description: Windows Server 上の Linux サブシステムのインストール手順です。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269780"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="8f433-104">Windows Server インストールガイド</span><span class="sxs-lookup"><span data-stu-id="8f433-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="8f433-105">Windows Server 2019 以降に適用されます</span><span class="sxs-lookup"><span data-stu-id="8f433-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="8f433-106">Microsoft は、windows [Server で](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)windows Subsystem for Linux を使用できるようになったことを、build2017 年に発表しました。</span><span class="sxs-lookup"><span data-stu-id="8f433-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="8f433-107">これらの手順では、windows Server 1709 以降で Windows Subsystem for Linux を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f433-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="8f433-108">Windows Subsystem for Linux (WSL) を有効にする</span><span class="sxs-lookup"><span data-stu-id="8f433-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="8f433-109">Windows で Linux ディストリビューションを実行するには、[Windows Subsystem for Linux] オプション機能を有効にし、再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f433-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="8f433-110">管理者として PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="8f433-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="8f433-111">メッセージが表示されたら、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="8f433-111">Restart your computer when prompted.</span></span> <span data-ttu-id="8f433-112">**この再起動は**、wsl が信頼された実行環境を開始できるようにするために必要です。</span><span class="sxs-lookup"><span data-stu-id="8f433-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="8f433-113">Linux ディストリビューションをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="8f433-113">Download a Linux distro</span></span>

<span data-ttu-id="8f433-114">お気に入りの Linux ディストリビューションをダウンロードするには、こちら[の手順](install-manual.md)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="8f433-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="8f433-115">Linux ディストリビューションを抽出してインストールする</span><span class="sxs-lookup"><span data-stu-id="8f433-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="8f433-116">これで、ディストリビューションをダウンロードしたので、その内容を抽出し、ディストリビューションを手動でインストールします。</span><span class="sxs-lookup"><span data-stu-id="8f433-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="8f433-117">PowerShell を使用して、パッケージの内容を抽出します。`<distro>.appx`</span><span class="sxs-lookup"><span data-stu-id="8f433-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="8f433-118">ディストリビューションランチャーを実行してインストールを完了し、という名前`<distro>.exe`のターゲットフォルダーでディストリビューションランチャーアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="8f433-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="8f433-119">例: `ubuntu.exe`、など。</span><span class="sxs-lookup"><span data-stu-id="8f433-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server での Ubuntu ディストリビューションの拡張](media/server-appx-expand.png)

    > <span data-ttu-id="8f433-121">**トラブルシューティング**</span><span class="sxs-lookup"><span data-stu-id="8f433-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="8f433-122">次**のエラーによりインストールに失敗しました: 0x8007007e**:このエラーは、システムで WSL がサポートされていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="8f433-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="8f433-123">次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8f433-123">Make sure that:</span></span>
    >   * <span data-ttu-id="8f433-124">Windows ビルド16215以降を実行しています。</span><span class="sxs-lookup"><span data-stu-id="8f433-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="8f433-125">[ビルドを確認](troubleshooting.md#check-your-build-number)します。</span><span class="sxs-lookup"><span data-stu-id="8f433-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="8f433-126">Windows Subsystem for Linux のオプションコンポーネントが有効になり、コンピューターが再起動されました。</span><span class="sxs-lookup"><span data-stu-id="8f433-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="8f433-127">[WSL が有効になっていることを確認して](troubleshooting.md#confirm-wsl-is-enabled)ください。</span><span class="sxs-lookup"><span data-stu-id="8f433-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="8f433-128">ディストリビューションパスを Windows 環境パス (`C:\Users\Administrator\Ubuntu`この例では) に追加します。たとえば、Powershell を使用します。</span><span class="sxs-lookup"><span data-stu-id="8f433-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="8f433-129">を入力`<distro>.exe`して、任意のパスからディストリビューションを起動できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8f433-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="8f433-130">たとえば次のようになります。`ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="8f433-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="8f433-131">Linux ディストリビューションがインストールされたので、ディストリビューションを使用する前に、[新しいディストリビューションインスタンスを初期化](initialize-distro.md)する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f433-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
