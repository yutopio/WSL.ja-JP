---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4ae5b8452ae2aec679c2f0450dc48644b77fc1c9
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020956"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="f79c2-104">WSL 2 のインストール手順</span><span class="sxs-lookup"><span data-stu-id="f79c2-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="f79c2-105">WSL 2 をインストールして使用を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f79c2-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="f79c2-106">WSL がインストールされていることを確認します (この手順については[こちら](./install-win10.md)を参照してください)。また、Windows 10 ビルド18917以降を実行していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f79c2-106">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 build 18917 or higher</span></span>
   - <span data-ttu-id="f79c2-107">ビルド18917以降を使用していることを確認するには[、Windows Insider プログラムに](https://insider.windows.com/en-us/)参加して、"高速" リングを選択してください。</span><span class="sxs-lookup"><span data-stu-id="f79c2-107">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="f79c2-108">Windows のバージョンを確認するには、コマンドプロンプトを開き`ver` 、コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f79c2-108">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="f79c2-109">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="f79c2-109">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="f79c2-110">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="f79c2-110">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="f79c2-111">現在のディストリビューションが使用している WSL のバージョンを確認する</span><span class="sxs-lookup"><span data-stu-id="f79c2-111">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="f79c2-112">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="f79c2-112">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="f79c2-113">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="f79c2-113">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="f79c2-114">これらの変更を有効にした後、コンピューターを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f79c2-114">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="f79c2-115">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="f79c2-115">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="f79c2-116">PowerShell で、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="f79c2-116">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="f79c2-117">`<Distro>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="f79c2-117">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="f79c2-118">(これらは、コマンド `wsl -l` を使用して確認できます)。</span><span class="sxs-lookup"><span data-stu-id="f79c2-118">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="f79c2-119">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="f79c2-119">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="f79c2-120">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="f79c2-120">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="f79c2-121">これにより、インストールする新しいディストリビューションはすべて WSL 2 ディストリビューションとして初期化されます。</span><span class="sxs-lookup"><span data-stu-id="f79c2-121">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="f79c2-122">現在のディストリビューションが使用している WSL のバージョンを確認して終了する</span><span class="sxs-lookup"><span data-stu-id="f79c2-122">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="f79c2-123">各ディストリビューションでどのバージョンの WSL が使用されているかを確認するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f79c2-123">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="f79c2-124">`wsl --list --verbose` または `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="f79c2-124">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="f79c2-125">上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="f79c2-125">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="f79c2-126">これで、WSL 2 ディストリビューションを自由に使い始めることができます。</span><span class="sxs-lookup"><span data-stu-id="f79c2-126">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="f79c2-127">トラブルシューティング:</span><span class="sxs-lookup"><span data-stu-id="f79c2-127">Troubleshooting:</span></span> 

<span data-ttu-id="f79c2-128">WSL2 のインストール時の関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f79c2-128">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="f79c2-129">その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f79c2-129">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="f79c2-130">**インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**</span><span class="sxs-lookup"><span data-stu-id="f79c2-130">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="f79c2-131">コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f79c2-131">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="f79c2-132">これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。</span><span class="sxs-lookup"><span data-stu-id="f79c2-132">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="f79c2-133">**アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="f79c2-133">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="f79c2-134">Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f79c2-134">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="f79c2-135">WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="f79c2-135">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="f79c2-136">WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f79c2-136">You can find the full WSL install instructions [here](./install-win10.md).</span></span>