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
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063260"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="1d5b7-104">WSL のカスタムの Linux ディストリビューションの作成</span><span class="sxs-lookup"><span data-stu-id="1d5b7-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="1d5b7-105">Microsoft Store の WSL ディストリビューションのパッケージをビルドおよびサイドロード用のカスタムの Linux ディストリビューションのパッケージを作成する、オープン ソース WSL サンプルを使用します。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="1d5b7-106">検索することができます、[ディストリビューション ランチャー リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)GitHub でします。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="1d5b7-107">このプロジェクトが有効にします。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-107">This project enables:</span></span>
* <span data-ttu-id="1d5b7-108">パッケージ化し、として、appx WSL で実行されている Linux ディストリビューションを送信する Linux ディストリビューションのメンテナンス</span><span class="sxs-lookup"><span data-stu-id="1d5b7-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="1d5b7-109">開発者は開発用コンピューターにサイドロードできるカスタムの Linux ディストリビューションの作成</span><span class="sxs-lookup"><span data-stu-id="1d5b7-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="1d5b7-110">背景</span><span class="sxs-lookup"><span data-stu-id="1d5b7-110">Background</span></span>
<span data-ttu-id="1d5b7-111">Microsoft Store 経由での UWP アプリケーションとして WSL の Linux ディストリビューションを配布します。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="1d5b7-112">WSL - Windows カーネルに配置されるサブシステムで実行し、それらのアプリケーションをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="1d5b7-113">この配信メカニズムは、以前のブログ投稿で説明したように、多くのメリットが。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-113">This delivery mechanism has many benefits as discussed in an earlier blog post.</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="1d5b7-114">カスタムの Linux ディストリビューションのパッケージのサイドロード</span><span class="sxs-lookup"><span data-stu-id="1d5b7-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="1d5b7-115">パーソナル コンピューターにサイドローディングするアプリケーションとして、カスタムの Linux ディストリビューションのパッケージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="1d5b7-116">カスタム パッケージは配布されません Microsoft Store を介して配布 maintainer として送信する場合を除きに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="1d5b7-117">アプリをサイドロードするコンピューターを設定するには"For Developers"の下のシステム設定でこれを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="1d5b7-118">開発者モード、または選択したアプリのサイドロードをいずれかが必要</span><span class="sxs-lookup"><span data-stu-id="1d5b7-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="1d5b7-119">Linux ディストリビューションで、管理者や</span><span class="sxs-lookup"><span data-stu-id="1d5b7-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="1d5b7-120">ストアに送信するには発行の承認を受信するという点で協力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="1d5b7-121">Microsoft Store へのお使いのディストリビューションの追加対象の Linux ディストリビューションの所有者は場合に、お問い合わせくださいwslpartners@microsoft.comします。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="1d5b7-122">作業の開始</span><span class="sxs-lookup"><span data-stu-id="1d5b7-122">Getting Started</span></span>
<span data-ttu-id="1d5b7-123">指示に従って、[ディストリビューション ランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)カスタム Linux ディストリビューションのパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="1d5b7-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="1d5b7-124">チームのブログ</span><span class="sxs-lookup"><span data-stu-id="1d5b7-124">Team Blogs</span></span>
*  [<span data-ttu-id="1d5b7-125">Linux ディストリビューションのメンテナンスとサイドローディング カスタム Linux ディストリビューション用の WSL サンプルのソーシングを開く</span><span class="sxs-lookup"><span data-stu-id="1d5b7-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="1d5b7-126">コマンド ラインのブログ</span><span class="sxs-lookup"><span data-stu-id="1d5b7-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="1d5b7-127">ご意見とご感想</span><span class="sxs-lookup"><span data-stu-id="1d5b7-127">Provide Feedback</span></span>
* [<span data-ttu-id="1d5b7-128">ディストリビューション ランチャー Gitub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="1d5b7-128">Distro Launcher Gitub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="1d5b7-129">WSL の GitHub の issue トラッカー</span><span class="sxs-lookup"><span data-stu-id="1d5b7-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="1d5b7-130">コマンド ライン UserVoice ポータル</span><span class="sxs-lookup"><span data-stu-id="1d5b7-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
