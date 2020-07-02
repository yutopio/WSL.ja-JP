---
title: Windows Server に Linux サブシステムをインストールする
description: Windows Server 上の Linux サブシステムのインストール手順です。
keywords: BashOnWindows, bash, wsl, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671022"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="4b920-104">Windows Server インストール ガイド</span><span class="sxs-lookup"><span data-stu-id="4b920-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="4b920-105">Linux 用 Windows サブシステムは、Windows Server 2019 (バージョン 1709) 以降にインストールできます。</span><span class="sxs-lookup"><span data-stu-id="4b920-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="4b920-106">このガイドでは、お使いのマシンで WSL を有効にする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="4b920-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="4b920-107">Linux 用 Windows サブシステムを有効にする</span><span class="sxs-lookup"><span data-stu-id="4b920-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="4b920-108">Windows 上で Linux ディストリビューションを実行する前に、"Linux 用 Windows サブシステム" オプション機能を有効にして再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b920-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="4b920-109">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="4b920-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="4b920-110">Linux ディストリビューションをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="4b920-110">Download a Linux distribution</span></span>

<span data-ttu-id="4b920-111">[これらの手順](install-manual.md)に従って、お気に入りの Linux ディストリビューションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="4b920-111">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="4b920-112">Linux ディストリビューションを展開してインストールする</span><span class="sxs-lookup"><span data-stu-id="4b920-112">Extract and install a Linux distribution</span></span>

<span data-ttu-id="4b920-113">Linux ディストリビューションをダウンロードしたら、その内容を展開して手動でインストールするために、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4b920-113">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="4b920-114">PowerShell を使用して、`<distro>.appx` パッケージの内容を展開します。</span><span class="sxs-lookup"><span data-stu-id="4b920-114">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="4b920-115">ターゲット フォルダーでディストリビューション ランチャー アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="4b920-115">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="4b920-116">ランチャーには、通常、`<distro>.exe` という名前が付けられます (たとえば、`ubuntu.exe`)。</span><span class="sxs-lookup"><span data-stu-id="4b920-116">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Windows Server 上の展開された Ubuntu ディストリビューション](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="4b920-118">**エラー 0x8007007e が発生してインストールに失敗しました**:このエラーが発生した場合、お使いのシステムは WSL をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4b920-118">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="4b920-119">Windows ビルド 16215 以降を実行していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4b920-119">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="4b920-120">[ビルドを確認してください](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="4b920-120">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="4b920-121">さらに、[WSL が有効になっていることを確認](troubleshooting.md#confirm-wsl-is-enabled)し、この機能を有効にした後にコンピューターが再起動されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4b920-121">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="4b920-122">3. PowerShell を使用して、Windows 環境の PATH (この例では `C:\Users\Administrator\Ubuntu`) にディストリビューション パスを追加します。</span><span class="sxs-lookup"><span data-stu-id="4b920-122">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="4b920-123">これで、「`<distro>.exe`」と入力して任意のパスからディストリビューションを起動できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4b920-123">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="4b920-124">たとえば、 `ubuntu.exe`と指定します。</span><span class="sxs-lookup"><span data-stu-id="4b920-124">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="4b920-125">インストールされたら、使用する前に[新しいディストリビューション インスタンスを初期化する](initialize-distro.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="4b920-125">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
