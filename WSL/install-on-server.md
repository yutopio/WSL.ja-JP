---
title: Windows Server に Linux サブシステムをインストールする
description: Windows Server 上の Linux サブシステムのインストール手順です。
keywords: BashOnWindows, bash, wsl, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 805b7d266020c62e0c6f58889541517d44db3726
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153076"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="527bb-104">Windows Server インストール ガイド</span><span class="sxs-lookup"><span data-stu-id="527bb-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="527bb-105">Linux 用 Windows サブシステムは、Windows Server 2019 (バージョン 1709) 以降にインストールできます。</span><span class="sxs-lookup"><span data-stu-id="527bb-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="527bb-106">このガイドでは、お使いのマシンで WSL を有効にする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="527bb-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="527bb-107">Linux 用 Windows サブシステムを有効にする</span><span class="sxs-lookup"><span data-stu-id="527bb-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="527bb-108">Windows 上で Linux ディストリビューションを実行する前に、"Linux 用 Windows サブシステム" オプション機能を有効にして再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="527bb-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="527bb-109">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="527bb-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

<span data-ttu-id="527bb-110">**100% のシステム コールの互換性とより高速な IO パフォーマンスが必要な場合は、以下を読んで WSL 2 をインストールしてください。**</span><span class="sxs-lookup"><span data-stu-id="527bb-110">**If you're looking for 100% system call compatibility and faster IO performance, read below to install WSL 2!**</span></span>

<span data-ttu-id="527bb-111">WSL 2 は、Windows 10、バージョン 2004、ビルド 19041 以上でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="527bb-111">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="527bb-112">[Windows のバージョンを更新しなければならない](ms-settings:windowsupdate)場合があります。</span><span class="sxs-lookup"><span data-stu-id="527bb-112">You may need to [update your Windows version](ms-settings:windowsupdate).</span></span>

<span data-ttu-id="527bb-113">**WSL 1 から続ける場合は、プロンプトが表示されたらマシンを再起動し、[こちら](./install-on-server.md#download-a-linux-distribution)** に従ってインストールを続行してください</span><span class="sxs-lookup"><span data-stu-id="527bb-113">**If continuing with WSL 1, restart your machine when prompted and continue with installation [here](./install-on-server.md#download-a-linux-distribution)**</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="527bb-114">仮想マシン プラットフォームのオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="527bb-114">Enable the Virtual Machine Platform optional component</span></span>

<span data-ttu-id="527bb-115">"仮想マシン プラットフォーム" のオプション コンポーネントがインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="527bb-115">Ensure the 'Virtual Machine Platform' optional component is installed.</span></span> <span data-ttu-id="527bb-116">これを行うには、PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="527bb-116">You can do that by running the following command in PowerShell:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="527bb-117">Linux ディストリビューションをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="527bb-117">Download a Linux distribution</span></span>

<span data-ttu-id="527bb-118">[これらの手順](install-manual.md)に従って、お気に入りの Linux ディストリビューションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="527bb-118">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="527bb-119">Linux ディストリビューションを展開してインストールする</span><span class="sxs-lookup"><span data-stu-id="527bb-119">Extract and install a Linux distribution</span></span>

<span data-ttu-id="527bb-120">Linux ディストリビューションをダウンロードしたら、その内容を展開して手動でインストールするために、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="527bb-120">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="527bb-121">PowerShell を使用して、`<distro>.appx` パッケージの内容を展開します。</span><span class="sxs-lookup"><span data-stu-id="527bb-121">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="527bb-122">ターゲット フォルダーでディストリビューション ランチャー アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="527bb-122">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="527bb-123">ランチャーには、通常、`<distro>.exe` という名前が付けられます (たとえば、`ubuntu.exe`)。</span><span class="sxs-lookup"><span data-stu-id="527bb-123">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Windows Server 上の展開された Ubuntu ディストリビューション](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="527bb-125">**エラー 0x8007007e が発生してインストールに失敗しました**:このエラーが発生した場合、お使いのシステムは WSL をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="527bb-125">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="527bb-126">Windows ビルド 16215 以降を実行していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="527bb-126">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="527bb-127">[ビルドを確認してください](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="527bb-127">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="527bb-128">さらに、[WSL が有効になっていることを確認](troubleshooting.md#confirm-wsl-is-enabled)し、この機能を有効にした後にコンピューターが再起動されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="527bb-128">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="527bb-129">3. PowerShell を使用して、Windows 環境の PATH (この例では `C:\Users\Administrator\Ubuntu`) にディストリビューション パスを追加します。</span><span class="sxs-lookup"><span data-stu-id="527bb-129">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="527bb-130">これで、「`<distro>.exe`」と入力して任意のパスからディストリビューションを起動できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="527bb-130">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="527bb-131">たとえば、 `ubuntu.exe`と指定します。</span><span class="sxs-lookup"><span data-stu-id="527bb-131">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="527bb-132">インストールされたら、使用する前に[新しいディストリビューション インスタンスを初期化する](initialize-distro.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="527bb-132">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
