---
title: WSL 2 をインストールします。
description: WSL 2 のインストール手順
keywords: BashOnWindows、bash、wsl、wsl2、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステムのインストールします。
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038082"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="a6035-104">WSL 2 のインストール手順</span><span class="sxs-lookup"><span data-stu-id="a6035-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="a6035-105">インストールして開始には、WSL 2 は、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="a6035-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="a6035-106">'仮想マシン プラットフォーム' オプションのコンポーネントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a6035-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="a6035-107">WSL 2 のコマンドラインを使用してバックアップするディストリビューションを設定します。</span><span class="sxs-lookup"><span data-stu-id="a6035-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="a6035-108">使用している WSL、ディストリビューションのバージョン確認します。</span><span class="sxs-lookup"><span data-stu-id="a6035-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="a6035-109">'仮想マシン プラットフォーム' オプションのコンポーネントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a6035-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="a6035-110">管理者として PowerShell を開きを実行します。</span><span class="sxs-lookup"><span data-stu-id="a6035-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="a6035-111">これらの変更が有効にした後、コンピューターを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6035-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="a6035-112">WSL 2 のコマンドラインを使用してバックアップするディストリビューションを設定します。</span><span class="sxs-lookup"><span data-stu-id="a6035-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="a6035-113">Powershell を実行します。</span><span class="sxs-lookup"><span data-stu-id="a6035-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="a6035-114">置き換えてくださいと`<Distro>`ディストリビューションの実際の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a6035-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="a6035-115">(これらは、コマンドを使用して: `wsl -l`)。</span><span class="sxs-lookup"><span data-stu-id="a6035-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="a6035-116">上記と同じコマンドを実行して、' 2' で ' 1' に置き換えることによって WSL 1 にいつでも変更することができます。</span><span class="sxs-lookup"><span data-stu-id="a6035-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="a6035-117">さらに、WSL 2 に、既定のアーキテクチャを作成する場合は、これを行う次のコマンドで。</span><span class="sxs-lookup"><span data-stu-id="a6035-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="a6035-118">これにより、いずれかをインストールする新しいディストリビューション WSL 2 ディストリビューションとして初期化します。</span><span class="sxs-lookup"><span data-stu-id="a6035-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="a6035-119">使用している WSL、ディストリビューションのバージョンの確認が完了します。</span><span class="sxs-lookup"><span data-stu-id="a6035-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="a6035-120">次のコマンドを使用して、各ディストリビューションを使用して WSL のバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6035-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="a6035-121">`wsl --list --verbose` または `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="a6035-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="a6035-122">上の選択したディストリビューションは、'2'、'version' 列の下を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6035-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="a6035-123">完了したら、WSL 2 ディストリビューションを使用する自由!</span><span class="sxs-lookup"><span data-stu-id="a6035-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 