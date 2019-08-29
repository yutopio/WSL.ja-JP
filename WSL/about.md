---
title: Windows Subsystem for Linux の詳細
description: Windows Subsystem for Linux の動作の詳細については、こちらを参照してください。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、gnu、linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c8e3b3f7ec13109485d7efa29739dadc8bfacf7
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122668"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="77af9-104">Linux 用 Windows サブシステムのドキュメント</span><span class="sxs-lookup"><span data-stu-id="77af9-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="77af9-105">Windows Subsystem for Linux を使用すると、開発者は、ほとんどのコマンドラインツール、ユーティリティ、アプリケーションを含む GNU/Linux 環境を、変更されていない状態で、仮想マシンのオーバーヘッドなしで、Windows 上で直接実行できます。</span><span class="sxs-lookup"><span data-stu-id="77af9-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="77af9-106">可能な代替手段としては以下の方法があります。</span><span class="sxs-lookup"><span data-stu-id="77af9-106">You can:</span></span>

1. <span data-ttu-id="77af9-107">[Microsoft Store から、使い慣れた](https://aka.ms/wslstore)GNU/Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="77af9-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="77af9-108">、、 `sed`、またはその他の ELF-64 バイナリなどの一般的なコマンドラインフリーソフトウェアを実行します。 `awk` `grep`</span><span class="sxs-lookup"><span data-stu-id="77af9-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="77af9-109">次のような Bash シェルスクリプトと GNU/Linux コマンドラインアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="77af9-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="77af9-110">ツール: vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="77af9-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="77af9-111">言語：Javascript/node.js、Ruby、Python、C/C++、 C# & F#、Rust、ゴーなど。</span><span class="sxs-lookup"><span data-stu-id="77af9-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="77af9-112">サービス: sshd、MySQL、Apache、ライト tpd</span><span class="sxs-lookup"><span data-stu-id="77af9-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="77af9-113">独自の GNU/Linux ディストリビューションパッケージマネージャーを使用して、追加のソフトウェアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="77af9-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="77af9-114">Unix に似たコマンドラインシェルを使用して Windows アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="77af9-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="77af9-115">Windows で GNU/Linux アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="77af9-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="77af9-116">作業の開始</span><span class="sxs-lookup"><span data-stu-id="77af9-116">Getting Started</span></span>

* [<span data-ttu-id="77af9-117">Windows 10 に Linux をインストールする</span><span class="sxs-lookup"><span data-stu-id="77af9-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="77af9-118">コマンドリファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77af9-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="77af9-119">よく寄せられる質問を読む</span><span class="sxs-lookup"><span data-stu-id="77af9-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="77af9-120">チームのブログ</span><span class="sxs-lookup"><span data-stu-id="77af9-120">Team Blogs</span></span>
*  [<span data-ttu-id="77af9-121">ビデオとブログのコレクションを使用した投稿の概要</span><span class="sxs-lookup"><span data-stu-id="77af9-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="77af9-122">[コマンドラインのブログ](https://blogs.msdn.microsoft.com/commandline/)能動的</span><span class="sxs-lookup"><span data-stu-id="77af9-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="77af9-123">[Linux 用 Windows サブシステムのブログ](https://blogs.msdn.microsoft.com/wsl/)経緯</span><span class="sxs-lookup"><span data-stu-id="77af9-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="77af9-124">投稿 & 記事</span><span class="sxs-lookup"><span data-stu-id="77af9-124">Posts & Articles</span></span>
* [<span data-ttu-id="77af9-125">Windows で Bash on Ubuntu を実行する</span><span class="sxs-lookup"><span data-stu-id="77af9-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="77af9-126">開発者は Windows 10 で Bash およびモード Ubuntu Linux バイナリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="77af9-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="77af9-127">Windows 上の ubuntu – Windows 開発者向けの Ubuntu</span><span class="sxs-lookup"><span data-stu-id="77af9-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="77af9-128">ご意見とご感想</span><span class="sxs-lookup"><span data-stu-id="77af9-128">Provide Feedback</span></span>
* [<span data-ttu-id="77af9-129">GitHub の問題の追跡ツール</span><span class="sxs-lookup"><span data-stu-id="77af9-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="77af9-130">コマンドライン UserVoice ポータル</span><span class="sxs-lookup"><span data-stu-id="77af9-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
