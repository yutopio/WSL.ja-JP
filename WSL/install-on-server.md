---
title: Windows Server で Linux サブシステムをインストールします。
description: Windows Server で Linux サブシステムのインストール手順。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、windows server 用 windows サブシステム
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 25723395212575f8fe2dcbfbd30b59de9431816a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035077"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="75c72-104">Windows Server インストール ガイド</span><span class="sxs-lookup"><span data-stu-id="75c72-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="75c72-105">Windows Server 2019 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="75c72-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="75c72-106">/Build2017、Windows Subsystem for Linux がなります、Microsoft が発表されました/ [Windows Server で使用可能な](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)します。</span><span class="sxs-lookup"><span data-stu-id="75c72-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="75c72-107">これらの手順は、Windows Server 1709 以降の Linux 用 Windows サブシステムを実行している説明します。</span><span class="sxs-lookup"><span data-stu-id="75c72-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="75c72-108">Linux (WSL) の Windows サブシステムを有効にします。</span><span class="sxs-lookup"><span data-stu-id="75c72-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="75c72-109">を Windows での Linux ディストリビューションを実行する前に、"Windows サブシステムの Linux"の省略可能な機能を有効にし、再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="75c72-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="75c72-110">管理者として PowerShell を開きを実行します。</span><span class="sxs-lookup"><span data-stu-id="75c72-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="75c72-111">コンピューターが表示されたら再起動します。</span><span class="sxs-lookup"><span data-stu-id="75c72-111">Restart your computer when prompted.</span></span> <span data-ttu-id="75c72-112">**この再起動は必要な**WSL が信頼できる実行環境を開始できることを保証するためにします。</span><span class="sxs-lookup"><span data-stu-id="75c72-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="75c72-113">Linux ディストリビューションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="75c72-113">Download a Linux distro</span></span>

<span data-ttu-id="75c72-114">次の[手順](install-manual.md)お気に入りの Linux ディストリビューションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="75c72-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="75c72-115">抽出して、Linux ディストリビューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="75c72-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="75c72-116">これで、ディストリビューションをダウンロードすると、その内容を抽出およびディストリビューションを手動でインストールします。</span><span class="sxs-lookup"><span data-stu-id="75c72-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="75c72-117">抽出、`<distro>.appx`例: PowerShell を使用して、パッケージの内容。</span><span class="sxs-lookup"><span data-stu-id="75c72-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. <span data-ttu-id="75c72-118">インストールを完了するには、ディストリビューションのランチャー アプリケーションをターゲット フォルダーで実行ディストリビューション ランチャーをという名前の実行`<distro>.exe`します。</span><span class="sxs-lookup"><span data-stu-id="75c72-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="75c72-119">例:`ubuntu.exe`など。</span><span class="sxs-lookup"><span data-stu-id="75c72-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server での展開の Ubuntu ディストリビューション](media/server-appx-expand.png)

    > <span data-ttu-id="75c72-121">**トラブルシューティング**</span><span class="sxs-lookup"><span data-stu-id="75c72-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="75c72-122">**インストールに失敗しましたエラー 0x8007007e**:WSL をサポートしていないシステムでこのエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="75c72-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="75c72-123">次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="75c72-123">Make sure that:</span></span>
    >   * <span data-ttu-id="75c72-124">16215 またはそれ以降は、Windows ビルドを実行しています。</span><span class="sxs-lookup"><span data-stu-id="75c72-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="75c72-125">[ビルド確認](troubleshooting.md#check-your-build-number)します。</span><span class="sxs-lookup"><span data-stu-id="75c72-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="75c72-126">Linux の省略可能なコンポーネント用 Windows サブシステムが有効になっており、コンピューターが再起動します。</span><span class="sxs-lookup"><span data-stu-id="75c72-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="75c72-127">[WSL が有効になっていることを確認](troubleshooting.md#confirm-wsl-is-enabled)します。</span><span class="sxs-lookup"><span data-stu-id="75c72-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="75c72-128">Windows 環境のパスに、ディストリビューションのパスを追加 (`C:\Users\Administrator\Ubuntu`この例では)、Powershell を使用するなど。</span><span class="sxs-lookup"><span data-stu-id="75c72-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="75c72-129">」と入力して任意のパスから、ディストリビューションを起動できるようになりました`<distro>.exe`します。</span><span class="sxs-lookup"><span data-stu-id="75c72-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="75c72-130">たとえば次のようになります。`ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="75c72-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="75c72-131">必要があります、Linux ディストリビューションがインストールされた[ディストリビューションの新しいインスタンスを初期化](initialize-distro.md)ディストリビューションを使用する前にします。</span><span class="sxs-lookup"><span data-stu-id="75c72-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
