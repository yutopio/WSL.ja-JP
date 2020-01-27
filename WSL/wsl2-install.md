---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91bd479e922fc29bf11b89dcfe06fa381632c4fa
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520551"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="64624-104">WSL 2 のインストール手順</span><span class="sxs-lookup"><span data-stu-id="64624-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="64624-105">WSL2 をインストールする方法については、以下のビデオをご覧ください。または、この記事の「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64624-105">You can watch the video below, or read on in this article to learn how to install WSL2.</span></span> 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

<span data-ttu-id="64624-106">WSL 2 をインストールして使用を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="64624-106">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="64624-107">WSL 2 は、Windows 10 ビルド18917以降でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="64624-107">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="64624-108">WSL がインストールされていることを確認します (この手順については[こちら](./install-win10.md)を参照してください)。また、Windows 10**ビルド 18917**以降を実行していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="64624-108">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="64624-109">ビルド18917以降を使用していることを確認するには[、Windows Insider プログラムに](https://insider.windows.com/en-us/)参加して、"高速" リングまたは "低速" リングを選択してください。</span><span class="sxs-lookup"><span data-stu-id="64624-109">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="64624-110">Windows のバージョンを確認するには、コマンドプロンプトを開き、`ver` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="64624-110">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="64624-111">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="64624-111">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="64624-112">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="64624-112">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="64624-113">現在のディストリビューションが使用している WSL のバージョンを確認する</span><span class="sxs-lookup"><span data-stu-id="64624-113">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="64624-114">' 仮想マシンプラットフォーム ' オプションのコンポーネントを有効にし、WSL が有効になっていることを確認してください</span><span class="sxs-lookup"><span data-stu-id="64624-114">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="64624-115">Windows Subsystem for Linux と仮想マシンプラットフォームのオプションコンポーネントの両方がインストールされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64624-115">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="64624-116">これを行うには、PowerShell で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="64624-116">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="64624-117">両方のコンポーネントのインストールを完了するには、コンピューターを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="64624-117">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="64624-118">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="64624-118">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="64624-119">Linux ディストリビューションがインストールされていない場合は、 [Windows 10](./install-win10.md#install-your-linux-distribution-of-choice)のインストールに関するドキュメントページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64624-119">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="64624-120">ディストリビューションを設定するには、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="64624-120">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="64624-121">`<Distro>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="64624-121">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="64624-122">(これらは、コマンド `wsl -l` を使用して確認できます)。</span><span class="sxs-lookup"><span data-stu-id="64624-122">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="64624-123">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="64624-123">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="64624-124">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="64624-124">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="64624-125">これにより、インストールする新しいディストリビューションはすべて WSL 2 ディストリビューションとして初期化されます。</span><span class="sxs-lookup"><span data-stu-id="64624-125">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="64624-126">現在のディストリビューションが使用している WSL のバージョンを確認して終了する</span><span class="sxs-lookup"><span data-stu-id="64624-126">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="64624-127">各ディストリビューションでどのバージョンの WSL が使用されているかを確認するには、次のコマンドを使用します (Windows ビルド18917以降でのみ使用できます)。</span><span class="sxs-lookup"><span data-stu-id="64624-127">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="64624-128">`wsl --list --verbose` または `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="64624-128">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="64624-129">上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="64624-129">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="64624-130">これで、WSL 2 ディストリビューションを自由に使い始めることができます。</span><span class="sxs-lookup"><span data-stu-id="64624-130">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="64624-131">トラブルシューティング :</span><span class="sxs-lookup"><span data-stu-id="64624-131">Troubleshooting:</span></span> 

<span data-ttu-id="64624-132">WSL2 のインストール時の関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="64624-132">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="64624-133">その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64624-133">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="64624-134">**インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**</span><span class="sxs-lookup"><span data-stu-id="64624-134">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="64624-135">コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="64624-135">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="64624-136">これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。</span><span class="sxs-lookup"><span data-stu-id="64624-136">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="64624-137">**アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="64624-137">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="64624-138">Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="64624-138">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="64624-139">WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="64624-139">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="64624-140">WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64624-140">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="64624-141">**仮想ディスクシステムの制限により、要求された操作を完了できませんでした。バーチャルハードディスクファイルは、圧縮と暗号化を解除する必要があり、スパースにすることはできません。**</span><span class="sxs-lookup"><span data-stu-id="64624-141">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="64624-142">この問題が追跡されている[#4103 Wsl Github スレッド](https://github.com/microsoft/WSL/issues/4103)を確認して、更新された情報を確認してください。</span><span class="sxs-lookup"><span data-stu-id="64624-142">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="64624-143">**"Wsl" という用語は、コマンドレット、関数、スクリプトファイル、または操作可能なプログラムの名前として認識されません。**</span><span class="sxs-lookup"><span data-stu-id="64624-143">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="64624-144">[Windows Subsystem For Linux のオプションコンポーネントがインストールさ](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled)れていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="64624-144">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="64624-145">また、Arm64 デバイスを使用していて、PowerShell からこのコマンドを実行している場合は、このエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64624-145">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="64624-146">代わりに、 [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)またはコマンドプロンプトから `wsl.exe` を実行します。</span><span class="sxs-lookup"><span data-stu-id="64624-146">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
