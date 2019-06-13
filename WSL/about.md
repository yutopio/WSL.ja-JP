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
ms.localizationpriority: High
ms.openlocfilehash: f2df3c06d6c56aa8bc5a41ea9f075635b70c8685
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040808"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="ca268-104">Linux のドキュメント用の Windows サブシステム</span><span class="sxs-lookup"><span data-stu-id="ca268-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="ca268-105">Windows Subsystem for Linux では、Windows、未変更の状態で仮想マシンのオーバーヘッドなしで直接開発者のほとんどのコマンド ライン ツール、ユーティリティ、およびアプリケーションを含む--Gnu/linux 環境を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="ca268-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="ca268-106">可能な代替手段としては以下の方法があります。</span><span class="sxs-lookup"><span data-stu-id="ca268-106">You can:</span></span>

1. <span data-ttu-id="ca268-107">お気に入りの GNU/Linux ディストリビューションを選択[Windows ストアから](https://aka.ms/wslstore)します。</span><span class="sxs-lookup"><span data-stu-id="ca268-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="ca268-108">一般的なコマンド ライン無料のソフトウェアを実行します。 `grep`、 `sed`、 `awk`、またはその他の ELF 64 バイナリ。</span><span class="sxs-lookup"><span data-stu-id="ca268-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="ca268-109">Bash シェル スクリプトとを含む Gnu/linux コマンド ライン アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca268-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="ca268-110">ツール: vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="ca268-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="ca268-111">言語：Javascript/node.js、Ruby、Python、C/C++、 C# & F#、信頼、移動など。</span><span class="sxs-lookup"><span data-stu-id="ca268-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="ca268-112">サービス: sshd、MySQL、Apache、lighttpd</span><span class="sxs-lookup"><span data-stu-id="ca268-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="ca268-113">独自の GNU/Linux 配布パッケージ マネージャーを使用して追加のソフトウェアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="ca268-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="ca268-114">Unix のようなコマンド ライン シェルを使用して Windows アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="ca268-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="ca268-115">Windows 上の Gnu/linux アプリケーションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ca268-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="ca268-116">作業の開始</span><span class="sxs-lookup"><span data-stu-id="ca268-116">Getting Started</span></span>

* [<span data-ttu-id="ca268-117">Windows 10 上の Linux をインストールします。</span><span class="sxs-lookup"><span data-stu-id="ca268-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="ca268-118">コマンドのリファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca268-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="ca268-119">読み取りについてよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ca268-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="ca268-120">チームのブログ</span><span class="sxs-lookup"><span data-stu-id="ca268-120">Team Blogs</span></span>
*  [<span data-ttu-id="ca268-121">ビデオとブログのコレクションでの概要の投稿</span><span class="sxs-lookup"><span data-stu-id="ca268-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="ca268-122">[コマンド ライン ブログ](https://blogs.msdn.microsoft.com/commandline/)(アクティブ)</span><span class="sxs-lookup"><span data-stu-id="ca268-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="ca268-123">[Linux ブログ用 Windows サブシステム](https://blogs.msdn.microsoft.com/wsl/)(履歴)</span><span class="sxs-lookup"><span data-stu-id="ca268-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="ca268-124">投稿と記事</span><span class="sxs-lookup"><span data-stu-id="ca268-124">Posts & Articles</span></span>
* [<span data-ttu-id="ca268-125">実行の Bash on Ubuntu on Windows</span><span class="sxs-lookup"><span data-stu-id="ca268-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="ca268-126">開発者は Windows 10 の Bash と Usermode Ubuntu Linux のバイナリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ca268-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="ca268-127">Ubuntu on Windows: Windows 開発者向けの Ubuntu 空間</span><span class="sxs-lookup"><span data-stu-id="ca268-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="ca268-128">ご意見とご感想</span><span class="sxs-lookup"><span data-stu-id="ca268-128">Provide Feedback</span></span>
* [<span data-ttu-id="ca268-129">GitHub の issue トラッカー</span><span class="sxs-lookup"><span data-stu-id="ca268-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="ca268-130">コマンド ライン UserVoice ポータル</span><span class="sxs-lookup"><span data-stu-id="ca268-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
