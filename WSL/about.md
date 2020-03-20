---
title: Windows Subsystem for Linux の詳細
description: Windows Subsystem for Linux のしくみについて説明します。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: fbb1ce5cf5d5c83e25d0a6a0cece7b70537a44a1
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200199"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="d91fd-104">Windows Subsystem for Linux に関するドキュメント</span><span class="sxs-lookup"><span data-stu-id="d91fd-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="d91fd-105">Windows Subsystem for Linux を使用すると、開発者は、仮想マシンのオーバーヘッドなしで、ほとんどのコマンド ライン ツール、ユーティリティ、アプリケーションを含む GNU/Linux 環境を変更せずそのまま Windows 上で直接実行できます。</span><span class="sxs-lookup"><span data-stu-id="d91fd-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="d91fd-106">次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="d91fd-106">You can:</span></span>

1. <span data-ttu-id="d91fd-107">[Microsoft Store から](https://aka.ms/wslstore)好みの GNU/Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d91fd-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="d91fd-108">`grep`、`sed`、`awk` などの一般的なコマンド ライン無料ソフトウェアや、その他の ELF-64 バイナリを実行します。</span><span class="sxs-lookup"><span data-stu-id="d91fd-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="d91fd-109">以下のような Bash シェル スクリプトや GNU/Linux コマンド ライン アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="d91fd-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="d91fd-110">ツール: vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="d91fd-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="d91fd-111">言語:Javascript/node.js、Ruby、Python、C/C++、 C# および F#、Rust、Go など</span><span class="sxs-lookup"><span data-stu-id="d91fd-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="d91fd-112">サービス: sshd、MySQL、Apache、lighttpd</span><span class="sxs-lookup"><span data-stu-id="d91fd-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="d91fd-113">独自の GNU/Linux ディストリビューション パッケージ マネージャーを使用して、追加のソフトウェアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d91fd-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="d91fd-114">Unix に似たコマンド ライン シェルを使用して Windows アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="d91fd-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="d91fd-115">Windows で GNU/Linux アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="d91fd-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="d91fd-116">はじめに</span><span class="sxs-lookup"><span data-stu-id="d91fd-116">Getting Started</span></span>

* [<span data-ttu-id="d91fd-117">Windows 10 に Linux をインストールする</span><span class="sxs-lookup"><span data-stu-id="d91fd-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="d91fd-118">コマンド リファレンスを参照する</span><span class="sxs-lookup"><span data-stu-id="d91fd-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="d91fd-119">よく寄せられる質問を読む</span><span class="sxs-lookup"><span data-stu-id="d91fd-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="d91fd-120">チームのブログ</span><span class="sxs-lookup"><span data-stu-id="d91fd-120">Team Blogs</span></span>
*  [<span data-ttu-id="d91fd-121">ビデオとブログのコレクションを含む概要の投稿</span><span class="sxs-lookup"><span data-stu-id="d91fd-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="d91fd-122">[コマンド ラインに関するブログ](https://blogs.msdn.microsoft.com/commandline/) (アクティブ)</span><span class="sxs-lookup"><span data-stu-id="d91fd-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="d91fd-123">[Windows Subsystem for Linux に関するブログ](https://blogs.msdn.microsoft.com/wsl/) (履歴)</span><span class="sxs-lookup"><span data-stu-id="d91fd-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="d91fd-124">投稿と記事</span><span class="sxs-lookup"><span data-stu-id="d91fd-124">Posts & Articles</span></span>
* [<span data-ttu-id="d91fd-125">Bash on Ubuntu on Windows の実行</span><span class="sxs-lookup"><span data-stu-id="d91fd-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="d91fd-126">開発者は Windows 10 で Bash およびユーザー モード Ubuntu Linux バイナリを実行可能</span><span class="sxs-lookup"><span data-stu-id="d91fd-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="d91fd-127">Windows 上の Ubuntu - Windows 開発者向けの Ubuntu ユーザー空間</span><span class="sxs-lookup"><span data-stu-id="d91fd-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="d91fd-128">ご意見とご感想</span><span class="sxs-lookup"><span data-stu-id="d91fd-128">Provide Feedback</span></span>
* [<span data-ttu-id="d91fd-129">GitHub の問題の追跡ツール</span><span class="sxs-lookup"><span data-stu-id="d91fd-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

