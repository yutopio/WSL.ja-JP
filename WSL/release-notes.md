---
title: Windows Subsystem for Linux のリリース ノート
description: Windows Subsystem for Linux のリリース ノート。  毎週更新されます。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: b92c20bad50d0c58da05bb0c8f26a69d4c0b2970
ms.sourcegitcommit: 050f6095e92469b903db8ddf9356df5b22b21804
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "71910302"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="b2153-105">Windows Subsystem for Linux のリリース ノート</span><span class="sxs-lookup"><span data-stu-id="b2153-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18995"></a><span data-ttu-id="b2153-106">ビルド 18995</span><span class="sxs-lookup"><span data-stu-id="b2153-106">Build 18995</span></span>
<span data-ttu-id="b2153-107">ビルド 18995 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-107">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="b2153-108">[WSL2] 操作が中断された後に DrvFs マウントの動作が停止する問題を修正します (例: ctrl-c) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="b2153-108">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="b2153-109">[WSL2] hvsocket メッセージが非常に多い場合の処理を修正します [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="b2153-109">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="b2153-110">[WSL2] stdin がファイルの場合の相互運用に関する問題を修正します [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="b2153-110">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="b2153-111">[WSL2] 予期しないネットワークの状態が検出されたときにサービスがクラッシュする問題を修正します [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="b2153-111">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="b2153-112">[WSL2] 現在のプロセスに環境変数がない場合は、相互運用サーバーからディストリビューションの名前を照会します</span><span class="sxs-lookup"><span data-stu-id="b2153-112">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="b2153-113">[WSL2] stdin がファイルの場合の相互運用に関する問題を修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-113">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="b2153-114">[WSL2] Linux カーネル バージョンを 4.19.72 に更新します</span><span class="sxs-lookup"><span data-stu-id="b2153-114">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="b2153-115">[WSL2] .wslconfig を使用して追加のカーネル コマンド ライン パラメーターを指定する機能を追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-115">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments

