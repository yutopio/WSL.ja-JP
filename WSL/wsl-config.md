---
title: Linux ディストリビューションを管理します。
description: 一覧に表示され、Linux 用 Windows サブシステムで実行されている複数の Linux ディストリビューションの構成を参照します。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、wsl.conf wslconfig 用 windows サブシステム
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063500"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="3bbe0-104">管理および Linux 用の Windows サブシステムの構成</span><span class="sxs-lookup"><span data-stu-id="3bbe0-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="3bbe0-105">Windows 10 Fall Creators Update 以降を適用します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="3bbe0-106">表示、更新された[インストール ガイド](./install_guide.md)新しい管理機能を Windows ストアからの複数の Linux ディストリビューションの実行を開始します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Windows Store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="3bbe0-107">WSL を実行する方法</span><span class="sxs-lookup"><span data-stu-id="3bbe0-107">Ways to run WSL</span></span>

<span data-ttu-id="3bbe0-108">Linux 用 Windows サブシステムで Linux を実行する方法はたくさんあります。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="3bbe0-109">`[distro]` ie `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-109">`[distro]` ie `ubuntu`</span></span>
1. <span data-ttu-id="3bbe0-110">`wsl.exe` または `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="3bbe0-111">`wsl [command]` または `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="3bbe0-112">使用する必要がありますメソッドは、何をしているに依存します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="3bbe0-113">WSL を配布して起動します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-113">Launch WSL by distribution</span></span>

<span data-ttu-id="3bbe0-114">ディストリビューション固有のアプリケーションを使用してディストリビューションを実行して、独自のコンソール ウィンドウには、その配布を起動します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![WSL を [スタート] メニューから起動します。](media/start-launch.png)

<span data-ttu-id="3bbe0-116">Windows ストアで「起動」をクリックすると同じです。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-116">It is the same as clicking "Launch" in the Windows Store.</span></span>

![Windows ストアから WSL を起動します。](media/store-launch.png)

<span data-ttu-id="3bbe0-118">実行して、コマンドラインから、配布を実行することも`[distribution].exe`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="3bbe0-119">ディストリビューションを実行して、この方法でコマンドラインからの欠点はことには自動的に作業ディレクトリ現在のディレクトリからに変更配布のホーム ディレクトリ。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="3bbe0-120">**例:**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-120">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="3bbe0-121">wsl と wsl [コマンド]</span><span class="sxs-lookup"><span data-stu-id="3bbe0-121">wsl and wsl [command]</span></span>

<span data-ttu-id="3bbe0-122">WSL をコマンドラインから実行する最善の方法を使用して`wsl.exe`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="3bbe0-123">**例:**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="3bbe0-124">だけでなく`wsl`に現在の作業ディレクトリを維持、に沿って側の Windows のコマンドの 1 つのコマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="3bbe0-125">**例:**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-125">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

<span data-ttu-id="3bbe0-126">**例:**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-126">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="3bbe0-127">複数の Linux ディストリビューションを管理します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="3bbe0-128">Windows 10 バージョンが 1903 以降</span><span class="sxs-lookup"><span data-stu-id="3bbe0-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="3bbe0-129">使用することができます`wsl.exe`ディストリビューション、Windows サブシステムでの Linux (WSL)、利用可能なディストリビューションの一覧を表示する既定のディストリビューションを設定、ディストリビューションをアンインストールするなどを管理します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="3bbe0-130">各 Linux ディストリビューションが独自の構成を個別に管理します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="3bbe0-131">ディストリビューション固有のコマンドを表示する実行`[distro.exe] /?`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="3bbe0-132">たとえば、 `ubuntu /?`があります。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="3bbe0-133">ディストリビューションの一覧</span><span class="sxs-lookup"><span data-stu-id="3bbe0-133">List distributions</span></span>

<span data-ttu-id="3bbe0-134">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="3bbe0-135">WSL を利用できる Linux ディストリビューションを使用可能なを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="3bbe0-136">分布が表示されている場合がインストールされ、使用する準備が完了します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="3bbe0-137">現在使用するものも含め、すべてのディストリビューションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="3bbe0-138">これらは、アンインストール、インストールすると、処理中である可能性がありますや破損した状態では。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="3bbe0-139">現在実行されているすべてのディストリビューションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="3bbe0-140">既定の配布を設定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-140">Set a default distribution</span></span>

<span data-ttu-id="3bbe0-141">既定のディストリビューションで WSL を実行するときに実行される 1 つ`wsl`コマンド行にします。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="3bbe0-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="3bbe0-143">既定の配布を設定`<DistributionName>`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="3bbe0-144">**例:**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-144">**Example:**</span></span>  
<span data-ttu-id="3bbe0-145">`wsl -s Ubuntu` 既定のディストリビューションを Ubuntu に設定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="3bbe0-146">今すぐ実行すると`wsl npm init`Ubuntu で実行されます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="3bbe0-147">実行した場合の`wsl`Ubuntu のセッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="3bbe0-148">登録を解除して、配布を再インストール</span><span class="sxs-lookup"><span data-stu-id="3bbe0-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="3bbe0-149">Linux ディストリビューションは、Windows でインストールできるときにストアは、ストアからをアンインストールできません。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-149">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="3bbe0-150">WSL 構成は、未登録のアンインストールに配布できます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="3bbe0-151">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="3bbe0-152">**注:**、登録を解除するとすべてのデータ、設定、およびそのディストリビューションに関連付けられているソフトウェアは完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="3bbe0-153">ストアから再インストールすると、分布のクリーンなコピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="3bbe0-154">WSL から配布を再インストールまたはクリーンアップできるように登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="3bbe0-155">例: `wsl -unregister Ubuntu` WSL で使用可能なディストリビューションから Ubuntu を削除します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-155">For example: `wsl -unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="3bbe0-156">実行すると`wsl --list`表示されません。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="3bbe0-157">を再インストールするには、Windows ストアで、分布を検索し、「起動」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-157">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="3bbe0-158">特定のユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-158">Run as a specific user</span></span>

