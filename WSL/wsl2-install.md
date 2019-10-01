---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 386b6793f00300bc9dabd1613cfd69b19d222f0b
ms.sourcegitcommit: eb7b572388c6bddbf6e8ad8d01927660fe66aecf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2019
ms.locfileid: "71692462"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="9b1c8-104">WSL 2 のインストール手順</span><span class="sxs-lookup"><span data-stu-id="9b1c8-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="9b1c8-105">WSL 2 をインストールして使用を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="9b1c8-106">WSL 2 は、Windows 10 ビルド18917以降でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="9b1c8-107">WSL がインストールされていることを確認します (この手順については[こちら](./install-win10.md)を参照してください)。また、Windows 10**ビルド 18917**以降を実行していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="9b1c8-108">ビルド18917以降を使用していることを確認するには[、Windows Insider プログラムに](https://insider.windows.com/en-us/)参加して、"高速" リングを選択してください。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="9b1c8-109">Windows のバージョンを確認するには、コマンドプロンプトを開き`ver` 、コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="9b1c8-110">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="9b1c8-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="9b1c8-111">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="9b1c8-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="9b1c8-112">現在のディストリビューションが使用している WSL のバージョンを確認する</span><span class="sxs-lookup"><span data-stu-id="9b1c8-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="9b1c8-113">' 仮想マシンプラットフォーム ' オプションのコンポーネントを有効にし、WSL が有効になっていることを確認してください</span><span class="sxs-lookup"><span data-stu-id="9b1c8-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="9b1c8-114">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-114">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="9b1c8-115">これにより、仮想マシンプラットフォームと Linux 用 Windows サブシステムのオプションコンポーネントの両方がインストールされます。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-115">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="9b1c8-116">これらのコマンドを実行したら、コンピューターを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-116">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="9b1c8-117">コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="9b1c8-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="9b1c8-118">PowerShell で、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-118">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="9b1c8-119">`<Distro>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-119">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="9b1c8-120">(これらは、コマンド `wsl -l` を使用して確認できます)。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-120">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="9b1c8-121">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-121">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="9b1c8-122">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-122">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="9b1c8-123">これにより、インストールする新しいディストリビューションはすべて WSL 2 ディストリビューションとして初期化されます。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-123">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="9b1c8-124">現在のディストリビューションが使用している WSL のバージョンを確認して終了する</span><span class="sxs-lookup"><span data-stu-id="9b1c8-124">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="9b1c8-125">各ディストリビューションでどのバージョンの WSL が使用されているかを確認するには、次のコマンドを使用します (Windows ビルド18917以降でのみ使用できます)。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-125">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="9b1c8-126">`wsl --list --verbose` または `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="9b1c8-126">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="9b1c8-127">上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-127">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="9b1c8-128">これで、WSL 2 ディストリビューションを自由に使い始めることができます。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-128">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="9b1c8-129">トラブルシューティング:</span><span class="sxs-lookup"><span data-stu-id="9b1c8-129">Troubleshooting:</span></span> 

<span data-ttu-id="9b1c8-130">WSL2 のインストール時の関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-130">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="9b1c8-131">その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-131">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="9b1c8-132">**インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**</span><span class="sxs-lookup"><span data-stu-id="9b1c8-132">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="9b1c8-133">コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-133">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="9b1c8-134">これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-134">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="9b1c8-135">**アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="9b1c8-135">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="9b1c8-136">Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-136">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="9b1c8-137">WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-137">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="9b1c8-138">WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b1c8-138">You can find the full WSL install instructions [here](./install-win10.md).</span></span>