```

## <a name="build-18990"></a><span data-ttu-id="b2153-116">ビルド 18990</span><span class="sxs-lookup"><span data-stu-id="b2153-116">Build 18990</span></span>
<span data-ttu-id="b2153-117">ビルド 18990 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-117">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="b2153-118">\\\\wsl$ のディレクトリの一覧のパフォーマンスを向上します</span><span class="sxs-lookup"><span data-stu-id="b2153-118">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="b2153-119">[WSL2] 追加のブート エントロピーを挿入します [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="b2153-119">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="b2153-120">[WSL2] su または sudo を使用する場合の Windows の相互運用を修正します [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="b2153-120">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>


## <a name="build-18980"></a><span data-ttu-id="b2153-121">ビルド 18980</span><span class="sxs-lookup"><span data-stu-id="b2153-121">Build 18980</span></span>
<span data-ttu-id="b2153-122">ビルド 18980 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-122">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="b2153-123">FILE_READ_DATA を拒否するシンボリック リンクの読み取りを修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-123">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="b2153-124">これには、"C:\Document and Settings" など、下位互換性のために Windows が作成するすべてのシンボリック リンクや、ユーザー プロファイル ディレクトリ内の一連のシンボリック リンクが含まれます</span><span class="sxs-lookup"><span data-stu-id="b2153-124">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="b2153-125">予期しないファイル システム状態を致命的ではないものとします [GH 4334、4305]</span><span class="sxs-lookup"><span data-stu-id="b2153-125">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="b2153-126">[WSL2] CPU/ファームウェアで仮想化がサポートされている場合に、arm64 のサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-126">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="b2153-127">[WSL2] 特権のないユーザーがカーネル ログを表示することを許可します</span><span class="sxs-lookup"><span data-stu-id="b2153-127">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="b2153-128">[WSL2] stdout/stderr のソケットが閉じられているときの出力リレーを修正します [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="b2153-128">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="b2153-129">[WSL2] バッテリーおよび AC アダプターのパススルーをサポートします</span><span class="sxs-lookup"><span data-stu-id="b2153-129">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="b2153-130">[WSL2] Linux カーネルを 4.19.67 に更新します</span><span class="sxs-lookup"><span data-stu-id="b2153-130">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="b2153-131">/Etc/wsl.conf に既定のユーザー名を設定する機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-131">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="b2153-132">ビルド 18975</span><span class="sxs-lookup"><span data-stu-id="b2153-132">Build 18975</span></span>
<span data-ttu-id="b2153-133">ビルド 18975 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-133">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="b2153-134">[WSL2] 複数の localhost の信頼性に関する問題を修正しました [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="b2153-134">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="b2153-135">ビルド 18970</span><span class="sxs-lookup"><span data-stu-id="b2153-135">Build 18970</span></span>
<span data-ttu-id="b2153-136">ビルド 18970 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-136">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="b2153-137">[WSL2] システムがスリープ状態から再開するときにホスト時刻と時刻を同期します [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="b2153-137">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="b2153-138">[WSL2] 可能な場合、Windows ボリュームに NT シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="b2153-138">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="b2153-139">[WSL2] UTS、IPC、PID、および Mount の各名前空間にディストリビューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="b2153-139">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="b2153-140">[WSL2] サーバーが localhost に直接バインドするときの localhost ポート リレーを修正します [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="b2153-140">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="b2153-141">[WSL2] 出力がリダイレクトされるときの相互運用を修正します [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="b2153-141">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="b2153-142">[WSL2] 絶対 NT シンボリック リンクの変換をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b2153-142">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="b2153-143">[WSL2] カーネルを 4.19.59 に更新します</span><span class="sxs-lookup"><span data-stu-id="b2153-143">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="b2153-144">[WSL2] eth0 のサブネット マスクを正しく設定します。</span><span class="sxs-lookup"><span data-stu-id="b2153-144">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="b2153-145">[WSL2] 終了イベントが通知されたときにコンソール ワーカー ループから抜け出すようにロジックを変更します。</span><span class="sxs-lookup"><span data-stu-id="b2153-145">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="b2153-146">[WSL2] ディストリビューションが実行されていないときに、ディストリビューション VHD を取り出します。</span><span class="sxs-lookup"><span data-stu-id="b2153-146">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="b2153-147">[WSL2] 空の値を正しく処理するように構成の解析ライブラリを修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-147">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="b2153-148">[WSL2] クロス ディストリビューション マウントを作成することにより、Docker Desktop をサポートします。</span><span class="sxs-lookup"><span data-stu-id="b2153-148">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="b2153-149">/etc/wsl.conf ファイルに次の行を追加することにより、ディストリビューションはこの動作をオプトインできます。</span><span class="sxs-lookup"><span data-stu-id="b2153-149">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="b2153-150">ビルド 18945</span><span class="sxs-lookup"><span data-stu-id="b2153-150">Build 18945</span></span>
<span data-ttu-id="b2153-151">ビルド 18945 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-151">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-152">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-152">WSL</span></span>
* <span data-ttu-id="b2153-153">[WSL2] localhost:port を使用して、WSL2 のリスニング tcp ソケットにホストからアクセスできるようにします</span><span class="sxs-lookup"><span data-stu-id="b2153-153">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="b2153-154">[WSL2] インストール/変換エラーの修正と、今後の問題を追跡するための追加の診断 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="b2153-154">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="b2153-155">[WSL2] WSL2 ネットワーク問題の診断能力を向上させます</span><span class="sxs-lookup"><span data-stu-id="b2153-155">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="b2153-156">[WSL2] カーネル バージョンを 4.19.55 に更新します</span><span class="sxs-lookup"><span data-stu-id="b2153-156">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="b2153-157">[WSL2] Docker に必要な構成オプションを使用してカーネルを更新します [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="b2153-157">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="b2153-158">[WSL2] ライトウェイト ユーティリティ VM に割り当てられる CPU の数を、ホストと同じになるように増やします (以前は、カーネル構成の CONFIG_NR_CPUS によって 8 個に制限されていました) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="b2153-158">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="b2153-159">[WSL2] WSL2 ライトウェイト VM 用のスワップ ファイルを作成します</span><span class="sxs-lookup"><span data-stu-id="b2153-159">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="b2153-160">[WSL2] \\\\wsl$\\distro (たとえば、sshfs) を使用してユーザー マウントを表示できるようにします [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="b2153-160">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="b2153-161">[WSL2] 9p ファイルシステムのパフォーマンスを改善します</span><span class="sxs-lookup"><span data-stu-id="b2153-161">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="b2153-162">[WSL2] VHD ACL が無制限に拡張されないようにします [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="b2153-162">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="b2153-163">[WSL2] SquashFS と xt_conntrack をサポートするようにカーネル構成を更新します [GH 4107、4123]</span><span class="sxs-lookup"><span data-stu-id="b2153-163">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="b2153-164">[WSL2] /etc/wsl.conf の interop.enabled オプションの修正 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="b2153-164">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="b2153-165">[WSL2] ファイルシステムで EA がサポートされていない場合、ENOTSUP を返します</span><span class="sxs-lookup"><span data-stu-id="b2153-165">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="b2153-166">[WSL2] \\\\wsl$ での CopyFile のハングを修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-166">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="b2153-167">既定の umask を 0022 に切り替えて、filesystem.umask 設定を /etc/wsl.conf に追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-167">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="b2153-168">シンボリック リンクを正しく解決するように wslpath を修正します。これは、19h1 での不具合でした [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="b2153-168">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="b2153-169">WSL2 設定を調整するために %UserProfile%\\.wslconfig ファイルを導入します</span><span class="sxs-lookup"><span data-stu-id="b2153-169">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="b2153-170">ビルド 18917</span><span class="sxs-lookup"><span data-stu-id="b2153-170">Build 18917</span></span>
<span data-ttu-id="b2153-171">ビルド 18917 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-171">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-172">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-172">WSL</span></span>
* <span data-ttu-id="b2153-173">WSL 2 が利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-173">WSL 2 is now available!</span></span> <span data-ttu-id="b2153-174">詳細については、[ブログ](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-174">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="b2153-175">シンボリック リンクを使用した Windows プロセスの起動が正常に機能しなかった不具合を修正します [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="b2153-175">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="b2153-176">wsl.exe --list --verbose、wsl.exe --list --quiet、および wsl.exe --import --version の各オプションを wsl.exe に追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-176">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="b2153-177">wsl.exe --shutdown オプションを追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-177">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="b2153-178">Plan 9:書き込みを成功させるためにディレクトリを開くことを許可します</span><span class="sxs-lookup"><span data-stu-id="b2153-178">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="b2153-179">ビルド 18890</span><span class="sxs-lookup"><span data-stu-id="b2153-179">Build 18890</span></span>
<span data-ttu-id="b2153-180">ビルド 18890 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-180">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-181">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-181">WSL</span></span>
* <span data-ttu-id="b2153-182">ノンブロッキング ソケット リーク [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="b2153-182">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="b2153-183">ターミナルへの EOF 入力が後続の読み取りをブロックする可能性があります [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="b2153-183">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="b2153-184">wsl.conf を参照するように resolv.conf ヘッダーを更新します [GH 3928 で説明]</span><span class="sxs-lookup"><span data-stu-id="b2153-184">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="b2153-185">epoll の delete コードでのデッドロック [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="b2153-185">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="b2153-186">--import および – export の引数のスペースを処理します [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="b2153-186">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="b2153-187">mmap を使用したファイルの拡張が正しく機能しません [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="b2153-187">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="b2153-188">ARM64 の \\\\wsl$ アクセスが正常に動作しないという問題を修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-188">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="b2153-189">wsl.exe 用のより適切な既定アイコンを追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-189">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="b2153-190">ビルド 18342</span><span class="sxs-lookup"><span data-stu-id="b2153-190">Build 18342</span></span>
<span data-ttu-id="b2153-191">ビルド 18342 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-191">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-192">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-192">WSL</span></span>
* <span data-ttu-id="b2153-193">ユーザーが Windows から WSL ディストリビューションの Linux ファイルにアクセスできるようにする機能を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-193">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="b2153-194">これらのファイルには、コマンド ラインを使用してアクセスできます。また、ファイル エクスプローラーや VSCode などの Windows アプリもこれらのファイルと対話できます。</span><span class="sxs-lookup"><span data-stu-id="b2153-194">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="b2153-195">\\\\wsl$\\<distro_name> に移動してファイルにアクセスするか、\\\\wsl$ に移動して実行中のディストリビューションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="b2153-195">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="b2153-196">CPU 情報タグを追加し、Cpus_allowed[_list] の値を修正します [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="b2153-196">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="b2153-197">リーダー以外のスレッドからの exec をサポートします [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="b2153-197">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="b2153-198">構成の更新エラーを致命的でないものとして処理します [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="b2153-198">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="b2153-199">オフセットを正しく処理するように binfmt を更新します [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="b2153-199">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="b2153-200">Plan 9 のネットワーク ドライブのマッピングを有効にします [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="b2153-200">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="b2153-201">バインド マウントのための Windows -> Linux および Linux -> Windows のパスの変換をサポートします</span><span class="sxs-lookup"><span data-stu-id="b2153-201">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="b2153-202">読み取り専用で開かれたファイルにマッピング用の読み取り専用セクションを作成します</span><span class="sxs-lookup"><span data-stu-id="b2153-202">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="b2153-203">ビルド 18334</span><span class="sxs-lookup"><span data-stu-id="b2153-203">Build 18334</span></span>
<span data-ttu-id="b2153-204">ビルド 18334 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-204">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-205">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-205">WSL</span></span>
* <span data-ttu-id="b2153-206">Windows タイム ゾーンが Linux タイム ゾーンにマップされる方法を再設計します [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="b2153-206">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="b2153-207">メモリ リークを修正し、新しい文字列変換関数を追加します [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="b2153-207">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="b2153-208">スレッドがない threadgroup での SIGCONT は no-op です [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="b2153-208">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="b2153-209">/proc/self/fd にソケットと epoll のファイル記述子を正しく表示します</span><span class="sxs-lookup"><span data-stu-id="b2153-209">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="b2153-210">ビルド 18305</span><span class="sxs-lookup"><span data-stu-id="b2153-210">Build 18305</span></span>
<span data-ttu-id="b2153-211">ビルド 18305 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-211">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-212">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-212">WSL</span></span>
* <span data-ttu-id="b2153-213">プライマリ スレッドが終了すると、pthread はファイルへのアクセスを失います [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="b2153-213">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="b2153-214">必要な場合を除き、TIOCSCTTY は “force” パラメーターを無視します [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="b2153-214">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="b2153-215">wsl.exe コマンド ラインの機能強化と、インポート/エクスポートの機能の追加。</span><span class="sxs-lookup"><span data-stu-id="b2153-215">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="b2153-216">ビルド 18277</span><span class="sxs-lookup"><span data-stu-id="b2153-216">Build 18277</span></span>
<span data-ttu-id="b2153-217">ビルド 18277 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-217">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-218">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-218">WSL</span></span>
* <span data-ttu-id="b2153-219">ビルド 18272 で発生した「そのようなインターフェイスはサポートされていません」というエラーを修正します [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="b2153-219">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="b2153-220">umount システム コールの MNT_FORCE フラグを無視します [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="b2153-220">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="b2153-221">公式の CreatePseudoConsole API を使用するように WSL の相互運用を切り替えます</span><span class="sxs-lookup"><span data-stu-id="b2153-221">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="b2153-222">FUTEX_WAIT の再起動時にタイムアウト値を保持しません</span><span class="sxs-lookup"><span data-stu-id="b2153-222">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="b2153-223">ビルド 18272</span><span class="sxs-lookup"><span data-stu-id="b2153-223">Build 18272</span></span>
<span data-ttu-id="b2153-224">ビルド18272の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-224">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-225">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-225">WSL</span></span>
* <span data-ttu-id="b2153-226">**警告:** このビルドには、WSL を操作不能にする問題があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-226">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="b2153-227">ディストリビューションを起動しようとすると、「そのようなインターフェイスはサポートされていません」というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-227">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="b2153-228">この問題は修正されており、次週の Insider Fast ビルドに組み込まれます。</span><span class="sxs-lookup"><span data-stu-id="b2153-228">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="b2153-229">このビルドをインストールした場合は、「設定」->「更新とセキュリティ」->「回復」を選択し、「前のバージョンの Windows 10 に戻す」を使用することで、前の Windows ビルドにロールバックできます。</span><span class="sxs-lookup"><span data-stu-id="b2153-229">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="b2153-230">ビルド 18267</span><span class="sxs-lookup"><span data-stu-id="b2153-230">Build 18267</span></span>
<span data-ttu-id="b2153-231">ビルド 18267 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-231">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-232">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-232">WSL</span></span>
* <span data-ttu-id="b2153-233">ゾンビ プロセスが回収されず、無期限に存在し続ける問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-233">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="b2153-234">エラー メッセージが最大長を超えると、WslRegisterDistribution がハングします [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="b2153-234">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="b2153-235">DrvFs で読み取り専用ファイルに対して fsync を正常に実行できるようにします [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="b2153-235">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="b2153-236">内部にシンボリック リンクを作成する前に /bin ディレクトリと /sbin ディレクトリが存在することを確認します [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="b2153-236">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="b2153-237">WSL インスタンスに対するインスタンス終了タイムアウト メカニズムを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-237">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="b2153-238">タイムアウトは現在 15 秒に設定されています。つまり、最後の WSL プロセスが終了してから 15 秒後にインスタンスが終了します。</span><span class="sxs-lookup"><span data-stu-id="b2153-238">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="b2153-239">ディストリビューションをすぐに終了するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="b2153-239">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="b2153-240">ビルド 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="b2153-240">Build 17763 (1809)</span></span>
<span data-ttu-id="b2153-241">ビルド 17763 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-241">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-242">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-242">WSL</span></span>
* <span data-ttu-id="b2153-243">Setpriority システム コールのアクセス許可チェックが厳しすぎて、同じスレッドの優先順位を変更できません [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="b2153-243">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b2153-244">clock_gettime(CLOCK_BOOTTIME) に対して負値が返されないように、バイアスのかかっていない割り込み時間が起動時間に使用されていることを確認します [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="b2153-244">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b2153-245">WSL binfmt インタープリターでシンボリック リンクを処理します [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="b2153-245">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b2153-246">threadgroup リーダー ファイル記述子のクリーンアップの処理が改善されました。</span><span class="sxs-lookup"><span data-stu-id="b2153-246">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="b2153-247">オーバーフローを回避するために、KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用するように WSL を切り替えます [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="b2153-247">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b2153-248">Ptrace のアタッチにより、システム コールから無効な戻り値が返される場合があります [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="b2153-248">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b2153-249">AF_UNIX に関連したいくつかの問題を修正します [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="b2153-249">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b2153-250">現在の作業ディレクトリが 5 文字未満の場合に WSL の相互運用が失敗する原因となる問題を修正します [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="b2153-250">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="b2153-251">存在しないポートへのループバック接続の失敗による 1 秒間の遅延を回避します [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="b2153-251">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b2153-252">/proc/sys/fs/file-max スタブ ファイルを追加します [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="b2153-252">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b2153-253">より正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="b2153-253">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b2153-254">PR_SET_PTRACER のサポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="b2153-254">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b2153-255">エッジ トリガーされた epoll イベントをパイプ ファイルシステムが誤ってクリアします [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b2153-255">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b2153-256">NTFS シンボリック リンクによって起動された Win32 実行可能ファイルはシンボリック リンク名を考慮しません [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b2153-256">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="b2153-257">ゾンビ サポートを強化しました [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="b2153-257">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b2153-258">Windows の相互運用の動作を制御するための wsl.conf エントリを追加します [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="b2153-258">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b2153-259">getsockname で必ずしも UNIX ソケット ファミリの種類が返されない問題を修正します [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="b2153-259">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b2153-260">TIOCSTI のサポートを追加します [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="b2153-260">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b2153-261">接続処理中のノンブロッキング ソケットは、書き込み試行に対して EAGAIN を返します [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="b2153-261">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b2153-262">マウントされた VHD での相互運用をサポートします [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="b2153-262">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b2153-263">ルート フォルダーでのアクセス許可チェックの問題を修正します [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="b2153-263">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b2153-264">TTY キーボードの ioctl (KDGKBTYPE、KDGKBMODE、および KDSKBMODE) に対する制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-264">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b2153-265">Windows UI アプリは、バックグラウンドで起動された場合でも実行されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-265">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="b2153-266">wsl -u または --user オプションを追加します [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="b2153-266">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b2153-267">高速スタートアップが有効になっているときの WSL の起動問題を修正します [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="b2153-267">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b2153-268">UNIX ソケットは切断されたピア資格情報を保持する必要があります [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="b2153-268">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b2153-269">ノンブロッキング UNIX ソケットが EAGAIN で無限に失敗します [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="b2153-269">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b2153-270">case=off が、drvfs マウントの新しい既定の種類です [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="b2153-270">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b2153-271">詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-271">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b2153-272">実行中のディストリビューションを停止するための wslconfig /terminate を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-272">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="b2153-273">スペースを含むパスを正しく処理しない WSL シェル コンテキスト メニュー エントリの問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-273">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b2153-274">ディレクトリごとの大文字と小文字の区別を拡張属性として公開します</span><span class="sxs-lookup"><span data-stu-id="b2153-274">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b2153-275">ARM64: キャッシュのメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="b2153-275">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b2153-276">[dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。</span><span class="sxs-lookup"><span data-stu-id="b2153-276">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b2153-277">DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみをエスケープ解除します。</span><span class="sxs-lookup"><span data-stu-id="b2153-277">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="b2153-278">ELF パーサー インタープリターの長さの検証での Off-by-one エラーを修正します [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="b2153-278">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b2153-279">過去の時刻が設定された WSL 絶対タイマーは起動しません [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="b2153-279">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b2153-280">新しく作成された再解析ポイントが、親ディレクトリにそのように表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="b2153-280">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b2153-281">DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。</span><span class="sxs-lookup"><span data-stu-id="b2153-281">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="b2153-282">ファイルが存在していてもマルチスレッドの操作で ENOENT が返される場合がある追加の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-282">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b2153-283">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b2153-283">[GH 2712]</span></span>
* <span data-ttu-id="b2153-284">UMCI が有効になっているときの WSL の起動エラーを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-284">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b2153-285">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b2153-285">[GH 3020]</span></span>
* <span data-ttu-id="b2153-286">WSL を起動するエクスプローラーのコンテキスト メニューを追加します [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="b2153-286">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b2153-287">使用するには、エクスプローラー ウィンドウで Shift キーを押しながら右クリックします。</span><span class="sxs-lookup"><span data-stu-id="b2153-287">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b2153-288">UNIX ソケットのノンブロッキング動作を修正します [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="b2153-288">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b2153-289">GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-289">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b2153-290">マウント伝達フラグのサポートを追加します [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="b2153-290">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b2153-291">truncate で INotify イベントが発生しない問題を修正します [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="b2153-291">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b2153-292">シェルを使用せずに 1 つのバイナリを呼び出す wsl.exe の --exec オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-292">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b2153-293">特定のディストリビューションを選択する wsl.exe の --distribution オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-293">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="b2153-294">dmesg の制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-294">Limited support for dmesg.</span></span> <span data-ttu-id="b2153-295">アプリケーションは、dmesg にログを記録できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-295">Applications can now log to dmesg.</span></span> <span data-ttu-id="b2153-296">WSL ドライバーは、限られた情報を dmesg に記録します。</span><span class="sxs-lookup"><span data-stu-id="b2153-296">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b2153-297">将来的には、ドライバーからのその他の情報や診断情報を伝達するように拡張できます。</span><span class="sxs-lookup"><span data-stu-id="b2153-297">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b2153-298">注: dmesg は、現在、`/dev/kmsg` デバイス インターフェイスを介してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b2153-298">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b2153-299">`syslog` システム コール インターフェイスはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b2153-299">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="b2153-300">そのため、一部の `dmesg` コマンド ラインのオプション (`-S`、`-C` など) は機能しません。</span><span class="sxs-lookup"><span data-stu-id="b2153-300">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b2153-301">ネイティブに一致するように、シリアル デバイスの既定の gid とモードを変更します [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="b2153-301">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b2153-302">DrvFs で拡張属性がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-302">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b2153-303">注:DrvFs では、拡張属性の名前にいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-303">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b2153-304">一部の文字 ('/'、':'、'\*' など) は使用できません。また、DrvFs では拡張属性名の大文字と小文字は区別されません</span><span class="sxs-lookup"><span data-stu-id="b2153-304">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="b2153-305">ビルド 18252 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="b2153-305">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="b2153-306">ビルド 18252 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-306">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-307">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-307">WSL</span></span>
* <span data-ttu-id="b2153-308">init と bsdtar のバイナリを lxssmanager dll から別のツール フォルダーに移動します</span><span class="sxs-lookup"><span data-stu-id="b2153-308">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="b2153-309">CLONE_FILES を使用しているときのファイル記述子の終了に関する競合を修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-309">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="b2153-310">DrvFs パスを変換するときに /proc/pid/mountinfo の省略可能なフィールドを処理します</span><span class="sxs-lookup"><span data-stu-id="b2153-310">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="b2153-311">S_IFREG のメタデータのサポートなしに DrvFs mknod を正常に実行できるようにします</span><span class="sxs-lookup"><span data-stu-id="b2153-311">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="b2153-312">DrvFs に作成される読み取り専用ファイルには readonly 属性セットが必要です [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="b2153-312">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="b2153-313">DrvFs のマウントを処理する /sbin/mount.drvfs ヘルパーを追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-313">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="b2153-314">DrvFs で POSIX rename を使用します。</span><span class="sxs-lookup"><span data-stu-id="b2153-314">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="b2153-315">ボリューム GUID がないボリュームでのパスの変換を許可します。</span><span class="sxs-lookup"><span data-stu-id="b2153-315">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="b2153-316">ビルド 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b2153-316">Build 17738 (Fast)</span></span>
<span data-ttu-id="b2153-317">ビルド 17738 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-317">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-318">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-318">WSL</span></span>
* <span data-ttu-id="b2153-319">Setpriority システム コールのアクセス許可チェックが厳しすぎて、同じスレッドの優先順位を変更できません [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="b2153-319">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b2153-320">clock_gettime(CLOCK_BOOTTIME) に対して負値が返されないように、バイアスのかかっていない割り込み時間が起動時間に使用されていることを確認します [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="b2153-320">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b2153-321">WSL binfmt インタープリターでシンボリック リンクを処理します [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="b2153-321">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b2153-322">threadgroup リーダー ファイル記述子のクリーンアップの処理が改善されました。</span><span class="sxs-lookup"><span data-stu-id="b2153-322">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="b2153-323">ビルド 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b2153-323">Build 17728 (Fast)</span></span>
<span data-ttu-id="b2153-324">ビルド 17728 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-324">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-325">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-325">WSL</span></span>
* <span data-ttu-id="b2153-326">オーバーフローを回避するために、KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用するように WSL を切り替えます [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="b2153-326">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b2153-327">Ptrace のアタッチにより、システム コールから無効な戻り値が返される場合があります [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="b2153-327">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b2153-328">AF_UNIX に関連した複数の問題を修正します [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="b2153-328">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b2153-329">現在の作業ディレクトリが 5 文字未満の場合に WSL の相互運用が失敗する原因となる問題を修正します [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="b2153-329">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="b2153-330">ビルド 18204 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="b2153-330">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="b2153-331">ビルド 18204 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-331">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-332">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-332">WSL</span></span>
* <span data-ttu-id="b2153-333">エッジ トリガーされた epoll イベントをパイプ ファイルシステムが誤ってクリアします [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b2153-333">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b2153-334">NTFS シンボリック リンクによって起動された Win32 実行可能ファイルはシンボリック リンク名を考慮しません [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b2153-334">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="b2153-335">ビルド 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b2153-335">Build 17723 (Fast)</span></span>
<span data-ttu-id="b2153-336">ビルド 17723 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-336">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-337">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-337">WSL</span></span>
* <span data-ttu-id="b2153-338">存在しないポートへのループバック接続の失敗による 1 秒間の遅延を回避します [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="b2153-338">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b2153-339">/proc/sys/fs/file-max スタブ ファイルを追加します [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="b2153-339">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b2153-340">より正確な IPV6 スコープ情報。</span><span class="sxs-lookup"><span data-stu-id="b2153-340">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b2153-341">PR_SET_PTRACER のサポート [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="b2153-341">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b2153-342">エッジ トリガーされた epoll イベントをパイプ ファイルシステムが誤ってクリアします [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b2153-342">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b2153-343">NTFS シンボリック リンクによって起動された Win32 実行可能ファイルはシンボリック リンク名を考慮しません [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b2153-343">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="b2153-344">ビルド 17713</span><span class="sxs-lookup"><span data-stu-id="b2153-344">Build 17713</span></span>
<span data-ttu-id="b2153-345">ビルド 17713 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-345">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-346">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-346">WSL</span></span>
* <span data-ttu-id="b2153-347">ゾンビ サポートを強化しました [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="b2153-347">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b2153-348">Windows の相互運用の動作を制御するための wsl.conf エントリを追加します [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="b2153-348">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b2153-349">getsockname で必ずしも UNIX ソケット ファミリの種類が返されない問題を修正します [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="b2153-349">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b2153-350">TIOCSTI のサポートを追加します [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="b2153-350">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b2153-351">接続処理中のノンブロッキング ソケットは、書き込み試行に対して EAGAIN を返します [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="b2153-351">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b2153-352">マウントされた VHD での相互運用をサポートします [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="b2153-352">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b2153-353">ルート フォルダーでのアクセス許可チェックの問題を修正します [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="b2153-353">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b2153-354">TTY キーボードの ioctl (KDGKBTYPE、KDGKBMODE、および KDSKBMODE) に対する制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-354">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b2153-355">Windows UI アプリは、バックグラウンドで起動された場合でも実行されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-355">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="b2153-356">ビルド 17704</span><span class="sxs-lookup"><span data-stu-id="b2153-356">Build 17704</span></span>
<span data-ttu-id="b2153-357">ビルド 17704 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-357">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-358">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-358">WSL</span></span>
* <span data-ttu-id="b2153-359">wsl -u または --user オプションを追加します [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="b2153-359">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b2153-360">高速スタートアップが有効になっているときの WSL の起動問題を修正します [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="b2153-360">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b2153-361">UNIX ソケットは切断されたピア資格情報を保持する必要があります [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="b2153-361">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b2153-362">ノンブロッキング UNIX ソケットが EAGAIN で無限に失敗します [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="b2153-362">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b2153-363">case=off が、drvfs マウントの新しい既定の種類です [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="b2153-363">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b2153-364">詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-364">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b2153-365">実行中のディストリビューションを停止するための wslconfig /terminate を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-365">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="b2153-366">ビルド 17692</span><span class="sxs-lookup"><span data-stu-id="b2153-366">Build 17692</span></span>
<span data-ttu-id="b2153-367">ビルド 17692 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-367">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-368">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-368">WSL</span></span>
* <span data-ttu-id="b2153-369">スペースを含むパスを正しく処理しない WSL シェル コンテキスト メニュー エントリの問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-369">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b2153-370">ディレクトリごとの大文字と小文字の区別を拡張属性として公開します</span><span class="sxs-lookup"><span data-stu-id="b2153-370">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b2153-371">ARM64: キャッシュのメンテナンス操作をエミュレートします。</span><span class="sxs-lookup"><span data-stu-id="b2153-371">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b2153-372">[dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。</span><span class="sxs-lookup"><span data-stu-id="b2153-372">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b2153-373">DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみをエスケープ解除します。</span><span class="sxs-lookup"><span data-stu-id="b2153-373">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="b2153-374">ビルド 17686</span><span class="sxs-lookup"><span data-stu-id="b2153-374">Build 17686</span></span>
<span data-ttu-id="b2153-375">ビルド 17686 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-375">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-376">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-376">WSL</span></span>
* <span data-ttu-id="b2153-377">ELF パーサー インタープリターの長さの検証での Off-by-one エラーを修正します [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="b2153-377">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b2153-378">過去の時刻が設定された WSL 絶対タイマーは起動しません [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="b2153-378">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b2153-379">新しく作成された再解析ポイントが、親ディレクトリにそのように表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="b2153-379">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b2153-380">DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。</span><span class="sxs-lookup"><span data-stu-id="b2153-380">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="b2153-381">ビルド 17677</span><span class="sxs-lookup"><span data-stu-id="b2153-381">Build 17677</span></span>
<span data-ttu-id="b2153-382">ビルド 17677 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-382">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-383">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-383">WSL</span></span>
* <span data-ttu-id="b2153-384">ファイルが存在していてもマルチスレッドの操作で ENOENT が返される場合がある追加の問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-384">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b2153-385">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b2153-385">[GH 2712]</span></span>
* <span data-ttu-id="b2153-386">UMCI が有効になっているときの WSL の起動エラーを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-386">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b2153-387">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b2153-387">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="b2153-388">ビルド 17666</span><span class="sxs-lookup"><span data-stu-id="b2153-388">Build 17666</span></span>
<span data-ttu-id="b2153-389">ビルド 17666 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-389">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-390">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-390">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="b2153-391">警告:一部の AMD チップセットに WSL の実行を妨げる問題があります [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="b2153-391">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="b2153-392">修正は準備できており、間もなく Insider ビルド ブランチで公開されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-392">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="b2153-393">WSL を起動するエクスプローラーのコンテキスト メニューを追加します [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="b2153-393">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b2153-394">使用するには、エクスプローラー ウィンドウで Shift キーを押しながら右クリックします。</span><span class="sxs-lookup"><span data-stu-id="b2153-394">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b2153-395">UNIX ソケットのノンブロッキング動作を修正します [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="b2153-395">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b2153-396">GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-396">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b2153-397">マウント伝達フラグのサポートを追加します [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="b2153-397">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b2153-398">truncate で INotify イベントが発生しない問題を修正します [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="b2153-398">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b2153-399">シェルを使用せずに 1 つのバイナリを呼び出す wsl.exe の --exec オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-399">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b2153-400">特定のディストリビューションを選択する wsl.exe の --distribution オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-400">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="b2153-401">ビルド 17655 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="b2153-401">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="b2153-402">ビルド 17655 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-402">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-403">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-403">WSL</span></span>
* <span data-ttu-id="b2153-404">dmesg の制限付きサポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-404">Limited support for dmesg.</span></span> <span data-ttu-id="b2153-405">アプリケーションは、dmesg にログを記録できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-405">Applications can now log to dmesg.</span></span> <span data-ttu-id="b2153-406">WSL ドライバーは、限られた情報を dmesg に記録します。</span><span class="sxs-lookup"><span data-stu-id="b2153-406">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b2153-407">将来的には、ドライバーからのその他の情報や診断情報を伝達するように拡張できます。</span><span class="sxs-lookup"><span data-stu-id="b2153-407">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b2153-408">注: 現在、dmesg は `/dev/kmsg` デバイス インターフェイスを介してサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b2153-408">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b2153-409">`syslog` システム コール インターフェイスはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b2153-409">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="b2153-410">そのため、一部の `dmesg` コマンド ラインのオプション (`-S`、`-C` など) は機能しません。</span><span class="sxs-lookup"><span data-stu-id="b2153-410">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b2153-411">ファイルが存在している場合でもマルチスレッドの操作で ENOENT が返される場合がある問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-411">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b2153-412">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b2153-412">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="b2153-413">ビルド 17639 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="b2153-413">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="b2153-414">ビルド 17639 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-414">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-415">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-415">WSL</span></span>
* <span data-ttu-id="b2153-416">ネイティブに一致するように、シリアル デバイスの既定の gid とモードを変更します [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="b2153-416">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b2153-417">DrvFs で拡張属性がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-417">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b2153-418">注:DrvFs では、拡張属性の名前にいくつかの制限があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-418">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b2153-419">特に、一部の文字 ('/'、':'、'\*' など) は使用できません。また、拡張属性名は DrvFs では大文字と小文字が区別されません</span><span class="sxs-lookup"><span data-stu-id="b2153-419">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="b2153-420">ビルド 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b2153-420">Build 17133 (Fast)</span></span>
<span data-ttu-id="b2153-421">ビルド 17133 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-421">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-422">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-422">WSL</span></span>
* <span data-ttu-id="b2153-423">WSL でのハングの修正。</span><span class="sxs-lookup"><span data-stu-id="b2153-423">Fix for hang in WSL.</span></span> <span data-ttu-id="b2153-424">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="b2153-424">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="b2153-425">ビルド 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="b2153-425">Build 17128 (Fast)</span></span>
<span data-ttu-id="b2153-426">ビルド 17128 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-426">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-427">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-427">WSL</span></span>
* <span data-ttu-id="b2153-428">なし</span><span class="sxs-lookup"><span data-stu-id="b2153-428">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="b2153-429">ビルド 17627 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="b2153-429">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="b2153-430">ビルド 17627 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-430">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-431">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-431">WSL</span></span>
* <span data-ttu-id="b2153-432">futex の pi 対応操作のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-432">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="b2153-433">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="b2153-433">[GH 1006]</span></span>
    * <span data-ttu-id="b2153-434">優先順位は現在サポートされている WSL 機能ではないため、制限がありますが、標準の使用はブロック解除する必要がある点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-434">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="b2153-435">WSL プロセスに対する Windows ファイアウォールのサポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-435">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="b2153-436">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="b2153-436">[GH 1852]</span></span>
    * <span data-ttu-id="b2153-437">たとえば、WSL python プロセスが任意のポートでリッスンできるようにするには、次の管理者特権の Windows コマンドを使用します: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="b2153-437">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="b2153-438">ファイアウォール規則を追加する方法の詳細については、[リンク](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-438">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="b2153-439">WSL を使用するときにユーザーの既定のシェルを考慮します。</span><span class="sxs-lookup"><span data-stu-id="b2153-439">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="b2153-440">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="b2153-440">[GH 2372]</span></span>
* <span data-ttu-id="b2153-441">すべてのネットワーク インターフェイスをイーサネットとして報告します。</span><span class="sxs-lookup"><span data-stu-id="b2153-441">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="b2153-442">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="b2153-442">[GH 2996]</span></span>
* <span data-ttu-id="b2153-443">破損した /etc/passwd ファイルの処理が改善。</span><span class="sxs-lookup"><span data-stu-id="b2153-443">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="b2153-444">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="b2153-444">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="b2153-445">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-445">Console</span></span>
* <span data-ttu-id="b2153-446">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-446">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-447">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-447">LTP Results:</span></span>
<span data-ttu-id="b2153-448">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-448">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="b2153-449">ビルド 17618 (前へスキップ)</span><span class="sxs-lookup"><span data-stu-id="b2153-449">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="b2153-450">ビルド 17618 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-450">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-451">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-451">WSL</span></span>
* <span data-ttu-id="b2153-452">NT 相互運用のために pseudoconsole 機能を導入します [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="b2153-452">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="b2153-453">レガシ インストール メカニズム (lxrun.exe) は非推奨となりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-453">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="b2153-454">ディストリビューションをインストールするためのサポートされているメカニズムは、Microsoft Store 経由です。</span><span class="sxs-lookup"><span data-stu-id="b2153-454">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="b2153-455">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-455">Console</span></span>
* <span data-ttu-id="b2153-456">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-456">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-457">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-457">LTP Results:</span></span>
<span data-ttu-id="b2153-458">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-458">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="b2153-459">ビルド 17110</span><span class="sxs-lookup"><span data-stu-id="b2153-459">Build 17110</span></span>
<span data-ttu-id="b2153-460">ビルド 17110 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-460">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-461">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-461">WSL</span></span>
* <span data-ttu-id="b2153-462">/init を Windows から終了することを許可します [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="b2153-462">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="b2153-463">DrvFs では、ディレクトリごとの大文字小文字の区別が既定で使用されるようになりました ("case = dir" マウント オプションと同等)。</span><span class="sxs-lookup"><span data-stu-id="b2153-463">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="b2153-464">"case=force" (以前の動作) を使用するには、レジストリ キーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-464">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="b2153-465">“case=force” を使用する必要がある場合は、次のコマンドを実行して有効にします: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="b2153-465">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="b2153-466">以前のバージョンの Windows に含まれている WSL で作成された既存のディレクトリがあり、大文字と小文字を区別する必要がある場合は、次の fsutil.exe を使用して大文字と小文字を区別するように指定します: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="b2153-466">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="b2153-467">uname システム コールから NULL の終了文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-467">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="b2153-468">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-468">Console</span></span>
* <span data-ttu-id="b2153-469">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-469">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-470">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-470">LTP Results:</span></span>
<span data-ttu-id="b2153-471">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-471">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="b2153-472">ビルド 17107</span><span class="sxs-lookup"><span data-stu-id="b2153-472">Build 17107</span></span>
<span data-ttu-id="b2153-473">ビルド 17107 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-473">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-474">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-474">WSL</span></span>
* <span data-ttu-id="b2153-475">マスター pty エンドポイントで TCSETSF と TCSETSW をサポートします [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="b2153-475">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="b2153-476">相互運用プロセスを同時に開始すると、EINVAL が発生します [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="b2153-476">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="b2153-477">/proc/pid/status に適切なトレース状態を表示するように PTRACE_ATTACH を修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-477">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="b2153-478">CLEARTID フラグと SETTID フラグの両方を指定して複製された、有効期間の短いプロセスが、TID アドレスをクリアせずに終了する場合がある競合を修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-478">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="b2153-479">17093 より前のビルドから移行するときに、Linux ファイルシステムのディレクトリをアップグレードする際にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="b2153-479">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="b2153-480">17093 のファイルシステムの変更について詳しくは、[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) のリリース ノートを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-480">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="b2153-481">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-481">Console</span></span>
* <span data-ttu-id="b2153-482">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-482">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-483">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-483">LTP Results:</span></span>
<span data-ttu-id="b2153-484">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-484">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="b2153-485">ビルド 17101</span><span class="sxs-lookup"><span data-stu-id="b2153-485">Build 17101</span></span>
<span data-ttu-id="b2153-486">ビルド 17101 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-486">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-487">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-487">WSL</span></span>
* <span data-ttu-id="b2153-488">signalfd のサポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-488">Support for signalfd.</span></span> <span data-ttu-id="b2153-489">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="b2153-489">[GH 129]</span></span>
* <span data-ttu-id="b2153-490">無効な NTFS 文字を含むファイル名を、プライベート Unicode 文字としてエンコードすることによってサポートします。</span><span class="sxs-lookup"><span data-stu-id="b2153-490">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="b2153-491">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="b2153-491">[GH 1514]</span></span>
* <span data-ttu-id="b2153-492">書き込みがサポートされていない場合、自動マウントは読み取り専用にフォールバックします。</span><span class="sxs-lookup"><span data-stu-id="b2153-492">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="b2153-493">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="b2153-493">[GH 2603]</span></span>
* <span data-ttu-id="b2153-494">Unicode サロゲート ペア (絵文字など) の貼り付けを許可します。</span><span class="sxs-lookup"><span data-stu-id="b2153-494">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="b2153-495">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="b2153-495">[GH 2765]</span></span>
* <span data-ttu-id="b2153-496">/proc および /sys 内の疑似ファイルは、select、poll、epoll などから、読み書き可能を返します。[GH 2838]</span><span class="sxs-lookup"><span data-stu-id="b2153-496">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="b2153-497">レジストリが改ざんされているか破損している場合にサービスが無限ループに入る原因となる問題を修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-497">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="b2153-498">iproute2 の新しい (アップストリーム 4.14) バージョンで機能するように netlink メッセージを修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-498">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="b2153-499">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-499">Console</span></span>
* <span data-ttu-id="b2153-500">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-500">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-501">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-501">LTP Results:</span></span>
<span data-ttu-id="b2153-502">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-502">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="b2153-503">ビルド 17093</span><span class="sxs-lookup"><span data-stu-id="b2153-503">Build 17093</span></span>
<span data-ttu-id="b2153-504">ビルド 17093 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-504">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="b2153-505">重要:</span><span class="sxs-lookup"><span data-stu-id="b2153-505">Important:</span></span>
<span data-ttu-id="b2153-506">このビルドにアップグレードした後に初めて WSL を開始するときに、Linux ファイルシステムのディレクトリをアップグレードする作業を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-506">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="b2153-507">この処理には数分かかる場合があるため、WSL の開始に時間がかかっているように見えることがあります。</span><span class="sxs-lookup"><span data-stu-id="b2153-507">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="b2153-508">これは、ストアからインストールされた各ディストリビューションにつき 1 回のみ発生します。</span><span class="sxs-lookup"><span data-stu-id="b2153-508">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="b2153-509">DrvFs での大文字と小文字の区別のサポートを改善しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-509">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="b2153-510">DrvFs では、ディレクトリごとの大文字小文字の区別がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-510">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="b2153-511">これは、ディレクトリに設定できる新しいフラグで、これらのディレクトリ内のすべての操作を大文字と小文字を区別して扱う必要があることを示します。これにより、Windows アプリケーションでも、大文字と小文字のみが異なるファイルを正しく開くことが可能になります。</span><span class="sxs-lookup"><span data-stu-id="b2153-511">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="b2153-512">DrvFs には、ディレクトリごとに大文字と小文字の区別を制御する新しいマウント オプションがあります</span><span class="sxs-lookup"><span data-stu-id="b2153-512">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="b2153-513">case=force: すべてのディレクトリは、大文字小文字を区別して処理されます (ドライブのルートを除く)。</span><span class="sxs-lookup"><span data-stu-id="b2153-513">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="b2153-514">WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-514">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="b2153-515">これは、新しいディレクトリに大文字小文字を区別するようにマークを付けることを除き、従来の動作です。</span><span class="sxs-lookup"><span data-stu-id="b2153-515">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="b2153-516">case=dir: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは、大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="b2153-516">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b2153-517">WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-517">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="b2153-518">case=off: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは、大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="b2153-518">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b2153-519">WSL で作成された新しいディレクトリは、大文字と小文字を区別しないようにマークが付けられます。</span><span class="sxs-lookup"><span data-stu-id="b2153-519">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="b2153-520">注: 以前のリリースの WSL によって作成されたディレクトリにはこのフラグが設定されていないため、"case=dir" オプションを使用しても、大文字と小文字を区別して処理されません。</span><span class="sxs-lookup"><span data-stu-id="b2153-520">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="b2153-521">既存のディレクトリにこのフラグを設定する方法は、近日公開予定です。</span><span class="sxs-lookup"><span data-stu-id="b2153-521">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="b2153-522">これらのオプションを使用したマウントの例 (既存のドライブの場合、別のオプションを使用してマウントする前にマウントを解除する必要があります): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="b2153-522">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="b2153-523">現時点では、case=force がまだ既定のオプションです。</span><span class="sxs-lookup"><span data-stu-id="b2153-523">For now, case=force is still the default option.</span></span> <span data-ttu-id="b2153-524">これは将来、case=dir に変更されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-524">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="b2153-525">DrvFs をマウントするときに Windows パスでスラッシュを使用できるようになりました。例: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="b2153-525">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="b2153-526">WSL は、インスタンスの開始時に /etc/fstab ファイルを処理するようになりました [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="b2153-526">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="b2153-527">これは、DrvFs ドライブを自動的にマウントする前に行われます。fstab によって既にマウントされているドライブは自動的には再マウントされないため、特定のドライブのマウント ポイントを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b2153-527">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="b2153-528">この動作は、wsl.conf を使用して無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b2153-528">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="b2153-529">/proc 内の mount、mountinfo、および mountstats の各ファイルは、円記号やスペースなどの特殊文字を正しくエスケープ処理します [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="b2153-529">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="b2153-530">WSL シンボリック リンクなどの DrvFs で作成された特殊ファイル、またはメタデータが有効になっている場合の FIFO やソケットを、Windows からコピーおよび移動できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-530">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="b2153-531">WSL は、wsl.conf を使用してさらに構成可能です</span><span class="sxs-lookup"><span data-stu-id="b2153-531">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="b2153-532">サブシステムを起動するたびに適用される WSL の特定の機能を自動的に構成するための方法を追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-532">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="b2153-533">これには自動マウント オプションとネットワーク構成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2153-533">This includes automount options and network configuration.</span></span> <span data-ttu-id="b2153-534">詳細については、次のブログ投稿を参照してください: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="b2153-534">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="b2153-535">AF_UNIX により、WSL 上の Linux プロセスと Windows ネイティブ プロセス間のソケット接続が可能になります</span><span class="sxs-lookup"><span data-stu-id="b2153-535">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="b2153-536">WSL と Windows のアプリケーションは、UNIX ソケット経由で相互に通信できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-536">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="b2153-537">Windows でサービスを実行し、それを Windows と WSL の両方のアプリで使用できるようにする場合を考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="b2153-537">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="b2153-538">これは、UNIX ソケットを使用することで可能になりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-538">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="b2153-539">詳細については、次のブログ投稿をお読みください: https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="b2153-539">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-540">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-540">WSL</span></span>
* <span data-ttu-id="b2153-541">MAP_NORESERVE で mmap() をサポートします [GH 121、2784]</span><span class="sxs-lookup"><span data-stu-id="b2153-541">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="b2153-542">CLONE_PTRACE と CLONE_UNTRACED をサポートします [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="b2153-542">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="b2153-543">複製で SIGCHLD 以外の終了シグナルを処理します [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="b2153-543">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="b2153-544">/proc/sys/fs/inotify/max_user_instances および /proc/sys/fs/inotify/max_user_watches をスタブします [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="b2153-544">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="b2153-545">ゼロ以外のオフセットの読み込みヘッダーを含む ELF バイナリの読み込みエラー [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="b2153-545">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="b2153-546">イメージを読み込むときにページの末尾バイトをゼロ設定します。</span><span class="sxs-lookup"><span data-stu-id="b2153-546">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="b2153-547">execve が警告なしにプロセスを終了するケースを削減します</span><span class="sxs-lookup"><span data-stu-id="b2153-547">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="b2153-548">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-548">Console</span></span>
* <span data-ttu-id="b2153-549">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-549">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-550">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-550">LTP Results:</span></span>
<span data-ttu-id="b2153-551">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-551">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="b2153-552">ビルド 17083</span><span class="sxs-lookup"><span data-stu-id="b2153-552">Build 17083</span></span>
<span data-ttu-id="b2153-553">ビルド 17083 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-553">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-554">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-554">WSL</span></span>
* <span data-ttu-id="b2153-555">epoll に関連したバグチェックを修正しました [GH 2798、2801、2857]</span><span class="sxs-lookup"><span data-stu-id="b2153-555">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="b2153-556">ASLR をオフにする際のハングを修正しました [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="b2153-556">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="b2153-557">mmap 操作がアトミックに見えるようにします [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="b2153-557">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="b2153-558">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-558">Console</span></span>
* <span data-ttu-id="b2153-559">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-559">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-560">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-560">LTP Results:</span></span>
<span data-ttu-id="b2153-561">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-561">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="b2153-562">ビルド 17074</span><span class="sxs-lookup"><span data-stu-id="b2153-562">Build 17074</span></span>
<span data-ttu-id="b2153-563">ビルド 17074 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-563">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-564">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-564">WSL</span></span>
* <span data-ttu-id="b2153-565">DrvFs メタデータのストレージ形式を修正しました [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="b2153-565">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="b2153-566">**重要:** このビルドより前に作成された DrvFs メタデータは、正しく表示されないか、まったく表示されません。</span><span class="sxs-lookup"><span data-stu-id="b2153-566">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="b2153-567">影響を受けるファイルを修正するには、chmod と chown を使用してメタデータを再適用します。</span><span class="sxs-lookup"><span data-stu-id="b2153-567">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="b2153-568">複数のシグナルと再開可能なシステム コールの問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-568">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="b2153-569">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-569">Console</span></span>
* <span data-ttu-id="b2153-570">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-570">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-571">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-571">LTP Results:</span></span>
<span data-ttu-id="b2153-572">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-572">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="b2153-573">ビルド 17063</span><span class="sxs-lookup"><span data-stu-id="b2153-573">Build 17063</span></span>
<span data-ttu-id="b2153-574">ビルド 17063 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-574">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b2153-575">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-575">WSL</span></span>
* <span data-ttu-id="b2153-576">DrvFs で追加の Linux メタデータがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b2153-576">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="b2153-577">これにより、chmod/chown を使用してファイルの所有者とモードを設定できるほか、FIFO、UNIX ソケット、デバイス ファイルなどの特殊ファイルを作成することも可能になります。</span><span class="sxs-lookup"><span data-stu-id="b2153-577">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="b2153-578">現時点では、これはまだ試験段階のため、既定では無効になっています。</span><span class="sxs-lookup"><span data-stu-id="b2153-578">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="b2153-579">**注:** DrvFs で使用されるメタデータ形式のバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-579">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="b2153-580">メタデータは実験のためにこのビルドでは機能しますが、今後のビルドでは、このビルドで作成されたメタデータは正しく読み取られません。</span><span class="sxs-lookup"><span data-stu-id="b2153-580">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="b2153-581">変更したファイルの所有者を手動で更新する必要がある場合があり、カスタム デバイス ID を持つデバイスは再作成しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b2153-581">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="b2153-582">有効にするには、メタデータ オプションを使用して DrvFs をマウントします (既存のマウントで有効にするには、最初にマウントを解除する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="b2153-582">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="b2153-583">Linux のアクセス許可は、追加のメタデータとしてファイルに追加されます。Windows のアクセス許可には影響はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-583">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="b2153-584">Windows エディターを使用してファイルを編集すると、メタデータが削除されることがありますので注意してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-584">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="b2153-585">この場合、そのファイルは既定のアクセス許可に戻ります。</span><span class="sxs-lookup"><span data-stu-id="b2153-585">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="b2153-586">メタデータなしでファイルを制御するためのマウント オプションを DrvFs に追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-586">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="b2153-587">uid: 全ファイルの所有者に使用されるユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="b2153-587">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b2153-588">gid: 全ファイルの所有者に使用されるグループ ID。</span><span class="sxs-lookup"><span data-stu-id="b2153-588">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b2153-589">umask: 全ファイルとディレクトリに対して除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="b2153-589">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="b2153-590">fmask: すべての標準ファイルに対して除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="b2153-590">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="b2153-591">dmask: 全ディレクトリに対して除外するアクセス許可の 8 進数のマスク。</span><span class="sxs-lookup"><span data-stu-id="b2153-591">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="b2153-592">次に、例を示します。</span><span class="sxs-lookup"><span data-stu-id="b2153-592">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="b2153-593">メタデータ オプションと組み合わせて、メタデータのないファイルに対する既定のアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2153-593">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="b2153-594">WSL と Win32 の間で環境変数がどのように流れるかを構成するために、新しい環境変数 `WSLENV` を導入しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-594">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="b2153-595">次に、例を示します。</span><span class="sxs-lookup"><span data-stu-id="b2153-595">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="b2153-596">`WSLENV` は、Win32 から WSL プロセスを起動するとき、または WSL から Win32 プロセスを起動するときに含めることができる環境変数のコロン区切りリストです。</span><span class="sxs-lookup"><span data-stu-id="b2153-596">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="b2153-597">各変数の末尾にはスラッシュを付け、その後に、変換方法を指定するフラグを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b2153-597">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="b2153-598">p:この値は、WSL パスと Win32 パスの間で変換されるパスです。</span><span class="sxs-lookup"><span data-stu-id="b2153-598">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="b2153-599">l:この値は、パスのリストです。</span><span class="sxs-lookup"><span data-stu-id="b2153-599">l: The value is a list of paths.</span></span> <span data-ttu-id="b2153-600">WSL では、コロンで区切られたリストです。</span><span class="sxs-lookup"><span data-stu-id="b2153-600">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="b2153-601">Win32 では、セミコロンで区切られたリストです。</span><span class="sxs-lookup"><span data-stu-id="b2153-601">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="b2153-602">u:この値は、Win32 から WSL を呼び出すときにのみ含める必要があります</span><span class="sxs-lookup"><span data-stu-id="b2153-602">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="b2153-603">w:この値は、WSL から Win32 を呼び出すときにのみ含める必要があります</span><span class="sxs-lookup"><span data-stu-id="b2153-603">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="b2153-604">.bashrc またはユーザーのカスタム Windows 環境で `WSLENV` を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b2153-604">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="b2153-605">drvfs マウントは、tar、cp -p からのタイムスタンプを正しく保持します (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="b2153-605">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="b2153-606">drvfs シンボリック リンクは正しいサイズを報告します (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="b2153-606">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="b2153-607">非常に大きい IO サイズに対して読み取り/書き込みが機能します (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="b2153-607">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="b2153-608">waitpid はプロセス グループ ID で機能します (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="b2153-608">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="b2153-609">大きな予約領域での mmap のパフォーマンスが大幅に改善しました。ghc のパフォーマンスが改善します (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="b2153-609">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="b2153-610">READ_IMPLIES_EXEC のパーソナリティ サポート。maxima および clisp を修正します (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="b2153-610">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="b2153-611">mprotect で PROT_GROWSDOWN がサポートされます。clisp を修正します (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="b2153-611">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="b2153-612">オーバーコミット モードでのページ フォールトの修正。sbcl の修正 (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="b2153-612">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="b2153-613">clone でより多くのフラグの組み合わせがサポートされます</span><span class="sxs-lookup"><span data-stu-id="b2153-613">clone supports more flags combinations</span></span>
* <span data-ttu-id="b2153-614">epoll ファイルの select/epoll をサポートします (以前は操作なし)。</span><span class="sxs-lookup"><span data-stu-id="b2153-614">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="b2153-615">未実装のシステム コールの ptrace を通知します。</span><span class="sxs-lookup"><span data-stu-id="b2153-615">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="b2153-616">resolv.conf ネームサーバーを生成しているときに実行されていないインターフェイスを無視します [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="b2153-616">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="b2153-617">物理アドレスのないネットワーク インターフェイスを列挙します。</span><span class="sxs-lookup"><span data-stu-id="b2153-617">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="b2153-618">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="b2153-618">[GH 2685]</span></span>
* <span data-ttu-id="b2153-619">その他のバグ修正と機能強化。</span><span class="sxs-lookup"><span data-stu-id="b2153-619">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="b2153-620">開発者は Windows 上で Linux ツールを利用できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-620">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="b2153-621">Windows コマンド ライン ツールチェーンに、bsdtar (tar) と curl が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2153-621">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="b2153-622">これらの 2 つの新しいツールの追加に関する詳細と、それを使った Windows での開発者エクスペリエンスの形成については、[こちらのブログ](https://aka.ms/tarcurlwindows)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-622">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="b2153-623">`AF_UNIX` は、Windows Insider SDK (17061+) で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="b2153-623">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="b2153-624">`AF_UNIX` の詳細と、Windows 上で開発者がそれをどのように使用できるかについては、[こちらのブログ](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)をお読みください。</span><span class="sxs-lookup"><span data-stu-id="b2153-624">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="b2153-625">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-625">Console</span></span>
* <span data-ttu-id="b2153-626">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-626">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-627">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-627">LTP Results:</span></span>
<span data-ttu-id="b2153-628">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-628">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="b2153-629">ビルド 17046</span><span class="sxs-lookup"><span data-stu-id="b2153-629">Build 17046</span></span>

<span data-ttu-id="b2153-630">ビルド 17046 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-630">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="b2153-631">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-631">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-632">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-632">WSL</span></span>
- <span data-ttu-id="b2153-633">アクティブ ターミナルなしでプロセスの実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="b2153-633">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="b2153-634">[GH 709、1007、1511、2252、2391 など]</span><span class="sxs-lookup"><span data-stu-id="b2153-634">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="b2153-635">CLONE_VFORK および CLONE_VM のサポートの強化。</span><span class="sxs-lookup"><span data-stu-id="b2153-635">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="b2153-636">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="b2153-636">[GH 1878, 2615]</span></span>
- <span data-ttu-id="b2153-637">WSL ネットワーク操作で TDI フィルター ドライバーをスキップします。</span><span class="sxs-lookup"><span data-stu-id="b2153-637">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="b2153-638">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="b2153-638">[GH 1554]</span></span>
- <span data-ttu-id="b2153-639">DrvFs は、特定の条件に適合したときに NT シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="b2153-639">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="b2153-640">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="b2153-640">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="b2153-641">リンク対象は、相対パスである必要があり、マウント ポイントやシンボリック リンクと交差してはならず、存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-641">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="b2153-642">開発者モードが有効になっていない場合、ユーザーは SE_CREATE_SYMBOLIC_LINK_PRIVILEGE を持っている必要があります (このためには、通常、管理者特権で wsl.exe を起動する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="b2153-642">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="b2153-643">それ以外の状況でも、DrvFs は WSL シンボリック リンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="b2153-643">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="b2153-644">管理者特権と非管理者特権での WSL インスタンスの同時実行を許可します。</span><span class="sxs-lookup"><span data-stu-id="b2153-644">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="b2153-645">/proc/sys/kernel/yama/ptrace_scope をサポートします</span><span class="sxs-lookup"><span data-stu-id="b2153-645">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="b2153-646">WSL<->Windows のパスの変換を実行するために wslpath を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-646">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="b2153-647">[GH 522、1243、1834、2327 など]</span><span class="sxs-lookup"><span data-stu-id="b2153-647">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="b2153-648">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-648">Console</span></span>
- <span data-ttu-id="b2153-649">修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-649">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-650">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-650">LTP Results:</span></span>
<span data-ttu-id="b2153-651">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-651">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="b2153-652">ビルド 17040</span><span class="sxs-lookup"><span data-stu-id="b2153-652">Build 17040</span></span>

<span data-ttu-id="b2153-653">ビルド 17040 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-653">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-654">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-655">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-655">WSL</span></span>
- <span data-ttu-id="b2153-656">17035 以降修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-656">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-657">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-657">Console</span></span>
- <span data-ttu-id="b2153-658">17035 以降修正なし。</span><span class="sxs-lookup"><span data-stu-id="b2153-658">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-659">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-659">LTP Results:</span></span>
<span data-ttu-id="b2153-660">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-660">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="b2153-661">ビルド 17035</span><span class="sxs-lookup"><span data-stu-id="b2153-661">Build 17035</span></span>

<span data-ttu-id="b2153-662">ビルド 17035 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-662">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-663">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-663">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-664">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-664">WSL</span></span>
- <span data-ttu-id="b2153-665">DrvFs 上のファイルにアクセスすると、時々 EINVAL で失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="b2153-665">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="b2153-666">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="b2153-666">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-667">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-667">Console</span></span>
- <span data-ttu-id="b2153-668">VT モードで行を挿入または削除するときに一部の色が失われます。</span><span class="sxs-lookup"><span data-stu-id="b2153-668">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-669">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-669">LTP Results:</span></span>
<span data-ttu-id="b2153-670">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-670">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="b2153-671">ビルド 17025</span><span class="sxs-lookup"><span data-stu-id="b2153-671">Build 17025</span></span>

<span data-ttu-id="b2153-672">ビルド 17025 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-672">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-673">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-674">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-674">WSL</span></span>
- <span data-ttu-id="b2153-675">新しいフォアグラウンド プロセス グループで初期プロセスを開始します [GH 1653、2510]。</span><span class="sxs-lookup"><span data-stu-id="b2153-675">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="b2153-676">SIGHUP 配信の修正 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="b2153-676">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="b2153-677">指定されていない場合、既定の仮想ブリッジ名を生成します [GH 2497]。</span><span class="sxs-lookup"><span data-stu-id="b2153-677">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="b2153-678">/proc/sys/kernel/random/boot_id を実装します [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="b2153-678">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="b2153-679">追加の相互運用 stdout/stderr パイプの修正。</span><span class="sxs-lookup"><span data-stu-id="b2153-679">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="b2153-680">syncfs システム コールをスタブします。</span><span class="sxs-lookup"><span data-stu-id="b2153-680">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-681">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-681">Console</span></span>
- <span data-ttu-id="b2153-682">サード パーティ コンソールの入力 VT 変換を修正します [GH 111]</span><span class="sxs-lookup"><span data-stu-id="b2153-682">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-683">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-683">LTP Results:</span></span>
<span data-ttu-id="b2153-684">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-684">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="b2153-685">ビルド 17017</span><span class="sxs-lookup"><span data-stu-id="b2153-685">Build 17017</span></span>

<span data-ttu-id="b2153-686">ビルド 17017 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-686">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-687">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-687">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-688">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-688">WSL</span></span>
- <span data-ttu-id="b2153-689">空の ELF プログラム ヘッダーを無視します [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="b2153-689">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="b2153-690">LxssManager が非対話型ユーザーに対して WSL インスタンスを作成することを許可します (ssh およびスケジュールされたタスクのサポート) [GH 777、1602]。</span><span class="sxs-lookup"><span data-stu-id="b2153-690">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="b2153-691">WSL->Win32-> WSL ("開始") シナリオをサポートします [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="b2153-691">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="b2153-692">相互運用によって起動されたコンソール アプリの終了に対する制限付きサポート [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="b2153-692">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="b2153-693">devpts のマウント オプションをサポートします [GH 1948]。</span><span class="sxs-lookup"><span data-stu-id="b2153-693">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="b2153-694">Ptrace が子のスタートアップをブロックします [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="b2153-694">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="b2153-695">EPOLLET で一部のイベントが欠落します [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="b2153-695">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="b2153-696">PTRACE_GETSIGINFO でより多くのデータが返されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-696">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="b2153-697">lseek を指定した Getdents により、誤った結果が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-697">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="b2153-698">これ以上データがないパイプで入力を待機することによる、いくつかの Win32 相互運用アプリのハングを修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-698">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="b2153-699">tty/pty ファイルに対する O_ASYNC サポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-699">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="b2153-700">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-700">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-701">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-701">Console</span></span>
- <span data-ttu-id="b2153-702">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-702">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-703">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-703">LTP Results:</span></span>
<span data-ttu-id="b2153-704">テストを実行中。</span><span class="sxs-lookup"><span data-stu-id="b2153-704">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="b2153-705">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="b2153-705">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="b2153-706">ビルド 16288</span><span class="sxs-lookup"><span data-stu-id="b2153-706">Build 16288</span></span>

<span data-ttu-id="b2153-707">ビルド 16288 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-707">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-708">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-709">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-709">WSL</span></span>
- <span data-ttu-id="b2153-710">ソケット ファイル記述子の uid、gid、およびモードを正しく初期化して報告します [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="b2153-710">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="b2153-711">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-711">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-712">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-712">Console</span></span>
- <span data-ttu-id="b2153-713">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-713">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-714">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-714">LTP Results:</span></span>
<span data-ttu-id="b2153-715">16273 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="b2153-715">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="b2153-716">ビルド 16278</span><span class="sxs-lookup"><span data-stu-id="b2153-716">Build 16278</span></span>

<span data-ttu-id="b2153-717">ビルド 162738 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-717">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-718">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-718">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-719">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-719">WSL</span></span>
- <span data-ttu-id="b2153-720">LX MM 状態を解除するときに、ファイルによってサポートされているセクションのマップされたビューを明示的にマップ解除します [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="b2153-720">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="b2153-721">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-721">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-722">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-722">Console</span></span>
- <span data-ttu-id="b2153-723">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-723">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-724">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-724">LTP Results:</span></span>
<span data-ttu-id="b2153-725">16273 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="b2153-725">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="b2153-726">ビルド 16275</span><span class="sxs-lookup"><span data-stu-id="b2153-726">Build 16275</span></span>

<span data-ttu-id="b2153-727">ビルド 162735 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-727">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-728">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-729">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-729">WSL</span></span>
- <span data-ttu-id="b2153-730">このリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-730">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-731">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-731">Console</span></span>
- <span data-ttu-id="b2153-732">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-732">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-733">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-733">LTP Results:</span></span>
<span data-ttu-id="b2153-734">16273 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="b2153-734">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="b2153-735">ビルド 16273</span><span class="sxs-lookup"><span data-stu-id="b2153-735">Build 16273</span></span>

<span data-ttu-id="b2153-736">ビルド 16273 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-736">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-737">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-737">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-738">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-738">WSL</span></span>
- <span data-ttu-id="b2153-739">DrvFs がディレクトリに対して間違ったファイルの種類を報告することがあった問題を修正しました [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="b2153-739">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="b2153-740">uevent を使用するプログラムのブロックを解除するために NETLINK_KOBJECT_UEVENT ソケットの作成を許可します [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="b2153-740">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="b2153-741">ノンブロッキング接続のサポートを追加します [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="b2153-741">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="b2153-742">CLONE_FS clone システム コール フラグを実装します [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="b2153-742">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="b2153-743">NT 相互運用でタブや引用符が正しく処理されないことに関する問題を修正します [GH 1625、2164]</span><span class="sxs-lookup"><span data-stu-id="b2153-743">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="b2153-744">WSL インスタンスを再起動しようとしたときにアクセスが拒否されるエラーを解決します [GH 651、2095]</span><span class="sxs-lookup"><span data-stu-id="b2153-744">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="b2153-745">futex の FUTEX_REQUEUE 操作と FUTEX_CMP_REQUEUE 操作を実装します [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="b2153-745">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="b2153-746">さまざまな SysFs ファイルのアクセス許可を修正します [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="b2153-746">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="b2153-747">セットアップ中の Haskell スタックのハングを修正します [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="b2153-747">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="b2153-748">binfmt_misc の 'C'、'O'、および 'P' のフラグを実装します [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="b2153-748">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="b2153-749">/proc/sys/kernel /shmmax /shmmni & /threads-max を追加します [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="b2153-749">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="b2153-750">ioprio_set システム コールの部分的サポートを追加します [GH 498]</span><span class="sxs-lookup"><span data-stu-id="b2153-750">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="b2153-751">SO_REUSEPORT をスタブし、netlink ソケットに対する SO_PASSCRED のサポートを追加します [GH 69]</span><span class="sxs-lookup"><span data-stu-id="b2153-751">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="b2153-752">ディストリビューションを現在インストールまたはアンインストールしている場合に、RegisterDistribuiton から別のエラー コードが返されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-752">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="b2153-753">wslconfig.exe によって部分的にインストールされた WSL ディストリビューションの登録解除を許可します</span><span class="sxs-lookup"><span data-stu-id="b2153-753">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="b2153-754">udp::msg_peek からの python ソケット テストのハングを修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-754">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="b2153-755">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-755">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-756">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-756">Console</span></span>
- <span data-ttu-id="b2153-757">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-757">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-758">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-758">LTP Results:</span></span>
<span data-ttu-id="b2153-759">テストの合計:1904</span><span class="sxs-lookup"><span data-stu-id="b2153-759">Total Tests: 1904</span></span><br/>
<span data-ttu-id="b2153-760">スキップされたテストの合計:209</span><span class="sxs-lookup"><span data-stu-id="b2153-760">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="b2153-761">失敗の合計:229</span><span class="sxs-lookup"><span data-stu-id="b2153-761">Total Failures: 229</span></span><br/>
[<span data-ttu-id="b2153-762">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-762">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="b2153-763">ビルド 16257</span><span class="sxs-lookup"><span data-stu-id="b2153-763">Build 16257</span></span>

<span data-ttu-id="b2153-764">ビルド 16257 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-764">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-765">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-765">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-766">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-766">WSL</span></span>
- <span data-ttu-id="b2153-767">prlimit64 システム コールを実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-767">Implement prlimit64 system call</span></span>
- <span data-ttu-id="b2153-768">ulimit -n (setrlimit RLIMIT_NOFILE) に対するサポートを追加します [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="b2153-768">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="b2153-769">TCP ソケットに対して MSG_MORE をスタブします [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="b2153-769">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="b2153-770">無効な AT_EXECFN 補助ベクトルの動作を修正します [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="b2153-770">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="b2153-771">console/tty のコピー/貼り付けの動作を修正し、改善された完全バッファー処理を追加します [GH 2204、2131]</span><span class="sxs-lookup"><span data-stu-id="b2153-771">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="b2153-772">set-user-ID プログラムと set-group-ID プログラムの補助ベクトルに AT_SECURE を設定します [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="b2153-772">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="b2153-773">疑似ターミナルのマスター エンドポイントが TIOCPGRP を処理しません [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="b2153-773">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="b2153-774">LxFs でのディレクトリの巻き戻しについて lseek を修正します [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="b2153-774">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="b2153-775">高い使用率の後に /dev/ptmx がロックします [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="b2153-775">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="b2153-776">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-776">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-777">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-777">Console</span></span>
- <span data-ttu-id="b2153-778">すべての場所での横線とアンダースコアの修正 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="b2153-778">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="b2153-779">プロセス順序の変更により NPM のクローズが困難になった問題の修正 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="b2153-779">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="b2153-780">新しいカラー スキームを追加しました: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="b2153-780">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-781">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-781">LTP Results:</span></span>
<span data-ttu-id="b2153-782">16251 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="b2153-782">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-783">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-783">Syscall Support</span></span>
<span data-ttu-id="b2153-784">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-784">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-785">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-785">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="b2153-786">の既知の問題</span><span class="sxs-lookup"><span data-stu-id="b2153-786">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="b2153-787">GitHub の問題 2392:Windows フォルダーが WSL によって認識されない...</span><span class="sxs-lookup"><span data-stu-id="b2153-787">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="b2153-788">ビルド 16257 で、WSL には、`/mnt/c/...` を介して Windows ファイル/フォルダーを列挙するときに問題があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-788">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="b2153-789">この問題は修正済みであり、2017 年 8 月 14 日から始まる週の間に Insiders ビルドでリリースされます。</span><span class="sxs-lookup"><span data-stu-id="b2153-789">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="b2153-790">ビルド 16251</span><span class="sxs-lookup"><span data-stu-id="b2153-790">Build 16251</span></span>

<span data-ttu-id="b2153-791">ビルド 16251 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-791">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-792">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-792">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-793">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-793">WSL</span></span>
- <span data-ttu-id="b2153-794">WSL のオプション コンポーネントからベータ タグを削除します。詳細については、[ブログ投稿](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-794">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="b2153-795">exec で set-user-ID と set-group-ID のバイナリに対して保存されている set uid と gid を正しく初期化します [GH 962、1415、2072]</span><span class="sxs-lookup"><span data-stu-id="b2153-795">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="b2153-796">ptrace PTRACE_O_TRACEEXIT に対するサポートを追加しました [GH 555]</span><span class="sxs-lookup"><span data-stu-id="b2153-796">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="b2153-797">ptrace PTRACE_GETFPREGS と PTRACE_GETREGSET (NT_FPREGSET を使用) に対するサポートを追加しました [GH 555]</span><span class="sxs-lookup"><span data-stu-id="b2153-797">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="b2153-798">無視されたシグナルでの停止について ptrace を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-798">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="b2153-799">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-799">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-800">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-800">Console</span></span>
- <span data-ttu-id="b2153-801">このリリースでは、コンソールに関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-801">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-802">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-802">LTP Results:</span></span>
<span data-ttu-id="b2153-803">合格したテストの数:768</span><span class="sxs-lookup"><span data-stu-id="b2153-803">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="b2153-804">失敗したテストの数:244</span><span class="sxs-lookup"><span data-stu-id="b2153-804">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="b2153-805">スキップされたテストの数:96</span><span class="sxs-lookup"><span data-stu-id="b2153-805">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="b2153-806">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-806">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="b2153-807">ビルド 16241</span><span class="sxs-lookup"><span data-stu-id="b2153-807">Build 16241</span></span>

<span data-ttu-id="b2153-808">ビルド 16241 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-808">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-809">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-809">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b2153-810">WSL</span><span class="sxs-lookup"><span data-stu-id="b2153-810">WSL</span></span>
- <span data-ttu-id="b2153-811">このリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-811">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b2153-812">Console</span><span class="sxs-lookup"><span data-stu-id="b2153-812">Console</span></span>
- <span data-ttu-id="b2153-813">[こちら](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)で最初に報告された、交差行の DEC に対して誤った文字が出力されることの修正</span><span class="sxs-lookup"><span data-stu-id="b2153-813">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="b2153-814">コード ページ 65001 (utf8) に出力テキストが表示されないことの修正</span><span class="sxs-lookup"><span data-stu-id="b2153-814">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="b2153-815">ある色の RGB 値に対して行われた変更を、選択の変更時にパレットの他の部分に転送しないでください。</span><span class="sxs-lookup"><span data-stu-id="b2153-815">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="b2153-816">これにより、コンソール プロパティ シートがずっと使いやすくなります。</span><span class="sxs-lookup"><span data-stu-id="b2153-816">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="b2153-817">Ctrl+S が正しく機能していないように見えます</span><span class="sxs-lookup"><span data-stu-id="b2153-817">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="b2153-818">Un-Bold/-Dim が ANSI エスケープ コードにまったく存在しません [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="b2153-818">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="b2153-819">コンソールで Vim の色のテーマが正しくサポートされていません [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="b2153-819">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="b2153-820">特定の文字を貼り付けられません [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="b2153-820">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="b2153-821">編集/コマンド ライン上に存在するときに、bash ウィンドウのサイズ変更で、サイズ変更のリフローの操作が正しく行われません [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="b2153-821">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="b2153-822">Ctrl-L を押しても画面はダーティな状態のままです [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="b2153-822">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="b2153-823">HDPI に VT を表示する際のコンソール レンダリングのバグ [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="b2153-823">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="b2153-824">Unicode 文字 U+30FB で日本語の文字が正しく表示されません [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="b2153-824">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="b2153-825">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-825">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="b2153-826">ビルド 16237</span><span class="sxs-lookup"><span data-stu-id="b2153-826">Build 16237</span></span>

<span data-ttu-id="b2153-827">ビルド 16237 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-827">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-828">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-828">Fixed</span></span>
- <span data-ttu-id="b2153-829">LxFs で EA がないファイルには既定の属性を使用します (root、root、0000)</span><span class="sxs-lookup"><span data-stu-id="b2153-829">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="b2153-830">拡張属性を使用するディストリビューションのサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-830">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="b2153-831">getdents と getdents64 によって返されるエントリのパディングを修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-831">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="b2153-832">shmctl SHM_STAT システム コールのアクセス許可チェックを修正します [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="b2153-832">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="b2153-833">tty の正しくない初期 epoll 状態を修正しました [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="b2153-833">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="b2153-834">DrvFs readdir ですべてのエントリが返されない問題を修正します [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="b2153-834">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="b2153-835">ファイルのリンクが解除されているときの LxFs readdir を修正します [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="b2153-835">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="b2153-836">リンクが解除されている drvfs ファイルを procfs を介して再オープンできるようにします</span><span class="sxs-lookup"><span data-stu-id="b2153-836">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="b2153-837">WSL の機能を無効にするためのグローバル レジストリ キー オーバーライドを追加しました (相互運用/ドライブのマウント)</span><span class="sxs-lookup"><span data-stu-id="b2153-837">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="b2153-838">DrvFs (および LxFs) の "stat" での間違ったブロック カウントを修正します [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="b2153-838">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="b2153-839">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-839">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="b2153-840">ビルド 16232</span><span class="sxs-lookup"><span data-stu-id="b2153-840">Build 16232</span></span>

<span data-ttu-id="b2153-841">ビルド 16232 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-841">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-842">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-842">Fixed</span></span>
- <span data-ttu-id="b2153-843">このリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-843">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="b2153-844">ビルド 16226</span><span class="sxs-lookup"><span data-stu-id="b2153-844">Build 16226</span></span>

<span data-ttu-id="b2153-845">ビルド 16226 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-845">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-846">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-846">Fixed</span></span>
- <span data-ttu-id="b2153-847">xattr に関連したシステム コールのサポート (getxattr、setxattr、listxattr、removexattr)。</span><span class="sxs-lookup"><span data-stu-id="b2153-847">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="b2153-848">security.capablity xattr のサポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-848">security.capablity xattr support.</span></span>
- <span data-ttu-id="b2153-849">特定のファイルシステムとフィルター (MS 以外の SMB サーバーを含む) との互換性を改善しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-849">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="b2153-850">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="b2153-850">[GH #1952]</span></span>
- <span data-ttu-id="b2153-851">OneDrive プレースホルダー、GVFS プレースホルダー、および Compact OS 圧縮ファイルのサポートを強化しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-851">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="b2153-852">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-852">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="b2153-853">ビルド 16215</span><span class="sxs-lookup"><span data-stu-id="b2153-853">Build 16215</span></span>

<span data-ttu-id="b2153-854">ビルド 16215 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-854">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-855">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-855">Fixed</span></span>
- <span data-ttu-id="b2153-856">WSL で開発者モードが不要になりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-856">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="b2153-857">drvfs でディレクトリ ジャンクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b2153-857">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="b2153-858">WSL ディストリビューション appx パッケージのアンインストールを処理します。</span><span class="sxs-lookup"><span data-stu-id="b2153-858">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="b2153-859">プライベート マッピングと共有マッピングを表示するように procfs を更新します。</span><span class="sxs-lookup"><span data-stu-id="b2153-859">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="b2153-860">部分的にインストールまたはアンインストールされたディストリビューションをクリーンアップする wslconfig.exe の機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-860">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="b2153-861">TCP ソケットに対する IP_MTU_DISCOVER のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-861">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="b2153-862">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="b2153-862">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="b2153-863">AF_INADDR へのルート用のプロトコル ファミリを推測します。</span><span class="sxs-lookup"><span data-stu-id="b2153-863">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="b2153-864">シリアル デバイスの機能強化 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="b2153-864">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="b2153-865">ビルド 16199</span><span class="sxs-lookup"><span data-stu-id="b2153-865">Build 16199</span></span>

<span data-ttu-id="b2153-866">ビルド 16199 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-866">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-867">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-867">Fixed</span></span>
- <span data-ttu-id="b2153-868">これらのリリースでは、WSL に関連する変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-868">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="b2153-869">ビルド 16193</span><span class="sxs-lookup"><span data-stu-id="b2153-869">Build 16193</span></span>

<span data-ttu-id="b2153-870">ビルド 16193 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-870">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-871">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-871">Fixed</span></span>
- <span data-ttu-id="b2153-872">SIGCONT の送信と threadgroup の終了との間の競合状態 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="b2153-872">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="b2153-873">FILE_DEVICE_CONSOLE ではなく FILE_DEVICE_NAMED_PIPE を報告するように tty デバイスと pty デバイスを変更します [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="b2153-873">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="b2153-874">IP_OPTIONS の SSH 修正</span><span class="sxs-lookup"><span data-stu-id="b2153-874">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="b2153-875">DrvFs のマウントを init デーモンに移動しました [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="b2153-875">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="b2153-876">後続の NT シンボリック リンクに対するサポートを DrvFs に追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-876">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="b2153-877">ビルド 16184</span><span class="sxs-lookup"><span data-stu-id="b2153-877">Build 16184</span></span>

<span data-ttu-id="b2153-878">ビルド 16184 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-878">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-879">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-879">Fixed</span></span>
- <span data-ttu-id="b2153-880">apt パッケージのメンテナンス タスク (lxrun.exe/update) を削除しました</span><span class="sxs-lookup"><span data-stu-id="b2153-880">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="b2153-881">Node.js の Windows プロセスから出力が表示されない問題を修正しました [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="b2153-881">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="b2153-882">lxcore での配置要件を緩和します [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="b2153-882">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="b2153-883">複数のシステム コールで AT_EMPTY_PATH フラグの処理を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-883">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="b2153-884">開いているハンドルがある DrvFs ファイルを削除するとファイルで未定義の動作が示される問題を修正しました [GH 544、966、1357、1535、1615]</span><span class="sxs-lookup"><span data-stu-id="b2153-884">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="b2153-885">/etc/hosts は、Windows hosts ファイルからエントリを継承するようになりました (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="b2153-885">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="b2153-886">ビルド 16179</span><span class="sxs-lookup"><span data-stu-id="b2153-886">Build 16179</span></span>

<span data-ttu-id="b2153-887">ビルド 16179 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-887">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-888">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-888">Fixed</span></span>
- <span data-ttu-id="b2153-889">今週は、WSL の変更はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-889">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="b2153-890">ビルド 16176</span><span class="sxs-lookup"><span data-stu-id="b2153-890">Build 16176</span></span>

<span data-ttu-id="b2153-891">ビルド 16176 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-891">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-892">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-892">Fixed</span></span>

- [<span data-ttu-id="b2153-893">シリアル サポートを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b2153-893">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="b2153-894">IP ソケット オプション IP_OPTIONS を追加しました [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="b2153-894">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="b2153-895">(nginx/PHP-FPM にファイルをアップロード中に) pwritev 関数を実装しました [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="b2153-895">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="b2153-896">IP ソケット オプション IP_MULTICAST_IF および IPV6_MULTICAST_IF を追加しました [GH 990]</span><span class="sxs-lookup"><span data-stu-id="b2153-896">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="b2153-897">ソケット オプション IP_MULTICAST_LOOP および IPV6_MULTICAST_LOOP に対するサポート [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="b2153-897">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="b2153-898">apps node、traceroute、dig、nslookup、host に対する IP(V6)_MTU ソケット オプションを追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-898">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="b2153-899">IP ソケット オプション IPV6_UNICAST_HOPS を追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-899">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="b2153-900">ファイルシステムの機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-900">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="b2153-901">UNC パスのマウントを許可します</span><span class="sxs-lookup"><span data-stu-id="b2153-901">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="b2153-902">drvfs で CDFS のサポートを有効にします</span><span class="sxs-lookup"><span data-stu-id="b2153-902">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="b2153-903">drvfs でネットワーク ファイル システムのアクセス許可を正しく処理します</span><span class="sxs-lookup"><span data-stu-id="b2153-903">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="b2153-904">drvfs へのリモート ドライブのサポートを追加します</span><span class="sxs-lookup"><span data-stu-id="b2153-904">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="b2153-905">drvfs で FAT のサポートを有効にします</span><span class="sxs-lookup"><span data-stu-id="b2153-905">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="b2153-906">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-906">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-907">LTP の結果</span><span class="sxs-lookup"><span data-stu-id="b2153-907">LTP Results</span></span>
<span data-ttu-id="b2153-908">15042 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="b2153-908">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="b2153-909">ビルド 16170</span><span class="sxs-lookup"><span data-stu-id="b2153-909">Build 16170</span></span>

<span data-ttu-id="b2153-910">ビルド 16170 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-910">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="b2153-911">WSL のテストに関する取り組みを説明する新しい[ブログ投稿](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)をリリースしました。</span><span class="sxs-lookup"><span data-stu-id="b2153-911">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="b2153-912">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-912">Fixed</span></span>

- <span data-ttu-id="b2153-913">ソケット オプション IP_ADD_MEMBERSHIP および IPV6_ADD_MEMBERSHIP をサポートします [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="b2153-913">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="b2153-914">PTRACE_OLDSETOPTIONS のサポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-914">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="b2153-915">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="b2153-915">[GH 1692]</span></span>
- <span data-ttu-id="b2153-916">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-916">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-917">LTP の結果</span><span class="sxs-lookup"><span data-stu-id="b2153-917">LTP Results</span></span>
<span data-ttu-id="b2153-918">15042 以降変更はありません</span><span class="sxs-lookup"><span data-stu-id="b2153-918">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="b2153-919">ビルド 15046 から Windows 10 Creators Update まで</span><span class="sxs-lookup"><span data-stu-id="b2153-919">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="b2153-920">Windows 10 の Creators Update への組み込みが予定されている WSL の修正または機能はこれ以上ありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-920">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="b2153-921">WSL のリリース ノートは、次回の主要な Windows Update をターゲットとする追加に向けて、今後数週間のうちに再開されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-921">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="b2153-922">ビルド 15046 の一般的な Windows 情報および今後の Insider リリースについては、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-922">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="b2153-923">ビルド 15042</span><span class="sxs-lookup"><span data-stu-id="b2153-923">Build 15042</span></span>

<span data-ttu-id="b2153-924">ビルド 15042 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-924">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-925">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-925">Fixed</span></span>

- <span data-ttu-id="b2153-926">".." で終わるパスを削除する際のデッドロックの修正</span><span class="sxs-lookup"><span data-stu-id="b2153-926">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="b2153-927">FIONBIO が成功時に 0 を返さないという問題を修正しました [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="b2153-927">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="b2153-928">inet データグラム ソケットの長さゼロの読み取りの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-928">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="b2153-929">drvfs inode 参照での競合状態が原因で発生する可能性があるデッドロックを修正します [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="b2153-929">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="b2153-930">UNIX ソケット補助データに対する拡張サポート、SCM_CREDENTIALS および SCM_RIGHTS [GH 514、613、1326]</span><span class="sxs-lookup"><span data-stu-id="b2153-930">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="b2153-931">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-931">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-932">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-932">LTP Results:</span></span>
<span data-ttu-id="b2153-933">合格したテストの数:737</span><span class="sxs-lookup"><span data-stu-id="b2153-933">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b2153-934">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="b2153-934">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="b2153-935">ビルド 15031</span><span class="sxs-lookup"><span data-stu-id="b2153-935">Build 15031</span></span>

<span data-ttu-id="b2153-936">ビルド 15031 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-936">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-937">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-937">Fixed</span></span>

- <span data-ttu-id="b2153-938">time(2) が散発的に不適切な動作をするバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-938">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="b2153-939">\*SIGPROCMASK システム コールによってシグナル マスクが破損する問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-939">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="b2153-940">WSL プロセス作成通知で完全な長さのコマンド ラインが返されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-940">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="b2153-941">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="b2153-941">[GH 1632]</span></span>
- <span data-ttu-id="b2153-942">WSL は、GDB のハングについて ptrace を介してスレッドの終了を報告するようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-942">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="b2153-943">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="b2153-943">[GH 1196]</span></span>
- <span data-ttu-id="b2153-944">tmux の IO が大量に行われた後に ptys がハングするバグを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-944">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="b2153-945">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="b2153-945">[GH 1358]</span></span>
- <span data-ttu-id="b2153-946">複数のシステム コール (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create) でタイムアウトの検証を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-946">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="b2153-947">eventfd EFD_SEMAPHORE のサポートを追加しました [GH 452]</span><span class="sxs-lookup"><span data-stu-id="b2153-947">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="b2153-948">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-948">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-949">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-949">LTP Results:</span></span>
<span data-ttu-id="b2153-950">合格したテストの数:737</span><span class="sxs-lookup"><span data-stu-id="b2153-950">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b2153-951">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="b2153-951">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b2153-952">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-952">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="b2153-953">ビルド 15025</span><span class="sxs-lookup"><span data-stu-id="b2153-953">Build 15025</span></span>

<span data-ttu-id="b2153-954">ビルド 15025 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-954">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-955">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-955">Fixed</span></span>

- <span data-ttu-id="b2153-956">grep 2.27 を破損したバグの修正 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="b2153-956">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="b2153-957">eventfd2 システム コールに対して EFD_SEMAPHORE フラグを実装しました [GH 452]</span><span class="sxs-lookup"><span data-stu-id="b2153-957">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="b2153-958">/proc/[pid]/net/ipv6_route を実装しました [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="b2153-958">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="b2153-959">Unix ストリーム ソケットに対するシグナル駆動型 IO のサポート [GH 393、68]</span><span class="sxs-lookup"><span data-stu-id="b2153-959">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="b2153-960">F_GETPIPE_SZ および F_SETPIPE_SZ をサポートします [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="b2153-960">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="b2153-961">recvmmsg() システム コールを実装します [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="b2153-961">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="b2153-962">epoll_wait() が待機していなかったというバグを修正しました [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="b2153-962">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="b2153-963">/proc/version_signature を実装</span><span class="sxs-lookup"><span data-stu-id="b2153-963">Implement /proc/version_signature</span></span>
- <span data-ttu-id="b2153-964">Tee システム コールは、両方のファイル記述子が同じパイプを参照している場合にエラーを返すようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-964">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="b2153-965">UNIX ソケットに対する SO_PEERCRED の正しい動作を実装しました</span><span class="sxs-lookup"><span data-stu-id="b2153-965">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="b2153-966">tkill システム コールの無効なパラメーター処理を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-966">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="b2153-967">drvfs のパフォーマンスを向上させるための変更</span><span class="sxs-lookup"><span data-stu-id="b2153-967">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="b2153-968">Ruby の IO ブロックに対する軽微な修正</span><span class="sxs-lookup"><span data-stu-id="b2153-968">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="b2153-969">inet ソケットの MSG_DONTWAIT フラグに対して recvmsg() が EINVAL を返すという問題を修正しました [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="b2153-969">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="b2153-970">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-970">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-971">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-971">LTP Results:</span></span>
<span data-ttu-id="b2153-972">合格したテストの数:732</span><span class="sxs-lookup"><span data-stu-id="b2153-972">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="b2153-973">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="b2153-973">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b2153-974">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-974">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="b2153-975">ビルド 15019</span><span class="sxs-lookup"><span data-stu-id="b2153-975">Build 15019</span></span>

<span data-ttu-id="b2153-976">ビルド 15019 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-976">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-977">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-977">Fixed</span></span>

- <span data-ttu-id="b2153-978">htop などのツールに対して procfs で CPU 使用量が誤って報告されるバグを修正しました (GH 823、945、971)</span><span class="sxs-lookup"><span data-stu-id="b2153-978">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="b2153-979">既存のファイルに対して O_TRUNC を使用して open () を呼び出すと、inotify は IN_OPEN の前に IN_MODIFY を生成するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-979">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="b2153-980">Postgress を有効にするための UNIX ソケット getsockopt SO_ERROR に対する修正 [GH 61、1354]</span><span class="sxs-lookup"><span data-stu-id="b2153-980">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="b2153-981">GO 言語に対して /proc/sys/net/core/somaxconn を実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-981">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="b2153-982">Apt-get パッケージ更新のバックグラウンド タスクは、非表示で実行されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-982">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="b2153-983">ipv6 localhost のスコープをクリアします (Spring-Framework(Java) エラー)。</span><span class="sxs-lookup"><span data-stu-id="b2153-983">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="b2153-984">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-984">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-985">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-985">LTP Results:</span></span>
<span data-ttu-id="b2153-986">合格したテストの数:714</span><span class="sxs-lookup"><span data-stu-id="b2153-986">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="b2153-987">不合格の数 (失敗した、スキップしたなど):249</span><span class="sxs-lookup"><span data-stu-id="b2153-987">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="b2153-988">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-988">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="b2153-989">ビルド 15014</span><span class="sxs-lookup"><span data-stu-id="b2153-989">Build 15014</span></span>

<span data-ttu-id="b2153-990">ビルド 15014 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-990">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-991">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-991">Fixed</span></span>

- <span data-ttu-id="b2153-992">Ctrl+C は意図したとおりに動作するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-992">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="b2153-993">htop と ps auxw は正しいリソース使用量を表示するようになりました (GH #516)</span><span class="sxs-lookup"><span data-stu-id="b2153-993">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="b2153-994">NT 例外からシグナルへの基本的な変換。</span><span class="sxs-lookup"><span data-stu-id="b2153-994">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="b2153-995">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="b2153-995">(GH #513)</span></span>
- <span data-ttu-id="b2153-996">fallocate は、領域が不足しているときに、EINVAL ではなく ENOSPC で失敗するようになりました (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="b2153-996">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="b2153-997">/proc/sys/kernel/sem を追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-997">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="b2153-998">semop システム コールと semtimedop システム コールを実装しました</span><span class="sxs-lookup"><span data-stu-id="b2153-998">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="b2153-999">IP_RECVTOS および IPV6_RECVTCLASS ソケット オプションでの nslookup エラーを修正しました (GH 69)</span><span class="sxs-lookup"><span data-stu-id="b2153-999">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="b2153-1000">ソケット オプション IP_RECVTTL および IPV6_RECVHOPLIMIT に対するサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1000">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="b2153-1001">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1001">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1002">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1002">LTP Results:</span></span>
<span data-ttu-id="b2153-1003">合格したテストの数:709</span><span class="sxs-lookup"><span data-stu-id="b2153-1003">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b2153-1004">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="b2153-1004">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b2153-1005">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1005">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="b2153-1006">システム コールの概要</span><span class="sxs-lookup"><span data-stu-id="b2153-1006">Syscall Summary</span></span>
<span data-ttu-id="b2153-1007">システム コールの合計:384</span><span class="sxs-lookup"><span data-stu-id="b2153-1007">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="b2153-1008">実装の合計:235</span><span class="sxs-lookup"><span data-stu-id="b2153-1008">Total Implemented: 235</span></span> </br>
<span data-ttu-id="b2153-1009">スタブの合計:22</span><span class="sxs-lookup"><span data-stu-id="b2153-1009">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="b2153-1010">未実装の合計:127</span><span class="sxs-lookup"><span data-stu-id="b2153-1010">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="b2153-1011">詳細な内訳</span><span class="sxs-lookup"><span data-stu-id="b2153-1011">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="b2153-1012">ビルド 15007</span><span class="sxs-lookup"><span data-stu-id="b2153-1012">Build 15007</span></span>

<span data-ttu-id="b2153-1013">ビルド 15007 の一般的な Windows 情報については、[Windows ブログ]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1013">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b2153-1014">既知の問題</span><span class="sxs-lookup"><span data-stu-id="b2153-1014">Known Issue</span></span>

- <span data-ttu-id="b2153-1015">コンソールが一部の Ctrl + <key> 入力を認識しないという既知のバグがあります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1015">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b2153-1016">これには、通常の "c" キーが押されたものとして機能する ctrl-c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1016">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b2153-1017">対応策 :代替キーを Ctrl+C にマップします。</span><span class="sxs-lookup"><span data-stu-id="b2153-1017">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b2153-1018">たとえば、Ctrl+K を Ctrl+C にマップするには、`stty intr \^k` を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1018">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b2153-1019">このマッピングはターミナルごとに行い、*毎回* bash が起動されるたびに実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1019">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b2153-1020">ユーザーはオプションを探索し、これを `.bashrc` に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1020">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="b2153-1021">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1021">Fixed</span></span>

- <span data-ttu-id="b2153-1022">実行中の WSL が CPU コアの 100% を消費するという問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1022">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="b2153-1023">ソケット オプション IP_PKTINFO、IPV6_RECVPKTINFO がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1023">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="b2153-1024">(GH #851、987)</span><span class="sxs-lookup"><span data-stu-id="b2153-1024">(GH #851, 987)</span></span>
- <span data-ttu-id="b2153-1025">lxcore でネットワーク インターフェイスの物理アドレスが 16 バイトに切り捨てられます (GH #1452、1414、1343、468、308)</span><span class="sxs-lookup"><span data-stu-id="b2153-1025">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="b2153-1026">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1026">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1027">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1027">LTP Results:</span></span>
<span data-ttu-id="b2153-1028">合格したテストの数:709</span><span class="sxs-lookup"><span data-stu-id="b2153-1028">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b2153-1029">不合格の数 (失敗した、スキップしたなど):255</span><span class="sxs-lookup"><span data-stu-id="b2153-1029">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b2153-1030">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1030">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="b2153-1031">ビルド 15002</span><span class="sxs-lookup"><span data-stu-id="b2153-1031">Build 15002</span></span>

<span data-ttu-id="b2153-1032">ビルド 15002 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1032">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b2153-1033">既知の問題</span><span class="sxs-lookup"><span data-stu-id="b2153-1033">Known Issue</span></span>

<span data-ttu-id="b2153-1034">2 つの既知の問題:</span><span class="sxs-lookup"><span data-stu-id="b2153-1034">Two known issues:</span></span>
- <span data-ttu-id="b2153-1035">コンソールが一部の Ctrl + <key> 入力を認識しないという既知のバグがあります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1035">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b2153-1036">これには、通常の "c" キーが押されたものとして機能する ctrl-c コマンドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1036">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b2153-1037">対応策 :代替キーを Ctrl+C にマップします。</span><span class="sxs-lookup"><span data-stu-id="b2153-1037">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b2153-1038">たとえば、Ctrl+K を Ctrl+C にマップするには、`stty intr \^k` を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1038">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b2153-1039">このマッピングはターミナルごとに行い、*毎回* bash が起動されるたびに実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1039">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b2153-1040">ユーザーはオプションを探索し、これを `.bashrc` に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1040">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="b2153-1041">WSL が実行されている間、システム スレッドは CPU コアの 100% を消費します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1041">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="b2153-1042">根本原因は、内部で対処されて修正されています。</span><span class="sxs-lookup"><span data-stu-id="b2153-1042">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="b2153-1043">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1043">Fixed</span></span>

- <span data-ttu-id="b2153-1044">すべての bash セッションは、同じアクセス許可レベルで作成することが必要になりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1044">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="b2153-1045">別のレベルでセッションを開始しようとすると、ブロックされます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1045">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="b2153-1046">つまり、管理コンソールと非管理コンソールを同時に実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1046">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="b2153-1047">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="b2153-1047">(GH #626)</span></span>
<br/>
- <span data-ttu-id="b2153-1048">次の NETLINK_ROUTE メッセージを実装しました (Windows 管理者が必要)</span><span class="sxs-lookup"><span data-stu-id="b2153-1048">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="b2153-1049">RTM_NEWADDR (`ip addr add` をサポート)</span><span class="sxs-lookup"><span data-stu-id="b2153-1049">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="b2153-1050">RTM_NEWROUTE (`ip route add` をサポート)</span><span class="sxs-lookup"><span data-stu-id="b2153-1050">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="b2153-1051">RTM_DELADDR (`ip addr del` をサポート)</span><span class="sxs-lookup"><span data-stu-id="b2153-1051">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="b2153-1052">RTM_DELROUTE (`ip route del` をサポート)</span><span class="sxs-lookup"><span data-stu-id="b2153-1052">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="b2153-1053">更新するパッケージについてのスケジュールされたタスク チェックは、従量課金接続では実行されなくなります (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="b2153-1053">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="b2153-1054">次のようにパイプがスタックするエラーを修正しました。bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="b2153-1054">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b2153-1055">TCP_KEEPCNT ソケット オプションを実装しました (GH #843)</span><span class="sxs-lookup"><span data-stu-id="b2153-1055">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="b2153-1056">IP_MTU_DISCOVER INET ソケット オプションを実装しました (GH #720、717、170、69)</span><span class="sxs-lookup"><span data-stu-id="b2153-1056">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="b2153-1057">NT パス参照を使用して init から NT バイナリを実行する従来の機能を削除しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1057">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="b2153-1058">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="b2153-1058">(GH #1325)</span></span>
- <span data-ttu-id="b2153-1059">グループ/その他の読み取りアクセスを許可するように /dev/kmsg のモードを修正します (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="b2153-1059">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="b2153-1060">/proc/sys/kernel/random/uuid を実装しました (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="b2153-1060">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="b2153-1061">プロセスの開始時刻が 2432 年と表示されていたエラーを修正しました (GH #974)</span><span class="sxs-lookup"><span data-stu-id="b2153-1061">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="b2153-1062">既定の TERM 環境変数を xterm-256color に切り替えました (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="b2153-1062">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="b2153-1063">プロセスのフォーク中のプロセス コミットの計算方法を変更しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1063">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="b2153-1064">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="b2153-1064">(GH #1286)</span></span>
- <span data-ttu-id="b2153-1065">/proc/sys/vm/overcommit_memory を実装しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1065">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="b2153-1066">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="b2153-1066">(GH #1286)</span></span>
- <span data-ttu-id="b2153-1067">/proc/net/route ファイルを実装しました (GH #69)</span><span class="sxs-lookup"><span data-stu-id="b2153-1067">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="b2153-1068">ショートカット名が誤ってローカライズされるエラーを修正しました (GH #696)</span><span class="sxs-lookup"><span data-stu-id="b2153-1068">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="b2153-1069">プログラム ヘッダーが PATH_MAX 以下でなければならないことを誤って検証をしている elf 解析ロジックを修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1069">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="b2153-1070">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="b2153-1070">(GH #1048)</span></span>
- <span data-ttu-id="b2153-1071">procfs、sysfs、cgroupfs、および binfmtfs に対する statfs コールバックを実装しました (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="b2153-1071">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="b2153-1072">閉じない AptPackageIndexUpdate ウィンドウを修正しました (GH #1184、さらに GH #1193 でも説明)</span><span class="sxs-lookup"><span data-stu-id="b2153-1072">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="b2153-1073">ASLR パーソナリティ ADDR_NO_RANDOMIZE のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1073">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="b2153-1074">(GH #1148、1128)</span><span class="sxs-lookup"><span data-stu-id="b2153-1074">(GH #1148, 1128)</span></span>
- <span data-ttu-id="b2153-1075">AV 中の適切な gdb スタック トレースのために PTRACE_GETSIGINFO、SIGSEGV を改善しました (GH #875)</span><span class="sxs-lookup"><span data-stu-id="b2153-1075">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="b2153-1076">patchelf バイナリに対する Elf の解析は失敗しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1076">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="b2153-1077">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="b2153-1077">(GH #471)</span></span>
- <span data-ttu-id="b2153-1078">/etc/resolv.conf に伝搬される VPN DNS (GH #416、1350)</span><span class="sxs-lookup"><span data-stu-id="b2153-1078">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="b2153-1079">より信頼性の高いデータ転送のための TCP クローズに対する機能強化。</span><span class="sxs-lookup"><span data-stu-id="b2153-1079">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="b2153-1080">(GH #610、616、1025、1335)</span><span class="sxs-lookup"><span data-stu-id="b2153-1080">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="b2153-1081">開いているファイルの数が多すぎるときに適切なエラー コードが返されるようになりました (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="b2153-1081">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="b2153-1082">(GH #1126、2090)</span><span class="sxs-lookup"><span data-stu-id="b2153-1082">(GH #1126, 2090)</span></span>
- <span data-ttu-id="b2153-1083">Windows の監査ログは、プロセス作成の監査でイメージ名を報告するようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1083">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="b2153-1084">bash ウィンドウ内から bash.exe を起動すると、正常に失敗するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1084">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="b2153-1085">相互運用が LxFs の作業ディレクトリにアクセスできないときのエラー メッセージを追加しました (例: notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="b2153-1085">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="b2153-1086">Windows のパスが WSL で切り捨てられていた問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1086">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="b2153-1087">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1087">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1088">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1088">LTP Results:</span></span>
<span data-ttu-id="b2153-1089">合格したテストの数:690</span><span class="sxs-lookup"><span data-stu-id="b2153-1089">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="b2153-1090">不合格の数 (失敗した、スキップしたなど):274</span><span class="sxs-lookup"><span data-stu-id="b2153-1090">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="b2153-1091">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1091">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1092">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1092">Syscall Support</span></span>
<span data-ttu-id="b2153-1093">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1093">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1094">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1094">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="b2153-1095">ビルド 14986</span><span class="sxs-lookup"><span data-stu-id="b2153-1095">Build 14986</span></span>

<span data-ttu-id="b2153-1096">ビルド 14986 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1096">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1097">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1097">Fixed</span></span>

- <span data-ttu-id="b2153-1098">Netlink および Pty の IOCTL でのバグチェックを修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1098">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="b2153-1099">カーネルのバージョンは、Xenial との一貫性のために 4.4.0-43 を報告するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1099">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="b2153-1100">入力が 'nul:' に向けられたときに Bash.exe が起動するようになりました (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="b2153-1100">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="b2153-1101">スレッド ID が procfs で正しく報告されるようになりました (GH #967)</span><span class="sxs-lookup"><span data-stu-id="b2153-1101">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="b2153-1102">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR のフラグが inotify_add_watch() でサポートされるようになりました (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="b2153-1102">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="b2153-1103">timer_create システム コールおよび関連するシステム コールを実装します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1103">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="b2153-1104">これにより GHC サポートが有効になります (GH #307)</span><span class="sxs-lookup"><span data-stu-id="b2153-1104">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="b2153-1105">Ping で 0.000 ミリ秒の時間が返される問題を修正しました (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="b2153-1105">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="b2153-1106">開いているファイルの数が多すぎるときに適切なエラー コードを返します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1106">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="b2153-1107">インターフェイスのハードウェア アドレスが 32 バイトの場合 (Teredo インターフェイスなど) に、Netlink のネットワーク インターフェイス データの要求が EINVAL で失敗する WSL の問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1107">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="b2153-1108">Linux の "ip" ユーティリティには、WSL が 32 バイトのハードウェア アドレスを報告した場合にクラッシュするバグが含まれていることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1108">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="b2153-1109">これは、WSL ではなく、"ip" のバグです。</span><span class="sxs-lookup"><span data-stu-id="b2153-1109">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="b2153-1110">"Ip" ユーティリティは、ハードウェア アドレスの出力に使用される文字列バッファーの長さをハードコーディングしますが、そのバッファーは 32 バイトのハードウェア アドレスを出力するには小さすぎます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1110">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="b2153-1111">その他の修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1111">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1112">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1112">LTP Results:</span></span>
<span data-ttu-id="b2153-1113">合格したテストの数:669</span><span class="sxs-lookup"><span data-stu-id="b2153-1113">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="b2153-1114">不合格の数 (失敗した、スキップしたなど):258</span><span class="sxs-lookup"><span data-stu-id="b2153-1114">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b2153-1115">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1116">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1116">Syscall Support</span></span>
<span data-ttu-id="b2153-1117">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1117">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1118">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1118">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="b2153-1119">ビルド 14971</span><span class="sxs-lookup"><span data-stu-id="b2153-1119">Build 14971</span></span>

<span data-ttu-id="b2153-1120">ビルド 14971 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1120">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1121">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1121">Fixed</span></span>

 - <span data-ttu-id="b2153-1122">Microsoft の制御を超える状況により、Windows Subsystem for Linux のこのビルドには更新はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1122">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b2153-1123">定期的にスケジュールされた更新は、次のリリースから再開されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1123">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1124">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1124">LTP Results:</span></span>
<span data-ttu-id="b2153-1125">14965 から変更されていません</span><span class="sxs-lookup"><span data-stu-id="b2153-1125">Unchanged from 14965</span></span> </br>
<span data-ttu-id="b2153-1126">合格したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="b2153-1126">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b2153-1127">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="b2153-1127">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b2153-1128">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1128">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="b2153-1129">ビルド 14965</span><span class="sxs-lookup"><span data-stu-id="b2153-1129">Build 14965</span></span>

<span data-ttu-id="b2153-1130">ビルド 14965 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1130">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1131">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1131">Fixed</span></span>

- <span data-ttu-id="b2153-1132">Netlink ソケット NETLINK_ROUTE プロトコルの RTM_GETLINK と RTM_GETADDR に対するサポート (GH #468)</span><span class="sxs-lookup"><span data-stu-id="b2153-1132">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="b2153-1133">ネットワークの列挙に対して ifconfig コマンドと ip コマンドを有効にします</span><span class="sxs-lookup"><span data-stu-id="b2153-1133">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="b2153-1134">詳細については、[WSL ネットワークに関するブログ投稿](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1134">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="b2153-1135">/sbin は、既定でユーザーのパスに含まれるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1135">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="b2153-1136">NT ユーザー パスが既定で WSL パスに追加されるようになりました (つまり、Linux パスに System32 を追加せずに notepad.exe を入力できるようになりました)</span><span class="sxs-lookup"><span data-stu-id="b2153-1136">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="b2153-1137">/proc/sys/kernel/cap_last_cap のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1137">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="b2153-1138">現在の作業ディレクトリに ANSI 以外の文字が含まれている場合、WSL から NT バイナリを起動できるようになりました (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="b2153-1138">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="b2153-1139">切断された UNIX ストリーム ソケットでのシャットダウンを許可します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1139">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="b2153-1140">PR_GET_PDEATHSIG のサポートを追加しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1140">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="b2153-1141">CLONE_PARENT のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1141">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="b2153-1142">次のようにパイプがスタックするエラーを修正しました。bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="b2153-1142">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b2153-1143">現在のターミナルに接続する要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1143">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="b2153-1144">/proc/<pid>/oom_score_adj を書き込み可能としてマークします。</span><span class="sxs-lookup"><span data-stu-id="b2153-1144">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="b2153-1145">/sys/fs/cgroup フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1145">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="b2153-1146">sched_setaffinity は、アフィニティ ビット マスクの数を返します</span><span class="sxs-lookup"><span data-stu-id="b2153-1146">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="b2153-1147">インタープリター パスの長さが 64 文字未満でなければならないことを誤って想定している ELF 検証ロジックを修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1147">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="b2153-1148">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="b2153-1148">(GH #743)</span></span>
- <span data-ttu-id="b2153-1149">オープン ファイル記述子により、コンソール ウィンドウが開いたままになることがあります (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="b2153-1149">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="b2153-1150">rename() がターゲット名の末尾スラッシュで失敗したエラーを修正しました (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="b2153-1150">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="b2153-1151">/proc/net/dev ファイルを実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-1151">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="b2153-1152">タイマー精度が原因の 0.000 ミリ秒の Ping を修正します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1152">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="b2153-1153">/proc/self/environ を実装しました (GH #730)</span><span class="sxs-lookup"><span data-stu-id="b2153-1153">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="b2153-1154">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1154">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1155">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1155">LTP Results:</span></span>
<span data-ttu-id="b2153-1156">合格したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="b2153-1156">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b2153-1157">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="b2153-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b2153-1158">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="b2153-1159">ビルド 14959</span><span class="sxs-lookup"><span data-stu-id="b2153-1159">Build 14959</span></span>

<span data-ttu-id="b2153-1160">ビルド 14959 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1160">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1161">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1161">Fixed</span></span>

- <span data-ttu-id="b2153-1162">Windows の Pico プロセス通知を改善しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1162">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="b2153-1163">[WSL ブログ](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)に追加情報があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1163">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="b2153-1164">Windows の相互運用性での安定性を向上させました</span><span class="sxs-lookup"><span data-stu-id="b2153-1164">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="b2153-1165">エンタープライズ データ保護 (EDP) が有効になっているときに bash.exe を起動すると発生するエラー 0x80070057 を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1165">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="b2153-1166">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1166">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1167">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1167">LTP Results:</span></span>
<span data-ttu-id="b2153-1168">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="b2153-1168">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b2153-1169">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="b2153-1169">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b2153-1170">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1170">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="b2153-1171">ビルド 14955</span><span class="sxs-lookup"><span data-stu-id="b2153-1171">Build 14955</span></span>

<span data-ttu-id="b2153-1172">ビルド 14955 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1172">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1173">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1173">Fixed</span></span>

 - <span data-ttu-id="b2153-1174">Microsoft の制御を超える状況により、Windows Subsystem for Linux のこのビルドには更新はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1174">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b2153-1175">定期的にスケジュールされた更新は、次のリリースから再開されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1175">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1176">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1176">LTP Results:</span></span>
<span data-ttu-id="b2153-1177">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="b2153-1177">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b2153-1178">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="b2153-1178">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b2153-1179">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1179">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="b2153-1180">ビルド 14951</span><span class="sxs-lookup"><span data-stu-id="b2153-1180">Build 14951</span></span>

<span data-ttu-id="b2153-1181">ビルド 14951 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1181">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="b2153-1182">新機能:Windows/Ubuntu の相互運用性</span><span class="sxs-lookup"><span data-stu-id="b2153-1182">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="b2153-1183">Windows バイナリを WSL コマンド ラインから直接呼び出せるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1183">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="b2153-1184">これによりユーザーは、今まで可能ではなかった方法で Windows 環境およびシステムと対話ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1184">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="b2153-1185">簡単な例として、ユーザーは次のコマンドを実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1185">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="b2153-1186">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1186">More information can be found at:</span></span>

- [<span data-ttu-id="b2153-1187">相互運用に関する WSL チームのブログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1187">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="b2153-1188">MSDN 相互運用のドキュメント</span><span class="sxs-lookup"><span data-stu-id="b2153-1188">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="b2153-1189">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1189">Fixed</span></span>

- <span data-ttu-id="b2153-1190">すべての新しい WSL インスタンスで Ubuntu 16.04 (Xenial) がインストールされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1190">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="b2153-1191">既存の 14.04 (Trusty) インスタンスを使用しているユーザーは自動的にアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1191">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="b2153-1192">インストール中に設定されたロケールが表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1192">Locale set during install is now displayed</span></span>
- <span data-ttu-id="b2153-1193">ファイルへの WSL プロセスのリダイレクトが必ずしも機能しないというバグを含む、ターミナルの機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1193">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="b2153-1194">コンソールの有効期間は bash.exe の有効期間に関連付けられている必要があります</span><span class="sxs-lookup"><span data-stu-id="b2153-1194">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="b2153-1195">コンソール ウィンドウのサイズは、バッファー サイズではなく表示サイズを使用する必要があります</span><span class="sxs-lookup"><span data-stu-id="b2153-1195">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="b2153-1196">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1196">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1197">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1197">LTP Results:</span></span>
<span data-ttu-id="b2153-1198">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="b2153-1198">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b2153-1199">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="b2153-1199">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b2153-1200">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1200">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="b2153-1201">ビルド 14946</span><span class="sxs-lookup"><span data-stu-id="b2153-1201">Build 14946</span></span>

<span data-ttu-id="b2153-1202">ビルド 14946 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1202">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1203">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1203">Fixed</span></span>

- <span data-ttu-id="b2153-1204">スペースまたは引用符を含む NT ユーザー名を持つユーザーの WSL ユーザー アカウントの作成を妨げる問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1204">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="b2153-1205">stat でディレクトリのリンク数に対して 0 が返されるように、VolFs と DrvFs を変更します</span><span class="sxs-lookup"><span data-stu-id="b2153-1205">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="b2153-1206">IPV6_MULTICAST_HOPS ソケット オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b2153-1206">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="b2153-1207">1 つの tty につき 1 つのコンソール I/O ループに制限します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1207">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="b2153-1208">たとえば、次のコマンドが可能です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1208">Example: the following command is possible:</span></span>
  - <span data-ttu-id="b2153-1209">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="b2153-1209">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="b2153-1210">/proc/cpuinfo でスペースをタブに置き換えます (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="b2153-1210">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="b2153-1211">DrvFs は、マウントされた Windows ボリュームと一致する名前で mountinfo に表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1211">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="b2153-1212">/home と /root が正しい名前で mountinfo に表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1212">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="b2153-1213">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1213">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1214">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1214">LTP Results:</span></span>
<span data-ttu-id="b2153-1215">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="b2153-1215">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b2153-1216">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="b2153-1216">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b2153-1217">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1217">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="b2153-1218">ビルド 14942</span><span class="sxs-lookup"><span data-stu-id="b2153-1218">Build 14942</span></span>

<span data-ttu-id="b2153-1219">ビルド 14942 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/onefourninefourtwoooooo)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1219">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1220">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1220">Fixed</span></span>

- <span data-ttu-id="b2153-1221">SSH をブロックしていた “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” ネットワーク クラッシュを含め、複数のバグチェックに対処しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1221">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="b2153-1222">DrvFs の Windows アプリケーションから生成された通知に対する inotifiy のサポートが有効になりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1222">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="b2153-1223">mongod に対して TCP_KEEPIDLE および TCP_KEEPINTVL を実装します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1223">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="b2153-1224">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="b2153-1224">(GH #695)</span></span>
- <span data-ttu-id="b2153-1225">pivot_root システム コールを実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-1225">Implement the pivot_root system call</span></span>
- <span data-ttu-id="b2153-1226">SO_DONTROUTE に対してソケット オプションを実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-1226">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="b2153-1227">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1227">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="b2153-1228">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1228">LTP Results:</span></span>
<span data-ttu-id="b2153-1229">合格したテストの数:665</span><span class="sxs-lookup"><span data-stu-id="b2153-1229">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b2153-1230">不合格の数 (失敗した、スキップしたなど):263</span><span class="sxs-lookup"><span data-stu-id="b2153-1230">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b2153-1231">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1231">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1232">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1232">Syscall Support</span></span>
<span data-ttu-id="b2153-1233">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1233">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1234">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1234">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="b2153-1235">ビルド 14936</span><span class="sxs-lookup"><span data-stu-id="b2153-1235">Build 14936</span></span>

<span data-ttu-id="b2153-1236">ビルド 14936 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1236">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="b2153-1237">注:WSL は、今後のリリースで Ubuntu 14.04 (Trusty) ではなく、Ubuntu バージョン 16.04 (Xenial) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="b2153-1237">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="b2153-1238">この変更は、新しいインスタンスをインストールする Insiders に適用されます (lxrun.exe、あるいは bash.exe のインストールまたは初回の実行)。</span><span class="sxs-lookup"><span data-stu-id="b2153-1238">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="b2153-1239">Trusty を使用する既存のインスタンスは、自動的にアップグレードされません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1239">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="b2153-1240">ユーザーは、do-release-upgrade コマンドを使用して、Trusty イメージを Xenial にアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1240">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="b2153-1241">既知の問題</span><span class="sxs-lookup"><span data-stu-id="b2153-1241">Known Issue</span></span>
<span data-ttu-id="b2153-1242">WSL では、いくつかのソケット実装で問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="b2153-1242">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="b2153-1243">バグチェックを実行するとクラッシュし、エラー “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” が出されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1243">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="b2153-1244">この問題の最も一般的な発現は、SSH を使用したときのクラッシュです。</span><span class="sxs-lookup"><span data-stu-id="b2153-1244">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="b2153-1245">根本原因は内部ビルドで修正され、最も早い機会に Insiders にプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1245">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="b2153-1246">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1246">Fixed</span></span>

- <span data-ttu-id="b2153-1247">chroot システム コールを実装しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1247">Implemented the chroot system call</span></span>
- <span data-ttu-id="b2153-1248">~~Drvfs 上の Windows アプリケーションから生成された通知のサポートを含む~~ inotify の機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1248">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="b2153-1249">訂正:Windows アプリケーションからの変更に対する Inotify のサポートは、現時点では利用できません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1249">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="b2153-1250">IPV6::<port n> へのソケット バインドで、IPV6_V6ONLY がサポートされるようになりました (GH #68、#157、#393、#460、#674、#740、#982、#996)</span><span class="sxs-lookup"><span data-stu-id="b2153-1250">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="b2153-1251">waitid システム コールに対する WNOWAIT 動作を実装しました (GH #638)</span><span class="sxs-lookup"><span data-stu-id="b2153-1251">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="b2153-1252">IP ソケット オプション IP_HDRINCL と IP_TTL のサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1252">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="b2153-1253">長さゼロの read() はすぐに戻ります (GH #975)</span><span class="sxs-lookup"><span data-stu-id="b2153-1253">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="b2153-1254">.tar ファイルに NULL 終端文字を含まないファイル名とファイル名のプレフィックスを正しく処理します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1254">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="b2153-1255">/dev/null に対する epoll サポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1255">epoll support for /dev/null</span></span>
- <span data-ttu-id="b2153-1256">/dev/alarm タイム ソースを修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-1256">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="b2153-1257">Bash -c はファイルにリダイレクトできるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1257">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="b2153-1258">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1258">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1259">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1259">LTP Results:</span></span>
<span data-ttu-id="b2153-1260">合格したテストの数:664</span><span class="sxs-lookup"><span data-stu-id="b2153-1260">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b2153-1261">不合格の数 (失敗した、スキップしたなど):264</span><span class="sxs-lookup"><span data-stu-id="b2153-1261">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="b2153-1262">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1262">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1263">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1263">Syscall Support</span></span>
<span data-ttu-id="b2153-1264">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1264">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1265">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1265">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="b2153-1266">ビルド 14931</span><span class="sxs-lookup"><span data-stu-id="b2153-1266">Build 14931</span></span>

<span data-ttu-id="b2153-1267">ビルド 14931 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1267">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1268">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1268">Fixed</span></span>

 - <span data-ttu-id="b2153-1269">Microsoft の制御を超える状況により、Windows Subsystem for Linux のこのビルドには更新はありません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1269">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b2153-1270">定期的にスケジュールされた更新は、次のリリースから再開されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1270">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="b2153-1271">ビルド 14926</span><span class="sxs-lookup"><span data-stu-id="b2153-1271">Build 14926</span></span>

<span data-ttu-id="b2153-1272">ビルド 14926 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1272">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1273">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1273">Fixed</span></span>

- <span data-ttu-id="b2153-1274">管理者特権を持たないコンソールで Ping が機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1274">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="b2153-1275">Ping6 が、この場合も管理者特権なしでサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1275">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="b2153-1276">WSL を使用して変更されたファイルに対する Inotify サポート。</span><span class="sxs-lookup"><span data-stu-id="b2153-1276">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="b2153-1277">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="b2153-1277">(GH #216)</span></span>
  - <span data-ttu-id="b2153-1278">サポートされるフラグ:</span><span class="sxs-lookup"><span data-stu-id="b2153-1278">Flags supported:</span></span>
    - <span data-ttu-id="b2153-1279">inotify_init1:LX_O_CLOEXEC、LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="b2153-1279">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="b2153-1280">inotify_add_watch イベント:LX_IN_ACCESS、LX_IN_MODIFY、LX_IN_ATTRIB、LX_IN_CLOSE_WRITE、LX_IN_CLOSE_NOWRITE、LX_IN_OPEN、LX_IN_MOVED_FROM、LX_IN_MOVED_TO、LX_IN_CREATE、LX_IN_DELETE、LX_IN_DELETE_SELF、LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="b2153-1280">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="b2153-1281">inotify_add_watch 属性:LX_IN_DONT_FOLLOW、LX_IN_EXCL_UNLINK、LX_IN_MASK_ADD、LX_IN_ONESHOT、LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="b2153-1281">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="b2153-1282">出力の読み取り:LX_IN_ISDIR、LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="b2153-1282">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="b2153-1283">既知の問題:Windows アプリケーションからファイルを変更してもイベントは生成されません</span><span class="sxs-lookup"><span data-stu-id="b2153-1283">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="b2153-1284">Unix ソケットで SCM_CREDENTIALS がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1284">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b2153-1285">LTP の結果:</span><span class="sxs-lookup"><span data-stu-id="b2153-1285">LTP Results:</span></span>
<span data-ttu-id="b2153-1286">合格したテストの数:651</span><span class="sxs-lookup"><span data-stu-id="b2153-1286">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="b2153-1287">不合格の数 (失敗した、スキップしたなど):258</span><span class="sxs-lookup"><span data-stu-id="b2153-1287">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b2153-1288">LTP テスト実行ログ</span><span class="sxs-lookup"><span data-stu-id="b2153-1288">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="b2153-1289">ビルド 14915</span><span class="sxs-lookup"><span data-stu-id="b2153-1289">Build 14915</span></span>

<span data-ttu-id="b2153-1290">ビルド 14915 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1290">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1291">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1291">Fixed</span></span>
-  <span data-ttu-id="b2153-1292">UNIX データグラム ソケットに対する Socketpair (GH #262)</span><span class="sxs-lookup"><span data-stu-id="b2153-1292">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="b2153-1293">SO_REUSEADDR に対する UNIX ソケット サポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1293">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="b2153-1294">SO_BROADCAST に対する UNIX ソケット サポート (GH #568)</span><span class="sxs-lookup"><span data-stu-id="b2153-1294">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="b2153-1295">SOCK_SEQPACKET に対する UNIX ソケット サポート (GH #758、#546)</span><span class="sxs-lookup"><span data-stu-id="b2153-1295">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="b2153-1296">UNIX データグラム ソケット send、recv、および shutdown に対するサポートの追加</span><span class="sxs-lookup"><span data-stu-id="b2153-1296">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="b2153-1297">固定されていないアドレスに対する無効な mmap パラメーター検証によるバグチェックの修正。</span><span class="sxs-lookup"><span data-stu-id="b2153-1297">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="b2153-1298">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="b2153-1298">(GH #847)</span></span>
- <span data-ttu-id="b2153-1299">ターミナルの状態の中断/再開のサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1299">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="b2153-1300">Screen ユーティリティのブロックを解除する TIOCPKT ioctl のサポート (GH #774)</span><span class="sxs-lookup"><span data-stu-id="b2153-1300">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="b2153-1301">既知の問題:ファンクション キーが動作しません</span><span class="sxs-lookup"><span data-stu-id="b2153-1301">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="b2153-1302">解放されたメンバー 'ReaderReady' が LxpTimerFdWorkerRoutine によってアクセスされる原因となる TimerFd での競合を修正しました (GH #814)</span><span class="sxs-lookup"><span data-stu-id="b2153-1302">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="b2153-1303">futex、poll、および clock_nanosleep に対する再起動可能システム コールのサポートを有効にします</span><span class="sxs-lookup"><span data-stu-id="b2153-1303">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="b2153-1304">bind mount のサポートを追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1304">Added bind mount support</span></span>
- <span data-ttu-id="b2153-1305">マウント名前空間に対する unshare のサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1305">unshare for mount namespace support</span></span>
    - <span data-ttu-id="b2153-1306">既知の問題:`unshare(CLONE_NEWNS)` を使用して新しいマウント名前空間を作成するときに、現在の作業ディレクトリは引き続き古い名前空間を指します</span><span class="sxs-lookup"><span data-stu-id="b2153-1306">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="b2153-1307">その他の機能強化とバグ修正</span><span class="sxs-lookup"><span data-stu-id="b2153-1307">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="b2153-1308">ビルド 14905</span><span class="sxs-lookup"><span data-stu-id="b2153-1308">Build 14905</span></span>

<span data-ttu-id="b2153-1309">ビルド 14905 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1309">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1310">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1310">Fixed</span></span>
- <span data-ttu-id="b2153-1311">再起動可能システム コールがサポートされるようになりました (GH #349、GH #520)</span><span class="sxs-lookup"><span data-stu-id="b2153-1311">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="b2153-1312">/ で終了するディレクトリへのシンボリック リンクが動作するようになりました (GH #650)</span><span class="sxs-lookup"><span data-stu-id="b2153-1312">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="b2153-1313">/dev/random に対する RNDGETENTCNT ioctl を実装しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1313">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="b2153-1314">/proc/[pid]/mounts、/proc/[pid]/mountinfo、および /proc/[pid]/mountstats のファイルを実装しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1314">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="b2153-1315">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1315">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="b2153-1316">ビルド 14901</span><span class="sxs-lookup"><span data-stu-id="b2153-1316">Build 14901</span></span>
<span data-ttu-id="b2153-1317">Windows 10 Anniversary Update リリース以降の最初の Insider ビルド。</span><span class="sxs-lookup"><span data-stu-id="b2153-1317">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="b2153-1318">ビルド 14901 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1318">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1319">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1319">Fixed</span></span>
- <span data-ttu-id="b2153-1320">末尾のスラッシュの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1320">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="b2153-1321">`$ mv a/c/ a/b/` などのコマンドが機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1321">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="b2153-1322">インストールで、Ubuntu のロケールを Windows のロケールに設定すべきかどうかを確認するプロンプトが出されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1322">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="b2153-1323">ns フォルダーに対する Procfs のサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1323">Procfs support for ns folder</span></span>
- <span data-ttu-id="b2153-1324">tmpfs、procfs、および sysfs のファイルシステムに対して mount と unmount を追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1324">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="b2153-1325">mknod[at] 32 ビット ABI の署名を修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-1325">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="b2153-1326">UNIX ソケットをディスパッチ モデルに移行しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1326">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="b2153-1327">setsockopt を使用して設定された INET ソケットの recv バッファー サイズを優先します</span><span class="sxs-lookup"><span data-stu-id="b2153-1327">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="b2153-1328">MSG_CMSG_CLOEXEC Unix ソケット受信メッセージ フラグを実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-1328">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="b2153-1329">Linux プロセスの stdin/stdout パイプのリダイレクト (GH #2)</span><span class="sxs-lookup"><span data-stu-id="b2153-1329">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="b2153-1330">CMD で bash -c コマンドのパイプを許可します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1330">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="b2153-1331">例:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="b2153-1331">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="b2153-1332">複数のページ ファイルがあるシステムに Bash をインストールできるようになりました (GH #538、#358)</span><span class="sxs-lookup"><span data-stu-id="b2153-1332">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="b2153-1333">既定の INET ソケット バッファー サイズは、既定の Ubuntu セットアップのものと一致している必要があります</span><span class="sxs-lookup"><span data-stu-id="b2153-1333">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="b2153-1334">xattr システム コールを listxattr に合わせて配置します</span><span class="sxs-lookup"><span data-stu-id="b2153-1334">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="b2153-1335">SIOCGIFCONF から有効な IPv4 アドレスを持つインターフェイスのみを返します</span><span class="sxs-lookup"><span data-stu-id="b2153-1335">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="b2153-1336">ptrace によって挿入される際のシグナルの既定のアクションを修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-1336">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="b2153-1337">/proc/sys/vm/min_free_kbytes を実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-1337">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="b2153-1338">sigreturn でコンテキストを復元するときにマシン コンテキスト レジスタの値を使用します</span><span class="sxs-lookup"><span data-stu-id="b2153-1338">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="b2153-1339">これにより、一部のユーザーで java と javac がハングしていた問題が解決されます</span><span class="sxs-lookup"><span data-stu-id="b2153-1339">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="b2153-1340">/proc/sys/kernel/hostname を実装します</span><span class="sxs-lookup"><span data-stu-id="b2153-1340">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1341">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1341">Syscall Support</span></span>
<span data-ttu-id="b2153-1342">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1342">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1343">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1343">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="b2153-1344">ビルド 14388 から Windows 10 Anniversary Update まで</span><span class="sxs-lookup"><span data-stu-id="b2153-1344">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="b2153-1345">ビルド 14388 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/14388wip)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1345">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b2153-1346">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1346">Fixed</span></span>
- <span data-ttu-id="b2153-1347">8/2 の Windows 10 Anniversary Update の準備をするための修正</span><span class="sxs-lookup"><span data-stu-id="b2153-1347">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="b2153-1348">Anniversary Update での WSL の詳細情報については、こちらの[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください</span><span class="sxs-lookup"><span data-stu-id="b2153-1348">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="b2153-1349">ビルド 14376</span><span class="sxs-lookup"><span data-stu-id="b2153-1349">Build 14376</span></span>
<span data-ttu-id="b2153-1350">ビルド 14376 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1350">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b2153-1351">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1351">Fixed</span></span>
- <span data-ttu-id="b2153-1352">apt-get がハングするいくつかのインスタンスを削除しました (GH #493)</span><span class="sxs-lookup"><span data-stu-id="b2153-1352">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="b2153-1353">空のマウントが正しく処理されなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1353">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="b2153-1354">ramdisk が正しくマウントされなかった問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1354">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="b2153-1355">フラグをサポートするように UNIX ソケット accept を変更します (一部 GH #451)</span><span class="sxs-lookup"><span data-stu-id="b2153-1355">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="b2153-1356">一般的なネットワークに関連したブルースクリーンを修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1356">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="b2153-1357">/proc/[pid]/task にアクセスするときのブルースクリーンを修正しました (GH #523)</span><span class="sxs-lookup"><span data-stu-id="b2153-1357">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="b2153-1358">一部の pty シナリオでの高い CPU 使用率を修正しました (GH #488、#504)</span><span class="sxs-lookup"><span data-stu-id="b2153-1358">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="b2153-1359">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1359">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="b2153-1360">ビルド 14371</span><span class="sxs-lookup"><span data-stu-id="b2153-1360">Build 14371</span></span>
<span data-ttu-id="b2153-1361">ビルド 14371 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1361">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b2153-1362">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1362">Fixed</span></span>
- <span data-ttu-id="b2153-1363">ptrace を使用する際の SIGCHLD と wait () のタイミングの競合を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1363">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="b2153-1364">パスの末尾に / がある場合の一部の動作を修正しました (GH #432)</span><span class="sxs-lookup"><span data-stu-id="b2153-1364">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="b2153-1365">子への開いたハンドルのために rename/unlink が失敗する問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1365">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="b2153-1366">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1366">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="b2153-1367">ビルド 14366</span><span class="sxs-lookup"><span data-stu-id="b2153-1367">Build 14366</span></span>
<span data-ttu-id="b2153-1368">ビルド 14366 の一般的な Windows 情報については、[Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1368">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b2153-1369">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1369">Fixed</span></span>
- <span data-ttu-id="b2153-1370">シンボリック リンクを使用したファイル作成の修正</span><span class="sxs-lookup"><span data-stu-id="b2153-1370">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="b2153-1371">Python 用 listxattr を追加しました (GH 385)</span><span class="sxs-lookup"><span data-stu-id="b2153-1371">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="b2153-1372">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1372">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1373">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1373">Syscall Support</span></span>
-   <span data-ttu-id="b2153-1374">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1374">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1375">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1375">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="b2153-1376">ビルド 14361</span><span class="sxs-lookup"><span data-stu-id="b2153-1376">Build 14361</span></span>
<span data-ttu-id="b2153-1377">ビルド 14361 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14361)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1377">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b2153-1378">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1378">Fixed</span></span>
- <span data-ttu-id="b2153-1379">Bash on Ubuntu on Windows で実行しているときに、DrvFs で大文字と小文字が区別されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1379">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="b2153-1380">ユーザーは、/mnt/c ドライブで case.txt と CASE.TXT を使用できます</span><span class="sxs-lookup"><span data-stu-id="b2153-1380">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="b2153-1381">大文字小文字の区別は、Bash on Ubuntu on Windows でのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b2153-1381">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="b2153-1382">Bash の外では、NTFS はファイルを正しく報告しますが、Windows からのファイルの操作で、予期しない動作が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1382">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="b2153-1383">各ボリュームのルート (つまり、/mnt/c) では大文字小文字の区別はありません</span><span class="sxs-lookup"><span data-stu-id="b2153-1383">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="b2153-1384">Windows でのこれらのファイルの処理について詳しくは、[こちら](https://support.microsoft.com/en-us/kb/100625)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1384">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="b2153-1385">pty / tty のサポートが大幅に強化されました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1385">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="b2153-1386">TMUX のようなアプリケーションがサポートされるようになりました (GH #40)</span><span class="sxs-lookup"><span data-stu-id="b2153-1386">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="b2153-1387">ユーザー アカウントが必ずしも作成されないというインストールの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1387">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="b2153-1388">非常に長い引数リストを使用できるように、コマンド ラインの引数の構造を最適化しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1388">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="b2153-1389">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="b2153-1389">(GH #153)</span></span>
- <span data-ttu-id="b2153-1390">DrvFs から read_only ファイルの削除および chmod を実行できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1390">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="b2153-1391">切断時にターミナルがハングする一部のインスタンスを修正しました (GH #43)</span><span class="sxs-lookup"><span data-stu-id="b2153-1391">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="b2153-1392">chmod および chown が tty デバイスで機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1392">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="b2153-1393">localhost として 0.0.0.0 および :: への接続を許可します (GH #388)</span><span class="sxs-lookup"><span data-stu-id="b2153-1393">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="b2153-1394">Sendmsg/recvmsg は、>1 の IO ベクトル長を処理するようになりました (一部 GH #376)</span><span class="sxs-lookup"><span data-stu-id="b2153-1394">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="b2153-1395">ユーザーは、自動生成された hosts ファイルをオプトアウトできるようになりました (GH #398)</span><span class="sxs-lookup"><span data-stu-id="b2153-1395">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="b2153-1396">インストール中に Linux のロケールを NT のロケールに自動的に一致させます (GH #11)</span><span class="sxs-lookup"><span data-stu-id="b2153-1396">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="b2153-1397">/proc/sys/vm/swappiness ファイルを追加しました (GH #306)</span><span class="sxs-lookup"><span data-stu-id="b2153-1397">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="b2153-1398">strace が正常に終了するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1398">strace now exits correctly</span></span>
- <span data-ttu-id="b2153-1399">/proc/self/fd を使用したパイプの再オープンを許可します (GH #222)</span><span class="sxs-lookup"><span data-stu-id="b2153-1399">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="b2153-1400">DrvFs で %LOCALAPPDATA%\lxss の下のディレクトリが非表示になります (GH #270)</span><span class="sxs-lookup"><span data-stu-id="b2153-1400">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="b2153-1401">bash.exe ~ の処理の改善。</span><span class="sxs-lookup"><span data-stu-id="b2153-1401">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="b2153-1402">“bash ~ -c ls” のようなコマンドがサポートされるようになりました (GH #467)</span><span class="sxs-lookup"><span data-stu-id="b2153-1402">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="b2153-1403">ソケットが、シャットダウン中に使用可能な epoll read を通知するようになりました (GH #271)</span><span class="sxs-lookup"><span data-stu-id="b2153-1403">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="b2153-1404">lxrun /uninstall でファイルとフォルダーの削除ジョブが改善されました</span><span class="sxs-lookup"><span data-stu-id="b2153-1404">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="b2153-1405">ps -f を修正しました (GH #246)</span><span class="sxs-lookup"><span data-stu-id="b2153-1405">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="b2153-1406">xEmacs などの x11 アプリのサポートを強化しました (GH #481)</span><span class="sxs-lookup"><span data-stu-id="b2153-1406">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="b2153-1407">既定の Ubuntu 設定に一致するように初期スレッドのスタック サイズを更新しました。また、get_rlimit システム コールにサイズを正しく報告します (GH #172、#258)</span><span class="sxs-lookup"><span data-stu-id="b2153-1407">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="b2153-1408">Pico プロセスのイメージ名の報告を改善しました (監査のためなど)</span><span class="sxs-lookup"><span data-stu-id="b2153-1408">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="b2153-1409">df コマンドに対して /proc/mountinfo を実装しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1409">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="b2153-1410">子名のシンボリック リンクのエラー コードを修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1410">Fixed symlink error code for child name .</span></span> <span data-ttu-id="b2153-1411">(. および ..)</span><span class="sxs-lookup"><span data-stu-id="b2153-1411">and ..</span></span>
- <span data-ttu-id="b2153-1412">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1412">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1413">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1413">Syscall Support</span></span>
<span data-ttu-id="b2153-1414">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1414">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1415">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1415">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="b2153-1416">ビルド 14352</span><span class="sxs-lookup"><span data-stu-id="b2153-1416">Build 14352</span></span>
<span data-ttu-id="b2153-1417">ビルド 14352 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14352)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1417">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1418">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1418">Fixed</span></span>
- <span data-ttu-id="b2153-1419">大きなファイルが正しくダウンロードまたは作成されなかった問題を修正しました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1419">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="b2153-1420">これにより、npm と他のシナリオのブロックが解除されます (GH #3、GH #313)</span><span class="sxs-lookup"><span data-stu-id="b2153-1420">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="b2153-1421">ソケットがハングするいくつかのインスタンスを削除しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1421">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="b2153-1422">いくつかの ptrace エラーを修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1422">Corrected some ptrace errors</span></span>
- <span data-ttu-id="b2153-1423">WSL で 255 文字を超えるファイル名が許可される問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1423">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="b2153-1424">英語以外の文字のサポートが強化されました</span><span class="sxs-lookup"><span data-stu-id="b2153-1424">Improved support for non-English characters</span></span>
- <span data-ttu-id="b2153-1425">現在の Windows タイムゾーンのデータを追加し、既定として設定します</span><span class="sxs-lookup"><span data-stu-id="b2153-1425">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="b2153-1426">マウント ポイントごとに一意のデバイス ID (JRE 修正 – GH #49)</span><span class="sxs-lookup"><span data-stu-id="b2153-1426">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="b2153-1427">“.”</span><span class="sxs-lookup"><span data-stu-id="b2153-1427">Correct issue with paths containing “.”</span></span> <span data-ttu-id="b2153-1428">および “..” を含むパスの問題を修正します</span><span class="sxs-lookup"><span data-stu-id="b2153-1428">and “..”</span></span>
- <span data-ttu-id="b2153-1429">Fifo のサポートを追加しました (GH #71)</span><span class="sxs-lookup"><span data-stu-id="b2153-1429">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="b2153-1430">ネイティブ Ubuntu 形式に一致するように resolv.conf の形式を更新しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1430">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="b2153-1431">一部の procfs のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="b2153-1431">Some procfs cleanup</span></span>
- <span data-ttu-id="b2153-1432">管理者コンソールの Ping を有効にしました (GH #18)</span><span class="sxs-lookup"><span data-stu-id="b2153-1432">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1433">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1433">Syscall Support</span></span>
<span data-ttu-id="b2153-1434">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1434">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1435">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1435">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="b2153-1436">ビルド 14342</span><span class="sxs-lookup"><span data-stu-id="b2153-1436">Build 14342</span></span>
<span data-ttu-id="b2153-1437">ビルド 14342 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14342)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1437">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="b2153-1438">VolFs および DriveFs の情報については、[WSL ブログ](https://blogs.msdn.microsoft.com/wsl)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1438">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b2153-1439">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1439">Fixed</span></span>
- <span data-ttu-id="b2153-1440">Windows ユーザーのユーザー名に Unicode 文字が含まれている場合のインストールの問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1440">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="b2153-1441">FAQ にある apt-get update udev の回避策が、初回の実行時に既定で提供されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1441">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="b2153-1442">DriveFs (/mnt/<drive>) ディレクトリでシンボリック リンクを有効にしました</span><span class="sxs-lookup"><span data-stu-id="b2153-1442">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="b2153-1443">シンボリック リンクが DriveFs と VolFs 間で機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1443">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="b2153-1444">アドレス指定された最上位のパス解析の問題に対処し、ls .// が期待どおりに動作するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1444">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="b2153-1445">DriveFs での npm install、および -g オプションが機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1445">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="b2153-1446">PHP サーバーの起動を妨げている問題を修正しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1446">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="b2153-1447">ネイティブ Ubuntu により近く一致するように $PATH などの既定の環境値を更新しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1447">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="b2153-1448">apt パッケージ キャッシュを更新するための Windows での週単位のメンテナンス タスクを追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1448">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="b2153-1449">ELF ヘッダー検証の問題を修正しました。WSL ですべての Melkor オプションがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1449">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="b2153-1450">Zsh シェルが機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1450">Zsh shell is functional</span></span>
- <span data-ttu-id="b2153-1451">プリコンパイル済みの Go バイナリがサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1451">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="b2153-1452">Bash.exe の初回実行時のプロンプトが正しくローカライズされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1452">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="b2153-1453">/proc/meminfo が正しい情報を返すようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1453">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="b2153-1454">ソケットが VFS でサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1454">Sockets now supported in VFS</span></span>
- <span data-ttu-id="b2153-1455">/dev が tempfs としてマウントされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1455">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="b2153-1456">Fifo がサポートされるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1456">Fifo now supported</span></span>
- <span data-ttu-id="b2153-1457">マルチコア システムが /proc/cpuinfo に正しく表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1457">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="b2153-1458">初回実行時のダウンロードにおける追加の改善とエラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="b2153-1458">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="b2153-1459">システム コールの機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="b2153-1459">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b2153-1460">サポートされるシステム コールの一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1460">Supported syscall list below.</span></span>
- <span data-ttu-id="b2153-1461">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1461">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="b2153-1462">の既知の問題</span><span class="sxs-lookup"><span data-stu-id="b2153-1462">Known Issues</span></span>
- <span data-ttu-id="b2153-1463">場合によって、DriveFs で ‘..’</span><span class="sxs-lookup"><span data-stu-id="b2153-1463">Not resolving ‘..’</span></span> <span data-ttu-id="b2153-1464">が正しく解決されません</span><span class="sxs-lookup"><span data-stu-id="b2153-1464">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1465">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1465">Syscall Support</span></span>
<span data-ttu-id="b2153-1466">次に示すのは、WSL に何らかの実装がある新しい、または強化されたシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1466">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b2153-1467">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1467">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="b2153-1468">ビルド 14332</span><span class="sxs-lookup"><span data-stu-id="b2153-1468">Build 14332</span></span>

<span data-ttu-id="b2153-1469">ビルド 14332 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14332)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1469">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="b2153-1470">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1470">Fixed</span></span>
- <span data-ttu-id="b2153-1471">DNS エントリの優先順位付けを含め、resolv.conf の生成が改善されました</span><span class="sxs-lookup"><span data-stu-id="b2153-1471">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="b2153-1472">/mnt ドライブと /mnt 以外のドライブとの間のファイルとディレクトリの移動に関する問題</span><span class="sxs-lookup"><span data-stu-id="b2153-1472">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="b2153-1473">シンボリック リンクを使って tar ファイルを作成できるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1473">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="b2153-1474">インスタンス作成時に既定の /run/lock ディレクトリを追加しました</span><span class="sxs-lookup"><span data-stu-id="b2153-1474">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="b2153-1475">適切な stat 情報を返すように /dev/null を更新します</span><span class="sxs-lookup"><span data-stu-id="b2153-1475">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="b2153-1476">初回実行時のダウンロードにおける追加エラー</span><span class="sxs-lookup"><span data-stu-id="b2153-1476">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="b2153-1477">システム コールの機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="b2153-1477">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b2153-1478">サポートされるシステム コールの一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1478">Supported syscall list below.</span></span>
- <span data-ttu-id="b2153-1479">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1479">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1480">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1480">Syscall Support</span></span>
<span data-ttu-id="b2153-1481">以下は、WSL に何らかの実装がある新しいシステム コールです。</span><span class="sxs-lookup"><span data-stu-id="b2153-1481">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="b2153-1482">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1482">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="b2153-1483">ビルド 14328</span><span class="sxs-lookup"><span data-stu-id="b2153-1483">Build 14328</span></span>

<span data-ttu-id="b2153-1484">ビルド 14332 の一般的な Windows 情報については、[Windows ブログ](https://aka.ms/wip14328)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2153-1484">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="b2153-1485">新機能</span><span class="sxs-lookup"><span data-stu-id="b2153-1485">New Features</span></span>
* <span data-ttu-id="b2153-1486">Linux ユーザーがサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1486">Now support Linux users.</span></span>  <span data-ttu-id="b2153-1487">Bash on Ubuntu on Windows をインストールすると、Linux ユーザーの作成を求めるプロンプトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2153-1487">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="b2153-1488">詳細については、 https://aka.ms/wslusers にアクセスしてください</span><span class="sxs-lookup"><span data-stu-id="b2153-1488">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="b2153-1489">ホスト名は、Windows コンピューター名に設定されるようになりました。@localhost はもう使用されません</span><span class="sxs-lookup"><span data-stu-id="b2153-1489">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="b2153-1490">ビルド 14328 の詳細については、次を参照してください: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="b2153-1490">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="b2153-1491">固定</span><span class="sxs-lookup"><span data-stu-id="b2153-1491">Fixed</span></span>
* <span data-ttu-id="b2153-1492">/mnt/<drive> 以外のファイルに対するシンボリック リンクの機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1492">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="b2153-1493">npm install が機能するようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1493">npm install now works</span></span>
    * <span data-ttu-id="b2153-1494">jdk / jre は、[こちら](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)の説明を使用してインストールできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2153-1494">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="b2153-1495">既知の問題: シンボリック リンクは Windows マウントでは機能しません。</span><span class="sxs-lookup"><span data-stu-id="b2153-1495">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="b2153-1496">機能は今後のビルドで使用できるようになる予定です</span><span class="sxs-lookup"><span data-stu-id="b2153-1496">Functionality will be available in a later build</span></span>
* <span data-ttu-id="b2153-1497">top と htop が表示されるようになりました</span><span class="sxs-lookup"><span data-stu-id="b2153-1497">top and htop now display</span></span>
* <span data-ttu-id="b2153-1498">一部のインストール エラーに対する追加のエラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="b2153-1498">Additional error messages for some install failures</span></span>
* <span data-ttu-id="b2153-1499">システム コールの機能強化とバグ修正。</span><span class="sxs-lookup"><span data-stu-id="b2153-1499">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="b2153-1500">サポートされるシステム コールの一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b2153-1500">Supported syscall list below.</span></span>
* <span data-ttu-id="b2153-1501">その他のバグ修正と機能強化</span><span class="sxs-lookup"><span data-stu-id="b2153-1501">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b2153-1502">システム コールのサポート</span><span class="sxs-lookup"><span data-stu-id="b2153-1502">Syscall Support</span></span>
<span data-ttu-id="b2153-1503">次に示すのは、WSL に何らかの実装があるシステム コールの一覧です。</span><span class="sxs-lookup"><span data-stu-id="b2153-1503">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="b2153-1504">この一覧にあるシステム コールは、少なくとも 1 つのシナリオではサポートされていますが、現時点では、一部のパラメーターがサポートされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2153-1504">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
