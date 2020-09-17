---
title: WSL 用のカスタム Linux ディストリビューションを構築する
description: Windows Subsystem for Linux のカスタム Linux ディストリビューションを作成する方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows サブシステム、ディストリビューション、カスタム
ms.date: 09/15/2020
ms.topic: article
ms.openlocfilehash: 8b898cbee12aaff6e575afbeaa57d52c3a2c9e75
ms.sourcegitcommit: ba3399a5ffeffd23551315acd04ea6848d30693b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2020
ms.locfileid: "90719151"
---
# <a name="creating-a-custom-linux-distribution-for-wsl"></a><span data-ttu-id="72214-104">WSL 用のカスタム Linux ディストリビューションの作成</span><span class="sxs-lookup"><span data-stu-id="72214-104">Creating a Custom Linux Distribution for WSL</span></span>

<span data-ttu-id="72214-105">オープンソースの WSL サンプルを使用して、Microsoft Store 用の WSL ディストリビューションパッケージを構築したり、サイドローディング用のカスタム Linux ディストリビューションパッケージを作成したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="72214-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="72214-106">[ディストリビューションランチャーリポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)は GitHub で入手できます。</span><span class="sxs-lookup"><span data-stu-id="72214-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="72214-107">このプロジェクトでは、次のことが可能です。</span><span class="sxs-lookup"><span data-stu-id="72214-107">This project enables:</span></span>

- <span data-ttu-id="72214-108">Linux ディストリビューションの管理パックは、WSL で実行される appx として Linux ディストリビューションをパッケージ化して送信します。</span><span class="sxs-lookup"><span data-stu-id="72214-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
- <span data-ttu-id="72214-109">開発者が開発用コンピューターにサイドロードできるカスタム Linux ディストリビューションを作成する</span><span class="sxs-lookup"><span data-stu-id="72214-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="72214-110">背景</span><span class="sxs-lookup"><span data-stu-id="72214-110">Background</span></span>

<span data-ttu-id="72214-111">Microsoft Store を通じて、WSL 用の Linux ディストリビューションを UWP アプリケーションとして配布します。</span><span class="sxs-lookup"><span data-stu-id="72214-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="72214-112">これらのアプリケーションは、WSL-Windows カーネル内にあるサブシステムで実行できます。</span><span class="sxs-lookup"><span data-stu-id="72214-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="72214-113">この配信メカニズムには、 [前のブログ記事](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)で説明したように多くの利点があります。</span><span class="sxs-lookup"><span data-stu-id="72214-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="72214-114">カスタム Linux ディストリビューションパッケージのサイドローディング</span><span class="sxs-lookup"><span data-stu-id="72214-114">Sideloading a Custom Linux Distro Package</span></span>

<span data-ttu-id="72214-115">カスタム Linux ディストリビューションパッケージをアプリケーションとして作成し、パーソナルコンピューターでサイドロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="72214-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="72214-116">配布のメンテナンスツールとして送信しない限り、カスタムパッケージは Microsoft Store を通じて配布されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="72214-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="72214-117">アプリをサイドロードするようにコンピューターを設定するには、[開発者向け] の [システム設定] でこれを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="72214-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="72214-118">開発者モードまたはサイドロードアプリが選択されていることを確認してください</span><span class="sxs-lookup"><span data-stu-id="72214-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="72214-119">Linux ディストリビューションの場合</span><span class="sxs-lookup"><span data-stu-id="72214-119">For Linux Distro Maintainers</span></span>

<span data-ttu-id="72214-120">ストアに送信するには、発行の承認を受けるために microsoft と協力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72214-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="72214-121">ディストリビューションを Microsoft Store に追加することに関心がある Linux ディストリビューションの所有者は、にお問い合わせください wslpartners@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="72214-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="72214-122">作業の開始</span><span class="sxs-lookup"><span data-stu-id="72214-122">Getting Started</span></span>

<span data-ttu-id="72214-123">[ディストリビューションランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)の指示に従って、カスタム Linux ディストリビューションパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="72214-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

## <a name="team-blogs"></a><span data-ttu-id="72214-124">チームのブログ</span><span class="sxs-lookup"><span data-stu-id="72214-124">Team Blogs</span></span>

-  [<span data-ttu-id="72214-125">Linux ディストリビューションの WSL サンプルをオープンソーシングカスタム Linux ディストリビューションの展開とサイドローディング</span><span class="sxs-lookup"><span data-stu-id="72214-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
- [<span data-ttu-id="72214-126">コマンドラインのブログ</span><span class="sxs-lookup"><span data-stu-id="72214-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="72214-127">フィードバックの提供</span><span class="sxs-lookup"><span data-stu-id="72214-127">Provide Feedback</span></span>

- [<span data-ttu-id="72214-128">ディストリビューションランチャー GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="72214-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
- [<span data-ttu-id="72214-129">GitHub issue tracker for WSL</span><span class="sxs-lookup"><span data-stu-id="72214-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
- [<span data-ttu-id="72214-130">コマンド ライン UserVoice ポータル</span><span class="sxs-lookup"><span data-stu-id="72214-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
