---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0220d642854f9fc7fe2a85357ad2e70e0b888ed8
ms.sourcegitcommit: f878e88921d36e01e32624a9c60ee9de3d706a2e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "69620098"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="71b6a-104">WSL 2 のインストール手順</span><span class="sxs-lookup"><span data-stu-id="71b6a-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="71b6a-105">WSL 2 をインストールして使用を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="71b6a-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="71b6a-106">WSL がインストールされていることを確認します (この手順については[こちら](./install-win10.md)を参照してください)。また、Windows 10 ビルド18917以降を実行していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="71b6a-106">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 build 18917 or higher</span></span>
- <span data-ttu-id="71b6a-107">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="71b6a-107">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="71b6a-108">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="71b6a-108">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="71b6a-109">現在のディストリビューションが使用している WSL のバージョンを確認する</span><span class="sxs-lookup"><span data-stu-id="71b6a-109">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="71b6a-110">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="71b6a-110">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="71b6a-111">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="71b6a-111">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="71b6a-112">これらの変更を有効にした後、コンピューターを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71b6a-112">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="71b6a-113">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="71b6a-113">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="71b6a-114">PowerShell で、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="71b6a-114">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="71b6a-115">`<Distro>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="71b6a-115">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="71b6a-116">(これらは、コマンド `wsl -l` を使用して確認できます)。</span><span class="sxs-lookup"><span data-stu-id="71b6a-116">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="71b6a-117">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="71b6a-117">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="71b6a-118">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="71b6a-118">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="71b6a-119">これにより、インストールする新しいディストリビューションはすべて WSL 2 ディストリビューションとして初期化されます。</span><span class="sxs-lookup"><span data-stu-id="71b6a-119">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="71b6a-120">現在のディストリビューションが使用している WSL のバージョンを確認して終了する</span><span class="sxs-lookup"><span data-stu-id="71b6a-120">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="71b6a-121">各ディストリビューションでどのバージョンの WSL が使用されているかを確認するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="71b6a-121">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="71b6a-122">`wsl --list --verbose` または `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="71b6a-122">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="71b6a-123">上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="71b6a-123">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="71b6a-124">これで、WSL 2 ディストリビューションを自由に使い始めることができます。</span><span class="sxs-lookup"><span data-stu-id="71b6a-124">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="71b6a-125">トラブルシューティング:</span><span class="sxs-lookup"><span data-stu-id="71b6a-125">Troubleshooting:</span></span> 

<span data-ttu-id="71b6a-126">WSL2 のインストール時の関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="71b6a-126">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="71b6a-127">その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71b6a-127">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="71b6a-128">**インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**</span><span class="sxs-lookup"><span data-stu-id="71b6a-128">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="71b6a-129">コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="71b6a-129">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="71b6a-130">これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。</span><span class="sxs-lookup"><span data-stu-id="71b6a-130">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="71b6a-131">**アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="71b6a-131">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="71b6a-132">Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="71b6a-132">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="71b6a-133">WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="71b6a-133">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="71b6a-134">WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71b6a-134">You can find the full WSL install instructions [here](./install-win10.md).</span></span>