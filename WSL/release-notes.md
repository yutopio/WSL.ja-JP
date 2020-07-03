---
title: Windows Subsystem for Linux のリリース ノート
description: Windows Subsystem for Linux のリリース ノート。  毎週更新されます。
keywords: リリース ノート, wsl, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu
author: benhillis
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 2fcf24719f037a29bab7652fc75ac82cc0b6176a
ms.sourcegitcommit: 031a74801e03a90aed4b34c4fd5bfe964fc30994
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2020
ms.locfileid: "84942596"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="fc430-105">Windows Subsystem for Linux のリリース ノート</span><span class="sxs-lookup"><span data-stu-id="fc430-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-20150"></a><span data-ttu-id="fc430-106">ビルド 20150</span><span class="sxs-lookup"><span data-stu-id="fc430-106">Build 20150</span></span>
<span data-ttu-id="fc430-107">ビルド 20150 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-107">For general Windows information on build 20150 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span></span>

* <span data-ttu-id="fc430-108">WSL2 GPU コンピューティングの場合、詳しくは、[Windows ブログ](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-108">WSL2 GPU compute see [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/) for more information.</span></span>
* <span data-ttu-id="fc430-109">WSL を簡単に設定できるように wsl.exe --install コマンド ライン オプションを導入します。</span><span class="sxs-lookup"><span data-stu-id="fc430-109">Introduce wsl.exe --install command line option to easily set up WSL.</span></span>
* <span data-ttu-id="fc430-110">WSL2 カーネルへの更新を管理するための wsl.exe --update コマンド ライン オプションを導入します。</span><span class="sxs-lookup"><span data-stu-id="fc430-110">Introduce wsl.exe --update command line option to manage updates to the WSL2 kernel.</span></span> 
* <span data-ttu-id="fc430-111">WSL2 を既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="fc430-111">Set WSL2 as the default.</span></span>
* <span data-ttu-id="fc430-112">WSL2 vm の正常なシャットダウン タイムアウトを増やします。</span><span class="sxs-lookup"><span data-stu-id="fc430-112">Increase WSL2 vm graceful shutdown timeout.</span></span>
* <span data-ttu-id="fc430-113">デバイス メモリをマッピングするときの virtio-9p 競合状態を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-113">Fix virtio-9p race condition when mapping device memory.</span></span>
* <span data-ttu-id="fc430-114">UAC が無効になっている場合は、昇格された 9p サーバーを実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="fc430-114">Don't run an elevated 9p server if UAC is disabled.</span></span>

## <a name="build-19640"></a><span data-ttu-id="fc430-115">ビルド 19640</span><span class="sxs-lookup"><span data-stu-id="fc430-115">Build 19640</span></span>
<span data-ttu-id="fc430-116">ビルド 19640 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-116">For general Windows information on build 19640 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span></span>

* <span data-ttu-id="fc430-117">[WSL2] virtio-9p (drvfs) の安定性が向上しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-117">[WSL2] Stability improvements for virtio-9p (drvfs).</span></span>

## <a name="build-19555"></a><span data-ttu-id="fc430-118">ビルド 19555</span><span class="sxs-lookup"><span data-stu-id="fc430-118">Build 19555</span></span>
<span data-ttu-id="fc430-119">ビルド 19555 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-119">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="fc430-120">[WSL2] インストールおよび変換の操作によって使用されるメモリの量を制限するには、メモリ cgroup を使用します [GH 4669]</span><span class="sxs-lookup"><span data-stu-id="fc430-120">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="fc430-121">機能の検出機能を向上させるため、Linux 用 Windows サブシステムのオプションのコンポーネントが有効になっていない場合 wsl.exe を使用します</span><span class="sxs-lookup"><span data-stu-id="fc430-121">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="fc430-122">WSL のオプションのコンポーネントがインストールされていない場合、wsl.exe を変更してヘルプ テキストを出力します</span><span class="sxs-lookup"><span data-stu-id="fc430-122">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="fc430-123">インスタンス作成時の競合状態を修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-123">Fix race condition when creating instances</span></span>
* <span data-ttu-id="fc430-124">すべてのコマンド ライン機能を含む wslclient.dll を作成します</span><span class="sxs-lookup"><span data-stu-id="fc430-124">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="fc430-125">LxssManagerUser サービスの停止中にクラッシュしないようにします</span><span class="sxs-lookup"><span data-stu-id="fc430-125">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="fc430-126">distroName パラメーターが NULL の場合に wslapi.dll ファスト フェールを修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-126">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="fc430-127">ビルド 19041</span><span class="sxs-lookup"><span data-stu-id="fc430-127">Build 19041</span></span>
<span data-ttu-id="fc430-128">ビルド 19041 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-128">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="fc430-129">[WSL2] プロセスを起動する前にシグナル マスクをクリアします</span><span class="sxs-lookup"><span data-stu-id="fc430-129">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="fc430-130">[WSL2] Linux カーネルを 4.19.84 に更新します</span><span class="sxs-lookup"><span data-stu-id="fc430-130">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="fc430-131">symlink が非相対である場合に /etc/resolv.conf symlink の作成を処理します</span><span class="sxs-lookup"><span data-stu-id="fc430-131">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="fc430-132">ビルド 19028</span><span class="sxs-lookup"><span data-stu-id="fc430-132">Build 19028</span></span>
<span data-ttu-id="fc430-133">ビルド 19028 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-133">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="fc430-134">[WSL2] Linux カーネルを 4.19.81 に更新します</span><span class="sxs-lookup"><span data-stu-id="fc430-134">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="fc430-135">[WSL2] /dev/net/tun to 0666 の既定のアクセス許可を変更します [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="fc430-135">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="fc430-136">[WSL2] Linux VM に割り当てられた既定のメモリ容量を、ホスト メモリの80% に調整します</span><span class="sxs-lookup"><span data-stu-id="fc430-136">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="fc430-137">[WSL2] タイムアウトがある要求を処理するように相互運用サーバーを修正し、不適切な呼び出し元がサーバーを切断できないようにします</span><span class="sxs-lookup"><span data-stu-id="fc430-137">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="fc430-138">ビルド 19018</span><span class="sxs-lookup"><span data-stu-id="fc430-138">Build 19018</span></span>
<span data-ttu-id="fc430-139">ビルド 19018 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-139">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="fc430-140">[WSL2] 9p マウントの既定値として cache=mmap を使用して dotnet アプリを修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-140">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="fc430-141">[WSL2] localhost リレーの修正プログラム [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="fc430-141">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="fc430-142">[WSL2] ディストリビューション間で状態を共有するためにクロスディストリビューション共有の tmpfs マウントを導入</span><span class="sxs-lookup"><span data-stu-id="fc430-142">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="fc430-143">\\\\wsl$ の永続ネットワーク ドライブを復元する修正</span><span class="sxs-lookup"><span data-stu-id="fc430-143">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="fc430-144">ビルド 19013</span><span class="sxs-lookup"><span data-stu-id="fc430-144">Build 19013</span></span>
<span data-ttu-id="fc430-145">ビルド 19013 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-145">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="fc430-146">[WSL2] WSL ユーティリティ VM のメモリ パフォーマンスを向上します。</span><span class="sxs-lookup"><span data-stu-id="fc430-146">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="fc430-147">使用されなくなったメモリは解放されてホストに戻されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-147">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="fc430-148">[WSL2] カーネル バージョンを 4.19.79 に更新します。</span><span class="sxs-lookup"><span data-stu-id="fc430-148">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="fc430-149">(CONFIG_HIGH_RES_TIMERS、CONFIG_TASK_XACCT、CONFIG_TASK_IO_ACCOUNTING、CONFIG_SCHED_HRTICK、CONFIG_BRIDGE_VLAN_FILTERING を追加)。</span><span class="sxs-lookup"><span data-stu-id="fc430-149">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="fc430-150">[WSL2] stdin が閉じていないパイプ ハンドルであるケースに対処するために入力リレーを修正します [GH 4424]</span><span class="sxs-lookup"><span data-stu-id="fc430-150">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="fc430-151">\\\\wsl$ 大文字と小文字を区別しないかどうかの確認を行います。</span><span class="sxs-lookup"><span data-stu-id="fc430-151">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="fc430-152">ビルド 19002</span><span class="sxs-lookup"><span data-stu-id="fc430-152">Build 19002</span></span>
<span data-ttu-id="fc430-153">ビルド 19002 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-153">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="fc430-154">[WSL] 一部の Unicode 文字の処理に関する問題を修正します: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="fc430-154">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="fc430-155">[WSL] ビルド間のアップグレードの直後に起動すると、まれにディストリビューションが登録解除されるケースを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-155">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="fc430-156">[WSL] インスタンスのアイドル タイマーがキャンセルされない場合にシャットダウンする wsl.exe の問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-156">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="fc430-157">ビルド 18995</span><span class="sxs-lookup"><span data-stu-id="fc430-157">Build 18995</span></span>
<span data-ttu-id="fc430-158">ビルド 18995 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-158">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="fc430-159">[WSL2] 操作が中断された後に DrvFs マウントの動作が停止する問題を修正します (例: ctrl-c) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="fc430-159">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="fc430-160">[WSL2] hvsocket メッセージが非常に多い場合の処理を修正します [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="fc430-160">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="fc430-161">[WSL2] stdin がファイルの場合の相互運用に関する問題を修正します [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="fc430-161">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="fc430-162">[WSL2] 予期しないネットワークの状態が検出されたときにサービスがクラッシュする問題を修正します [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="fc430-162">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="fc430-163">[WSL2] 現在のプロセスに環境変数がない場合は、相互運用サーバーからディストリビューションの名前を照会します</span><span class="sxs-lookup"><span data-stu-id="fc430-163">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="fc430-164">[WSL2] stdin がファイルの場合の相互運用に関する問題を修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-164">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="fc430-165">[WSL2] Linux カーネル バージョンを 4.19.72 に更新します</span><span class="sxs-lookup"><span data-stu-id="fc430-165">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="fc430-166">[WSL2] .wslconfig を使用して追加のカーネル コマンド ライン パラメーターを指定する機能を追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-166">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="fc430-167">ビルド 18990</span><span class="sxs-lookup"><span data-stu-id="fc430-167">Build 18990</span></span>
<span data-ttu-id="fc430-168">ビルド 18990 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-168">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="fc430-169">\\\\wsl$ のディレクトリの一覧のパフォーマンスを向上します</span><span class="sxs-lookup"><span data-stu-id="fc430-169">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="fc430-170">[WSL2] 追加のブート エントロピーを挿入します [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="fc430-170">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="fc430-171">[WSL2] su または sudo を使用する場合の Windows の相互運用を修正します [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="fc430-171">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="fc430-172">ビルド 18980</span><span class="sxs-lookup"><span data-stu-id="fc430-172">Build 18980</span></span>
<span data-ttu-id="fc430-173">ビルド 18980 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-173">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="fc430-174">FILE_READ_DATA を拒否するシンボリック リンクの読み取りを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-174">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="fc430-175">これには、"C:\Document and Settings" など、下位互換性のために Windows が作成するすべてのシンボリック リンクや、ユーザー プロファイル ディレクトリ内の一連のシンボリック リンクが含まれます</span><span class="sxs-lookup"><span data-stu-id="fc430-175">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="fc430-176">予期しないファイル システム状態を致命的ではないものとします [GH 4334、4305]</span><span class="sxs-lookup"><span data-stu-id="fc430-176">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="fc430-177">[WSL2] CPU/ファームウェアで仮想化がサポートされている場合に、arm64 のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-177">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="fc430-178">[WSL2] 特権のないユーザーがカーネル ログを表示することを許可します</span><span class="sxs-lookup"><span data-stu-id="fc430-178">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="fc430-179">[WSL2] stdout/stderr のソケットが閉じられているときの出力リレーを修正します [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="fc430-179">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="fc430-180">[WSL2] バッテリーおよび AC アダプターのパススルーをサポートします</span><span class="sxs-lookup"><span data-stu-id="fc430-180">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="fc430-181">[WSL2] Linux カーネルを 4.19.67 に更新します</span><span class="sxs-lookup"><span data-stu-id="fc430-181">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="fc430-182">/Etc/wsl.conf に既定のユーザー名を設定する機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-182">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="fc430-183">ビルド 18975</span><span class="sxs-lookup"><span data-stu-id="fc430-183">Build 18975</span></span>
<span data-ttu-id="fc430-184">ビルド 18975 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-184">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="fc430-185">[WSL2] 複数の localhost の信頼性に関する問題を修正しました [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="fc430-185">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="fc430-186">ビルド 18970</span><span class="sxs-lookup"><span data-stu-id="fc430-186">Build 18970</span></span>
<span data-ttu-id="fc430-187">ビルド 18970 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-187">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="fc430-188">[WSL2] システムがスリープ状態から再開するときにホスト時刻と時刻を同期します [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="fc430-188">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="fc430-189">[WSL2] 可能な場合、Windows ボリュームに NT シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="fc430-189">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="fc430-190">[WSL2] UTS、IPC、PID、および Mount の各名前空間にディストリビューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="fc430-190">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="fc430-191">[WSL2] サーバーが localhost に直接バインドするときの localhost ポート リレーを修正します [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="fc430-191">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="fc430-192">[WSL2] 出力がリダイレクトされるときの相互運用を修正します [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="fc430-192">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="fc430-193">[WSL2] 絶対 NT シンボリック リンクの変換をサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc430-193">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="fc430-194">[WSL2] カーネルを 4.19.59 に更新します</span><span class="sxs-lookup"><span data-stu-id="fc430-194">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="fc430-195">[WSL2] eth0 のサブネット マスクを正しく設定します。</span><span class="sxs-lookup"><span data-stu-id="fc430-195">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="fc430-196">[WSL2] 終了イベントが通知されたときにコンソール ワーカー ループから抜け出すようにロジックを変更します。</span><span class="sxs-lookup"><span data-stu-id="fc430-196">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="fc430-197">[WSL2] ディストリビューションが実行されていないときに、ディストリビューション VHD を取り出します。</span><span class="sxs-lookup"><span data-stu-id="fc430-197">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="fc430-198">[WSL2] 空の値を正しく処理するように構成の解析ライブラリを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-198">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="fc430-199">[WSL2] クロス ディストリビューション マウントを作成することにより、Docker Desktop をサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc430-199">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="fc430-200">/etc/wsl.conf ファイルに次の行を追加することにより、ディストリビューションはこの動作をオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="fc430-200">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="fc430-201">ビルド 18945</span><span class="sxs-lookup"><span data-stu-id="fc430-201">Build 18945</span></span>
<span data-ttu-id="fc430-202">ビルド 18945 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-202">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-203">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-203">WSL</span></span>
* <span data-ttu-id="fc430-204">[WSL2] localhost:port を使用して、WSL2 のリスニング tcp ソケットにホストからアクセスできるようにします</span><span class="sxs-lookup"><span data-stu-id="fc430-204">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="fc430-205">[WSL2] インストール/変換エラーの修正と、今後の問題を追跡するための追加の診断 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="fc430-205">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="fc430-206">[WSL2] WSL2 ネットワーク問題の診断能力を向上させます</span><span class="sxs-lookup"><span data-stu-id="fc430-206">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="fc430-207">[WSL2] カーネル バージョンを 4.19.55 に更新します</span><span class="sxs-lookup"><span data-stu-id="fc430-207">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="fc430-208">[WSL2] Docker に必要な構成オプションを使用してカーネルを更新します [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="fc430-208">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="fc430-209">[WSL2] ライトウェイト ユーティリティ VM に割り当てられる CPU の数を、ホストと同じになるように増やします (以前は、カーネル構成の CONFIG_NR_CPUS によって 8 個に制限されていました) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="fc430-209">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="fc430-210">[WSL2] WSL2 ライトウェイト VM 用のスワップ ファイルを作成します</span><span class="sxs-lookup"><span data-stu-id="fc430-210">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="fc430-211">[WSL2] \\\\wsl$\\distro (たとえば、sshfs) を使用してユーザー マウントを表示できるようにします [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="fc430-211">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="fc430-212">[WSL2] 9p ファイルシステムのパフォーマンスを改善します</span><span class="sxs-lookup"><span data-stu-id="fc430-212">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="fc430-213">[WSL2] VHD ACL が無制限に拡張されないようにします [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="fc430-213">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="fc430-214">[WSL2] SquashFS と xt_conntrack をサポートするようにカーネル構成を更新します [GH 4107、4123]</span><span class="sxs-lookup"><span data-stu-id="fc430-214">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="fc430-215">[WSL2] /etc/wsl.conf の interop.enabled オプションの修正 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="fc430-215">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="fc430-216">[WSL2] ファイルシステムで EA がサポートされていない場合、ENOTSUP を返します</span><span class="sxs-lookup"><span data-stu-id="fc430-216">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="fc430-217">[WSL2] \\\\wsl$ での CopyFile のハングを修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-217">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="fc430-218">既定の umask を 0022 に切り替えて、filesystem.umask 設定を /etc/wsl.conf に追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-218">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="fc430-219">シンボリック リンクを正しく解決するように wslpath を修正します。これは、19h1 での不具合でした [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="fc430-219">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="fc430-220">WSL2 設定を調整するために %UserProfile%\\.wslconfig ファイルを導入します</span><span class="sxs-lookup"><span data-stu-id="fc430-220">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="fc430-221">ビルド 18917</span><span class="sxs-lookup"><span data-stu-id="fc430-221">Build 18917</span></span>
<span data-ttu-id="fc430-222">ビルド 18917 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-222">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-223">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-223">WSL</span></span>
* <span data-ttu-id="fc430-224">WSL 2 が利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-224">WSL 2 is now available!</span></span> <span data-ttu-id="fc430-225">詳細については、[ブログ](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-225">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="fc430-226">シンボリック リンクを使用した Windows プロセスの起動が正常に機能しなかった不具合を修正します [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="fc430-226">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="fc430-227">wsl.exe --list --verbose、wsl.exe --list --quiet、および wsl.exe --import --version の各オプションを wsl.exe に追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-227">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="fc430-228">wsl.exe --shutdown オプションを追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-228">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="fc430-229">Plan 9:書き込みを成功させるためにディレクトリを開くことを許可します</span><span class="sxs-lookup"><span data-stu-id="fc430-229">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="fc430-230">ビルド 18890</span><span class="sxs-lookup"><span data-stu-id="fc430-230">Build 18890</span></span>
<span data-ttu-id="fc430-231">ビルド 18890 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-231">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-232">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-232">WSL</span></span>
* <span data-ttu-id="fc430-233">ノンブロッキング ソケット リーク [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="fc430-233">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="fc430-234">ターミナルへの EOF 入力が後続の読み取りをブロックする可能性があります [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="fc430-234">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="fc430-235">wsl.conf を参照するように resolv.conf ヘッダーを更新します [GH 3928 で説明]</span><span class="sxs-lookup"><span data-stu-id="fc430-235">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="fc430-236">epoll の delete コードでのデッドロック [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="fc430-236">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="fc430-237">--import および – export の引数のスペースを処理します [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="fc430-237">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="fc430-238">mmap を使用したファイルの拡張が正しく機能しません [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="fc430-238">Extending mmap'd files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="fc430-239">ARM64 の \\\\wsl$ アクセスが正常に動作しないという問題を修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-239">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="fc430-240">wsl.exe 用のより適切な既定アイコンを追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-240">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="fc430-241">ビルド 18342</span><span class="sxs-lookup"><span data-stu-id="fc430-241">Build 18342</span></span>
<span data-ttu-id="fc430-242">ビルド 18342 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-242">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-243">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-243">WSL</span></span>
* <span data-ttu-id="fc430-244">ユーザーが Windows から WSL ディストリビューションの Linux ファイルにアクセスできるようにする機能を追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-244">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="fc430-245">これらのファイルには、コマンド ラインを使用してアクセスできます。また、ファイル エクスプローラーや VSCode などの Windows アプリもこれらのファイルと対話できます。</span><span class="sxs-lookup"><span data-stu-id="fc430-245">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="fc430-246">\\\\wsl$\\<distro_name> に移動してファイルにアクセスするか、\\\\wsl$ に移動して実行中のディストリビューションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="fc430-246">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="fc430-247">CPU 情報タグを追加し、Cpus_allowed[_list] の値を修正します [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="fc430-247">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="fc430-248">リーダー以外のスレッドからの exec をサポートします [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="fc430-248">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="fc430-249">構成の更新エラーを致命的でないものとして処理します [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="fc430-249">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="fc430-250">オフセットを正しく処理するように binfmt を更新します [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="fc430-250">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="fc430-251">Plan 9 のネットワーク ドライブのマッピングを有効にします [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="fc430-251">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="fc430-252">バインド マウントのための Windows -> Linux および Linux -> Windows のパスの変換をサポートします</span><span class="sxs-lookup"><span data-stu-id="fc430-252">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="fc430-253">読み取り専用で開かれたファイルにマッピング用の読み取り専用セクションを作成します</span><span class="sxs-lookup"><span data-stu-id="fc430-253">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="fc430-254">ビルド 18334</span><span class="sxs-lookup"><span data-stu-id="fc430-254">Build 18334</span></span>
<span data-ttu-id="fc430-255">ビルド 18334 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-255">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-256">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-256">WSL</span></span>
* <span data-ttu-id="fc430-257">Windows タイム ゾーンが Linux タイム ゾーンにマップされる方法を再設計します [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="fc430-257">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="fc430-258">メモリ リークを修正し、新しい文字列変換関数を追加します [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="fc430-258">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="fc430-259">スレッドがない threadgroup での SIGCONT は no-op です [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="fc430-259">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="fc430-260">/proc/self/fd にソケットと epoll のファイル記述子を正しく表示します</span><span class="sxs-lookup"><span data-stu-id="fc430-260">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="fc430-261">ビルド 18305</span><span class="sxs-lookup"><span data-stu-id="fc430-261">Build 18305</span></span>
<span data-ttu-id="fc430-262">ビルド 18305 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-262">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-263">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-263">WSL</span></span>
* <span data-ttu-id="fc430-264">プライマリ スレッドが終了すると、pthread はファイルへのアクセスを失います [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="fc430-264">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="fc430-265">必要な場合を除き、TIOCSCTTY では "force" パラメーターが無視されます [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="fc430-265">TIOCSCTTY should ignore the "force" parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="fc430-266">wsl.exe コマンド ラインの機能強化と、インポート/エクスポートの機能の追加。</span><span class="sxs-lookup"><span data-stu-id="fc430-266">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="fc430-267">ビルド 18277</span><span class="sxs-lookup"><span data-stu-id="fc430-267">Build 18277</span></span>
<span data-ttu-id="fc430-268">ビルド 18277 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-268">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-269">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-269">WSL</span></span>
* <span data-ttu-id="fc430-270">ビルド 18272 で発生した「そのようなインターフェイスはサポートされていません」というエラーを修正します [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="fc430-270">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="fc430-271">umount システム コールの MNT_FORCE フラグを無視します [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="fc430-271">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="fc430-272">公式の CreatePseudoConsole API を使用するように WSL の相互運用を切り替えます</span><span class="sxs-lookup"><span data-stu-id="fc430-272">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="fc430-273">FUTEX_WAIT の再起動時にタイムアウト値を保持しません</span><span class="sxs-lookup"><span data-stu-id="fc430-273">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="fc430-274">ビルド 18272</span><span class="sxs-lookup"><span data-stu-id="fc430-274">Build 18272</span></span>
<span data-ttu-id="fc430-275">ビルド18272の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-275">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-276">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-276">WSL</span></span>
* <span data-ttu-id="fc430-277">**警告:** このビルドには、WSL を操作不能にする問題があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-277">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="fc430-278">ディストリビューションを起動しようとすると、「そのようなインターフェイスはサポートされていません」というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-278">When trying to launch your distribution you will see a "No such interface supported" error.</span></span> <span data-ttu-id="fc430-279">この問題は修正されており、次週の Insider Fast ビルドに組み込まれます。</span><span class="sxs-lookup"><span data-stu-id="fc430-279">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="fc430-280">このビルドをインストールした場合は、[設定] -> [更新とセキュリティ] -> [回復] を選択し、「前のバージョンの Windows 10 に戻す」を使用することで、前の Windows ビルドにロールバックできます。</span><span class="sxs-lookup"><span data-stu-id="fc430-280">If you've installed this build you can roll back to the previous Windows build using "Go back to the previous version of Windows 10" in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="fc430-281">ビルド 18267</span><span class="sxs-lookup"><span data-stu-id="fc430-281">Build 18267</span></span>
<span data-ttu-id="fc430-282">ビルド 18267 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-282">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-283">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-283">WSL</span></span>
* <span data-ttu-id="fc430-284">ゾンビ プロセスが回収されず、無期限に存在し続ける問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-284">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="fc430-285">エラー メッセージが最大長を超えると、WslRegisterDistribution がハングします [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="fc430-285">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="fc430-286">DrvFs で読み取り専用ファイルに対して fsync を正常に実行できるようにします [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="fc430-286">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="fc430-287">内部にシンボリック リンクを作成する前に /bin ディレクトリと /sbin ディレクトリが存在することを確認します [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="fc430-287">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="fc430-288">WSL インスタンスに対するインスタンス終了タイムアウト メカニズムを追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-288">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="fc430-289">タイムアウトは現在 15 秒に設定されています。つまり、最後の WSL プロセスが終了してから 15 秒後にインスタンスが終了します。</span><span class="sxs-lookup"><span data-stu-id="fc430-289">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="fc430-290">ディストリビューションをすぐに終了するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc430-290">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="fc430-291">ビルド 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="fc430-291">Build 17763 (1809)</span></span>
<span data-ttu-id="fc430-292">ビルド 17763 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-292">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-293">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-293">WSL</span></span>
* <span data-ttu-id="fc430-294">Setpriority システム コールのアクセス許可チェックが厳しすぎて、同じスレッドの優先順位を変更できません [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="fc430-294">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="fc430-295">clock_gettime(CLOCK_BOOTTIME) に対して負値が返されないように、バイアスのかかっていない割り込み時間が起動時間に使用されていることを確認します [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="fc430-295">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="fc430-296">WSL binfmt インタープリターでシンボリック リンクを処理します [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="fc430-296">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="fc430-297">threadgroup リーダー ファイル記述子のクリーンアップの処理が改善されました。</span><span class="sxs-lookup"><span data-stu-id="fc430-297">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="fc430-298">オーバーフローを回避するために、KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用するように WSL を切り替えます [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="fc430-298">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="fc430-299">Ptrace のアタッチにより、システム コールから無効な戻り値が返される場合があります [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="fc430-299">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="fc430-300">AF_UNIX に関連したいくつかの問題を修正します [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="fc430-300">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="fc430-301">現在の作業ディレクトリが 5 文字未満の場合に WSL の相互運用が失敗する原因となる問題を修正します [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="fc430-301">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="fc430-302">存在しないポートへのループバック接続の失敗による 1 秒間の遅延を回避します [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="fc430-302">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="fc430-303">/proc/sys/fs/file-max スタブ ファイルを追加します [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="fc430-303">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="fc430-304">より正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="fc430-304">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="fc430-305">PR_SET_PTRACER のサポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="fc430-305">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="fc430-306">エッジ トリガーされた epoll イベントをパイプ ファイルシステムが誤ってクリアします [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="fc430-306">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="fc430-307">NTFS シンボリック リンクによって起動された Win32 実行可能ファイルはシンボリック リンク名を考慮しません [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="fc430-307">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="fc430-308">ゾンビ サポートを強化しました [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="fc430-308">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="fc430-309">Windows の相互運用の動作を制御するための wsl.conf エントリを追加します [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="fc430-309">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="fc430-310">getsockname で必ずしも UNIX ソケット ファミリの種類が返されない問題を修正します [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="fc430-310">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="fc430-311">TIOCSTI のサポートを追加します [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="fc430-311">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="fc430-312">接続処理中のノンブロッキング ソケットは、書き込み試行に対して EAGAIN を返します [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="fc430-312">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="fc430-313">マウントされた VHD での相互運用をサポートします [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="fc430-313">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="fc430-314">ルート フォルダーでのアクセス許可チェックの問題を修正します [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="fc430-314">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="fc430-315">TTY キーボードの ioctl (KDGKBTYPE、KDGKBMODE、および KDSKBMODE) に対する制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-315">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="fc430-316">Windows UI アプリは、バックグラウンドで起動された場合でも実行されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-316">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="fc430-317">wsl -u または --user オプションを追加します [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="fc430-317">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="fc430-318">高速スタートアップが有効になっているときの WSL の起動問題を修正します [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="fc430-318">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="fc430-319">UNIX ソケットは切断されたピア資格情報を保持する必要があります [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="fc430-319">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="fc430-320">ノンブロッキング UNIX ソケットが EAGAIN で無限に失敗します [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="fc430-320">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="fc430-321">case=off が、drvfs マウントの新しい既定の種類です [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="fc430-321">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="fc430-322">詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-322">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="fc430-323">実行中のディストリビューションを停止するための wslconfig /terminate を追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-323">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="fc430-324">スペースを含むパスを正しく処理しない WSL シェル コンテキスト メニュー エントリの問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-324">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="fc430-325">ディレクトリごとの大文字と小文字の区別を拡張属性として公開します</span><span class="sxs-lookup"><span data-stu-id="fc430-325">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="fc430-326">ARM64: キャッシュのメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="fc430-326">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="fc430-327">[dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。</span><span class="sxs-lookup"><span data-stu-id="fc430-327">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="fc430-328">DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみをエスケープ解除します。</span><span class="sxs-lookup"><span data-stu-id="fc430-328">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="fc430-329">ELF パーサー インタープリターの長さの検証での Off-by-one エラーを修正します [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="fc430-329">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="fc430-330">過去の時刻が設定された WSL 絶対タイマーは起動しません [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="fc430-330">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="fc430-331">新しく作成された再解析ポイントが、親ディレクトリにそのように表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="fc430-331">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="fc430-332">DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。</span><span class="sxs-lookup"><span data-stu-id="fc430-332">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="fc430-333">ファイルが存在していてもマルチスレッドの操作で ENOENT が返される場合がある追加の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-333">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="fc430-334">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="fc430-334">[GH 2712]</span></span>
* <span data-ttu-id="fc430-335">UMCI が有効になっているときの WSL の起動エラーを修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-335">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="fc430-336">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="fc430-336">[GH 3020]</span></span>
* <span data-ttu-id="fc430-337">WSL を起動するエクスプローラーのコンテキスト メニューを追加します [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="fc430-337">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="fc430-338">使用するには、エクスプローラー ウィンドウで Shift キーを押しながら右クリックします。</span><span class="sxs-lookup"><span data-stu-id="fc430-338">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="fc430-339">UNIX ソケットのノンブロッキング動作を修正します [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="fc430-339">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="fc430-340">GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-340">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="fc430-341">マウント伝達フラグのサポートを追加します [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="fc430-341">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="fc430-342">truncate で INotify イベントが発生しない問題を修正します [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="fc430-342">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="fc430-343">シェルを使用せずに 1 つのバイナリを呼び出す wsl.exe の --exec オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-343">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="fc430-344">特定のディストリビューションを選択する wsl.exe の --distribution オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-344">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="fc430-345">dmesg の制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-345">Limited support for dmesg.</span></span> <span data-ttu-id="fc430-346">アプリケーションは、dmesg にログを記録できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-346">Applications can now log to dmesg.</span></span> <span data-ttu-id="fc430-347">WSL ドライバーは、限られた情報を dmesg に記録します。</span><span class="sxs-lookup"><span data-stu-id="fc430-347">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="fc430-348">将来的には、ドライバーからのその他の情報や診断情報を伝達するように拡張できます。</span><span class="sxs-lookup"><span data-stu-id="fc430-348">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="fc430-349">注: dmesg は、現在、`/dev/kmsg` デバイス インターフェイスを介してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="fc430-349">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="fc430-350">`syslog` システム コール インターフェイスはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fc430-350">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="fc430-351">そのため、一部の `dmesg` コマンド ラインのオプション (`-S`、`-C` など) は機能しません。</span><span class="sxs-lookup"><span data-stu-id="fc430-351">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="fc430-352">ネイティブに一致するように、シリアル デバイスの既定の gid とモードを変更します [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="fc430-352">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="fc430-353">DrvFs で拡張属性がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-353">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="fc430-354">注: DrvFs では、拡張属性の名前にいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-354">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="fc430-355">一部の文字 ('/'、':'、'\*' など) は使用できません。また、DrvFs では拡張属性名の大文字と小文字は区別されません</span><span class="sxs-lookup"><span data-stu-id="fc430-355">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="fc430-356">ビルド 18252 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="fc430-356">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="fc430-357">ビルド 18252 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-357">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-358">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-358">WSL</span></span>
* <span data-ttu-id="fc430-359">init と bsdtar のバイナリを lxssmanager dll から別のツール フォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="fc430-359">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="fc430-360">CLONE_FILES を使用しているときのファイル記述子の終了に関する競合を修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-360">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="fc430-361">DrvFs パスを変換するときに /proc/pid/mountinfo の省略可能なフィールドを処理します</span><span class="sxs-lookup"><span data-stu-id="fc430-361">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="fc430-362">S_IFREG のメタデータのサポートなしに DrvFs mknod を正常に実行できるようにします</span><span class="sxs-lookup"><span data-stu-id="fc430-362">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="fc430-363">DrvFs に作成される読み取り専用ファイルには readonly 属性セットが必要です [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="fc430-363">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="fc430-364">DrvFs のマウントを処理する /sbin/mount.drvfs ヘルパーを追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-364">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="fc430-365">DrvFs で POSIX rename を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc430-365">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="fc430-366">ボリューム GUID がないボリュームでのパスの変換を許可します。</span><span class="sxs-lookup"><span data-stu-id="fc430-366">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="fc430-367">ビルド 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc430-367">Build 17738 (Fast)</span></span>
<span data-ttu-id="fc430-368">ビルド 17738 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-368">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-369">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-369">WSL</span></span>
* <span data-ttu-id="fc430-370">Setpriority システム コールのアクセス許可チェックが厳しすぎて、同じスレッドの優先順位を変更できません [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="fc430-370">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="fc430-371">clock_gettime(CLOCK_BOOTTIME) に対して負値が返されないように、バイアスのかかっていない割り込み時間が起動時間に使用されていることを確認します [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="fc430-371">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="fc430-372">WSL binfmt インタープリターでシンボリック リンクを処理します [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="fc430-372">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="fc430-373">threadgroup リーダー ファイル記述子のクリーンアップの処理が改善されました。</span><span class="sxs-lookup"><span data-stu-id="fc430-373">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="fc430-374">ビルド 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc430-374">Build 17728 (Fast)</span></span>
<span data-ttu-id="fc430-375">ビルド 17728 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-375">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-376">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-376">WSL</span></span>
* <span data-ttu-id="fc430-377">オーバーフローを回避するために、KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用するように WSL を切り替えます [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="fc430-377">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="fc430-378">Ptrace のアタッチにより、システム コールから無効な戻り値が返される場合があります [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="fc430-378">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="fc430-379">AF_UNIX に関連した複数の問題を修正します [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="fc430-379">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="fc430-380">現在の作業ディレクトリが 5 文字未満の場合に WSL の相互運用が失敗する原因となる問題を修正します [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="fc430-380">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="fc430-381">ビルド 18204 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="fc430-381">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="fc430-382">ビルド 18204 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-382">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-383">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-383">WSL</span></span>
* <span data-ttu-id="fc430-384">エッジ トリガーされた epoll イベントをパイプ ファイルシステムが誤ってクリアします [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="fc430-384">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="fc430-385">NTFS シンボリック リンクによって起動された Win32 実行可能ファイルはシンボリック リンク名を考慮しません [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="fc430-385">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="fc430-386">ビルド 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc430-386">Build 17723 (Fast)</span></span>
<span data-ttu-id="fc430-387">ビルド 17723 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-387">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-388">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-388">WSL</span></span>
* <span data-ttu-id="fc430-389">存在しないポートへのループバック接続の失敗による 1 秒間の遅延を回避します [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="fc430-389">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="fc430-390">/proc/sys/fs/file-max スタブ ファイルを追加します [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="fc430-390">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="fc430-391">より正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="fc430-391">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="fc430-392">PR_SET_PTRACER のサポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="fc430-392">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="fc430-393">エッジ トリガーされた epoll イベントをパイプ ファイルシステムが誤ってクリアします [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="fc430-393">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="fc430-394">NTFS シンボリック リンクによって起動された Win32 実行可能ファイルはシンボリック リンク名を考慮しません [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="fc430-394">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="fc430-395">ビルド 17713</span><span class="sxs-lookup"><span data-stu-id="fc430-395">Build 17713</span></span>
<span data-ttu-id="fc430-396">ビルド 17713 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-396">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-397">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-397">WSL</span></span>
* <span data-ttu-id="fc430-398">ゾンビ サポートを強化しました [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="fc430-398">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="fc430-399">Windows の相互運用の動作を制御するための wsl.conf エントリを追加します [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="fc430-399">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="fc430-400">getsockname で必ずしも UNIX ソケット ファミリの種類が返されない問題を修正します [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="fc430-400">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="fc430-401">TIOCSTI のサポートを追加します [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="fc430-401">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="fc430-402">接続処理中のノンブロッキング ソケットは、書き込み試行に対して EAGAIN を返します [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="fc430-402">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="fc430-403">マウントされた VHD での相互運用をサポートします [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="fc430-403">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="fc430-404">ルート フォルダーでのアクセス許可チェックの問題を修正します [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="fc430-404">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="fc430-405">TTY キーボードの ioctl (KDGKBTYPE、KDGKBMODE、および KDSKBMODE) に対する制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-405">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="fc430-406">Windows UI アプリは、バックグラウンドで起動された場合でも実行されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-406">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="fc430-407">ビルド 17704</span><span class="sxs-lookup"><span data-stu-id="fc430-407">Build 17704</span></span>
<span data-ttu-id="fc430-408">ビルド 17704 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-408">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-409">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-409">WSL</span></span>
* <span data-ttu-id="fc430-410">wsl -u または --user オプションを追加します [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="fc430-410">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="fc430-411">高速スタートアップが有効になっているときの WSL の起動問題を修正します [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="fc430-411">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="fc430-412">UNIX ソケットは切断されたピア資格情報を保持する必要があります [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="fc430-412">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="fc430-413">ノンブロッキング UNIX ソケットが EAGAIN で無限に失敗します [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="fc430-413">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="fc430-414">case=off が、drvfs マウントの新しい既定の種類です [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="fc430-414">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="fc430-415">詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-415">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="fc430-416">実行中のディストリビューションを停止するための wslconfig /terminate を追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-416">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="fc430-417">ビルド 17692</span><span class="sxs-lookup"><span data-stu-id="fc430-417">Build 17692</span></span>
<span data-ttu-id="fc430-418">ビルド 17692 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-418">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-419">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-419">WSL</span></span>
* <span data-ttu-id="fc430-420">スペースを含むパスを正しく処理しない WSL シェル コンテキスト メニュー エントリの問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-420">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="fc430-421">ディレクトリごとの大文字と小文字の区別を拡張属性として公開します</span><span class="sxs-lookup"><span data-stu-id="fc430-421">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="fc430-422">ARM64: キャッシュのメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="fc430-422">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="fc430-423">[dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。</span><span class="sxs-lookup"><span data-stu-id="fc430-423">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="fc430-424">DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみをエスケープ解除します。</span><span class="sxs-lookup"><span data-stu-id="fc430-424">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="fc430-425">ビルド 17686</span><span class="sxs-lookup"><span data-stu-id="fc430-425">Build 17686</span></span>
<span data-ttu-id="fc430-426">ビルド 17686 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-426">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-427">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-427">WSL</span></span>
* <span data-ttu-id="fc430-428">ELF パーサー インタープリターの長さの検証での Off-by-one エラーを修正します [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="fc430-428">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="fc430-429">過去の時刻が設定された WSL 絶対タイマーは起動しません [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="fc430-429">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="fc430-430">新しく作成された再解析ポイントが、親ディレクトリにそのように表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="fc430-430">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="fc430-431">DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。</span><span class="sxs-lookup"><span data-stu-id="fc430-431">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="fc430-432">ビルド 17677</span><span class="sxs-lookup"><span data-stu-id="fc430-432">Build 17677</span></span>
<span data-ttu-id="fc430-433">ビルド 17677 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-433">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-434">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-434">WSL</span></span>
* <span data-ttu-id="fc430-435">ファイルが存在していてもマルチスレッドの操作で ENOENT が返される場合がある追加の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-435">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="fc430-436">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="fc430-436">[GH 2712]</span></span>
* <span data-ttu-id="fc430-437">UMCI が有効になっているときの WSL の起動エラーを修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-437">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="fc430-438">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="fc430-438">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="fc430-439">ビルド 17666</span><span class="sxs-lookup"><span data-stu-id="fc430-439">Build 17666</span></span>
<span data-ttu-id="fc430-440">ビルド 17666 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-440">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-441">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-441">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="fc430-442">警告:一部の AMD チップセットに WSL の実行を妨げる問題があります [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="fc430-442">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="fc430-443">修正は準備できており、間もなく Insider ビルド ブランチで公開されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-443">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="fc430-444">WSL を起動するエクスプローラーのコンテキスト メニューを追加します [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="fc430-444">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="fc430-445">使用するには、エクスプローラー ウィンドウで Shift キーを押しながら右クリックします。</span><span class="sxs-lookup"><span data-stu-id="fc430-445">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="fc430-446">UNIX ソケットのノンブロッキング動作を修正します [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="fc430-446">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="fc430-447">GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-447">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="fc430-448">マウント伝達フラグのサポートを追加します [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="fc430-448">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="fc430-449">truncate で INotify イベントが発生しない問題を修正します [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="fc430-449">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="fc430-450">シェルを使用せずに 1 つのバイナリを呼び出す wsl.exe の --exec オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-450">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="fc430-451">特定のディストリビューションを選択する wsl.exe の --distribution オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-451">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="fc430-452">ビルド 17655 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="fc430-452">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="fc430-453">ビルド 17655 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-453">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-454">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-454">WSL</span></span>
* <span data-ttu-id="fc430-455">dmesg の制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-455">Limited support for dmesg.</span></span> <span data-ttu-id="fc430-456">アプリケーションは、dmesg にログを記録できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-456">Applications can now log to dmesg.</span></span> <span data-ttu-id="fc430-457">WSL ドライバーは、限られた情報を dmesg に記録します。</span><span class="sxs-lookup"><span data-stu-id="fc430-457">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="fc430-458">将来的には、ドライバーからのその他の情報や診断情報を伝達するように拡張できます。</span><span class="sxs-lookup"><span data-stu-id="fc430-458">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="fc430-459">注: 現在、dmesg は `/dev/kmsg` デバイス インターフェイスを介してサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fc430-459">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="fc430-460">`syslog` システム コール インターフェイスはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="fc430-460">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="fc430-461">そのため、一部の `dmesg` コマンド ラインのオプション (`-S`、`-C` など) は機能しません。</span><span class="sxs-lookup"><span data-stu-id="fc430-461">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="fc430-462">ファイルが存在している場合でもマルチスレッドの操作で ENOENT が返される場合がある問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-462">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="fc430-463">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="fc430-463">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="fc430-464">ビルド 17639 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="fc430-464">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="fc430-465">ビルド 17639 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-465">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-466">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-466">WSL</span></span>
* <span data-ttu-id="fc430-467">ネイティブに一致するように、シリアル デバイスの既定の gid とモードを変更します [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="fc430-467">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="fc430-468">DrvFs で拡張属性がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-468">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="fc430-469">注: DrvFs では、拡張属性の名前にいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-469">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="fc430-470">特に、一部の文字 ('/'、':'、'\*' など) は使用できません。また、拡張属性名は DrvFs では大文字と小文字が区別されません</span><span class="sxs-lookup"><span data-stu-id="fc430-470">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="fc430-471">ビルド 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc430-471">Build 17133 (Fast)</span></span>
<span data-ttu-id="fc430-472">ビルド 17133 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-472">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-473">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-473">WSL</span></span>
* <span data-ttu-id="fc430-474">WSL でのハングの修正。</span><span class="sxs-lookup"><span data-stu-id="fc430-474">Fix for hang in WSL.</span></span> <span data-ttu-id="fc430-475">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="fc430-475">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="fc430-476">ビルド 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="fc430-476">Build 17128 (Fast)</span></span>
<span data-ttu-id="fc430-477">ビルド 17128 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-477">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-478">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-478">WSL</span></span>
* <span data-ttu-id="fc430-479">None</span><span class="sxs-lookup"><span data-stu-id="fc430-479">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="fc430-480">ビルド 17627 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="fc430-480">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="fc430-481">ビルド 17627 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-481">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-482">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-482">WSL</span></span>
* <span data-ttu-id="fc430-483">futex の pi 対応操作のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-483">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="fc430-484">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="fc430-484">[GH 1006]</span></span>
    * <span data-ttu-id="fc430-485">優先順位は現在サポートされている WSL 機能ではないため、制限がありますが、標準の使用はブロック解除する必要がある点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-485">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="fc430-486">WSL プロセスに対する Windows ファイアウォールのサポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-486">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="fc430-487">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="fc430-487">[GH 1852]</span></span>
    * <span data-ttu-id="fc430-488">たとえば、WSL python プロセスが任意のポートでリッスンできるようにするには、次の管理者特権の Windows コマンドを使用します: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="fc430-488">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="fc430-489">ファイアウォール規則を追加する方法の詳細については、[リンク](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-489">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="fc430-490">WSL を使用するときにユーザーの既定のシェルを考慮します。</span><span class="sxs-lookup"><span data-stu-id="fc430-490">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="fc430-491">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="fc430-491">[GH 2372]</span></span>
* <span data-ttu-id="fc430-492">すべてのネットワーク インターフェイスをイーサネットとして報告します。</span><span class="sxs-lookup"><span data-stu-id="fc430-492">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="fc430-493">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="fc430-493">[GH 2996]</span></span>
* <span data-ttu-id="fc430-494">破損した /etc/passwd ファイルの処理が改善。</span><span class="sxs-lookup"><span data-stu-id="fc430-494">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="fc430-495">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="fc430-495">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="fc430-496">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-496">Console</span></span>
* <span data-ttu-id="fc430-497">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-498">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-498">LTP Results:</span></span>
<span data-ttu-id="fc430-499">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-499">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="fc430-500">ビルド 17618 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="fc430-500">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="fc430-501">ビルド 17618 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-501">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-502">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-502">WSL</span></span>
* <span data-ttu-id="fc430-503">NT 相互運用のために pseudoconsole 機能を導入します [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="fc430-503">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="fc430-504">レガシ インストール メカニズム (lxrun.exe) は非推奨となりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-504">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="fc430-505">ディストリビューションをインストールするためのサポートされているメカニズムは、Microsoft Store 経由です。</span><span class="sxs-lookup"><span data-stu-id="fc430-505">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="fc430-506">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-506">Console</span></span>
* <span data-ttu-id="fc430-507">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-507">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-508">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-508">LTP Results:</span></span>
<span data-ttu-id="fc430-509">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-509">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="fc430-510">ビルド 17110</span><span class="sxs-lookup"><span data-stu-id="fc430-510">Build 17110</span></span>
<span data-ttu-id="fc430-511">ビルド 17110 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-511">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-512">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-512">WSL</span></span>
* <span data-ttu-id="fc430-513">/init を Windows から終了することを許可します [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="fc430-513">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="fc430-514">DrvFs では、ディレクトリごとの大文字小文字の区別が既定で使用されるようになりました ("case = dir" マウント オプションと同等)。</span><span class="sxs-lookup"><span data-stu-id="fc430-514">DrvFs now uses per-directory case sensitivity by default (equivalent to the "case=dir" mount option).</span></span>
    * <span data-ttu-id="fc430-515">"case=force" (以前の動作) を使用するには、レジストリ キーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-515">Using "case=force" (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="fc430-516">"case=force" を使用する必要がある場合は、次のコマンドを実行して有効にします: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="fc430-516">Run the following command to enable "case=force" if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="fc430-517">以前のバージョンの Windows に含まれている WSL で作成された既存のディレクトリがあり、大文字と小文字を区別する必要がある場合は、次の fsutil.exe を使用して大文字と小文字を区別するように指定します: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="fc430-517">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="fc430-518">uname システム コールから NULL の終了文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-518">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="fc430-519">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-519">Console</span></span>
* <span data-ttu-id="fc430-520">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-520">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-521">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-521">LTP Results:</span></span>
<span data-ttu-id="fc430-522">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-522">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="fc430-523">ビルド 17107</span><span class="sxs-lookup"><span data-stu-id="fc430-523">Build 17107</span></span>
<span data-ttu-id="fc430-524">ビルド 17107 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-524">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-525">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-525">WSL</span></span>
* <span data-ttu-id="fc430-526">マスター pty エンドポイントで TCSETSF と TCSETSW をサポートします [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="fc430-526">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="fc430-527">相互運用プロセスを同時に開始すると、EINVAL が発生します [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="fc430-527">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="fc430-528">/proc/pid/status に適切なトレース状態を表示するように PTRACE_ATTACH を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-528">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="fc430-529">CLEARTID フラグと SETTID フラグの両方を指定して複製された、有効期間の短いプロセスが、TID アドレスをクリアせずに終了する場合がある競合を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-529">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="fc430-530">17093 より前のビルドから移行するときに、Linux ファイルシステムのディレクトリをアップグレードする際にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc430-530">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="fc430-531">17093 のファイルシステムの変更について詳しくは、[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) のリリース ノートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-531">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="fc430-532">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-532">Console</span></span>
* <span data-ttu-id="fc430-533">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-533">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-534">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-534">LTP Results:</span></span>
<span data-ttu-id="fc430-535">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-535">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="fc430-536">ビルド 17101</span><span class="sxs-lookup"><span data-stu-id="fc430-536">Build 17101</span></span>
<span data-ttu-id="fc430-537">ビルド 17101 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-537">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-538">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-538">WSL</span></span>
* <span data-ttu-id="fc430-539">signalfd のサポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-539">Support for signalfd.</span></span> <span data-ttu-id="fc430-540">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="fc430-540">[GH 129]</span></span>
* <span data-ttu-id="fc430-541">無効な NTFS 文字を含むファイル名を、プライベート Unicode 文字としてエンコードすることによってサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc430-541">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="fc430-542">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="fc430-542">[GH 1514]</span></span>
* <span data-ttu-id="fc430-543">書き込みがサポートされていない場合、自動マウントは読み取り専用にフォールバックします。</span><span class="sxs-lookup"><span data-stu-id="fc430-543">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="fc430-544">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="fc430-544">[GH 2603]</span></span>
* <span data-ttu-id="fc430-545">Unicode サロゲート ペア (絵文字など) の貼り付けを許可します。</span><span class="sxs-lookup"><span data-stu-id="fc430-545">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="fc430-546">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="fc430-546">[GH 2765]</span></span>
* <span data-ttu-id="fc430-547">/proc および /sys 内の疑似ファイルは、select、poll、epoll などから、読み書き可能を返します。[GH 2838]</span><span class="sxs-lookup"><span data-stu-id="fc430-547">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="fc430-548">レジストリが改ざんされているか破損している場合にサービスが無限ループに入る原因となる問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-548">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="fc430-549">iproute2 の新しい (アップストリーム 4.14) バージョンで機能するように netlink メッセージを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-549">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="fc430-550">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-550">Console</span></span>
* <span data-ttu-id="fc430-551">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-551">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-552">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-552">LTP Results:</span></span>
<span data-ttu-id="fc430-553">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-553">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="fc430-554">ビルド 17093</span><span class="sxs-lookup"><span data-stu-id="fc430-554">Build 17093</span></span>
<span data-ttu-id="fc430-555">ビルド 17093 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-555">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="fc430-556">重要:</span><span class="sxs-lookup"><span data-stu-id="fc430-556">Important:</span></span>
<span data-ttu-id="fc430-557">このビルドにアップグレードした後に初めて WSL を開始するときに、Linux ファイルシステムのディレクトリをアップグレードする作業を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-557">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="fc430-558">この処理には数分かかる場合があるため、WSL の開始に時間がかかっているように見えることがあります。</span><span class="sxs-lookup"><span data-stu-id="fc430-558">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="fc430-559">これは、ストアからインストールされた各ディストリビューションにつき 1 回のみ発生します。</span><span class="sxs-lookup"><span data-stu-id="fc430-559">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="fc430-560">DrvFs での大文字と小文字の区別のサポートを改善しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-560">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="fc430-561">DrvFs では、ディレクトリごとの大文字小文字の区別がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-561">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="fc430-562">これは、ディレクトリに設定できる新しいフラグで、これらのディレクトリ内のすべての操作を大文字と小文字を区別して扱う必要があることを示します。これにより、Windows アプリケーションでも、大文字と小文字のみが異なるファイルを正しく開くことが可能になります。</span><span class="sxs-lookup"><span data-stu-id="fc430-562">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="fc430-563">DrvFs には、ディレクトリごとに大文字と小文字の区別を制御する新しいマウント オプションがあります</span><span class="sxs-lookup"><span data-stu-id="fc430-563">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="fc430-564">case=force: すべてのディレクトリは、大文字小文字を区別して処理されます (ドライブのルートを除く)。</span><span class="sxs-lookup"><span data-stu-id="fc430-564">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="fc430-565">WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-565">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="fc430-566">これは、新しいディレクトリに大文字小文字を区別するようにマークを付けることを除き、従来の動作です。</span><span class="sxs-lookup"><span data-stu-id="fc430-566">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="fc430-567">case=dir: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは、大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="fc430-567">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="fc430-568">WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-568">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="fc430-569">case=off: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは、大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="fc430-569">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="fc430-570">WSL で作成された新しいディレクトリは、大文字と小文字を区別しないようにマークが付けられます。</span><span class="sxs-lookup"><span data-stu-id="fc430-570">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="fc430-571">注: 以前のリリースの WSL によって作成されたディレクトリにはこのフラグが設定されていないため、"case=dir" オプションを使用しても、大文字と小文字を区別して処理されません。</span><span class="sxs-lookup"><span data-stu-id="fc430-571">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the "case=dir" option.</span></span> <span data-ttu-id="fc430-572">既存のディレクトリにこのフラグを設定する方法は、近日公開予定です。</span><span class="sxs-lookup"><span data-stu-id="fc430-572">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="fc430-573">これらのオプションを使用したマウントの例 (既存のドライブの場合、別のオプションを使用してマウントする前にマウントを解除する必要があります): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="fc430-573">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="fc430-574">現時点では、case=force がまだ既定のオプションです。</span><span class="sxs-lookup"><span data-stu-id="fc430-574">For now, case=force is still the default option.</span></span> <span data-ttu-id="fc430-575">これは将来、case=dir に変更されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-575">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="fc430-576">DrvFs をマウントするときに Windows パスでスラッシュを使用できるようになりました。例: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="fc430-576">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="fc430-577">WSL は、インスタンスの開始時に /etc/fstab ファイルを処理するようになりました [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="fc430-577">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="fc430-578">これは、DrvFs ドライブを自動的にマウントする前に行われます。fstab によって既にマウントされているドライブは自動的には再マウントされないため、特定のドライブのマウント ポイントを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="fc430-578">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="fc430-579">この動作は、wsl.conf を使用して無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="fc430-579">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="fc430-580">/proc 内の mount、mountinfo、および mountstats の各ファイルは、円記号やスペースなどの特殊文字を正しくエスケープ処理します [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="fc430-580">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="fc430-581">WSL シンボリック リンクなどの DrvFs で作成された特殊ファイル、またはメタデータが有効になっている場合の FIFO やソケットを、Windows からコピーおよび移動できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-581">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="fc430-582">WSL は、wsl.conf を使用してさらに構成可能です</span><span class="sxs-lookup"><span data-stu-id="fc430-582">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="fc430-583">サブシステムを起動するたびに適用される WSL の特定の機能を自動的に構成するための方法を追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-583">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="fc430-584">これには自動マウント オプションとネットワーク構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc430-584">This includes automount options and network configuration.</span></span> <span data-ttu-id="fc430-585">詳細については、次のブログ投稿を参照してください: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="fc430-585">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="fc430-586">AF_UNIX により、WSL 上の Linux プロセスと Windows ネイティブ プロセス間のソケット接続が可能になります</span><span class="sxs-lookup"><span data-stu-id="fc430-586">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="fc430-587">WSL と Windows のアプリケーションは、UNIX ソケット経由で相互に通信できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-587">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="fc430-588">Windows でサービスを実行し、それを Windows と WSL の両方のアプリで使用できるようにする場合を考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="fc430-588">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="fc430-589">これは、UNIX ソケットを使用することで可能になりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-589">Now, that's possible with Unix sockets.</span></span> <span data-ttu-id="fc430-590">詳細については、次のブログ投稿をお読みください: https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="fc430-590">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-591">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-591">WSL</span></span>
* <span data-ttu-id="fc430-592">MAP_NORESERVE で mmap() をサポートします [GH 121、2784]</span><span class="sxs-lookup"><span data-stu-id="fc430-592">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="fc430-593">CLONE_PTRACE と CLONE_UNTRACED をサポートします [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="fc430-593">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="fc430-594">複製で SIGCHLD 以外の終了シグナルを処理します [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="fc430-594">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="fc430-595">/proc/sys/fs/inotify/max_user_instances および /proc/sys/fs/inotify/max_user_watches をスタブします [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="fc430-595">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="fc430-596">ゼロ以外のオフセットの読み込みヘッダーを含む ELF バイナリの読み込みエラー [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="fc430-596">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="fc430-597">イメージを読み込むときにページの末尾バイトをゼロ設定します。</span><span class="sxs-lookup"><span data-stu-id="fc430-597">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="fc430-598">execve が警告なしにプロセスを終了するケースを削減します</span><span class="sxs-lookup"><span data-stu-id="fc430-598">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="fc430-599">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-599">Console</span></span>
* <span data-ttu-id="fc430-600">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-600">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-601">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-601">LTP Results:</span></span>
<span data-ttu-id="fc430-602">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-602">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="fc430-603">ビルド 17083</span><span class="sxs-lookup"><span data-stu-id="fc430-603">Build 17083</span></span>
<span data-ttu-id="fc430-604">ビルド 17083 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-604">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-605">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-605">WSL</span></span>
* <span data-ttu-id="fc430-606">epoll に関連したバグチェックを修正しました [GH 2798、2801、2857]</span><span class="sxs-lookup"><span data-stu-id="fc430-606">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="fc430-607">ASLR をオフにする際のハングを修正しました [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="fc430-607">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="fc430-608">mmap 操作がアトミックに見えるようにします [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="fc430-608">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="fc430-609">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-609">Console</span></span>
* <span data-ttu-id="fc430-610">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-610">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-611">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-611">LTP Results:</span></span>
<span data-ttu-id="fc430-612">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-612">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="fc430-613">ビルド 17074</span><span class="sxs-lookup"><span data-stu-id="fc430-613">Build 17074</span></span>
<span data-ttu-id="fc430-614">ビルド 17074 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-614">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-615">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-615">WSL</span></span>
* <span data-ttu-id="fc430-616">DrvFs メタデータのストレージ形式を修正しました [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="fc430-616">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="fc430-617">**重要:** このビルドより前に作成された DrvFs メタデータは、正しく表示されないか、まったく表示されません。</span><span class="sxs-lookup"><span data-stu-id="fc430-617">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="fc430-618">影響を受けるファイルを修正するには、chmod と chown を使用してメタデータを再適用します。</span><span class="sxs-lookup"><span data-stu-id="fc430-618">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="fc430-619">複数のシグナルと再開可能なシステム コールの問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-619">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="fc430-620">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-620">Console</span></span>
* <span data-ttu-id="fc430-621">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-621">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-622">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-622">LTP Results:</span></span>
<span data-ttu-id="fc430-623">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-623">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="fc430-624">ビルド 17063</span><span class="sxs-lookup"><span data-stu-id="fc430-624">Build 17063</span></span>
<span data-ttu-id="fc430-625">ビルド 17063 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-625">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="fc430-626">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-626">WSL</span></span>
* <span data-ttu-id="fc430-627">DrvFs で追加の Linux メタデータがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="fc430-627">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="fc430-628">これにより、chmod/chown を使用してファイルの所有者とモードを設定できるほか、FIFO、UNIX ソケット、デバイス ファイルなどの特殊ファイルを作成することも可能になります。</span><span class="sxs-lookup"><span data-stu-id="fc430-628">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="fc430-629">現時点では、これはまだ試験段階のため、既定では無効になっています。</span><span class="sxs-lookup"><span data-stu-id="fc430-629">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="fc430-630">**注:** DrvFs で使用されるメタデータ形式のバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-630">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="fc430-631">メタデータは実験のためにこのビルドでは機能しますが、今後のビルドでは、このビルドで作成されたメタデータは正しく読み取られません。</span><span class="sxs-lookup"><span data-stu-id="fc430-631">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="fc430-632">変更したファイルの所有者を手動で更新する必要がある場合があり、カスタム デバイス ID を持つデバイスは再作成しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fc430-632">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="fc430-633">有効にするには、メタデータ オプションを使用して DrvFs をマウントします (既存のマウントで有効にするには、最初にマウントを解除する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="fc430-633">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="fc430-634">Linux のアクセス許可は、追加のメタデータとしてファイルに追加されます。Windows のアクセス許可には影響はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-634">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="fc430-635">Windows エディターを使用してファイルを編集すると、メタデータが削除されることがありますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-635">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="fc430-636">この場合、そのファイルは既定のアクセス許可に戻ります。</span><span class="sxs-lookup"><span data-stu-id="fc430-636">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="fc430-637">メタデータなしでファイルを制御するためのマウント オプションを DrvFs に追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-637">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="fc430-638">uid: 全ファイルの所有者に使用されるユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="fc430-638">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="fc430-639">gid: 全ファイルの所有者に使用されるグループ ID。</span><span class="sxs-lookup"><span data-stu-id="fc430-639">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="fc430-640">umask: 全ファイルとディレクトリに対して除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="fc430-640">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="fc430-641">fmask: すべての標準ファイルに対して除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="fc430-641">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="fc430-642">dmask: 全ディレクトリに対して除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="fc430-642">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="fc430-643">たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="fc430-643">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="fc430-644">メタデータ オプションと組み合わせて、メタデータのないファイルに対する既定のアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc430-644">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="fc430-645">WSL と Win32 の間で環境変数がどのように流れるかを構成するために、新しい環境変数 `WSLENV` を導入しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-645">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="fc430-646">たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="fc430-646">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="fc430-647">`WSLENV` は、Win32 から WSL プロセスを起動するとき、または WSL から Win32 プロセスを起動するときに含めることができる環境変数のコロン区切りリストです。</span><span class="sxs-lookup"><span data-stu-id="fc430-647">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="fc430-648">各変数の末尾にはスラッシュを付け、その後に、変換方法を指定するフラグを指定できます。</span><span class="sxs-lookup"><span data-stu-id="fc430-648">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="fc430-649">p:この値は、WSL パスと Win32 パスの間で変換されるパスです。</span><span class="sxs-lookup"><span data-stu-id="fc430-649">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="fc430-650">l:この値は、パスのリストです。</span><span class="sxs-lookup"><span data-stu-id="fc430-650">l: The value is a list of paths.</span></span> <span data-ttu-id="fc430-651">WSL では、コロンで区切られたリストです。</span><span class="sxs-lookup"><span data-stu-id="fc430-651">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="fc430-652">Win32 では、セミコロンで区切られたリストです。</span><span class="sxs-lookup"><span data-stu-id="fc430-652">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="fc430-653">u:この値は、Win32 から WSL を呼び出すときにのみ含める必要があります</span><span class="sxs-lookup"><span data-stu-id="fc430-653">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="fc430-654">w:この値は、WSL から Win32 を呼び出すときにのみ含める必要があります</span><span class="sxs-lookup"><span data-stu-id="fc430-654">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="fc430-655">.bashrc またはユーザーのカスタム Windows 環境で `WSLENV` を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc430-655">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="fc430-656">drvfs マウントは、tar、cp -p からのタイムスタンプを正しく保持します (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="fc430-656">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="fc430-657">drvfs シンボリック リンクは正しいサイズを報告します (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="fc430-657">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="fc430-658">非常に大きい IO サイズに対して読み取り/書き込みが機能します (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="fc430-658">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="fc430-659">waitpid はプロセス グループ ID で機能します (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="fc430-659">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="fc430-660">大きな予約領域での mmap のパフォーマンスが大幅に改善しました。ghc のパフォーマンスが改善します (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="fc430-660">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="fc430-661">READ_IMPLIES_EXEC のパーソナリティ サポート。maxima および clisp を修正します (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="fc430-661">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="fc430-662">mprotect で PROT_GROWSDOWN がサポートされます。clisp を修正します (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="fc430-662">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="fc430-663">オーバーコミット モードでのページ フォールトの修正。sbcl の修正 (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="fc430-663">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="fc430-664">clone でより多くのフラグの組み合わせがサポートされます</span><span class="sxs-lookup"><span data-stu-id="fc430-664">clone supports more flags combinations</span></span>
* <span data-ttu-id="fc430-665">epoll ファイルの select/epoll をサポートします (以前は操作なし)。</span><span class="sxs-lookup"><span data-stu-id="fc430-665">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="fc430-666">未実装のシステム コールの ptrace を通知します。</span><span class="sxs-lookup"><span data-stu-id="fc430-666">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="fc430-667">resolv.conf ネームサーバーを生成しているときに実行されていないインターフェイスを無視します [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="fc430-667">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="fc430-668">物理アドレスのないネットワーク インターフェイスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="fc430-668">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="fc430-669">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="fc430-669">[GH 2685]</span></span>
* <span data-ttu-id="fc430-670">その他のバグ修正と機能強化。</span><span class="sxs-lookup"><span data-stu-id="fc430-670">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="fc430-671">開発者は Windows 上で Linux ツールを利用できるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-671">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="fc430-672">Windows コマンド ライン ツールチェーンに、bsdtar (tar) と curl が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc430-672">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="fc430-673">これらの 2 つの新しいツールの追加に関する詳細と、それを使った Windows での開発者エクスペリエンスの形成については、[こちらのブログ](https://aka.ms/tarcurlwindows)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-673">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they're shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="fc430-674">`AF_UNIX` は、Windows Insider SDK (17061+) で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="fc430-674">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="fc430-675">`AF_UNIX` の詳細と、Windows 上で開発者がそれをどのように使用できるかについては、[こちらのブログ](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)をお読みください。</span><span class="sxs-lookup"><span data-stu-id="fc430-675">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="fc430-676">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-676">Console</span></span>
* <span data-ttu-id="fc430-677">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-677">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-678">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-678">LTP Results:</span></span>
<span data-ttu-id="fc430-679">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-679">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="fc430-680">ビルド 17046</span><span class="sxs-lookup"><span data-stu-id="fc430-680">Build 17046</span></span>

<span data-ttu-id="fc430-681">ビルド 17046 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-681">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="fc430-682">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-682">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-683">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-683">WSL</span></span>
- <span data-ttu-id="fc430-684">アクティブ ターミナルなしでプロセスの実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="fc430-684">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="fc430-685">[GH 709、1007、1511、2252、2391 など]</span><span class="sxs-lookup"><span data-stu-id="fc430-685">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="fc430-686">CLONE_VFORK および CLONE_VM のサポートの強化。</span><span class="sxs-lookup"><span data-stu-id="fc430-686">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="fc430-687">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="fc430-687">[GH 1878, 2615]</span></span>
- <span data-ttu-id="fc430-688">WSL ネットワーク操作で TDI フィルター ドライバーをスキップします。</span><span class="sxs-lookup"><span data-stu-id="fc430-688">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="fc430-689">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="fc430-689">[GH 1554]</span></span>
- <span data-ttu-id="fc430-690">DrvFs は、特定の条件に適合したときに NT シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="fc430-690">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="fc430-691">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="fc430-691">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="fc430-692">リンク対象は、相対パスである必要があり、マウント ポイントやシンボリック リンクと交差してはならず、存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-692">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="fc430-693">開発者モードが有効になっていない場合、ユーザーは SE_CREATE_SYMBOLIC_LINK_PRIVILEGE を持っている必要があります (このためには、通常、管理者特権で wsl.exe を起動する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="fc430-693">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="fc430-694">それ以外の状況でも、DrvFs は WSL シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="fc430-694">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="fc430-695">管理者特権と非管理者特権での WSL インスタンスの同時実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="fc430-695">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="fc430-696">/proc/sys/kernel/yama/ptrace_scope をサポートします</span><span class="sxs-lookup"><span data-stu-id="fc430-696">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="fc430-697">WSL<->Windows のパスの変換を実行するために wslpath を追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-697">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="fc430-698">[GH 522、1243、1834、2327 など]</span><span class="sxs-lookup"><span data-stu-id="fc430-698">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with '/' instead of '\\'

      EX: wslpath 'c:\users'
  ```
  #### <a name="console"></a><span data-ttu-id="fc430-699">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-699">Console</span></span>
- <span data-ttu-id="fc430-700">修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-700">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-701">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-701">LTP Results:</span></span>
<span data-ttu-id="fc430-702">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-702">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="fc430-703">ビルド 17040</span><span class="sxs-lookup"><span data-stu-id="fc430-703">Build 17040</span></span>

<span data-ttu-id="fc430-704">ビルド 17040 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-704">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-705">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-705">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-706">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-706">WSL</span></span>
- <span data-ttu-id="fc430-707">17035 以降修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-707">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-708">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-708">Console</span></span>
- <span data-ttu-id="fc430-709">17035 以降修正なし。</span><span class="sxs-lookup"><span data-stu-id="fc430-709">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-710">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-710">LTP Results:</span></span>
<span data-ttu-id="fc430-711">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-711">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="fc430-712">ビルド 17035</span><span class="sxs-lookup"><span data-stu-id="fc430-712">Build 17035</span></span>

<span data-ttu-id="fc430-713">ビルド 17035 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-713">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-714">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-714">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-715">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-715">WSL</span></span>
- <span data-ttu-id="fc430-716">DrvFs 上のファイルにアクセスすると、時々 EINVAL で失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="fc430-716">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="fc430-717">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="fc430-717">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-718">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-718">Console</span></span>
- <span data-ttu-id="fc430-719">VT モードで行を挿入または削除するときに一部の色が失われます。</span><span class="sxs-lookup"><span data-stu-id="fc430-719">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-720">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-720">LTP Results:</span></span>
<span data-ttu-id="fc430-721">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-721">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="fc430-722">ビルド 17025</span><span class="sxs-lookup"><span data-stu-id="fc430-722">Build 17025</span></span>

<span data-ttu-id="fc430-723">ビルド 17025 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-723">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-724">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-724">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-725">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-725">WSL</span></span>
- <span data-ttu-id="fc430-726">新しいフォアグラウンド プロセス グループで初期プロセスを開始します [GH 1653、2510]。</span><span class="sxs-lookup"><span data-stu-id="fc430-726">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="fc430-727">SIGHUP 配信の修正 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="fc430-727">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="fc430-728">指定されていない場合、既定の仮想ブリッジ名を生成します [GH 2497]。</span><span class="sxs-lookup"><span data-stu-id="fc430-728">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="fc430-729">/proc/sys/kernel/random/boot_id を実装します [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="fc430-729">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="fc430-730">追加の相互運用 stdout/stderr パイプの修正。</span><span class="sxs-lookup"><span data-stu-id="fc430-730">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="fc430-731">syncfs システム コールをスタブします。</span><span class="sxs-lookup"><span data-stu-id="fc430-731">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-732">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-732">Console</span></span>
- <span data-ttu-id="fc430-733">サード パーティ コンソールの入力 VT 変換を修正します [GH 111]</span><span class="sxs-lookup"><span data-stu-id="fc430-733">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-734">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-734">LTP Results:</span></span>
<span data-ttu-id="fc430-735">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-735">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="fc430-736">ビルド 17017</span><span class="sxs-lookup"><span data-stu-id="fc430-736">Build 17017</span></span>

<span data-ttu-id="fc430-737">ビルド 17017 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-737">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-738">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-738">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-739">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-739">WSL</span></span>
- <span data-ttu-id="fc430-740">空の ELF プログラム ヘッダーを無視します [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="fc430-740">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="fc430-741">LxssManager が非対話型ユーザーに対して WSL インスタンスを作成することを許可します (ssh およびスケジュールされたタスクのサポート) [GH 777、1602]。</span><span class="sxs-lookup"><span data-stu-id="fc430-741">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="fc430-742">WSL->Win32-> WSL ("開始") シナリオをサポートします [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="fc430-742">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="fc430-743">相互運用によって起動されたコンソール アプリの終了に対する制限付きサポート [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="fc430-743">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="fc430-744">devpts のマウント オプションをサポートします [GH 1948]。</span><span class="sxs-lookup"><span data-stu-id="fc430-744">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="fc430-745">Ptrace が子のスタートアップをブロックします [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="fc430-745">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="fc430-746">EPOLLET で一部のイベントが欠落します [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="fc430-746">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="fc430-747">PTRACE_GETSIGINFO でより多くのデータが返されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-747">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="fc430-748">lseek を指定した Getdents により、誤った結果が生成されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-748">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="fc430-749">これ以上データがないパイプで入力を待機することによる、いくつかの Win32 相互運用アプリのハングを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-749">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="fc430-750">tty/pty ファイルに対する O_ASYNC サポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-750">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="fc430-751">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-751">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-752">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-752">Console</span></span>
- <span data-ttu-id="fc430-753">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-753">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-754">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-754">LTP Results:</span></span>
<span data-ttu-id="fc430-755">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="fc430-755">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="fc430-756">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="fc430-756">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="fc430-757">ビルド 16288</span><span class="sxs-lookup"><span data-stu-id="fc430-757">Build 16288</span></span>

<span data-ttu-id="fc430-758">ビルド 16288 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-758">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-759">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-759">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-760">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-760">WSL</span></span>
- <span data-ttu-id="fc430-761">ソケット ファイル記述子の uid、gid、およびモードを正しく初期化して報告します [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="fc430-761">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="fc430-762">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-762">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-763">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-763">Console</span></span>
- <span data-ttu-id="fc430-764">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-764">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-765">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-765">LTP Results:</span></span>
<span data-ttu-id="fc430-766">16273 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="fc430-766">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="fc430-767">ビルド 16278</span><span class="sxs-lookup"><span data-stu-id="fc430-767">Build 16278</span></span>

<span data-ttu-id="fc430-768">ビルド 162738 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-768">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-769">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-769">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-770">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-770">WSL</span></span>
- <span data-ttu-id="fc430-771">LX MM 状態を解除するときに、ファイルによってサポートされているセクションのマップされたビューを明示的にマップ解除します [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="fc430-771">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="fc430-772">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-772">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-773">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-773">Console</span></span>
- <span data-ttu-id="fc430-774">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-774">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-775">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-775">LTP Results:</span></span>
<span data-ttu-id="fc430-776">16273 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="fc430-776">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="fc430-777">ビルド 16275</span><span class="sxs-lookup"><span data-stu-id="fc430-777">Build 16275</span></span>

<span data-ttu-id="fc430-778">ビルド 162735 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-778">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-779">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-779">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-780">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-780">WSL</span></span>
- <span data-ttu-id="fc430-781">このリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-781">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-782">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-782">Console</span></span>
- <span data-ttu-id="fc430-783">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-783">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-784">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-784">LTP Results:</span></span>
<span data-ttu-id="fc430-785">16273 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="fc430-785">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="fc430-786">ビルド 16273</span><span class="sxs-lookup"><span data-stu-id="fc430-786">Build 16273</span></span>

<span data-ttu-id="fc430-787">ビルド 16273 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-787">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-788">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-788">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-789">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-789">WSL</span></span>
- <span data-ttu-id="fc430-790">DrvFs がディレクトリに対して間違ったファイルの種類を報告することがあった問題を修正しました [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="fc430-790">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="fc430-791">uevent を使用するプログラムのブロックを解除するために NETLINK_KOBJECT_UEVENT ソケットの作成を許可します [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="fc430-791">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="fc430-792">ノンブロッキング接続のサポートを追加します [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="fc430-792">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="fc430-793">CLONE_FS clone システム コール フラグを実装します [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="fc430-793">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="fc430-794">NT 相互運用でタブや引用符が正しく処理されないことに関する問題を修正します [GH 1625、2164]</span><span class="sxs-lookup"><span data-stu-id="fc430-794">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="fc430-795">WSL インスタンスを再起動しようとしたときにアクセスが拒否されるエラーを解決します [GH 651、2095]</span><span class="sxs-lookup"><span data-stu-id="fc430-795">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="fc430-796">futex の FUTEX_REQUEUE 操作と FUTEX_CMP_REQUEUE 操作を実装します [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="fc430-796">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="fc430-797">さまざまな SysFs ファイルのアクセス許可を修正します [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="fc430-797">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="fc430-798">セットアップ中の Haskell スタックのハングを修正します [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="fc430-798">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="fc430-799">binfmt_misc の 'C'、'O'、および 'P' のフラグを実装します [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="fc430-799">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="fc430-800">/proc/sys/kernel /shmmax /shmmni & /threads-max を追加します [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="fc430-800">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="fc430-801">ioprio_set システム コールの部分的サポートを追加します [GH 498]</span><span class="sxs-lookup"><span data-stu-id="fc430-801">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="fc430-802">SO_REUSEPORT をスタブし、netlink ソケットに対する SO_PASSCRED のサポートを追加します [GH 69]</span><span class="sxs-lookup"><span data-stu-id="fc430-802">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="fc430-803">ディストリビューションを現在インストールまたはアンインストールしている場合に、RegisterDistribuiton から別のエラー コードが返されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-803">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="fc430-804">wslconfig.exe によって部分的にインストールされた WSL ディストリビューションの登録解除を許可します</span><span class="sxs-lookup"><span data-stu-id="fc430-804">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="fc430-805">udp::msg_peek からの python ソケット テストのハングを修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-805">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="fc430-806">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-806">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-807">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-807">Console</span></span>
- <span data-ttu-id="fc430-808">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-808">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-809">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-809">LTP Results:</span></span>
<span data-ttu-id="fc430-810">テストの合計:1904</span><span class="sxs-lookup"><span data-stu-id="fc430-810">Total Tests: 1904</span></span><br/>
<span data-ttu-id="fc430-811">スキップされたテストの合計:209</span><span class="sxs-lookup"><span data-stu-id="fc430-811">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="fc430-812">失敗の合計:229</span><span class="sxs-lookup"><span data-stu-id="fc430-812">Total Failures: 229</span></span><br/>
[<span data-ttu-id="fc430-813">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-813">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="fc430-814">ビルド 16257</span><span class="sxs-lookup"><span data-stu-id="fc430-814">Build 16257</span></span>

<span data-ttu-id="fc430-815">ビルド 16257 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-815">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-816">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-816">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-817">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-817">WSL</span></span>
- <span data-ttu-id="fc430-818">prlimit64 システム コールを実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-818">Implement prlimit64 system call</span></span>
- <span data-ttu-id="fc430-819">ulimit -n (setrlimit RLIMIT_NOFILE) に対するサポートを追加します [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="fc430-819">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="fc430-820">TCP ソケットに対して MSG_MORE をスタブします [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="fc430-820">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="fc430-821">無効な AT_EXECFN 補助ベクトルの動作を修正します [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="fc430-821">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="fc430-822">console/tty のコピー/貼り付けの動作を修正し、改善された完全バッファー処理を追加します [GH 2204、2131]</span><span class="sxs-lookup"><span data-stu-id="fc430-822">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="fc430-823">set-user-ID プログラムと set-group-ID プログラムの補助ベクトルに AT_SECURE を設定します [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="fc430-823">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="fc430-824">疑似ターミナルのマスター エンドポイントが TIOCPGRP を処理しません [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="fc430-824">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="fc430-825">LxFs でのディレクトリの巻き戻しについて lseek を修正します [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="fc430-825">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="fc430-826">高い使用率の後に /dev/ptmx がロックします [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="fc430-826">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="fc430-827">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-827">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-828">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-828">Console</span></span>
- <span data-ttu-id="fc430-829">すべての場所での横線とアンダースコアの修正 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="fc430-829">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="fc430-830">プロセス順序の変更により NPM のクローズが困難になった問題の修正 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="fc430-830">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="fc430-831">新しいカラー スキームを追加しました: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="fc430-831">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-832">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-832">LTP Results:</span></span>
<span data-ttu-id="fc430-833">16251 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="fc430-833">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-834">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-834">Syscall Support</span></span>
<span data-ttu-id="fc430-835">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-835">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-836">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-836">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="fc430-837">の既知の問題</span><span class="sxs-lookup"><span data-stu-id="fc430-837">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>[<span data-ttu-id="fc430-838">GitHub の問題 2392:Windows フォルダーが WSL によって認識されない...</span><span class="sxs-lookup"><span data-stu-id="fc430-838">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="fc430-839">ビルド 16257 で、WSL には、`/mnt/c/...` を介して Windows ファイル/フォルダーを列挙するときに問題があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-839">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="fc430-840">この問題は修正済みであり、2017 年 8 月 14 日から始まる週の間に Insiders ビルドでリリースされます。</span><span class="sxs-lookup"><span data-stu-id="fc430-840">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="fc430-841">ビルド 16251</span><span class="sxs-lookup"><span data-stu-id="fc430-841">Build 16251</span></span>

<span data-ttu-id="fc430-842">ビルド 16251 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-842">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-843">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-843">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-844">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-844">WSL</span></span>
- <span data-ttu-id="fc430-845">WSL のオプション コンポーネントからベータ タグを削除します。詳細については、[ブログ投稿](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-845">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="fc430-846">exec で set-user-ID と set-group-ID のバイナリに対して保存されている set uid と gid を正しく初期化します [GH 962、1415、2072]</span><span class="sxs-lookup"><span data-stu-id="fc430-846">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="fc430-847">ptrace PTRACE_O_TRACEEXIT に対するサポートを追加しました [GH 555]</span><span class="sxs-lookup"><span data-stu-id="fc430-847">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="fc430-848">ptrace PTRACE_GETFPREGS と PTRACE_GETREGSET (NT_FPREGSET を使用) に対するサポートを追加しました [GH 555]</span><span class="sxs-lookup"><span data-stu-id="fc430-848">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="fc430-849">無視されたシグナルでの停止について ptrace を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-849">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="fc430-850">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-850">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-851">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-851">Console</span></span>
- <span data-ttu-id="fc430-852">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-852">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-853">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-853">LTP Results:</span></span>
<span data-ttu-id="fc430-854">合格したテストの数:768</span><span class="sxs-lookup"><span data-stu-id="fc430-854">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="fc430-855">失敗したテストの数:244</span><span class="sxs-lookup"><span data-stu-id="fc430-855">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="fc430-856">スキップされたテストの数:96</span><span class="sxs-lookup"><span data-stu-id="fc430-856">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="fc430-857">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-857">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="fc430-858">ビルド 16241</span><span class="sxs-lookup"><span data-stu-id="fc430-858">Build 16241</span></span>

<span data-ttu-id="fc430-859">ビルド 16241 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-859">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-860">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-860">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="fc430-861">WSL</span><span class="sxs-lookup"><span data-stu-id="fc430-861">WSL</span></span>
- <span data-ttu-id="fc430-862">このリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-862">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="fc430-863">コンソール</span><span class="sxs-lookup"><span data-stu-id="fc430-863">Console</span></span>
- <span data-ttu-id="fc430-864">[こちら](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)で最初に報告された、交差行の DEC に対して誤った文字が出力されることの修正</span><span class="sxs-lookup"><span data-stu-id="fc430-864">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="fc430-865">コード ページ 65001 (utf8) に出力テキストが表示されないことの修正</span><span class="sxs-lookup"><span data-stu-id="fc430-865">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="fc430-866">ある色の RGB 値に対して行われた変更を、選択の変更時にパレットの他の部分に転送しないでください。</span><span class="sxs-lookup"><span data-stu-id="fc430-866">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="fc430-867">これにより、コンソール プロパティ シートがずっと使いやすくなります。</span><span class="sxs-lookup"><span data-stu-id="fc430-867">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="fc430-868">Ctrl+S が正しく機能していないように見えます</span><span class="sxs-lookup"><span data-stu-id="fc430-868">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="fc430-869">Un-Bold/-Dim が ANSI エスケープ コードにまったく存在しません [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="fc430-869">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="fc430-870">コンソールで Vim の色のテーマが正しくサポートされていません [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="fc430-870">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="fc430-871">特定の文字を貼り付けられません [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="fc430-871">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="fc430-872">編集/コマンド ライン上に存在するときに、bash ウィンドウのサイズ変更で、サイズ変更のリフローの操作が正しく行われません [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="fc430-872">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="fc430-873">Ctrl-L を押しても画面はダーティな状態のままです [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="fc430-873">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="fc430-874">HDPI に VT を表示する際のコンソール レンダリングのバグ [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="fc430-874">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="fc430-875">Unicode 文字 U+30FB で日本語の文字が正しく表示されません [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="fc430-875">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="fc430-876">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-876">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="fc430-877">ビルド 16237</span><span class="sxs-lookup"><span data-stu-id="fc430-877">Build 16237</span></span>

<span data-ttu-id="fc430-878">ビルド 16237 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-878">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-879">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-879">Fixed</span></span>
- <span data-ttu-id="fc430-880">LxFs で EA がないファイルには既定の属性を使用します (root、root、0000)</span><span class="sxs-lookup"><span data-stu-id="fc430-880">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="fc430-881">拡張属性を使用するディストリビューションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-881">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="fc430-882">getdents と getdents64 によって返されるエントリのパディングを修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-882">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="fc430-883">shmctl SHM_STAT システム コールのアクセス許可チェックを修正します [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="fc430-883">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="fc430-884">tty の正しくない初期 epoll 状態を修正しました [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="fc430-884">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="fc430-885">DrvFs readdir ですべてのエントリが返されない問題を修正します [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="fc430-885">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="fc430-886">ファイルのリンクが解除されているときの LxFs readdir を修正します [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="fc430-886">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="fc430-887">リンクが解除されている drvfs ファイルを procfs を介して再オープンできるようにします</span><span class="sxs-lookup"><span data-stu-id="fc430-887">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="fc430-888">WSL の機能を無効にするためのグローバル レジストリ キー オーバーライドを追加しました (相互運用/ドライブのマウント)</span><span class="sxs-lookup"><span data-stu-id="fc430-888">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="fc430-889">DrvFs (および LxFs) の "stat" での間違ったブロック カウントを修正します [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="fc430-889">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="fc430-890">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-890">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="fc430-891">ビルド 16232</span><span class="sxs-lookup"><span data-stu-id="fc430-891">Build 16232</span></span>

<span data-ttu-id="fc430-892">ビルド 16232 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-892">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-893">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-893">Fixed</span></span>
- <span data-ttu-id="fc430-894">このリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-894">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="fc430-895">ビルド 16226</span><span class="sxs-lookup"><span data-stu-id="fc430-895">Build 16226</span></span>

<span data-ttu-id="fc430-896">ビルド 16226 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-896">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-897">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-897">Fixed</span></span>
- <span data-ttu-id="fc430-898">xattr に関連したシステム コールのサポート (getxattr、setxattr、listxattr、removexattr)。</span><span class="sxs-lookup"><span data-stu-id="fc430-898">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="fc430-899">security.capablity xattr のサポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-899">security.capablity xattr support.</span></span>
- <span data-ttu-id="fc430-900">特定のファイルシステムとフィルター (MS 以外の SMB サーバーを含む) との互換性を改善しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-900">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="fc430-901">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="fc430-901">[GH #1952]</span></span>
- <span data-ttu-id="fc430-902">OneDrive プレースホルダー、GVFS プレースホルダー、および Compact OS 圧縮ファイルのサポートを強化しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-902">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="fc430-903">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-903">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="fc430-904">ビルド 16215</span><span class="sxs-lookup"><span data-stu-id="fc430-904">Build 16215</span></span>

<span data-ttu-id="fc430-905">ビルド 16215 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-905">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-906">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-906">Fixed</span></span>
- <span data-ttu-id="fc430-907">WSL で開発者モードが不要になりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-907">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="fc430-908">drvfs でディレクトリ ジャンクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc430-908">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="fc430-909">WSL ディストリビューション appx パッケージのアンインストールを処理します。</span><span class="sxs-lookup"><span data-stu-id="fc430-909">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="fc430-910">プライベート マッピングと共有マッピングを表示するように procfs を更新します。</span><span class="sxs-lookup"><span data-stu-id="fc430-910">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="fc430-911">部分的にインストールまたはアンインストールされたディストリビューションをクリーンアップする wslconfig.exe の機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-911">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="fc430-912">TCP ソケットに対する IP_MTU_DISCOVER のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-912">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="fc430-913">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="fc430-913">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="fc430-914">AF_INADDR へのルート用のプロトコル ファミリを推測します。</span><span class="sxs-lookup"><span data-stu-id="fc430-914">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="fc430-915">シリアル デバイスの機能強化 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="fc430-915">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="fc430-916">ビルド 16199</span><span class="sxs-lookup"><span data-stu-id="fc430-916">Build 16199</span></span>

<span data-ttu-id="fc430-917">ビルド 16199 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-917">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-918">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-918">Fixed</span></span>
- <span data-ttu-id="fc430-919">これらのリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-919">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="fc430-920">ビルド 16193</span><span class="sxs-lookup"><span data-stu-id="fc430-920">Build 16193</span></span>

<span data-ttu-id="fc430-921">ビルド 16193 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-921">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-922">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-922">Fixed</span></span>
- <span data-ttu-id="fc430-923">SIGCONT の送信と threadgroup の終了との間の競合状態 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="fc430-923">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="fc430-924">FILE_DEVICE_CONSOLE ではなく FILE_DEVICE_NAMED_PIPE を報告するように tty デバイスと pty デバイスを変更します [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="fc430-924">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="fc430-925">IP_OPTIONS の SSH 修正</span><span class="sxs-lookup"><span data-stu-id="fc430-925">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="fc430-926">DrvFs のマウントを init デーモンに移動しました [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="fc430-926">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="fc430-927">後続の NT シンボリック リンクに対するサポートを DrvFs に追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-927">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="fc430-928">ビルド 16184</span><span class="sxs-lookup"><span data-stu-id="fc430-928">Build 16184</span></span>

<span data-ttu-id="fc430-929">ビルド 16184 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-929">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-930">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-930">Fixed</span></span>
- <span data-ttu-id="fc430-931">apt パッケージのメンテナンス タスク (lxrun.exe/update) を削除しました</span><span class="sxs-lookup"><span data-stu-id="fc430-931">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="fc430-932">Node.js の Windows プロセスから出力が表示されない問題を修正しました [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="fc430-932">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="fc430-933">lxcore での配置要件を緩和します [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="fc430-933">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="fc430-934">複数のシステム コールで AT_EMPTY_PATH フラグの処理を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-934">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="fc430-935">開いているハンドルがある DrvFs ファイルを削除するとファイルで未定義の動作が示される問題を修正しました [GH 544、966、1357、1535、1615]</span><span class="sxs-lookup"><span data-stu-id="fc430-935">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="fc430-936">/etc/hosts は、Windows hosts ファイルからエントリを継承するようになりました (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="fc430-936">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="fc430-937">ビルド 16179</span><span class="sxs-lookup"><span data-stu-id="fc430-937">Build 16179</span></span>

<span data-ttu-id="fc430-938">ビルド 16179 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-938">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-939">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-939">Fixed</span></span>
- <span data-ttu-id="fc430-940">今週は、WSL の変更はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-940">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="fc430-941">ビルド 16176</span><span class="sxs-lookup"><span data-stu-id="fc430-941">Build 16176</span></span>

<span data-ttu-id="fc430-942">ビルド 16176 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-942">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-943">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-943">Fixed</span></span>

- [<span data-ttu-id="fc430-944">シリアル サポートを有効にしました</span><span class="sxs-lookup"><span data-stu-id="fc430-944">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="fc430-945">IP ソケット オプション IP_OPTIONS を追加しました [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="fc430-945">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="fc430-946">(nginx/PHP-FPM にファイルをアップロード中に) pwritev 関数を実装しました [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="fc430-946">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="fc430-947">IP ソケット オプション IP_MULTICAST_IF および IPV6_MULTICAST_IF を追加しました [GH 990]</span><span class="sxs-lookup"><span data-stu-id="fc430-947">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="fc430-948">ソケット オプション IP_MULTICAST_LOOP および IPV6_MULTICAST_LOOP に対するサポート [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="fc430-948">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="fc430-949">apps node、traceroute、dig、nslookup、host に対する IP(V6)_MTU ソケット オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-949">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="fc430-950">IP ソケット オプション IPV6_UNICAST_HOPS を追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-950">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="fc430-951">ファイルシステムの機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-951">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="fc430-952">UNC パスのマウントを許可します</span><span class="sxs-lookup"><span data-stu-id="fc430-952">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="fc430-953">drvfs で CDFS のサポートを有効にします</span><span class="sxs-lookup"><span data-stu-id="fc430-953">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="fc430-954">drvfs でネットワーク ファイル システムのアクセス許可を正しく処理します</span><span class="sxs-lookup"><span data-stu-id="fc430-954">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="fc430-955">drvfs へのリモート ドライブのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="fc430-955">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="fc430-956">drvfs で FAT のサポートを有効にします</span><span class="sxs-lookup"><span data-stu-id="fc430-956">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="fc430-957">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-957">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-958">LTP の結果</span><span class="sxs-lookup"><span data-stu-id="fc430-958">LTP Results</span></span>
<span data-ttu-id="fc430-959">15042 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="fc430-959">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="fc430-960">ビルド 16170</span><span class="sxs-lookup"><span data-stu-id="fc430-960">Build 16170</span></span>

<span data-ttu-id="fc430-961">ビルド 16170 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-961">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="fc430-962">WSL のテストに関する取り組みを説明する新しい[ブログ投稿](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)をリリースしました。</span><span class="sxs-lookup"><span data-stu-id="fc430-962">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="fc430-963">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-963">Fixed</span></span>

- <span data-ttu-id="fc430-964">ソケット オプション IP_ADD_MEMBERSHIP および IPV6_ADD_MEMBERSHIP をサポートします [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="fc430-964">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="fc430-965">PTRACE_OLDSETOPTIONS のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-965">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="fc430-966">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="fc430-966">[GH 1692]</span></span>
- <span data-ttu-id="fc430-967">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-967">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-968">LTP の結果</span><span class="sxs-lookup"><span data-stu-id="fc430-968">LTP Results</span></span>
<span data-ttu-id="fc430-969">15042 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="fc430-969">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="fc430-970">ビルド 15046 から Windows 10 Creators Update まで</span><span class="sxs-lookup"><span data-stu-id="fc430-970">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="fc430-971">Windows 10 の Creators Update への組み込みが予定されている WSL の修正または機能はこれ以上ありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-971">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="fc430-972">WSL のリリース ノートは、次回の主要な Windows Update をターゲットとする追加に向けて、今後数週間のうちに再開されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-972">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="fc430-973">ビルド 15046 の一般的な Windows 情報および今後の Insider リリースについては、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-973">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="fc430-974">ビルド 15042</span><span class="sxs-lookup"><span data-stu-id="fc430-974">Build 15042</span></span>

<span data-ttu-id="fc430-975">ビルド 15042 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-975">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-976">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-976">Fixed</span></span>

- <span data-ttu-id="fc430-977">".." で終わるパスを削除する際のデッドロックの修正</span><span class="sxs-lookup"><span data-stu-id="fc430-977">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="fc430-978">FIONBIO が成功時に 0 を返さないという問題を修正しました [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="fc430-978">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="fc430-979">inet データグラム ソケットの長さゼロの読み取りの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-979">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="fc430-980">drvfs inode 参照での競合状態が原因で発生する可能性があるデッドロックを修正します [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="fc430-980">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="fc430-981">UNIX ソケット補助データに対する拡張サポート、SCM_CREDENTIALS および SCM_RIGHTS [GH 514、613、1326]</span><span class="sxs-lookup"><span data-stu-id="fc430-981">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="fc430-982">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-982">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-983">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-983">LTP Results:</span></span>
<span data-ttu-id="fc430-984">合格したテストの数:737</span><span class="sxs-lookup"><span data-stu-id="fc430-984">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="fc430-985">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="fc430-985">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="fc430-986">ビルド 15031</span><span class="sxs-lookup"><span data-stu-id="fc430-986">Build 15031</span></span>

<span data-ttu-id="fc430-987">ビルド 15031 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-987">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-988">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-988">Fixed</span></span>

- <span data-ttu-id="fc430-989">time(2) が散発的に不適切な動作をするバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-989">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="fc430-990">\*SIGPROCMASK システム コールによってシグナル マスクが破損する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-990">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="fc430-991">WSL プロセス作成通知で完全な長さのコマンド ラインが返されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-991">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="fc430-992">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="fc430-992">[GH 1632]</span></span>
- <span data-ttu-id="fc430-993">WSL は、GDB のハングについて ptrace を介してスレッドの終了を報告するようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-993">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="fc430-994">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="fc430-994">[GH 1196]</span></span>
- <span data-ttu-id="fc430-995">tmux の IO が大量に行われた後に ptys がハングするバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-995">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="fc430-996">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="fc430-996">[GH 1358]</span></span>
- <span data-ttu-id="fc430-997">複数のシステム コール (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create) でタイムアウトの検証を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-997">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="fc430-998">eventfd EFD_SEMAPHORE のサポートを追加しました [GH 452]</span><span class="sxs-lookup"><span data-stu-id="fc430-998">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="fc430-999">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-999">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1000">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1000">LTP Results:</span></span>
<span data-ttu-id="fc430-1001">合格したテストの数:737</span><span class="sxs-lookup"><span data-stu-id="fc430-1001">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="fc430-1002">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="fc430-1002">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc430-1003">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1003">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="fc430-1004">ビルド 15025</span><span class="sxs-lookup"><span data-stu-id="fc430-1004">Build 15025</span></span>

<span data-ttu-id="fc430-1005">ビルド 15025 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1005">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1006">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1006">Fixed</span></span>

- <span data-ttu-id="fc430-1007">grep 2.27 を破損したバグの修正 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="fc430-1007">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="fc430-1008">eventfd2 システム コールに対して EFD_SEMAPHORE フラグを実装しました [GH 452]</span><span class="sxs-lookup"><span data-stu-id="fc430-1008">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="fc430-1009">/proc/[pid]/net/ipv6_route を実装しました [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="fc430-1009">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="fc430-1010">Unix ストリーム ソケットに対するシグナル駆動型 IO のサポート [GH 393、68]</span><span class="sxs-lookup"><span data-stu-id="fc430-1010">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="fc430-1011">F_GETPIPE_SZ および F_SETPIPE_SZ をサポートします [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="fc430-1011">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="fc430-1012">recvmmsg() システム コールを実装します [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="fc430-1012">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="fc430-1013">epoll_wait() が待機していなかったというバグを修正しました [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="fc430-1013">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="fc430-1014">/proc/version_signature を実装</span><span class="sxs-lookup"><span data-stu-id="fc430-1014">Implement /proc/version_signature</span></span>
- <span data-ttu-id="fc430-1015">Tee システム コールは、両方のファイル記述子が同じパイプを参照している場合にエラーを返すようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1015">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="fc430-1016">UNIX ソケットに対する SO_PEERCRED の正しい動作を実装しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1016">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="fc430-1017">tkill システム コールの無効なパラメーター処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1017">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="fc430-1018">drvfs のパフォーマンスを向上させるための変更</span><span class="sxs-lookup"><span data-stu-id="fc430-1018">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="fc430-1019">Ruby の IO ブロックに対する軽微な修正</span><span class="sxs-lookup"><span data-stu-id="fc430-1019">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="fc430-1020">inet ソケットの MSG_DONTWAIT フラグに対して recvmsg() が EINVAL を返すという問題を修正しました [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="fc430-1020">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="fc430-1021">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1021">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1022">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1022">LTP Results:</span></span>
<span data-ttu-id="fc430-1023">合格したテストの数:732</span><span class="sxs-lookup"><span data-stu-id="fc430-1023">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="fc430-1024">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="fc430-1024">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc430-1025">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1025">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="fc430-1026">ビルド 15019</span><span class="sxs-lookup"><span data-stu-id="fc430-1026">Build 15019</span></span>

<span data-ttu-id="fc430-1027">ビルド 15019 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1027">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1028">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1028">Fixed</span></span>

- <span data-ttu-id="fc430-1029">htop などのツールに対して procfs で CPU 使用量が誤って報告されるバグを修正しました (GH 823、945、971)</span><span class="sxs-lookup"><span data-stu-id="fc430-1029">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="fc430-1030">既存のファイルに対して O_TRUNC を使用して open () を呼び出すと、inotify は IN_OPEN の前に IN_MODIFY を生成するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1030">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="fc430-1031">Postgress を有効にするための UNIX ソケット getsockopt SO_ERROR に対する修正 [GH 61、1354]</span><span class="sxs-lookup"><span data-stu-id="fc430-1031">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="fc430-1032">GO 言語に対して /proc/sys/net/core/somaxconn を実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-1032">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="fc430-1033">Apt-get パッケージ更新のバックグラウンド タスクは、非表示で実行されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1033">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="fc430-1034">ipv6 localhost のスコープをクリアします (Spring-Framework(Java) エラー)。</span><span class="sxs-lookup"><span data-stu-id="fc430-1034">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="fc430-1035">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1035">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1036">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1036">LTP Results:</span></span>
<span data-ttu-id="fc430-1037">合格したテストの数:714</span><span class="sxs-lookup"><span data-stu-id="fc430-1037">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="fc430-1038">不合格の数 (失敗した、スキップしたなど):249</span><span class="sxs-lookup"><span data-stu-id="fc430-1038">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="fc430-1039">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1039">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="fc430-1040">ビルド 15014</span><span class="sxs-lookup"><span data-stu-id="fc430-1040">Build 15014</span></span>

<span data-ttu-id="fc430-1041">ビルド 15014 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1041">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1042">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1042">Fixed</span></span>

- <span data-ttu-id="fc430-1043">Ctrl+C は意図したとおりに動作するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1043">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="fc430-1044">htop と ps auxw は正しいリソース使用量を表示するようになりました (GH #516)</span><span class="sxs-lookup"><span data-stu-id="fc430-1044">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="fc430-1045">NT 例外からシグナルへの基本的な変換。</span><span class="sxs-lookup"><span data-stu-id="fc430-1045">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="fc430-1046">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="fc430-1046">(GH #513)</span></span>
- <span data-ttu-id="fc430-1047">fallocate は、領域が不足しているときに、EINVAL ではなく ENOSPC で失敗するようになりました (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="fc430-1047">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="fc430-1048">/proc/sys/kernel/sem を追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1048">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="fc430-1049">semop システム コールと semtimedop システム コールを実装しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1049">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="fc430-1050">IP_RECVTOS および IPV6_RECVTCLASS ソケット オプションでの nslookup エラーを修正しました (GH 69)</span><span class="sxs-lookup"><span data-stu-id="fc430-1050">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="fc430-1051">ソケット オプション IP_RECVTTL および IPV6_RECVHOPLIMIT に対するサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1051">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="fc430-1052">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1052">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1053">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1053">LTP Results:</span></span>
<span data-ttu-id="fc430-1054">合格したテストの数:709</span><span class="sxs-lookup"><span data-stu-id="fc430-1054">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="fc430-1055">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="fc430-1055">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc430-1056">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1056">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="fc430-1057">システム コールの概要</span><span class="sxs-lookup"><span data-stu-id="fc430-1057">Syscall Summary</span></span>
<span data-ttu-id="fc430-1058">システム コールの合計:384</span><span class="sxs-lookup"><span data-stu-id="fc430-1058">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="fc430-1059">実装の合計:235</span><span class="sxs-lookup"><span data-stu-id="fc430-1059">Total Implemented: 235</span></span> </br>
<span data-ttu-id="fc430-1060">スタブの合計:22</span><span class="sxs-lookup"><span data-stu-id="fc430-1060">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="fc430-1061">未実装の合計:127</span><span class="sxs-lookup"><span data-stu-id="fc430-1061">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="fc430-1062">詳細な内訳</span><span class="sxs-lookup"><span data-stu-id="fc430-1062">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="fc430-1063">ビルド 15007</span><span class="sxs-lookup"><span data-stu-id="fc430-1063">Build 15007</span></span>

<span data-ttu-id="fc430-1064">ビルド 15007 の一般的な Windows 情報については、[Windows ブログ]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1064">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="fc430-1065">既知の問題</span><span class="sxs-lookup"><span data-stu-id="fc430-1065">Known Issue</span></span>

- <span data-ttu-id="fc430-1066">コンソールが一部の Ctrl + <key> 入力を認識しないという既知のバグがあります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1066">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="fc430-1067">これには、通常の "c" キーが押されたものとして機能する ctrl-c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1067">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="fc430-1068">対応策 :代替キーを Ctrl+C にマップします。</span><span class="sxs-lookup"><span data-stu-id="fc430-1068">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="fc430-1069">たとえば、Ctrl+K を Ctrl+C にマップするには、`stty intr \^k` を実行します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1069">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="fc430-1070">このマッピングはターミナルごとに行い、*毎回* bash が起動されるたびに実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1070">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="fc430-1071">ユーザーはオプションを探索し、これを `.bashrc` に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1071">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="fc430-1072">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1072">Fixed</span></span>

- <span data-ttu-id="fc430-1073">実行中の WSL が CPU コアの 100% を消費するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1073">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="fc430-1074">ソケット オプション IP_PKTINFO、IPV6_RECVPKTINFO がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1074">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="fc430-1075">(GH #851、987)</span><span class="sxs-lookup"><span data-stu-id="fc430-1075">(GH #851, 987)</span></span>
- <span data-ttu-id="fc430-1076">lxcore でネットワーク インターフェイスの物理アドレスが 16 バイトに切り捨てられます (GH #1452、1414、1343、468、308)</span><span class="sxs-lookup"><span data-stu-id="fc430-1076">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="fc430-1077">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1077">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1078">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1078">LTP Results:</span></span>
<span data-ttu-id="fc430-1079">合格したテストの数:709</span><span class="sxs-lookup"><span data-stu-id="fc430-1079">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="fc430-1080">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="fc430-1080">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="fc430-1081">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1081">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="fc430-1082">ビルド 15002</span><span class="sxs-lookup"><span data-stu-id="fc430-1082">Build 15002</span></span>

<span data-ttu-id="fc430-1083">ビルド 15002 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1083">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="fc430-1084">既知の問題</span><span class="sxs-lookup"><span data-stu-id="fc430-1084">Known Issue</span></span>

<span data-ttu-id="fc430-1085">2 つの既知の問題:</span><span class="sxs-lookup"><span data-stu-id="fc430-1085">Two known issues:</span></span>
- <span data-ttu-id="fc430-1086">コンソールが一部の Ctrl + <key> 入力を認識しないという既知のバグがあります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1086">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="fc430-1087">これには、通常の "c" キーが押されたものとして機能する ctrl-c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1087">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="fc430-1088">対応策 :代替キーを Ctrl+C にマップします。</span><span class="sxs-lookup"><span data-stu-id="fc430-1088">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="fc430-1089">たとえば、Ctrl+K を Ctrl+C にマップするには、`stty intr \^k` を実行します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1089">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="fc430-1090">このマッピングはターミナルごとに行い、*毎回* bash が起動されるたびに実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1090">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="fc430-1091">ユーザーはオプションを探索し、これを `.bashrc` に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1091">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="fc430-1092">WSL が実行されている間、システム スレッドは CPU コアの 100% を消費します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1092">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="fc430-1093">根本原因は、内部で対処されて修正されています。</span><span class="sxs-lookup"><span data-stu-id="fc430-1093">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="fc430-1094">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1094">Fixed</span></span>

- <span data-ttu-id="fc430-1095">すべての bash セッションは、同じアクセス許可レベルで作成することが必要になりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1095">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="fc430-1096">別のレベルでセッションを開始しようとすると、ブロックされます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1096">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="fc430-1097">つまり、管理コンソールと非管理コンソールを同時に実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1097">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="fc430-1098">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="fc430-1098">(GH #626)</span></span>
<br/>
- <span data-ttu-id="fc430-1099">次の NETLINK_ROUTE メッセージを実装しました (Windows 管理者が必要)</span><span class="sxs-lookup"><span data-stu-id="fc430-1099">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="fc430-1100">RTM_NEWADDR (`ip addr add` をサポート)</span><span class="sxs-lookup"><span data-stu-id="fc430-1100">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="fc430-1101">RTM_NEWROUTE (`ip route add` をサポート)</span><span class="sxs-lookup"><span data-stu-id="fc430-1101">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="fc430-1102">RTM_DELADDR (`ip addr del` をサポート)</span><span class="sxs-lookup"><span data-stu-id="fc430-1102">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="fc430-1103">RTM_DELROUTE (`ip route del` をサポート)</span><span class="sxs-lookup"><span data-stu-id="fc430-1103">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="fc430-1104">更新するパッケージについてのスケジュールされたタスク チェックは、従量課金接続では実行されなくなります (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="fc430-1104">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="fc430-1105">次のようにパイプがスタックするエラーを修正しました。bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="fc430-1105">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="fc430-1106">TCP_KEEPCNT ソケット オプションを実装しました (GH #843)</span><span class="sxs-lookup"><span data-stu-id="fc430-1106">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="fc430-1107">IP_MTU_DISCOVER INET ソケット オプションを実装しました (GH #720、717、170、69)</span><span class="sxs-lookup"><span data-stu-id="fc430-1107">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="fc430-1108">NT パス参照を使用して init から NT バイナリを実行する従来の機能を削除しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1108">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="fc430-1109">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="fc430-1109">(GH #1325)</span></span>
- <span data-ttu-id="fc430-1110">グループ/その他の読み取りアクセスを許可するように /dev/kmsg のモードを修正します (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="fc430-1110">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="fc430-1111">/proc/sys/kernel/random/uuid を実装しました (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="fc430-1111">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="fc430-1112">プロセスの開始時刻が 2432 年と表示されていたエラーを修正しました (GH #974)</span><span class="sxs-lookup"><span data-stu-id="fc430-1112">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="fc430-1113">既定の TERM 環境変数を xterm-256color に切り替えました (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="fc430-1113">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="fc430-1114">プロセスのフォーク中のプロセス コミットの計算方法を変更しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1114">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="fc430-1115">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="fc430-1115">(GH #1286)</span></span>
- <span data-ttu-id="fc430-1116">/proc/sys/vm/overcommit_memory を実装しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1116">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="fc430-1117">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="fc430-1117">(GH #1286)</span></span>
- <span data-ttu-id="fc430-1118">/proc/net/route ファイルを実装しました (GH #69)</span><span class="sxs-lookup"><span data-stu-id="fc430-1118">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="fc430-1119">ショートカット名が誤ってローカライズされるエラーを修正しました (GH #696)</span><span class="sxs-lookup"><span data-stu-id="fc430-1119">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="fc430-1120">プログラム ヘッダーが PATH_MAX 以下でなければならないことを誤って検証をしている elf 解析ロジックを修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1120">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="fc430-1121">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="fc430-1121">(GH #1048)</span></span>
- <span data-ttu-id="fc430-1122">procfs、sysfs、cgroupfs、および binfmtfs に対する statfs コールバックを実装しました (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="fc430-1122">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="fc430-1123">閉じない AptPackageIndexUpdate ウィンドウを修正しました (GH #1184、さらに GH #1193 でも説明)</span><span class="sxs-lookup"><span data-stu-id="fc430-1123">Fixed AptPackageIndexUpdate windows that won't close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="fc430-1124">ASLR パーソナリティ ADDR_NO_RANDOMIZE のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1124">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="fc430-1125">(GH #1148、1128)</span><span class="sxs-lookup"><span data-stu-id="fc430-1125">(GH #1148, 1128)</span></span>
- <span data-ttu-id="fc430-1126">AV 中の適切な gdb スタック トレースのために PTRACE_GETSIGINFO、SIGSEGV を改善しました (GH #875)</span><span class="sxs-lookup"><span data-stu-id="fc430-1126">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="fc430-1127">patchelf バイナリに対する Elf の解析は失敗しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1127">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="fc430-1128">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="fc430-1128">(GH #471)</span></span>
- <span data-ttu-id="fc430-1129">/etc/resolv.conf に伝搬される VPN DNS (GH #416、1350)</span><span class="sxs-lookup"><span data-stu-id="fc430-1129">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="fc430-1130">より信頼性の高いデータ転送のための TCP クローズに対する機能強化。</span><span class="sxs-lookup"><span data-stu-id="fc430-1130">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="fc430-1131">(GH #610、616、1025、1335)</span><span class="sxs-lookup"><span data-stu-id="fc430-1131">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="fc430-1132">開いているファイルの数が多すぎるときに適切なエラー コードが返されるようになりました (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="fc430-1132">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="fc430-1133">(GH #1126、2090)</span><span class="sxs-lookup"><span data-stu-id="fc430-1133">(GH #1126, 2090)</span></span>
- <span data-ttu-id="fc430-1134">Windows の監査ログは、プロセス作成の監査でイメージ名を報告するようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1134">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="fc430-1135">bash ウィンドウ内から bash.exe を起動すると、正常に失敗するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1135">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="fc430-1136">相互運用が LxFs の作業ディレクトリにアクセスできないときのエラー メッセージを追加しました (例: notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="fc430-1136">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="fc430-1137">Windows のパスが WSL で切り捨てられていた問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1137">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="fc430-1138">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1138">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1139">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1139">LTP Results:</span></span>
<span data-ttu-id="fc430-1140">合格したテストの数:690</span><span class="sxs-lookup"><span data-stu-id="fc430-1140">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="fc430-1141">不合格の数 (失敗した、スキップしたなど):274</span><span class="sxs-lookup"><span data-stu-id="fc430-1141">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="fc430-1142">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1142">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1143">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1143">Syscall Support</span></span>
<span data-ttu-id="fc430-1144">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1144">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1145">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1145">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="fc430-1146">ビルド 14986</span><span class="sxs-lookup"><span data-stu-id="fc430-1146">Build 14986</span></span>

<span data-ttu-id="fc430-1147">ビルド 14986 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1147">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1148">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1148">Fixed</span></span>

- <span data-ttu-id="fc430-1149">Netlink および Pty の IOCTL でのバグチェックを修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1149">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="fc430-1150">カーネルのバージョンは、Xenial との一貫性のために 4.4.0-43 を報告するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1150">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="fc430-1151">入力が 'nul:' に向けられたときに Bash.exe が起動するようになりました (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="fc430-1151">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="fc430-1152">スレッド ID が procfs で正しく報告されるようになりました (GH #967)</span><span class="sxs-lookup"><span data-stu-id="fc430-1152">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="fc430-1153">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR のフラグが inotify_add_watch() でサポートされるようになりました (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="fc430-1153">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="fc430-1154">timer_create システム コールおよび関連するシステム コールを実装します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1154">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="fc430-1155">これにより GHC サポートが有効になります (GH #307)</span><span class="sxs-lookup"><span data-stu-id="fc430-1155">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="fc430-1156">Ping で 0.000 ミリ秒の時間が返される問題を修正しました (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="fc430-1156">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="fc430-1157">開いているファイルの数が多すぎるときに適切なエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1157">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="fc430-1158">インターフェイスのハードウェア アドレスが 32 バイトの場合 (Teredo インターフェイスなど) に、Netlink のネットワーク インターフェイス データの要求が EINVAL で失敗する WSL の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1158">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="fc430-1159">Linux の "ip" ユーティリティには、WSL が 32 バイトのハードウェア アドレスを報告した場合にクラッシュするバグが含まれていることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1159">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="fc430-1160">これは、WSL ではなく、"ip" のバグです。</span><span class="sxs-lookup"><span data-stu-id="fc430-1160">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="fc430-1161">"ip" ユーティリティは、ハードウェア アドレスの出力に使用される文字列バッファーの長さをハードコーディングしますが、そのバッファーは 32 バイトのハードウェア アドレスを出力するには小さすぎます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1161">The "ip" utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="fc430-1162">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1162">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1163">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1163">LTP Results:</span></span>
<span data-ttu-id="fc430-1164">合格したテストの数:669</span><span class="sxs-lookup"><span data-stu-id="fc430-1164">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="fc430-1165">不合格の数 (失敗した、スキップしたなど):258</span><span class="sxs-lookup"><span data-stu-id="fc430-1165">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="fc430-1166">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1166">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1167">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1167">Syscall Support</span></span>
<span data-ttu-id="fc430-1168">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1168">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1169">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1169">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="fc430-1170">ビルド 14971</span><span class="sxs-lookup"><span data-stu-id="fc430-1170">Build 14971</span></span>

<span data-ttu-id="fc430-1171">ビルド 14971 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1171">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1172">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1172">Fixed</span></span>

 - <span data-ttu-id="fc430-1173">Microsoft の制御を超える状況により、Windows Subsystem for Linux のこのビルドには更新はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1173">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="fc430-1174">定期的にスケジュールされた更新は、次のリリースから再開されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1174">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1175">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1175">LTP Results:</span></span>
<span data-ttu-id="fc430-1176">14965 から変更されていません</span><span class="sxs-lookup"><span data-stu-id="fc430-1176">Unchanged from 14965</span></span> </br>
<span data-ttu-id="fc430-1177">合格したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="fc430-1177">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="fc430-1178">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="fc430-1178">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc430-1179">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1179">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="fc430-1180">ビルド 14965</span><span class="sxs-lookup"><span data-stu-id="fc430-1180">Build 14965</span></span>

<span data-ttu-id="fc430-1181">ビルド 14965 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1181">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1182">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1182">Fixed</span></span>

- <span data-ttu-id="fc430-1183">Netlink ソケット NETLINK_ROUTE プロトコルの RTM_GETLINK と RTM_GETADDR に対するサポート (GH #468)</span><span class="sxs-lookup"><span data-stu-id="fc430-1183">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="fc430-1184">ネットワークの列挙に対して ifconfig コマンドと ip コマンドを有効にします</span><span class="sxs-lookup"><span data-stu-id="fc430-1184">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="fc430-1185">詳細については、[WSL ネットワークに関するブログ投稿](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1185">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="fc430-1186">/sbin は、既定でユーザーのパスに含まれるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1186">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="fc430-1187">NT ユーザー パスが既定で WSL パスに追加されるようになりました (つまり、Linux パスに System32 を追加せずに notepad.exe を入力できるようになりました)</span><span class="sxs-lookup"><span data-stu-id="fc430-1187">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="fc430-1188">/proc/sys/kernel/cap_last_cap のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1188">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="fc430-1189">現在の作業ディレクトリに ANSI 以外の文字が含まれている場合、WSL から NT バイナリを起動できるようになりました (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="fc430-1189">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="fc430-1190">切断された UNIX ストリーム ソケットでのシャットダウンを許可します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1190">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="fc430-1191">PR_GET_PDEATHSIG のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1191">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="fc430-1192">CLONE_PARENT のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1192">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="fc430-1193">次のようにパイプがスタックするエラーを修正しました。bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="fc430-1193">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="fc430-1194">現在のターミナルに接続する要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1194">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="fc430-1195">/proc/<pid>/oom_score_adj を書き込み可能としてマークします。</span><span class="sxs-lookup"><span data-stu-id="fc430-1195">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="fc430-1196">/sys/fs/cgroup フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1196">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="fc430-1197">sched_setaffinity は、アフィニティ ビット マスクの数を返します</span><span class="sxs-lookup"><span data-stu-id="fc430-1197">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="fc430-1198">インタープリター パスの長さが 64 文字未満でなければならないことを誤って想定している ELF 検証ロジックを修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1198">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="fc430-1199">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="fc430-1199">(GH #743)</span></span>
- <span data-ttu-id="fc430-1200">オープン ファイル記述子により、コンソール ウィンドウが開いたままになることがあります (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="fc430-1200">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="fc430-1201">rename() がターゲット名の末尾スラッシュで失敗したエラーを修正しました (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="fc430-1201">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="fc430-1202">/proc/net/dev ファイルを実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-1202">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="fc430-1203">タイマー精度が原因の 0.000 ミリ秒の Ping を修正します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1203">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="fc430-1204">/proc/self/environ を実装しました (GH #730)</span><span class="sxs-lookup"><span data-stu-id="fc430-1204">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="fc430-1205">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1205">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1206">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1206">LTP Results:</span></span>
<span data-ttu-id="fc430-1207">合格したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="fc430-1207">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="fc430-1208">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="fc430-1208">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc430-1209">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1209">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="fc430-1210">ビルド 14959</span><span class="sxs-lookup"><span data-stu-id="fc430-1210">Build 14959</span></span>

<span data-ttu-id="fc430-1211">ビルド 14959 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1211">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1212">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1212">Fixed</span></span>

- <span data-ttu-id="fc430-1213">Windows の Pico プロセス通知を改善しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1213">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="fc430-1214">[WSL ブログ](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)に追加情報があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1214">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="fc430-1215">Windows の相互運用性での安定性を向上させました</span><span class="sxs-lookup"><span data-stu-id="fc430-1215">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="fc430-1216">エンタープライズ データ保護 (EDP) が有効になっているときに bash.exe を起動すると発生するエラー 0x80070057 を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1216">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="fc430-1217">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1217">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1218">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1218">LTP Results:</span></span>
<span data-ttu-id="fc430-1219">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="fc430-1219">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc430-1220">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="fc430-1220">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc430-1221">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1221">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="fc430-1222">ビルド 14955</span><span class="sxs-lookup"><span data-stu-id="fc430-1222">Build 14955</span></span>

<span data-ttu-id="fc430-1223">ビルド 14955 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1223">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1224">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1224">Fixed</span></span>

 - <span data-ttu-id="fc430-1225">Microsoft の制御を超える状況により、Windows Subsystem for Linux のこのビルドには更新はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1225">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="fc430-1226">定期的にスケジュールされた更新は、次のリリースから再開されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1226">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1227">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1227">LTP Results:</span></span>
<span data-ttu-id="fc430-1228">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="fc430-1228">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc430-1229">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="fc430-1229">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc430-1230">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1230">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="fc430-1231">ビルド 14951</span><span class="sxs-lookup"><span data-stu-id="fc430-1231">Build 14951</span></span>

<span data-ttu-id="fc430-1232">ビルド 14951 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1232">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="fc430-1233">新機能:Windows/Ubuntu の相互運用性</span><span class="sxs-lookup"><span data-stu-id="fc430-1233">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="fc430-1234">Windows バイナリを WSL コマンド ラインから直接呼び出せるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1234">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="fc430-1235">これによりユーザーは、今まで可能ではなかった方法で Windows 環境およびシステムと対話ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1235">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="fc430-1236">簡単な例として、ユーザーは次のコマンドを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1236">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="fc430-1237">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1237">More information can be found at:</span></span>

- [<span data-ttu-id="fc430-1238">相互運用に関する WSL チームのブログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1238">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="fc430-1239">MSDN 相互運用のドキュメント</span><span class="sxs-lookup"><span data-stu-id="fc430-1239">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="fc430-1240">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1240">Fixed</span></span>

- <span data-ttu-id="fc430-1241">すべての新しい WSL インスタンスで Ubuntu 16.04 (Xenial) がインストールされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1241">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="fc430-1242">既存の 14.04 (Trusty) インスタンスを使用しているユーザーは自動的にアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1242">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="fc430-1243">インストール中に設定されたロケールが表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1243">Locale set during install is now displayed</span></span>
- <span data-ttu-id="fc430-1244">ファイルへの WSL プロセスのリダイレクトが必ずしも機能しないというバグを含む、ターミナルの機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1244">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="fc430-1245">コンソールの有効期間は bash.exe の有効期間に関連付けられている必要があります</span><span class="sxs-lookup"><span data-stu-id="fc430-1245">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="fc430-1246">コンソール ウィンドウのサイズは、バッファー サイズではなく表示サイズを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="fc430-1246">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="fc430-1247">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1247">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1248">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1248">LTP Results:</span></span>
<span data-ttu-id="fc430-1249">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="fc430-1249">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc430-1250">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="fc430-1250">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc430-1251">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1251">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="fc430-1252">ビルド 14946</span><span class="sxs-lookup"><span data-stu-id="fc430-1252">Build 14946</span></span>

<span data-ttu-id="fc430-1253">ビルド 14946 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1253">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1254">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1254">Fixed</span></span>

- <span data-ttu-id="fc430-1255">スペースまたは引用符を含む NT ユーザー名を持つユーザーの WSL ユーザー アカウントの作成を妨げる問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1255">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="fc430-1256">stat でディレクトリのリンク数に対して 0 が返されるように、VolFs と DrvFs を変更します</span><span class="sxs-lookup"><span data-stu-id="fc430-1256">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="fc430-1257">IPV6_MULTICAST_HOPS ソケット オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fc430-1257">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="fc430-1258">1 つの tty につき 1 つのコンソール I/O ループに制限します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1258">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="fc430-1259">たとえば、次のコマンドが可能です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1259">Example: the following command is possible:</span></span>
  - <span data-ttu-id="fc430-1260">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="fc430-1260">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="fc430-1261">/proc/cpuinfo でスペースをタブに置き換えます (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="fc430-1261">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="fc430-1262">DrvFs は、マウントされた Windows ボリュームと一致する名前で mountinfo に表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1262">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="fc430-1263">/home と /root が正しい名前で mountinfo に表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1263">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="fc430-1264">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1264">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1265">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1265">LTP Results:</span></span>
<span data-ttu-id="fc430-1266">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="fc430-1266">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc430-1267">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="fc430-1267">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc430-1268">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1268">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="fc430-1269">ビルド 14942</span><span class="sxs-lookup"><span data-stu-id="fc430-1269">Build 14942</span></span>

<span data-ttu-id="fc430-1270">ビルド 14942 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/onefourninefourtwoooooo)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1270">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1271">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1271">Fixed</span></span>

- <span data-ttu-id="fc430-1272">SSH をブロックしていた "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" ネットワーク クラッシュを含め、複数のバグチェックに対処しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1272">A number of bugchecks addressed, including the "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" networking crash which was blocking SSH</span></span>
- <span data-ttu-id="fc430-1273">DrvFs の Windows アプリケーションから生成された通知に対する inotifiy のサポートが有効になりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1273">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="fc430-1274">mongod に対して TCP_KEEPIDLE および TCP_KEEPINTVL を実装します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1274">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="fc430-1275">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="fc430-1275">(GH #695)</span></span>
- <span data-ttu-id="fc430-1276">pivot_root システム コールを実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-1276">Implement the pivot_root system call</span></span>
- <span data-ttu-id="fc430-1277">SO_DONTROUTE に対してソケット オプションを実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-1277">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="fc430-1278">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1278">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="fc430-1279">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1279">LTP Results:</span></span>
<span data-ttu-id="fc430-1280">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="fc430-1280">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="fc430-1281">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="fc430-1281">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="fc430-1282">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1282">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1283">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1283">Syscall Support</span></span>
<span data-ttu-id="fc430-1284">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1284">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1285">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1285">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="fc430-1286">ビルド 14936</span><span class="sxs-lookup"><span data-stu-id="fc430-1286">Build 14936</span></span>

<span data-ttu-id="fc430-1287">ビルド 14936 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1287">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="fc430-1288">注: WSL は、今後のリリースで Ubuntu 14.04 (Trusty) ではなく、Ubuntu バージョン 16.04 (Xenial) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="fc430-1288">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="fc430-1289">この変更は、新しいインスタンスをインストールする Insiders に適用されます (lxrun.exe、あるいは bash.exe のインストールまたは初回の実行)。</span><span class="sxs-lookup"><span data-stu-id="fc430-1289">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="fc430-1290">Trusty を使用する既存のインスタンスは、自動的にアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1290">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="fc430-1291">ユーザーは、do-release-upgrade コマンドを使用して、Trusty イメージを Xenial にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1291">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="fc430-1292">既知の問題</span><span class="sxs-lookup"><span data-stu-id="fc430-1292">Known Issue</span></span>
<span data-ttu-id="fc430-1293">WSL では、いくつかのソケット実装で問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="fc430-1293">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="fc430-1294">バグチェックを実行するとクラッシュし、エラー "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" が出されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1294">The bugcheck manifests itself as a crash with the error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span></span>  <span data-ttu-id="fc430-1295">この問題の最も一般的な発現は、SSH を使用したときのクラッシュです。</span><span class="sxs-lookup"><span data-stu-id="fc430-1295">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="fc430-1296">根本原因は内部ビルドで修正され、最も早い機会に Insiders にプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1296">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="fc430-1297">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1297">Fixed</span></span>

- <span data-ttu-id="fc430-1298">chroot システム コールを実装しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1298">Implemented the chroot system call</span></span>
- <span data-ttu-id="fc430-1299">~~Drvfs 上の Windows アプリケーションから生成された通知のサポートを含む~~ inotify の機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1299">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="fc430-1300">訂正:Windows アプリケーションからの変更に対する Inotify のサポートは、現時点では利用できません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1300">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="fc430-1301">IPV6::<port n> へのソケット バインドで、IPV6_V6ONLY がサポートされるようになりました (GH #68、#157、#393、#460、#674、#740、#982、#996)</span><span class="sxs-lookup"><span data-stu-id="fc430-1301">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="fc430-1302">waitid システム コールに対する WNOWAIT 動作を実装しました (GH #638)</span><span class="sxs-lookup"><span data-stu-id="fc430-1302">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="fc430-1303">IP ソケット オプション IP_HDRINCL と IP_TTL のサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1303">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="fc430-1304">長さゼロの read() はすぐに戻ります (GH #975)</span><span class="sxs-lookup"><span data-stu-id="fc430-1304">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="fc430-1305">.tar ファイルに NULL 終端文字を含まないファイル名とファイル名のプレフィックスを正しく処理します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1305">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="fc430-1306">/dev/null に対する epoll サポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1306">epoll support for /dev/null</span></span>
- <span data-ttu-id="fc430-1307">/dev/alarm タイム ソースを修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-1307">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="fc430-1308">Bash -c はファイルにリダイレクトできるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1308">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="fc430-1309">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1309">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1310">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1310">LTP Results:</span></span>
<span data-ttu-id="fc430-1311">合格したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="fc430-1311">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="fc430-1312">不合格の数 (失敗した、スキップしたなど):264</span><span class="sxs-lookup"><span data-stu-id="fc430-1312">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="fc430-1313">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1313">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1314">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1314">Syscall Support</span></span>
<span data-ttu-id="fc430-1315">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1315">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1316">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1316">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="fc430-1317">ビルド 14931</span><span class="sxs-lookup"><span data-stu-id="fc430-1317">Build 14931</span></span>

<span data-ttu-id="fc430-1318">ビルド 14931 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1318">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1319">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1319">Fixed</span></span>

 - <span data-ttu-id="fc430-1320">Microsoft の制御を超える状況により、Windows Subsystem for Linux のこのビルドには更新はありません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1320">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="fc430-1321">定期的にスケジュールされた更新は、次のリリースから再開されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1321">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="fc430-1322">ビルド 14926</span><span class="sxs-lookup"><span data-stu-id="fc430-1322">Build 14926</span></span>

<span data-ttu-id="fc430-1323">ビルド 14926 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1323">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1324">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1324">Fixed</span></span>

- <span data-ttu-id="fc430-1325">管理者特権を持たないコンソールで Ping が機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1325">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="fc430-1326">Ping6 が、この場合も管理者特権なしでサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1326">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="fc430-1327">WSL を使用して変更されたファイルに対する Inotify サポート。</span><span class="sxs-lookup"><span data-stu-id="fc430-1327">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="fc430-1328">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="fc430-1328">(GH #216)</span></span>
  - <span data-ttu-id="fc430-1329">サポートされるフラグ:</span><span class="sxs-lookup"><span data-stu-id="fc430-1329">Flags supported:</span></span>
    - <span data-ttu-id="fc430-1330">inotify_init1:LX_O_CLOEXEC、LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="fc430-1330">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="fc430-1331">inotify_add_watch イベント:LX_IN_ACCESS、LX_IN_MODIFY、LX_IN_ATTRIB、LX_IN_CLOSE_WRITE、LX_IN_CLOSE_NOWRITE、LX_IN_OPEN、LX_IN_MOVED_FROM、LX_IN_MOVED_TO、LX_IN_CREATE、LX_IN_DELETE、LX_IN_DELETE_SELF、LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="fc430-1331">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="fc430-1332">inotify_add_watch 属性:LX_IN_DONT_FOLLOW、LX_IN_EXCL_UNLINK、LX_IN_MASK_ADD、LX_IN_ONESHOT、LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="fc430-1332">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="fc430-1333">出力の読み取り:LX_IN_ISDIR、LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="fc430-1333">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="fc430-1334">既知の問題:Windows アプリケーションからファイルを変更してもイベントは生成されません</span><span class="sxs-lookup"><span data-stu-id="fc430-1334">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="fc430-1335">Unix ソケットで SCM_CREDENTIALS がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1335">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="fc430-1336">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="fc430-1336">LTP Results:</span></span>
<span data-ttu-id="fc430-1337">合格したテストの数:651</span><span class="sxs-lookup"><span data-stu-id="fc430-1337">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="fc430-1338">不合格の数 (失敗した、スキップしたなど):258</span><span class="sxs-lookup"><span data-stu-id="fc430-1338">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="fc430-1339">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="fc430-1339">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="fc430-1340">ビルド 14915</span><span class="sxs-lookup"><span data-stu-id="fc430-1340">Build 14915</span></span>

<span data-ttu-id="fc430-1341">ビルド 14915 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1341">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1342">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1342">Fixed</span></span>
-  <span data-ttu-id="fc430-1343">UNIX データグラム ソケットに対する Socketpair (GH #262)</span><span class="sxs-lookup"><span data-stu-id="fc430-1343">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="fc430-1344">SO_REUSEADDR に対する UNIX ソケット サポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1344">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="fc430-1345">SO_BROADCAST に対する UNIX ソケット サポート (GH #568)</span><span class="sxs-lookup"><span data-stu-id="fc430-1345">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="fc430-1346">SOCK_SEQPACKET に対する UNIX ソケット サポート (GH #758、#546)</span><span class="sxs-lookup"><span data-stu-id="fc430-1346">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="fc430-1347">UNIX データグラム ソケット send、recv、および shutdown に対するサポートの追加</span><span class="sxs-lookup"><span data-stu-id="fc430-1347">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="fc430-1348">固定されていないアドレスに対する無効な mmap パラメーター検証によるバグチェックの修正。</span><span class="sxs-lookup"><span data-stu-id="fc430-1348">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="fc430-1349">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="fc430-1349">(GH #847)</span></span>
- <span data-ttu-id="fc430-1350">ターミナルの状態の中断/再開のサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1350">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="fc430-1351">Screen ユーティリティのブロックを解除する TIOCPKT ioctl のサポート (GH #774)</span><span class="sxs-lookup"><span data-stu-id="fc430-1351">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="fc430-1352">既知の問題:ファンクション キーが動作しません</span><span class="sxs-lookup"><span data-stu-id="fc430-1352">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="fc430-1353">解放されたメンバー 'ReaderReady' が LxpTimerFdWorkerRoutine によってアクセスされる原因となる TimerFd での競合を修正しました (GH #814)</span><span class="sxs-lookup"><span data-stu-id="fc430-1353">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="fc430-1354">futex、poll、および clock_nanosleep に対する再起動可能システム コールのサポートを有効にします</span><span class="sxs-lookup"><span data-stu-id="fc430-1354">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="fc430-1355">bind mount のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1355">Added bind mount support</span></span>
- <span data-ttu-id="fc430-1356">マウント名前空間に対する unshare のサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1356">unshare for mount namespace support</span></span>
    - <span data-ttu-id="fc430-1357">既知の問題:`unshare(CLONE_NEWNS)` を使用して新しいマウント名前空間を作成するときに、現在の作業ディレクトリは引き続き古い名前空間を指します</span><span class="sxs-lookup"><span data-stu-id="fc430-1357">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="fc430-1358">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="fc430-1358">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="fc430-1359">ビルド 14905</span><span class="sxs-lookup"><span data-stu-id="fc430-1359">Build 14905</span></span>

<span data-ttu-id="fc430-1360">ビルド 14905 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1360">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1361">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1361">Fixed</span></span>
- <span data-ttu-id="fc430-1362">再起動可能システム コールがサポートされるようになりました (GH #349、GH #520)</span><span class="sxs-lookup"><span data-stu-id="fc430-1362">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="fc430-1363">/ で終了するディレクトリへのシンボリック リンクが動作するようになりました (GH #650)</span><span class="sxs-lookup"><span data-stu-id="fc430-1363">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="fc430-1364">/dev/random に対する RNDGETENTCNT ioctl を実装しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1364">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="fc430-1365">/proc/[pid]/mounts、/proc/[pid]/mountinfo、および /proc/[pid]/mountstats のファイルを実装しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1365">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="fc430-1366">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1366">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="fc430-1367">ビルド 14901</span><span class="sxs-lookup"><span data-stu-id="fc430-1367">Build 14901</span></span>
<span data-ttu-id="fc430-1368">Windows 10 Anniversary Update リリース以降の最初の Insider ビルド。</span><span class="sxs-lookup"><span data-stu-id="fc430-1368">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="fc430-1369">ビルド 14901 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1369">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1370">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1370">Fixed</span></span>
- <span data-ttu-id="fc430-1371">末尾のスラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1371">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="fc430-1372">`$ mv a/c/ a/b/` などのコマンドが機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1372">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="fc430-1373">インストールで、Ubuntu のロケールを Windows のロケールに設定すべきかどうかを確認するプロンプトが出されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1373">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="fc430-1374">ns フォルダーに対する Procfs のサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1374">Procfs support for ns folder</span></span>
- <span data-ttu-id="fc430-1375">tmpfs、procfs、および sysfs のファイルシステムに対して mount と unmount を追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1375">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="fc430-1376">mknod[at] 32 ビット ABI の署名を修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-1376">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="fc430-1377">UNIX ソケットをディスパッチ モデルに移行しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1377">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="fc430-1378">setsockopt を使用して設定された INET ソケットの recv バッファー サイズを優先します</span><span class="sxs-lookup"><span data-stu-id="fc430-1378">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="fc430-1379">MSG_CMSG_CLOEXEC Unix ソケット受信メッセージ フラグを実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-1379">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="fc430-1380">Linux プロセスの stdin/stdout パイプのリダイレクト (GH #2)</span><span class="sxs-lookup"><span data-stu-id="fc430-1380">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="fc430-1381">CMD で bash -c コマンドのパイプを許可します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1381">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="fc430-1382">例:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="fc430-1382">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="fc430-1383">複数のページ ファイルがあるシステムに Bash をインストールできるようになりました (GH #538、#358)</span><span class="sxs-lookup"><span data-stu-id="fc430-1383">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="fc430-1384">既定の INET ソケット バッファー サイズは、既定の Ubuntu セットアップのものと一致している必要があります</span><span class="sxs-lookup"><span data-stu-id="fc430-1384">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="fc430-1385">xattr システム コールを listxattr に合わせて配置します</span><span class="sxs-lookup"><span data-stu-id="fc430-1385">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="fc430-1386">SIOCGIFCONF から有効な IPv4 アドレスを持つインターフェイスのみを返します</span><span class="sxs-lookup"><span data-stu-id="fc430-1386">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="fc430-1387">ptrace によって挿入される際のシグナルの既定のアクションを修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-1387">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="fc430-1388">/proc/sys/vm/min_free_kbytes を実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-1388">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="fc430-1389">sigreturn でコンテキストを復元するときにマシン コンテキスト レジスタの値を使用します</span><span class="sxs-lookup"><span data-stu-id="fc430-1389">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="fc430-1390">これにより、一部のユーザーで java と javac がハングしていた問題が解決されます</span><span class="sxs-lookup"><span data-stu-id="fc430-1390">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="fc430-1391">/proc/sys/kernel/hostname を実装します</span><span class="sxs-lookup"><span data-stu-id="fc430-1391">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1392">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1392">Syscall Support</span></span>
<span data-ttu-id="fc430-1393">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1394">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="fc430-1395">ビルド 14388 から Windows 10 Anniversary Update まで</span><span class="sxs-lookup"><span data-stu-id="fc430-1395">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="fc430-1396">ビルド 14388 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/14388wip)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1396">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc430-1397">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1397">Fixed</span></span>
- <span data-ttu-id="fc430-1398">8/2 の Windows 10 Anniversary Update の準備をするための修正</span><span class="sxs-lookup"><span data-stu-id="fc430-1398">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="fc430-1399">Anniversary Update での WSL の詳細情報については、こちらの[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください</span><span class="sxs-lookup"><span data-stu-id="fc430-1399">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="fc430-1400">ビルド 14376</span><span class="sxs-lookup"><span data-stu-id="fc430-1400">Build 14376</span></span>
<span data-ttu-id="fc430-1401">ビルド 14376 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1401">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc430-1402">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1402">Fixed</span></span>
- <span data-ttu-id="fc430-1403">apt-get がハングするいくつかのインスタンスを削除しました (GH #493)</span><span class="sxs-lookup"><span data-stu-id="fc430-1403">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="fc430-1404">空のマウントが正しく処理されなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1404">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="fc430-1405">ramdisk が正しくマウントされなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1405">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="fc430-1406">フラグをサポートするように UNIX ソケット accept を変更します (一部 GH #451)</span><span class="sxs-lookup"><span data-stu-id="fc430-1406">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="fc430-1407">一般的なネットワークに関連したブルースクリーンを修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1407">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="fc430-1408">/proc/[pid]/task にアクセスするときのブルースクリーンを修正しました (GH #523)</span><span class="sxs-lookup"><span data-stu-id="fc430-1408">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="fc430-1409">一部の pty シナリオでの高い CPU 使用率を修正しました (GH #488、#504)</span><span class="sxs-lookup"><span data-stu-id="fc430-1409">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="fc430-1410">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1410">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="fc430-1411">ビルド 14371</span><span class="sxs-lookup"><span data-stu-id="fc430-1411">Build 14371</span></span>
<span data-ttu-id="fc430-1412">ビルド 14371 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1412">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc430-1413">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1413">Fixed</span></span>
- <span data-ttu-id="fc430-1414">ptrace を使用する際の SIGCHLD と wait () のタイミングの競合を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1414">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="fc430-1415">パスの末尾に / がある場合の一部の動作を修正しました (GH #432)</span><span class="sxs-lookup"><span data-stu-id="fc430-1415">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="fc430-1416">子への開いたハンドルのために rename/unlink が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1416">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="fc430-1417">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1417">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="fc430-1418">ビルド 14366</span><span class="sxs-lookup"><span data-stu-id="fc430-1418">Build 14366</span></span>
<span data-ttu-id="fc430-1419">ビルド 14366 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1419">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc430-1420">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1420">Fixed</span></span>
- <span data-ttu-id="fc430-1421">シンボリック リンクを使用したファイル作成の修正</span><span class="sxs-lookup"><span data-stu-id="fc430-1421">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="fc430-1422">Python 用 listxattr を追加しました (GH 385)</span><span class="sxs-lookup"><span data-stu-id="fc430-1422">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="fc430-1423">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1423">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1424">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1424">Syscall Support</span></span>
-   <span data-ttu-id="fc430-1425">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1425">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1426">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1426">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="fc430-1427">ビルド 14361</span><span class="sxs-lookup"><span data-stu-id="fc430-1427">Build 14361</span></span>
<span data-ttu-id="fc430-1428">ビルド 14361 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14361)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1428">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc430-1429">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1429">Fixed</span></span>
- <span data-ttu-id="fc430-1430">Bash on Ubuntu on Windows で実行しているときに、DrvFs で大文字と小文字が区別されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1430">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="fc430-1431">ユーザーは、/mnt/c ドライブで case.txt と CASE.TXT を使用できます</span><span class="sxs-lookup"><span data-stu-id="fc430-1431">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="fc430-1432">大文字小文字の区別は、Bash on Ubuntu on Windows でのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="fc430-1432">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="fc430-1433">Bash の外では、NTFS はファイルを正しく報告しますが、Windows からのファイルの操作で、予期しない動作が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1433">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="fc430-1434">各ボリュームのルート (つまり、/mnt/c) では大文字小文字の区別はありません</span><span class="sxs-lookup"><span data-stu-id="fc430-1434">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="fc430-1435">Windows でのこれらのファイルの処理について詳しくは、[こちら](https://support.microsoft.com/kb/100625)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1435">More information on handling these files in Windows can be found [here](https://support.microsoft.com/kb/100625).</span></span>
- <span data-ttu-id="fc430-1436">pty / tty のサポートが大幅に強化されました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1436">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="fc430-1437">TMUX のようなアプリケーションがサポートされるようになりました (GH #40)</span><span class="sxs-lookup"><span data-stu-id="fc430-1437">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="fc430-1438">ユーザー アカウントが必ずしも作成されないというインストールの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1438">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="fc430-1439">非常に長い引数リストを使用できるように、コマンド ラインの引数の構造を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1439">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="fc430-1440">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="fc430-1440">(GH #153)</span></span>
- <span data-ttu-id="fc430-1441">DrvFs から read_only ファイルの削除および chmod を実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1441">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="fc430-1442">切断時にターミナルがハングする一部のインスタンスを修正しました (GH #43)</span><span class="sxs-lookup"><span data-stu-id="fc430-1442">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="fc430-1443">chmod および chown が tty デバイスで機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1443">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="fc430-1444">localhost として 0.0.0.0 および :: への接続を許可します (GH #388)</span><span class="sxs-lookup"><span data-stu-id="fc430-1444">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="fc430-1445">Sendmsg/recvmsg は、>1 の IO ベクトル長を処理するようになりました (一部 GH #376)</span><span class="sxs-lookup"><span data-stu-id="fc430-1445">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="fc430-1446">ユーザーは、自動生成された hosts ファイルをオプトアウトできるようになりました (GH #398)</span><span class="sxs-lookup"><span data-stu-id="fc430-1446">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="fc430-1447">インストール中に Linux のロケールを NT のロケールに自動的に一致させます (GH #11)</span><span class="sxs-lookup"><span data-stu-id="fc430-1447">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="fc430-1448">/proc/sys/vm/swappiness ファイルを追加しました (GH #306)</span><span class="sxs-lookup"><span data-stu-id="fc430-1448">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="fc430-1449">strace が正常に終了するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1449">strace now exits correctly</span></span>
- <span data-ttu-id="fc430-1450">/proc/self/fd を使用したパイプの再オープンを許可します (GH #222)</span><span class="sxs-lookup"><span data-stu-id="fc430-1450">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="fc430-1451">DrvFs で %LOCALAPPDATA%\lxss の下のディレクトリが非表示になります (GH #270)</span><span class="sxs-lookup"><span data-stu-id="fc430-1451">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="fc430-1452">bash.exe ~ の処理の改善。</span><span class="sxs-lookup"><span data-stu-id="fc430-1452">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="fc430-1453">"bash ~ -c ls" のようなコマンドがサポートされるようになりました (GH #467)</span><span class="sxs-lookup"><span data-stu-id="fc430-1453">Commands like "bash ~ -c ls" now supported (GH #467)</span></span>
- <span data-ttu-id="fc430-1454">ソケットが、シャットダウン中に使用可能な epoll read を通知するようになりました (GH #271)</span><span class="sxs-lookup"><span data-stu-id="fc430-1454">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="fc430-1455">lxrun /uninstall でファイルとフォルダーの削除ジョブが改善されました</span><span class="sxs-lookup"><span data-stu-id="fc430-1455">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="fc430-1456">ps -f を修正しました (GH #246)</span><span class="sxs-lookup"><span data-stu-id="fc430-1456">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="fc430-1457">xEmacs などの x11 アプリのサポートを強化しました (GH #481)</span><span class="sxs-lookup"><span data-stu-id="fc430-1457">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="fc430-1458">既定の Ubuntu 設定に一致するように初期スレッドのスタック サイズを更新しました。また、get_rlimit システム コールにサイズを正しく報告します (GH #172、#258)</span><span class="sxs-lookup"><span data-stu-id="fc430-1458">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="fc430-1459">Pico プロセスのイメージ名の報告を改善しました (監査のためなど)</span><span class="sxs-lookup"><span data-stu-id="fc430-1459">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="fc430-1460">df コマンドに対して /proc/mountinfo を実装しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1460">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="fc430-1461">子名のシンボリック リンクのエラー コードを修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1461">Fixed symlink error code for child name .</span></span> <span data-ttu-id="fc430-1462">(. および ..)</span><span class="sxs-lookup"><span data-stu-id="fc430-1462">and ..</span></span>
- <span data-ttu-id="fc430-1463">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1463">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1464">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1464">Syscall Support</span></span>
<span data-ttu-id="fc430-1465">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1465">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1466">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1466">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="fc430-1467">ビルド 14352</span><span class="sxs-lookup"><span data-stu-id="fc430-1467">Build 14352</span></span>
<span data-ttu-id="fc430-1468">ビルド 14352 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14352)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1468">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1469">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1469">Fixed</span></span>
- <span data-ttu-id="fc430-1470">大きなファイルが正しくダウンロードまたは作成されなかった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1470">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="fc430-1471">これにより、npm と他のシナリオのブロックが解除されます (GH #3、GH #313)</span><span class="sxs-lookup"><span data-stu-id="fc430-1471">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="fc430-1472">ソケットがハングするいくつかのインスタンスを削除しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1472">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="fc430-1473">いくつかの ptrace エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1473">Corrected some ptrace errors</span></span>
- <span data-ttu-id="fc430-1474">WSL で 255 文字を超えるファイル名が許可される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1474">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="fc430-1475">英語以外の文字のサポートが強化されました</span><span class="sxs-lookup"><span data-stu-id="fc430-1475">Improved support for non-English characters</span></span>
- <span data-ttu-id="fc430-1476">現在の Windows タイムゾーンのデータを追加し、既定として設定します</span><span class="sxs-lookup"><span data-stu-id="fc430-1476">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="fc430-1477">マウント ポイントごとに一意のデバイス ID (JRE 修正 – GH #49)</span><span class="sxs-lookup"><span data-stu-id="fc430-1477">Unique device id's for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="fc430-1478">"."{}および ".." を含むパスの問題を修正します</span><span class="sxs-lookup"><span data-stu-id="fc430-1478">Correct issue with paths containing "." and ".."</span></span>
- <span data-ttu-id="fc430-1479">Fifo のサポートを追加しました (GH #71)</span><span class="sxs-lookup"><span data-stu-id="fc430-1479">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="fc430-1480">ネイティブ Ubuntu 形式に一致するように resolv.conf の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1480">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="fc430-1481">一部の procfs のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="fc430-1481">Some procfs cleanup</span></span>
- <span data-ttu-id="fc430-1482">管理者コンソールの Ping を有効にしました (GH #18)</span><span class="sxs-lookup"><span data-stu-id="fc430-1482">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1483">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1483">Syscall Support</span></span>
<span data-ttu-id="fc430-1484">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1484">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1485">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1485">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="fc430-1486">ビルド 14342</span><span class="sxs-lookup"><span data-stu-id="fc430-1486">Build 14342</span></span>
<span data-ttu-id="fc430-1487">ビルド 14342 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14342)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1487">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="fc430-1488">VolFs および DriveFs の情報については、[WSL ブログ](https://blogs.msdn.microsoft.com/wsl)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1488">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="fc430-1489">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1489">Fixed</span></span>
- <span data-ttu-id="fc430-1490">Windows ユーザーのユーザー名に Unicode 文字が含まれている場合のインストールの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1490">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="fc430-1491">FAQ にある apt-get update udev の回避策が、初回の実行時に既定で提供されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1491">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="fc430-1492">DriveFs (/mnt/<drive>) ディレクトリでシンボリック リンクを有効にしました</span><span class="sxs-lookup"><span data-stu-id="fc430-1492">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="fc430-1493">シンボリック リンクが DriveFs と VolFs 間で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1493">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="fc430-1494">アドレス指定された最上位のパス解析の問題に対処し、ls .// が期待どおりに動作するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1494">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="fc430-1495">DriveFs での npm install、および -g オプションが機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1495">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="fc430-1496">PHP サーバーの起動を妨げている問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1496">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="fc430-1497">ネイティブ Ubuntu により近く一致するように $PATH などの既定の環境値を更新しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1497">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="fc430-1498">apt パッケージ キャッシュを更新するための Windows での週単位のメンテナンス タスクを追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1498">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="fc430-1499">ELF ヘッダー検証の問題を修正しました。WSL ですべての Melkor オプションがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1499">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="fc430-1500">Zsh シェルが機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1500">Zsh shell is functional</span></span>
- <span data-ttu-id="fc430-1501">プリコンパイル済みの Go バイナリがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1501">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="fc430-1502">Bash.exe の初回実行時のプロンプトが正しくローカライズされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1502">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="fc430-1503">/proc/meminfo が正しい情報を返すようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1503">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="fc430-1504">ソケットが VFS でサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1504">Sockets now supported in VFS</span></span>
- <span data-ttu-id="fc430-1505">/dev が tempfs としてマウントされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1505">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="fc430-1506">Fifo がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1506">Fifo now supported</span></span>
- <span data-ttu-id="fc430-1507">マルチコア システムが /proc/cpuinfo に正しく表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1507">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="fc430-1508">初回実行時のダウンロードにおける追加の改善とエラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="fc430-1508">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="fc430-1509">システム コールの機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="fc430-1509">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="fc430-1510">サポートされるシステム コールの一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1510">Supported syscall list below.</span></span>
- <span data-ttu-id="fc430-1511">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1511">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="fc430-1512">の既知の問題</span><span class="sxs-lookup"><span data-stu-id="fc430-1512">Known Issues</span></span>
- <span data-ttu-id="fc430-1513">場合によって、DriveFs で '..'</span><span class="sxs-lookup"><span data-stu-id="fc430-1513">Not resolving '..'</span></span> <span data-ttu-id="fc430-1514">が正しく解決されません</span><span class="sxs-lookup"><span data-stu-id="fc430-1514">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1515">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1515">Syscall Support</span></span>
<span data-ttu-id="fc430-1516">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1516">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="fc430-1517">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1517">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="fc430-1518">ビルド 14332</span><span class="sxs-lookup"><span data-stu-id="fc430-1518">Build 14332</span></span>

<span data-ttu-id="fc430-1519">ビルド 14332 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14332)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1519">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="fc430-1520">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1520">Fixed</span></span>
- <span data-ttu-id="fc430-1521">DNS エントリの優先順位付けを含め、resolv.conf の生成が改善されました</span><span class="sxs-lookup"><span data-stu-id="fc430-1521">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="fc430-1522">/mnt ドライブと /mnt 以外のドライブとの間のファイルとディレクトリの移動に関する問題</span><span class="sxs-lookup"><span data-stu-id="fc430-1522">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="fc430-1523">シンボリック リンクを使って tar ファイルを作成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1523">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="fc430-1524">インスタンス作成時に既定の /run/lock ディレクトリを追加しました</span><span class="sxs-lookup"><span data-stu-id="fc430-1524">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="fc430-1525">適切な stat 情報を返すように /dev/null を更新します</span><span class="sxs-lookup"><span data-stu-id="fc430-1525">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="fc430-1526">初回実行時のダウンロードにおける追加エラー</span><span class="sxs-lookup"><span data-stu-id="fc430-1526">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="fc430-1527">システム コールの機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="fc430-1527">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="fc430-1528">サポートされるシステム コールの一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1528">Supported syscall list below.</span></span>
- <span data-ttu-id="fc430-1529">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1529">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1530">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1530">Syscall Support</span></span>
<span data-ttu-id="fc430-1531">以下は、WSL に何らかの実装がある新しいシステム コールです。</span><span class="sxs-lookup"><span data-stu-id="fc430-1531">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="fc430-1532">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1532">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="fc430-1533">ビルド 14328</span><span class="sxs-lookup"><span data-stu-id="fc430-1533">Build 14328</span></span>

<span data-ttu-id="fc430-1534">ビルド 14332 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14328)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc430-1534">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="fc430-1535">新機能</span><span class="sxs-lookup"><span data-stu-id="fc430-1535">New Features</span></span>
* <span data-ttu-id="fc430-1536">Linux ユーザーがサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1536">Now support Linux users.</span></span>  <span data-ttu-id="fc430-1537">Bash on Ubuntu on Windows をインストールすると、Linux ユーザーの作成を求めるプロンプトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc430-1537">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="fc430-1538">詳細については、 https://aka.ms/wslusers にアクセスしてください</span><span class="sxs-lookup"><span data-stu-id="fc430-1538">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="fc430-1539">ホスト名は、Windows コンピューター名に設定されるようになりました。@localhost はもう使用されません</span><span class="sxs-lookup"><span data-stu-id="fc430-1539">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="fc430-1540">ビルド 14328 の詳細についは、次を参照してください: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="fc430-1540">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="fc430-1541">固定</span><span class="sxs-lookup"><span data-stu-id="fc430-1541">Fixed</span></span>
* <span data-ttu-id="fc430-1542">/mnt/<drive> 以外のファイルに対するシンボリック リンクの機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1542">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="fc430-1543">npm install が機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1543">npm install now works</span></span>
    * <span data-ttu-id="fc430-1544">jdk / jre は、[こちら](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)の説明を使用してインストールできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fc430-1544">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="fc430-1545">既知の問題: シンボリック リンクは Windows マウントでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="fc430-1545">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="fc430-1546">機能は今後のビルドで使用できるようになる予定です</span><span class="sxs-lookup"><span data-stu-id="fc430-1546">Functionality will be available in a later build</span></span>
* <span data-ttu-id="fc430-1547">top と htop が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="fc430-1547">top and htop now display</span></span>
* <span data-ttu-id="fc430-1548">一部のインストール エラーに対する追加のエラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="fc430-1548">Additional error messages for some install failures</span></span>
* <span data-ttu-id="fc430-1549">システム コールの機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="fc430-1549">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="fc430-1550">サポートされるシステム コールの一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="fc430-1550">Supported syscall list below.</span></span>
* <span data-ttu-id="fc430-1551">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="fc430-1551">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="fc430-1552">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="fc430-1552">Syscall Support</span></span>
<span data-ttu-id="fc430-1553">次に示すのは、WSL に何らかの実装があるシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="fc430-1553">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="fc430-1554">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc430-1554">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
