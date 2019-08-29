---
title: Windows と Linux の相互運用性
description: Windows Subsystem for Linux で実行されている Linux ディストリビューションとの Windows の相互運用性について説明します。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122731"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="7c90e-103">Windows と Linux の相互運用性のための windows サブシステム</span><span class="sxs-lookup"><span data-stu-id="7c90e-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="7c90e-104">**秋の作成者の更新に関する情報が更新されました。**</span><span class="sxs-lookup"><span data-stu-id="7c90e-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="7c90e-105">作成者の更新プログラムまたは記念日の更新プログラムを実行している場合は、[作成者[/記念日] セクション](interop.md#creators-update-and-anniversary-update)に移動します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="7c90e-106">Windows Subsystem for Linux (WSL) は、Windows と Linux 間の統合を継続的に改善しています。</span><span class="sxs-lookup"><span data-stu-id="7c90e-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="7c90e-107">可能な代替手段としては以下の方法があります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-107">You can:</span></span>

1. <span data-ttu-id="7c90e-108">Linux コンソールから Windows バイナリを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="7c90e-109">Windows コンソールから Linux バイナリを起動します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="7c90e-110">**Windows Insider ビルド 17063 +** Linux と Windows の間で環境変数を共有します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="7c90e-111">これにより、Windows と WSL の間でシームレスなエクスペリエンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="7c90e-112">技術的な詳細については、 [Wsl ブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="7c90e-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="7c90e-113">Windows コマンドラインからの Linux ツールの実行</span><span class="sxs-lookup"><span data-stu-id="7c90e-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="7c90e-114">を使用して`wsl.exe <command>`、Windows コマンドプロンプト (CMD または PowerShell) から Linux バイナリを実行します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="7c90e-115">バイナリは次の方法で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="7c90e-116">現在のコマンドプロンプトまたは PowerShell プロンプトと同じ作業ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="7c90e-117">WSL の既定のユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="7c90e-118">呼び出しプロセスとターミナルと同じ Windows 管理者権限を持っている。</span><span class="sxs-lookup"><span data-stu-id="7c90e-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="7c90e-119">以下に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="7c90e-120">次に示す`wsl.exe` Linux コマンドは、wsl でのコマンド実行と同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="7c90e-121">Sudo、パイプ、ファイルリダイレクトなどが機能します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="7c90e-122">Sudo を使用した例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="7c90e-123">WSL コマンドと Windows コマンドを混在させた例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="7c90e-124">に`wsl.exe`渡されるコマンドは、変更せずに wsl プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="7c90e-125">ファイルパスは WSL 形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="7c90e-126">パスを使用した例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="7c90e-127">WSL から Windows ツールを実行する</span><span class="sxs-lookup"><span data-stu-id="7c90e-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="7c90e-128">WSL は、を使用して`[binary name].exe`、wsl コマンドラインから直接 Windows バイナリを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="7c90e-129">たとえば、`notepad.exe` のようにします。</span><span class="sxs-lookup"><span data-stu-id="7c90e-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="7c90e-130">Windows の実行可能ファイルの実行を容易にするために、windows `$PATH`のパスは、Linux では、[作成者] の更新プログラムに含まれています。</span><span class="sxs-lookup"><span data-stu-id="7c90e-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="7c90e-131">この方法で実行されるアプリケーションには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="7c90e-132">作業ディレクトリを WSL コマンドプロンプトとして保持します (ほとんどの場合、例外については後述します)。</span><span class="sxs-lookup"><span data-stu-id="7c90e-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="7c90e-133">WSL プロセスと同じ権限が与えられている。</span><span class="sxs-lookup"><span data-stu-id="7c90e-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="7c90e-134">をアクティブな Windows ユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="7c90e-135">コマンドプロンプトから直接実行されたかのように、Windows タスクマネージャーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="7c90e-136">例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="7c90e-137">WSL で実行される Windows 実行可能ファイルは、ネイティブの Linux 実行可能ファイルと同様に処理されます (パイプ、リダイレクト、バックグラウンド処理が想定どおりに動作します)。</span><span class="sxs-lookup"><span data-stu-id="7c90e-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="7c90e-138">パイプを使用した例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="7c90e-139">混合ウィンドウと WSL コマンドを使用する例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="7c90e-140">Windows バイナリには、ファイル拡張子が含まれている必要があります。また、ファイルの大文字と小文字が一致している必要があります</span><span class="sxs-lookup"><span data-stu-id="7c90e-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="7c90e-141">バッチスクリプトを含む非実行可能ファイル。</span><span class="sxs-lookup"><span data-stu-id="7c90e-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="7c90e-142">コマンドを使用し`dir`て、の`cmd.exe /C`ような CMD ネイティブコマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="7c90e-143">例 :</span><span class="sxs-lookup"><span data-stu-id="7c90e-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="7c90e-144">パラメーターは、変更されていない Windows バイナリに渡されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="7c90e-145">例として、で`C:\temp\foo.txt` `notepad.exe`は次のコマンドが開きます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="7c90e-146">Wsl の Windows アプリケーションを使用して、 `/mnt/<x>`volfs (下にないファイル) にあるファイルを変更することはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7c90e-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="7c90e-147">既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="7c90e-148">例を次に示します。が最初に`C:\temp`起動され、現在の wsl ディレクトリがユーザーのホームに変更されます。 `wsl.exe`</span><span class="sxs-lookup"><span data-stu-id="7c90e-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="7c90e-149">ユーザー `notepad.exe`のホームディレクトリからが呼び出されると、wsl は notepad.exe 作業`C:\temp`ディレクトリとして自動的にに戻ります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="7c90e-150">Windows と WSL の間で環境変数を共有する</span><span class="sxs-lookup"><span data-stu-id="7c90e-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="7c90e-151">Windows Insider ビルド17063以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="7c90e-152">17063より前では、wsl がアクセスできる Windows 環境変数`PATH`のみが使用されていました (したがって、wsl の下から Win32 実行可能ファイルを起動できます)。</span><span class="sxs-lookup"><span data-stu-id="7c90e-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="7c90e-153">17063以降、wsl および windows share `WSLENV`は、wsl で実行される Windows および Linux ディストリビューションをブリッジするために作成された特殊な環境変数です。</span><span class="sxs-lookup"><span data-stu-id="7c90e-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="7c90e-154">次の`WSLENV`プロパティ:</span><span class="sxs-lookup"><span data-stu-id="7c90e-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="7c90e-155">これは共有されています。Windows と WSL の両方の環境に存在します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="7c90e-156">これは、Windows と WSL の間で共有する環境変数の一覧です。</span><span class="sxs-lookup"><span data-stu-id="7c90e-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="7c90e-157">環境変数の書式を設定して、Windows および WSL で適切に動作させることができます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="7c90e-158">で`WSLENV`は、環境変数の変換方法に影響を与える4つのフラグが用意されています。</span><span class="sxs-lookup"><span data-stu-id="7c90e-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="7c90e-159">`WSLENV`示す</span><span class="sxs-lookup"><span data-stu-id="7c90e-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="7c90e-160">`/p`-WSL/Linux スタイルパスと Win32 パス間のパスを変換します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="7c90e-161">`/l`-環境変数がパスのリストであることを示します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="7c90e-162">`/u`-Win32 から WSL を実行する場合にのみ、この環境変数を含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="7c90e-163">`/w`-WSL から Win32 を実行する場合にのみ、この環境変数を含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="7c90e-164">フラグは、必要に応じて組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="7c90e-165">相互運用を無効にする</span><span class="sxs-lookup"><span data-stu-id="7c90e-165">Disable Interop</span></span>

<span data-ttu-id="7c90e-166">ユーザーは、次のコマンドを root として実行することで、1つの WSL セッションに対して Windows バイナリを実行する機能を無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="7c90e-167">Windows バイナリを再び有効にするには、すべての WSL セッションを終了し、bash を再実行するか、ルートとして次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="7c90e-168">相互運用機能の無効化は、WSL セッション間では保持されません。新しいセッションが開始されると、相互運用が再び有効になります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="7c90e-169">作成者の更新プログラムと記念日の更新</span><span class="sxs-lookup"><span data-stu-id="7c90e-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="7c90e-170">相互運用機能の更新は、より新しい相互運用エクスペリエンスに似ていますが、いくつかの大きな違いがあります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="7c90e-171">要約すると、以下のようになります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-171">To summarize:</span></span>

* <span data-ttu-id="7c90e-172">`bash.exe`は非推奨とされ`wsl.exe`、に置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="7c90e-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="7c90e-173">`-c`で`wsl.exe`は、単一のコマンドを実行するオプションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="7c90e-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="7c90e-174">Windows パスは WSL に含まれています`$PATH`</span><span class="sxs-lookup"><span data-stu-id="7c90e-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="7c90e-175">相互運用を無効にするプロセスは変更されていません。</span><span class="sxs-lookup"><span data-stu-id="7c90e-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="7c90e-176">Windows コマンドラインからの WSL の呼び出し</span><span class="sxs-lookup"><span data-stu-id="7c90e-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="7c90e-177">Linux バイナリは、Windows コマンドプロンプトまたは PowerShell から呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="7c90e-178">この方法で呼び出されるバイナリには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="7c90e-179">CMD または PowerShell プロンプトと同じ作業ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="7c90e-180">WSL の既定のユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="7c90e-181">呼び出しプロセスとターミナルと同じ Windows 管理者権限を持っている。</span><span class="sxs-lookup"><span data-stu-id="7c90e-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="7c90e-182">例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="7c90e-183">この方法で呼び出された Linux コマンドは、他の Windows アプリケーションと同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="7c90e-184">入力、パイプ、ファイルリダイレクトなどが想定どおりに動作します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="7c90e-185">例 :</span><span class="sxs-lookup"><span data-stu-id="7c90e-185">Examples:</span></span>

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

<span data-ttu-id="7c90e-186">に`bash -c`渡される wsl コマンドは、変更せずに wsl プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="7c90e-187">ファイルパスは WSL 形式で指定する必要があり、関連する文字をエスケープするために注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="7c90e-188">例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="7c90e-189">WSL からの Windows バイナリの呼び出し</span><span class="sxs-lookup"><span data-stu-id="7c90e-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="7c90e-190">Windows Subsystem for Linux は、WSL コマンドラインから直接 Windows バイナリを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="7c90e-191">この方法で実行されるアプリケーションには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="7c90e-192">以下で説明するシナリオを除き、作業ディレクトリは WSL コマンドプロンプトとして保持してください。</span><span class="sxs-lookup"><span data-stu-id="7c90e-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="7c90e-193">`bash.exe`プロセスと同じ権限を持っている。</span><span class="sxs-lookup"><span data-stu-id="7c90e-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="7c90e-194">をアクティブな Windows ユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="7c90e-195">コマンドプロンプトから直接実行されたかのように、Windows タスクマネージャーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="7c90e-196">例:</span><span class="sxs-lookup"><span data-stu-id="7c90e-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="7c90e-197">WSL では、これらの実行可能ファイルはネイティブの Linux 実行可能ファイルと同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="7c90e-198">これは、Linux パスにディレクトリを追加し、コマンド間でパイプを使用して正常に動作することを意味します。</span><span class="sxs-lookup"><span data-stu-id="7c90e-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="7c90e-199">例 :</span><span class="sxs-lookup"><span data-stu-id="7c90e-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="7c90e-200">Windows バイナリには、ファイル拡張子が含まれている必要があります。ファイルの大文字と小文字の区別、および実行可能ファイルです。</span><span class="sxs-lookup"><span data-stu-id="7c90e-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="7c90e-201">バッチスクリプトやコマンド`dir`などを含む非実行可能ファイルは、コマンドを使用して`/mnt/c/Windows/System32/cmd.exe /C`実行できます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="7c90e-202">例 :</span><span class="sxs-lookup"><span data-stu-id="7c90e-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="7c90e-203">パラメーターは、変更されていない Windows バイナリに渡されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="7c90e-204">例として、で`C:\temp\foo.txt` `notepad.exe`は次のコマンドが開きます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="7c90e-205">Windows アプリケーションを使用して、volfs ( `/mnt/<x>`下にないファイル) にあるファイルを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="7c90e-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="7c90e-206">既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻されます。</span><span class="sxs-lookup"><span data-stu-id="7c90e-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="7c90e-207">例を次に示します。が最初に`C:\temp`起動され、現在の wsl ディレクトリがユーザーのホームに変更されます。 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="7c90e-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="7c90e-208">ユーザー `notepad.exe`のホームディレクトリからが呼び出されると、wsl は notepad.exe 作業`C:\temp`ディレクトリとして自動的にに戻ります。</span><span class="sxs-lookup"><span data-stu-id="7c90e-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