<span data-ttu-id="3bbe0-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="3bbe0-160">WSL は、指定したユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-160">Run WSL as the specified user.</span></span> <span data-ttu-id="3bbe0-161">WSL 配布内でそのユーザーが存在する必要がありますに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="3bbe0-162">特定の配布を実行します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-162">Run a specific distribution</span></span>

<span data-ttu-id="3bbe0-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="3bbe0-164">WSL の指定した配布を実行する、既定値を変更することがなく特定の配布のコマンドを送信するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="3bbe0-165">Windows 10 バージョンが 1903 より前のバージョン</span><span class="sxs-lookup"><span data-stu-id="3bbe0-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="3bbe0-166">WSL Config (`wslconfig.exe`) for Linux (WSL) Windows サブシステムで実行されている Linux ディストリビューションを管理するためのコマンド ライン ツールです。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="3bbe0-167">利用可能なディストリビューションを一覧表示、設定の既定のディストリビューションおよびディストリビューションをアンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="3bbe0-168">WSL Config は span またはディストリビューションの調整設定の場合に便利ですが、各 Linux ディストリビューション個別に管理しない独自構成します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="3bbe0-169">ディストリビューション固有のコマンドを表示する実行`[distro.exe] /?`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="3bbe0-170">たとえば、 `ubuntu /?`があります。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="3bbe0-171">Wslconfig のすべての使用可能なオプションを表示するには、次のコマンドを実行します。  `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a><span data-ttu-id="3bbe0-172">ディストリビューションの一覧</span><span class="sxs-lookup"><span data-stu-id="3bbe0-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="3bbe0-173">WSL を利用できる Linux ディストリビューションを使用可能なを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="3bbe0-174">分布が表示されている場合がインストールされ、使用する準備が完了します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="3bbe0-175">現在使用するものも含め、すべてのディストリビューションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="3bbe0-176">これらは、アンインストール、インストールすると、処理中である可能性がありますや破損した状態では。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="3bbe0-177">既定の配布を設定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-177">Set a default distribution</span></span>

<span data-ttu-id="3bbe0-178">既定のディストリビューションで WSL を実行するときに実行される 1 つ`wsl`コマンド行にします。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="3bbe0-179">既定の配布を設定`<DistributionName>`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="3bbe0-180">**例:**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-180">**Example:**</span></span>  
<span data-ttu-id="3bbe0-181">`wslconfig /setdefault Ubuntu` 既定のディストリビューションを Ubuntu に設定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="3bbe0-182">今すぐ実行すると`wsl npm init`Ubuntu で実行されます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="3bbe0-183">実行した場合の`wsl`Ubuntu のセッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="3bbe0-184">登録を解除して、配布を再インストール</span><span class="sxs-lookup"><span data-stu-id="3bbe0-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="3bbe0-185">Linux ディストリビューションは、Windows でインストールできるときにストアは、ストアからをアンインストールできません。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-185">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="3bbe0-186">WSL 構成は、未登録のアンインストールに配布できます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="3bbe0-187">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="3bbe0-188">**注:**、登録を解除するとすべてのデータ、設定、およびそのディストリビューションに関連付けられているソフトウェアは完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="3bbe0-189">ストアから再インストールすると、分布のクリーンなコピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="3bbe0-190">WSL から配布を再インストールまたはクリーンアップできるように登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="3bbe0-191">例: `wslconfig /unregister Ubuntu` WSL で使用可能なディストリビューションから Ubuntu を削除します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="3bbe0-192">実行すると`wslconfig /list`表示されません。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="3bbe0-193">を再インストールするには、Windows ストアで、分布を検索し、「起動」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-193">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="3bbe0-194">WSL 起動を設定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-194">Set WSL launch settings</span></span>

> <span data-ttu-id="3bbe0-195">**Windows Insider ビルド 17093 で使用でき、それ以降**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="3bbe0-196">サブシステムを使用して、起動するたびに適用される WSL で特定の機能を自動構成`wsl.conf`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="3bbe0-197">右にはここで、これが含まれていますに対する自動マウント オプションおよびネットワークの構成。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="3bbe0-198">`wsl.conf` 場合は、各 Linux ディストリビューションである`/etc/wsl.conf`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="3bbe0-199">ファイルがない場合を自分でその作成できます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="3bbe0-200">WSL では、ファイルの存在が検出され、その内容を読み取る。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="3bbe0-201">ファイルが見つからないか、形式が正しくない場合 (つまり、不適切なマークアップの書式設定)、WSL は引き続き通常どおり起動します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="3bbe0-202">サンプルを次に示します`wsl.conf`ファイルは、ディストリビューションに追加できます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="3bbe0-203">構成オプション</span><span class="sxs-lookup"><span data-stu-id="3bbe0-203">Configuration Options</span></span>

<span data-ttu-id="3bbe0-204">.Ini の表記規則、合わせてセクション、キーとして宣言されます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="3bbe0-205">WSL は、2 つのセクションをサポートしています:`automount`と`network`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="3bbe0-206">自動マウント</span><span class="sxs-lookup"><span data-stu-id="3bbe0-206">automount</span></span>

<span data-ttu-id="3bbe0-207">セクションの内容: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-207">Section: `[automount]`</span></span>


| <span data-ttu-id="3bbe0-208">key</span><span class="sxs-lookup"><span data-stu-id="3bbe0-208">key</span></span>        | <span data-ttu-id="3bbe0-209">value</span><span class="sxs-lookup"><span data-stu-id="3bbe0-209">value</span></span>                          | <span data-ttu-id="3bbe0-210">既定値 (default)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-210">default</span></span>      | <span data-ttu-id="3bbe0-211">ノート</span><span class="sxs-lookup"><span data-stu-id="3bbe0-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbe0-212">enabled</span><span class="sxs-lookup"><span data-stu-id="3bbe0-212">enabled</span></span>    | <span data-ttu-id="3bbe0-213">boolean</span><span class="sxs-lookup"><span data-stu-id="3bbe0-213">boolean</span></span>                        | <span data-ttu-id="3bbe0-214">true</span><span class="sxs-lookup"><span data-stu-id="3bbe0-214">true</span></span>         | <span data-ttu-id="3bbe0-215">`true` 固定ドライブ (つまり、エラーの原因</span><span class="sxs-lookup"><span data-stu-id="3bbe0-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="3bbe0-216">`C:/` または`D:/`) DrvFs 下で自動的にマウントする`/mnt`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="3bbe0-217">`false` ドライブを自動的にマウントしないを手動でまたはを使用してに引き続きマウントしてでした`fstab`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="3bbe0-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="3bbe0-218">mountFsTab</span></span> | <span data-ttu-id="3bbe0-219">boolean</span><span class="sxs-lookup"><span data-stu-id="3bbe0-219">boolean</span></span>                        | <span data-ttu-id="3bbe0-220">true</span><span class="sxs-lookup"><span data-stu-id="3bbe0-220">true</span></span>         | <span data-ttu-id="3bbe0-221">`true` 設定`/etc/fstab`処理する WSL 開始します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="3bbe0-222">/etc/fstab は、SMB 共有のように、その他のファイル システムを宣言するファイルです。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="3bbe0-223">したがっての開始時に WSL で自動的にこれらのファイル システムをマウントできます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="3bbe0-224">ルート</span><span class="sxs-lookup"><span data-stu-id="3bbe0-224">root</span></span>       | <span data-ttu-id="3bbe0-225">String</span><span class="sxs-lookup"><span data-stu-id="3bbe0-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="3bbe0-226">固定ドライブが自動的にマウントされます、ディレクトリを設定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="3bbe0-227">WSL でのディレクトリがある場合など`/windir/`指定こととして、ルートには必要でマウントされている固定ドライブを参照してください。 `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="3bbe0-228">オプション</span><span class="sxs-lookup"><span data-stu-id="3bbe0-228">options</span></span>    | <span data-ttu-id="3bbe0-229">値のコンマ区切りの一覧</span><span class="sxs-lookup"><span data-stu-id="3bbe0-229">comma-separated list of values</span></span> | <span data-ttu-id="3bbe0-230">空の文字列</span><span class="sxs-lookup"><span data-stu-id="3bbe0-230">empty string</span></span> | <span data-ttu-id="3bbe0-231">この値は、既定 DrvFs マウント オプション文字列に追加されます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="3bbe0-232">**DrvFs 固有のオプションのみを指定することができます。**</span><span class="sxs-lookup"><span data-stu-id="3bbe0-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="3bbe0-233">バイナリのマウントがフラグに解析は通常のオプションがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="3bbe0-234">これらのオプションを明示的に指定する場合は、/etc/fstab で実行するすべてのドライブを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="3bbe0-235">既定では、WSL uid と gid 値に設定の既定のユーザー (uid を使用した Ubuntu ディストリビューションでは、既定のユーザーが作成 = 1000、gid = 1000)。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="3bbe0-236">ユーザーは、このキーを使用して明示的に gid または uid オプションを指定する場合、関連付けられている値が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="3bbe0-237">それ以外の場合、既定値は常に追加されます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="3bbe0-238">**注:** これらのオプションは、すべて自動的にマウントされたドライブのマウント オプションとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="3bbe0-239">特定のドライブのみのオプションを変更するには、/etc/fstab を代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="3bbe0-240">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="3bbe0-240">network</span></span>

