---
title: Windows Subsystem for Linux のリリースノート
description: Windows Subsystem for Linux のリリースノートです。  毎週更新されました。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: e2d9d5fc70c173e9b516ab7af01599b623b40b39
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "67042426"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="6ccbd-105">Windows Subsystem for Linux のリリースノート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18917"></a><span data-ttu-id="6ccbd-106">ビルド18917</span><span class="sxs-lookup"><span data-stu-id="6ccbd-106">Build 18917</span></span>
<span data-ttu-id="6ccbd-107">ビルド18917の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-107">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-108">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-108">WSL</span></span>
* <span data-ttu-id="6ccbd-109">WSL 2 が利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-109">WSL 2 is now available!</span></span> <span data-ttu-id="6ccbd-110">詳細については、[ブログ](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-110">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="6ccbd-111">シンボリックリンクを使用した Windows プロセスの起動が正常に機能しない回帰を修正する [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-111">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="6ccbd-112">Wsl--list--verbose, wsl--list--quiet, および wsl .exe--import--version オプションを wsl に追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-112">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="6ccbd-113">Wsl--shutdown オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-113">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="6ccbd-114">プラン 9:書き込み用のディレクトリを開くことを成功させる</span><span class="sxs-lookup"><span data-stu-id="6ccbd-114">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="6ccbd-115">ビルド18890</span><span class="sxs-lookup"><span data-stu-id="6ccbd-115">Build 18890</span></span>
<span data-ttu-id="6ccbd-116">ビルド18890の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-116">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-117">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-117">WSL</span></span>
* <span data-ttu-id="6ccbd-118">非ブロッキングソケットリーク [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-118">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="6ccbd-119">ターミナルへの EOF 入力が後続の読み取りをブロックする可能性がある [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-119">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="6ccbd-120">Resolv.conf を参照するようにを更新する (GH 3928 で説明)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-120">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="6ccbd-121">Epoll delete コードでのデッドロック [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-121">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="6ccbd-122">--Import および– export の引数内のスペースを処理する [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-122">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="6ccbd-123">Mmap ファイルの拡張が正しく機能しない [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-123">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="6ccbd-124">ARM64 \\wsl $ アクセスが正常に動作しない問題を修正します</span><span class="sxs-lookup"><span data-stu-id="6ccbd-124">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="6ccbd-125">Wsl のより適切な既定のアイコンを追加する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-125">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="6ccbd-126">ビルド18342</span><span class="sxs-lookup"><span data-stu-id="6ccbd-126">Build 18342</span></span>
<span data-ttu-id="6ccbd-127">ビルド18342の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-127">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-128">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-128">WSL</span></span>
* <span data-ttu-id="6ccbd-129">Windows から WSL ディストリビューションの Linux ファイルにユーザーがアクセスできる機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-129">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="6ccbd-130">これらのファイルには、コマンドラインを使用してアクセスできます。また、ファイルエクスプローラーや VSCode などの Windows アプリもこれらのファイルと対話できます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-130">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="6ccbd-131">\\Wsl $ \\ \\ \\< distro_name > に移動してファイルにアクセスするか、wsl $ に移動して実行中のディストリビューションの一覧を表示します。\\</span><span class="sxs-lookup"><span data-stu-id="6ccbd-131">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="6ccbd-132">CPU 情報タグを追加し、Cpus_allowed [リスト] の値を修正する [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-132">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="6ccbd-133">リーダー以外のスレッドからの exec のサポート [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-133">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="6ccbd-134">構成の更新エラーを致命的でないものとして扱う [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-134">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="6ccbd-135">オフセットを正しく処理するように binfmt を更新する [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-135">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="6ccbd-136">プラン9のネットワークドライブのマッピングを有効にする [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-136">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="6ccbd-137">Windows > Linux および Linux をサポートする-bind マウント用の Windows パス変換 ></span><span class="sxs-lookup"><span data-stu-id="6ccbd-137">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="6ccbd-138">読み取り専用で開かれたファイルのマッピングの読み取り専用セクションを作成する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-138">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="6ccbd-139">ビルド18334</span><span class="sxs-lookup"><span data-stu-id="6ccbd-139">Build 18334</span></span>
<span data-ttu-id="6ccbd-140">ビルド18334の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-140">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-141">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-141">WSL</span></span>
* <span data-ttu-id="6ccbd-142">Windows タイムゾーンを Linux タイムゾーンにマップする方法の設計 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-142">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="6ccbd-143">メモリリークを修正し、新しい文字列変換関数を追加する [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-143">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="6ccbd-144">スレッドのない threadgroup の SIGCONT は、no op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-144">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="6ccbd-145">/Proc/self/fd にソケットと epoll ファイル記述子を正しく表示する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-145">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="6ccbd-146">ビルド18305</span><span class="sxs-lookup"><span data-stu-id="6ccbd-146">Build 18305</span></span>
<span data-ttu-id="6ccbd-147">ビルド18305の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-147">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-148">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-148">WSL</span></span>
* <span data-ttu-id="6ccbd-149">pthreads プライマリスレッドが終了したときにファイルへのアクセスが失われる [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-149">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="6ccbd-150">TIOCSCTTY は、必要な場合を除き、"force" パラメーターを無視する必要があります [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-150">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="6ccbd-151">wsl コマンドラインの機能強化とインポート/エクスポート機能の追加。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-151">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="6ccbd-152">ビルド18277</span><span class="sxs-lookup"><span data-stu-id="6ccbd-152">Build 18277</span></span>
<span data-ttu-id="6ccbd-153">ビルド18277の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-153">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-154">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-154">WSL</span></span>
* <span data-ttu-id="6ccbd-155">ビルド18272で導入された "そのようなインターフェイスがサポートされていません" というエラーを修正する [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-155">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="6ccbd-156">Umount syscall の MNT_FORCE フラグを無視する [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-156">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="6ccbd-157">WSL 相互運用機能を切り替えて、正式な Create擬似コンソール API を使用する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-157">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="6ccbd-158">FUTEX_WAIT の再起動時にタイムアウト値を保持しない</span><span class="sxs-lookup"><span data-stu-id="6ccbd-158">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="6ccbd-159">ビルド18272</span><span class="sxs-lookup"><span data-stu-id="6ccbd-159">Build 18272</span></span>
<span data-ttu-id="6ccbd-160">ビルド18272の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-160">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-161">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-161">WSL</span></span>
* <span data-ttu-id="6ccbd-162">**要する**このビルドには、WSL が動作しなくなる問題があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-162">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="6ccbd-163">ディストリビューションを起動しようとすると、"そのようなインターフェイスはサポートされていません" というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-163">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="6ccbd-164">この問題は修正され、来週の Insider Fast ビルドに含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-164">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="6ccbd-165">このビルドがインストールされている場合は、「設定-> Update & Security-> Recovery」の「以前のバージョンの Windows 10 に戻る」を使用して、以前の Windows ビルドにロールバックできます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-165">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="6ccbd-166">ビルド18267</span><span class="sxs-lookup"><span data-stu-id="6ccbd-166">Build 18267</span></span>
<span data-ttu-id="6ccbd-167">ビルド18267の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-167">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-168">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-168">WSL</span></span>
* <span data-ttu-id="6ccbd-169">ゾンビプロセスが reaped されず、無期限に保持される問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-169">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="6ccbd-170">エラーメッセージが最大長を超えた場合、WslRegisterDistribution がハングする [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-170">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="6ccbd-171">DrvFs で読み取り専用ファイルの fsync を正常に実行できるようにする [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-171">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="6ccbd-172">[GH 3584] 内にシンボリックリンクを作成する前に、/bin と/sbin ディレクトリが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-172">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="6ccbd-173">WSL インスタンスのインスタンス終了タイムアウトメカニズムが追加されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-173">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="6ccbd-174">タイムアウトは現在15秒に設定されています。つまり、最後の WSL プロセスが終了してから15秒後にインスタンスが終了します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-174">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="6ccbd-175">ディストリビューションをすぐに終了するには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-175">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="6ccbd-176">ビルド 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-176">Build 17763 (1809)</span></span>
<span data-ttu-id="6ccbd-177">ビルド17763の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-177">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-178">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-178">WSL</span></span>
* <span data-ttu-id="6ccbd-179">同じスレッド優先順位を変更するための setpriority syscall アクセス許可チェックが strict すぎます [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-179">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="6ccbd-180">Clock_gettime (CLOCK_BOOTTIME) の負の値が返されないように、起動時間にバイアスをかけない割り込み時間を使用することを確認してください () [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-180">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="6ccbd-181">WSL binfmt インタープリターでのシンボリックリンクの処理 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-181">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="6ccbd-182">Threadgroup リーダーファイル記述子のクリーンアップをより適切に処理します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-182">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="6ccbd-183">KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用してオーバーフローを回避するように WSL を切り替える [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-183">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="6ccbd-184">Ptrace をアタッチすると、システムコールから無効な戻り値が返される [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-184">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="6ccbd-185">AF_UNIX 関連のいくつかの問題を修正する [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-185">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="6ccbd-186">現在の作業ディレクトリの長さが5文字未満の場合に WSL 相互運用機能が失敗する原因となる問題を修正しました [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-186">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="6ccbd-187">存在しないポートへのループバック接続で1秒間の遅延が発生しないようにする [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-187">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="6ccbd-188">/Proc/sys/fs/file-max スタブファイルの追加 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-188">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="6ccbd-189">より正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-189">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="6ccbd-190">PR_SET_PTRACER のサポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-190">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="6ccbd-191">パイプファイルシステムがエッジトリガーの epoll イベントを誤って消去しています [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-191">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="6ccbd-192">NTFS シンボリックリンクによって起動された Win32 実行可能ファイルがシンボリックリンク名を尊重しない [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-192">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="6ccbd-193">強化されたゾンビサポート [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-193">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="6ccbd-194">Windows 相互運用機能の動作を制御するための wsl のエントリを追加する [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-194">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="6ccbd-195">常に UNIX ソケットファミリの種類を返す getsockname でないことを修正する [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-195">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="6ccbd-196">TIOCSTI のサポートを追加する [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-196">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="6ccbd-197">接続処理中の非ブロッキングソケットは、書き込み試行に EAGAIN を返します [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-197">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="6ccbd-198">マウントされた Vhd での相互運用のサポート [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-198">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="6ccbd-199">ルートフォルダーでのアクセス許可チェックの問題の修正 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-199">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="6ccbd-200">TTY キーボード ioctl KDGKBTYPE、KDGKBMODE、および KDSKBMODE のサポートが制限されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-200">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="6ccbd-201">Windows UI アプリは、バックグラウンドで起動した場合でも実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-201">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="6ccbd-202">Wsl-u または--user オプションを追加する [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-202">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="6ccbd-203">高速スタートアップが有効になっているときの WSL 起動の問題を修正する [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-203">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="6ccbd-204">Unix ソケットが切断されたピア資格情報を保持する必要がある [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-204">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="6ccbd-205">EAGAIN で無制限の非ブロッキング Unix ソケットが失敗する [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-205">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="6ccbd-206">case = off は新しい既定の drvfs マウントの種類 [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-206">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="6ccbd-207">詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-207">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="6ccbd-208">Wslconfig/terminate を追加して、実行中のディストリビューションを停止します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-208">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="6ccbd-209">スペースを含むパスを正しく処理しない WSL シェルコンテキストメニューエントリの問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-209">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="6ccbd-210">ディレクトリごとの大文字と小文字の区別を拡張属性として公開する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-210">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="6ccbd-211">ARM64: キャッシュメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-211">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="6ccbd-212">[Dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-212">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="6ccbd-213">DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみを unescape します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-213">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="6ccbd-214">ELF パーサーインタープリターの長さの検証での1つずつのエラーの修正 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-214">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="6ccbd-215">過去の時間を持つ WSL 絶対タイマーが起動しない [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-215">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="6ccbd-216">新しく作成された再解析ポイントが親ディレクトリに表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-216">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="6ccbd-217">DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-217">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="6ccbd-218">ファイルが存在する場合でも、マルチスレッド操作が ENOENT を返す可能性のある追加の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-218">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="6ccbd-219">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-219">[GH 2712]</span></span>
* <span data-ttu-id="6ccbd-220">UMCI が有効になっているときの WSL 起動エラーを修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-220">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="6ccbd-221">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-221">[GH 3020]</span></span>
* <span data-ttu-id="6ccbd-222">WSL [GH 437, 603, 1836] を起動するには、エクスプローラーのコンテキストメニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-222">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="6ccbd-223">を使用するには、エクスプローラーウィンドウで、shift キーを押しながら右クリックします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-223">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="6ccbd-224">Unix ソケットの非ブロッキング動作の修正 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-224">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="6ccbd-225">GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-225">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="6ccbd-226">マウント伝達フラグ [GH 2911] のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-226">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="6ccbd-227">Truncate で inotify イベントが発生しない問題を修正する [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-227">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="6ccbd-228">シェルを使用せずに1つのバイナリを呼び出すには、wsl の--exec オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-228">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="6ccbd-229">特定のディストリビューションを選択するには、wsl のディストリビューションオプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-229">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="6ccbd-230">Dmesg のサポートが制限されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-230">Limited support for dmesg.</span></span> <span data-ttu-id="6ccbd-231">アプリケーションは、dmesg にログを記録できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-231">Applications can now log to dmesg.</span></span> <span data-ttu-id="6ccbd-232">WSL ドライバーは、制限された情報を dmesg に記録します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-232">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="6ccbd-233">将来は、この機能を拡張して、ドライバーから他の情報や診断情報を伝達することができます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-233">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="6ccbd-234">注: 現在、 `/dev/kmsg` dmesg はデバイスインターフェイスでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-234">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="6ccbd-235">`syslog`syscall インターフェイスはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-235">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="6ccbd-236">そのため、などの一部の`dmesg`コマンドラインオプション`-S` `-C`は機能しません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-236">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="6ccbd-237">ネイティブと一致するように既定の gid とシリアルデバイスのモードを変更する [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-237">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="6ccbd-238">DrvFs は拡張属性をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-238">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="6ccbd-239">注:DrvFs では、拡張属性の名前にいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-239">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="6ccbd-240">一部の文字 ('/'、': '、'\*' など) は使用できません。また、拡張属性名は、drvfs では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-240">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="6ccbd-241">ビルド 18252 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-241">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="6ccbd-242">ビルド18252の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-242">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-243">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-243">WSL</span></span>
* <span data-ttu-id="6ccbd-244">Init と bsdtar のバイナリを lxssmanager dll から別のツールフォルダーに移動する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-244">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="6ccbd-245">CLONE_FILES を使用するときのファイル記述子の終了に関する競合を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-245">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="6ccbd-246">DrvFs パスを変換するときに/proc/pid/mountinfo の省略可能なフィールドを処理する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-246">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="6ccbd-247">S_IFREG のメタデータをサポートせずに DrvFs mknod を正常に実行できるようにする</span><span class="sxs-lookup"><span data-stu-id="6ccbd-247">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="6ccbd-248">DrvFs で作成される readonly ファイルは、readonly 属性セットを持つ必要があります [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-248">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="6ccbd-249">DrvFs のマウントを処理する/sbin/mount.drvfs helper を追加する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-249">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="6ccbd-250">DrvFs で POSIX 名の変更を使用します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-250">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="6ccbd-251">ボリューム GUID がないボリュームでパスの変換を許可します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-251">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="6ccbd-252">ビルド 17738 (高速)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-252">Build 17738 (Fast)</span></span>
<span data-ttu-id="6ccbd-253">ビルド17738の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-253">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-254">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-254">WSL</span></span>
* <span data-ttu-id="6ccbd-255">同じスレッド優先順位を変更するための setpriority syscall アクセス許可チェックが strict すぎます [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-255">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="6ccbd-256">Clock_gettime (CLOCK_BOOTTIME) の負の値が返されないように、起動時間にバイアスをかけない割り込み時間を使用することを確認してください () [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-256">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="6ccbd-257">WSL binfmt インタープリターでのシンボリックリンクの処理 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-257">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="6ccbd-258">Threadgroup リーダーファイル記述子のクリーンアップをより適切に処理します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-258">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="6ccbd-259">ビルド 17728 (高速)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-259">Build 17728 (Fast)</span></span>
<span data-ttu-id="6ccbd-260">ビルド17728の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-260">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-261">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-261">WSL</span></span>
* <span data-ttu-id="6ccbd-262">KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用してオーバーフローを回避するように WSL を切り替える [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-262">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="6ccbd-263">Ptrace をアタッチすると、システムコールから無効な戻り値が返される [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-263">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="6ccbd-264">AF_UNIX 関連のさまざまな問題を修正する [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-264">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="6ccbd-265">現在の作業ディレクトリの長さが5文字未満の場合に WSL 相互運用機能が失敗する原因となる問題を修正しました [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-265">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="6ccbd-266">ビルド 18204 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-266">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="6ccbd-267">ビルド18204の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-267">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-268">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-268">WSL</span></span>
* <span data-ttu-id="6ccbd-269">パイプファイルシステム inadvertenly によるエッジトリガー epoll イベントの消去 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="6ccbd-270">NTFS シンボリックリンクによって起動された Win32 実行可能ファイルがシンボリックリンク名を尊重しない [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="6ccbd-271">ビルド 17723 (高速)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-271">Build 17723 (Fast)</span></span>
<span data-ttu-id="6ccbd-272">ビルド17723の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-272">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-273">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-273">WSL</span></span>
* <span data-ttu-id="6ccbd-274">存在しないポートへのループバック接続で1秒間の遅延が発生しないようにする [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-274">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="6ccbd-275">/Proc/sys/fs/file-max スタブファイルの追加 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-275">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="6ccbd-276">より正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-276">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="6ccbd-277">PR_SET_PTRACER のサポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-277">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="6ccbd-278">パイプファイルシステム inadvertenly によるエッジトリガー epoll イベントの消去 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-278">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="6ccbd-279">NTFS シンボリックリンクによって起動された Win32 実行可能ファイルがシンボリックリンク名を尊重しない [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-279">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="6ccbd-280">ビルド17713</span><span class="sxs-lookup"><span data-stu-id="6ccbd-280">Build 17713</span></span>
<span data-ttu-id="6ccbd-281">ビルド17713の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-281">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-282">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-282">WSL</span></span>
* <span data-ttu-id="6ccbd-283">強化されたゾンビサポート [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-283">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="6ccbd-284">Windows 相互運用機能の動作を制御するための wsl のエントリを追加する [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-284">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="6ccbd-285">常に UNIX ソケットファミリの種類を返す getsockname でないことを修正する [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-285">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="6ccbd-286">TIOCSTI のサポートを追加する [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-286">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="6ccbd-287">接続処理中の非ブロッキングソケットは、書き込み試行に EAGAIN を返します [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-287">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="6ccbd-288">マウントされた Vhd での相互運用のサポート [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-288">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="6ccbd-289">ルートフォルダーでのアクセス許可チェックの問題の修正 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-289">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="6ccbd-290">TTY キーボード ioctl KDGKBTYPE、KDGKBMODE、および KDSKBMODE のサポートが制限されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-290">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="6ccbd-291">Windows UI アプリは、バックグラウンドで起動した場合でも実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-291">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="6ccbd-292">ビルド17704</span><span class="sxs-lookup"><span data-stu-id="6ccbd-292">Build 17704</span></span>
<span data-ttu-id="6ccbd-293">ビルド17704の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-293">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-294">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-294">WSL</span></span>
* <span data-ttu-id="6ccbd-295">Wsl-u または--user オプションを追加する [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-295">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="6ccbd-296">高速スタートアップが有効になっているときの WSL 起動の問題を修正する [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-296">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="6ccbd-297">Unix ソケットが切断されたピア資格情報を保持する必要がある [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-297">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="6ccbd-298">EAGAIN で無制限の非ブロッキング Unix ソケットが失敗する [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-298">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="6ccbd-299">case = off は新しい既定の drvfs マウントの種類 [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-299">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="6ccbd-300">詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-300">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="6ccbd-301">Wslconfig/terminate を追加して、実行中のディストリビューションを停止します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-301">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="6ccbd-302">ビルド 17692</span><span class="sxs-lookup"><span data-stu-id="6ccbd-302">Build 17692</span></span>
<span data-ttu-id="6ccbd-303">ビルド17692の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-303">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-304">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-304">WSL</span></span>
* <span data-ttu-id="6ccbd-305">スペースを含むパスを正しく処理しない WSL シェルコンテキストメニューエントリの問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-305">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="6ccbd-306">ディレクトリごとの大文字と小文字の区別を拡張属性として公開する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-306">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="6ccbd-307">ARM64: キャッシュメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-307">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="6ccbd-308">[Dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-308">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="6ccbd-309">DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみを unescape します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-309">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="6ccbd-310">ビルド 17686</span><span class="sxs-lookup"><span data-stu-id="6ccbd-310">Build 17686</span></span>
<span data-ttu-id="6ccbd-311">ビルド17686の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-311">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-312">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-312">WSL</span></span>
* <span data-ttu-id="6ccbd-313">ELF パーサーインタープリターの長さの検証での1つずつのエラーの修正 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-313">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="6ccbd-314">過去の時間を持つ WSL 絶対タイマーが起動しない [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-314">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="6ccbd-315">新しく作成された再解析ポイントが親ディレクトリに表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-315">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="6ccbd-316">DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-316">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="6ccbd-317">ビルド17677</span><span class="sxs-lookup"><span data-stu-id="6ccbd-317">Build 17677</span></span>
<span data-ttu-id="6ccbd-318">ビルド17677の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-318">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-319">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-319">WSL</span></span>
* <span data-ttu-id="6ccbd-320">ファイルが存在する場合でも、マルチスレッド操作が ENOENT を返す可能性のある追加の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-320">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="6ccbd-321">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-321">[GH 2712]</span></span>
* <span data-ttu-id="6ccbd-322">UMCI が有効になっているときの WSL 起動エラーを修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-322">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="6ccbd-323">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-323">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="6ccbd-324">ビルド17666</span><span class="sxs-lookup"><span data-stu-id="6ccbd-324">Build 17666</span></span>
<span data-ttu-id="6ccbd-325">ビルド17666の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-325">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-326">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-326">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="6ccbd-327">警告:一部の AMD チップセットで WSL の実行を妨げる問題があります [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-327">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="6ccbd-328">修正の準備ができました。 Insider Build 分岐に変更することができます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-328">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="6ccbd-329">WSL [GH 437, 603, 1836] を起動するには、エクスプローラーのコンテキストメニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-329">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="6ccbd-330">[エクスプローラー] ウィンドウで [保留] をクリックして右クリックします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-330">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="6ccbd-331">Unix ソケットの非ブロッキング動作の修正 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-331">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="6ccbd-332">GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-332">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="6ccbd-333">マウント伝達フラグ [GH 2911] のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-333">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="6ccbd-334">Truncate で inotify イベントが発生しない問題を修正する [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-334">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="6ccbd-335">シェルを使用せずに1つのバイナリを呼び出すには、wsl の--exec オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-335">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="6ccbd-336">特定のディストリビューションを選択するには、wsl のディストリビューションオプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-336">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="6ccbd-337">ビルド 17655 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-337">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="6ccbd-338">ビルド17655の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-338">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-339">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-339">WSL</span></span>
* <span data-ttu-id="6ccbd-340">Dmesg のサポートが制限されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-340">Limited support for dmesg.</span></span> <span data-ttu-id="6ccbd-341">アプリケーションは、dmesg にログを記録できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-341">Applications can now log to dmesg.</span></span> <span data-ttu-id="6ccbd-342">WSL ドライバーは、制限された情報を dmesg に記録します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-342">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="6ccbd-343">将来は、この機能を拡張して、ドライバーから他の情報や診断情報を伝達することができます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-343">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="6ccbd-344">注: 現在、 `/dev/kmsg` dmesg はデバイスインターフェイスでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-344">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="6ccbd-345">`syslog`sycall インターフェイスは、まだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-345">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="6ccbd-346">そのため、などの一部の`dmesg`コマンドラインオプション`-S` `-C`は機能しません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-346">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="6ccbd-347">ファイルが存在する場合でも、マルチスレッド操作で ENOENT が返される問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-347">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="6ccbd-348">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-348">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="6ccbd-349">ビルド 17639 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-349">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="6ccbd-350">ビルド17639の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-350">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-351">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-351">WSL</span></span>
* <span data-ttu-id="6ccbd-352">ネイティブと一致するように既定の gid とシリアルデバイスのモードを変更する [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-352">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="6ccbd-353">DrvFs は拡張属性をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-353">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="6ccbd-354">注:DrvFs では、拡張属性の名前にいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-354">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="6ccbd-355">特に、一部の文字 ('/'、': '、'\*' など) は使用できません。また、拡張属性名は、drvfs では大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-355">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="6ccbd-356">ビルド 17133 (高速)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-356">Build 17133 (Fast)</span></span>
<span data-ttu-id="6ccbd-357">ビルド17133の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-357">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-358">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-358">WSL</span></span>
* <span data-ttu-id="6ccbd-359">WSL のハングを修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-359">Fix for hang in WSL.</span></span> <span data-ttu-id="6ccbd-360">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-360">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="6ccbd-361">ビルド 17128 (高速)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-361">Build 17128 (Fast)</span></span>
<span data-ttu-id="6ccbd-362">ビルド17128の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-362">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-363">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-363">WSL</span></span>
* <span data-ttu-id="6ccbd-364">なし</span><span class="sxs-lookup"><span data-stu-id="6ccbd-364">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="6ccbd-365">ビルド 17627 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-365">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="6ccbd-366">ビルド17627の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-366">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-367">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-367">WSL</span></span>
* <span data-ttu-id="6ccbd-368">Futex pi 対応の操作のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-368">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="6ccbd-369">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-369">[GH 1006]</span></span>
    * <span data-ttu-id="6ccbd-370">優先順位は現在サポートされている WSL 機能ではないため、制限がありますが、標準の使用をブロック解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-370">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="6ccbd-371">WSL プロセス用の Windows ファイアウォールのサポート。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-371">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="6ccbd-372">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-372">[GH 1852]</span></span>
    * <span data-ttu-id="6ccbd-373">たとえば、WSL python プロセスが任意のポートでリッスンできるようにするには、管理者特権の Windows cmd を使用します。```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="6ccbd-373">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="6ccbd-374">ファイアウォール規則を追加する方法の詳細については、「[リンク](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-374">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="6ccbd-375">Wsl を使用するときのユーザーの既定のシェルを尊重します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-375">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="6ccbd-376">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-376">[GH 2372]</span></span>
* <span data-ttu-id="6ccbd-377">すべてのネットワークインターフェイスをイーサネットとして報告します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-377">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="6ccbd-378">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-378">[GH 2996]</span></span>
* <span data-ttu-id="6ccbd-379">破損した/etc/passwd ファイルの処理が改善されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-379">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="6ccbd-380">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-380">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-381">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-381">Console</span></span>
* <span data-ttu-id="6ccbd-382">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-382">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-383">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-383">LTP Results:</span></span>
<span data-ttu-id="6ccbd-384">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-384">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="6ccbd-385">ビルド 17618 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-385">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="6ccbd-386">ビルド17618の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-386">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-387">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-387">WSL</span></span>
* <span data-ttu-id="6ccbd-388">NT interop の擬似コンソール機能の導入 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-388">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="6ccbd-389">レガシインストールメカニズム (lxrun) は非推奨となりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-389">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="6ccbd-390">ディストリビューションのインストールに関してサポートされているメカニズムは、Microsoft Store を使用することです。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-390">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-391">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-391">Console</span></span>
* <span data-ttu-id="6ccbd-392">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-392">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-393">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-393">LTP Results:</span></span>
<span data-ttu-id="6ccbd-394">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-394">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="6ccbd-395">ビルド 17110</span><span class="sxs-lookup"><span data-stu-id="6ccbd-395">Build 17110</span></span>
<span data-ttu-id="6ccbd-396">ビルド17110の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-396">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-397">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-397">WSL</span></span>
* <span data-ttu-id="6ccbd-398">/Init を Windows から終了することを許可します [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-398">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="6ccbd-399">DrvFs では、既定でディレクトリごとの大文字小文字の区別が使用されるようになりました ("case = dir" マウントオプションと同等)。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-399">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="6ccbd-400">"Case = force" (以前の動作) を使用するには、レジストリキーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-400">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="6ccbd-401">次のコマンドを実行して、使用する必要がある場合は "case = force" を有効にします。 reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="6ccbd-401">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="6ccbd-402">以前のバージョンの Windows で wsl で作成された既存のディレクトリがあり、大文字と小文字を区別する必要がある場合は、fsutil を使用し<path>て大文字と小文字を区別するように指定します。 fsutil .exe ファイル setcasesensitiveinfo enable</span><span class="sxs-lookup"><span data-stu-id="6ccbd-402">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="6ccbd-403">Uname syscall から返された NULL の終了文字列。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-403">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-404">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-404">Console</span></span>
* <span data-ttu-id="6ccbd-405">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-405">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-406">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-406">LTP Results:</span></span>
<span data-ttu-id="6ccbd-407">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-407">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="6ccbd-408">ビルド17107</span><span class="sxs-lookup"><span data-stu-id="6ccbd-408">Build 17107</span></span>
<span data-ttu-id="6ccbd-409">ビルド17107の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-409">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-410">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-410">WSL</span></span>
* <span data-ttu-id="6ccbd-411">マスター pty エンドポイントで TCSETSF と TCSETSF をサポートする [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-411">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="6ccbd-412">相互運用プロセスを同時に開始すると、EINVAL [GH 2813] になります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-412">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="6ccbd-413">/Proc/pid/status. に適切なトレースの状態を表示するように PTRACE_ATTACH を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-413">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="6ccbd-414">CLEARTID フラグと SETTID フラグの両方で複製された短い有効期間のプロセスが、TID アドレスをクリアせずに終了する可能性がある競合を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-414">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="6ccbd-415">17093より前のビルドから移動するときに、Linux ファイルシステムディレクトリをアップグレードするときにメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-415">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="6ccbd-416">17093ファイルシステムの変更の詳細については、 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)のリリースノートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-416">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-417">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-417">Console</span></span>
* <span data-ttu-id="6ccbd-418">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-418">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-419">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-419">LTP Results:</span></span>
<span data-ttu-id="6ccbd-420">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-420">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="6ccbd-421">ビルド17101</span><span class="sxs-lookup"><span data-stu-id="6ccbd-421">Build 17101</span></span>
<span data-ttu-id="6ccbd-422">ビルド17101の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-422">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-423">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-423">WSL</span></span>
* <span data-ttu-id="6ccbd-424">Signalfd のサポート。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-424">Support for signalfd.</span></span> <span data-ttu-id="6ccbd-425">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-425">[GH 129]</span></span>
* <span data-ttu-id="6ccbd-426">ファイル名に無効な NTFS 文字を含むファイル名は、プライベート Unicode 文字としてエンコードすることによってサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-426">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="6ccbd-427">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-427">[GH 1514]</span></span>
* <span data-ttu-id="6ccbd-428">書き込みがサポートされていない場合、自動マウントは読み取り専用にフォールバックします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-428">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="6ccbd-429">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-429">[GH 2603]</span></span>
* <span data-ttu-id="6ccbd-430">Unicode サロゲートペア (絵文字文字など) の貼り付けを許可します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-430">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="6ccbd-431">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-431">[GH 2765]</span></span>
* <span data-ttu-id="6ccbd-432">/Proc および/sys の疑似ファイルは、select、poll、epoll、et al から読み取りおよび書き込み準備を返す必要があります。 [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-432">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="6ccbd-433">レジストリが改ざんされているか、または破損している場合に、サービスが無限ループに入る可能性のある問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-433">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="6ccbd-434">Iproute2 の新しい (アップストリーム 4.14) バージョンで動作するように netlink メッセージを修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-434">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-435">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-435">Console</span></span>
* <span data-ttu-id="6ccbd-436">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-436">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-437">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-437">LTP Results:</span></span>
<span data-ttu-id="6ccbd-438">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-438">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="6ccbd-439">ビルド17093</span><span class="sxs-lookup"><span data-stu-id="6ccbd-439">Build 17093</span></span>
<span data-ttu-id="6ccbd-440">ビルド17093の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-440">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="6ccbd-441">重要:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-441">Important:</span></span>
<span data-ttu-id="6ccbd-442">このビルドにアップグレードした後に初めて WSL を開始するときは、Linux ファイルシステムディレクトリをアップグレードする作業を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-442">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="6ccbd-443">この処理には数分かかる場合があるため、WSL の開始に時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-443">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="6ccbd-444">これは、ストアからインストールされた各ディストリビューションにつき1回のみ発生します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-444">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="6ccbd-445">DrvFs での大文字と小文字の区別のサポートが向上しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-445">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="6ccbd-446">DrvFs では、ディレクトリごとの大文字小文字の区別がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-446">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="6ccbd-447">これは、ディレクトリに設定できる新しいフラグで、これらのディレクトリ内のすべての操作を大文字と小文字を区別して扱う必要があることを示します。これにより、Windows アプリケーションでも大文字と小文字のみが異なるファイルを正しく開くことができます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-447">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="6ccbd-448">DrvFs には、ディレクトリごとに大文字と小文字の区別を制御する新しいマウントオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-448">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="6ccbd-449">case = force: すべてのディレクトリは大文字と小文字を区別して処理されます (ドライブのルートを除く)。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-449">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="6ccbd-450">WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-450">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="6ccbd-451">これは、新しいディレクトリの大文字小文字の区別をマークする場合を除き、従来の動作です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-451">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="6ccbd-452">case = dir: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-452">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="6ccbd-453">WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-453">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="6ccbd-454">case = off: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-454">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="6ccbd-455">WSL で作成された新しいディレクトリは、大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-455">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="6ccbd-456">注: 以前のリリースで WSL によって作成されたディレクトリには、このフラグが設定されていないため、"case = dir" オプションを使用した場合、は大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-456">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="6ccbd-457">既存のディレクトリにこのフラグを設定する方法は近日中に予定されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-457">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="6ccbd-458">これらのオプションを使用してマウントする例 (既存のドライブの場合は、別のオプションでマウントする前にマウントを解除する必要があります): sudo mount-t drvfs C:/mnt/c case = dir</span><span class="sxs-lookup"><span data-stu-id="6ccbd-458">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="6ccbd-459">ここでは、case = force は引き続き既定のオプションです。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-459">For now, case=force is still the default option.</span></span> <span data-ttu-id="6ccbd-460">これは、将来、case = dir に変更されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-460">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="6ccbd-461">DrvFs をマウントするときに Windows パスでスラッシュを使用できるようになりました。例: sudo mount-t drvfs/server/mnt/share</span><span class="sxs-lookup"><span data-stu-id="6ccbd-461">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="6ccbd-462">WSL は、インスタンスの開始時に/etc/fstab ファイルを処理するようになりました [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-462">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="6ccbd-463">これは、DrvFs ドライブを自動的にマウントする前に行われます。fstab によって既にマウントされているドライブは自動的には再マウントされないため、特定のドライブのマウントポイントを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-463">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="6ccbd-464">この動作は、wsl を使用して無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-464">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="6ccbd-465">Mount、mountinfo、および mountstats の各ファイルは、円記号やスペースなどの特殊文字を正しくエスケープします [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-465">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="6ccbd-466">WSL シンボリックリンクなどの DrvFs を使用して作成された特殊なファイル、またはメタデータが有効になっている場合は、fifo とソケットを使用して、Windows からコピーおよび移動できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-466">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="6ccbd-467">WSL は wsl. conf で構成可能</span><span class="sxs-lookup"><span data-stu-id="6ccbd-467">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="6ccbd-468">WSL で特定の機能を自動的に構成するためのメソッドを追加しました。これは、サブシステムを起動するたびに適用されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-468">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="6ccbd-469">これには、自動マウントオプションとネットワーク構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-469">This includes automount options and network configuration.</span></span> <span data-ttu-id="6ccbd-470">詳細については、次のブログ投稿を参照してください。 https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="6ccbd-470">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="6ccbd-471">AF_UNIX は、WSL および Windows ネイティブプロセスでの Linux プロセス間のソケット接続を許可します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-471">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="6ccbd-472">WSL と Windows アプリケーションは、Unix ソケット経由で相互に通信できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-472">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="6ccbd-473">Windows でサービスを実行し、Windows と WSL アプリの両方で使用できるようにする場合を考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-473">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="6ccbd-474">これは、Unix ソケットで可能です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-474">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="6ccbd-475">詳細については、ブログの投稿の「」を参照してください。 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="6ccbd-475">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-476">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-476">WSL</span></span>
* <span data-ttu-id="6ccbd-477">MAP_NORESERVE を使用した mmap () のサポート [GH 121、2784]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-477">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="6ccbd-478">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-478">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="6ccbd-479">複製で SIGCHLD 以外の終了シグナルを処理する [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-479">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="6ccbd-480">スタブ/proc/sys/fs/inotify/max_user_instances と/proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-480">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="6ccbd-481">0以外のオフセットで読み込みヘッダーを含む ELF バイナリの読み込み中にエラーが発生した [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-481">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="6ccbd-482">イメージの読み込み時に、ページの末尾のバイトをゼロアウトします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-482">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="6ccbd-483">Execve がサイレントモードでプロセスを終了するケースを減らす</span><span class="sxs-lookup"><span data-stu-id="6ccbd-483">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-484">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-484">Console</span></span>
* <span data-ttu-id="6ccbd-485">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-486">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-486">LTP Results:</span></span>
<span data-ttu-id="6ccbd-487">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-487">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="6ccbd-488">ビルド 17083</span><span class="sxs-lookup"><span data-stu-id="6ccbd-488">Build 17083</span></span>
<span data-ttu-id="6ccbd-489">ビルド17083の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-489">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-490">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-490">WSL</span></span>
* <span data-ttu-id="6ccbd-491">Epoll に関連するバグチェック (GH 2798、2801、2857) を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-491">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="6ccbd-492">ASLR をオフにするとハングを修正する [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-492">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="6ccbd-493">Mmap 操作がアトミックとして表示されることを確認する [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-493">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-494">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-494">Console</span></span>
* <span data-ttu-id="6ccbd-495">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-496">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-496">LTP Results:</span></span>
<span data-ttu-id="6ccbd-497">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-497">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="6ccbd-498">ビルド17074</span><span class="sxs-lookup"><span data-stu-id="6ccbd-498">Build 17074</span></span>
<span data-ttu-id="6ccbd-499">ビルド17074の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-499">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-500">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-500">WSL</span></span>
* <span data-ttu-id="6ccbd-501">DrvFs メタデータの固定ストレージ形式 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-501">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="6ccbd-502">**重要:** このビルドの前に作成された DrvFs メタデータは、正しく表示されないか、まったく表示されません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-502">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="6ccbd-503">影響を受けるファイルを修正するには、chmod と chown を使用してメタデータを再適用します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-503">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="6ccbd-504">複数のシグナルと再開可能な syscall の問題を修正した。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-504">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-505">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-505">Console</span></span>
* <span data-ttu-id="6ccbd-506">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-506">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-507">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-507">LTP Results:</span></span>
<span data-ttu-id="6ccbd-508">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-508">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="6ccbd-509">ビルド17063</span><span class="sxs-lookup"><span data-stu-id="6ccbd-509">Build 17063</span></span>
<span data-ttu-id="6ccbd-510">ビルド17063の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-510">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="6ccbd-511">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-511">WSL</span></span>
* <span data-ttu-id="6ccbd-512">DrvFs は、追加の Linux メタデータをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-512">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="6ccbd-513">これにより、chmod/chown を使用してファイルの所有者とモードを設定できるほか、fifo、unix ソケット、デバイスファイルなどの特殊なファイルを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-513">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="6ccbd-514">現時点では、これはまだ試験段階であるため、既定では無効になっています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-514">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="6ccbd-515">**注:** DrvFs で使用されるメタデータ形式のバグを修正しています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-515">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="6ccbd-516">メタデータは実験のためにこのビルドで機能しますが、今後のビルドでは、このビルドによって作成されたメタデータを正しく読み取ることができません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-516">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="6ccbd-517">変更したファイルの所有者を手動で更新しなければならない場合があります。カスタムデバイス ID を持つデバイスを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-517">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="6ccbd-518">有効にするには、メタデータオプションを使用して DrvFs をマウントします (既存のマウントで有効にするには、最初にマウントを解除する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-518">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="6ccbd-519">Linux のアクセス許可は、ファイルに追加のメタデータとして追加されます。Windows のアクセス許可には影響しません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-519">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="6ccbd-520">Windows エディターを使用してファイルを編集すると、メタデータが削除される場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-520">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="6ccbd-521">この場合、ファイルは既定のアクセス許可に戻ります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-521">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="6ccbd-522">メタデータなしでファイルを制御するための、DrvFs にマウントオプションを追加しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-522">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="6ccbd-523">uid: すべてのファイルの所有者に使用されるユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-523">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="6ccbd-524">gid: すべてのファイルの所有者に使用されるグループ ID。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-524">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="6ccbd-525">umask: すべてのファイルとディレクトリに対して除外するアクセス許可の8進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-525">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="6ccbd-526">fmask: すべての標準ファイルに対して除外するアクセス許可の8進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-526">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="6ccbd-527">dmask: すべてのディレクトリに対して除外するアクセス許可の8進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-527">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="6ccbd-528">例:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-528">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="6ccbd-529">メタデータオプションと組み合わせて、メタデータのないファイルに対する既定のアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-529">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="6ccbd-530">では、wsl と`WSLENV`Win32 の間で環境変数がどのように流れるかを構成するために、新しい環境変数が導入されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-530">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="6ccbd-531">例:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-531">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="6ccbd-532">`WSLENV`は、wsl から Win32 または Win32 プロセスから WSL プロセスを起動するときに含めることができる環境変数のコロン区切りの一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-532">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="6ccbd-533">各変数には、スラッシュとその後に続くフラグを付けて、変換方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-533">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="6ccbd-534">irtran-p値は、WSL パスと Win32 パスの間で変換されるパスです。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-534">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="6ccbd-535">左右値はパスの一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-535">l: The value is a list of paths.</span></span> <span data-ttu-id="6ccbd-536">WSL では、コロンで区切られたリストです。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-536">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="6ccbd-537">Win32 では、セミコロンで区切られたリストです。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-537">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="6ccbd-538">u値は、Win32 から WSL を呼び出すときにのみ含める必要があります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-538">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="6ccbd-539">リダイレクト値は、WSL から Win32 を呼び出すときにのみ含める必要があります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-539">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="6ccbd-540">ユーザーのカスタム`WSLENV` Windows 環境では、.bashrc またはを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-540">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="6ccbd-541">drvfs マウントによって tar、cp-p からのタイムスタンプが正しく保持される (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-541">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="6ccbd-542">drvfs symlink は正しいサイズを報告します (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-542">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="6ccbd-543">I/O サイズが非常に大きい場合の読み取り/書き込みの機能 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-543">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="6ccbd-544">waitpid はプロセスグループ Id と連動します (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-544">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="6ccbd-545">大きな予約領域での mmap パフォーマンスが大幅に向上しました。ghc のパフォーマンスを向上させます (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-545">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="6ccbd-546">READ_IMPLIES_EXEC でのパーソナリティのサポート最大化 a と clisp (GH 1185) を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-546">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="6ccbd-547">mprotect は PROT_GROWSDOWN をサポートしています。clisp (GH 1128) を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-547">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="6ccbd-548">過剰コミットモードでのページフォールトの修正sbcl (GH 1128) を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-548">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="6ccbd-549">複製では、より多くのフラグの組み合わせがサポートされます</span><span class="sxs-lookup"><span data-stu-id="6ccbd-549">clone supports more flags combinations</span></span>
* <span data-ttu-id="6ccbd-550">Epoll ファイルの select/epoll (以前は no op) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-550">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="6ccbd-551">未実装の syscall の ptrace を通知します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-551">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="6ccbd-552">Resolv.conf を生成するときにアップしていないインターフェイスを無視する [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-552">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="6ccbd-553">物理アドレスのないネットワークインターフェイスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-553">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="6ccbd-554">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-554">[GH 2685]</span></span>
* <span data-ttu-id="6ccbd-555">追加のバグの修正と改善。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-555">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="6ccbd-556">Windows の開発者が使用できる Linux ツール</span><span class="sxs-lookup"><span data-stu-id="6ccbd-556">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="6ccbd-557">Windows コマンドラインツールチェーンには、bsdtar (tar) と curl が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-557">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="6ccbd-558">この2つの新しいツールの追加の詳細と、Windows での開発者エクスペリエンスの整形方法を確認するには、[このブログ](https://aka.ms/tarcurlwindows)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-558">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="6ccbd-559">`AF_UNIX`は、Windows Insider SDK (17061 +) で利用できます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-559">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="6ccbd-560">の詳細と、Windows 上の`AF_UNIX`開発者が使用する方法については、[このブログ](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-560">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="6ccbd-561">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-561">Console</span></span>
* <span data-ttu-id="6ccbd-562">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-563">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-563">LTP Results:</span></span>
<span data-ttu-id="6ccbd-564">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-564">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="6ccbd-565">ビルド17046</span><span class="sxs-lookup"><span data-stu-id="6ccbd-565">Build 17046</span></span>

<span data-ttu-id="6ccbd-566">ビルド17046の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-566">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="6ccbd-567">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-567">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-568">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-568">WSL</span></span>
- <span data-ttu-id="6ccbd-569">アクティブなターミナルを使用せずにプロセスを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-569">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="6ccbd-570">[GH 709、1007、1511、2252、2391、et al.]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="6ccbd-571">CLONE_VFORK と CLONE_VM のサポートの強化。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-571">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="6ccbd-572">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-572">[GH 1878, 2615]</span></span>
- <span data-ttu-id="6ccbd-573">WSL ネットワーク操作の TDI フィルタードライバーをスキップします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-573">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="6ccbd-574">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-574">[GH 1554]</span></span>
- <span data-ttu-id="6ccbd-575">DrvFs は、特定の条件が満たされたときに NT シンボリックリンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-575">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="6ccbd-576">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-576">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="6ccbd-577">リンク先は相対パスである必要があり、マウントポイントやシンボリックリンクを越えることはできず、存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-577">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="6ccbd-578">開発者モードが有効になっていない場合は、ユーザーは SE_CREATE_SYMBOLIC_LINK_PRIVILEGE を持っている必要があります (通常は、管理者特権で起動する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-578">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="6ccbd-579">それ以外の状況でも、DrvFs は WSL シンボリックリンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-579">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="6ccbd-580">昇格および昇格されていない WSL インスタンスの同時実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-580">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="6ccbd-581">/Proc/sys/kernel/yama/ptrace_scope のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-581">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="6ccbd-582">Wslpath を追加して、WSL <-> Windows パス変換を実行します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-582">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="6ccbd-583">[GH 522、1243、1834、2327、et al]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-583">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="6ccbd-584">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-584">Console</span></span>
- <span data-ttu-id="6ccbd-585">修正はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-585">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-586">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-586">LTP Results:</span></span>
<span data-ttu-id="6ccbd-587">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-587">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="6ccbd-588">ビルド17040</span><span class="sxs-lookup"><span data-stu-id="6ccbd-588">Build 17040</span></span>

<span data-ttu-id="6ccbd-589">ビルド17040の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-589">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-590">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-591">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-591">WSL</span></span>
- <span data-ttu-id="6ccbd-592">17035以降の修正プログラムはありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-592">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-593">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-593">Console</span></span>
- <span data-ttu-id="6ccbd-594">17035以降の修正プログラムはありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-594">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-595">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-595">LTP Results:</span></span>
<span data-ttu-id="6ccbd-596">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-596">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="6ccbd-597">ビルド17035</span><span class="sxs-lookup"><span data-stu-id="6ccbd-597">Build 17035</span></span>

<span data-ttu-id="6ccbd-598">ビルド17035の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-598">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-599">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-599">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-600">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-600">WSL</span></span>
- <span data-ttu-id="6ccbd-601">DrvFs 上のファイルへのアクセスは、場合によっては、EINVAL で失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-601">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="6ccbd-602">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-602">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-603">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-603">Console</span></span>
- <span data-ttu-id="6ccbd-604">VT モードで行を挿入または削除するときに色が失われることがあります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-604">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-605">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-605">LTP Results:</span></span>
<span data-ttu-id="6ccbd-606">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-606">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="6ccbd-607">ビルド17025</span><span class="sxs-lookup"><span data-stu-id="6ccbd-607">Build 17025</span></span>

<span data-ttu-id="6ccbd-608">ビルド17025の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-608">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-609">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-609">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-610">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-610">WSL</span></span>
- <span data-ttu-id="6ccbd-611">新しいフォアグラウンドプロセスグループで初期プロセスを開始します [GH 1653, 2510]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-611">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="6ccbd-612">SIGHUP 配信の修正プログラム [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-612">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="6ccbd-613">[GH 2497] が指定されていない場合は、既定の仮想ブリッジ名を生成します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-613">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="6ccbd-614">/Proc/sys/kernel/random/boot_id [GH 2518] を実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-614">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="6ccbd-615">相互運用機能の stdout/stderr パイプの修正。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-615">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="6ccbd-616">Syncfs システム呼び出しをスタブします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-616">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-617">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-617">Console</span></span>
- <span data-ttu-id="6ccbd-618">サードパーティコンソールの入力 VT translation の修正 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-618">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-619">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-619">LTP Results:</span></span>
<span data-ttu-id="6ccbd-620">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-620">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="6ccbd-621">ビルド17017</span><span class="sxs-lookup"><span data-stu-id="6ccbd-621">Build 17017</span></span>

<span data-ttu-id="6ccbd-622">ビルド17017の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-622">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-623">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-623">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-624">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-624">WSL</span></span>
- <span data-ttu-id="6ccbd-625">空の ELF プログラムヘッダー [GH 330] を無視します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-625">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="6ccbd-626">LxssManager が非対話型ユーザーの WSL インスタンスを作成できるようにします (ssh およびスケジュールされたタスクのサポート) [GH 777, 1602]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-626">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="6ccbd-627">WSL-> Win32 > WSL ("設立") シナリオのサポート [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-627">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="6ccbd-628">相互運用機能によって起動されるコンソールアプリの終了の制限付きサポート [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-628">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="6ccbd-629">Devpts のマウントオプション [GH 1948] をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-629">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="6ccbd-630">Ptrace が子スタートアップをブロックしています [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-630">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="6ccbd-631">EPOLLET には、一部のイベント [GH 2462] がありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-631">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="6ccbd-632">PTRACE_GETSIGINFO の他のデータを返します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-632">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="6ccbd-633">Getdents と lseek では、正しくない結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-633">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="6ccbd-634">いくつかの Win32 相互運用アプリのハングを修正しました。これ以上データのないパイプで入力を待機しています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-634">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="6ccbd-635">O_ASYNC は、tty/pty ファイルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-635">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="6ccbd-636">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-636">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-637">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-637">Console</span></span>
- <span data-ttu-id="6ccbd-638">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-638">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-639">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-639">LTP Results:</span></span>
<span data-ttu-id="6ccbd-640">テストを実行中です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-640">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="6ccbd-641">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="6ccbd-641">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="6ccbd-642">ビルド16288</span><span class="sxs-lookup"><span data-stu-id="6ccbd-642">Build 16288</span></span>

<span data-ttu-id="6ccbd-643">ビルド16288の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-643">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-644">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-645">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-645">WSL</span></span>
- <span data-ttu-id="6ccbd-646">ソケットファイル記述子の uid、gid、およびモードを正しく初期化して報告する [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-646">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="6ccbd-647">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-647">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-648">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-648">Console</span></span>
- <span data-ttu-id="6ccbd-649">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-649">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-650">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-650">LTP Results:</span></span>
<span data-ttu-id="6ccbd-651">16273以降の変更はありません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-651">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="6ccbd-652">ビルド16278</span><span class="sxs-lookup"><span data-stu-id="6ccbd-652">Build 16278</span></span>

<span data-ttu-id="6ccbd-653">ビルド162738の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-653">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-654">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-655">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-655">WSL</span></span>
- <span data-ttu-id="6ccbd-656">LX MM 状態を解除するときに、ファイルによってサポートされるセクションのマップされたビューを明示的にマップ解除する [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-656">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="6ccbd-657">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-657">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-658">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-658">Console</span></span>
- <span data-ttu-id="6ccbd-659">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-660">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-660">LTP Results:</span></span>
<span data-ttu-id="6ccbd-661">16273以降の変更はありません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-661">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="6ccbd-662">ビルド16275</span><span class="sxs-lookup"><span data-stu-id="6ccbd-662">Build 16275</span></span>

<span data-ttu-id="6ccbd-663">ビルド162735の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-663">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-664">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-665">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-665">WSL</span></span>
- <span data-ttu-id="6ccbd-666">このリリースでは、WSL 関連の変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-666">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-667">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-667">Console</span></span>
- <span data-ttu-id="6ccbd-668">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-668">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-669">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-669">LTP Results:</span></span>
<span data-ttu-id="6ccbd-670">16273以降の変更はありません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-670">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="6ccbd-671">ビルド16273</span><span class="sxs-lookup"><span data-stu-id="6ccbd-671">Build 16273</span></span>

<span data-ttu-id="6ccbd-672">ビルド16273の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-672">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-673">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-674">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-674">WSL</span></span>
- <span data-ttu-id="6ccbd-675">DrvFs がディレクトリに対して正しくないファイルの種類を報告する場合があるという問題を修正しました [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-675">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="6ccbd-676">Uevent [GH 1121、2293、2242、2295、2235、648、637] を使用するプログラムのブロックを解除するための NETLINK_KOBJECT_UEVENT sockets の作成を許可します</span><span class="sxs-lookup"><span data-stu-id="6ccbd-676">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="6ccbd-677">非ブロッキング接続のサポートを追加する [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-677">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="6ccbd-678">CLONE_FS CLONE システム呼び出しフラグを実装する [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-678">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="6ccbd-679">NT interop でタブまたは引用符を正しく処理しない問題を修正する [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-679">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="6ccbd-680">WSL インスタンスを再起動しようとしたときにアクセス拒否エラーを解決する [GH 651、2095]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-680">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="6ccbd-681">Futex FUTEX_REQUEUE と FUTEX_CMP_REQUEUE 操作の実装 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-681">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="6ccbd-682">さまざまな SysFs ファイルのアクセス許可を修正する [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-682">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="6ccbd-683">セットアップ中に Haskell stack のハングを修正する [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-683">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="6ccbd-684">Binfmt_misc ' C ' ' O ' および ' P ' フラグを実装する [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-684">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="6ccbd-685">/Proc/sys/kernel/shmmax/shmmni & 追加する [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-685">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="6ccbd-686">Ioprio_set システム呼び出しの部分的なサポートを追加する [GH 498]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-686">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="6ccbd-687">スタブ SO_REUSEPORT & SO_PASSCRED for netlink sockets のサポートの追加 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-687">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="6ccbd-688">ディストリビューションが現在インストールまたはアンインストールされている場合は、RegisterDistribuiton から別のエラーコードを返します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-688">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="6ccbd-689">Wslconfig .exe 経由で部分的にインストールされた WSL ディストリビューションの登録解除を許可する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-689">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="6ccbd-690">Udp:: msg_peek から python ソケットテストハングを修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-690">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="6ccbd-691">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-691">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-692">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-692">Console</span></span>
- <span data-ttu-id="6ccbd-693">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-693">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-694">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-694">LTP Results:</span></span>
<span data-ttu-id="6ccbd-695">テストの合計:1904</span><span class="sxs-lookup"><span data-stu-id="6ccbd-695">Total Tests: 1904</span></span><br/>
<span data-ttu-id="6ccbd-696">スキップされたテストの合計数:209</span><span class="sxs-lookup"><span data-stu-id="6ccbd-696">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="6ccbd-697">合計エラー数:229</span><span class="sxs-lookup"><span data-stu-id="6ccbd-697">Total Failures: 229</span></span><br/>
[<span data-ttu-id="6ccbd-698">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-698">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="6ccbd-699">ビルド 16257</span><span class="sxs-lookup"><span data-stu-id="6ccbd-699">Build 16257</span></span>

<span data-ttu-id="6ccbd-700">ビルド16257の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-700">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-701">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-701">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-702">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-702">WSL</span></span>
- <span data-ttu-id="6ccbd-703">Prlimit64 システム呼び出しを実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-703">Implement prlimit64 system call</span></span>
- <span data-ttu-id="6ccbd-704">Ulimit-n (setrlimit RLIMIT_NOFILE) のサポートを追加する [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-704">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="6ccbd-705">TCP ソケットのスタブ MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-705">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="6ccbd-706">無効な AT_EXECFN 補助ベクター動作の修正 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-706">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="6ccbd-707">コンソール/tty のコピー/貼り付け動作を修正し、完全なバッファー処理をさらに追加する [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-707">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="6ccbd-708">AT_SECURE プログラムと set-group-ID プログラムの補助ベクターでの設定 [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-708">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="6ccbd-709">Psuedo-ターミナルマスターエンドポイントが TIOCPGRP を処理しない [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-709">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="6ccbd-710">Lseek が LxFs のディレクトリを巻き戻していることを修正する [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-710">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="6ccbd-711">大きな使用率が高くなった後の GH のロック [1882]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-711">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="6ccbd-712">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-712">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-713">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-713">Console</span></span>
- <span data-ttu-id="6ccbd-714">すべての場所で水平線/アンダースコアを修正する [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-714">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="6ccbd-715">プロセスの順序が変更されたことを修正し、NPM を閉じることが困難になる [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-715">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="6ccbd-716">新しい配色を追加しました。 https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="6ccbd-716">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-717">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-717">LTP Results:</span></span>
<span data-ttu-id="6ccbd-718">16251以降の変更はありません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-718">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-719">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-719">Syscall Support</span></span>
<span data-ttu-id="6ccbd-720">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-720">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-721">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-721">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="6ccbd-722">既知の問題</span><span class="sxs-lookup"><span data-stu-id="6ccbd-722">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="6ccbd-723">GitHub の問題 2392:Windows フォルダーは WSL によって認識されません...</span><span class="sxs-lookup"><span data-stu-id="6ccbd-723">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="6ccbd-724">ビルド16257では、を介し`/mnt/c/...`て Windows ファイル/フォルダーを列挙するときに、wsl に問題があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-724">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="6ccbd-725">この問題は修正されており、8/14/2017 の実行時に、Insider ビルドでリリースされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-725">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="6ccbd-726">ビルド16251</span><span class="sxs-lookup"><span data-stu-id="6ccbd-726">Build 16251</span></span>

<span data-ttu-id="6ccbd-727">ビルド16251の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-727">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-728">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-729">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-729">WSL</span></span>
- <span data-ttu-id="6ccbd-730">WSL オプションコンポーネントからベータタグを削除します。詳細については、[ブログの投稿](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-730">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="6ccbd-731">Set-ユーザー ID および set-ID バイナリが exec で正しく初期化されました。 exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-731">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="6ccbd-732">Ptrace PTRACE_O_TRACEEXIT のサポートを追加しました [GH 555]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-732">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="6ccbd-733">NT_FPREGSET を使用した ptrace PTRACE_GETFPREGS と PTRACE_GETREGSET のサポートを追加しました [GH 555]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-733">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="6ccbd-734">無視されたシグナルで停止する ptrace を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-734">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="6ccbd-735">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-735">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-736">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-736">Console</span></span>
- <span data-ttu-id="6ccbd-737">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-737">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-738">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-738">LTP Results:</span></span>
<span data-ttu-id="6ccbd-739">成功したテストの数:768</span><span class="sxs-lookup"><span data-stu-id="6ccbd-739">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="6ccbd-740">失敗したテストの数:244</span><span class="sxs-lookup"><span data-stu-id="6ccbd-740">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="6ccbd-741">スキップされたテストの数:96</span><span class="sxs-lookup"><span data-stu-id="6ccbd-741">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="6ccbd-742">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-742">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="6ccbd-743">ビルド16241</span><span class="sxs-lookup"><span data-stu-id="6ccbd-743">Build 16241</span></span>

<span data-ttu-id="6ccbd-744">ビルド16241の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-744">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-745">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-745">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="6ccbd-746">WSL</span><span class="sxs-lookup"><span data-stu-id="6ccbd-746">WSL</span></span>
- <span data-ttu-id="6ccbd-747">このリリースでは、WSL 関連の変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-747">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="6ccbd-748">Console</span><span class="sxs-lookup"><span data-stu-id="6ccbd-748">Console</span></span>
- <span data-ttu-id="6ccbd-749">[ここで](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)最初に報告された、10進線に誤った文字を出力するように修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-749">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="6ccbd-750">コードページ 65001 (utf8) に出力テキストが表示されないように修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-750">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="6ccbd-751">ある色の RGB 値に対して行われた変更を、選択の変更時にパレットの他の部分に転送しないでください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-751">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="6ccbd-752">これにより、コンソールプロパティシートが非常に使いやすいようになります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-752">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="6ccbd-753">Ctrl + S が正しく動作していません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-753">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="6ccbd-754">ANSI エスケープコードに完全に存在しない太字/-Dim [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-754">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="6ccbd-755">コンソールが Vim 色のテーマを正しくサポートしていない [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-755">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="6ccbd-756">特定の文字を貼り付けることはできません [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-756">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="6ccbd-757">編集/コマンドライン上にあるときに bash ウィンドウのサイズを変更すると、リフローサイズの変更がおかしくなる [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-757">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="6ccbd-758">Ctrl + L を押したまま画面をダーティにする [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-758">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="6ccbd-759">HDPI で VT を表示するときのコンソールレンダリングのバグ [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-759">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="6ccbd-760">Unicode 文字 U + 30FB で Japansese 文字が奇妙に見える [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-760">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="6ccbd-761">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-761">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="6ccbd-762">ビルド 16237</span><span class="sxs-lookup"><span data-stu-id="6ccbd-762">Build 16237</span></span>

<span data-ttu-id="6ccbd-763">ビルド16237の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-763">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-764">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-764">Fixed</span></span>
- <span data-ttu-id="6ccbd-765">Lxfs に EAs がないファイルの既定の属性を使用する (ルート、ルート、0000)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-765">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="6ccbd-766">拡張属性を使用するディストリビューションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-766">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="6ccbd-767">Getdents と getdents64 によって返されるエントリの埋め込みを修正する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-767">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="6ccbd-768">Shmctl SHM_STAT システム呼び出しのアクセス許可チェックを修正する [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-768">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="6ccbd-769">Tty の初期 epoll 状態が正しくないことを修正した [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-769">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="6ccbd-770">すべてのエントリを返さないように DrvFs readdir を修正する [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-770">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="6ccbd-771">ファイルのリンクが解除されたときに LxFs readdir を修正する [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-771">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="6ccbd-772">Procfs を使用して、リンクされていない drvfs ファイルを再び開くことを許可する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-772">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="6ccbd-773">WSL 機能を無効にするためのグローバルレジストリキーの上書き (相互運用/ドライブのマウント) を追加しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-773">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="6ccbd-774">DrvFs (および LxFs) の "stat" で間違ったブロックカウントを修正する [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-774">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="6ccbd-775">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-775">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="6ccbd-776">ビルド16232</span><span class="sxs-lookup"><span data-stu-id="6ccbd-776">Build 16232</span></span>

<span data-ttu-id="6ccbd-777">ビルド16232の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-777">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-778">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-778">Fixed</span></span>
- <span data-ttu-id="6ccbd-779">このリリースでは、WSL 関連の変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-779">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="6ccbd-780">ビルド16226</span><span class="sxs-lookup"><span data-stu-id="6ccbd-780">Build 16226</span></span>

<span data-ttu-id="6ccbd-781">ビルド16226の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-781">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-782">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-782">Fixed</span></span>
- <span data-ttu-id="6ccbd-783">xattr 関連の syscall サポート (getxattr、setxattr、listxattr、removexattr)。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-783">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="6ccbd-784">capablity xattr のサポート。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-784">security.capablity xattr support.</span></span>
- <span data-ttu-id="6ccbd-785">特定のファイルシステムとフィルター (MS 以外の SMB サーバーを含む) との互換性が向上しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-785">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="6ccbd-786">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-786">[GH #1952]</span></span>
- <span data-ttu-id="6ccbd-787">OneDrive プレースホルダー、GVFS プレースホルダー、および圧縮された OS 圧縮ファイルのサポートが強化されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-787">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="6ccbd-788">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-788">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="6ccbd-789">ビルド16215</span><span class="sxs-lookup"><span data-stu-id="6ccbd-789">Build 16215</span></span>

<span data-ttu-id="6ccbd-790">ビルド16215の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-790">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-791">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-791">Fixed</span></span>
- <span data-ttu-id="6ccbd-792">WSL には開発者モードが不要になりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-792">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="6ccbd-793">Drvfs のディレクトリの接合をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-793">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="6ccbd-794">WSL distribution appx パッケージのアンインストールを処理します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-794">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="6ccbd-795">Procfs を更新して、プライベートと共有のマッピングを表示します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-795">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="6ccbd-796">Wslconfig .exe を追加して、部分的にインストールまたはアンインストールされたディストリビューションをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-796">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="6ccbd-797">TCP ソケット用の IP_MTU_DISCOVER のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-797">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="6ccbd-798">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-798">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="6ccbd-799">AF_INADDR へのルートのプロトコルファミリを推定します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-799">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="6ccbd-800">シリアルデバイスの機能強化 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-800">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="6ccbd-801">ビルド16199</span><span class="sxs-lookup"><span data-stu-id="6ccbd-801">Build 16199</span></span>

<span data-ttu-id="6ccbd-802">ビルド16199の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-802">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-803">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-803">Fixed</span></span>
- <span data-ttu-id="6ccbd-804">これらのリリースでは、WSL 関連の変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-804">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="6ccbd-805">ビルド16193</span><span class="sxs-lookup"><span data-stu-id="6ccbd-805">Build 16193</span></span>

<span data-ttu-id="6ccbd-806">ビルド16193の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-806">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-807">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-807">Fixed</span></span>
- <span data-ttu-id="6ccbd-808">送信 SIGCONT と threadgroup 終了の間の競合状態 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-808">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="6ccbd-809">tty および pty デバイスを FILE_DEVICE_CONSOLE ではなくレポート FILE_DEVICE_NAMED_PIPE に変更する [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-809">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="6ccbd-810">IP_OPTIONS の SSH 修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-810">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="6ccbd-811">DrvFs を init デーモンにマウントしました [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-811">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="6ccbd-812">次の NT シンボリックリンクに対する DrvFs のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-812">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="6ccbd-813">ビルド16184</span><span class="sxs-lookup"><span data-stu-id="6ccbd-813">Build 16184</span></span>

<span data-ttu-id="6ccbd-814">ビルド16184の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-814">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-815">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-815">Fixed</span></span>
- <span data-ttu-id="6ccbd-816">Apt パッケージのメンテナンスタスク (lxrun/update) を削除しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-816">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="6ccbd-817">Node.js の Windows プロセスからに表示されない修正済みの出力 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-817">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="6ccbd-818">Lxcore での調整要件の緩和 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-818">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="6ccbd-819">システム呼び出しの数値における AT_EMPTY_PATH フラグの処理を修正した。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-819">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="6ccbd-820">開いているハンドルを持つ DrvFs ファイルを削除すると、ファイルに未定義の動作が発生する問題を修正した (GH 544、966、1357、1535、1615)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-820">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="6ccbd-821">/etc/hosts は Windows hosts ファイル (%windir%\system32\drivers\etc\hosts) からエントリを継承するようになりました [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-821">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="6ccbd-822">ビルド16179</span><span class="sxs-lookup"><span data-stu-id="6ccbd-822">Build 16179</span></span>

<span data-ttu-id="6ccbd-823">ビルド16179の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-823">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-824">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-824">Fixed</span></span>
- <span data-ttu-id="6ccbd-825">今週、WSL の変更はありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-825">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="6ccbd-826">ビルド16176</span><span class="sxs-lookup"><span data-stu-id="6ccbd-826">Build 16176</span></span>

<span data-ttu-id="6ccbd-827">ビルド16176の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-827">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-828">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-828">Fixed</span></span>

- [<span data-ttu-id="6ccbd-829">有効なシリアルサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-829">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="6ccbd-830">追加された IP ソケットオプション IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-830">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="6ccbd-831">Pwritev 関数の実装 (nginx/PHP-FPM へのファイルのアップロード) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-831">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="6ccbd-832">追加された IP ソケットオプション IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-832">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="6ccbd-833">ソケットオプション IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP のサポート [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-833">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="6ccbd-834">Apps ノード、traceroute、掘り下げ、nslookup、host の IP (V6) MTU socket オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-834">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="6ccbd-835">追加された IP ソケットオプション IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="6ccbd-835">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="6ccbd-836">ファイルシステムの機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-836">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="6ccbd-837">UNC パスのマウントを許可する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-837">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="6ccbd-838">Drvfs で CDF サポートを有効にする</span><span class="sxs-lookup"><span data-stu-id="6ccbd-838">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="6ccbd-839">Drvfs でネットワークファイルシステムのアクセス許可を正しく処理する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-839">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="6ccbd-840">Drvfs にリモートドライブのサポートを追加する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-840">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="6ccbd-841">Drvfs での FAT サポートを有効にする</span><span class="sxs-lookup"><span data-stu-id="6ccbd-841">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="6ccbd-842">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-842">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-843">LTP の結果</span><span class="sxs-lookup"><span data-stu-id="6ccbd-843">LTP Results</span></span>
<span data-ttu-id="6ccbd-844">15042以降の変更はありません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-844">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="6ccbd-845">ビルド16170</span><span class="sxs-lookup"><span data-stu-id="6ccbd-845">Build 16170</span></span>

<span data-ttu-id="6ccbd-846">ビルド16170の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-846">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="6ccbd-847">WSL のテストの取り組みについて説明する新しい[ブログ投稿](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)をリリースしました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-847">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="6ccbd-848">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-848">Fixed</span></span>

- <span data-ttu-id="6ccbd-849">サポートソケットオプション IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-849">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="6ccbd-850">PTRACE_OLDSETOPTIONS のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-850">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="6ccbd-851">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-851">[GH 1692]</span></span>
- <span data-ttu-id="6ccbd-852">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-852">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-853">LTP の結果</span><span class="sxs-lookup"><span data-stu-id="6ccbd-853">LTP Results</span></span>
<span data-ttu-id="6ccbd-854">15042以降の変更はありません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-854">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="6ccbd-855">ビルド15046から Windows 10 の作成者への更新</span><span class="sxs-lookup"><span data-stu-id="6ccbd-855">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="6ccbd-856">Windows 10 の作成者の更新プログラムに含まれるように計画されている WSL 修正プログラムや機能はこれ以上ありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-856">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="6ccbd-857">WSL のリリースノートは、次の主要な Windows Update を対象とした追加のために、今後数週間にわたって再開されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-857">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="6ccbd-858">ビルド15046および今後の Insider リリースに関する一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-858">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="6ccbd-859">ビルド15042</span><span class="sxs-lookup"><span data-stu-id="6ccbd-859">Build 15042</span></span>

<span data-ttu-id="6ccbd-860">ビルド15042の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-860">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-861">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-861">Fixed</span></span>

- <span data-ttu-id="6ccbd-862">"." で終わるパスの削除時にデッドロックが発生する問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-862">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="6ccbd-863">FIONBIO が成功時に0を返さないという問題を修正した [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-863">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="6ccbd-864">Inet データグラムソケットの長さゼロの読み取りに関する問題を修正した</span><span class="sxs-lookup"><span data-stu-id="6ccbd-864">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="6ccbd-865">Drvfs inode 参照で競合状態が発生したことが原因でデッドロックが発生する可能性を修正する [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-865">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="6ccbd-866">Unix ソケットの補助データの拡張サポートSCM_CREDENTIALS および SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-866">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="6ccbd-867">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-867">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-868">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-868">LTP Results:</span></span>
<span data-ttu-id="6ccbd-869">成功したテストの数:737</span><span class="sxs-lookup"><span data-stu-id="6ccbd-869">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="6ccbd-870">非パッシング (失敗、スキップされたなど) の数:255</span><span class="sxs-lookup"><span data-stu-id="6ccbd-870">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="6ccbd-871">ビルド15031</span><span class="sxs-lookup"><span data-stu-id="6ccbd-871">Build 15031</span></span>

<span data-ttu-id="6ccbd-872">ビルド15031の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-872">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-873">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-873">Fixed</span></span>

- <span data-ttu-id="6ccbd-874">Time (2) が散発的に不適切な動作するバグを修正しています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-874">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="6ccbd-875">\* SIGSYSCALL MASK がシグナルマスクを破壊する可能性がある問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-875">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="6ccbd-876">WSL プロセス作成通知でコマンドラインの完全な長さを返すようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-876">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="6ccbd-877">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-877">[GH 1632]</span></span>
- <span data-ttu-id="6ccbd-878">WSL は、GDB がハングした場合に ptrace を介してスレッドの終了を報告するようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-878">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="6ccbd-879">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-879">[GH 1196]</span></span>
- <span data-ttu-id="6ccbd-880">Tmux IO が大量に発生した後に ptys がハングするバグを修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-880">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="6ccbd-881">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-881">[GH 1358]</span></span>
- <span data-ttu-id="6ccbd-882">多くのシステムコールでタイムアウトの検証を修正 (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-882">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="6ccbd-883">追加された eventfd EFD_SEMAPHORE サポート [GH 452]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-883">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="6ccbd-884">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-884">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-885">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-885">LTP Results:</span></span>
<span data-ttu-id="6ccbd-886">成功したテストの数:737</span><span class="sxs-lookup"><span data-stu-id="6ccbd-886">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="6ccbd-887">非パッシング (失敗、スキップされたなど) の数:255</span><span class="sxs-lookup"><span data-stu-id="6ccbd-887">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6ccbd-888">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-888">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="6ccbd-889">ビルド15025</span><span class="sxs-lookup"><span data-stu-id="6ccbd-889">Build 15025</span></span>

<span data-ttu-id="6ccbd-890">ビルド15025の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-890">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-891">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-891">Fixed</span></span>

- <span data-ttu-id="6ccbd-892">Grep 2.27 を破損したバグの修正 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-892">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="6ccbd-893">Eventfd2 syscall の EFD_SEMAPHORE フラグの実装 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-893">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="6ccbd-894">実装された/proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-894">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="6ccbd-895">Unix ストリームソケットに対するシグナル駆動型 IO のサポート [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-895">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="6ccbd-896">F_GETPIPE_SZ と F_SETPIPE_SZ のサポート [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-896">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="6ccbd-897">Recvmmsg () syscall の実装 [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-897">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="6ccbd-898">Epoll_wait () が待機していないバグを修正 [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-898">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="6ccbd-899">/Proc/version_signature を実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-899">Implement /proc/version_signature</span></span>
- <span data-ttu-id="6ccbd-900">T syscall は、両方のファイル記述子が同じパイプを参照している場合にエラーを返すようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-900">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="6ccbd-901">Unix ソケット用の SO_PEERCRED の正しい動作を実装しています</span><span class="sxs-lookup"><span data-stu-id="6ccbd-901">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="6ccbd-902">Tkill syscall の無効なパラメーター処理を修正した</span><span class="sxs-lookup"><span data-stu-id="6ccbd-902">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="6ccbd-903">Drvfs の preformace を増やすための変更</span><span class="sxs-lookup"><span data-stu-id="6ccbd-903">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="6ccbd-904">Ruby IO ブロックの軽微な修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-904">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="6ccbd-905">Inet sockets の MSG_DONTWAIT フラグの EINVAL を返す recvmsg () を修正した [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-905">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="6ccbd-906">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-906">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-907">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-907">LTP Results:</span></span>
<span data-ttu-id="6ccbd-908">成功したテストの数:732</span><span class="sxs-lookup"><span data-stu-id="6ccbd-908">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="6ccbd-909">非パッシング (失敗、スキップされたなど) の数:255</span><span class="sxs-lookup"><span data-stu-id="6ccbd-909">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6ccbd-910">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-910">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="6ccbd-911">ビルド15019</span><span class="sxs-lookup"><span data-stu-id="6ccbd-911">Build 15019</span></span>

<span data-ttu-id="6ccbd-912">ビルド15019の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-912">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-913">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-913">Fixed</span></span>

- <span data-ttu-id="6ccbd-914">Htop (GH 823、945、971) などのツールに対して procfs の CPU 使用率が誤って報告されたバグを修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-914">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="6ccbd-915">既存のファイルに対して O_TRUNC を使用して open () を呼び出すと、IN_OPEN の前に IN_MODIFY が生成されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-915">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="6ccbd-916">Unix socket getsockopt SO_ERROR で postgress [GH 61, 1354] を有効にするための修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-916">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="6ccbd-917">/Proc/sys/net/core/somaxconn を実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-917">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="6ccbd-918">Apt-パッケージ更新のバックグラウンドタスクをビューから非表示にするようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-918">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="6ccbd-919">Ipv6 localhost のスコープをクリアします (Spring Framework (Java) エラー)。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-919">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="6ccbd-920">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-920">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-921">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-921">LTP Results:</span></span>
<span data-ttu-id="6ccbd-922">成功したテストの数:714</span><span class="sxs-lookup"><span data-stu-id="6ccbd-922">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="6ccbd-923">非パッシング (失敗、スキップされたなど) の数:249</span><span class="sxs-lookup"><span data-stu-id="6ccbd-923">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="6ccbd-924">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-924">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="6ccbd-925">ビルド15014</span><span class="sxs-lookup"><span data-stu-id="6ccbd-925">Build 15014</span></span>

<span data-ttu-id="6ccbd-926">ビルド15014の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-926">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-927">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-927">Fixed</span></span>

- <span data-ttu-id="6ccbd-928">Ctrl + C は意図したとおりに動作するようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-928">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="6ccbd-929">htop と ps auxw で、正しいリソース使用率 (GH #516) が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-929">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="6ccbd-930">NT 例外からシグナルへの基本的な変換です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-930">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="6ccbd-931">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-931">(GH #513)</span></span>
- <span data-ttu-id="6ccbd-932">fallocate は、EINVAL (GH #1571) ではなく領域が不足しているときに、ENOSPC で失敗するようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-932">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="6ccbd-933">追加された/proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-933">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="6ccbd-934">Semop および semtimedop システム呼び出しを実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-934">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="6ccbd-935">IP_RECVTOS & IPV6_RECVTCLASS socket オプションで nslookup エラーを修正した (GH 69)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-935">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="6ccbd-936">ソケットオプションの IP_RECVTTL と IPV6_RECVHOPLIMIT のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-936">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="6ccbd-937">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-937">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-938">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-938">LTP Results:</span></span>
<span data-ttu-id="6ccbd-939">成功したテストの数:709</span><span class="sxs-lookup"><span data-stu-id="6ccbd-939">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="6ccbd-940">非パッシング (失敗、スキップされたなど) の数:255</span><span class="sxs-lookup"><span data-stu-id="6ccbd-940">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6ccbd-941">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-941">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="6ccbd-942">Syscall の概要</span><span class="sxs-lookup"><span data-stu-id="6ccbd-942">Syscall Summary</span></span>
<span data-ttu-id="6ccbd-943">合計 Syscall:384</span><span class="sxs-lookup"><span data-stu-id="6ccbd-943">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="6ccbd-944">実装された合計:235</span><span class="sxs-lookup"><span data-stu-id="6ccbd-944">Total Implemented: 235</span></span> </br>
<span data-ttu-id="6ccbd-945">スタブの合計数:22</span><span class="sxs-lookup"><span data-stu-id="6ccbd-945">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="6ccbd-946">未実装の合計数:127</span><span class="sxs-lookup"><span data-stu-id="6ccbd-946">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="6ccbd-947">詳細な内訳</span><span class="sxs-lookup"><span data-stu-id="6ccbd-947">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="6ccbd-948">ビルド15007</span><span class="sxs-lookup"><span data-stu-id="6ccbd-948">Build 15007</span></span>

<span data-ttu-id="6ccbd-949">ビルド15007の一般的な Windows 情報については、 [windows のブログ]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-949">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="6ccbd-950">既知の問題</span><span class="sxs-lookup"><span data-stu-id="6ccbd-950">Known Issue</span></span>

- <span data-ttu-id="6ccbd-951">コンソールが一部の Ctrl + <key>入力を認識しないという既知のバグがあります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="6ccbd-952">これには、通常の "c" キーの押下として機能する ctrl + c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="6ccbd-953">回避策:代替キーを Ctrl + C にマップします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="6ccbd-954">たとえば、ctrl + K を Ctrl + C キーにマップするに`stty intr \^k`は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="6ccbd-955">このマッピングはターミナル単位で行われ、bash が起動されるたび*に実行さ*れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="6ccbd-956">ユーザーは、オプションを調べて、`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="6ccbd-956">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="6ccbd-957">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-957">Fixed</span></span>

- <span data-ttu-id="6ccbd-958">WSL を実行すると CPU コアの 100% が消費される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-958">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="6ccbd-959">ソケットオプション IP_PKTINFO、IPV6_RECVPKTINFO がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-959">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="6ccbd-960">(GH #851、987)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-960">(GH #851, 987)</span></span>
- <span data-ttu-id="6ccbd-961">Lxcore でネットワークインターフェイスの物理アドレスを16バイトに切り捨てる (GH #1452、1414、1343、468、308)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-961">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="6ccbd-962">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-962">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-963">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-963">LTP Results:</span></span>
<span data-ttu-id="6ccbd-964">成功したテストの数:709</span><span class="sxs-lookup"><span data-stu-id="6ccbd-964">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="6ccbd-965">非パッシング (失敗、スキップされたなど) の数:255</span><span class="sxs-lookup"><span data-stu-id="6ccbd-965">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="6ccbd-966">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-966">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="6ccbd-967">ビルド15002</span><span class="sxs-lookup"><span data-stu-id="6ccbd-967">Build 15002</span></span>

<span data-ttu-id="6ccbd-968">ビルド15002の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-968">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="6ccbd-969">既知の問題</span><span class="sxs-lookup"><span data-stu-id="6ccbd-969">Known Issue</span></span>

<span data-ttu-id="6ccbd-970">2つの既知の問題:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-970">Two known issues:</span></span>
- <span data-ttu-id="6ccbd-971">コンソールが一部の Ctrl + <key>入力を認識しないという既知のバグがあります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="6ccbd-972">これには、通常の "c" キーの押下として機能する ctrl + c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="6ccbd-973">回避策:代替キーを Ctrl + C にマップします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="6ccbd-974">たとえば、ctrl + K を Ctrl + C キーにマップするに`stty intr \^k`は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="6ccbd-975">このマッピングはターミナル単位で行われ、bash が起動されるたび*に実行さ*れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="6ccbd-976">ユーザーは、オプションを調べて、`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="6ccbd-976">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="6ccbd-977">WSL が実行されている間、システムスレッドは CPU コアの 100% を消費します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-977">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="6ccbd-978">根本原因は、内部的に解決されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-978">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="6ccbd-979">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-979">Fixed</span></span>

- <span data-ttu-id="6ccbd-980">すべての bash セッションは、同じアクセス許可レベルで作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-980">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="6ccbd-981">別のレベルでセッションを開始しようとすると、ブロックされます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-981">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="6ccbd-982">つまり、管理者コンソールと管理者以外のコンソールを同時に実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-982">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="6ccbd-983">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-983">(GH #626)</span></span>
<br/>
- <span data-ttu-id="6ccbd-984">次の NETLINK_ROUTE メッセージを実装した (Windows 管理者が必要)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-984">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="6ccbd-985">RTM_NEWADDR (サポート`ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-985">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="6ccbd-986">RTM_NEWROUTE (サポート`ip route add`)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-986">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="6ccbd-987">RTM_DELADDR (サポート`ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-987">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="6ccbd-988">RTM_DELROUTE (サポート`ip route del`)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-988">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="6ccbd-989">更新するパッケージのスケジュールされたタスクは、従量制課金接続では実行されなくなります (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-989">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="6ccbd-990">パイプがスタックした場合のエラーを修正します。 bash-c "ls-alR/" |bash-c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-990">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="6ccbd-991">実装された TCP_KEEPCNT socket オプション (GH #843)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-991">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="6ccbd-992">IP_MTU_DISCOVER INET socket オプション (GH #720、717、170、69) を実装しています</span><span class="sxs-lookup"><span data-stu-id="6ccbd-992">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="6ccbd-993">Nt パス参照を使用して init から NT バイナリを実行する従来の機能を削除しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-993">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="6ccbd-994">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-994">(GH #1325)</span></span>
- <span data-ttu-id="6ccbd-995">グループまたはその他の読み取りアクセスを許可するように更新モードを修正する (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-995">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="6ccbd-996">実装された/proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-996">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="6ccbd-997">プロセスの開始時刻が2432年 (GH #974) と表示されたエラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-997">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="6ccbd-998">既定の用語環境変数を xterm-256 色に切り替えました (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-998">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="6ccbd-999">プロセスフォーク中にコミットが計算される方法を変更しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-999">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="6ccbd-1000">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1000">(GH #1286)</span></span>
- <span data-ttu-id="6ccbd-1001">/Proc/sys/vm/overcommit_memory. の実装</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1001">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="6ccbd-1002">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1002">(GH #1286)</span></span>
- <span data-ttu-id="6ccbd-1003">実装された/proc/net/route ファイル (GH #69)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1003">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="6ccbd-1004">ショートカット名が正しくローカライズされていないエラーを修正しました (GH #696)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1004">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="6ccbd-1005">プログラムヘッダーの検証に誤りのある elf 解析ロジックを修正した場合は、PATH_MAX 未満である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1005">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="6ccbd-1006">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1006">(GH #1048)</span></span>
- <span data-ttu-id="6ccbd-1007">Procfs、sysfs、cgroupfs、および binfmtfs (GH #1378) の statfs コールバックを実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1007">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="6ccbd-1008">閉じることのできない AptPackageIndexUpdate ウィンドウを修正しました (GH #1184、GH #1193 で説明)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1008">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="6ccbd-1009">ASLR パーソナリティ ADDR_NO_RANDOMIZE のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1009">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="6ccbd-1010">(GH #1148、1128)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1010">(GH #1148, 1128)</span></span>
- <span data-ttu-id="6ccbd-1011">AV 中に適切な gdb スタックトレースを実現するための PTRACE_GETSIGINFO、SIGSEGV が改善されました (GH #875)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1011">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="6ccbd-1012">Elf の解析は、パッチ elf バイナリでは失敗します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1012">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="6ccbd-1013">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1013">(GH #471)</span></span>
- <span data-ttu-id="6ccbd-1014">/Etc/resolv.conf に反映された VPN DNS (GH #416、1350)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1014">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="6ccbd-1015">より信頼性の高いデータ転送のための TCP close の機能強化。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1015">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="6ccbd-1016">(GH #610、616、1025、1335)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1016">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="6ccbd-1017">開いているファイルが多すぎる場合 (EMFILE)、適切なエラーコードを返すようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1017">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="6ccbd-1018">(GH #1126、2090)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1018">(GH #1126, 2090)</span></span>
- <span data-ttu-id="6ccbd-1019">Windows 監査ログで、プロセス作成の監査でイメージ名が報告されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1019">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="6ccbd-1020">Bash ウィンドウ内から bash を起動すると、正常に失敗する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1020">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="6ccbd-1021">相互運用機能が LxFs で作業ディレクトリにアクセスできないときにエラーメッセージが追加されました (例: .bashrc)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1021">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="6ccbd-1022">WSL で Windows パスが切り捨てられた問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1022">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="6ccbd-1023">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1024">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1024">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1025">成功したテストの数:690</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1025">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="6ccbd-1026">非パッシング (失敗、スキップされたなど) の数:274</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1026">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="6ccbd-1027">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1028">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1028">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1029">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1029">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1030">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1030">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="6ccbd-1031">ビルド14986</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1031">Build 14986</span></span>

<span data-ttu-id="6ccbd-1032">ビルド14986の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1032">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1033">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1033">Fixed</span></span>

- <span data-ttu-id="6ccbd-1034">Netlink および Pty Ioctl を使用したバグチェックの修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1034">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="6ccbd-1035">カーネルのバージョンが Xenial との一貫性のために 4.4.0-43 を報告するようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1035">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="6ccbd-1036">"Nul:" にリダイレクトされたときに Bash が起動するようになりました (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1036">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="6ccbd-1037">Procfs (GH #967) でスレッド Id が正しくレポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1037">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="6ccbd-1038">IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |IN_ISDIR フラグが inotify_add_watch () でサポートされるようになりました (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="6ccbd-1039">Timer_create と関連するシステムコールを実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1039">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="6ccbd-1040">これにより、GHC サポート (GH #307) が可能になります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1040">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="6ccbd-1041">Ping によって 0.000 m の時間 (GH #1296) が返された問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1041">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="6ccbd-1042">開いているファイルが多すぎる場合は、正しいエラーコードを返します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1042">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="6ccbd-1043">WSL の Netlink 要求が、インターフェイスのハードウェアアドレスが32バイト (Teredo インターフェイスなど) の場合は EINVAL で失敗する問題を修正した。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1043">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="6ccbd-1044">Linux の "ip" ユーティリティには、WSL が32バイトのハードウェアアドレスを報告した場合にクラッシュするバグが含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1044">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="6ccbd-1045">これは、WSL ではなく、"ip" のバグです。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1045">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="6ccbd-1046">"Ip" ユーティリティは、ハードウェアアドレスの印刷に使用される文字列バッファーの長さをハードコーディングします。また、32バイトのハードウェアアドレスを出力するには、バッファーが小さすぎます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1046">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="6ccbd-1047">その他の修正プログラムと機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1047">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1048">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1048">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1049">成功したテストの数:669</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1049">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="6ccbd-1050">非パッシング (失敗、スキップされたなど) の数:258</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1050">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="6ccbd-1051">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1051">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1052">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1052">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1053">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1053">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1054">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1054">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="6ccbd-1055">ビルド14971</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1055">Build 14971</span></span>

<span data-ttu-id="6ccbd-1056">ビルド14971の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1056">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1057">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1057">Fixed</span></span>

 - <span data-ttu-id="6ccbd-1058">Windows Subsystem for Linux では、コントロールを超える状況により、このビルドには更新プログラムがありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1058">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="6ccbd-1059">定期的にスケジュールされた更新は、次回のリリースで再開されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1059">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1060">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1060">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1061">14965から変更されていません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1061">Unchanged from 14965</span></span> </br>
<span data-ttu-id="6ccbd-1062">成功したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1062">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="6ccbd-1063">非パッシング (失敗、スキップされたなど) の数:263</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1063">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6ccbd-1064">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1064">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="6ccbd-1065">ビルド14965</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1065">Build 14965</span></span>

<span data-ttu-id="6ccbd-1066">ビルド14965の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1066">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1067">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1067">Fixed</span></span>

- <span data-ttu-id="6ccbd-1068">Netlink sockets NETLINK_ROUTE protocol の RTM_GETLINK および RTM_GETADDR (GH #468) のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1068">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="6ccbd-1069">ネットワーク列挙に対する ifconfig および ip コマンドを有効にします</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1069">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="6ccbd-1070">詳細については、 [Wsl ネットワークに関するブログ記事](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1070">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="6ccbd-1071">/sbin がユーザーのパスに既定で含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1071">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="6ccbd-1072">NT ユーザーパスが既定で WSL パスに追加されました (つまり、Linux パスに System32 を追加せずに notepad.exe を入力できるようになりました)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1072">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="6ccbd-1073">/Proc/sys/kernel/cap_last_cap のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1073">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="6ccbd-1074">現在の作業ディレクトリに ansi 以外の文字が含まれている場合、WSL から NT バイナリを起動できるようになりました (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1074">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="6ccbd-1075">切断された unix ストリームソケットでのシャットダウンを許可します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1075">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="6ccbd-1076">PR_GET_PDEATHSIG のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1076">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="6ccbd-1077">CLONE_PARENT のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1077">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="6ccbd-1078">パイプがスタックした場合のエラーを修正します。 bash-c "ls-alR/" |bash-c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1078">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="6ccbd-1079">現在のターミナルに接続するための要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1079">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="6ccbd-1080">/Proc/<pid>/oom_score_adj を書き込み可能としてマークします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1080">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="6ccbd-1081">/Fs フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1081">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="6ccbd-1082">sched_setaffinity は、関係ビットマスクの数を返す必要があります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1082">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="6ccbd-1083">インタープリターパスの長さが64文字未満であることを誤って想定している ELF 検証ロジックを修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1083">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="6ccbd-1084">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1084">(GH #743)</span></span>
- <span data-ttu-id="6ccbd-1085">開いているファイル記述子は、コンソールウィンドウを開いたままにすることができます (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1085">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="6ccbd-1086">名前の変更 () がターゲット名の末尾のスラッシュで失敗した Fixeed エラー (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1086">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="6ccbd-1087">/Proc/net/dev ファイルを実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1087">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="6ccbd-1088">タイマー精度による 0.000 ms ping を修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1088">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="6ccbd-1089">実装された/proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1089">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="6ccbd-1090">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1090">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1091">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1091">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1092">成功したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1092">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="6ccbd-1093">非パッシング (失敗、スキップされたなど) の数:263</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1093">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6ccbd-1094">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1094">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="6ccbd-1095">ビルド14959</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1095">Build 14959</span></span>

<span data-ttu-id="6ccbd-1096">ビルド14959の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1096">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1097">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1097">Fixed</span></span>

- <span data-ttu-id="6ccbd-1098">Windows の Pico Process 通知が改善されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1098">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="6ccbd-1099">[Wsl ブログ](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)に記載されている追加情報。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1099">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="6ccbd-1100">Windows の相互運用性による安定性の向上</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1100">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="6ccbd-1101">エンタープライズデータ保護 (EDP) が有効になっている場合に bash を起動したときのエラー0x80070057 を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1101">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="6ccbd-1102">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1102">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1103">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1103">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1104">成功したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6ccbd-1105">非パッシング (失敗、スキップされたなど) の数:263</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6ccbd-1106">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="6ccbd-1107">ビルド14955</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1107">Build 14955</span></span>

<span data-ttu-id="6ccbd-1108">ビルド14955の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1108">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1109">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1109">Fixed</span></span>

 - <span data-ttu-id="6ccbd-1110">Windows Subsystem for Linux では、コントロールを超える状況により、このビルドには更新プログラムがありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1110">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="6ccbd-1111">定期的にスケジュールされた更新は、次回のリリースで再開されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1111">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1112">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1112">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1113">成功したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1113">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6ccbd-1114">非パッシング (失敗、スキップされたなど) の数:263</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1114">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6ccbd-1115">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="6ccbd-1116">ビルド14951</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1116">Build 14951</span></span>

<span data-ttu-id="6ccbd-1117">ビルド14951の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1117">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="6ccbd-1118">新機能:Windows/Ubuntu の相互運用性</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1118">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="6ccbd-1119">Windows バイナリを WSL コマンドラインから直接呼び出すことができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1119">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="6ccbd-1120">これにより、ユーザーは Windows 環境とシステムを、不可能な方法で操作できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1120">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="6ccbd-1121">簡単な例として、ユーザーが次のコマンドを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1121">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="6ccbd-1122">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1122">More information can be found at:</span></span>

- [<span data-ttu-id="6ccbd-1123">相互運用のための WSL チームブログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1123">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="6ccbd-1124">MSDN Interop のドキュメント</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1124">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1125">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1125">Fixed</span></span>

- <span data-ttu-id="6ccbd-1126">Ubuntu 16.04 (Xenial) が、すべての新しい WSL インスタンスにインストールされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1126">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="6ccbd-1127">既存の 14.04 (Trusty) インスタンスを持つユーザーは自動的にアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1127">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="6ccbd-1128">インストール中に設定されたロケールが表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1128">Locale set during install is now displayed</span></span>
- <span data-ttu-id="6ccbd-1129">WSL プロセスをファイルにリダイレクトする場合のバグを含むターミナルの機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1129">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="6ccbd-1130">コンソールの有効期間は、bash の有効期間に関連付けられている必要があります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1130">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="6ccbd-1131">コンソールウィンドウのサイズは、バッファーサイズではなく表示サイズを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1131">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="6ccbd-1132">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1132">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1133">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1133">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1134">成功したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1134">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6ccbd-1135">非パッシング (失敗、スキップされたなど) の数:263</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1135">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6ccbd-1136">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1136">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="6ccbd-1137">ビルド14946</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1137">Build 14946</span></span>

<span data-ttu-id="6ccbd-1138">ビルド14946の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1138">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1139">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1139">Fixed</span></span>

- <span data-ttu-id="6ccbd-1140">スペースまたは引用符を含む NT ユーザー名を持つユーザーの WSL ユーザーアカウントを作成できない問題を修正しています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1140">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="6ccbd-1141">ディレクトリのリンク数が stat で0を返すように、VolFs と DrvFs を変更します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1141">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="6ccbd-1142">IPV6_MULTICAST_HOPS socket オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1142">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="6ccbd-1143">Tty ごとに1つのコンソール i/o ループに制限します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1143">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="6ccbd-1144">例: 次のコマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1144">Example: the following command is possible:</span></span>
  - <span data-ttu-id="6ccbd-1145">bash-c "echo data" |bash-c "ssh user@example.com " cat > foo .txt ""</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1145">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="6ccbd-1146">/proc/cpuinfo のタブでスペースを置換する (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1146">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="6ccbd-1147">Mountinfo に DrvFs が、マウントされた Windows ボリュームと一致する名前で表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1147">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="6ccbd-1148">/home と/root が mountinfo に正しい名前で表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1148">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="6ccbd-1149">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1149">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1150">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1150">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1151">成功したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1151">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6ccbd-1152">非パッシング (失敗、スキップされたなど) の数:263</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1152">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6ccbd-1153">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1153">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="6ccbd-1154">ビルド14942</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1154">Build 14942</span></span>

<span data-ttu-id="6ccbd-1155">ビルド14942の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/onefourninefourtwoooooo)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1155">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1156">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1156">Fixed</span></span>

- <span data-ttu-id="6ccbd-1157">SSH をブロックしていた "NOEXECUTE MEMORY の実行を試行しました" というネットワーククラッシュを含む、いくつかのバグを解決しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1157">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="6ccbd-1158">DrvFs の Windows アプリケーションから生成された通知の inotifiy サポートがになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1158">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="6ccbd-1159">TCP_KEEPIDLE と TCP_KEEPINTVL を mongod 用に実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1159">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="6ccbd-1160">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1160">(GH #695)</span></span>
- <span data-ttu-id="6ccbd-1161">Pivot_root システムコールを実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1161">Implement the pivot_root system call</span></span>
- <span data-ttu-id="6ccbd-1162">SO_DONTROUTE のソケットの実装オプション</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1162">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="6ccbd-1163">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1163">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1164">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1164">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1165">成功したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1165">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="6ccbd-1166">非パッシング (失敗、スキップされたなど) の数:263</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="6ccbd-1167">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1168">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1168">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1169">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1169">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1170">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1170">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="6ccbd-1171">ビルド14936</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1171">Build 14936</span></span>

<span data-ttu-id="6ccbd-1172">ビルド14936の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1172">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="6ccbd-1173">注:WSL は、今後のリリースで Ubuntu 14.04 (Trusty) ではなく、Ubuntu バージョン 16.04 (Xenial) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1173">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="6ccbd-1174">この変更は、新しいインスタンスをインストールする場合に適用されます (lxrun/install または bash の最初の実行)。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1174">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="6ccbd-1175">Trusty を使用した既存のインスタンスは自動的にはアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1175">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="6ccbd-1176">ユーザーは、Trusty コマンドを使用して、自分のイメージを Xenial にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1176">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="6ccbd-1177">既知の問題</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1177">Known Issue</span></span>
<span data-ttu-id="6ccbd-1178">WSL でいくつかのソケット実装に問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1178">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="6ccbd-1179">"NOEXECUTE MEMORY の実行を試行しました" というエラーが発生すると、バグチェックはクラッシュします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1179">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="6ccbd-1180">この問題の最も一般的な取り組みは、ssh を使用する場合のクラッシュです。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1180">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="6ccbd-1181">根本原因は内部ビルドで固定されており、最も早い機会に Insider にプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1181">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1182">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1182">Fixed</span></span>

- <span data-ttu-id="6ccbd-1183">Chroot システム呼び出しを実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1183">Implemented the chroot system call</span></span>
- <span data-ttu-id="6ccbd-1184">~~DrvFs の Windows アプリケーションから生成された通知のサポートを含む~~inotify の機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1184">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="6ccbd-1185">量現時点では利用できない Windows アプリケーションからの変更については、Inotify のサポートが提供されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1185">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="6ccbd-1186">IPV6 へのソケットバインド:<port n> : で IPV6_V6ONLY (GH #68、#157、#393、#460、#674、#740、#982、#996) がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1186">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="6ccbd-1187">Waitid systemcall が実装された WNOWAIT 動作 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1187">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="6ccbd-1188">IP ソケットオプション IP_HDRINCL と IP_TTL のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1188">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="6ccbd-1189">長さ0の読み取り () はすぐに返される必要があります (GH #975)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1189">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="6ccbd-1190">Tar ファイルに NULL 終端文字を含まないファイル名とファイル名プレフィックスを正しく処理します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1190">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="6ccbd-1191">/dev/null の epoll サポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1191">epoll support for /dev/null</span></span>
- <span data-ttu-id="6ccbd-1192">更新プログラムのタイムソースを修正する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1192">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="6ccbd-1193">Bash-c がファイルにリダイレクトできるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1193">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="6ccbd-1194">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1194">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1195">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1195">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1196">成功したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1196">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="6ccbd-1197">非パッシング (失敗、スキップされたなど) の数:264</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1197">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="6ccbd-1198">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1198">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1199">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1199">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1200">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1200">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1201">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1201">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="6ccbd-1202">ビルド14931</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1202">Build 14931</span></span>

<span data-ttu-id="6ccbd-1203">ビルド14931の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1203">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1204">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1204">Fixed</span></span>

 - <span data-ttu-id="6ccbd-1205">Windows Subsystem for Linux では、コントロールを超える状況により、このビルドには更新プログラムがありません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1205">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="6ccbd-1206">定期的にスケジュールされた更新は、次のリリースで再開されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1206">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="6ccbd-1207">ビルド14926</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1207">Build 14926</span></span>

<span data-ttu-id="6ccbd-1208">ビルド14926の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1208">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1209">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1209">Fixed</span></span>

- <span data-ttu-id="6ccbd-1210">管理者特権を持たないコンソールで Ping が機能するようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1210">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="6ccbd-1211">Ping6 がサポートされるようになりました。管理者特権も必要ありません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1211">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="6ccbd-1212">WSL によって変更されたファイルの Inotify サポート。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1212">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="6ccbd-1213">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1213">(GH #216)</span></span>
  - <span data-ttu-id="6ccbd-1214">サポートされているフラグ:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1214">Flags supported:</span></span>
    - <span data-ttu-id="6ccbd-1215">inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="6ccbd-1216">inotify_add_watch イベント:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1216">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="6ccbd-1217">inotify_add_watch 属性 (i):LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1217">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="6ccbd-1218">出力の読み取り:LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1218">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="6ccbd-1219">既知の問題:Windows アプリケーションからファイルを変更してもイベントが生成されない</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1219">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="6ccbd-1220">Unix ソケットで SCM_CREDENTIALS がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1220">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="6ccbd-1221">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1221">LTP Results:</span></span>
<span data-ttu-id="6ccbd-1222">成功したテストの数:651</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1222">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="6ccbd-1223">非パッシング (失敗、スキップされたなど) の数:258</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1223">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="6ccbd-1224">LTP テストの実行ログ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1224">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="6ccbd-1225">ビルド14915</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1225">Build 14915</span></span>

<span data-ttu-id="6ccbd-1226">ビルド14915の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1226">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1227">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1227">Fixed</span></span>
-  <span data-ttu-id="6ccbd-1228">Unix データグラムソケットの socketpair (GH #262)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1228">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="6ccbd-1229">SO_REUSEADDR の Unix ソケットサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1229">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="6ccbd-1230">SO_BROADCAST の UNIX ソケットサポート (GH #568)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1230">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="6ccbd-1231">SOCK_SEQPACKET の Unix ソケットサポート (GH #758、#546)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1231">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="6ccbd-1232">Unix データグラムソケットの送信、受信、およびシャットダウンのサポートの追加</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1232">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="6ccbd-1233">非固定アドレスに対する mmap パラメーターの検証が無効なため、バグチェックを修正します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1233">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="6ccbd-1234">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1234">(GH #847)</span></span>
- <span data-ttu-id="6ccbd-1235">ターミナル状態の中断/再開のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1235">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="6ccbd-1236">画面ユーティリティのブロックを解除する TIOCPKT ioctl のサポート (GH #774)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1236">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="6ccbd-1237">既知の問題:関数キーが動作していません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1237">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="6ccbd-1238">TimerFd の競合を修正しました。これにより、解放されたメンバー ' ReaderReady ' が Lxp Timerfdworkspace Erroutine (GH #814) によってアクセスされる可能性があります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1238">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="6ccbd-1239">Futex、投票、clock_nanosleep の再起動可能なシステムコールのサポートを有効にする</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1239">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="6ccbd-1240">バインドマウントサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1240">Added bind mount support</span></span>
- <span data-ttu-id="6ccbd-1241">マウントの名前空間のサポートの共有を解除する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1241">unshare for mount namespace support</span></span>
    - <span data-ttu-id="6ccbd-1242">既知の問題:現在の作業ディレクトリを使用し`unshare(CLONE_NEWNS)`て新しいマウント名前空間を作成すると、引き続き古い名前空間が参照されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1242">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="6ccbd-1243">追加の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1243">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="6ccbd-1244">ビルド14905</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1244">Build 14905</span></span>

<span data-ttu-id="6ccbd-1245">ビルド14905の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1245">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1246">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1246">Fixed</span></span>
- <span data-ttu-id="6ccbd-1247">再開可能なシステムコールがサポートされるようになりました (GH #349、GH #520)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1247">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="6ccbd-1248">現在操作中のディレクトリへのシンボリックリンク (GH #650)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1248">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="6ccbd-1249">/Dev/random の RNDGETENTCNT ioctl を実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1249">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="6ccbd-1250">/Proc/[pid]/マウント,/proc/[pid]/mountinfo および/proc/[pid]/mountstats ファイルを実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1250">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="6ccbd-1251">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1251">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="6ccbd-1252">ビルド14901</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1252">Build 14901</span></span>
<span data-ttu-id="6ccbd-1253">Windows 10 記念日更新リリースの最初の Insider ビルド。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1253">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="6ccbd-1254">ビルド14901の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1254">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1255">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1255">Fixed</span></span>
- <span data-ttu-id="6ccbd-1256">末尾のスラッシュの問題を修正した</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1256">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="6ccbd-1257">などのコマンドが動作するようになりました`$ mv a/c/ a/b/`</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1257">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="6ccbd-1258">Ubuntu ロケールを Windows ロケールに設定するかどうかを確認するメッセージが表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1258">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="6ccbd-1259">Ns フォルダーの Procfs サポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1259">Procfs support for ns folder</span></span>
- <span data-ttu-id="6ccbd-1260">Tmpfs、procfs、および sysfs ファイルシステムのマウントとマウント解除を追加しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1260">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="6ccbd-1261">Mknod [at] 32 ビット ABI 署名の修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1261">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="6ccbd-1262">Unix ソケットをディスパッチモデルに移行</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1262">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="6ccbd-1263">Setsockopt を使用して、INET ソケットの recv バッファーサイズを設定する必要があります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1263">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="6ccbd-1264">MSG_CMSG_CLOEXEC unix socket receive message フラグを実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1264">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="6ccbd-1265">Linux プロセス stdin/stdout パイプのリダイレクト (GH #2)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1265">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="6ccbd-1266">CMD で bash-c コマンドのパイプを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1266">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="6ccbd-1267">例: > dir |bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1267">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="6ccbd-1268">Bash を複数のシステムにインストールできるようになりました (GH #538、#358)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1268">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="6ccbd-1269">既定の INET ソケットバッファーサイズは、既定の Ubuntu セットアップのものと一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1269">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="6ccbd-1270">Xattr syscall を listxattr に揃える</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1270">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="6ccbd-1271">SIOCGIFCONF から有効な IPv4 アドレスを持つインターフェイスのみを返す</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1271">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="6ccbd-1272">Ptrace によって挿入されるときのシグナルの既定の動作を修正する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1272">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="6ccbd-1273">/proc/sys/vm/min_free_kbytes を実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1273">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="6ccbd-1274">Sigreturn でコンテキストを復元するときにマシンコンテキストレジスタの値を使用する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1274">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="6ccbd-1275">これにより、一部のユーザーに対して java と javac がハングした問題が解決されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1275">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="6ccbd-1276">/Proc/sys/kernel/hostname を実装する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1276">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1277">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1277">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1278">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1278">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1279">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1279">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="6ccbd-1280">14388を Windows 10 記念日更新プログラムにビルドする</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1280">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="6ccbd-1281">ビルド14388の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/14388wip)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1281">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1282">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1282">Fixed</span></span>
- <span data-ttu-id="6ccbd-1283">8/2 で Windows 10 記念日更新プログラムを準備するための修正プログラム</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1283">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="6ccbd-1284">記念日の更新に関する詳細については、こちらの[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1284">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="6ccbd-1285">ビルド14376</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1285">Build 14376</span></span>
<span data-ttu-id="6ccbd-1286">ビルド14376の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1286">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1287">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1287">Fixed</span></span>
- <span data-ttu-id="6ccbd-1288">Apt-get がハングするインスタンスをいくつか削除しました (GH #493)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1288">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="6ccbd-1289">空のマウントが正しく処理されない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1289">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="6ccbd-1290">Ramdisks が正しくマウントされていない問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1290">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="6ccbd-1291">Unix ソケットの受け入れをサポートフラグに変更する (partial GH #451)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1291">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="6ccbd-1292">一般的なネットワーク関連のブルースクリーンを修正した</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1292">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="6ccbd-1293">/Proc/[pid]/task (GH #523) にアクセスするときにブルースクリーンを修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1293">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="6ccbd-1294">一部の pty シナリオ (GH #488、#504) の高 CPU 使用率を修正した</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1294">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="6ccbd-1295">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1295">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="6ccbd-1296">ビルド14371</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1296">Build 14371</span></span>
<span data-ttu-id="6ccbd-1297">ビルド14371の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1297">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1298">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1298">Fixed</span></span>
- <span data-ttu-id="6ccbd-1299">Ptrace を使用するときに SIGCHLD と wait () を使用してタイミングレースを修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1299">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="6ccbd-1300">パスの末尾に/(GH #432) がある場合の動作を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1300">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="6ccbd-1301">子へのハンドルが開いているため、名前の変更とリンク解除に失敗する問題を修正した</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1301">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="6ccbd-1302">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1302">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="6ccbd-1303">ビルド14366</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1303">Build 14366</span></span>
<span data-ttu-id="6ccbd-1304">ビルド14366の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1304">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1305">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1305">Fixed</span></span>
- <span data-ttu-id="6ccbd-1306">シンボリックリンクを使用したファイル作成時の修正</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1306">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="6ccbd-1307">Python 用 listxattr (GH 385) が追加されました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1307">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="6ccbd-1308">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1308">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1309">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1309">Syscall Support</span></span>
-   <span data-ttu-id="6ccbd-1310">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1310">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1311">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1311">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="6ccbd-1312">ビルド14361</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1312">Build 14361</span></span>
<span data-ttu-id="6ccbd-1313">ビルド14361の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14361)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1313">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1314">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1314">Fixed</span></span>
- <span data-ttu-id="6ccbd-1315">Windows 上で Bash on Ubuntu を実行すると、DrvFs の大文字と小文字が区別されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1315">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="6ccbd-1316">ユーザーは .txt と大文字小文字を区別することができます。/Mnt/c ドライブ上の TXT</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1316">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="6ccbd-1317">大文字小文字の区別は、Bash on Ubuntu on Windows でのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1317">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="6ccbd-1318">Bash の外部では、ファイルが正しく報告されますが、予期しない動作が Windows からのファイルの操作で発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1318">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="6ccbd-1319">各ボリュームのルート (つまり/mnt/c) は大文字と小文字が区別されません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1319">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="6ccbd-1320">これらのファイルを Windows で処理する方法の詳細については、[こちら](https://support.microsoft.com/en-us/kb/100625)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1320">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="6ccbd-1321">Pty/tty のサポートが大幅に強化されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1321">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="6ccbd-1322">TMUX のようなアプリケーションがサポートされるようになりました (GH #40)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1322">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="6ccbd-1323">ユーザーアカウントが常に作成されていないインストールの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1323">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="6ccbd-1324">非常に長い引数リストを許可する最適化されたコマンドライン arg 構造体。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1324">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="6ccbd-1325">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1325">(GH #153)</span></span>
- <span data-ttu-id="6ccbd-1326">DrvFs からファイルを削除することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1326">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="6ccbd-1327">切断時にターミナルがハングする一部のインスタンスを修正した (GH #43)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1327">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="6ccbd-1328">chmod と chown が tty デバイスで動作するようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1328">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="6ccbd-1329">0\.0.0.0 および:: as localhost (GH #388) への接続を許可します</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1329">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="6ccbd-1330">Sendmsg/recvmsg が > 1 (partial GH #376) の IO ベクターの長さを処理するようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1330">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="6ccbd-1331">ユーザーは、自動生成された hosts ファイル (GH #398) をオプトアウトできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1331">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="6ccbd-1332">インストール中に Linux ロケールを NT ロケールに自動的に一致させる (GH #11)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1332">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="6ccbd-1333">/Proc/sys/vm/swappiness ファイル (GH #306) が追加されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1333">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="6ccbd-1334">strace が正常に終了するようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1334">strace now exits correctly</span></span>
- <span data-ttu-id="6ccbd-1335">/Proc/self/fd を使用してパイプを再度開くことを許可する (GH #222)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1335">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="6ccbd-1336">DrvFs から%LOCALAPPDATA%\lxss の下にあるディレクトリを非表示にする (GH #270)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1336">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="6ccbd-1337">Bash の処理の強化 ~.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1337">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="6ccbd-1338">などのコマンド"bash ~-c %.ls"(GH #467) をサポートするようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1338">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="6ccbd-1339">ソケットはシャットダウン中に使用可能な epoll read を通知するようになりました (GH #271)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1339">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="6ccbd-1340">lxrun/uninstall では、ファイルとフォルダーを削除する機能が改善されています。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1340">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="6ccbd-1341">修正された ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1341">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="6ccbd-1342">XEmacs (GH #481) などの x11 アプリのサポートの強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1342">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="6ccbd-1343">既定の Ubuntu 設定に一致するように初期スレッドスタックサイズを更新し、get_rlimit syscall (GH #172、#258) にサイズを正しく報告しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1343">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="6ccbd-1344">Pico プロセスのイメージ名 (監査のためなど) のレポートが改善されました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1344">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="6ccbd-1345">Df コマンドの/proc/mountinfo を実装します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1345">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="6ccbd-1346">子名のシンボリックリンクエラーコードを修正した。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1346">Fixed symlink error code for child name .</span></span> <span data-ttu-id="6ccbd-1347">そして。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1347">and ..</span></span>
- <span data-ttu-id="6ccbd-1348">追加の改善バグ修正と改善</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1348">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1349">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1349">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1350">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1351">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="6ccbd-1352">ビルド14352</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1352">Build 14352</span></span>
<span data-ttu-id="6ccbd-1353">ビルド14352の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14352)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1353">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1354">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1354">Fixed</span></span>
- <span data-ttu-id="6ccbd-1355">大きなファイルが正しくダウンロードまたは作成されなかった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1355">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="6ccbd-1356">これにより、npm とその他のシナリオ (GH #3、GH #313) のブロックが解除されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1356">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="6ccbd-1357">ソケットがハングする一部のインスタンスを削除しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1357">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="6ccbd-1358">いくつかの ptrace エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1358">Corrected some ptrace errors</span></span>
- <span data-ttu-id="6ccbd-1359">255文字を超えるファイル名を許可する WSL の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1359">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="6ccbd-1360">英語以外の文字のサポートの強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1360">Improved support for non-English characters</span></span>
- <span data-ttu-id="6ccbd-1361">現在の Windows タイムゾーンデータを追加し、既定として設定する</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1361">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="6ccbd-1362">各マウントポイントの一意のデバイス id (jre fix – GH #49)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1362">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="6ccbd-1363">"." を含むパスの問題を修正してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1363">Correct issue with paths containing “.”</span></span> <span data-ttu-id="6ccbd-1364">および "."</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1364">and “..”</span></span>
- <span data-ttu-id="6ccbd-1365">追加された Fifo サポート (GH #71)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1365">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="6ccbd-1366">ネイティブ Ubuntu 形式に一致するように resolv.conf の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1366">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="6ccbd-1367">一部の procfs クリーンアップ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1367">Some procfs cleanup</span></span>
- <span data-ttu-id="6ccbd-1368">管理者コンソールの ping を有効にする (GH #18)</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1368">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1369">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1369">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1370">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1371">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="6ccbd-1372">ビルド14342</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1372">Build 14342</span></span>
<span data-ttu-id="6ccbd-1373">ビルド14342の一般的な Windows 情報については、 [Windows ブログ](https://aka.ms/wip14342)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1373">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="6ccbd-1374">VolFs とドライブ Fs に関する情報は、 [Wsl ブログ](https://blogs.msdn.microsoft.com/wsl)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1374">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1375">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1375">Fixed</span></span>
- <span data-ttu-id="6ccbd-1376">Windows ユーザーのユーザー名に Unicode 文字が含まれている場合のインストールの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1376">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="6ccbd-1377">FAQ の apt get 更新 udev の回避策は、最初の実行時に既定で提供されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1377">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="6ccbd-1378">ドライブ fs (/mnt/<drive>) ディレクトリでのシンボリックリンクの有効化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1378">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="6ccbd-1379">シンボリックリンクがドライブ Fs と VolFs 間で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1379">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="6ccbd-1380">解析の問題、アドレス指定された最上位レベル パス: %.ls/期待どおりに、正しく動作/。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1380">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="6ccbd-1381">npm がドライブ Fs にインストールされ、-g オプションが機能するようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1381">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="6ccbd-1382">PHP サーバーの起動を妨げている問題を修正した</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1382">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="6ccbd-1383">ネイティブ Ubuntu に近い $PATH など、既定の環境値が更新されました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1383">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="6ccbd-1384">Apt パッケージキャッシュを更新するための週単位のメンテナンスタスクが Windows に追加されました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1384">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="6ccbd-1385">ELF ヘッダーの検証に関する問題を修正しました。 WSL ですべての Melkor オプションがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1385">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="6ccbd-1386">Zsh シェルが機能しています</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1386">Zsh shell is functional</span></span>
- <span data-ttu-id="6ccbd-1387">プリコンパイル済みのジャンプバイナリがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1387">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="6ccbd-1388">Bash の初回実行時のプロンプトが正しくローカライズされるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1388">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="6ccbd-1389">/proc/meminfo が正しい情報を返すようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1389">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="6ccbd-1390">VFS でソケットがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1390">Sockets now supported in VFS</span></span>
- <span data-ttu-id="6ccbd-1391">/dev が tempfs としてマウントされるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1391">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="6ccbd-1392">Fifo がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1392">Fifo now supported</span></span>
- <span data-ttu-id="6ccbd-1393">/Proc/cpuinfo で、マルチコアシステムが正しく表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1393">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="6ccbd-1394">初回実行時の追加の改善とエラーメッセージのダウンロード</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1394">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="6ccbd-1395">Syscall の機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1395">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="6ccbd-1396">以下のサポートされている syscall 一覧。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1396">Supported syscall list below.</span></span>
- <span data-ttu-id="6ccbd-1397">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1397">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="6ccbd-1398">既知の問題</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1398">Known Issues</span></span>
- <span data-ttu-id="6ccbd-1399">'. ' を解決できません</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1399">Not resolving ‘..’</span></span> <span data-ttu-id="6ccbd-1400">場合によっては、ドライブ Fs で正しく動作します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1400">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1401">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1401">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1402">次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1402">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1403">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1403">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="6ccbd-1404">ビルド14332</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1404">Build 14332</span></span>

<span data-ttu-id="6ccbd-1405">ビルド14332の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14332)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1405">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="6ccbd-1406">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1406">Fixed</span></span>
- <span data-ttu-id="6ccbd-1407">DNS エントリの優先順位を含む resolv.conf の生成の向上</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1407">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="6ccbd-1408">/Mnt ドライブと/mnt 以外のドライブの間でファイルとディレクトリを移動する場合の問題</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1408">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="6ccbd-1409">シンボリックリンクを使用して Tar ファイルを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1409">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="6ccbd-1410">インスタンスの作成時に既定の/run/lock ディレクトリが追加されました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1410">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="6ccbd-1411">/Dev/null を更新して適切な stat 情報を返す</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1411">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="6ccbd-1412">初回実行時のダウンロード時の追加エラー</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1412">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="6ccbd-1413">Syscall の機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1413">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="6ccbd-1414">以下のサポートされている syscall 一覧。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1414">Supported syscall list below.</span></span>
- <span data-ttu-id="6ccbd-1415">追加の改善バグ修正と改善</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1415">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1416">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1416">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1417">以下は、WSL で実装がいくつかある新しい syscall です。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1417">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="6ccbd-1418">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1418">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="6ccbd-1419">ビルド14328</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1419">Build 14328</span></span>

<span data-ttu-id="6ccbd-1420">ビルド14332の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14328)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1420">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="6ccbd-1421">新機能</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1421">New Features</span></span>
* <span data-ttu-id="6ccbd-1422">Linux ユーザーがサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1422">Now support Linux users.</span></span>  <span data-ttu-id="6ccbd-1423">Bash on Ubuntu on Windows をインストールすると、Linux ユーザーの作成を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1423">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="6ccbd-1424">詳細については、「」を参照してください。 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1424">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="6ccbd-1425">ホスト名が Windows コンピューター名に設定されました@localhost</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1425">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="6ccbd-1426">ビルド14328の詳細については、次を参照してください。 https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1426">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="6ccbd-1427">固定</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1427">Fixed</span></span>
* <span data-ttu-id="6ccbd-1428">非/mnt/<drive>ファイルのシンボリックリンクの機能強化</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1428">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="6ccbd-1429">npm のインストールが機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1429">npm install now works</span></span>
    * <span data-ttu-id="6ccbd-1430">jdk/jre[はここ](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)に記載されている手順に従ってインストールできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1430">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="6ccbd-1431">既知の問題: symlink は Windows マウントでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1431">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="6ccbd-1432">機能は、後のビルドで使用できるようになります</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1432">Functionality will be available in a later build</span></span>
* <span data-ttu-id="6ccbd-1433">上部と htop が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1433">top and htop now display</span></span>
* <span data-ttu-id="6ccbd-1434">一部のインストールエラーに関する追加のエラーメッセージ</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1434">Additional error messages for some install failures</span></span>
* <span data-ttu-id="6ccbd-1435">Syscall の機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1435">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="6ccbd-1436">以下のサポートされている syscall 一覧。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1436">Supported syscall list below.</span></span>
* <span data-ttu-id="6ccbd-1437">追加の改善バグ修正と改善</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1437">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="6ccbd-1438">Syscall のサポート</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1438">Syscall Support</span></span>
<span data-ttu-id="6ccbd-1439">WSL で実装がいくつかある syscall の一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1439">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="6ccbd-1440">この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ccbd-1440">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
