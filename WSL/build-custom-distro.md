---
title: WSL 用、カスタムの Linux ディストリビューションでのビルドします。
description: Linux 用 Windows サブシステムのカスタムの Linux ディストリビューションを作成する方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows サブシステム、ディストリビューション、カスタム
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040776"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="44ab0-104">WSL のカスタムの Linux ディストリビューションの作成</span><span class="sxs-lookup"><span data-stu-id="44ab0-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="44ab0-105">Microsoft Store の WSL ディストリビューションのパッケージをビルドおよびサイドロード用のカスタムの Linux ディストリビューションのパッケージを作成する、オープン ソース WSL サンプルを使用します。</span><span class="sxs-lookup"><span data-stu-id="44ab0-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="44ab0-106">検索することができます、[ディストリビューション ランチャー リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)GitHub でします。</span><span class="sxs-lookup"><span data-stu-id="44ab0-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="44ab0-107">このプロジェクトが有効にします。</span><span class="sxs-lookup"><span data-stu-id="44ab0-107">This project enables:</span></span>
* <span data-ttu-id="44ab0-108">パッケージ化し、として、appx WSL で実行されている Linux ディストリビューションを送信する Linux ディストリビューションのメンテナンス</span><span class="sxs-lookup"><span data-stu-id="44ab0-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="44ab0-109">開発者は開発用コンピューターにサイドロードできるカスタムの Linux ディストリビューションの作成</span><span class="sxs-lookup"><span data-stu-id="44ab0-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="44ab0-110">背景</span><span class="sxs-lookup"><span data-stu-id="44ab0-110">Background</span></span>
<span data-ttu-id="44ab0-111">Microsoft Store 経由での UWP アプリケーションとして WSL の Linux ディストリビューションを配布します。</span><span class="sxs-lookup"><span data-stu-id="44ab0-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="44ab0-112">WSL - Windows カーネルに配置されるサブシステムで実行し、それらのアプリケーションをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="44ab0-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="44ab0-113">説明したように、この配信メカニズムによって多くの利点があります、[以前ブログの投稿](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)します。</span><span class="sxs-lookup"><span data-stu-id="44ab0-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="44ab0-114">カスタムの Linux ディストリビューションのパッケージのサイドロード</span><span class="sxs-lookup"><span data-stu-id="44ab0-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="44ab0-115">パーソナル コンピューターにサイドローディングするアプリケーションとして、カスタムの Linux ディストリビューションのパッケージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="44ab0-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="44ab0-116">カスタム パッケージは配布されません Microsoft Store を介して配布 maintainer として送信する場合を除きに注意してください。</span><span class="sxs-lookup"><span data-stu-id="44ab0-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="44ab0-117">アプリをサイドロードするコンピューターを設定するには"For Developers"の下のシステム設定でこれを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="44ab0-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="44ab0-118">開発者モード、または選択したアプリのサイドロードをいずれかが必要</span><span class="sxs-lookup"><span data-stu-id="44ab0-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="44ab0-119">Linux ディストリビューションで、管理者や</span><span class="sxs-lookup"><span data-stu-id="44ab0-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="44ab0-120">ストアに送信するには発行の承認を受信するという点で協力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44ab0-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="44ab0-121">Microsoft Store へのお使いのディストリビューションの追加対象の Linux ディストリビューションの所有者は場合に、お問い合わせくださいwslpartners@microsoft.comします。</span><span class="sxs-lookup"><span data-stu-id="44ab0-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="44ab0-122">作業の開始</span><span class="sxs-lookup"><span data-stu-id="44ab0-122">Getting Started</span></span>
<span data-ttu-id="44ab0-123">指示に従って、[ディストリビューション ランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)カスタム Linux ディストリビューションのパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="44ab0-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="44ab0-124">チームのブログ</span><span class="sxs-lookup"><span data-stu-id="44ab0-124">Team Blogs</span></span>
*  [<span data-ttu-id="44ab0-125">Linux ディストリビューションのメンテナンスとサイドローディング カスタム Linux ディストリビューション用の WSL サンプルのソーシングを開く</span><span class="sxs-lookup"><span data-stu-id="44ab0-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="44ab0-126">コマンド ラインのブログ</span><span class="sxs-lookup"><span data-stu-id="44ab0-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="44ab0-127">ご意見とご感想</span><span class="sxs-lookup"><span data-stu-id="44ab0-127">Provide Feedback</span></span>
* [<span data-ttu-id="44ab0-128">ディストリビューションの起動ツールの GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="44ab0-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="44ab0-129">WSL の GitHub の issue トラッカー</span><span class="sxs-lookup"><span data-stu-id="44ab0-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="44ab0-130">コマンド ライン UserVoice ポータル</span><span class="sxs-lookup"><span data-stu-id="44ab0-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