<span data-ttu-id="3bbe0-241">セクション ラベル: `[network]`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-241">Section label: `[network]`</span></span>

| <span data-ttu-id="3bbe0-242">key</span><span class="sxs-lookup"><span data-stu-id="3bbe0-242">key</span></span> | <span data-ttu-id="3bbe0-243">value</span><span class="sxs-lookup"><span data-stu-id="3bbe0-243">value</span></span> | <span data-ttu-id="3bbe0-244">既定値 (default)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-244">default</span></span> | <span data-ttu-id="3bbe0-245">ノート</span><span class="sxs-lookup"><span data-stu-id="3bbe0-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="3bbe0-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="3bbe0-246">generateHosts</span></span> | <span data-ttu-id="3bbe0-247">boolean</span><span class="sxs-lookup"><span data-stu-id="3bbe0-247">boolean</span></span> | `true` | <span data-ttu-id="3bbe0-248">`true` 設定を生成する WSL`/etc/hosts`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="3bbe0-249">`hosts`ファイルには、ホスト名の対応する IP アドレスの静的なマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="3bbe0-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="3bbe0-250">generateResolvConf</span></span> | <span data-ttu-id="3bbe0-251">boolean</span><span class="sxs-lookup"><span data-stu-id="3bbe0-251">boolean</span></span> | `true` | <span data-ttu-id="3bbe0-252">`true` 設定を生成する WSL`/etc/resolv.conf`します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="3bbe0-253">`resolv.conf`特定のホスト名をその IP アドレスに解決することができる DNS の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="3bbe0-254">相互運用機能</span><span class="sxs-lookup"><span data-stu-id="3bbe0-254">interop</span></span>

