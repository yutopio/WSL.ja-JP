---
title: Linux との Windows の相互運用性
description: Windows Subsystem for Linux で実行されている Linux ディストリビューションとの Windows の相互運用性について説明します。
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f8b0150c044f5011b84e80cac4befd752c4dc552
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269804"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="da5e2-103">Windows との Windows Subsystem for Linux の相互運用性</span><span class="sxs-lookup"><span data-stu-id="da5e2-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="da5e2-104">**Fall Creators Update 向けに更新されました。**</span><span class="sxs-lookup"><span data-stu-id="da5e2-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="da5e2-105">Creators Update または Anniversary Update を実行している場合は、[Creators/Anniversary Update に関するセクション](interop.md#creators-update-and-anniversary-update)に移動してください。</span><span class="sxs-lookup"><span data-stu-id="da5e2-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="da5e2-106">Windows Subsystem for Linux (WSL) は、Windows と Linux 間の統合を継続的に向上させています。</span><span class="sxs-lookup"><span data-stu-id="da5e2-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="da5e2-107">次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="da5e2-107">You can:</span></span>

1. <span data-ttu-id="da5e2-108">Linux コンソールから Windows バイナリを起動します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="da5e2-109">Windows コンソールから Linux バイナリを起動します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="da5e2-110">**Windows Insiders Build 17063 以降**では、Linux と Windows の間で環境変数を共有します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="da5e2-111">これにより、Windows と WSL の間でシームレスなエクスペリエンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="da5e2-112">技術的な詳細については、[WSL のブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="da5e2-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="da5e2-113">Windows コマンド ラインからの Linux ツールの実行</span><span class="sxs-lookup"><span data-stu-id="da5e2-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="da5e2-114">`wsl.exe <command>` を使用して、Windows コマンド プロンプト (CMD または PowerShell) から Linux バイナリを実行します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="da5e2-115">この方法で起動されるバイナリには、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="da5e2-116">現在の CMD または PowerShell プロンプトと同じ作業ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="da5e2-117">WSL の既定のユーザーとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="da5e2-118">呼び出し元のプロセスおよびターミナルと同じ Windows 管理者権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="da5e2-119">たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="da5e2-120">`wsl.exe` の後の Linux コマンドは、WSL での任意のコマンド実行と同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="da5e2-121">sudo、パイプ処理、ファイル リダイレクトなどが機能します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="da5e2-122">sudo を使用した例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="da5e2-123">WSL コマンドと Windows コマンドを組み合わせた例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="da5e2-124">`wsl.exe` に渡されるコマンドは、変更なしで WSL プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="da5e2-125">ファイル パスは WSL 形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="da5e2-126">パスを指定した例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="da5e2-127">WSL からの Windows ツールの実行</span><span class="sxs-lookup"><span data-stu-id="da5e2-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="da5e2-128">WSL では、`[binary name].exe` を使用して、WSL コマンド ラインから Windows バイナリを直接起動することができます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="da5e2-129">たとえば、`notepad.exe` のように指定します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="da5e2-130">Windows 実行可能ファイルの実行を容易にするために、Fall Creators Update では Windows のパスは Linux `$PATH` に含まれています。</span><span class="sxs-lookup"><span data-stu-id="da5e2-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="da5e2-131">この方法で実行されるアプリケーションには、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="da5e2-132">ほとんどの場合、作業ディレクトリを WSL コマンド プロンプトとして保持します (例外については後述します)。</span><span class="sxs-lookup"><span data-stu-id="da5e2-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="da5e2-133">WSL プロセスと同じアクセス許可権限が与えられています。</span><span class="sxs-lookup"><span data-stu-id="da5e2-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="da5e2-134">アクティブな Windows ユーザーとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="da5e2-135">CMD プロンプトから直接実行されたかのように、Windows タスク マネージャーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="da5e2-136">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="da5e2-137">WSL で実行される Windows 実行可能ファイルは、ネイティブの Linux 実行可能ファイルと同様に処理されます。パイプ処理、リダイレクト、さらにバックグラウンド処理も想定どおりに機能します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="da5e2-138">パイプを使用した例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="da5e2-139">Windows コマンドと WSL コマンドの組み合わせを使用した例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="da5e2-140">Windows バイナリは、ファイル拡張子を含み、ファイルの大文字と小文字が一致し、実行可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="da5e2-141">非実行可能ファイルにはバッチ スクリプトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="da5e2-142">`dir` などの CMD ネイティブ コマンドは、`cmd.exe /C` コマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="da5e2-143">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="da5e2-144">パラメーターは、変更されずに Windows バイナリに渡されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="da5e2-145">たとえば、次のコマンドによって `notepad.exe` で `C:\temp\foo.txt` が開きます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="da5e2-146">WSL の Windows アプリケーションを使用して、VolFs にあるファイル (`/mnt/<x>` の下にないファイル) を変更することはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="da5e2-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="da5e2-147">既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻ります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="da5e2-148">たとえば、`wsl.exe` が最初に `C:\temp` から起動され、現在の WSL ディレクトリがユーザーのホームに変更されているとします。</span><span class="sxs-lookup"><span data-stu-id="da5e2-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="da5e2-149">`notepad.exe` がユーザーのホーム ディレクトリからが呼び出されると、WSL は notepad.exe の作業ディレクトリとして `C:\temp` に自動的に戻ります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="da5e2-150">Windows と WSL の間での環境変数の共有</span><span class="sxs-lookup"><span data-stu-id="da5e2-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="da5e2-151">Windows Insider Build 17063 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="da5e2-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="da5e2-152">17063 より前では、WSL がアクセスできる唯一の Windows 環境変数は `PATH` でした (そのため、WSL で Win32 実行可能ファイルを起動できました)。</span><span class="sxs-lookup"><span data-stu-id="da5e2-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="da5e2-153">17063 以降、WSL と Windows は `WSLENV` を共有します。これは、WSL で実行される Windows と Linux のディストリビューションをつなぐために作成された特殊な環境変数です。</span><span class="sxs-lookup"><span data-stu-id="da5e2-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="da5e2-154">`WSLENV` の特性:</span><span class="sxs-lookup"><span data-stu-id="da5e2-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="da5e2-155">共有され、Windows と WSL の両方の環境に存在します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="da5e2-156">Windows と WSL の間で共有する環境変数の一覧です。</span><span class="sxs-lookup"><span data-stu-id="da5e2-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="da5e2-157">Windows と WSL で適切に機能するように環境変数をフォーマットできます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="da5e2-158">環境変数の変換方法に影響する、`WSLENV` で利用可能な 4 つのフラグがあります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="da5e2-159">`WSLENV` のフラグ:</span><span class="sxs-lookup"><span data-stu-id="da5e2-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="da5e2-160">`/p` - WSL/Linux スタイル パスと Win32 パスの間でパスを変換します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="da5e2-161">`/l` - 環境変数がパスのリストであることを示します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="da5e2-162">`/u` - Win32 から WSL を実行する場合にのみ、この環境変数を含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="da5e2-163">`/w` - WSL から Win32 を実行する場合にのみ、この環境変数を含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="da5e2-164">フラグは、必要に応じて組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="da5e2-165">相互運用の無効化</span><span class="sxs-lookup"><span data-stu-id="da5e2-165">Disable Interop</span></span>

<span data-ttu-id="da5e2-166">ユーザーは、ルートとして次のコマンドを実行することで、1 つの WSL セッションに対して Windows バイナリを実行する機能を無効にできます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="da5e2-167">Windows バイナリを再び有効にするには、すべての WSL セッションを終了して bash.exe を再実行するか、ルートとして次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="da5e2-168">相互運用の無効化は、WSL セッション間で保持されません。新しいセッションが開始されると、相互運用は再び有効になります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="da5e2-169">Creators Update と Anniversary Update</span><span class="sxs-lookup"><span data-stu-id="da5e2-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="da5e2-170">Fall Creators Update 以前の相互運用エクスペリエンスは、より新しい相互運用エクスペリエンスに似ていますが、いくつかの大きな違いがあります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="da5e2-171">要約すると、以下のようになります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-171">To summarize:</span></span>

* <span data-ttu-id="da5e2-172">`bash.exe` は非推奨となり、`wsl.exe` に置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="da5e2-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="da5e2-173">1 つのコマンドを実行する場合の `-c` オプションは、`wsl.exe` で必要ありません。</span><span class="sxs-lookup"><span data-stu-id="da5e2-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="da5e2-174">Windows パスは WSL `$PATH` に含まれています。</span><span class="sxs-lookup"><span data-stu-id="da5e2-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="da5e2-175">相互運用を無効にするプロセスは変更されていません。</span><span class="sxs-lookup"><span data-stu-id="da5e2-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="da5e2-176">Windows コマンド ラインからの WSL の起動</span><span class="sxs-lookup"><span data-stu-id="da5e2-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="da5e2-177">Linux バイナリは、Windows コマンド プロンプトまたは PowerShell から起動できます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="da5e2-178">この方法で起動されるバイナリには、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="da5e2-179">CMD または PowerShell プロンプトと同じ作業ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="da5e2-180">WSL の既定のユーザーとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="da5e2-181">呼び出し元のプロセスおよびターミナルと同じ Windows 管理者権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="da5e2-182">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="da5e2-183">この方法で呼び出された Linux コマンドは、他の Windows アプリケーションと同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="da5e2-184">sudo、パイプ処理、ファイル リダイレクトなどが想定どおりに機能します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="da5e2-185">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-185">Examples:</span></span>

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

<span data-ttu-id="da5e2-186">`bash -c` に渡される WSL コマンドは、変更なしで WSL プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="da5e2-187">ファイル パスは WSL 形式で指定する必要があり、関連文字をエスケープするように注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="da5e2-188">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="da5e2-189">WSL からの Windows バイナリの起動</span><span class="sxs-lookup"><span data-stu-id="da5e2-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="da5e2-190">Windows Subsystem for Linux では、WSL コマンド ラインから Windows バイナリを直接起動することができます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="da5e2-191">この方法で実行されるアプリケーションには、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="da5e2-192">作業ディレクトリを WSL コマンド プロンプトとして保持します。ただし、以降で説明するシナリオを除きます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="da5e2-193">`bash.exe` プロセスと同じアクセス許可権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="da5e2-194">アクティブな Windows ユーザーとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="da5e2-195">CMD プロンプトから直接実行されたかのように、Windows タスク マネージャーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="da5e2-196">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="da5e2-197">WSL では、これらの実行可能ファイルはネイティブの Linux 実行可能ファイルと同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="da5e2-198">これは、Linux パスへのディレクトリの追加や、コマンド間でのパイプ処理が想定どおりに機能することを意味します。</span><span class="sxs-lookup"><span data-stu-id="da5e2-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="da5e2-199">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="da5e2-200">Windows バイナリは、ファイル拡張子を含み、ファイルの大文字と小文字が一致し、実行可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="da5e2-201">バッチ スクリプトや `dir` などのコマンドを含む非実行可能ファイルは、`/mnt/c/Windows/System32/cmd.exe /C` コマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="da5e2-202">例:</span><span class="sxs-lookup"><span data-stu-id="da5e2-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="da5e2-203">パラメーターは、変更されずに Windows バイナリに渡されます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="da5e2-204">たとえば、次のコマンドによって `notepad.exe` で `C:\temp\foo.txt` が開きます。</span><span class="sxs-lookup"><span data-stu-id="da5e2-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="da5e2-205">Windows アプリケーションを使用して、VolFs にあるファイル (`/mnt/<x>` の下にないファイル) を変更することはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="da5e2-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="da5e2-206">既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻ります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="da5e2-207">たとえば、`bash.exe` が最初に `C:\temp` から起動され、現在の WSL ディレクトリがユーザーのホームに変更されているとします。</span><span class="sxs-lookup"><span data-stu-id="da5e2-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="da5e2-208">`notepad.exe` がユーザーのホーム ディレクトリからが呼び出されると、WSL は notepad.exe の作業ディレクトリとして `C:\temp` に自動的に戻ります。</span><span class="sxs-lookup"><span data-stu-id="da5e2-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
