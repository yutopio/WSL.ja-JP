---
title: Linux 用 Windows サブシステムについて
description: Linux 用 Windows サブシステムのさまざまなバージョンやそれらの使用方法などについて説明します。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 07/21/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: c468f501894df9dfde4323471a6d20569ac82e9c
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2020
ms.locfileid: "88865965"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a><span data-ttu-id="2df1c-104">Linux 用 Windows サブシステムとは</span><span class="sxs-lookup"><span data-stu-id="2df1c-104">What is the Windows Subsystem for Linux?</span></span>

<span data-ttu-id="2df1c-105">Linux 用 Windows サブシステムを使用すると、開発者は、従来の仮想マシンまたはデュアルブート セットアップのオーバーヘッドなしで、ほとんどのコマンド ライン ツール、ユーティリティ、アプリケーションを含む GNU/Linux 環境を変更せずそのまま Windows 上で直接実行できます。</span><span class="sxs-lookup"><span data-stu-id="2df1c-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a traditional virtual machine or dualboot setup.</span></span>

<span data-ttu-id="2df1c-106">次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="2df1c-106">You can:</span></span>

* <span data-ttu-id="2df1c-107">[Microsoft Store から](https://aka.ms/wslstore)好みの GNU/Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2df1c-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
* <span data-ttu-id="2df1c-108">`grep`、`sed`、`awk` などの一般的なコマンドライン ツールや、その他の ELF-64 バイナリを実行します。</span><span class="sxs-lookup"><span data-stu-id="2df1c-108">Run common command-line tools such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span>
* <span data-ttu-id="2df1c-109">以下のような Bash シェル スクリプトや GNU/Linux コマンド ライン アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="2df1c-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="2df1c-110">ツール: vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="2df1c-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="2df1c-111">言語:[Node.js](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2)、JavaScript、[Python](https://docs.microsoft.com/windows/python/web-frameworks)、Ruby、C/C++、C# & F#、Rust、Go など</span><span class="sxs-lookup"><span data-stu-id="2df1c-111">Languages: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="2df1c-112">サービス:SSHD、[MySQL](./tutorials/wsl-database.md)、Apache、lighttpd、[MongoDB](./tutorials/wsl-database.md)、[PostgreSQL](./tutorials/wsl-database.md)。</span><span class="sxs-lookup"><span data-stu-id="2df1c-112">Services: SSHD, [MySQL](./tutorials/wsl-database.md), Apache, lighttpd, [MongoDB](./tutorials/wsl-database.md), [PostgreSQL](./tutorials/wsl-database.md).</span></span>
* <span data-ttu-id="2df1c-113">独自の GNU/Linux ディストリビューション パッケージ マネージャーを使用して、追加のソフトウェアをインストールします。</span><span class="sxs-lookup"><span data-stu-id="2df1c-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
* <span data-ttu-id="2df1c-114">Unix に似たコマンド ライン シェルを使用して Windows アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="2df1c-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
* <span data-ttu-id="2df1c-115">Windows で GNU/Linux アプリケーションを起動します。</span><span class="sxs-lookup"><span data-stu-id="2df1c-115">Invoke GNU/Linux applications on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="2df1c-116">WSL をインストールする</span><span class="sxs-lookup"><span data-stu-id="2df1c-116">Install WSL</span></span>](install-win10.md)

<br>

> [!VIDEO https://www.youtube.com/embed/48k317kOxqg]

## <a name="what-is-wsl-2"></a><span data-ttu-id="2df1c-117">WSL 2 とは</span><span class="sxs-lookup"><span data-stu-id="2df1c-117">What is WSL 2?</span></span>

<span data-ttu-id="2df1c-118">WSL 2 は、Linux 用 Windows サブシステムが Windows 上で ELF64 Linux バイナリを実行できるようにする、Linux 用 Windows サブシステム アーキテクチャの新しいバージョンです。</span><span class="sxs-lookup"><span data-stu-id="2df1c-118">WSL 2 is a new version of the Windows Subsystem for Linux architecture that powers the Windows Subsystem for Linux to run ELF64 Linux binaries on Windows.</span></span> <span data-ttu-id="2df1c-119">その主な目標は、**ファイル システムのパフォーマンスを向上させること**と、**システム コールの完全な互換性**を追加することです。</span><span class="sxs-lookup"><span data-stu-id="2df1c-119">Its primary goals are to **increase file system performance**, as well as adding **full system call compatibility**.</span></span>

<span data-ttu-id="2df1c-120">この新しいアーキテクチャによって、こうした Linux バイナリと、Windows やお使いのコンピューターのハードウェアとの対話方法は変わりますが、ユーザー エクスペリエンスは WSL 1 (現在幅広く利用されているバージョン) と同じです。</span><span class="sxs-lookup"><span data-stu-id="2df1c-120">This new architecture changes how these Linux binaries interact with Windows and your computer's hardware, but still provides the same user experience as in WSL 1 (the current widely available version).</span></span>

<span data-ttu-id="2df1c-121">個々の Linux ディストリビューションは、WSL 1 または WSL 2 アーキテクチャで実行できます。</span><span class="sxs-lookup"><span data-stu-id="2df1c-121">Individual Linux distributions can be run with either the WSL 1 or WSL 2 architecture.</span></span> <span data-ttu-id="2df1c-122">各ディストリビューションはいつでもアップグレードまたはダウングレードできます。また、WSL 1 ディストリビューションと WSL 2 ディストリビューションをサイド バイ サイドで実行することができます。</span><span class="sxs-lookup"><span data-stu-id="2df1c-122">Each distribution can be upgraded or downgraded at any time and you can run WSL 1 and WSL 2 distributions side by side.</span></span> <span data-ttu-id="2df1c-123">WSL 2 には、実際の Linux カーネルを実行することによるメリットが得られるまったく新しいアーキテクチャが使用されています。</span><span class="sxs-lookup"><span data-stu-id="2df1c-123">WSL 2 uses an entirely new architecture that benefits from running a real Linux kernel.</span></span>

<br>

> [!VIDEO https://www.youtube.com/embed/MrZolfGm8Zk]

## <a name="next-steps"></a><span data-ttu-id="2df1c-124">次の手順</span><span class="sxs-lookup"><span data-stu-id="2df1c-124">Next steps</span></span>

* [<span data-ttu-id="2df1c-125">WSL 1 をインストールし、WSL 2 に更新する</span><span class="sxs-lookup"><span data-stu-id="2df1c-125">Install WSL 1 and update to WSL 2</span></span>](./install-win10.md)

* [<span data-ttu-id="2df1c-126">WSL 2 と WSL 1 を比較する</span><span class="sxs-lookup"><span data-stu-id="2df1c-126">Compare WSL 2 and WSL 1</span></span>](./compare-versions.md)

* [<span data-ttu-id="2df1c-127">新しい Linux ディストリビューションのユーザー アカウントとパスワードを作成する</span><span class="sxs-lookup"><span data-stu-id="2df1c-127">Create a user account and password for your new Linux distribution</span></span>](./user-support.md)

* [<span data-ttu-id="2df1c-128">よく寄せられる質問を読む</span><span class="sxs-lookup"><span data-stu-id="2df1c-128">Read Frequently Asked Questions</span></span>](./faq.md)

* [<span data-ttu-id="2df1c-129">WSL 2 に関してよく寄せられる質問を読む</span><span class="sxs-lookup"><span data-stu-id="2df1c-129">Read Frequently Asked Questions about WSL 2</span></span>](./wsl2-faq.md)

* [<span data-ttu-id="2df1c-130">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2df1c-130">Troubleshooting</span></span>](./troubleshooting.md)

* [<span data-ttu-id="2df1c-131">Windows と Linux の間で相互運用性コマンドを実行する</span><span class="sxs-lookup"><span data-stu-id="2df1c-131">Run interoperability commands between Windows and Linux</span></span>](./interop.md)

* [<span data-ttu-id="2df1c-132">起動コマンドと構成を実行する</span><span class="sxs-lookup"><span data-stu-id="2df1c-132">Run launch commands and configurations</span></span>](./wsl-config.md)

* [<span data-ttu-id="2df1c-133">ファイルのアクセス許可を設定する</span><span class="sxs-lookup"><span data-stu-id="2df1c-133">Set up file permissions</span></span>](./file-permissions.md)

* [<span data-ttu-id="2df1c-134">エンタープライズ向けの WSL を設定する</span><span class="sxs-lookup"><span data-stu-id="2df1c-134">Set up WSL for Enterprise</span></span>](./enterprise.md)

* [<span data-ttu-id="2df1c-135">WSL コマンドのリファレンスを見る</span><span class="sxs-lookup"><span data-stu-id="2df1c-135">Reference WSL commands</span></span>](./reference.md)

* [<span data-ttu-id="2df1c-136">カスタム ディストリビューションを作成する</span><span class="sxs-lookup"><span data-stu-id="2df1c-136">Build a custom distributions</span></span>](./build-custom-distro.md)

* [<span data-ttu-id="2df1c-137">WSL のリリース ノートを読む</span><span class="sxs-lookup"><span data-stu-id="2df1c-137">Read the WSL Release Notes</span></span>](./release-notes.md)
