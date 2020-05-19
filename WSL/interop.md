---
title: Linux との Windows の相互運用性
description: Windows Subsystem for Linux で実行されている Linux ディストリビューションとの Windows の相互運用性について説明します。
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: b1c7a64a86cf088159d1abee3b341328151428f6
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270846"
---
# <a name="windows-interoperability-with-linux"></a><span data-ttu-id="59a3b-103">Linux との Windows の相互運用性</span><span class="sxs-lookup"><span data-stu-id="59a3b-103">Windows interoperability with Linux</span></span>

<span data-ttu-id="59a3b-104">Windows Subsystem for Linux (WSL) は、Windows と Linux 間の統合を継続的に向上させています。</span><span class="sxs-lookup"><span data-stu-id="59a3b-104">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="59a3b-105">次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="59a3b-105">You can:</span></span>

* <span data-ttu-id="59a3b-106">Windows ツール (つまり、notepad.exe) を Linux コマンド ライン (つまり、Ubuntu) から実行する。</span><span class="sxs-lookup"><span data-stu-id="59a3b-106">Run Windows tools (ie. notepad.exe) from a Linux command line (ie. Ubuntu).</span></span>
* <span data-ttu-id="59a3b-107">Linux ツール (つまり、grep) を Windows コマンド ライン (つまり、PowerShell) から実行する。</span><span class="sxs-lookup"><span data-stu-id="59a3b-107">Run Linux tools (ie. grep) from a Windows command line (ie. PowerShell).</span></span>
* <span data-ttu-id="59a3b-108">Linux と Windows の間で環境変数を共有する。</span><span class="sxs-lookup"><span data-stu-id="59a3b-108">Share environment variables between Linux and Windows.</span></span> <span data-ttu-id="59a3b-109">(ビルド 17063 以降)</span><span class="sxs-lookup"><span data-stu-id="59a3b-109">(Build 17063+)</span></span>

