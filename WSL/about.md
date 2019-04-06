---
title: Linux 用 Windows サブシステムについて説明します
description: Windows Subsystem for Linux が動作する方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、gnu、linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: a9c8d32f2b87319b45b1b757b4d71c0a4c41292c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063510"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="93b22-104">Linux のドキュメント用の Windows サブシステム</span><span class="sxs-lookup"><span data-stu-id="93b22-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="93b22-105">Windows Subsystem for Linux では、Windows、未変更の状態で仮想マシンのオーバーヘッドなしで直接開発者のほとんどのコマンド ライン ツール、ユーティリティ、およびアプリケーションを含む--Gnu/linux 環境を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="93b22-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="93b22-106">可能な代替手段としては以下の方法があります。</span><span class="sxs-lookup"><span data-stu-id="93b22-106">You can:</span></span>

1. <span data-ttu-id="93b22-107">お気に入りの GNU/Linux ディストリビューションを選択[Windows ストアから](https://aka.ms/wslstore)します。</span><span class="sxs-lookup"><span data-stu-id="93b22-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="93b22-108">一般的なコマンド ライン無料のソフトウェアを実行します。 `grep`、 `sed`、 `awk`、またはその他の ELF 64 バイナリ。</span><span class="sxs-lookup"><span data-stu-id="93b22-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="93b22-109">Bash シェル スクリプトとを含む Gnu/linux コマンド ライン アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="93b22-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="93b22-110">ツール: vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="93b22-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="93b22-111">言語：Javascript/node.js、Ruby、Python、C/C++、 C# & F#、信頼、移動など。</span><span class="sxs-lookup"><span data-stu-id="93b22-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="93b22-112">サービス: sshd、MySQL、Apache、lighttpd</span><span class="sxs-lookup"><span data-stu-id="93b22-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="93b22-113">独自の GNU/Linux 配布パッケージ マネージャーを使用して追加のソフトウェアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="93b22-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="93b22-114">Unix のようなコマンド ライン シェルを使用して Windows アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="93b22-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="93b22-115">Windows 上の Gnu/linux アプリケーションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="93b22-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="93b22-116">概要</span><span class="sxs-lookup"><span data-stu-id="93b22-116">Getting started</span></span>

* [<span data-ttu-id="93b22-117">Windows 上の Linux をインストールします。</span><span class="sxs-lookup"><span data-stu-id="93b22-117">Install Linux on Windows</span></span>](install_guide.md)
* [<span data-ttu-id="93b22-118">コマンドのリファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93b22-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="93b22-119">読み取りについてよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="93b22-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="93b22-120">チームのブログ</span><span class="sxs-lookup"><span data-stu-id="93b22-120">Team Blogs</span></span>
*  [<span data-ttu-id="93b22-121">ビデオとブログのコレクションでの概要の投稿</span><span class="sxs-lookup"><span data-stu-id="93b22-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="93b22-122">[コマンド ライン ブログ](https://blogs.msdn.microsoft.com/commandline/)(アクティブ)</span><span class="sxs-lookup"><span data-stu-id="93b22-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="93b22-123">[Linux ブログ用 Windows サブシステム](https://blogs.msdn.microsoft.com/wsl/)(履歴)</span><span class="sxs-lookup"><span data-stu-id="93b22-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="93b22-124">投稿と記事</span><span class="sxs-lookup"><span data-stu-id="93b22-124">Posts & Articles</span></span>
* [<span data-ttu-id="93b22-125">Bash on Ubuntu on Windows の実行</span><span class="sxs-lookup"><span data-stu-id="93b22-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="93b22-126">開発者は Windows 10 の Bash と Usermode Ubuntu Linux のバイナリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="93b22-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="93b22-127">Ubuntu on Windows: Windows 開発者向けの Ubuntu 空間</span><span class="sxs-lookup"><span data-stu-id="93b22-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="93b22-128">ご意見とご感想</span><span class="sxs-lookup"><span data-stu-id="93b22-128">Provide Feedback</span></span>
* [<span data-ttu-id="93b22-129">GitHub の issue トラッカー</span><span class="sxs-lookup"><span data-stu-id="93b22-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="93b22-130">コマンド ライン UserVoice ポータル</span><span class="sxs-lookup"><span data-stu-id="93b22-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
