---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91994f3a075436c022acb9dadeea072142687b72
ms.sourcegitcommit: cf6d8e277ed3102f8f879b9f39ba0966d4ea6135
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "74164338"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="24b1c-104">WSL 2 のインストール手順</span><span class="sxs-lookup"><span data-stu-id="24b1c-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="24b1c-105">WSL 2 をインストールして使用を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="24b1c-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="24b1c-106">WSL 2 は、Windows 10 ビルド18917以降でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="24b1c-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="24b1c-107">WSL がインストールされていることを確認します (この手順については[こちら](./install-win10.md)を参照してください)。また、Windows 10**ビルド 18917**以降を実行していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="24b1c-108">ビルド18917以降を使用していることを確認するには[、Windows Insider プログラムに](https://insider.windows.com/en-us/)参加して、"高速" リングを選択してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="24b1c-109">Windows のバージョンを確認するには、コマンドプロンプトを開き、`ver` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="24b1c-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="24b1c-110">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="24b1c-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="24b1c-111">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="24b1c-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="24b1c-112">現在のディストリビューションが使用している WSL のバージョンを確認する</span><span class="sxs-lookup"><span data-stu-id="24b1c-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="24b1c-113">' 仮想マシンプラットフォーム ' オプションのコンポーネントを有効にし、WSL が有効になっていることを確認してください</span><span class="sxs-lookup"><span data-stu-id="24b1c-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="24b1c-114">' 仮想マシンプラットフォーム ' コンポーネントを有効にするには、PowerShell を管理者として開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="24b1c-114">To enable the 'Virtual Machine Platform' component open PowerShell as an administrator and run the command below.</span></span> <span data-ttu-id="24b1c-115">WSL を初めてインストールする場合は、再起動を求めるメッセージが表示されたら [いいえ] を選択します。これは、"Windows Subsystem for Linux" オプションコンポーネントをインストールした後で、コンピューターを再起動する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="24b1c-115">If you are installing WSL for the first time then select 'No' when prompted for a restart, as you will need to restart your machine anyway after installing the 'Windows Subsystem for Linux' optional component.</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

<span data-ttu-id="24b1c-116">また、Linux 用 Windows Subsystem オプションコンポーネントが有効になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24b1c-116">You will also need to make sure that the Windows Subsystem for Linux optional component is enabled.</span></span> <span data-ttu-id="24b1c-117">これを行うには、PowerShell ウィンドウから管理者特権で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="24b1c-117">You can do this by running the following command from a PowerShell window with administrator privileges:</span></span> 

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="24b1c-118">両方のコンポーネントのインストールを完了するには、コンピューターを再起動してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-118">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="24b1c-119">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="24b1c-119">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="24b1c-120">Linux ディストリビューションがインストールされていない場合は、 [Windows 10](./install-win10.md#install-your-linux-distribution-of-choice)のインストールに関するドキュメントページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-120">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="24b1c-121">PowerShell で、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="24b1c-121">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="24b1c-122">`<Distro>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-122">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="24b1c-123">(これらは、コマンド `wsl -l` を使用して確認できます)。</span><span class="sxs-lookup"><span data-stu-id="24b1c-123">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="24b1c-124">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="24b1c-124">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="24b1c-125">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="24b1c-125">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="24b1c-126">これにより、インストールする新しいディストリビューションはすべて WSL 2 ディストリビューションとして初期化されます。</span><span class="sxs-lookup"><span data-stu-id="24b1c-126">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="24b1c-127">現在のディストリビューションが使用している WSL のバージョンを確認して終了する</span><span class="sxs-lookup"><span data-stu-id="24b1c-127">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="24b1c-128">各ディストリビューションでどのバージョンの WSL が使用されているかを確認するには、次のコマンドを使用します (Windows ビルド18917以降でのみ使用できます)。</span><span class="sxs-lookup"><span data-stu-id="24b1c-128">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="24b1c-129">`wsl --list --verbose` または `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="24b1c-129">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="24b1c-130">上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="24b1c-130">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="24b1c-131">これで、WSL 2 ディストリビューションを自由に使い始めることができます。</span><span class="sxs-lookup"><span data-stu-id="24b1c-131">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="24b1c-132">トラブルシューティング:</span><span class="sxs-lookup"><span data-stu-id="24b1c-132">Troubleshooting:</span></span> 

<span data-ttu-id="24b1c-133">WSL2 のインストール時の関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="24b1c-133">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="24b1c-134">その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-134">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="24b1c-135">**インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**</span><span class="sxs-lookup"><span data-stu-id="24b1c-135">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="24b1c-136">コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-136">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="24b1c-137">これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。</span><span class="sxs-lookup"><span data-stu-id="24b1c-137">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="24b1c-138">**アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="24b1c-138">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="24b1c-139">Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-139">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="24b1c-140">WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="24b1c-140">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="24b1c-141">WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-141">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="24b1c-142">**仮想ディスクシステムの制限により、要求された操作を完了できませんでした。バーチャルハードディスクファイルは、圧縮と暗号化を解除する必要があり、スパースにすることはできません。**</span><span class="sxs-lookup"><span data-stu-id="24b1c-142">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="24b1c-143">この問題が追跡されている[#4103 Wsl Github スレッド](https://github.com/microsoft/WSL/issues/4103)を確認して、更新された情報を確認してください。</span><span class="sxs-lookup"><span data-stu-id="24b1c-143">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>