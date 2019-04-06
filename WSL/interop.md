---
title: Linux と Windows の相互運用
description: Linux 用 Windows サブシステムで実行されている Linux ディストリビューションでは、Windows の相互運用性をについて説明します。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063250"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="7dc37-103">Windows と Linux の相互運用性用 Windows サブシステム</span><span class="sxs-lookup"><span data-stu-id="7dc37-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> **<span data-ttu-id="7dc37-104">For Fall Creators Update が更新されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-104">Updated for Fall Creators Update.</span></span>**  
<span data-ttu-id="7dc37-105">Creators Update または Anniversary Update を実行している場合にジャンプ、 [Creators/Anniversary Update セクション](interop.md#creators-update-and-anniversary-update)します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="7dc37-106">Windows Subsystem for Linux (WSL) は、Windows と Linux 間の統合を継続的に向上です。</span><span class="sxs-lookup"><span data-stu-id="7dc37-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="7dc37-107">可能な代替手段としては以下の方法があります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-107">You can:</span></span>

1. <span data-ttu-id="7dc37-108">Linux コンソールから Windows バイナリを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="7dc37-109">Windows コンソールから Linux 向けのバイナリを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="7dc37-110">**Windows Insider のビルド 17063 +** Linux と Windows 環境変数を共有します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="7dc37-111">これは、Windows と WSL の間のシームレスなエクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="7dc37-112">技術的な詳細は、 [WSL ブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="7dc37-113">Windows コマンドラインから Linux ツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="7dc37-114">Windows コマンド プロンプト (CMD または PowerShell) を使用して、Linux のバイナリを実行する`wsl.exe <command>`します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="7dc37-115">バイナリをこの方法で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="7dc37-116">現在の CMD または PowerShell プロンプトとして同じ作業ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="7dc37-117">WSL の既定のユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="7dc37-118">呼び出し元のプロセスとターミナルとして同じ Windows 管理者権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="7dc37-119">次に、例を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="7dc37-120">Linux コマンド次`wsl.exe`WSL で実行する任意のコマンドのように処理されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="7dc37-121">Sudo、パイプ、およびファイルのリダイレクトなどの機能は、次の動作します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="7dc37-122">Sudo の使用例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="7dc37-123">WSL と Windows のコマンドを混在させる例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="7dc37-124">渡されるコマンド`wsl.exe`変更しなくても、WSL プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="7dc37-125">WSL 形式でファイル パスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="7dc37-126">パスの例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="7dc37-127">WSL から Windows ツールを実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="7dc37-128">WSL が使用して、WSL コマンドラインから直接 Windows バイナリを呼び出すことができます`[binary name].exe`します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="7dc37-129">たとえば、`notepad.exe` と記述します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="7dc37-130">Linux の Windows 実行可能ファイルを簡単に実行させるには、Windows のパスが含まれている`$PATH`Fall Creators Update でします。</span><span class="sxs-lookup"><span data-stu-id="7dc37-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="7dc37-131">この方法で実行するアプリケーションでは、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="7dc37-132">WSL のコマンド プロンプトとして作業ディレクトリを保持 (ほとんどの場合--例外について以下に説明)。</span><span class="sxs-lookup"><span data-stu-id="7dc37-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="7dc37-133">WSL プロセスと同じアクセス許可権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="7dc37-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="7dc37-134">アクティブな Windows ユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="7dc37-135">Windows タスク マネージャーに表示される場合に、コマンド プロンプトから直接実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="7dc37-136">以下に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="7dc37-137">WSL で実行、Windows 実行可能ファイルは、ネイティブの Linux 実行可能ファイル: リダイレクトのパイプとも想定どおりに作業するバック グラウンド処理を同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="7dc37-138">パイプを使用する例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="7dc37-139">Windows と WSL の混在のコマンドを使用する例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="7dc37-140">Windows バイナリでは、ファイル拡張子を含める、ファイルの場合も、一致、および実行可能する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="7dc37-141">などの非-実行可能ファイルは、スクリプトをバッチ処理します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="7dc37-142">などのネイティブ コマンドを CMD`dir`で実行できる`cmd.exe /C`コマンド。</span><span class="sxs-lookup"><span data-stu-id="7dc37-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="7dc37-143">例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="7dc37-144">パラメーターは、変更されていない Windows バイナリに渡されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="7dc37-145">次のコマンドを開く例として、`C:\temp\foo.txt`で`notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="7dc37-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="7dc37-146">VolFs 上にあるファイルの変更 (ファイルのない`/mnt/<x>`) WSL でのアプリケーションはサポートされていません、Windows とします。</span><span class="sxs-lookup"><span data-stu-id="7dc37-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="7dc37-147">既定では、WSL バイナリ WSL の現在のディレクトリとして、Windows の作業ディレクトリを保持しようとするは代替インスタンス作成のディレクトリで VolFs 作業ディレクトリがある場合。</span><span class="sxs-lookup"><span data-stu-id="7dc37-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="7dc37-148">たとえば;`wsl.exe`が最初に起動される`C:\temp`され、現在の WSL ディレクトリは、ユーザーのホームに変更されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="7dc37-149">ときに`notepad.exe`と呼ばれますが、ユーザーのホーム ディレクトリから WSL に自動的に戻ります`C:\temp`notepad.exe の作業ディレクトリとして。</span><span class="sxs-lookup"><span data-stu-id="7dc37-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="7dc37-150">Windows と WSL の間の環境変数を共有します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="7dc37-151">Windows Insider ビルド 17063 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="7dc37-152">WSL にアクセスできる Windows 環境変数のみが 17063、前に`PATH`(したがって、WSL 下から Win32 実行可能ファイルを起動する可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="7dc37-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="7dc37-153">17063 以降、WSL と Windows 共有`WSLENV`、特殊な環境変数が WSL で実行されている Windows と Linux のディストリビューションをブリッジするために作成します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="7dc37-154">プロパティの`WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="7dc37-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="7dc37-155">共有します。これは、Windows と WSL の両方の環境に存在します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="7dc37-156">これは、Windows と WSL 間で共有する環境変数の一覧です。</span><span class="sxs-lookup"><span data-stu-id="7dc37-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="7dc37-157">Windows と WSL で問題なく動作する環境変数を書式設定できます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="7dc37-158">使用できる 4 つのフラグがあります`WSLENV`その環境変数が変換される方法に影響を与える。</span><span class="sxs-lookup"><span data-stu-id="7dc37-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

`WSLENV` <span data-ttu-id="7dc37-159">フラグ:</span><span class="sxs-lookup"><span data-stu-id="7dc37-159">flags:</span></span>

* `/p` <span data-ttu-id="7dc37-160">-WSL/Linux 形式のパスと Win32 のパスの間のパスを変換します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-160">- translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* `/l` <span data-ttu-id="7dc37-161">-環境変数がパスの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-161">- indicates the environment variable is a list of paths.</span></span>
* `/u` <span data-ttu-id="7dc37-162">-Win32 から WSL を実行する場合にこの環境変数を含めるだけあることを示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-162">- indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* `/w` <span data-ttu-id="7dc37-163">-WSL から Win32 を実行する場合にこの環境変数を含めるだけあることを示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-163">- indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="7dc37-164">必要に応じて、フラグを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="7dc37-165">相互運用機能を無効にします。</span><span class="sxs-lookup"><span data-stu-id="7dc37-165">Disable Interop</span></span>

<span data-ttu-id="7dc37-166">ユーザーには、ルートとして、次のコマンドを実行して、単一の WSL セッションの Windows バイナリを実行する機能が無効にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="7dc37-167">Windows を再度有効にするには、バイナリ WSL のすべてのセッションを終了し、bash.exe を再実行またはルートとして次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="7dc37-168">WSL セッション間で相互運用機能を無効化は永続化されません--新しいセッションを起動するときに、相互運用機能を再度有効になります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="7dc37-169">Creators Update と Anniversary Update</span><span class="sxs-lookup"><span data-stu-id="7dc37-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="7dc37-170">相互運用エクスペリエンスの事前 Fall Creators Update は、相互運用機能の最新のエクスペリエンスに似ていますが、中には、handfull の主な相違点があります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handfull of major differences.</span></span>

<span data-ttu-id="7dc37-171">要約。</span><span class="sxs-lookup"><span data-stu-id="7dc37-171">To summarize:</span></span>

* `bash.exe` <span data-ttu-id="7dc37-172">非推奨とされ、置き換え`wsl.exe`します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-172">has been deprecated and replaced with `wsl.exe`.</span></span>
* `-c` <span data-ttu-id="7dc37-173">オプションでは必要ありません、1 つのコマンドを実行しているを`wsl.exe`します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-173">option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="7dc37-174">Windows のパスが、WSL に含まれる</span><span class="sxs-lookup"><span data-stu-id="7dc37-174">Windows path is included in the WSL</span></span> `$PATH`

<span data-ttu-id="7dc37-175">相互運用機能を無効にするためのプロセスは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7dc37-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="7dc37-176">WSL Windows コマンドラインからの呼び出し</span><span class="sxs-lookup"><span data-stu-id="7dc37-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="7dc37-177">Linux のバイナリは、Windows コマンド プロンプトから、または PowerShell から起動できます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="7dc37-178">この方法で呼び出されたバイナリの次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="7dc37-179">CMD または PowerShell プロンプトとして同じ作業ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="7dc37-180">WSL の既定のユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="7dc37-181">呼び出し元のプロセスとターミナルとして同じ Windows 管理者権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="7dc37-182">以下に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="7dc37-183">この方法で呼び出す Linux コマンドは、その他の Windows アプリケーションのように処理されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="7dc37-184">入力、パイプ、およびファイルのリダイレクトなどは、期待どおりに動作します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="7dc37-185">例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-185">Examples:</span></span>

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

<span data-ttu-id="7dc37-186">渡される WSL コマンド`bash -c`変更しなくても、WSL プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="7dc37-187">WSL 形式でファイル パスを指定する必要があり、関連する文字をエスケープする注意おく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="7dc37-188">以下に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="7dc37-189">WSL から呼び出し元の Windows バイナリ</span><span class="sxs-lookup"><span data-stu-id="7dc37-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="7dc37-190">Windows Subsystem for Linux は、WSL コマンドラインから直接 Windows バイナリを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="7dc37-191">この方法で実行するアプリケーションでは、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7dc37-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="7dc37-192">以下で説明するシナリオでは除く WSL コマンド プロンプトとして作業ディレクトリを保持します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="7dc37-193">同じアクセス許可権限を持ち、`bash.exe`プロセス。</span><span class="sxs-lookup"><span data-stu-id="7dc37-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="7dc37-194">アクティブな Windows ユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="7dc37-195">Windows タスク マネージャーに表示される場合に、コマンド プロンプトから直接実行します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="7dc37-196">以下に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="7dc37-197">WSL では、この実行可能ファイルはネイティブの Linux の実行可能ファイルのような処理されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="7dc37-198">これは、Linux パスにディレクトリを追加して、期待どおりのコマンド間でパイプを意味します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="7dc37-199">例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="7dc37-200">Windows バイナリは、ファイル拡張子を含めるし、ファイルの場合も、一致、実行可能します。</span><span class="sxs-lookup"><span data-stu-id="7dc37-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="7dc37-201">などの非-実行可能ファイルのバッチのスクリプトおよびコマンドのような`dir`で実行できる`/mnt/c/Windows/System32/cmd.exe /C`コマンド。</span><span class="sxs-lookup"><span data-stu-id="7dc37-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="7dc37-202">例:</span><span class="sxs-lookup"><span data-stu-id="7dc37-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="7dc37-203">パラメーターは、変更されていない Windows バイナリに渡されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="7dc37-204">次のコマンドを開く例として、`C:\temp\foo.txt`で`notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="7dc37-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="7dc37-205">VolFs 上にあるファイルの変更 (ファイルのない`/mnt/<x>`)、Windows のアプリケーションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7dc37-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="7dc37-206">既定では、WSL バイナリ WSL の現在のディレクトリとして、Windows の作業ディレクトリを保持しようは代替インスタンス作成のディレクトリの作業ディレクトリが VolFs にある場合。</span><span class="sxs-lookup"><span data-stu-id="7dc37-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="7dc37-207">たとえば;`bash.exe`が最初に起動される`C:\temp`され、現在の WSL ディレクトリは、ユーザーのホームに変更されます。</span><span class="sxs-lookup"><span data-stu-id="7dc37-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="7dc37-208">ときに`notepad.exe`と呼ばれますが、ユーザーのホーム ディレクトリから WSL に自動的に戻ります`C:\temp`notepad.exe の作業ディレクトリとして。</span><span class="sxs-lookup"><span data-stu-id="7dc37-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
