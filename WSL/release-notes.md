---
title: Windows Subsystem for Linux のリリース ノート
description: Windows Subsystem for Linux のリリース ノート。  毎週更新されます。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu 用 windows サブシステム
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988261"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="d84f9-105">Windows Subsystem for Linux のリリース ノート</span><span class="sxs-lookup"><span data-stu-id="d84f9-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18890"></a><span data-ttu-id="d84f9-106">ビルド 18890</span><span class="sxs-lookup"><span data-stu-id="d84f9-106">Build 18890</span></span>
<span data-ttu-id="d84f9-107">一般的な Windows ビルド 18890 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-107">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-108">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-108">WSL</span></span>
* <span data-ttu-id="d84f9-109">非ブロッキング ソケット リーク [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="d84f9-109">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="d84f9-110">EOF 入力ターミナルには、それ以降の読み取り [GH 3421] をブロックできます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-110">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="d84f9-111">[GH 3928 で説明した] wsl.conf を参照するヘッダーを resolv.conf を更新します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-111">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="d84f9-112">Epoll でデッドロック コード [GH 3922] の削除します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-112">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="d84f9-113">-インポートおよび – [GH 3932] をエクスポートする引数にスペースを処理します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-113">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="d84f9-114">Mmap の拡張ファイルが正しく機能しません [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="d84f9-114">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="d84f9-115">ARM64 に関する問題を解決する\\wsl$ アクセスが正しく機能していません</span><span class="sxs-lookup"><span data-stu-id="d84f9-115">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="d84f9-116">Wsl.exe の向上の既定のアイコンを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-116">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="d84f9-117">ビルド 18342</span><span class="sxs-lookup"><span data-stu-id="d84f9-117">Build 18342</span></span>
<span data-ttu-id="d84f9-118">一般的な Windows ビルド 18342 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-118">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-119">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-119">WSL</span></span>
* <span data-ttu-id="d84f9-120">ユーザーが Windows から WSL ディストリビューションでの Linux ファイルにアクセスする機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-120">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="d84f9-121">これらのファイルは、コマンドライン、およびもファイル エクスプ ローラー、VSCode のように、Windows アプリを使用アクセスできるなどは、これらのファイルと対話できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-121">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="d84f9-122">移動して、ファイルにアクセス\\ \\wsl$\\< distro_name > に移動してディストリビューションを実行しているの一覧を表示または\\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="d84f9-122">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="d84f9-123">追加の CPU 情報タグを追加し、[GH 2234] Cpus_allowed [リスト] の値を修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-123">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="d84f9-124">Exec 非リーダー スレッド [GH 3800] からのサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-124">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="d84f9-125">致命的でない [GH 3785] として構成の更新の失敗を扱う</span><span class="sxs-lookup"><span data-stu-id="d84f9-125">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="d84f9-126">[GH 3768] のオフセットを正しく処理するために binfmt を更新します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-126">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="d84f9-127">9 の計画 [GH 3854] のネットワーク ドライブのマッピングを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-127">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="d84f9-128">-> Linux のサポート Windows と Linux バインド マウント モードの Windows パスの変換を -></span><span class="sxs-lookup"><span data-stu-id="d84f9-128">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="d84f9-129">読み取り専用、開かれたファイルに読み取り専用のセクションで、マッピングを作成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-129">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="d84f9-130">ビルド 18334</span><span class="sxs-lookup"><span data-stu-id="d84f9-130">Build 18334</span></span>
<span data-ttu-id="d84f9-131">一般的な Windows ビルド 18334 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-131">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-132">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-132">WSL</span></span>
* <span data-ttu-id="d84f9-133">Windows タイム ゾーンが Linux のタイム ゾーン [GH 3747] にマップする方法を再設計します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-133">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="d84f9-134">メモリ リークを修正し、新しい文字列変換関数 [GH 3746] を追加</span><span class="sxs-lookup"><span data-stu-id="d84f9-134">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="d84f9-135">ないスレッドで、threadgroup SIGCONT は no-op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="d84f9-135">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="d84f9-136">正しく/proc/self/fd のソケットと epoll のファイル記述子を表示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-136">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="d84f9-137">ビルド 18305</span><span class="sxs-lookup"><span data-stu-id="d84f9-137">Build 18305</span></span>
<span data-ttu-id="d84f9-138">一般的な Windows ビルド 18305 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-138">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-139">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-139">WSL</span></span>
* <span data-ttu-id="d84f9-140">pthreads プライマリ スレッドの終了 [GH 3589] 時にファイルへのアクセスが失われる</span><span class="sxs-lookup"><span data-stu-id="d84f9-140">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="d84f9-141">必要である場合を除き、TIOCSCTTY は"-force"パラメーターを無視する必要があります [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="d84f9-141">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="d84f9-142">wsl.exe コマンドラインの機能強化と加算のインポート/エクスポート機能。</span><span class="sxs-lookup"><span data-stu-id="d84f9-142">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="d84f9-143">ビルド 18277</span><span class="sxs-lookup"><span data-stu-id="d84f9-143">Build 18277</span></span>
<span data-ttu-id="d84f9-144">一般的な Windows ビルド 18277 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-144">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-145">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-145">WSL</span></span>
* <span data-ttu-id="d84f9-146">ビルド 18272 [GH 3645] で導入された「インターフェイスがサポートされています」エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-146">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="d84f9-147">Umount syscall [GH 3605] の MNT_FORCE フラグを無視します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-147">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="d84f9-148">公式の CreatePseudoConsole API を使用してスイッチ WSL 相互運用機能</span><span class="sxs-lookup"><span data-stu-id="d84f9-148">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="d84f9-149">FUTEX_WAIT の再起動時には、タイムアウト値を管理なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-149">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="d84f9-150">ビルド 18272</span><span class="sxs-lookup"><span data-stu-id="d84f9-150">Build 18272</span></span>
<span data-ttu-id="d84f9-151">一般的な Windows ビルド 18272 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-151">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-152">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-152">WSL</span></span>
* <span data-ttu-id="d84f9-153">**警告:** WSL を使用できない、このビルドで問題があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-153">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="d84f9-154">お使いのディストリビューションを起動しようとするときは、「インターフェイスがサポートされています」エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-154">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="d84f9-155">問題は修正されており、次の週の高速 Insider ビルドになります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-155">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="d84f9-156">インストールしている場合ことができますにロールバックする前に"以前のバージョンの Windows 10 に Go"を使用して Windows ビルド設定でこのビルドに更新プログラム]-> [& セキュリティ Recovery]-> [です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-156">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="d84f9-157">ビルド 18267</span><span class="sxs-lookup"><span data-stu-id="d84f9-157">Build 18267</span></span>
<span data-ttu-id="d84f9-158">一般的な Windows ビルド 18267 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-158">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-159">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-159">WSL</span></span>
* <span data-ttu-id="d84f9-160">ゾンビのプロセスを取得しない可能性があります、無期限に問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-160">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="d84f9-161">エラー メッセージが [GH 3592] の最大長を超える場合、WslRegisterDistribution がハングします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-161">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="d84f9-162">Fsync DrvFs [GH 3556] で、読み取り専用のファイルが正常に許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-162">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="d84f9-163">[GH 3584] 内のシンボリック リンクを作成する前にディレクトリ/bin と/sbin ディレクトリが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-163">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="d84f9-164">WSL インスタンスのインスタンスの終了タイムアウト メカニズムを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-164">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="d84f9-165">タイムアウトは 15 秒、つまり、インスタンスは、最後の WSL プロセスが終了した後、15 秒を終了して現在設定されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-165">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="d84f9-166">ディストリビューションをすぐに終了するには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-166">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="d84f9-167">ビルド 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="d84f9-167">Build 17763 (1809)</span></span>
<span data-ttu-id="d84f9-168">一般的な Windows ビルド 17763 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-168">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-169">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-169">WSL</span></span>
* <span data-ttu-id="d84f9-170">Setpriority syscall アクセス許可のチェックが同じスレッドの優先順位 [GH 1838] を変更するためには厳格すぎます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-170">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="d84f9-171">バイアスをかけない割り込み時間が clock_gettime(CLOCK_BOOTTIME) [GH 3434] の負の値が返されないように、ブート時に使用されるように</span><span class="sxs-lookup"><span data-stu-id="d84f9-171">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="d84f9-172">WSL binfmt インタープリター [GH 3424] でハンドルのシンボリック リンク</span><span class="sxs-lookup"><span data-stu-id="d84f9-172">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="d84f9-173">Threadgroup リーダー ファイル記述子のクリーンアップの処理の改善。</span><span class="sxs-lookup"><span data-stu-id="d84f9-173">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="d84f9-174">WSL KeQueryInterruptTimePrecise を KeQueryPerformanceCounter ではなく [GH 3252] のオーバーフローを回避するために使用するスイッチします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-174">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="d84f9-175">Ptrace アタッチ システム コール [GH 1731] から不適切な戻り値が発生します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-175">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="d84f9-176">修正プログラムのいくつかの AF_UNIX 関連の問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="d84f9-176">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="d84f9-177">WSL の相互運用機能を現在の作業ディレクトリが 5 より小さい文字長 [GH 3379] の場合は失敗を引き起こす可能性のある問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-177">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="d84f9-178">存在しないポート [GH 3286] へのループバック接続に失敗した 1 つの 2 つ目の遅延を防ぐ</span><span class="sxs-lookup"><span data-stu-id="d84f9-178">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="d84f9-179">書き込むスタブ ファイル [GH 2893] の追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-179">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="d84f9-180">正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="d84f9-180">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="d84f9-181">PR_SET_PTRACER サポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="d84f9-181">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="d84f9-182">パイプのファイル システムが誤ってところイベント [GH 3276] の消去</span><span class="sxs-lookup"><span data-stu-id="d84f9-182">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="d84f9-183">Win32 実行可能ファイルの NTFS シンボリック リンクを使用して起動のリンクをシンボリック名 [GH 2909] を順守していません</span><span class="sxs-lookup"><span data-stu-id="d84f9-183">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="d84f9-184">ゾンビのサポート [GH 1353] の強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-184">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="d84f9-185">[GH 場合 1493] Windows の相互運用機能を制御するための wsl.conf エントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-185">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="d84f9-186">常にではありません UNIX ソケット ファミリの種類 [GH 1774] を返す getsockname 問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-186">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="d84f9-187">TIOCSTI [GH 1863] のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-187">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="d84f9-188">接続処理中の非ブロッキング ソケットの書き込み試行 [GH 2846] EAGAIN を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-188">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="d84f9-189">[GH 3246、3291] のマウントされた Vhd での相互運用機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-189">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="d84f9-190">アクセス許可のチェックのルート フォルダー [GH 3304] 上の問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-190">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="d84f9-191">TTY キーボード ioctl KDGKBTYPE、KDGKBMODE および KDSKBMODE の制限付きのサポート。</span><span class="sxs-lookup"><span data-stu-id="d84f9-191">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="d84f9-192">バック グラウンドで起動された場合でも、Windows UI アプリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-192">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="d84f9-193">Wsl-u または - ユーザー オプション [GH 1203] の追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-193">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="d84f9-194">高速スタートアップを有効にした場合、WSL 起動の問題を修正 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="d84f9-194">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="d84f9-195">Unix ソケットが切断されているピア資格情報 [GH 3183] を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-195">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="d84f9-196">非ブロッキング Unix ソケット EAGAIN [GH 3191] で無期限に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-196">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="d84f9-197">場合 = off が新しい既定 drvfs マウントの種類 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="d84f9-197">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="d84f9-198">参照してください[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-198">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="d84f9-199">Wslconfig を追加/ディストリビューションの実行を停止する終了します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-199">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="d84f9-200">WSL シェルのコンテキストにスペースを含むパスを正しく処理しないメニュー エントリの問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-200">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="d84f9-201">拡張属性として大文字と小文字をディレクトリあたりの公開します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-201">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="d84f9-202">ARM64: キャッシュのメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-202">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="d84f9-203">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-203">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="d84f9-204">DrvFs:、エスケープされた文字に対応するプライベートの範囲内の文字のみエスケープ解除します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-204">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="d84f9-205">ELF パーサー インタープリター長さの検証 [GH 3154] で 1 ではオフのエラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-205">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="d84f9-206">WSL の絶対タイマー、過去の時刻では [GH 3091] が起動されません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-206">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="d84f9-207">新しく作成した再解析ポイントはそのために一覧表示、親ディレクトリを確認します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-207">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="d84f9-208">アトミックに DrvFs で大文字と小文字のディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-208">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="d84f9-209">追加の問題を修正しました、ファイルが存在するにもかかわらずに、マルチ スレッド操作で ENOENT に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-209">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="d84f9-210">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="d84f9-210">[GH 2712]</span></span>
* <span data-ttu-id="d84f9-211">UMCI が有効にすると、固定 WSL はエラーを起動します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-211">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="d84f9-212">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="d84f9-212">[GH 3020]</span></span>
* <span data-ttu-id="d84f9-213">WSL [GH 437、603、1836] を起動するエクスプ ローラーのコンテキスト メニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-213">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="d84f9-214">を使用するには、shift キーを押しして、エクスプ ローラー ウィンドウで右クリックします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-214">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="d84f9-215">[GH 2822、3100] Unix ソケット非ブロッキング動作を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-215">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="d84f9-216">GH 2026 で報告される NETLINK コマンドのハングを修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-216">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="d84f9-217">マウント フラグと反映フラグ [GH 2911] のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-217">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="d84f9-218">切り捨てが発生しない inotify イベント [GH 2978] で問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-218">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="d84f9-219">追加 - wsl.exe シェルせず 1 つのバイナリを呼び出すための exec オプション。</span><span class="sxs-lookup"><span data-stu-id="d84f9-219">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="d84f9-220">追加 - 特定のディストリビューションを選択する wsl.exe の分散オプション。</span><span class="sxs-lookup"><span data-stu-id="d84f9-220">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="d84f9-221">Dmesg の制限付きのサポート。</span><span class="sxs-lookup"><span data-stu-id="d84f9-221">Limited support for dmesg.</span></span> <span data-ttu-id="d84f9-222">アプリケーションは、dmesg をログインできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-222">Applications can now log to dmesg.</span></span> <span data-ttu-id="d84f9-223">WSL ドライバーでは、dmesg に限定された情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-223">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="d84f9-224">今後、このドライバーから他の情報診断/を実行するために拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-224">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="d84f9-225">注: dmesg は現在サポートされてから、`/dev/kmsg`デバイス インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="d84f9-225">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="d84f9-226">`syslog` syscall インターフェイスはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-226">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="d84f9-227">そのため、いくつかの`dmesg`などのコマンド ライン オプション`-S`、`-C`機能しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-227">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="d84f9-228">既定の gid およびネイティブ [GH 3042] に一致するようにシリアル デバイスのモードを変更します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-228">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="d84f9-229">DrvFs 拡張属性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-229">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="d84f9-230">注:DrvFs では、拡張属性の名前をいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-230">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="d84f9-231">一部の文字 (のように '/'、':' と '\*') を許可、および拡張がない属性名は DrvFs で大文字小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-231">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="d84f9-232">ビルド 18252 (スキップ先)</span><span class="sxs-lookup"><span data-stu-id="d84f9-232">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="d84f9-233">一般的な Windows ビルド 18252 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-233">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-234">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-234">WSL</span></span>
* <span data-ttu-id="d84f9-235">Lxssmanager dll 外および個別のツールのフォルダーには、init と多くのバイナリを移動します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-235">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="d84f9-236">CLONE_FILES を使用する場合は、ファイル記述子を閉じる周囲の競合を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-236">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="d84f9-237">DrvFs パスを変換するときに、/proc/pid/mountinfo で省略可能なフィールドを処理します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-237">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="d84f9-238">S_IFREG のメタデータのサポートなしに成功 DrvFs mknod を許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-238">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="d84f9-239">DrvFs に作成される読み取り専用ファイルは読み取り専用属性が [GH 3411] の設定が必要</span><span class="sxs-lookup"><span data-stu-id="d84f9-239">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="d84f9-240">DrvFs マウントを処理するために/sbin/mount.drvfs ヘルパーを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-240">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="d84f9-241">DrvFs の POSIX 名の変更を使用します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-241">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="d84f9-242">ボリューム GUID を除くボリュームでは、パスの変換を許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-242">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="d84f9-243">17738 (Fast) のビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-243">Build 17738 (Fast)</span></span>
<span data-ttu-id="d84f9-244">一般的な Windows ビルド 17738 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-244">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-245">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-245">WSL</span></span>
* <span data-ttu-id="d84f9-246">Setpriority syscall アクセス許可のチェックが同じスレッドの優先順位 [GH 1838] を変更するためには厳格すぎます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-246">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="d84f9-247">バイアスをかけない割り込み時間が clock_gettime(CLOCK_BOOTTIME) [GH 3434] の負の値が返されないように、ブート時に使用されるように</span><span class="sxs-lookup"><span data-stu-id="d84f9-247">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="d84f9-248">WSL binfmt インタープリター [GH 3424] でハンドルのシンボリック リンク</span><span class="sxs-lookup"><span data-stu-id="d84f9-248">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="d84f9-249">Threadgroup リーダー ファイル記述子のクリーンアップの処理の改善。</span><span class="sxs-lookup"><span data-stu-id="d84f9-249">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="d84f9-250">17728 (Fast) のビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-250">Build 17728 (Fast)</span></span>
<span data-ttu-id="d84f9-251">一般的な Windows ビルド 17728 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-251">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-252">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-252">WSL</span></span>
* <span data-ttu-id="d84f9-253">WSL KeQueryInterruptTimePrecise を KeQueryPerformanceCounter ではなく [GH 3252] のオーバーフローを回避するために使用するスイッチします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-253">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="d84f9-254">Ptrace アタッチ システム コール [GH 1731] から不適切な戻り値が発生します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-254">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="d84f9-255">AF_UNIX 数に関連する修正プログラムの問題 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="d84f9-255">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="d84f9-256">WSL の相互運用機能を現在の作業ディレクトリが 5 より小さい文字長 [GH 3379] の場合は失敗を引き起こす可能性のある問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-256">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="d84f9-257">ビルド 18204 (スキップ先)</span><span class="sxs-lookup"><span data-stu-id="d84f9-257">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="d84f9-258">一般的な Windows ビルド 18204 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-258">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-259">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-259">WSL</span></span>
* <span data-ttu-id="d84f9-260">パイプのところイベント [GH 3276] をオフにすると、ファイル システム inadvertenly</span><span class="sxs-lookup"><span data-stu-id="d84f9-260">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="d84f9-261">Win32 実行可能ファイルの NTFS シンボリック リンクを使用して起動のリンクをシンボリック名 [GH 2909] を順守していません</span><span class="sxs-lookup"><span data-stu-id="d84f9-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="d84f9-262">17723 (Fast) のビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-262">Build 17723 (Fast)</span></span>
<span data-ttu-id="d84f9-263">一般的な Windows ビルド 17723 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-263">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-264">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-264">WSL</span></span>
* <span data-ttu-id="d84f9-265">存在しないポート [GH 3286] へのループバック接続に失敗した 1 つの 2 つ目の遅延を防ぐ</span><span class="sxs-lookup"><span data-stu-id="d84f9-265">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="d84f9-266">書き込むスタブ ファイル [GH 2893] の追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-266">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="d84f9-267">正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="d84f9-267">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="d84f9-268">PR_SET_PTRACER サポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="d84f9-268">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="d84f9-269">パイプのところイベント [GH 3276] をオフにすると、ファイル システム inadvertenly</span><span class="sxs-lookup"><span data-stu-id="d84f9-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="d84f9-270">Win32 実行可能ファイルの NTFS シンボリック リンクを使用して起動のリンクをシンボリック名 [GH 2909] を順守していません</span><span class="sxs-lookup"><span data-stu-id="d84f9-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="d84f9-271">ビルド 17713</span><span class="sxs-lookup"><span data-stu-id="d84f9-271">Build 17713</span></span>
<span data-ttu-id="d84f9-272">一般的な Windows ビルド 17713 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-272">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-273">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-273">WSL</span></span>
* <span data-ttu-id="d84f9-274">ゾンビのサポート [GH 1353] の強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-274">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="d84f9-275">[GH 場合 1493] Windows の相互運用機能を制御するための wsl.conf エントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-275">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="d84f9-276">常にではありません UNIX ソケット ファミリの種類 [GH 1774] を返す getsockname 問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-276">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="d84f9-277">TIOCSTI [GH 1863] のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-277">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="d84f9-278">接続処理中の非ブロッキング ソケットの書き込み試行 [GH 2846] EAGAIN を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-278">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="d84f9-279">[GH 3246、3291] のマウントされた Vhd での相互運用機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-279">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="d84f9-280">アクセス許可のチェックのルート フォルダー [GH 3304] 上の問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-280">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="d84f9-281">TTY キーボード ioctl KDGKBTYPE、KDGKBMODE および KDSKBMODE の制限付きのサポート。</span><span class="sxs-lookup"><span data-stu-id="d84f9-281">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="d84f9-282">バック グラウンドで起動された場合でも、Windows UI アプリを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-282">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="d84f9-283">ビルド 17704</span><span class="sxs-lookup"><span data-stu-id="d84f9-283">Build 17704</span></span>
<span data-ttu-id="d84f9-284">一般的な Windows ビルド 17704 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-284">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-285">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-285">WSL</span></span>
* <span data-ttu-id="d84f9-286">Wsl-u または - ユーザー オプション [GH 1203] の追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-286">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="d84f9-287">高速スタートアップを有効にした場合、WSL 起動の問題を修正 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="d84f9-287">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="d84f9-288">Unix ソケットが切断されているピア資格情報 [GH 3183] を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-288">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="d84f9-289">非ブロッキング Unix ソケット EAGAIN [GH 3191] で無期限に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-289">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="d84f9-290">場合 = off が新しい既定 drvfs マウントの種類 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="d84f9-290">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="d84f9-291">参照してください[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-291">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="d84f9-292">Wslconfig を追加/ディストリビューションの実行を停止する終了します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-292">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="d84f9-293">ビルド 17692</span><span class="sxs-lookup"><span data-stu-id="d84f9-293">Build 17692</span></span>
<span data-ttu-id="d84f9-294">一般的な Windows ビルド 17692 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-294">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-295">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-295">WSL</span></span>
* <span data-ttu-id="d84f9-296">WSL シェルのコンテキストにスペースを含むパスを正しく処理しないメニュー エントリの問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-296">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="d84f9-297">拡張属性として大文字と小文字をディレクトリあたりの公開します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-297">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="d84f9-298">ARM64: キャッシュのメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-298">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="d84f9-299">解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-299">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="d84f9-300">DrvFs:、エスケープされた文字に対応するプライベートの範囲内の文字のみエスケープ解除します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-300">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="d84f9-301">ビルド 17686</span><span class="sxs-lookup"><span data-stu-id="d84f9-301">Build 17686</span></span>
<span data-ttu-id="d84f9-302">一般的な Windows ビルド 17686 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-302">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-303">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-303">WSL</span></span>
* <span data-ttu-id="d84f9-304">ELF パーサー インタープリター長さの検証 [GH 3154] で 1 ではオフのエラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-304">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="d84f9-305">WSL の絶対タイマー、過去の時刻では [GH 3091] が起動されません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-305">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="d84f9-306">新しく作成した再解析ポイントはそのために一覧表示、親ディレクトリを確認します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-306">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="d84f9-307">アトミックに DrvFs で大文字と小文字のディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-307">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="d84f9-308">ビルド 17677</span><span class="sxs-lookup"><span data-stu-id="d84f9-308">Build 17677</span></span>
<span data-ttu-id="d84f9-309">一般的な Windows ビルド 17677 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-309">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-310">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-310">WSL</span></span>
* <span data-ttu-id="d84f9-311">追加の問題を修正しました、ファイルが存在するにもかかわらずに、マルチ スレッド操作で ENOENT に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-311">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="d84f9-312">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="d84f9-312">[GH 2712]</span></span>
* <span data-ttu-id="d84f9-313">UMCI が有効にすると、固定 WSL はエラーを起動します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-313">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="d84f9-314">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="d84f9-314">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="d84f9-315">ビルド 17666</span><span class="sxs-lookup"><span data-stu-id="d84f9-315">Build 17666</span></span>
<span data-ttu-id="d84f9-316">一般的な Windows ビルド 17666 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-316">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-317">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-317">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="d84f9-318">警告:WSL がいくつか AMD チップセット [GH 3134] で実行されていることを防止、問題があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-318">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="d84f9-319">修正プログラムは、その方法 Insider ビルド ブランチ準備しです。</span><span class="sxs-lookup"><span data-stu-id="d84f9-319">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="d84f9-320">WSL [GH 437、603、1836] を起動するエクスプ ローラーのコンテキスト メニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-320">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="d84f9-321">保留中の shift キーと、エクスプ ローラー ウィンドウで右クリックを使用します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-321">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="d84f9-322">[GH 2822、3100] unix ソケット非ブロッキング動作を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-322">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="d84f9-323">GH 2026 で報告される NETLINK コマンドのハングを修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-323">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="d84f9-324">マウント フラグと反映フラグ [GH 2911] のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-324">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="d84f9-325">切り捨てが発生しない inotify イベント [GH 2978] で問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-325">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="d84f9-326">追加 - wsl.exe シェルせず 1 つのバイナリを呼び出すための exec オプション。</span><span class="sxs-lookup"><span data-stu-id="d84f9-326">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="d84f9-327">追加 - 特定のディストリビューションを選択する wsl.exe の分散オプション。</span><span class="sxs-lookup"><span data-stu-id="d84f9-327">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="d84f9-328">ビルド 17655 (スキップ先)</span><span class="sxs-lookup"><span data-stu-id="d84f9-328">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="d84f9-329">一般的な Windows ビルド 17655 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-329">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-330">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-330">WSL</span></span>
* <span data-ttu-id="d84f9-331">Dmesg の制限付きのサポート。</span><span class="sxs-lookup"><span data-stu-id="d84f9-331">Limited support for dmesg.</span></span> <span data-ttu-id="d84f9-332">アプリケーションは、dmesg をログインできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-332">Applications can now log to dmesg.</span></span> <span data-ttu-id="d84f9-333">WSL ドライバーでは、dmesg に限定された情報を記録します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-333">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="d84f9-334">今後、このドライバーから他の情報診断/を実行するために拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-334">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="d84f9-335">注: dmesg は現在サポートされてから、`/dev/kmsg`デバイス インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="d84f9-335">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="d84f9-336">`syslog` sycall インターフェイスはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-336">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="d84f9-337">そのため、いくつかの`dmesg`などのコマンド ライン オプション`-S`、`-C`機能しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-337">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="d84f9-338">ファイルが存在するにもかかわらずに、マルチ スレッド操作で ENOENT に返すことが問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-338">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="d84f9-339">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="d84f9-339">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="d84f9-340">ビルド 17639 (スキップ先)</span><span class="sxs-lookup"><span data-stu-id="d84f9-340">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="d84f9-341">一般的な Windows ビルド 17639 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-341">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-342">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-342">WSL</span></span>
* <span data-ttu-id="d84f9-343">既定の gid およびネイティブ [GH 3042] に一致するようにシリアル デバイスのモードを変更します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-343">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="d84f9-344">DrvFs 拡張属性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-344">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="d84f9-345">注:DrvFs では、拡張属性の名前をいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-345">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="d84f9-346">具体的には、いくつかの文字 (のように '/'、':' と '\*') を許可、および拡張がない属性名は DrvFs で大文字小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-346">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="d84f9-347">17133 (Fast) のビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-347">Build 17133 (Fast)</span></span>
<span data-ttu-id="d84f9-348">一般的な Windows ビルド 17133 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-348">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-349">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-349">WSL</span></span>
* <span data-ttu-id="d84f9-350">WSL でハングを修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-350">Fix for hang in WSL.</span></span> <span data-ttu-id="d84f9-351">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="d84f9-351">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="d84f9-352">17128 (Fast) のビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-352">Build 17128 (Fast)</span></span>
<span data-ttu-id="d84f9-353">一般的な Windows ビルド 17128 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-353">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-354">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-354">WSL</span></span>
* <span data-ttu-id="d84f9-355">なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-355">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="d84f9-356">ビルド 17627 (スキップ先)</span><span class="sxs-lookup"><span data-stu-id="d84f9-356">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="d84f9-357">一般的な Windows ビルド 17627 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-357">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-358">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-358">WSL</span></span>
* <span data-ttu-id="d84f9-359">Futex pi に対応した操作のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-359">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="d84f9-360">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="d84f9-360">[GH 1006]</span></span>
    * <span data-ttu-id="d84f9-361">優先順位いないこと現在サポートされている WSL 機能、制限がありますが、標準の使用状況ブロックを解除する必要がありますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="d84f9-361">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="d84f9-362">WSL プロセスの Windows ファイアウォールのサポート。</span><span class="sxs-lookup"><span data-stu-id="d84f9-362">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="d84f9-363">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="d84f9-363">[GH 1852]</span></span>
    * <span data-ttu-id="d84f9-364">たとえば、WSL を許可するのには、任意のポートでリッスンするには、管理者特権で Windows cmd を使用に python が処理します。 ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="d84f9-364">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="d84f9-365">ファイアウォール規則を追加する方法の詳細については、次を参照してください[リンク。](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="d84f9-365">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="d84f9-366">Wsl.exe を使用する場合は、ユーザーの既定のシェルを尊重します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-366">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="d84f9-367">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="d84f9-367">[GH 2372]</span></span>
* <span data-ttu-id="d84f9-368">すべてのネットワーク インターフェイスは、イーサネットとして報告します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-368">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="d84f9-369">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="d84f9-369">[GH 2996]</span></span>
* <span data-ttu-id="d84f9-370">破損している/etc/passwd ファイルの処理の改善。</span><span class="sxs-lookup"><span data-stu-id="d84f9-370">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="d84f9-371">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="d84f9-371">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-372">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-372">Console</span></span>
* <span data-ttu-id="d84f9-373">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-373">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-374">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-374">LTP Results:</span></span>
<span data-ttu-id="d84f9-375">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-375">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="d84f9-376">ビルド 17618 (スキップ先)</span><span class="sxs-lookup"><span data-stu-id="d84f9-376">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="d84f9-377">一般的な Windows ビルド 17618 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-377">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-378">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-378">WSL</span></span>
* <span data-ttu-id="d84f9-379">NT の相互運用機能 pseudoconsole 機能が導入 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="d84f9-379">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="d84f9-380">レガシ インストール メカニズム (lxrun.exe) は非推奨とされました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-380">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="d84f9-381">ディストリビューションをインストールするためのサポートされているメカニズムは、Microsoft Store からです。</span><span class="sxs-lookup"><span data-stu-id="d84f9-381">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-382">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-382">Console</span></span>
* <span data-ttu-id="d84f9-383">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-383">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-384">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-384">LTP Results:</span></span>
<span data-ttu-id="d84f9-385">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-385">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="d84f9-386">ビルド 17110</span><span class="sxs-lookup"><span data-stu-id="d84f9-386">Build 17110</span></span>
<span data-ttu-id="d84f9-387">一般的な Windows ビルド 17110 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-387">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-388">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-388">WSL</span></span>
* <span data-ttu-id="d84f9-389">Windows [GH 2928] から終了する/init を許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-389">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="d84f9-390">DrvFs は既定でディレクトリあたり大文字小文字の区別を使用するようになりました (に相当します"ケース dir ="マウント オプション)。</span><span class="sxs-lookup"><span data-stu-id="d84f9-390">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="d84f9-391">使用して"ケース force ="(以前の動作) では、レジストリ キーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-391">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="d84f9-392">有効にするのには、次のコマンドを実行"ケース force ="それを使用する必要がある場合: reg HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1 を追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-392">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="d84f9-393">WSL で大文字と小文字を区別する必要がある Windows の以前のバージョンで作成された既存のディレクトリがある場合は、マークと小文字を区別する fsutil.exe を使用して: fsutil.exe ファイル setcasesensitiveinfo<path>を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-393">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="d84f9-394">Uname syscall から返される文字列を NULL に終了します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-394">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-395">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-395">Console</span></span>
* <span data-ttu-id="d84f9-396">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-396">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-397">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-397">LTP Results:</span></span>
<span data-ttu-id="d84f9-398">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-398">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="d84f9-399">ビルド 17107</span><span class="sxs-lookup"><span data-stu-id="d84f9-399">Build 17107</span></span>
<span data-ttu-id="d84f9-400">一般的な Windows ビルド 17107 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-400">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-401">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-401">WSL</span></span>
* <span data-ttu-id="d84f9-402">マスター pty エンドポイント [GH 2552] 上の TCSETSF と TCSETSW をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-402">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="d84f9-403">同時の相互運用プロセスの開始と、EINVAL [GH 2813] が発生することができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-403">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="d84f9-404">メモリ stat に適切なトレースの状態を表示する PTRACE_ATTACH を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-404">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="d84f9-405">CLEARTID と SETTID の両方のフラグでの有効期間が短いプロセスの複製、修正プログラムの競合はでした TID アドレスをクリアせずに終了します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-405">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="d84f9-406">Pre 17093 ビルドから移動するときに、Linux ファイル システムのディレクトリをアップグレードする場合は、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-406">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="d84f9-407">17093 ファイル システムの変更の詳細については、のリリース ノートを参照してください。 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-407">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-408">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-408">Console</span></span>
* <span data-ttu-id="d84f9-409">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-409">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-410">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-410">LTP Results:</span></span>
<span data-ttu-id="d84f9-411">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-411">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="d84f9-412">ビルド 17101</span><span class="sxs-lookup"><span data-stu-id="d84f9-412">Build 17101</span></span>
<span data-ttu-id="d84f9-413">一般的な Windows ビルド 17101 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-413">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-414">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-414">WSL</span></span>
* <span data-ttu-id="d84f9-415">Signalfd をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-415">Support for signalfd.</span></span> <span data-ttu-id="d84f9-416">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="d84f9-416">[GH 129]</span></span>
* <span data-ttu-id="d84f9-417">ファイル名がプライベートの Unicode 文字としてエンコードすることによって、NTFS の無効な文字を含むをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-417">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="d84f9-418">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="d84f9-418">[GH 1514]</span></span>
* <span data-ttu-id="d84f9-419">書き込みがサポートされていない場合、自動マウントは読み取り専用にフォールバックが。</span><span class="sxs-lookup"><span data-stu-id="d84f9-419">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="d84f9-420">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="d84f9-420">[GH 2603]</span></span>
* <span data-ttu-id="d84f9-421">(絵文字の文字) などの Unicode サロゲート ペアの貼り付けを許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-421">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="d84f9-422">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="d84f9-422">[GH 2765]</span></span>
* <span data-ttu-id="d84f9-423">擬似/proc と/sys が読み取りを返すし、select、ポーリング、epoll、副次的 [GH 2838] からの準備完了の書き込み</span><span class="sxs-lookup"><span data-stu-id="d84f9-423">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="d84f9-424">レジストリが改ざんされてまたは破損するいると、無限ループに移動するサービスを引き起こす可能性のある問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-424">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="d84f9-425">Iproute2 の新しい (4.14 アップ ストリーム) バージョンを使用する netlink メッセージを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-425">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-426">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-426">Console</span></span>
* <span data-ttu-id="d84f9-427">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-427">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-428">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-428">LTP Results:</span></span>
<span data-ttu-id="d84f9-429">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-429">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="d84f9-430">ビルド 17093</span><span class="sxs-lookup"><span data-stu-id="d84f9-430">Build 17093</span></span>
<span data-ttu-id="d84f9-431">一般的な Windows ビルド 17093 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-431">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="d84f9-432">重要:</span><span class="sxs-lookup"><span data-stu-id="d84f9-432">Important:</span></span>
<span data-ttu-id="d84f9-433">このビルドにアップグレードした後初めて WSL を開始するときに、Linux ファイル システムのディレクトリをアップグレードする作業の実行が必要です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-433">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="d84f9-434">緩やかに変化を開始する WSL が表示されるようには、数分にかかるこの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-434">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="d84f9-435">これは、ストアからインストールする各配布とにのみ発生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-435">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="d84f9-436">DrvFs での大文字小文字の区別のサポートが向上しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-436">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="d84f9-437">DrvFs は、ディレクトリあたり大文字小文字の区別をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-437">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="d84f9-438">これは、新しいフラグ設定可能なディレクトリをそれらのディレクトリ内のすべての操作を扱う必要があるかを示すで小文字の区別、でも Windows アプリケーション大文字と小文字が異なるだけファイルを正しく開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-438">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="d84f9-439">DrvFs がディレクトリ単位ごとに大文字小文字の区別を制御する新しいマウント オプション</span><span class="sxs-lookup"><span data-stu-id="d84f9-439">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="d84f9-440">ケース force =: すべてのディレクトリは小文字の区別 (ドライブのルート) を除くに扱われます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-440">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="d84f9-441">WSL で作成された新しいディレクトリは、大文字小文字が区別としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-441">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="d84f9-442">これは、新しいディレクトリの大文字と小文字をマークすることを除く、従来の動作です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-442">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="d84f9-443">ケース = dir: ディレクトリあたり大文字小文字の区別フラグを使用してディレクトリだけを小文字の区別; に扱われますその他のディレクトリは、大文字と小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-443">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="d84f9-444">WSL で作成された新しいディレクトリは、大文字小文字が区別としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-444">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="d84f9-445">ケース = オフ: ディレクトリあたり大文字小文字の区別フラグを使用してディレクトリだけを小文字の区別; に扱われますその他のディレクトリは、大文字と小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-445">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="d84f9-446">WSL で作成された新しいディレクトリは、大文字と小文字を区別しないとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-446">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="d84f9-447">注: 以前のリリースで WSL で作成されたディレクトリがないこのフラグが設定されるのでは扱われません小文字の区別を使用する場合、"ケース dir ="オプション。</span><span class="sxs-lookup"><span data-stu-id="d84f9-447">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="d84f9-448">既存のディレクトリにこのフラグを設定する方法は近日公開予定。</span><span class="sxs-lookup"><span data-stu-id="d84f9-448">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="d84f9-449">これらのオプションを使用してマウントの例 (既存のドライブをする必要がありますまずマウントを解除する前に、さまざまなオプションをマウントすることができます): sudo mount-t drvfs c:、/mnt/retention/o c ケース dir を =</span><span class="sxs-lookup"><span data-stu-id="d84f9-449">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="d84f9-450">ここでは、ケース = 強制は、既定のオプション。</span><span class="sxs-lookup"><span data-stu-id="d84f9-450">For now, case=force is still the default option.</span></span> <span data-ttu-id="d84f9-451">これは、ケースに変更、将来 dir を = です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-451">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="d84f9-452">例: DrvFs をマウントする際に Windows パスにスラッシュに使用することようになりましたことができます: sudo-t drvfs//server/share/mnt/share をマウントします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-452">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="d84f9-453">WSL は、今すぐ [GH 2636] インスタンスの起動中に、/etc/fstab ファイルを処理します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-453">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="d84f9-454">これは自動的に DrvFs ドライブをマウントする前に行われますfstab によって既にマウントされていたすべてのドライブはいない再マウントする、自動的に特定のドライブのマウント ポイントを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-454">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="d84f9-455">この動作は wsl.conf を使用してオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-455">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="d84f9-456">/Proc でマウント、mountinfo mountstats ファイルは、バック スラッシュとスペース [GH 2799] などの特殊文字を正しくエスケープします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-456">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="d84f9-457">メタデータが有効にした場合、WSL シンボリック リンク、または fifo ソケットなど DrvFs で作成された特別なファイルのコピーし、Windows 間で移動ようになりましたことができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-457">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="d84f9-458">WSL は wsl.conf でさらに構成できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-458">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="d84f9-459">サブシステムを起動するたびに適用される WSL で自動的に特定の機能を構成するためのメソッドを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-459">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="d84f9-460">これには、自動マウント オプションおよびネットワークの構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-460">This includes automount options and network configuration.</span></span> <span data-ttu-id="d84f9-461">こちらのブログでの詳細については、について説明します。 https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="d84f9-461">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="d84f9-462">AF_UNIX は、WSL 上の Linux プロセスと Windows のネイティブ プロセスの間のソケット接続を許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-462">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="d84f9-463">WSL および Windows アプリケーションは、Unix ソケット上で互いと通信ようになりましたできます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-463">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="d84f9-464">Windows でサービスを実行して、Windows と WSL の両方のアプリで使用できるようにする場合を考えます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-464">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="d84f9-465">ここで、Unix ソケットでできることです。</span><span class="sxs-lookup"><span data-stu-id="d84f9-465">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="d84f9-466">読み取りでの詳細は私たちのブログ投稿 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="d84f9-466">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-467">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-467">WSL</span></span>
* <span data-ttu-id="d84f9-468">Mmap() MAP_NORESERVE [GH 121、2784] でのサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-468">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="d84f9-469">CLONE_PTRACE と CLONE_UNTRACED [2781 GH 121、] をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-469">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="d84f9-470">[GH 121、2781] の複製で SIGCHLD 非終了のシグナルを処理します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-470">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="d84f9-471">スタブ/proc/sys/fs/inotify/max_user_instances と/proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="d84f9-471">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="d84f9-472">[GH 1884] の非ゼロ オフセットを持つロード ヘッダーを含む ELF バイナリの読み込みエラー</span><span class="sxs-lookup"><span data-stu-id="d84f9-472">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="d84f9-473">イメージの読み込み時に末尾のページのバイトをゼロにします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-473">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="d84f9-474">Execve プロセスが終了するサイレント モードでのケースを削減します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-474">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-475">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-475">Console</span></span>
* <span data-ttu-id="d84f9-476">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-476">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-477">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-477">LTP Results:</span></span>
<span data-ttu-id="d84f9-478">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-478">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="d84f9-479">ビルド 17083</span><span class="sxs-lookup"><span data-stu-id="d84f9-479">Build 17083</span></span>
<span data-ttu-id="d84f9-480">一般的な Windows ビルド 17083 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-480">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-481">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-481">WSL</span></span>
* <span data-ttu-id="d84f9-482">Epoll [GH 2798、2801 を報告しました 2857] に関連する固定のバグチェック</span><span class="sxs-lookup"><span data-stu-id="d84f9-482">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="d84f9-483">ASLR [GH 1185、2870] をオフにするときに固定がハングします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-483">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="d84f9-484">Mmap 操作にアトミック [GH 2732] が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-484">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-485">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-485">Console</span></span>
* <span data-ttu-id="d84f9-486">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-487">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-487">LTP Results:</span></span>
<span data-ttu-id="d84f9-488">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-488">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="d84f9-489">ビルド 17074</span><span class="sxs-lookup"><span data-stu-id="d84f9-489">Build 17074</span></span>
<span data-ttu-id="d84f9-490">一般的な Windows ビルド 17074 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-490">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-491">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-491">WSL</span></span>
* <span data-ttu-id="d84f9-492">固定のストレージ形式の DrvFs メタデータ [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="d84f9-492">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="d84f9-493">概要DrvFs メタデータがこのビルドは表示が正しくないかまったくない前に作成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-493">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="d84f9-494">影響を受けるファイルを修正するのにには、メタデータを再適用するのに chmod、chown を使用します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-494">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="d84f9-495">複数の信号と再開可能な syscall で問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-495">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-496">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-496">Console</span></span>
* <span data-ttu-id="d84f9-497">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-498">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-498">LTP Results:</span></span>
<span data-ttu-id="d84f9-499">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-499">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="d84f9-500">ビルド 17063</span><span class="sxs-lookup"><span data-stu-id="d84f9-500">Build 17063</span></span>
<span data-ttu-id="d84f9-501">一般的な Windows ビルド 17063 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-501">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="d84f9-502">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-502">WSL</span></span>
* <span data-ttu-id="d84f9-503">DrvFs には、Linux の追加のメタデータがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d84f9-503">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="d84f9-504">これにより、所有者と chmod/chown とも fifo、unix ソケット デバイス ファイルなどの特殊なファイルの作成を使用してファイルのモードを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-504">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="d84f9-505">これは既定で無効にここではまだ実験段階であるためです。</span><span class="sxs-lookup"><span data-stu-id="d84f9-505">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="d84f9-506">**注:** DrvFs で使用されるメタデータ形式でバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-506">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="d84f9-507">メタデータの実験用には、このビルドで動作しますが、将来のビルドのこのビルドによって作成されたメタデータが正しく読み取られない。</span><span class="sxs-lookup"><span data-stu-id="d84f9-507">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="d84f9-508">手動で変更されたファイルの所有者を更新する必要があり、カスタム デバイス ID を持つデバイスが再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-508">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="d84f9-509">メタデータのオプションを使用してマウント DrvFs を有効にする (既存のマウントを有効にするにする必要がありますまずマウントを解除できます)。</span><span class="sxs-lookup"><span data-stu-id="d84f9-509">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="d84f9-510">Linux のアクセス許可は、追加のメタデータとしては、ファイルに追加されます。Windows のアクセス許可には影響しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-510">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="d84f9-511">メタデータを削除 Windows エディターを使用してファイルを編集することがありますに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d84f9-511">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="d84f9-512">この場合、ファイルは、その既定のアクセス許可に戻されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-512">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="d84f9-513">メタデータなしのコントロール ファイルに追加されたマウント オプション DrvFs。</span><span class="sxs-lookup"><span data-stu-id="d84f9-513">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="d84f9-514">uid: すべてのファイルの所有者を使用するユーザーの ID。</span><span class="sxs-lookup"><span data-stu-id="d84f9-514">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="d84f9-515">gid: すべてのファイルの所有者のためのグループ ID。</span><span class="sxs-lookup"><span data-stu-id="d84f9-515">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="d84f9-516">umask: すべてのファイルとディレクトリを除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="d84f9-516">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="d84f9-517">fmask: すべての定期的なファイルを除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="d84f9-517">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="d84f9-518">dmask: すべてのディレクトリを除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="d84f9-518">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="d84f9-519">例:</span><span class="sxs-lookup"><span data-stu-id="d84f9-519">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="d84f9-520">メタデータのないファイルの既定のアクセス許可を指定するメタデータのオプションとの組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="d84f9-520">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="d84f9-521">新しい環境変数を導入`WSLENV`WSL と Win32 の間の環境変数のフローを構成する。</span><span class="sxs-lookup"><span data-stu-id="d84f9-521">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="d84f9-522">例:</span><span class="sxs-lookup"><span data-stu-id="d84f9-522">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="d84f9-523">`WSLENV` 環境変数 Win32 から WSL プロセスまたは WSL から Win32 プロセスを起動するときに含めることができるコロンで区切られた一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-523">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="d84f9-524">各変数は、次の後が変換される方法を指定するフラグのスラッシュに付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-524">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="d84f9-525">p:値は、Win32 のパスと WSL パスの間を変換するパスです。</span><span class="sxs-lookup"><span data-stu-id="d84f9-525">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="d84f9-526">L:値は、パスの一覧です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-526">l: The value is a list of paths.</span></span> <span data-ttu-id="d84f9-527">WSL、コロンで区切られたリストを勧めします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-527">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="d84f9-528">Win32 では、セミコロン区切りのリストを勧めします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-528">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="d84f9-529">u:値は、必ず含まれる Win32 の WSL を呼び出すときに</span><span class="sxs-lookup"><span data-stu-id="d84f9-529">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="d84f9-530">属性:値は、必ず含まれる WSL から Win32 を呼び出すときに</span><span class="sxs-lookup"><span data-stu-id="d84f9-530">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="d84f9-531">設定できる`WSLENV`.bashrc や、ユーザーのカスタムの Windows 環境でします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-531">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="d84f9-532">drvfs マウントは、tar からのタイムスタンプを正しく保持 cp-p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="d84f9-532">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="d84f9-533">drvfs シンボリック リンク レポートの適切なサイズ (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="d84f9-533">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="d84f9-534">読み取り/書き込みの IO サイズが非常に大きな (GH 2653) のしくみ</span><span class="sxs-lookup"><span data-stu-id="d84f9-534">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="d84f9-535">プロセス グループ Id (GH 2534) で未定義の動作します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-535">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="d84f9-536">大規模な予約のリージョンの強化された mmap パフォーマンスが大幅にghc (GH 1671) のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-536">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="d84f9-537">READ_IMPLIES_EXEC; のパーソナリティのサポート最大値および clisp (GH 1185) を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-537">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="d84f9-538">mprotect PROT_GROWSDOWN; をサポートしています修正 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="d84f9-538">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="d84f9-539">オーバー コミット モードをページ フォールトを修正修正 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="d84f9-539">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="d84f9-540">複製は、複数のフラグの組み合わせをサポートしています</span><span class="sxs-lookup"><span data-stu-id="d84f9-540">clone supports more flags combinations</span></span>
* <span data-ttu-id="d84f9-541">選択/epoll epoll ファイル (以前れません) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-541">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="d84f9-542">実装されていない syscall の ptrace を通知します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-542">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="d84f9-543">Resolv.conf nameservers [GH 2694] を生成するときのないインターフェイスを無視します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-543">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="d84f9-544">物理アドレスなしのネットワーク インターフェイスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-544">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="d84f9-545">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="d84f9-545">[GH 2685]</span></span>
* <span data-ttu-id="d84f9-546">追加のバグ修正と機能強化。</span><span class="sxs-lookup"><span data-stu-id="d84f9-546">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="d84f9-547">Windows 上の開発者が利用できる Linux ツール</span><span class="sxs-lookup"><span data-stu-id="d84f9-547">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="d84f9-548">Windows コマンド ライン ツール チェーンと curl の多く (tar) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d84f9-548">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="d84f9-549">読み取り[このブログ](https://aka.ms/tarcurlwindows)をこれら 2 つの新しいツールの追加の詳細を学習し、Windows での開発者エクスペリエンスを形成している方法を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d84f9-549">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="d84f9-550">`AF_UNIX` Windows Insider SDK (17061 +) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-550">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="d84f9-551">読み取り[このブログ](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)について`AF_UNIX`および Windows の開発者が使用できる方法です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-551">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="d84f9-552">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-552">Console</span></span>
* <span data-ttu-id="d84f9-553">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-553">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-554">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-554">LTP Results:</span></span>
<span data-ttu-id="d84f9-555">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-555">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="d84f9-556">ビルド 17046</span><span class="sxs-lookup"><span data-stu-id="d84f9-556">Build 17046</span></span>

<span data-ttu-id="d84f9-557">一般的な Windows ビルド 17046 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-557">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="d84f9-558">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-558">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-559">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-559">WSL</span></span>
- <span data-ttu-id="d84f9-560">アクティブなターミナルをせずに実行するプロセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-560">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="d84f9-561">[GH 709、1007、1511、2252、2391、et al]。</span><span class="sxs-lookup"><span data-stu-id="d84f9-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="d84f9-562">CLONE_VFORK といなくて向上をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-562">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="d84f9-563">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="d84f9-563">[GH 1878, 2615]</span></span>
- <span data-ttu-id="d84f9-564">WSL がネットワーク操作に TDI フィルター ドライバーをスキップします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-564">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="d84f9-565">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="d84f9-565">[GH 1554]</span></span>
- <span data-ttu-id="d84f9-566">DrvFs は、特定の条件が満たされたときに、NT シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-566">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="d84f9-567">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="d84f9-567">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="d84f9-568">リンク先は相対である必要があります、マウント ポイントやシンボリック リンクを越える必要がありますいないや、存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-568">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="d84f9-569">ユーザー必要があります (通常必要 wsl.exe 管理者特権でを起動すること) SE_CREATE_SYMBOLIC_LINK_PRIVILEGE、開発者モードがオンになっている場合を除き、します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-569">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="d84f9-570">その他のすべての状況で DrvFs はまだ WSL シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-570">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="d84f9-571">管理者特権と、管理者特権以外の WSL インスタンスを同時に実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-571">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="d84f9-572">/Proc/sys/kernel/yama/ptrace_scope をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-572">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="d84f9-573">WSL <> - Windows パスの変換を実行する wslpath を追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-573">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="d84f9-574">[GH 522、1243、1834、2327、et al]。</span><span class="sxs-lookup"><span data-stu-id="d84f9-574">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="d84f9-575">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-575">Console</span></span>
- <span data-ttu-id="d84f9-576">バグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-576">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-577">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-577">LTP Results:</span></span>
<span data-ttu-id="d84f9-578">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-578">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="d84f9-579">ビルド 17040</span><span class="sxs-lookup"><span data-stu-id="d84f9-579">Build 17040</span></span>

<span data-ttu-id="d84f9-580">一般的な Windows ビルド 17040 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-580">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-581">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-581">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-582">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-582">WSL</span></span>
- <span data-ttu-id="d84f9-583">17035 以降の修正プログラムがありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-583">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-584">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-584">Console</span></span>
- <span data-ttu-id="d84f9-585">17035 以降の修正プログラムがありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-585">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-586">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-586">LTP Results:</span></span>
<span data-ttu-id="d84f9-587">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-587">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="d84f9-588">ビルド 17035</span><span class="sxs-lookup"><span data-stu-id="d84f9-588">Build 17035</span></span>

<span data-ttu-id="d84f9-589">一般的な Windows ビルド 17035 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-589">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-590">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-591">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-591">WSL</span></span>
- <span data-ttu-id="d84f9-592">DrvFs ファイルへのアクセスによって変更できる場合によっては失敗します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-592">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="d84f9-593">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="d84f9-593">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-594">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-594">Console</span></span>
- <span data-ttu-id="d84f9-595">VT モード内の行の挿入/削除するときに色の一部が失われる。</span><span class="sxs-lookup"><span data-stu-id="d84f9-595">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-596">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-596">LTP Results:</span></span>
<span data-ttu-id="d84f9-597">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-597">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="d84f9-598">ビルド 17025</span><span class="sxs-lookup"><span data-stu-id="d84f9-598">Build 17025</span></span>

<span data-ttu-id="d84f9-599">一般的な Windows ビルド 17025 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-599">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-600">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-600">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-601">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-601">WSL</span></span>
- <span data-ttu-id="d84f9-602">新しいフォア グラウンド プロセス グループ [GH 1653、2510] 内には、初期のプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-602">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="d84f9-603">SIGHUP 配信では、[GH 2496] を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-603">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="d84f9-604">[GH 2497] 何もない場合は、既定の仮想のブリッジの名前を生成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-604">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="d84f9-605">/Proc/sys/kernel/random/boot_id [GH 2518] を実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-605">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="d84f9-606">複数の相互運用機能の stdout と stderr のパイプを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-606">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="d84f9-607">Syncfs システム コールをスタブします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-607">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-608">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-608">Console</span></span>
- <span data-ttu-id="d84f9-609">サード パーティ製コンソール [GH 111] の入力の VT 翻訳を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-609">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-610">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-610">LTP Results:</span></span>
<span data-ttu-id="d84f9-611">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-611">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="d84f9-612">ビルド 17017</span><span class="sxs-lookup"><span data-stu-id="d84f9-612">Build 17017</span></span>

<span data-ttu-id="d84f9-613">一般的な Windows ビルド 17017 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-613">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-614">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-614">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-615">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-615">WSL</span></span>
- <span data-ttu-id="d84f9-616">空の [GH 330] ELF プログラム ヘッダーを無視します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-616">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="d84f9-617">非対話型ユーザー用の WSL インスタンスを作成する LxssManager を許可する (ssh およびスケジュール タスクのサポート) [GH 777、1602]。</span><span class="sxs-lookup"><span data-stu-id="d84f9-617">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="d84f9-618">サポート WSL Win32]-> [WSL (「開始」) のシナリオ [GH 1228]-> [です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-618">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="d84f9-619">[GH 1614] 相互運用機能を介して呼び出すコンソール アプリの終了の制限付きのサポート。</span><span class="sxs-lookup"><span data-stu-id="d84f9-619">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="d84f9-620">Devpts [GH 1948] のマウント オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-620">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="d84f9-621">Ptrace 子 [GH 2333] の起動をブロックします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-621">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="d84f9-622">EPOLLET [GH 2462] の一部のイベントがありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-622">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="d84f9-623">PTRACE_GETSIGINFO 用のデータを返します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-623">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="d84f9-624">Lseek で Getdents には、正しくない結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-624">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="d84f9-625">データがなくなったをパイプで入力を待機しているいくつかの Win32 相互運用機能アプリ ハングを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-625">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="d84f9-626">Tty/pty ファイルの指定をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-626">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="d84f9-627">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-628">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-628">Console</span></span>
- <span data-ttu-id="d84f9-629">コンソールには、このリリースで変更が関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-630">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-630">LTP Results:</span></span>
<span data-ttu-id="d84f9-631">進行中のテスト。</span><span class="sxs-lookup"><span data-stu-id="d84f9-631">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="d84f9-632">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="d84f9-632">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="d84f9-633">ビルド 16288</span><span class="sxs-lookup"><span data-stu-id="d84f9-633">Build 16288</span></span>

<span data-ttu-id="d84f9-634">一般的な Windows ビルド 16288 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-634">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-635">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-635">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-636">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-636">WSL</span></span>
- <span data-ttu-id="d84f9-637">正しく初期化し、uid や gid、ソケット ファイル記述子の設定 [GH 2490] モードのレポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-637">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="d84f9-638">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-638">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-639">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-639">Console</span></span>
- <span data-ttu-id="d84f9-640">コンソールには、このリリースで変更が関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-640">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-641">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-641">LTP Results:</span></span>
<span data-ttu-id="d84f9-642">16273 以降変更なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-642">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="d84f9-643">ビルド 16278</span><span class="sxs-lookup"><span data-stu-id="d84f9-643">Build 16278</span></span>

<span data-ttu-id="d84f9-644">一般的な Windows ビルド 162738 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-644">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-645">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-645">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-646">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-646">WSL</span></span>
- <span data-ttu-id="d84f9-647">LX MM 状態 [GH 2415] 解除を行うときにバックアップ ファイルのセクションのマップ ビューを明示的にマップ解除します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-647">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="d84f9-648">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-648">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-649">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-649">Console</span></span>
- <span data-ttu-id="d84f9-650">コンソールには、このリリースで変更が関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-650">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-651">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-651">LTP Results:</span></span>
<span data-ttu-id="d84f9-652">16273 以降変更なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-652">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="d84f9-653">ビルド 16275</span><span class="sxs-lookup"><span data-stu-id="d84f9-653">Build 16275</span></span>

<span data-ttu-id="d84f9-654">一般的な Windows ビルド 162735 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-654">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-655">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-655">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-656">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-656">WSL</span></span>
- <span data-ttu-id="d84f9-657">このリリースで変更に関連付けられた WSL がありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-657">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-658">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-658">Console</span></span>
- <span data-ttu-id="d84f9-659">コンソールには、このリリースで変更が関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-660">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-660">LTP Results:</span></span>
<span data-ttu-id="d84f9-661">16273 以降変更なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-661">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="d84f9-662">ビルド 16273</span><span class="sxs-lookup"><span data-stu-id="d84f9-662">Build 16273</span></span>

<span data-ttu-id="d84f9-663">一般的な Windows ビルド 16273 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-663">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-664">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-665">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-665">WSL</span></span>
- <span data-ttu-id="d84f9-666">DrvFs ディレクトリ [GH 2392] の正しくないファイルの種類が報告されることが問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-666">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="d84f9-667">その使用 uevent プログラムのブロックを解除する NETLINK_KOBJECT_UEVENT ソケットの作成を許可する [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="d84f9-667">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="d84f9-668">接続の非ブロッキングのサポートを追加 [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="d84f9-668">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="d84f9-669">実装 CLONE_FS 複製システム呼び出しフラグ [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="d84f9-669">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="d84f9-670">タブまたは NT の相互運用 [GH 1625、2164] で正しく引用符を処理しないに関する問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-670">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="d84f9-671">解決するには再 WSL を起動しようとするときにエラー [GH 651、2095] のインスタンスにアクセスが拒否されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-671">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="d84f9-672">Futex FUTEX_REQUEUE および FUTEX_CMP_REQUEUE 操作 [GH 2242] 実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-672">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="d84f9-673">さまざまな SysFs ファイル [GH 2214] のアクセス許可を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-673">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="d84f9-674">[GH 2290] のセットアップ中に Haskell スタックのハングを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-674">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="d84f9-675">Binfmt_misc 'C' の実装 'o' と 'P' フラグ [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="d84f9-675">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="d84f9-676">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="d84f9-676">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="d84f9-677">Ioprio_set システム コール [GH 498] の部分的なサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-677">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="d84f9-678">スタブ SO_REUSEPORT SO_PASSCRED netlink ソケット [GH 69] のサポートを追加 (&)</span><span class="sxs-lookup"><span data-stu-id="d84f9-678">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="d84f9-679">現在、配布の場合、RegisterDistribuiton から別のエラー コードを返すインストールまたはアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-679">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="d84f9-680">部分的にインストールされている WSL ディストリビューション wslconfig.exe 経由での登録解除を許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-680">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="d84f9-681">Udp::msg_peek から python ソケット テスト ハングを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-681">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="d84f9-682">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-682">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-683">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-683">Console</span></span>
- <span data-ttu-id="d84f9-684">コンソールには、このリリースで変更が関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-684">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-685">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-685">LTP Results:</span></span>
<span data-ttu-id="d84f9-686">合計テスト数:1904</span><span class="sxs-lookup"><span data-stu-id="d84f9-686">Total Tests: 1904</span></span><br/>
<span data-ttu-id="d84f9-687">合計には、テストがスキップされました。209</span><span class="sxs-lookup"><span data-stu-id="d84f9-687">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="d84f9-688">失敗の総数:229</span><span class="sxs-lookup"><span data-stu-id="d84f9-688">Total Failures: 229</span></span><br/>
[<span data-ttu-id="d84f9-689">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-689">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="d84f9-690">ビルド 16257</span><span class="sxs-lookup"><span data-stu-id="d84f9-690">Build 16257</span></span>

<span data-ttu-id="d84f9-691">一般的な Windows ビルド 16257 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-691">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-692">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-693">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-693">WSL</span></span>
- <span data-ttu-id="d84f9-694">Prlimit64 システム コールを実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-694">Implement prlimit64 system call</span></span>
- <span data-ttu-id="d84f9-695">Ulimit n (setrlimit RLIMIT_NOFILE) のサポートを追加する [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="d84f9-695">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="d84f9-696">スタブ MSG_MORE TCP ソケット [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="d84f9-696">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="d84f9-697">無効な AT_EXECFN 補助ベクター動作 [GH 2133] を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-697">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="d84f9-698">コンソール/tty のコピー/貼り付けの動作を修正しより優れたいっぱいバッファー処理 [GH 2204、2131] の追加</span><span class="sxs-lookup"><span data-stu-id="d84f9-698">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="d84f9-699">ユーザー ID の設定およびグループ ID の設定のプログラム [GH 2031] 補助のベクトル内の AT_SECURE を設定します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-699">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="d84f9-700">擬似端末のマスター エンドポイント TIOCPGRP [GH 1063] は処理されません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-700">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="d84f9-701">修正プログラム lseek が LxFs [GH から 2310] 内のディレクトリを巻き戻すには</span><span class="sxs-lookup"><span data-stu-id="d84f9-701">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="d84f9-702">多量の使用 [GH 1882] 後に/dev/ptmx をロックします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-702">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="d84f9-703">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-703">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-704">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-704">Console</span></span>
- <span data-ttu-id="d84f9-705">水平方向の線/アンダー スコア Everywhere [GH 2168] の修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-705">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="d84f9-706">注文処理の変更 [GH 2170] を終了するは困難加えたら NPM 問題の修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-706">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="d84f9-707">この新しい配色を追加するには。 https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="d84f9-707">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-708">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-708">LTP Results:</span></span>
<span data-ttu-id="d84f9-709">16251 以降変更なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-709">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-710">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-710">Syscall Support</span></span>
<span data-ttu-id="d84f9-711">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-711">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-712">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-712">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="d84f9-713">既知の問題</span><span class="sxs-lookup"><span data-stu-id="d84f9-713">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="d84f9-714">GitHub 問題 2392:Windows フォルダーが WSL で認識されない.</span><span class="sxs-lookup"><span data-stu-id="d84f9-714">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="d84f9-715">WSL が経由で Windows のファイル/フォルダーを列挙中に問題が 16257 のビルドで`/mnt/c/...`します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-715">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="d84f9-716">この問題は修正されておりで解放する必要がある 2017 年 8 月 14 の開始週に Insider のビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-716">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="d84f9-717">ビルド 16251</span><span class="sxs-lookup"><span data-stu-id="d84f9-717">Build 16251</span></span>

<span data-ttu-id="d84f9-718">一般的な Windows ビルド 16251 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-718">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-719">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-719">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-720">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-720">WSL</span></span>
- <span data-ttu-id="d84f9-721">WSL オプションのコンポーネントからベータ版のタグを削除しを参照してください[ブログの投稿](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)詳細についてはします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-721">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="d84f9-722">保存された一連の uid と gid の exec [GH 962、1415、2072] でユーザー ID の設定とグループ ID の設定のバイナリを正しく初期化します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-722">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="d84f9-723">Ptrace PTRACE_O_TRACEEXIT [GH 555] のサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-723">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="d84f9-724">Ptrace サポートが追加されました PTRACE_GETFPREGS と PTRACE_GETREGSET NT_FPREGSET [GH 555] で</span><span class="sxs-lookup"><span data-stu-id="d84f9-724">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="d84f9-725">Ptrace を固定を停止する場合は無視信号</span><span class="sxs-lookup"><span data-stu-id="d84f9-725">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="d84f9-726">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-727">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-727">Console</span></span>
- <span data-ttu-id="d84f9-728">コンソールには、このリリースで変更が関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-729">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-729">LTP Results:</span></span>
<span data-ttu-id="d84f9-730">渡すテスト数:768</span><span class="sxs-lookup"><span data-stu-id="d84f9-730">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="d84f9-731">失敗したテスト数:244</span><span class="sxs-lookup"><span data-stu-id="d84f9-731">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="d84f9-732">スキップされたテスト数:96</span><span class="sxs-lookup"><span data-stu-id="d84f9-732">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="d84f9-733">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-733">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="d84f9-734">ビルド 16241</span><span class="sxs-lookup"><span data-stu-id="d84f9-734">Build 16241</span></span>

<span data-ttu-id="d84f9-735">一般的な Windows ビルド 16241 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-735">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-736">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="d84f9-737">WSL</span><span class="sxs-lookup"><span data-stu-id="d84f9-737">WSL</span></span>
- <span data-ttu-id="d84f9-738">このリリースで変更に関連付けられた WSL がありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-738">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="d84f9-739">Console</span><span class="sxs-lookup"><span data-stu-id="d84f9-739">Console</span></span>
- <span data-ttu-id="d84f9-740">報告されていた、交差行 DEC の正しくない文字を出力するための修正プログラム[ここ](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="d84f9-740">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="d84f9-741">コード ページ 65001 (utf8) に表示されている出力テキストの修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-741">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="d84f9-742">選択の変更、パレットの他の部分を 1 つの色の RGB 値に加えられた変更を転送することはありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-742">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="d84f9-743">これにより、コンソールのプロパティ シートを使用して、はるかに簡単です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-743">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="d84f9-744">Ctrl キーを押しながら S キーが正常に動作する表示されません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-744">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="d84f9-745">されていない太字/-Dim 不在であれば完全に ANSI エスケープ コード [GH 2174] から</span><span class="sxs-lookup"><span data-stu-id="d84f9-745">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="d84f9-746">コンソールで Vim の配色テーマ [GH 1706] を正しくサポートしません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-746">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="d84f9-747">特定の文字 [GH 2149] に貼り付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-747">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="d84f9-748">折り返しのサイズ変更が編集/コマンド ライン [GH ConEmu 1123] 機能がある場合は、bash ウィンドウをサイズ変更と対話妙</span><span class="sxs-lookup"><span data-stu-id="d84f9-748">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="d84f9-749">Ctrl キーを押し、-l まま画面ダーティ [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="d84f9-749">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="d84f9-750">HDPI [GH 1907] で VT を表示するときに、コンソール表示バグ</span><span class="sxs-lookup"><span data-stu-id="d84f9-750">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="d84f9-751">Japansese 文字が Unicode 文字 U + 30FB は奇妙に見える [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="d84f9-751">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="d84f9-752">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-752">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="d84f9-753">ビルド 16237</span><span class="sxs-lookup"><span data-stu-id="d84f9-753">Build 16237</span></span>

<span data-ttu-id="d84f9-754">一般的な Windows ビルド 16237 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-754">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-755">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-755">Fixed</span></span>
- <span data-ttu-id="d84f9-756">既定の属性を使用して、EAs のない lxfs (ルート、ルート、0000) でのファイル</span><span class="sxs-lookup"><span data-stu-id="d84f9-756">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="d84f9-757">拡張属性の使用のディストリビューションのサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-757">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="d84f9-758">埋め込み getdents と getdents64 で返されるエントリを修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-758">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="d84f9-759">Shmctl するシステム コール [GH 2068] のアクセス許可チェックを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-759">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="d84f9-760">Tty [GH 2231] の状態は固定の正しくない初期 epoll</span><span class="sxs-lookup"><span data-stu-id="d84f9-760">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="d84f9-761">[GH 2077] のすべてのエントリが返されない DrvFs readdir を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-761">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="d84f9-762">修正 LxFs readdir ファイルが [GH 2077] のリンクを解除</span><span class="sxs-lookup"><span data-stu-id="d84f9-762">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="d84f9-763">リンクされていない drvfs ファイルの詳しい情報を再度開くを許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-763">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="d84f9-764">WSL 機能を無効にするためのグローバル レジストリ キーのオーバーライドを追加 (相互運用機能/ドライブのマウント)</span><span class="sxs-lookup"><span data-stu-id="d84f9-764">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="d84f9-765">DrvFs (および LxFs)「状態」での不正なブロックの数の修正 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="d84f9-765">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="d84f9-766">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-766">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="d84f9-767">ビルド 16232</span><span class="sxs-lookup"><span data-stu-id="d84f9-767">Build 16232</span></span>

<span data-ttu-id="d84f9-768">一般的な Windows ビルド 16232 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-768">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-769">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-769">Fixed</span></span>
- <span data-ttu-id="d84f9-770">このリリースで変更に関連付けられた WSL がありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-770">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="d84f9-771">ビルド 16226</span><span class="sxs-lookup"><span data-stu-id="d84f9-771">Build 16226</span></span>

<span data-ttu-id="d84f9-772">一般的な Windows ビルド 16226 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-772">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-773">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-773">Fixed</span></span>
- <span data-ttu-id="d84f9-774">xattr 関連の syscall のサポート (getxattr、setxattr、listxattr、removexattr)。</span><span class="sxs-lookup"><span data-stu-id="d84f9-774">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="d84f9-775">security.capablity xattr サポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-775">security.capablity xattr support.</span></span>
- <span data-ttu-id="d84f9-776">特定のファイル システム フィルター、ミリ秒以外の SMB サーバーを含むと互換性の強化。</span><span class="sxs-lookup"><span data-stu-id="d84f9-776">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="d84f9-777">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="d84f9-777">[GH #1952]</span></span>
- <span data-ttu-id="d84f9-778">圧縮されたファイルを OneDrive のプレース ホルダー、GVFS のプレース ホルダー、およびコンパクトな OS のサポートを強化します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-778">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="d84f9-779">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-779">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="d84f9-780">ビルド 16215</span><span class="sxs-lookup"><span data-stu-id="d84f9-780">Build 16215</span></span>

<span data-ttu-id="d84f9-781">一般的な Windows ビルド 16215 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-781">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-782">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-782">Fixed</span></span>
- <span data-ttu-id="d84f9-783">WSL では、開発者モードが必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-783">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="d84f9-784">Drvfs でディレクトリ ジャンクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-784">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="d84f9-785">WSL 配布 appx パッケージのアンインストールを処理します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-785">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="d84f9-786">プライベートの表示に詳しい情報の更新プログラムとのマッピングを共有します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-786">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="d84f9-787">配布が部分的にインストールまたはアンインストールをクリーンアップする wslconfig.exe の機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-787">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="d84f9-788">TCP ソケット IP_MTU_DISCOVER のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-788">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="d84f9-789">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="d84f9-789">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="d84f9-790">AF_INADDR へのルートのプロトコル ファミリを推論します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-790">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="d84f9-791">シリアル デバイスの機能強化 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="d84f9-791">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="d84f9-792">ビルド 16199</span><span class="sxs-lookup"><span data-stu-id="d84f9-792">Build 16199</span></span>

<span data-ttu-id="d84f9-793">一般的な Windows ビルド 16199 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-793">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-794">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-794">Fixed</span></span>
- <span data-ttu-id="d84f9-795">これらのリリースで変更に関連付けられた WSL がありません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-795">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="d84f9-796">ビルド 16193</span><span class="sxs-lookup"><span data-stu-id="d84f9-796">Build 16193</span></span>

<span data-ttu-id="d84f9-797">一般的な Windows ビルド 16193 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-797">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-798">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-798">Fixed</span></span>
- <span data-ttu-id="d84f9-799">送信 SIGCONT と終了 [GH 1973] threadgroup 間で競合状態</span><span class="sxs-lookup"><span data-stu-id="d84f9-799">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="d84f9-800">レポート FILE_DEVICE_CONSOLE [GH 1840] ではなく FILE_DEVICE_NAMED_PIPE に tty および pty デバイスを変更します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-800">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="d84f9-801">なる用の SSH の修正プログラム</span><span class="sxs-lookup"><span data-stu-id="d84f9-801">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="d84f9-802">Init デーモンに DrvFs マウントを移動する [GH 1862、1968 年に、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="d84f9-802">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="d84f9-803">次の NT シンボリック リンク DrvFs でサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-803">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="d84f9-804">ビルド 16184</span><span class="sxs-lookup"><span data-stu-id="d84f9-804">Build 16184</span></span>

<span data-ttu-id="d84f9-805">一般的な Windows ビルド 16184 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-805">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-806">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-806">Fixed</span></span>
- <span data-ttu-id="d84f9-807">Removed apt package maintenance task (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="d84f9-807">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="d84f9-808">表示されない node.js [GH 1840] で、Windows プロセスから出力を修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-808">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="d84f9-809">Lxcore [GH 1794] のアラインメント要件を緩和します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-809">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="d84f9-810">システム呼び出し数の AT_EMPTY_PATH フラグの処理を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-810">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="d84f9-811">ハンドルを開いた DrvFs ファイルを削除して未定義の動作 [GH 544,966,1357,1535,1615] ファイルとが、問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-811">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="d84f9-812">/etc/ホストは Windows ホスト ファイル (%windir%\system32\drivers\etc\hosts) からエントリを継承ようになりました [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="d84f9-812">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="d84f9-813">ビルド 16179</span><span class="sxs-lookup"><span data-stu-id="d84f9-813">Build 16179</span></span>

<span data-ttu-id="d84f9-814">一般的な Windows ビルド 16179 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-814">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-815">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-815">Fixed</span></span>
- <span data-ttu-id="d84f9-816">WSL 変更はこの 1 週間です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-816">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="d84f9-817">ビルド 16176</span><span class="sxs-lookup"><span data-stu-id="d84f9-817">Build 16176</span></span>

<span data-ttu-id="d84f9-818">一般的な Windows ビルド 16176 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-818">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-819">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-819">Fixed</span></span>

- [<span data-ttu-id="d84f9-820">シリアル サポートを有効になっています。</span><span class="sxs-lookup"><span data-stu-id="d84f9-820">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="d84f9-821">IP ソケット オプションなる [GH 1116] が追加されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-821">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="d84f9-822">(ファイルのアップロードに nginx/PHP-FPM) 中の pwritev 関数の実装 [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="d84f9-822">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="d84f9-823">IP ソケット オプション IP_MULTICAST_IF & IPV6_MULTICAST_IF の追加 [GH 990]</span><span class="sxs-lookup"><span data-stu-id="d84f9-823">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="d84f9-824">IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP ソケット オプションのサポート [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="d84f9-824">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="d84f9-825">アプリのノード、traceroute、dig、nslookup、ホストの IP (V6) _MTU ソケット オプションが追加されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-825">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="d84f9-826">IP ソケット オプション IPV6_UNICAST_HOPS が追加されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-826">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="d84f9-827">ファイル システムの機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-827">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="d84f9-828">UNC パスをマウントをします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-828">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="d84f9-829">Drvfs で CDFS サポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-829">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="d84f9-830">Drvfs でネットワーク ファイル システムのアクセス許可を正しく処理します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-830">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="d84f9-831">Drvfs にリモート ドライブのサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-831">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="d84f9-832">FAT を有効にする drvfs のサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-832">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="d84f9-833">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-833">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-834">成る結果</span><span class="sxs-lookup"><span data-stu-id="d84f9-834">LTP Results</span></span>
<span data-ttu-id="d84f9-835">15042 以降変更なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-835">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="d84f9-836">ビルド 16170</span><span class="sxs-lookup"><span data-stu-id="d84f9-836">Build 16170</span></span>

<span data-ttu-id="d84f9-837">一般的な Windows ビルド 16170 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-837">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="d84f9-838">新しいリリースしました[ブログの投稿](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)WSL をテストする取り組みについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-838">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="d84f9-839">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-839">Fixed</span></span>

- <span data-ttu-id="d84f9-840">サポートのソケット オプション IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="d84f9-840">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="d84f9-841">PTRACE_OLDSETOPTIONS のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-841">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="d84f9-842">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="d84f9-842">[GH 1692]</span></span>
- <span data-ttu-id="d84f9-843">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-843">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-844">成る結果</span><span class="sxs-lookup"><span data-stu-id="d84f9-844">LTP Results</span></span>
<span data-ttu-id="d84f9-845">15042 以降変更なし</span><span class="sxs-lookup"><span data-stu-id="d84f9-845">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="d84f9-846">ビルドを Windows 10 15046 Creators Update</span><span class="sxs-lookup"><span data-stu-id="d84f9-846">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="d84f9-847">これ以上の WSL 修正プログラムや Windows 10 Creators Update に含める予定されている機能があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-847">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="d84f9-848">WSL のリリース ノートは、次の主要な Windows 更新プログラムを対象とする追加機能を今後数週間で再開されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-848">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="d84f9-849">一般的な Windows ビルド 15046 と将来の詳細についてはリリースのアクセス、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-849">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="d84f9-850">ビルド 15042</span><span class="sxs-lookup"><span data-stu-id="d84f9-850">Build 15042</span></span>

<span data-ttu-id="d84f9-851">一般的な Windows ビルド 15042 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-851">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-852">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-852">Fixed</span></span>

- <span data-ttu-id="d84f9-853">終わるパスを削除するときに、デッドロックの解決"..."</span><span class="sxs-lookup"><span data-stu-id="d84f9-853">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="d84f9-854">問題を修正しました、FIONBIO [GH 1683] 成功した場合に 0 が返されない</span><span class="sxs-lookup"><span data-stu-id="d84f9-854">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="d84f9-855">Inet データグラム ソケットの長さが 0 の読み取りで問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-855">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="d84f9-856">Drvfs inode 参照 [GH 1675] 内での競合状態が原因でデッドロックが発生を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-856">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="d84f9-857">Unix ソケット補助的なデータの拡張サポートSCM_CREDENTIALS と SCM_RIGHTS [GH 514、613、1326]</span><span class="sxs-lookup"><span data-stu-id="d84f9-857">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="d84f9-858">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-858">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-859">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-859">LTP Results:</span></span>
<span data-ttu-id="d84f9-860">テストの成功の数:737</span><span class="sxs-lookup"><span data-stu-id="d84f9-860">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="d84f9-861">不合格数 (失敗、スキップされたなど.)。255</span><span class="sxs-lookup"><span data-stu-id="d84f9-861">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="d84f9-862">ビルド 15031</span><span class="sxs-lookup"><span data-stu-id="d84f9-862">Build 15031</span></span>

<span data-ttu-id="d84f9-863">一般的な Windows ビルド 15031 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-863">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-864">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-864">Fixed</span></span>

- <span data-ttu-id="d84f9-865">Time(2) が誤動作が散発的バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-865">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="d84f9-866">修正され、発行場所 \* syscall を組み合わせて使用される信号のマスクが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-866">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="d84f9-867">WSL プロセスの作成の通知では、完全なコマンドラインの長さを返すようになりました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-867">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="d84f9-868">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="d84f9-868">[GH 1632]</span></span>
- <span data-ttu-id="d84f9-869">WSL は、今すぐ ptrace を GDB がハングすることによってスレッドの終了を報告します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-869">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="d84f9-870">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="d84f9-870">[GH 1196]</span></span>
- <span data-ttu-id="d84f9-871">負荷の高い tmux IO 後 pty がハング、バグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-871">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="d84f9-872">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="d84f9-872">[GH 1358]</span></span>
- <span data-ttu-id="d84f9-873">多くのシステム コール (futex、semtimedop、参照のこと、sigtimedwait、itimer、timer_create) での固定のタイムアウトの検証</span><span class="sxs-lookup"><span data-stu-id="d84f9-873">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="d84f9-874">追加された eventfd EFD_SEMAPHORE サポート [GH 452]</span><span class="sxs-lookup"><span data-stu-id="d84f9-874">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="d84f9-875">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-875">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-876">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-876">LTP Results:</span></span>
<span data-ttu-id="d84f9-877">テストの成功の数:737</span><span class="sxs-lookup"><span data-stu-id="d84f9-877">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="d84f9-878">不合格数 (失敗、スキップされたなど.)。255</span><span class="sxs-lookup"><span data-stu-id="d84f9-878">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d84f9-879">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-879">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="d84f9-880">ビルド 15025</span><span class="sxs-lookup"><span data-stu-id="d84f9-880">Build 15025</span></span>

<span data-ttu-id="d84f9-881">一般的な Windows ビルド 15025 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-881">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-882">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-882">Fixed</span></span>

- <span data-ttu-id="d84f9-883">その壊れて grep 2.27 [GH 1578] バグの修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-883">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="d84f9-884">実装された EFD_SEMAPHORE フラグ eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="d84f9-884">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="d84f9-885">/Proc/[pid]/net ipv6_route の実装 [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="d84f9-885">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="d84f9-886">シグナル ドリブン unix ストリーム ソケット [GH 393、68] の IO のサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-886">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="d84f9-887">F_GETPIPE_SZ と F_SETPIPE_SZ [GH 1012] サポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-887">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="d84f9-888">Recvmmsg() syscall [GH 1531] の実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-888">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="d84f9-889">Epoll_wait() でした [GH 1609] を待っているバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-889">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="d84f9-890">/Proc/version_signature を実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-890">Implement /proc/version_signature</span></span>
- <span data-ttu-id="d84f9-891">Tee syscall はエラーを両方のファイル記述子が同じパイプを参照している場合に返すようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-891">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="d84f9-892">Unix ソケット SO_PEERCRED に実装されている適切な動作</span><span class="sxs-lookup"><span data-stu-id="d84f9-892">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="d84f9-893">固定 tkill syscall 無効なパラメーターの処理</span><span class="sxs-lookup"><span data-stu-id="d84f9-893">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="d84f9-894">Drvfs の preformace の増加への変更</span><span class="sxs-lookup"><span data-stu-id="d84f9-894">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="d84f9-895">Ruby の IO のブロックの軽微な修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-895">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="d84f9-896">固定の recvmsg() MSG_DONTWAIT フラグ inet ソケット [GH 1296] の EINVAL を返す</span><span class="sxs-lookup"><span data-stu-id="d84f9-896">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="d84f9-897">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-897">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-898">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-898">LTP Results:</span></span>
<span data-ttu-id="d84f9-899">テストの成功の数:732</span><span class="sxs-lookup"><span data-stu-id="d84f9-899">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="d84f9-900">不合格数 (失敗、スキップされたなど.)。255</span><span class="sxs-lookup"><span data-stu-id="d84f9-900">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d84f9-901">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-901">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="d84f9-902">ビルド 15019</span><span class="sxs-lookup"><span data-stu-id="d84f9-902">Build 15019</span></span>

<span data-ttu-id="d84f9-903">一般的な Windows ビルド 15019 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-903">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-904">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-904">Fixed</span></span>

- <span data-ttu-id="d84f9-905">CPU 使用率を正しく報告されるバグを修正したければ (945、971 は GH 823) などのツールの詳しい情報</span><span class="sxs-lookup"><span data-stu-id="d84f9-905">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="d84f9-906">既存の O_TRUNC で open() の呼び出し時にファイル inotify ようになりました IN_OPEN 前に、IN_MODIFY が生成されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-906">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="d84f9-907">Unix ソケット getsockopt SO_ERROR postgress [GH 61、1354] を有効にするための修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-907">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="d84f9-908">GO 言語の実装の説明が</span><span class="sxs-lookup"><span data-stu-id="d84f9-908">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="d84f9-909">Apt get パッケージ更新プログラムのバック グラウンド タスク今すぐ表示せずに実行ビューから</span><span class="sxs-lookup"><span data-stu-id="d84f9-909">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="d84f9-910">Ipv6 localhost (Spring-Framework(Java) 失敗) のスコープをクリアします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-910">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="d84f9-911">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-911">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-912">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-912">LTP Results:</span></span>
<span data-ttu-id="d84f9-913">テストの成功の数:714</span><span class="sxs-lookup"><span data-stu-id="d84f9-913">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="d84f9-914">不合格数 (失敗、スキップされたなど.)。249</span><span class="sxs-lookup"><span data-stu-id="d84f9-914">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="d84f9-915">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-915">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="d84f9-916">ビルド 15014</span><span class="sxs-lookup"><span data-stu-id="d84f9-916">Build 15014</span></span>

<span data-ttu-id="d84f9-917">一般的な Windows ビルド 15014 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-917">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-918">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-918">Fixed</span></span>

- <span data-ttu-id="d84f9-919">意図したようになりました Ctrl + C</span><span class="sxs-lookup"><span data-stu-id="d84f9-919">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="d84f9-920">たければと ps auxw ここで表示する適切なリソース使用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="d84f9-920">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="d84f9-921">NT 例外シグナルの基本的な変換です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-921">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="d84f9-922">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="d84f9-922">(GH #513)</span></span>
- <span data-ttu-id="d84f9-923">EINVAL (GH #1571) ではなく容量が不足した場合、この fallocate は、今すぐ ENOSPC で失敗しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-923">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="d84f9-924">追加された/proc/sys/kernel/sem します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-924">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="d84f9-925">実装された semop と semtimedop システム コール</span><span class="sxs-lookup"><span data-stu-id="d84f9-925">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="d84f9-926">IP_RECVTOS & IPV6_RECVTCLASS ソケット オプション (GH 69) を使用して固定 nslookup のエラー</span><span class="sxs-lookup"><span data-stu-id="d84f9-926">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="d84f9-927">IP_RECVTTL と IPV6_RECVHOPLIMIT ソケット オプションのサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-927">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="d84f9-928">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-928">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-929">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-929">LTP Results:</span></span>
<span data-ttu-id="d84f9-930">テストの成功の数:709</span><span class="sxs-lookup"><span data-stu-id="d84f9-930">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="d84f9-931">不合格数 (失敗、スキップされたなど.)。255</span><span class="sxs-lookup"><span data-stu-id="d84f9-931">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d84f9-932">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-932">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="d84f9-933">Syscall の概要</span><span class="sxs-lookup"><span data-stu-id="d84f9-933">Syscall Summary</span></span>
<span data-ttu-id="d84f9-934">合計 Syscall:384</span><span class="sxs-lookup"><span data-stu-id="d84f9-934">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="d84f9-935">実装の合計:235</span><span class="sxs-lookup"><span data-stu-id="d84f9-935">Total Implemented: 235</span></span> </br>
<span data-ttu-id="d84f9-936">スタブの合計:22</span><span class="sxs-lookup"><span data-stu-id="d84f9-936">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="d84f9-937">合計が実装されていません。127</span><span class="sxs-lookup"><span data-stu-id="d84f9-937">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="d84f9-938">詳細な内訳</span><span class="sxs-lookup"><span data-stu-id="d84f9-938">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="d84f9-939">ビルド 15007</span><span class="sxs-lookup"><span data-stu-id="d84f9-939">Build 15007</span></span>

<span data-ttu-id="d84f9-940">一般的な Windows ビルド 15007 に関する情報を参照してください、 [Windows ブログ]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-940">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="d84f9-941">既知の問題</span><span class="sxs-lookup"><span data-stu-id="d84f9-941">Known Issue</span></span>

- <span data-ttu-id="d84f9-942">コンソールがいくつかの ctrl キーを認識しない既知のバグがある +<key>入力します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-942">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="d84f9-943">これには、標準の 'c' keypress として機能するを ctrl キーを押しながら c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-943">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="d84f9-944">対応策 :代替キーを Ctrl キーを押しながら C キーにマップします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-944">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="d84f9-945">たとえば、マップに Ctrl + C には、Ctrl + K は:`stty intr \^k`します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-945">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="d84f9-946">このマッピングは、ターミナルごとおよび実行する必要があります*すべて*時間 bash を起動します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-946">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="d84f9-947">ユーザーを含めるには、このオプションを調べることができます、 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="d84f9-947">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="d84f9-948">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-948">Fixed</span></span>

- <span data-ttu-id="d84f9-949">WSL を実行して、CPU コアの 100% を消費は、問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-949">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="d84f9-950">ソケットのオプション、IP_PKTINFO IPV6_RECVPKTINFO のようになりました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-950">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="d84f9-951">(987 GH # の 851)</span><span class="sxs-lookup"><span data-stu-id="d84f9-951">(GH #851, 987)</span></span>
- <span data-ttu-id="d84f9-952">Truncate lxcore 16 バイトにネットワーク インターフェイスの物理アドレス (GH #1452、1414、1343、468、308)</span><span class="sxs-lookup"><span data-stu-id="d84f9-952">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="d84f9-953">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-954">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-954">LTP Results:</span></span>
<span data-ttu-id="d84f9-955">テストの成功の数:709</span><span class="sxs-lookup"><span data-stu-id="d84f9-955">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="d84f9-956">不合格数 (失敗、スキップされたなど.)。255</span><span class="sxs-lookup"><span data-stu-id="d84f9-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="d84f9-957">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="d84f9-958">ビルド 15002</span><span class="sxs-lookup"><span data-stu-id="d84f9-958">Build 15002</span></span>

<span data-ttu-id="d84f9-959">一般的な Windows ビルド 15002 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-959">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="d84f9-960">既知の問題</span><span class="sxs-lookup"><span data-stu-id="d84f9-960">Known Issue</span></span>

<span data-ttu-id="d84f9-961">2 つの既知の問題:</span><span class="sxs-lookup"><span data-stu-id="d84f9-961">Two known issues:</span></span>
- <span data-ttu-id="d84f9-962">コンソールがいくつかの ctrl キーを認識しない既知のバグがある +<key>入力します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-962">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="d84f9-963">これには、標準の 'c' keypress として機能するを ctrl キーを押しながら c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-963">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="d84f9-964">対応策 :代替キーを Ctrl キーを押しながら C キーにマップします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-964">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="d84f9-965">たとえば、マップに Ctrl + C には、Ctrl + K は:`stty intr \^k`します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-965">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="d84f9-966">このマッピングは、ターミナルごとおよび実行する必要があります*すべて*時間 bash を起動します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-966">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="d84f9-967">ユーザーを含めるには、このオプションを調べることができます、 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="d84f9-967">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="d84f9-968">WSL の実行中にシステム スレッドは CPU コアの 100% を消費します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-968">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="d84f9-969">根本原因はアドレス指定され、内部的に固定します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-969">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="d84f9-970">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-970">Fixed</span></span>

- <span data-ttu-id="d84f9-971">すべての bash セッションを同じアクセス許可レベルで作成されましたする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-971">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="d84f9-972">さまざまなレベルでセッションを開始しようとしてがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-972">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="d84f9-973">つまり、管理者と管理者以外のコンソールを同時に実行できません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-973">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="d84f9-974">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="d84f9-974">(GH #626)</span></span>
<br/>
- <span data-ttu-id="d84f9-975">次の NETLINK_ROUTE メッセージを実装 (Windows の管理者権限が必要)</span><span class="sxs-lookup"><span data-stu-id="d84f9-975">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="d84f9-976">RTM_NEWADDR (サポート`ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="d84f9-976">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="d84f9-977">RTM_NEWROUTE (サポート`ip route add`)</span><span class="sxs-lookup"><span data-stu-id="d84f9-977">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="d84f9-978">RTM_DELADDR (サポート`ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="d84f9-978">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="d84f9-979">RTM_DELROUTE (サポート`ip route del`)</span><span class="sxs-lookup"><span data-stu-id="d84f9-979">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="d84f9-980">スケジュールされたタスクがパッケージを更新するためのチェックは、従量制課金接続 (GH #1371) では実行されなく</span><span class="sxs-lookup"><span data-stu-id="d84f9-980">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="d84f9-981">パイプの取得が詰まっているつまり bash-c エラーを修正しました"ls alR/"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="d84f9-981">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="d84f9-982">実装された TCP_KEEPCNT ソケット オプション (GH #843)</span><span class="sxs-lookup"><span data-stu-id="d84f9-982">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="d84f9-983">実装された IP_MTU_DISCOVER INET ソケット オプション (GH #720、717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="d84f9-983">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="d84f9-984">NT パス参照を init から NT バイナリを実行する従来の機能を削除します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-984">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="d84f9-985">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="d84f9-985">(GH #1325)</span></span>
- <span data-ttu-id="d84f9-986">開発/グループ/その他の読み取りアクセス (0644) (GH #1321) を許可する kmsg のモードを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-986">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="d84f9-987">実装された/proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="d84f9-987">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="d84f9-988">プロセスの開始時刻が年 2432 (GH #974) を示すエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-988">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="d84f9-989">スイッチの既定環境変数を TERM xterm 256color (GH #1446) を</span><span class="sxs-lookup"><span data-stu-id="d84f9-989">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="d84f9-990">変更のコミットを処理する方法は、プロセスの分岐の中に計算されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-990">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="d84f9-991">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="d84f9-991">(GH #1286)</span></span>
- <span data-ttu-id="d84f9-992">実装された受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-992">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="d84f9-993">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="d84f9-993">(GH #1286)</span></span>
- <span data-ttu-id="d84f9-994">実装された/proc/net/route ファイル (GH #69)</span><span class="sxs-lookup"><span data-stu-id="d84f9-994">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="d84f9-995">ショートカット名がない正しくエラーを修正しました (GH #696) のローカライズ</span><span class="sxs-lookup"><span data-stu-id="d84f9-995">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="d84f9-996">プログラムのヘッダーが正しく検証ロジックを解析する固定 elf 必要があります (以下に) 設定される。 します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-996">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="d84f9-997">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="d84f9-997">(GH #1048)</span></span>
- <span data-ttu-id="d84f9-998">詳しい情報、sysfs、cgroupfs、および binfmtfs (GH #1378) 実装 statfs コールバック</span><span class="sxs-lookup"><span data-stu-id="d84f9-998">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="d84f9-999">(GH #1184 も GH #1193 で説明) を閉じない固定の AptPackageIndexUpdate windows</span><span class="sxs-lookup"><span data-stu-id="d84f9-999">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="d84f9-1000">ASLR パーソナリティ ADDR_NO_RANDOMIZE サポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1000">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="d84f9-1001">(GH #1148、1128)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1001">(GH #1148, 1128)</span></span>
- <span data-ttu-id="d84f9-1002">強化された PTRACE_GETSIGINFO、AV (GH #875) 中に適切な gdb スタック トレースの SIGSEGV</span><span class="sxs-lookup"><span data-stu-id="d84f9-1002">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="d84f9-1003">Patchelf バイナリ elf が不要になった解析が失敗します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1003">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="d84f9-1004">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1004">(GH #471)</span></span>
- <span data-ttu-id="d84f9-1005">/Etc/resolv.conf (GH #416、1350) に VPN DNS が反映されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1005">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="d84f9-1006">TCP の機能強化より信頼性の高いデータの転送を閉じます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1006">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="d84f9-1007">(GH #610 616、1025、1335)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1007">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="d84f9-1008">適切なエラーを返すようになりましたコード ファイルが多すぎる場合に、(EMFILE) が開かれます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1008">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="d84f9-1009">(GH #1126、2090)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1009">(GH #1126, 2090)</span></span>
- <span data-ttu-id="d84f9-1010">Windows の監査ログから報告プロセスで、イメージの名前は、監査を作成します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1010">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="d84f9-1011">Bash ウィンドウ内から bash.exe を起動するときに正常に失敗します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1011">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="d84f9-1012">相互運用機能と、追加のエラー メッセージが LxFs (つまり notepad.exe .bashrc) の下の作業ディレクトリにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1012">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="d84f9-1013">Windows のパスが WSL で切り捨てられました問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1013">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="d84f9-1014">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1015">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1015">LTP Results:</span></span>
<span data-ttu-id="d84f9-1016">テストの成功の数:690</span><span class="sxs-lookup"><span data-stu-id="d84f9-1016">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="d84f9-1017">不合格数 (失敗、スキップされたなど.)。274</span><span class="sxs-lookup"><span data-stu-id="d84f9-1017">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="d84f9-1018">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1019">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1019">Syscall Support</span></span>
<span data-ttu-id="d84f9-1020">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1020">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1021">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1021">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="d84f9-1022">ビルド 14986</span><span class="sxs-lookup"><span data-stu-id="d84f9-1022">Build 14986</span></span>

<span data-ttu-id="d84f9-1023">一般的な Windows ビルド 14986 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1023">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1024">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1024">Fixed</span></span>

- <span data-ttu-id="d84f9-1025">固定のバグチェック Netlink と Pty Ioctl</span><span class="sxs-lookup"><span data-stu-id="d84f9-1025">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="d84f9-1026">カーネルのバージョンが現在 4.4.0-43 Xenial との整合性を報告します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1026">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="d84f9-1027">Bash.exe は入力の指示を起動 ' nul:' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1027">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="d84f9-1028">詳しい情報 (GH # の 967) で、スレッド Id を正しく今すぐ報告</span><span class="sxs-lookup"><span data-stu-id="d84f9-1028">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="d84f9-1029">IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |IN_ISDIR フラグが inotify_add_watch() (GH #1280) でサポートされています</span><span class="sxs-lookup"><span data-stu-id="d84f9-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="d84f9-1030">実装 timer_create と関連するシステムの呼び出し。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1030">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="d84f9-1031">これにより、GHC サポート (GH #307)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1031">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="d84f9-1032">Ping が 0.000ms (GH #1296) の時刻を返す問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1032">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="d84f9-1033">ファイルが多すぎますが開かれたときに、適切なエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1033">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="d84f9-1034">WSL で Netlink の要求のネットワーク インターフェイスのデータは失敗によって変更できるインターフェイスのハードウェアのアドレスが 32 バイト (など、Teredo インターフェイス) の場合の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1034">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="d84f9-1035">Linux"ip"ユーティリティが WSL が 32 バイトのハードウェアのアドレスを報告する場合、クラッシュがバグを含むことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1035">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="d84f9-1036">これは、"ip"、WSL ではないのバグです。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1036">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="d84f9-1037">ハードウェアのアドレスを印刷する、"ip"ユーティリティ ハードコード化文字列バッファーの長さが使用し、そのバッファーが小さすぎる 32 バイトのハードウェアのアドレスを印刷します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1037">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="d84f9-1038">追加の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1038">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1039">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1039">LTP Results:</span></span>
<span data-ttu-id="d84f9-1040">テストの成功の数:669</span><span class="sxs-lookup"><span data-stu-id="d84f9-1040">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="d84f9-1041">不合格数 (失敗、スキップされたなど.)。258</span><span class="sxs-lookup"><span data-stu-id="d84f9-1041">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="d84f9-1042">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1042">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1043">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1043">Syscall Support</span></span>
<span data-ttu-id="d84f9-1044">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1044">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1045">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1045">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="d84f9-1046">ビルド 14971</span><span class="sxs-lookup"><span data-stu-id="d84f9-1046">Build 14971</span></span>

<span data-ttu-id="d84f9-1047">一般的な Windows ビルド 14971 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1047">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1048">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1048">Fixed</span></span>

 - <span data-ttu-id="d84f9-1049">コントロールが及ばないのための更新はありません Windows Subsystem for Linux のビルドでします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1049">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="d84f9-1050">次回のリリースでは、定期的にスケジュールされた更新プログラムが再開されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1050">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1051">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1051">LTP Results:</span></span>
<span data-ttu-id="d84f9-1052">14965 から変更されていません</span><span class="sxs-lookup"><span data-stu-id="d84f9-1052">Unchanged from 14965</span></span> </br>
<span data-ttu-id="d84f9-1053">テストの成功の数:664</span><span class="sxs-lookup"><span data-stu-id="d84f9-1053">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="d84f9-1054">不合格数 (失敗、スキップされたなど.)。263</span><span class="sxs-lookup"><span data-stu-id="d84f9-1054">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d84f9-1055">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1055">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="d84f9-1056">ビルド 14965</span><span class="sxs-lookup"><span data-stu-id="d84f9-1056">Build 14965</span></span>

<span data-ttu-id="d84f9-1057">一般的な Windows ビルド 14965 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1057">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1058">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1058">Fixed</span></span>

- <span data-ttu-id="d84f9-1059">Netlink のサポートはソケット NETLINK_ROUTE プロトコルの RTM_GETLINK と RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1059">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="d84f9-1060">により、ネットワークの列挙体のコマンドを示している ifconfig と ip</span><span class="sxs-lookup"><span data-stu-id="d84f9-1060">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="d84f9-1061">詳細についてを参照、 [WSL ネットワー キング ブログの投稿](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1061">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="d84f9-1062">/sbin が既定では、ユーザーの path に追加</span><span class="sxs-lookup"><span data-stu-id="d84f9-1062">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="d84f9-1063">NT ユーザー パスのようになりました (つまりここで入力できます notepad.exe System32 を Linux パスに追加せずに) 既定で WSL パスに追加</span><span class="sxs-lookup"><span data-stu-id="d84f9-1063">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="d84f9-1064">/Proc/sys/kernel/cap_last_cap サポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1064">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="d84f9-1065">現在の作業ディレクトリには、ansi 以外の文字 (GH #1254) が含まれている場合は NT バイナリ WSL から起動することはようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1065">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="d84f9-1066">切断された unix ストリーム ソケットのシャット ダウンを許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1066">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="d84f9-1067">PR_GET_PDEATHSIG サポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1067">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="d84f9-1068">あるサポートが追加されました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1068">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="d84f9-1069">パイプの取得が詰まっているつまり bash-c エラーを修正しました"ls alR/"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1069">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="d84f9-1070">現在のターミナルに接続する要求の処理。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1070">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="d84f9-1071">/Proc/のマーク<pid>/oom_score_adj を書き込み可能です。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1071">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="d84f9-1072">/Sys/fs/cgroup フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1072">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="d84f9-1073">sched_setaffinity 関係ビット マスクの数を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1073">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="d84f9-1074">インタープリターのパスより小さい 64 文字を指定する必要がありますと誤った前提を ELF 検証ロジックを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1074">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="d84f9-1075">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1075">(GH #743)</span></span>
- <span data-ttu-id="d84f9-1076">開いているファイル記述子は、コンソール ウィンドウを開いて (GH #1187) を保持できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1076">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="d84f9-1077">末尾にスラッシュをターゲットの名前 (GH #1008) rename() が失敗しました Fixeed エラー</span><span class="sxs-lookup"><span data-stu-id="d84f9-1077">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="d84f9-1078">/Proc/net/dev ファイルを実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1078">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="d84f9-1079">固定 0.000ms タイマーの解決のために ping を実行します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1079">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="d84f9-1080">実装された/proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1080">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="d84f9-1081">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1081">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1082">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1082">LTP Results:</span></span>
<span data-ttu-id="d84f9-1083">テストの成功の数:664</span><span class="sxs-lookup"><span data-stu-id="d84f9-1083">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="d84f9-1084">不合格数 (失敗、スキップされたなど.)。263</span><span class="sxs-lookup"><span data-stu-id="d84f9-1084">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d84f9-1085">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1085">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="d84f9-1086">ビルド 14959</span><span class="sxs-lookup"><span data-stu-id="d84f9-1086">Build 14959</span></span>

<span data-ttu-id="d84f9-1087">一般的な Windows ビルド 14959 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1087">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1088">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1088">Fixed</span></span>

- <span data-ttu-id="d84f9-1089">Windows の Pico プロセス通知機能強化。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1089">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="d84f9-1090">詳細情報について、 [WSL ブログ](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1090">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="d84f9-1091">Windows の相互運用性と安定性の向上</span><span class="sxs-lookup"><span data-stu-id="d84f9-1091">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="d84f9-1092">0x80070057 エンタープライズ データ保護 (EDP) を有効にすると、bash.exe を起動するときにエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1092">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="d84f9-1093">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1093">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1094">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1094">LTP Results:</span></span>
<span data-ttu-id="d84f9-1095">テストの成功の数:665</span><span class="sxs-lookup"><span data-stu-id="d84f9-1095">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d84f9-1096">不合格数 (失敗、スキップされたなど.)。263</span><span class="sxs-lookup"><span data-stu-id="d84f9-1096">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d84f9-1097">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1097">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="d84f9-1098">ビルド 14955</span><span class="sxs-lookup"><span data-stu-id="d84f9-1098">Build 14955</span></span>

<span data-ttu-id="d84f9-1099">一般的な Windows ビルド 14955 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1099">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1100">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1100">Fixed</span></span>

 - <span data-ttu-id="d84f9-1101">コントロールが及ばないのための更新はありません Windows Subsystem for Linux のビルドでします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1101">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="d84f9-1102">次回のリリースでは、定期的にスケジュールされた更新プログラムが再開されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1102">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1103">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1103">LTP Results:</span></span>
<span data-ttu-id="d84f9-1104">テストの成功の数:665</span><span class="sxs-lookup"><span data-stu-id="d84f9-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d84f9-1105">不合格数 (失敗、スキップされたなど.)。263</span><span class="sxs-lookup"><span data-stu-id="d84f9-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d84f9-1106">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="d84f9-1107">ビルド 14951</span><span class="sxs-lookup"><span data-stu-id="d84f9-1107">Build 14951</span></span>

<span data-ttu-id="d84f9-1108">一般的な Windows ビルド 14951 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1108">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="d84f9-1109">新機能:Windows または Ubuntu の相互運用性</span><span class="sxs-lookup"><span data-stu-id="d84f9-1109">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="d84f9-1110">WSL のコマンドラインから直接 Windows バイナリを呼び出すようになりましたことができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1110">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="d84f9-1111">これにより、ユーザーは、Windows 環境と考えられるされていない方法でシステムとやり取りできるようにします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1111">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="d84f9-1112">簡単な例として、次のコマンドを実行することはようになりました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1112">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="d84f9-1113">詳細についてにあります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1113">More information can be found at:</span></span>

- [<span data-ttu-id="d84f9-1114">WSL の相互運用機能チームのブログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1114">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="d84f9-1115">相互運用機能の MSDN ドキュメント</span><span class="sxs-lookup"><span data-stu-id="d84f9-1115">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="d84f9-1116">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1116">Fixed</span></span>

- <span data-ttu-id="d84f9-1117">WSL のすべての新しいインスタンスを Ubuntu 16.04 (Xenial) がインストールされているようになりました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1117">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="d84f9-1118">14.04 (頼りになる) の既存のインスタンスを持つユーザーは自動的にアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1118">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="d84f9-1119">インストール中に設定されたロケールが表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1119">Locale set during install is now displayed</span></span>
- <span data-ttu-id="d84f9-1120">バグが常にではありませんが、WSL プロセスをファイルにリダイレクトする場所のターミナル強化機能します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1120">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="d84f9-1121">コンソールの有効期間は bash.exe 有効期間に関連付けられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1121">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="d84f9-1122">コンソール ウィンドウのサイズがバッファー サイズではなく、表示サイズを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1122">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="d84f9-1123">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1123">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1124">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1124">LTP Results:</span></span>
<span data-ttu-id="d84f9-1125">テストの成功の数:665</span><span class="sxs-lookup"><span data-stu-id="d84f9-1125">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d84f9-1126">不合格数 (失敗、スキップされたなど.)。263</span><span class="sxs-lookup"><span data-stu-id="d84f9-1126">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d84f9-1127">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1127">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="d84f9-1128">ビルド 14946</span><span class="sxs-lookup"><span data-stu-id="d84f9-1128">Build 14946</span></span>

<span data-ttu-id="d84f9-1129">一般的な Windows ビルド 14946 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1129">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1130">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1130">Fixed</span></span>

- <span data-ttu-id="d84f9-1131">スペースや引用符が含まれている NT ユーザー名とユーザー用の WSL ユーザー アカウントの作成を妨げる問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1131">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="d84f9-1132">Stat でディレクトリのリンク数の場合は 0 を返すには、VolFs と DrvFs を変更します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1132">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="d84f9-1133">IPV6_MULTICAST_HOPS ソケット オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1133">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="d84f9-1134">Tty あたりの I/O ループを 1 つのコンソールに制限されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1134">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="d84f9-1135">例: 次のコマンドは、考えられる。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1135">Example: the following command is possible:</span></span>
  - <span data-ttu-id="d84f9-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="d84f9-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="d84f9-1137">/proc/cpuinfo (GH #1115) にタブ スペースに置換します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1137">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="d84f9-1138">Windows のマウントされたボリュームに一致する名前を持つ mountinfo に DrvFs が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1138">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="d84f9-1139">/home と/root mountinfo 正しい名前で表示されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1139">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="d84f9-1140">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1140">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1141">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1141">LTP Results:</span></span>
<span data-ttu-id="d84f9-1142">テストの成功の数:665</span><span class="sxs-lookup"><span data-stu-id="d84f9-1142">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d84f9-1143">不合格数 (失敗、スキップされたなど.)。263</span><span class="sxs-lookup"><span data-stu-id="d84f9-1143">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d84f9-1144">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1144">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="d84f9-1145">ビルド 14942</span><span class="sxs-lookup"><span data-stu-id="d84f9-1145">Build 14942</span></span>

<span data-ttu-id="d84f9-1146">一般的な Windows ビルド 14942 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/onefourninefourtwoooooo)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1146">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1147">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1147">Fixed</span></span>

- <span data-ttu-id="d84f9-1148">メモリを含む、"試行された実行の NOEXECUTE"SSH がブロックしてクラッシュのネットワークのアドレス指定、バグチェック数</span><span class="sxs-lookup"><span data-stu-id="d84f9-1148">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="d84f9-1149">inotifiy サポート DrvFs 上の Windows アプリケーションから生成された通知がようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1149">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="d84f9-1150">Mongod の TCP_KEEPIDLE と TCP_KEEPINTVL を実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1150">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="d84f9-1151">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1151">(GH #695)</span></span>
- <span data-ttu-id="d84f9-1152">Pivot_root システム コールを実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1152">Implement the pivot_root system call</span></span>
- <span data-ttu-id="d84f9-1153">SO_DONTROUTE のソケット オプションを実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1153">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="d84f9-1154">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1154">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="d84f9-1155">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1155">LTP Results:</span></span>
<span data-ttu-id="d84f9-1156">テストの成功の数:665</span><span class="sxs-lookup"><span data-stu-id="d84f9-1156">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="d84f9-1157">不合格数 (失敗、スキップされたなど.)。263</span><span class="sxs-lookup"><span data-stu-id="d84f9-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="d84f9-1158">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1159">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1159">Syscall Support</span></span>
<span data-ttu-id="d84f9-1160">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1160">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1161">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1161">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="d84f9-1162">ビルド 14936</span><span class="sxs-lookup"><span data-stu-id="d84f9-1162">Build 14936</span></span>

<span data-ttu-id="d84f9-1163">一般的な Windows ビルド 14936 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1163">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="d84f9-1164">注:WSL では、Ubuntu バージョン 16.04 (Xenial) Ubuntu 14.04 (信頼性) ではなくを今後のリリースでインストールします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1164">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="d84f9-1165">この変更は、内部関係者が (lxrun.exe/install または bash.exe の最初の実行) の新しいインスタンスのインストールに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1165">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="d84f9-1166">信頼性と既存のインスタンスは自動的にアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1166">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="d84f9-1167">ユーザーは、do リリース-アップグレード コマンドを使用して Xenial に頼りになる、イメージをアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1167">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="d84f9-1168">既知の問題</span><span class="sxs-lookup"><span data-stu-id="d84f9-1168">Known Issue</span></span>
<span data-ttu-id="d84f9-1169">WSL でソケットの実装によって問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1169">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="d84f9-1170">バグチェックでは、"試行された実行の NOEXECUTE MEMORY"のエラーでクラッシュとして出現します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1170">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="d84f9-1171">この問題の最も一般的な形では、ssh を使用する場合、クラッシュです。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1171">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="d84f9-1172">根本原因は、内部のビルドでは固定され、内部関係者に、できるだけ早い機会にプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1172">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="d84f9-1173">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1173">Fixed</span></span>

- <span data-ttu-id="d84f9-1174">Chroot システム コールの実装</span><span class="sxs-lookup"><span data-stu-id="d84f9-1174">Implemented the chroot system call</span></span>
- <span data-ttu-id="d84f9-1175">Inotify 改善~~DrvFs 上の Windows アプリケーションから生成された通知のサポートを含む~~</span><span class="sxs-lookup"><span data-stu-id="d84f9-1175">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="d84f9-1176">修正:Inotify は、この時点ではない Windows アプリケーションから送信された変更のサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1176">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="d84f9-1177">ソケットの IPV6 へのバインド::<port n> IPV6_V6ONLY ようになりました (GH #68、#157、#393、#460、#674、#740、#982、#996)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1177">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="d84f9-1178">Waitid systemcall の WNOWAIT 動作 (GH #638) を実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1178">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="d84f9-1179">のでおよび IP_TTL IP ソケット オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1179">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="d84f9-1180">長さ 0 の read() をすぐに返す必要があります (GH #975)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1180">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="d84f9-1181">.Tar ファイルで、NULL 終端文字が含まれていないファイル名とファイル名のプレフィックスを正しく処理します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1181">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="d84f9-1182">/dev/null epoll のサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1182">epoll support for /dev/null</span></span>
- <span data-ttu-id="d84f9-1183">/Dev/alarm タイム ソースを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1183">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="d84f9-1184">Bash-c をファイルにリダイレクトできるようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1184">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="d84f9-1185">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1185">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1186">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1186">LTP Results:</span></span>
<span data-ttu-id="d84f9-1187">テストの成功の数:664</span><span class="sxs-lookup"><span data-stu-id="d84f9-1187">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="d84f9-1188">不合格数 (失敗、スキップされたなど.)。264</span><span class="sxs-lookup"><span data-stu-id="d84f9-1188">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="d84f9-1189">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1189">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1190">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1190">Syscall Support</span></span>
<span data-ttu-id="d84f9-1191">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1191">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1192">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1192">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="d84f9-1193">ビルド 14931</span><span class="sxs-lookup"><span data-stu-id="d84f9-1193">Build 14931</span></span>

<span data-ttu-id="d84f9-1194">一般的な Windows ビルド 14931 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1194">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1195">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1195">Fixed</span></span>

 - <span data-ttu-id="d84f9-1196">コントロールが及ばないのための更新はありません Windows Subsystem for Linux のビルドでします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1196">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="d84f9-1197">次のリリースで定期的にスケジュールされた更新プログラムが再開されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1197">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="d84f9-1198">ビルド 14926</span><span class="sxs-lookup"><span data-stu-id="d84f9-1198">Build 14926</span></span>

<span data-ttu-id="d84f9-1199">一般的な Windows ビルド 14926 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1199">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1200">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1200">Fixed</span></span>

- <span data-ttu-id="d84f9-1201">Ping は管理者特権がないコンソール</span><span class="sxs-lookup"><span data-stu-id="d84f9-1201">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="d84f9-1202">現在サポートされても管理者特権のない Ping6</span><span class="sxs-lookup"><span data-stu-id="d84f9-1202">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="d84f9-1203">WSL で変更されたファイルの Inotify サポート。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1203">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="d84f9-1204">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1204">(GH #216)</span></span>
  - <span data-ttu-id="d84f9-1205">サポートされているフラグ:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1205">Flags supported:</span></span>
    - <span data-ttu-id="d84f9-1206">inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="d84f9-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="d84f9-1207">inotify_add_watch イベント:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="d84f9-1207">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="d84f9-1208">inotify_add_watch 属性:LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="d84f9-1208">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="d84f9-1209">出力を参照してください。LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="d84f9-1209">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="d84f9-1210">既知の問題:Windows アプリケーションからファイルを変更するすべてのイベントを生成しません</span><span class="sxs-lookup"><span data-stu-id="d84f9-1210">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="d84f9-1211">Unix ソケットになりました SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="d84f9-1211">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="d84f9-1212">成る結果:</span><span class="sxs-lookup"><span data-stu-id="d84f9-1212">LTP Results:</span></span>
<span data-ttu-id="d84f9-1213">テストの成功の数:651</span><span class="sxs-lookup"><span data-stu-id="d84f9-1213">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="d84f9-1214">不合格数 (失敗、スキップされたなど.)。258</span><span class="sxs-lookup"><span data-stu-id="d84f9-1214">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="d84f9-1215">成るテスト実行のログ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1215">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="d84f9-1216">ビルド 14915</span><span class="sxs-lookup"><span data-stu-id="d84f9-1216">Build 14915</span></span>

<span data-ttu-id="d84f9-1217">一般的な Windows ビルド 14915 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1217">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1218">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1218">Fixed</span></span>
-  <span data-ttu-id="d84f9-1219">Socketpair unix データグラム ソケット (GH #262)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1219">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="d84f9-1220">SO_REUSEADDR の Unix ソケットのサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1220">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="d84f9-1221">UNIX ソケット サポート:so_broadcast (GH #568)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1221">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="d84f9-1222">型 (GH #758、#546) の Unix ソケットのサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1222">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="d84f9-1223">Unix データグラム ソケットの送信、受信、およびシャット ダウンのサポートの追加</span><span class="sxs-lookup"><span data-stu-id="d84f9-1223">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="d84f9-1224">非固定アドレスに無効な mmap パラメーターの検証のためのバグチェックを修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1224">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="d84f9-1225">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1225">(GH #847)</span></span>
- <span data-ttu-id="d84f9-1226">中断のサポート]、[ターミナル状態の再開</span><span class="sxs-lookup"><span data-stu-id="d84f9-1226">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="d84f9-1227">TIOCPKT ioctl 画面ユーティリティ (GH #774) ブロックを解除するためのサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1227">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="d84f9-1228">既知の問題:関数キーが動作していません</span><span class="sxs-lookup"><span data-stu-id="d84f9-1228">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="d84f9-1229">解放されたメンバー 'ReaderReady' へのアクセスを LxpTimerFdWorkerRoutine (GH #814) を引き起こす可能性のある TimerFd するときの競合を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1229">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="d84f9-1230">Futex、アンケート、および同様の再開可能なシステムの呼び出しのサポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1230">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="d84f9-1231">追加されたバインド マウントのサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1231">Added bind mount support</span></span>
- <span data-ttu-id="d84f9-1232">マウントの名前空間のサポートの共有を解除します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1232">unshare for mount namespace support</span></span>
    - <span data-ttu-id="d84f9-1233">既知の問題:新しいマウント名前空間を作成するときに`unshare(CLONE_NEWNS)`現在の作業ディレクトリは引き続き古い名前空間を指す</span><span class="sxs-lookup"><span data-stu-id="d84f9-1233">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="d84f9-1234">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="d84f9-1234">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="d84f9-1235">ビルド 14905</span><span class="sxs-lookup"><span data-stu-id="d84f9-1235">Build 14905</span></span>

<span data-ttu-id="d84f9-1236">一般的な Windows ビルド 14905 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1236">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1237">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1237">Fixed</span></span>
- <span data-ttu-id="d84f9-1238">呼び出しは今すぐ再起動可能なシステムには、(GH #349、GH #520) がサポートされています</span><span class="sxs-lookup"><span data-stu-id="d84f9-1238">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="d84f9-1239">ディレクトリ]、[今すぐに運用を終了 (GH #650) へのシンボリック リンク</span><span class="sxs-lookup"><span data-stu-id="d84f9-1239">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="d84f9-1240">/Dev/random の実装の RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="d84f9-1240">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="d84f9-1241">/Proc/[pid] を実装/マウント、/proc/[pid]/mountinfo と/proc/[pid]/mountstats ファイル</span><span class="sxs-lookup"><span data-stu-id="d84f9-1241">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="d84f9-1242">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1242">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="d84f9-1243">ビルド 14901</span><span class="sxs-lookup"><span data-stu-id="d84f9-1243">Build 14901</span></span>
<span data-ttu-id="d84f9-1244">最初の内部関係者は、Windows 10 Anniversary Update のリリースの投稿に対してビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1244">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="d84f9-1245">一般的な Windows ビルド 14901 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1245">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1246">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1246">Fixed</span></span>
- <span data-ttu-id="d84f9-1247">末尾のスラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1247">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="d84f9-1248">などのコマンド`$ mv a/c/ a/b/`作業ようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1248">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="d84f9-1249">Ubuntu のロケールは、Windows ロケールに設定する必要がある場合に要求をインストールするようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1249">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="d84f9-1250">Ns フォルダーの詳しい情報のサポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1250">Procfs support for ns folder</span></span>
- <span data-ttu-id="d84f9-1251">マウントを追加し、tmpfs、詳しい情報と sysfs ファイル システムのマウントを解除</span><span class="sxs-lookup"><span data-stu-id="d84f9-1251">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="d84f9-1252">[At] の 32 ビットの ABI 署名 mknod を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1252">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="d84f9-1253">Unix ソケットのディスパッチ モデルに移動</span><span class="sxs-lookup"><span data-stu-id="d84f9-1253">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="d84f9-1254">INET ソケットの受信バッファー サイズ、setsockopt を使用して設定を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1254">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="d84f9-1255">実装 MSG_CMSG_CLOEXEC unix ソケットの受信メッセージのフラグ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1255">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="d84f9-1256">Linux プロセス stdin と stdout パイプ リダイレクト (GH 2)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1256">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="d84f9-1257">Cmd. で bash-c コマンドのパイプ処理では、します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1257">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="d84f9-1258">例: > dir |bash-c"grep foo"</span><span class="sxs-lookup"><span data-stu-id="d84f9-1258">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="d84f9-1259">Bash は、複数のページファイル (GH #538、#358) をシステムにインストールするようになりましたことができます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1259">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="d84f9-1260">INET ソケット バッファーの既定のサイズには、Ubuntu の既定の設定の一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1260">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="d84f9-1261">Xattr syscall listxattr に揃える</span><span class="sxs-lookup"><span data-stu-id="d84f9-1261">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="d84f9-1262">のみ SIOCGIFCONF から有効な IPv4 アドレスとのインターフェイスを返す</span><span class="sxs-lookup"><span data-stu-id="d84f9-1262">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="d84f9-1263">Ptrace によって挿入されたときに既定のアクションを信号を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1263">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="d84f9-1264">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="d84f9-1264">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="d84f9-1265">Sigreturn でコンテキストを復元するときにコンピューター コンテキスト レジスタの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1265">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="d84f9-1266">Java と javac に一部のユーザーの分岐がどこで問題が解決します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1266">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="d84f9-1267">/Proc/sys/kernel/hostname を実装します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1267">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1268">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1268">Syscall Support</span></span>
<span data-ttu-id="d84f9-1269">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1270">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="d84f9-1271">Windows 10 Anniversary Update に 14388 をビルドします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1271">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="d84f9-1272">一般的な Windows ビルド 14388 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/14388wip)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1272">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d84f9-1273">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1273">Fixed</span></span>
- <span data-ttu-id="d84f9-1274">8/2 で、Windows 10 Anniversary Update の準備のための修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1274">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="d84f9-1275">WSL Anniversary update の詳細についてを参照できます、[ブログ](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1275">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="d84f9-1276">ビルド 14376</span><span class="sxs-lookup"><span data-stu-id="d84f9-1276">Build 14376</span></span>
<span data-ttu-id="d84f9-1277">一般的な Windows ビルド 14376 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1277">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d84f9-1278">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1278">Fixed</span></span>
- <span data-ttu-id="d84f9-1279">Apt get が (GH #493) がハングするいくつかのインスタンスの削除</span><span class="sxs-lookup"><span data-stu-id="d84f9-1279">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="d84f9-1280">空のマウントが正しく処理されませんが、問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1280">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="d84f9-1281">場所 ram ディスクがマウントされていない正しく問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1281">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="d84f9-1282">変更の unix ソケットのフラグ (部分的な GH #451) をサポートするために受け入れ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1282">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="d84f9-1283">固定の一般的なネットワーク関連のブルー スクリーン</span><span class="sxs-lookup"><span data-stu-id="d84f9-1283">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="d84f9-1284">/Proc/[pid] にアクセスする場合は、ブルー スクリーンを固定/task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1284">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="d84f9-1285">高の固定の CPU 使用率のいくつか pty シナリオ (GH #488、#504)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1285">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="d84f9-1286">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1286">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="d84f9-1287">ビルド 14371</span><span class="sxs-lookup"><span data-stu-id="d84f9-1287">Build 14371</span></span>
<span data-ttu-id="d84f9-1288">一般的な Windows ビルド 14371 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1288">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d84f9-1289">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1289">Fixed</span></span>
- <span data-ttu-id="d84f9-1290">Ptrace を使用する場合は、SIGCHLD wait() とタイミングの競合を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1290">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="d84f9-1291">パスは、末尾がある場合は、いくつかの動作を修正/(GH #432)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1291">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="d84f9-1292">名前の変更/リンク解除の子に開いているハンドルのために失敗したと問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1292">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="d84f9-1293">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1293">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="d84f9-1294">ビルド 14366</span><span class="sxs-lookup"><span data-stu-id="d84f9-1294">Build 14366</span></span>
<span data-ttu-id="d84f9-1295">一般的な Windows ビルド 14366 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1295">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d84f9-1296">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1296">Fixed</span></span>
- <span data-ttu-id="d84f9-1297">シンボリック リンクをファイルの作成を修正します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1297">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="d84f9-1298">追加された listxattr for Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1298">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="d84f9-1299">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1299">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1300">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1300">Syscall Support</span></span>
-   <span data-ttu-id="d84f9-1301">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1301">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1302">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1302">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="d84f9-1303">ビルド 14361</span><span class="sxs-lookup"><span data-stu-id="d84f9-1303">Build 14361</span></span>
<span data-ttu-id="d84f9-1304">一般的な Windows ビルド 14361 に情報を参照してください、 [Windows ブログ](https://aka.ms/wip14361)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1304">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d84f9-1305">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1305">Fixed</span></span>
- <span data-ttu-id="d84f9-1306">Windows 上の Ubuntu 上で Bash で実行する場合、DrvFs は大文字小文字が区別ようになりました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1306">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="d84f9-1307">ユーザーが case.txt とケース。TXT、/mnt/retention/c ドライブします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1307">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="d84f9-1308">大文字小文字の区別は、Bash on Ubuntu on Windows 内でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1308">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="d84f9-1309">NTFS の Bash の外側では、ファイルを正しく報告されますが、予期しない動作には、Windows からファイルとの対話が発生する場合。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1309">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="d84f9-1310">各ボリューム (つまり/mnt/c) のルートは大文字小文字を区別しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1310">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="d84f9-1311">Windows でこれらのファイルの処理の詳細についてはあります[ここ](https://support.microsoft.com/en-us/kb/100625)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1311">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="d84f9-1312">Pty を大幅に強化/tty をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1312">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="d84f9-1313">TMUX などのアプリケーションがサポートされています (GH #40)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1313">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="d84f9-1314">ユーザー アカウントが常にではありません作成の固定のインストールの問題</span><span class="sxs-lookup"><span data-stu-id="d84f9-1314">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="d84f9-1315">コマンド ライン arg 構造が非常に長い引数リストに最適化されています。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1315">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="d84f9-1316">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1316">(GH #153)</span></span>
- <span data-ttu-id="d84f9-1317">Read_only は、DrvFs からファイルを削除して chmod を行うようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1317">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="d84f9-1318">ターミナルのハングが (GH #43) を切断するいくつかのインスタンスを修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1318">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="d84f9-1319">chmod、chown tty を作業ようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1319">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="d84f9-1320">0.0.0.0 への接続を許可して:: localhost (GH #388) として</span><span class="sxs-lookup"><span data-stu-id="d84f9-1320">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="d84f9-1321">Sendmsg/検知の IO ベクターの長さを処理するようになりました > 1 (部分的な GH #376)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1321">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="d84f9-1322">ユーザーできるようになりましたオプトアウトのホストの自動生成されたファイル (GH #398)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1322">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="d84f9-1323">自動的にインストール (GH 11) 中に NT ロケールに Linux ロケールと一致します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1323">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="d84f9-1324">/Proc/sys/vm/swappiness ファイル (GH #306) の追加</span><span class="sxs-lookup"><span data-stu-id="d84f9-1324">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="d84f9-1325">strace が正しく終了ようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1325">strace now exits correctly</span></span>
- <span data-ttu-id="d84f9-1326">/Proc/self/fd (GH #222) を再度開くをパイプを許可します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1326">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="d84f9-1327">%LOCALAPPDATA%\lxss DrvFs (GH #270) から下のディレクトリを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1327">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="d84f9-1328">Bash.exe の処理の改善 ~。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1328">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="d84f9-1329">などのコマンド"bash ~-c %.ls"(GH #467) をサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1329">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="d84f9-1330">ソケットは epoll を通知するようになりました (GH #271) をシャット ダウン中に使用可能な読み取り</span><span class="sxs-lookup"><span data-stu-id="d84f9-1330">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="d84f9-1331">lxrun/uninstall 的確ファイルとフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1331">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="d84f9-1332">修正された ps f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1332">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="d84f9-1333">X11 のサポート強化 xEmacs (GH #481) などのアプリ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1333">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="d84f9-1334">Ubuntu の既定の設定と get_rlimit syscall (GH #172、#258) にサイズを正しく報告を照合する最初のスレッドのスタック サイズを更新</span><span class="sxs-lookup"><span data-stu-id="d84f9-1334">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="d84f9-1335">Pico プロセスのイメージ名 (例: 監査) 用のレポート機能の強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1335">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="d84f9-1336">実装された/proc/mountinfo df コマンド</span><span class="sxs-lookup"><span data-stu-id="d84f9-1336">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="d84f9-1337">子の名前のエラー コードのシンボリック リンクを修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1337">Fixed symlink error code for child name .</span></span> <span data-ttu-id="d84f9-1338">そして。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1338">and ..</span></span>
- <span data-ttu-id="d84f9-1339">追加の機能強化のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1339">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1340">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1340">Syscall Support</span></span>
<span data-ttu-id="d84f9-1341">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1341">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1342">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1342">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="d84f9-1343">ビルド 14352</span><span class="sxs-lookup"><span data-stu-id="d84f9-1343">Build 14352</span></span>
<span data-ttu-id="d84f9-1344">一般的な Windows ビルド 14352 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/wip14352)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1344">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1345">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1345">Fixed</span></span>
- <span data-ttu-id="d84f9-1346">大きなファイルが非ダウンロード/正常に作成された問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1346">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="d84f9-1347">これは、npm その他のシナリオ (GH 3、GH #313) ブロックを解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1347">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="d84f9-1348">ソケットのハングをいくつかのインスタンスの削除</span><span class="sxs-lookup"><span data-stu-id="d84f9-1348">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="d84f9-1349">一部の ptrace エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1349">Corrected some ptrace errors</span></span>
- <span data-ttu-id="d84f9-1350">WSL が 255 文字より長いファイル名を許可すると問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1350">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="d84f9-1351">英語以外の文字のサポート強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1351">Improved support for non-English characters</span></span>
- <span data-ttu-id="d84f9-1352">現在の Windows タイム ゾーン データを追加し、既定値として設定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1352">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="d84f9-1353">一意のデバイス id のそれぞれのマウント ポイント (jre の修正 – GH 番号 49)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1353">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="d84f9-1354">パスを格納している問題を修正"します"。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1354">Correct issue with paths containing “.”</span></span> <span data-ttu-id="d84f9-1355">および"."</span><span class="sxs-lookup"><span data-stu-id="d84f9-1355">and “..”</span></span>
- <span data-ttu-id="d84f9-1356">Fifo サポートが追加されました (GH #71)</span><span class="sxs-lookup"><span data-stu-id="d84f9-1356">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="d84f9-1357">Ubuntu のネイティブ形式を一致するように resolv.conf の更新の形式</span><span class="sxs-lookup"><span data-stu-id="d84f9-1357">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="d84f9-1358">いくつかの詳しい情報のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1358">Some procfs cleanup</span></span>
- <span data-ttu-id="d84f9-1359">管理コンソール (GH #18) の ping を有効になっています。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1359">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1360">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1360">Syscall Support</span></span>
<span data-ttu-id="d84f9-1361">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1361">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1362">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1362">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="d84f9-1363">ビルド 14342</span><span class="sxs-lookup"><span data-stu-id="d84f9-1363">Build 14342</span></span>
<span data-ttu-id="d84f9-1364">一般的な Windows についてビルド 14342、 [Windows ブログ](https://aka.ms/wip14342)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1364">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="d84f9-1365">VolFs と DriveFs に関する情報が見つかりません、 [WSL ブログ](https://blogs.msdn.microsoft.com/wsl)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1365">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="d84f9-1366">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1366">Fixed</span></span>
- <span data-ttu-id="d84f9-1367">Windows ユーザーは、ユーザー名に Unicode 文字がある場合に、インストールの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1367">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="d84f9-1368">FAQ の apt-get と更新プログラムの udev 回避策が初回実行時の既定値によって提供されるようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1368">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="d84f9-1369">DriveFs にシンボリック リンクを有効になっている (/mnt/<drive>) ディレクトリ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1369">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="d84f9-1370">シンボリック リンクが DriveFs と VolFs 間で作業するようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1370">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="d84f9-1371">解析の問題、アドレス指定された最上位レベル パス: %.ls/期待どおりに、正しく動作/。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1371">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="d84f9-1372">DriveFs に npm をインストールし、-g オプションが有効になった</span><span class="sxs-lookup"><span data-stu-id="d84f9-1372">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="d84f9-1373">PHP サーバーが起動できない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1373">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="d84f9-1374">Ubuntu のネイティブに近い一致を $PATH などの最新の既定環境値</span><span class="sxs-lookup"><span data-stu-id="d84f9-1374">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="d84f9-1375">Apt パッケージ キャッシュを更新する Windows で、毎週のメンテナンス タスクを追加</span><span class="sxs-lookup"><span data-stu-id="d84f9-1375">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="d84f9-1376">ELF ヘッダーの検証で問題を修正しました、WSL なりました Melkor のすべてのオプション</span><span class="sxs-lookup"><span data-stu-id="d84f9-1376">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="d84f9-1377">Zsh シェルが機能</span><span class="sxs-lookup"><span data-stu-id="d84f9-1377">Zsh shell is functional</span></span>
- <span data-ttu-id="d84f9-1378">Go のプリコンパイル済みのバイナリはサポートされています</span><span class="sxs-lookup"><span data-stu-id="d84f9-1378">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="d84f9-1379">最初に実行 Bash.exe で入力を求めるは正しくローカライズされています</span><span class="sxs-lookup"><span data-stu-id="d84f9-1379">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="d84f9-1380">proc/meminfo 返します情報を修正するようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1380">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="d84f9-1381">ソケットの VFS でサポートされています</span><span class="sxs-lookup"><span data-stu-id="d84f9-1381">Sockets now supported in VFS</span></span>
- <span data-ttu-id="d84f9-1382">tempfs として/dev がマウントされました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1382">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="d84f9-1383">Fifo のようになりました</span><span class="sxs-lookup"><span data-stu-id="d84f9-1383">Fifo now supported</span></span>
- <span data-ttu-id="d84f9-1384">Proc/cpuinfo で正しく表示されて、マルチコア システム</span><span class="sxs-lookup"><span data-stu-id="d84f9-1384">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="d84f9-1385">さらなる改良とエラー メッセージが最初の実行中にダウンロード</span><span class="sxs-lookup"><span data-stu-id="d84f9-1385">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="d84f9-1386">Syscall の機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1386">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="d84f9-1387">以下のサポートされている syscall 一覧。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1387">Supported syscall list below.</span></span>
- <span data-ttu-id="d84f9-1388">追加のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1388">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="d84f9-1389">既知の問題</span><span class="sxs-lookup"><span data-stu-id="d84f9-1389">Known Issues</span></span>
- <span data-ttu-id="d84f9-1390">解決されていません '… '</span><span class="sxs-lookup"><span data-stu-id="d84f9-1390">Not resolving ‘..’</span></span> <span data-ttu-id="d84f9-1391">場合によっては DriveFs で正しく</span><span class="sxs-lookup"><span data-stu-id="d84f9-1391">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1392">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1392">Syscall Support</span></span>
<span data-ttu-id="d84f9-1393">WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1394">少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="d84f9-1395">ビルド 14332</span><span class="sxs-lookup"><span data-stu-id="d84f9-1395">Build 14332</span></span>

<span data-ttu-id="d84f9-1396">一般的な Windows ビルド 14332 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/wip14332)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1396">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="d84f9-1397">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1397">Fixed</span></span>
- <span data-ttu-id="d84f9-1398">DNS エントリの優先順位付けを含む resolv.conf 生成の向上</span><span class="sxs-lookup"><span data-stu-id="d84f9-1398">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="d84f9-1399">/Mnt 間と非ファイルおよびディレクトリの移動に関する問題-mnt ドライブ/</span><span class="sxs-lookup"><span data-stu-id="d84f9-1399">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="d84f9-1400">Tar ファイル、シンボリック リンクは作成できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1400">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="d84f9-1401">インスタンスの作成時に追加された既定/run/lock ディレクトリ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1401">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="d84f9-1402">適切な統計情報を返すこと/dev/null を更新します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1402">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="d84f9-1403">最初の実行中にダウンロードするときにその他のエラー</span><span class="sxs-lookup"><span data-stu-id="d84f9-1403">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="d84f9-1404">Syscall の機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1404">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="d84f9-1405">以下のサポートされている syscall 一覧。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1405">Supported syscall list below.</span></span>
- <span data-ttu-id="d84f9-1406">追加の機能強化のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1406">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1407">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1407">Syscall Support</span></span>
<span data-ttu-id="d84f9-1408">WSL でいくつかの実装を含む新しい syscall を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1408">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="d84f9-1409">少なくとも 1 つのシナリオではこの一覧にシステム コールがサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点でします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1409">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="d84f9-1410">ビルド 14328</span><span class="sxs-lookup"><span data-stu-id="d84f9-1410">Build 14328</span></span>

<span data-ttu-id="d84f9-1411">一般的な Windows ビルド 14332 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/wip14328)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1411">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="d84f9-1412">新機能</span><span class="sxs-lookup"><span data-stu-id="d84f9-1412">New Features</span></span>
* <span data-ttu-id="d84f9-1413">Linux ユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1413">Now support Linux users.</span></span>  <span data-ttu-id="d84f9-1414">Ubuntu on Windows での Bash のインストールは、Linux ユーザーの作成を求められます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1414">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="d84f9-1415">詳細については、次を参照してください。 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="d84f9-1415">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="d84f9-1416">ホスト名がない設定を Windows コンピューター名にようになりました @localhost</span><span class="sxs-lookup"><span data-stu-id="d84f9-1416">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="d84f9-1417">詳細については、ビルド 14328 を参照してください。 https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="d84f9-1417">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="d84f9-1418">固定</span><span class="sxs-lookup"><span data-stu-id="d84f9-1418">Fixed</span></span>
* <span data-ttu-id="d84f9-1419">非/mnt/のシンボリック リンクの機能強化<drive>ファイル</span><span class="sxs-lookup"><span data-stu-id="d84f9-1419">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="d84f9-1420">npm インストール機能</span><span class="sxs-lookup"><span data-stu-id="d84f9-1420">npm install now works</span></span>
    * <span data-ttu-id="d84f9-1421">jdk jre を今すぐインストール可能な命令を使用して[ここ](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1421">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="d84f9-1422">既知の問題: Windows のマウントのシンボリック リンクが機能しません。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1422">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="d84f9-1423">機能は今後のビルドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1423">Functionality will be available in a later build</span></span>
* <span data-ttu-id="d84f9-1424">top としたければが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1424">top and htop now display</span></span>
* <span data-ttu-id="d84f9-1425">インストール エラーのいくつかの追加のエラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="d84f9-1425">Additional error messages for some install failures</span></span>
* <span data-ttu-id="d84f9-1426">Syscall の機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1426">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="d84f9-1427">以下のサポートされている syscall 一覧。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1427">Supported syscall list below.</span></span>
* <span data-ttu-id="d84f9-1428">追加の機能強化のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="d84f9-1428">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="d84f9-1429">Syscall サポート</span><span class="sxs-lookup"><span data-stu-id="d84f9-1429">Syscall Support</span></span>
<span data-ttu-id="d84f9-1430">WSL でのいくつかの実装を持って syscall の一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1430">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="d84f9-1431">Syscall この一覧には少なくとも 1 つのシナリオでサポートされてが可能性がありますがパラメーターをすべてサポートされていませんこの時点でします。</span><span class="sxs-lookup"><span data-stu-id="d84f9-1431">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