> [!NOTE]
> <span data-ttu-id="59a3b-110">Creators Update (2017 年 10 月、ビルド 16299) または Anniversary Update (2016 年 8 月、ビルド 14393) を実行している場合は、「[Windows 10 の以前のバージョン](#earlier-versions-of-windows-10)」に進んでください。</span><span class="sxs-lookup"><span data-stu-id="59a3b-110">If you're running Creators Update (Oct 2017, Build 16299) or Anniversary Update (Aug 2016, Build 14393), jump to the [Earlier versions of Windows 10](#earlier-versions-of-windows-10).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="59a3b-111">Windows コマンド ラインからの Linux ツールの実行</span><span class="sxs-lookup"><span data-stu-id="59a3b-111">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="59a3b-112">`wsl <command>` (または `wsl.exe <command>`) を使用して、Windows コマンド プロンプト (CMD) または PowerShell から Linux バイナリを実行します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-112">Run Linux binaries from the Windows Command Prompt (CMD) or PowerShell using `wsl <command>` (or `wsl.exe <command>`).</span></span>

<span data-ttu-id="59a3b-113">たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-113">For example:</span></span>

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="59a3b-114">この方法で起動されるバイナリには、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-114">Binaries invoked in this way:</span></span>

* <span data-ttu-id="59a3b-115">現在の CMD または PowerShell プロンプトと同じ作業ディレクトリを使用します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-115">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
* <span data-ttu-id="59a3b-116">WSL の既定のユーザーとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-116">Run as the WSL default user.</span></span>
* <span data-ttu-id="59a3b-117">呼び出し元のプロセスおよびターミナルと同じ Windows 管理者権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-117">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="59a3b-118">`wsl` (または `wsl.exe`) に続く Linux コマンドは、WSL での任意のコマンド実行と同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-118">The Linux command following `wsl` (or `wsl.exe`) is handled like any command run in WSL.</span></span>  <span data-ttu-id="59a3b-119">sudo、パイプ処理、ファイル リダイレクトなどが機能します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-119">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="59a3b-120">sudo を使用して既定の Linux ディストリビューションを更新する例:</span><span class="sxs-lookup"><span data-stu-id="59a3b-120">Example using sudo to update your default Linux distribution:</span></span>

```powershell
C:\temp> wsl sudo apt-get update
```

<span data-ttu-id="59a3b-121">このコマンドを実行すると、既定の Linux ディストリビューションのユーザー名が一覧表示され、パスワードの入力を求められます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-121">Your default Linux distribution user name will be listed after running this command and you will be asked for your password.</span></span> <span data-ttu-id="59a3b-122">パスワードを正しく入力すると、ディストリビューションによって更新プログラムがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-122">After entering your password correctly, your distribution will download updates.</span></span>

## <a name="mixing-linux-and-windows-commands"></a><span data-ttu-id="59a3b-123">Linux と Windows のコマンドを組み合わせて使用する</span><span class="sxs-lookup"><span data-stu-id="59a3b-123">Mixing Linux and Windows commands</span></span>

<span data-ttu-id="59a3b-124">PowerShell を使用して Linux と Windows のコマンドを組み合わせて使用するいくつかの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-124">Here are a few examples of mixing Linux and Windows commands using PowerShell.</span></span>

<span data-ttu-id="59a3b-125">Linux コマンド `ls -la` を使用してファイルを一覧表示し、PowerShell コマンド `findstr` を使用して "git" を含む単語の結果をフィルター処理するには、次のようにコマンドを組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-125">To use the Linux command `ls -la` to list files and the PowerShell command `findstr` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
wsl ls -la | findstr "git"
```

<span data-ttu-id="59a3b-126">Linux コマンド `dir` を使用してファイルを一覧表示し、PowerShell コマンド `grep` を使用して "git" を含む単語の結果をフィルター処理するには、次のようにコマンドを組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-126">To use the PowerShell command `dir` to list files and the Linux command `grep` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
C:\temp> dir | wsl grep git
```

<span data-ttu-id="59a3b-127">Linux コマンド `ls -la` を使用してファイルを一覧表示し、PowerShell コマンド `> out.txt` を使用してその一覧を "out.txt" という名前のテキスト ファイルに出力するには、次のようにコマンドを組み合わせます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-127">To use the Linux command `ls -la` to list files and the PowerShell command `> out.txt` to print that list to a text file named "out.txt", combine the commands:</span></span>

```powershell
C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="59a3b-128">`wsl.exe` に渡されるコマンドは、変更なしで WSL プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-128">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="59a3b-129">ファイル パスは WSL 形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-129">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="59a3b-130">PowerShell を使用して、Linux コマンド `ls -la` を使用して `/proc/cpuinfo` Linux ファイル システム パス内のファイルを一覧表示するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="59a3b-130">To use the Linux command `ls -la` to list files in the `/proc/cpuinfo` Linux file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

<span data-ttu-id="59a3b-131">PowerShell を使用して、Linux コマンド `ls -la` を使用して `C:\Program Files` Windows ファイル システム パス内のファイルを一覧表示するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="59a3b-131">To use the Linux command `ls -la` to list files in the `C:\Program Files` Windows file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a><span data-ttu-id="59a3b-132">Linux からの Windows ツールの実行</span><span class="sxs-lookup"><span data-stu-id="59a3b-132">Run Windows tools from Linux</span></span>

<span data-ttu-id="59a3b-133">WSL では、`[tool-name].exe` を使用して、WSL コマンド ラインから Windows ツールを直接実行することができます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-133">WSL can run Windows tools directly from the WSL command line using `[tool-name].exe`.</span></span>  <span data-ttu-id="59a3b-134">たとえば、`notepad.exe` のように指定します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-134">For example, `notepad.exe`.</span></span>

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

<span data-ttu-id="59a3b-135">この方法で実行されるアプリケーションには、次の特性があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-135">Applications run this way have the following properties:</span></span>

* <span data-ttu-id="59a3b-136">ほとんどの場合、作業ディレクトリを WSL コマンド プロンプトとして保持します (例外については後述します)。</span><span class="sxs-lookup"><span data-stu-id="59a3b-136">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
* <span data-ttu-id="59a3b-137">WSL プロセスと同じアクセス許可権限が与えられています。</span><span class="sxs-lookup"><span data-stu-id="59a3b-137">Have the same permission rights as the WSL process.</span></span>
* <span data-ttu-id="59a3b-138">アクティブな Windows ユーザーとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-138">Run as the active Windows user.</span></span>
* <span data-ttu-id="59a3b-139">CMD プロンプトから直接実行されたかのように、Windows タスク マネージャーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-139">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="59a3b-140">WSL で実行される Windows 実行可能ファイルは、ネイティブの Linux 実行可能ファイルと同様に処理されます。パイプ処理、リダイレクト、さらにバックグラウンド処理も想定どおりに機能します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-140">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="59a3b-141">Linux ディストリビューション (たとえば、Ubuntu) から Windows ツール `ipconfig.exe` を実行し、Linux ツール `grep` を使用して "IPv4" の結果をフィルター処理し、Linux ツール `cut` を使用して列フィールドを削除するには、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-141">To run the Windows tool `ipconfig.exe`, use the Linux tool `grep` to filter the "IPv4" results, and use the Linux tool `cut` to remove the column fields, from a Linux distribution (for example, Ubuntu) enter:</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="59a3b-142">Windows と Linux のコマンドを組み合わせた例を試してみましょう。</span><span class="sxs-lookup"><span data-stu-id="59a3b-142">Let's try an example mixing Windows and Linux commands.</span></span> <span data-ttu-id="59a3b-143">Linux ディストリビューション (つまり、Ubuntu) を開き、テキスト ファイルを作成します: `touch foo.txt`。</span><span class="sxs-lookup"><span data-stu-id="59a3b-143">Open your Linux distribution (ie. Ubuntu) and create a text file: `touch foo.txt`.</span></span> <span data-ttu-id="59a3b-144">次に、Linux コマンド `ls -la` を使用して直接ファイルとその作成の詳細を一覧表示し、さらに Windows PowerShell ツール `findstr.exe` を使用して結果をフィルター処理して `foo.txt` ファイルのみが結果に表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="59a3b-144">Now use the Linux command `ls -la` to list the direct files and their creation details, plus the Windows PowerShell tool `findstr.exe` to filter the results so only your `foo.txt` file shows in the results:</span></span>

```bash
ls -la | findstr.exe foo.txt
```

<span data-ttu-id="59a3b-145">Windows ツールは、ファイル拡張子を含み、ファイルの大文字と小文字が一致し、実行可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-145">Windows tools must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="59a3b-146">非実行可能ファイルにはバッチ スクリプトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-146">Non-executables including batch scripts.</span></span>  <span data-ttu-id="59a3b-147">`dir` などの CMD ネイティブ コマンドは、`cmd.exe /C` コマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-147">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="59a3b-148">たとえば、次のように入力して、Windows ファイル システムの C:\ ディレクトリの内容を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-148">For example, list the contents of your Windows files system C:\ directory, by entering:</span></span>

```bash
cmd.exe /C dir
```

<span data-ttu-id="59a3b-149">または、`ping` コマンドを使用して、エコー要求を microsoft.com Web サイトに送信します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-149">Or use the `ping` command to send an echo request to the microsoft.com website:</span></span>

```bash
ping.exe www.microsoft.com
```

<span data-ttu-id="59a3b-150">パラメーターは、変更されずに Windows バイナリに渡されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-150">Parameters are passed to the Windows binary unmodified.</span></span> <span data-ttu-id="59a3b-151">たとえば、次のコマンドを実行すると `C:\temp\foo.txt` が `notepad.exe` で開かれます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-151">As an example, the following command will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

```bash
notepad.exe "C:\temp\foo.txt"
```

<span data-ttu-id="59a3b-152">以下も有効です。</span><span class="sxs-lookup"><span data-stu-id="59a3b-152">This will also work:</span></span>

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="59a3b-153">Windows と WSL の間での環境変数の共有</span><span class="sxs-lookup"><span data-stu-id="59a3b-153">Share environment variables between Windows and WSL</span></span>

<span data-ttu-id="59a3b-154">WSL と Windows は `WSLENV` を共有します。これは、Windows と WSL で実行される Linux ディストリビューションをつなぐために作成された特殊な環境変数です。</span><span class="sxs-lookup"><span data-stu-id="59a3b-154">WSL and Windows share a special environment variable, `WSLENV`, created to bridge Windows and Linux distributions running on WSL.</span></span>

<span data-ttu-id="59a3b-155">`WSLENV` 変数のプロパティ:</span><span class="sxs-lookup"><span data-stu-id="59a3b-155">Properties of `WSLENV` variable:</span></span>

* <span data-ttu-id="59a3b-156">共有され、Windows と WSL の両方の環境に存在します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-156">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="59a3b-157">Windows と WSL の間で共有する環境変数の一覧です。</span><span class="sxs-lookup"><span data-stu-id="59a3b-157">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="59a3b-158">Windows と WSL で適切に機能するように環境変数をフォーマットできます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-158">It can format environment variables to work well in Windows and WSL.</span></span>

> [!NOTE]
> <span data-ttu-id="59a3b-159">17063 より前では、WSL がアクセスできる唯一の Windows 環境変数は `PATH` でした (そのため、WSL で Win32 実行可能ファイルを起動できました)。</span><span class="sxs-lookup"><span data-stu-id="59a3b-159">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span> <span data-ttu-id="59a3b-160">17063 以降、`WSLENV` がサポートされるようになります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-160">Starting in 17063, `WSLENV` begins being supported.</span></span>

## <a name="wslenv-flags"></a><span data-ttu-id="59a3b-161">WSLENV フラグ</span><span class="sxs-lookup"><span data-stu-id="59a3b-161">WSLENV flags</span></span>

<span data-ttu-id="59a3b-162">`WSLENV` には、環境変数の変換方法に影響を与える 4 つのフラグがあります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-162">There are four flags available in `WSLENV` to influence how the environment variable is translated.</span></span>

<span data-ttu-id="59a3b-163">`WSLENV` のフラグ:</span><span class="sxs-lookup"><span data-stu-id="59a3b-163">`WSLENV` flags:</span></span>

* <span data-ttu-id="59a3b-164">`/p` - WSL/Linux スタイル パスと Win32 パスの間でパスを変換します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-164">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="59a3b-165">`/l` - 環境変数がパスのリストであることを示します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-165">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="59a3b-166">`/u` - Win32 から WSL を実行する場合にのみ、この環境変数を含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-166">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="59a3b-167">`/w` - WSL から Win32 を実行する場合にのみ、この環境変数を含める必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-167">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="59a3b-168">フラグは、必要に応じて組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-168">Flags can be combined as needed.</span></span>

## <a name="disable-interoperability"></a><span data-ttu-id="59a3b-169">相互運用性の無効化</span><span class="sxs-lookup"><span data-stu-id="59a3b-169">Disable interoperability</span></span>

<span data-ttu-id="59a3b-170">ユーザーは、ルートとして次のコマンドを実行することで、1 つの WSL セッションに対して Windows ツールを実行する機能を無効にできます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-170">Users may disable the ability to run Windows tools for a single WSL session by running the following command as root:</span></span>

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="59a3b-171">Windows バイナリを再び有効にするには、すべての WSL セッションを終了して bash.exe を再実行するか、ルートとして次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-171">To re-enable Windows binaries, exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="59a3b-172">相互運用の無効化は、WSL セッション間で保持されません。新しいセッションが開始されると、相互運用は再び有効になります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-172">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="earlier-versions-of-windows-10"></a><span data-ttu-id="59a3b-173">Windows 10 の以前のバージョン</span><span class="sxs-lookup"><span data-stu-id="59a3b-173">Earlier versions of Windows 10</span></span>

<span data-ttu-id="59a3b-174">以前の Windows 10 バージョンでは、相互運用性コマンドにいくつかの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-174">There are several differences for the interoperability commands on earlier Windows 10 versions.</span></span> <span data-ttu-id="59a3b-175">Windows 10 の Creators Update (2017 年 10 月、Build 16299) バージョンまたは Anniversary Update (2016 年 8 月、Build 14393) バージョンを実行している場合は[最新の Windows バージョンに更新する](ms-settings:windowsupdate)ことをお勧めします。ただし、これが不可能な場合のために、相互運用性に関する相違点のいくつかを次にまとめてあります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-175">If you're running a Creators Update (Oct 2017, Build 16299), or Anniversary Update (Aug 2016, Build 14393) version of Windows 10, we recommend you [update to the latest Windows version](ms-settings:windowsupdate), but if that's not possible, we have outlined some of the interop differences below.</span></span>

<span data-ttu-id="59a3b-176">要約:</span><span class="sxs-lookup"><span data-stu-id="59a3b-176">Summary:</span></span>

* <span data-ttu-id="59a3b-177">`bash.exe` は `wsl.exe` に置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="59a3b-177">`bash.exe` has been replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="59a3b-178">1 つのコマンドを実行する場合の `-c` オプションは、`wsl.exe` で必要ありません。</span><span class="sxs-lookup"><span data-stu-id="59a3b-178">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="59a3b-179">Windows パスは WSL `$PATH` に含まれています。</span><span class="sxs-lookup"><span data-stu-id="59a3b-179">Windows path is included in the WSL `$PATH`.</span></span>
* <span data-ttu-id="59a3b-180">相互運用を無効にするプロセスは変更されていません。</span><span class="sxs-lookup"><span data-stu-id="59a3b-180">The process for disabling interop is unchanged.</span></span>

<span data-ttu-id="59a3b-181">Linux コマンドは Windows コマンド プロンプトまたは PowerShell から実行できますが、初期の Windows バージョンでは `bash` コマンドを使用することが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-181">Linux commands can be run from the Windows Command Prompt or from PowerShell, but for early Windows versions, you man need to use the `bash` command.</span></span> <span data-ttu-id="59a3b-182">たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-182">For example:</span></span>

```powershell
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="59a3b-183">sudo、パイプ処理、ファイル リダイレクトなどが想定どおりに機能します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-183">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="59a3b-184">`bash -c` に渡される WSL コマンドは、変更なしで WSL プロセスに転送されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-184">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="59a3b-185">ファイル パスは WSL 形式で指定する必要があり、関連文字をエスケープするように注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-185">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="59a3b-186">例:</span><span class="sxs-lookup"><span data-stu-id="59a3b-186">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

<span data-ttu-id="59a3b-187">または</span><span class="sxs-lookup"><span data-stu-id="59a3b-187">Or...</span></span>

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

<span data-ttu-id="59a3b-188">以前のバージョンの Windows 10 の WSL ディストリビューションから Windows ツールを呼び出す場合は、ディレクトリ パスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-188">When calling a Windows tool from a WSL distribution in an earlier version of Windows 10, you will need to specify the directory path.</span></span> <span data-ttu-id="59a3b-189">たとえば、WSL コマンド ラインから次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-189">For example, from your WSL command line, enter:</span></span>

```bash
/mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="59a3b-190">WSL では、これらの実行可能ファイルはネイティブの Linux 実行可能ファイルと同様に処理されます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-190">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="59a3b-191">これは、Linux パスへのディレクトリの追加や、コマンド間でのパイプ処理が想定どおりに機能することを意味します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-191">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="59a3b-192">たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-192">For example:</span></span>

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
<span data-ttu-id="59a3b-193">または</span><span class="sxs-lookup"><span data-stu-id="59a3b-193">Or</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="59a3b-194">Windows バイナリは、ファイル拡張子を含み、ファイルの大文字と小文字が一致し、実行可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="59a3b-194">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="59a3b-195">バッチ スクリプトや `dir` などのコマンドを含む非実行可能ファイルは、`/mnt/c/Windows/System32/cmd.exe /C` コマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="59a3b-195">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span> <span data-ttu-id="59a3b-196">たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="59a3b-196">For example:</span></span>

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a><span data-ttu-id="59a3b-197">その他の資料</span><span class="sxs-lookup"><span data-stu-id="59a3b-197">Additional resources</span></span>

* [<span data-ttu-id="59a3b-198">2016 年からの相互運用性に関する WSL のブログの投稿</span><span class="sxs-lookup"><span data-stu-id="59a3b-198">WSL blog post on interoperability from 2016</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)