<span data-ttu-id="3bbe0-255">セクション ラベル: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="3bbe0-255">Section label: `[interop]`</span></span>

<span data-ttu-id="3bbe0-256">これらのオプションとは、以降 Insider ビルド 17713 で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="3bbe0-257">key</span><span class="sxs-lookup"><span data-stu-id="3bbe0-257">key</span></span> | <span data-ttu-id="3bbe0-258">value</span><span class="sxs-lookup"><span data-stu-id="3bbe0-258">value</span></span> | <span data-ttu-id="3bbe0-259">既定値 (default)</span><span class="sxs-lookup"><span data-stu-id="3bbe0-259">default</span></span> | <span data-ttu-id="3bbe0-260">ノート</span><span class="sxs-lookup"><span data-stu-id="3bbe0-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="3bbe0-261">enabled</span><span class="sxs-lookup"><span data-stu-id="3bbe0-261">enabled</span></span> | <span data-ttu-id="3bbe0-262">boolean</span><span class="sxs-lookup"><span data-stu-id="3bbe0-262">boolean</span></span> | `true` | <span data-ttu-id="3bbe0-263">このキーの設定で、WSL が Windows の起動プロセスをサポートするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="3bbe0-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="3bbe0-264">appendWindowsPath</span></span> | <span data-ttu-id="3bbe0-265">boolean</span><span class="sxs-lookup"><span data-stu-id="3bbe0-265">boolean</span></span> | `true` | <span data-ttu-id="3bbe0-266">このキーの設定で、WSL が $PATH 環境変数に Windows のパス要素を追加するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3bbe0-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
