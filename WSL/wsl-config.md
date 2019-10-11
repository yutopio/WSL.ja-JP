---
title: Linux ディストリビューションの管理
description: Windows Subsystem for Linux で実行されている複数の Linux ディストリビューションの一覧表示と構成に関するリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e69810625d08baf734683ff06231f79132ce1519
ms.sourcegitcommit: e1cc2fe4de0fa03d5aea14f6b328f1bb9d0c59be
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2019
ms.locfileid: "71999393"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="58e1c-104">Windows Subsystem for Linux の管理と構成</span><span class="sxs-lookup"><span data-stu-id="58e1c-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="58e1c-105">Windows 10 Fall Creators Update 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="58e1c-106">新しい管理機能を試して、Microsoft Store から複数の Linux ディストリビューションの実行を開始するには、更新された[インストール ガイド](./install_guide.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58e1c-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="58e1c-107">WSL を実行する方法</span><span class="sxs-lookup"><span data-stu-id="58e1c-107">Ways to run WSL</span></span>

<span data-ttu-id="58e1c-108">Windows Subsystem for Linux での Linux の実行には、さまざまな方法があります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="58e1c-109">`[distro]`、例えば `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="58e1c-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="58e1c-110">`wsl.exe` または `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="58e1c-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="58e1c-111">`wsl [command]` または `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="58e1c-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="58e1c-112">どの方法を使用すべきかは、作業内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="58e1c-113">ディストリビューションによって WSL を起動する</span><span class="sxs-lookup"><span data-stu-id="58e1c-113">Launch WSL by distribution</span></span>

<span data-ttu-id="58e1c-114">ディストリビューション固有のアプリケーションを使用してディストリビューションを実行すると、そのディストリビューションが独自のコンソール ウィンドウで起動します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![[スタート] メニューからの WSL の起動](media/start-launch.png)

<span data-ttu-id="58e1c-116">これは、Microsoft Store で [起動] をクリックすることと同じです。</span><span class="sxs-lookup"><span data-stu-id="58e1c-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Microsoft Store からの WSL の起動](media/store-launch.png)

<span data-ttu-id="58e1c-118">`[distribution].exe` を実行して、コマンド ラインからディストリビューションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="58e1c-119">この方法でコマンド ラインからディストリビューションを実行すると、作業ディレクトリが現在のディレクトリからディストリビューションのホーム ディレクトリに自動的に変更されるという欠点があります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="58e1c-120">**例:**</span><span class="sxs-lookup"><span data-stu-id="58e1c-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="58e1c-121">wsl および wsl [コマンド]</span><span class="sxs-lookup"><span data-stu-id="58e1c-121">wsl and wsl [command]</span></span>

<span data-ttu-id="58e1c-122">コマンド ラインから WSL を実行する最善の方法は、`wsl.exe` を使用することです。</span><span class="sxs-lookup"><span data-stu-id="58e1c-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="58e1c-123">**例:**</span><span class="sxs-lookup"><span data-stu-id="58e1c-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="58e1c-124">`wsl` は、現在の作業ディレクトリを適切に維持するだけでなく、1 つのコマンドを Windows コマンドとともに実行できます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="58e1c-125">**例:**</span><span class="sxs-lookup"><span data-stu-id="58e1c-125">**Example:**</span></span>

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

<span data-ttu-id="58e1c-126">**例:**</span><span class="sxs-lookup"><span data-stu-id="58e1c-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="58e1c-127">複数の Linux ディストリビューションの管理</span><span class="sxs-lookup"><span data-stu-id="58e1c-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="58e1c-128">Windows 10 バージョン 1903 以降</span><span class="sxs-lookup"><span data-stu-id="58e1c-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="58e1c-129">`wsl.exe` を使用して、Windows Subsystem for Linux (WSL) のディストリビューションを管理できます。これには、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、ディストリビューションのアンインストールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="58e1c-130">各 Linux ディストリビューションは、個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="58e1c-131">ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="58e1c-132">たとえば、`ubuntu /?` のように指定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="58e1c-133">ディストリビューションの一覧表示</span><span class="sxs-lookup"><span data-stu-id="58e1c-133">List distributions</span></span>

<span data-ttu-id="58e1c-134">`wsl -l`、`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="58e1c-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="58e1c-135">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="58e1c-136">一覧表示されているディストリビューションは、インストールされており、使用できる状態です。</span><span class="sxs-lookup"><span data-stu-id="58e1c-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="58e1c-137">現在使用できないディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="58e1c-138">インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="58e1c-139">現在実行中のディストリビューションをすべて一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="58e1c-140">既定のディストリビューションの設定</span><span class="sxs-lookup"><span data-stu-id="58e1c-140">Set a default distribution</span></span>

<span data-ttu-id="58e1c-141">既定の WSL ディストリビューションは、コマンド ラインで `wsl` を実行するときに実行されるものです。</span><span class="sxs-lookup"><span data-stu-id="58e1c-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="58e1c-142">`wsl -s <DistributionName>`、`wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="58e1c-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="58e1c-143">既定のディストリビューションを `<DistributionName>` に設定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="58e1c-144">**例:**</span><span class="sxs-lookup"><span data-stu-id="58e1c-144">**Example:**</span></span>  
<span data-ttu-id="58e1c-145">`wsl -s Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="58e1c-146">これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="58e1c-147">`wsl` を実行すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="58e1c-148">ディストリビューションの登録解除と再インストール</span><span class="sxs-lookup"><span data-stu-id="58e1c-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="58e1c-149">Linux ディストリビューションは Microsoft Store を介してインストールできますが、そのストアを介してアンインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="58e1c-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="58e1c-150">WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="58e1c-151">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="58e1c-152">**注:** 登録が解除されると、そのディストリビューションに関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="58e1c-153">ストアから再インストールすると、ディストリビューションのクリーン コピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="58e1c-154">ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="58e1c-155">たとえば、`wsl --unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="58e1c-156">`wsl --list` を実行すると、それは一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="58e1c-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="58e1c-157">再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="58e1c-158">特定のユーザーとしての実行</span><span class="sxs-lookup"><span data-stu-id="58e1c-158">Run as a specific user</span></span>

<span data-ttu-id="58e1c-159">`wsl -u <Username>`、`wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="58e1c-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="58e1c-160">指定されたユーザーとして WSL を実行します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-160">Run WSL as the specified user.</span></span> <span data-ttu-id="58e1c-161">ユーザーは WSL ディストリビューション内に存在する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="58e1c-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="58e1c-162">特定のディストリビューションの実行</span><span class="sxs-lookup"><span data-stu-id="58e1c-162">Run a specific distribution</span></span>

<span data-ttu-id="58e1c-163">`wsl -d <DistributionName>`、`wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="58e1c-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="58e1c-164">WSL の指定したディストリビューションの実行は、既定値を変更する必要なしに、特定のディストリビューションにコマンドを送信するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="58e1c-165">Windows 10 バージョン 1903 より前のバージョン</span><span class="sxs-lookup"><span data-stu-id="58e1c-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="58e1c-166">WSL Config (`wslconfig.exe`) は、Windows Subsystem for Linux (WSL) で実行されている Linux ディストリビューションを管理するためのコマンド ライン ツールです。</span><span class="sxs-lookup"><span data-stu-id="58e1c-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="58e1c-167">これにより、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="58e1c-168">WSL Config はディストリビューションにまたがる設定やそれらを調整する設定に役立ちますが、各 Linux ディストリビューションは個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="58e1c-169">ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="58e1c-170">たとえば、`ubuntu /?` のように指定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="58e1c-171">wslconfig で使用可能なオプションをすべて表示するには、`wslconfig /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="58e1c-172">ディストリビューションの一覧表示</span><span class="sxs-lookup"><span data-stu-id="58e1c-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="58e1c-173">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="58e1c-174">一覧表示されているディストリビューションは、インストールされており、使用できる状態です。</span><span class="sxs-lookup"><span data-stu-id="58e1c-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="58e1c-175">現在使用できないディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="58e1c-176">インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="58e1c-177">既定のディストリビューションの設定</span><span class="sxs-lookup"><span data-stu-id="58e1c-177">Set a default distribution</span></span>

<span data-ttu-id="58e1c-178">既定の WSL ディストリビューションは、コマンド ラインで `wsl` を実行するときに実行されるものです。</span><span class="sxs-lookup"><span data-stu-id="58e1c-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="58e1c-179">既定のディストリビューションを `<DistributionName>` に設定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="58e1c-180">**例:**</span><span class="sxs-lookup"><span data-stu-id="58e1c-180">**Example:**</span></span>  
<span data-ttu-id="58e1c-181">`wslconfig /setdefault Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="58e1c-182">これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="58e1c-183">`wsl` を実行すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="58e1c-184">ディストリビューションの登録解除と再インストール</span><span class="sxs-lookup"><span data-stu-id="58e1c-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="58e1c-185">Linux ディストリビューションは Microsoft Store を介してインストールできますが、そのストアを介してアンインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="58e1c-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="58e1c-186">WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="58e1c-187">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="58e1c-188">**注:** 登録が解除されると、そのディストリビューションに関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="58e1c-189">ストアから再インストールすると、ディストリビューションのクリーン コピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="58e1c-190">ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="58e1c-191">たとえば、`wslconfig /unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="58e1c-192">`wslconfig /list` を実行すると、それは一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="58e1c-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="58e1c-193">再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="58e1c-194">WSL 起動設定の実行</span><span class="sxs-lookup"><span data-stu-id="58e1c-194">Set WSL launch settings</span></span>

> <span data-ttu-id="58e1c-195">**Windows Insider Build 17093 以降で使用可能**</span><span class="sxs-lookup"><span data-stu-id="58e1c-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="58e1c-196">`wsl.conf` を使用して、サブシステムを起動するたびに適用される、WSL の特定の機能を自動的に構成します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="58e1c-197">現時点では、これには自動マウント オプションとネットワーク構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="58e1c-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="58e1c-198">`wsl.conf` は、`/etc/wsl.conf` 内の各 Linux ディストリビューションにあります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="58e1c-199">そのファイルがそこになければ、自分で作成できます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="58e1c-200">WSL は、ファイルの存在を検出し、その内容を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="58e1c-201">ファイルが見つからないか、形式が正しくない (つまり、不適切なマークアップ形式である) 場合、WSL は通常どおりに起動を続けます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="58e1c-202">ディストリビューションに追加できる `wsl.conf` サンプル ファイルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="58e1c-203">構成オプション</span><span class="sxs-lookup"><span data-stu-id="58e1c-203">Configuration Options</span></span>

<span data-ttu-id="58e1c-204">.ini 規則に従って、キーはセクションの下で宣言されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="58e1c-205">WSL では、`automount` と `network` の 2 つのセクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="58e1c-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="58e1c-206">automount</span><span class="sxs-lookup"><span data-stu-id="58e1c-206">automount</span></span>

<span data-ttu-id="58e1c-207">セクション: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="58e1c-207">Section: `[automount]`</span></span>


| <span data-ttu-id="58e1c-208">key</span><span class="sxs-lookup"><span data-stu-id="58e1c-208">key</span></span>        | <span data-ttu-id="58e1c-209">value</span><span class="sxs-lookup"><span data-stu-id="58e1c-209">value</span></span>                          | <span data-ttu-id="58e1c-210">既定</span><span class="sxs-lookup"><span data-stu-id="58e1c-210">default</span></span>      | <span data-ttu-id="58e1c-211">注</span><span class="sxs-lookup"><span data-stu-id="58e1c-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e1c-212">enabled</span><span class="sxs-lookup"><span data-stu-id="58e1c-212">enabled</span></span>    | <span data-ttu-id="58e1c-213">boolean</span><span class="sxs-lookup"><span data-stu-id="58e1c-213">boolean</span></span>                        | <span data-ttu-id="58e1c-214">true</span><span class="sxs-lookup"><span data-stu-id="58e1c-214">true</span></span>         | <span data-ttu-id="58e1c-215">`true` にすると、固定ドライブ (つまり、</span><span class="sxs-lookup"><span data-stu-id="58e1c-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="58e1c-216">`C:/` または`D:/`) は `/mnt` の下に DrvFs で自動的にマウントされます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="58e1c-217">`false` にすると、ドライブは自動的にマウントされませんが、依然として手動または `fstab` を使用してマウントできます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="58e1c-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="58e1c-218">mountFsTab</span></span> | <span data-ttu-id="58e1c-219">boolean</span><span class="sxs-lookup"><span data-stu-id="58e1c-219">boolean</span></span>                        | <span data-ttu-id="58e1c-220">true</span><span class="sxs-lookup"><span data-stu-id="58e1c-220">true</span></span>         | <span data-ttu-id="58e1c-221">`true` にすると、WSL 開始時に処理されるように `/etc/fstab` を設定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="58e1c-222">/etc/fstab は、SMB 共有などの他のファイル システムを宣言できるファイルです。</span><span class="sxs-lookup"><span data-stu-id="58e1c-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="58e1c-223">そのため、起動時にこれらのファイル システムを WSL 内で自動的にマウントできます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="58e1c-224">root</span><span class="sxs-lookup"><span data-stu-id="58e1c-224">root</span></span>       | <span data-ttu-id="58e1c-225">String</span><span class="sxs-lookup"><span data-stu-id="58e1c-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="58e1c-226">固定ドライブが自動的にマウントされるディレクトリを設定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="58e1c-227">たとえば、`/windir/` に WSL のディレクトリがあり、それをルートとして指定すると、固定ドライブは `/windir/c` でマウントされることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="58e1c-228">オプション</span><span class="sxs-lookup"><span data-stu-id="58e1c-228">options</span></span>    | <span data-ttu-id="58e1c-229">値のコンマ区切りのリスト</span><span class="sxs-lookup"><span data-stu-id="58e1c-229">comma-separated list of values</span></span> | <span data-ttu-id="58e1c-230">空の文字列</span><span class="sxs-lookup"><span data-stu-id="58e1c-230">empty string</span></span> | <span data-ttu-id="58e1c-231">この値は、既定の DrvFs マウント オプション文字列に追加されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="58e1c-232">**DrvFs 固有のオプションのみを指定できます。**</span><span class="sxs-lookup"><span data-stu-id="58e1c-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="58e1c-233">マウント バイナリが通常、フラグに解析するオプションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="58e1c-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="58e1c-234">これらのオプションを明示的に指定する場合は、それを行う対象のドライブすべてを /etc/fstab に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="58e1c-235">既定では、WSL は uid と gid を既定のユーザーの値に設定します (Ubuntu ディストリビューションでは、既定のユーザーは uid = 1000、gid = 1000 で作成されます)。</span><span class="sxs-lookup"><span data-stu-id="58e1c-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="58e1c-236">ユーザーがこのキーを使用して gid または uid オプションを明示的に指定した場合、関連する値は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="58e1c-237">それ以外の場合は、既定値が常に追加されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="58e1c-238">**注:** これらのオプションは、自動的にマウントされたドライブすべてのマウント オプションとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="58e1c-239">特定のドライブのみのオプションを変更するには、代わりに /etc/fstab を使用します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

##### <a name="mount-options"></a><span data-ttu-id="58e1c-240">マウント オプション</span><span class="sxs-lookup"><span data-stu-id="58e1c-240">Mount options</span></span>

<span data-ttu-id="58e1c-241">Windows ドライブ (DrvFs) にさまざまなマウント オプションを設定すると、Windows ファイルのファイルのアクセス許可を計算する方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="58e1c-242">次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-242">The following options are available:</span></span>

| <span data-ttu-id="58e1c-243">Key</span><span class="sxs-lookup"><span data-stu-id="58e1c-243">Key</span></span> | <span data-ttu-id="58e1c-244">説明</span><span class="sxs-lookup"><span data-stu-id="58e1c-244">Description</span></span> | <span data-ttu-id="58e1c-245">Default</span><span class="sxs-lookup"><span data-stu-id="58e1c-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="58e1c-246">uid</span><span class="sxs-lookup"><span data-stu-id="58e1c-246">uid</span></span>| <span data-ttu-id="58e1c-247">すべてのファイルの所有者に使用するユーザー ID</span><span class="sxs-lookup"><span data-stu-id="58e1c-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="58e1c-248">WSL ディストリビューションの既定のユーザー ID (初回インストールの場合、既定値は 1000)</span><span class="sxs-lookup"><span data-stu-id="58e1c-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="58e1c-249">gid</span><span class="sxs-lookup"><span data-stu-id="58e1c-249">gid</span></span>| <span data-ttu-id="58e1c-250">すべてのファイルの所有者に使用するグループ ID</span><span class="sxs-lookup"><span data-stu-id="58e1c-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="58e1c-251">WSL ディストリビューションの既定のグループ ID (初回インストールの場合、既定値は 1000)</span><span class="sxs-lookup"><span data-stu-id="58e1c-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="58e1c-252">umask</span><span class="sxs-lookup"><span data-stu-id="58e1c-252">umask</span></span> | <span data-ttu-id="58e1c-253">すべてのファイルとディレクトリに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="58e1c-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="58e1c-254">000</span><span class="sxs-lookup"><span data-stu-id="58e1c-254">000</span></span>
|<span data-ttu-id="58e1c-255">fmask</span><span class="sxs-lookup"><span data-stu-id="58e1c-255">fmask</span></span> | <span data-ttu-id="58e1c-256">すべてのファイルに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="58e1c-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="58e1c-257">000</span><span class="sxs-lookup"><span data-stu-id="58e1c-257">000</span></span>
|<span data-ttu-id="58e1c-258">dmask</span><span class="sxs-lookup"><span data-stu-id="58e1c-258">dmask</span></span> | <span data-ttu-id="58e1c-259">すべてのディレクトリに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="58e1c-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="58e1c-260">000</span><span class="sxs-lookup"><span data-stu-id="58e1c-260">000</span></span>

<span data-ttu-id="58e1c-261">**注:** アクセス許可のマスクは、ファイルまたはディレクトリに適用される前に論理 OR 演算によって配置されます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="58e1c-262">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="58e1c-262">network</span></span>

<span data-ttu-id="58e1c-263">セクションのラベル: `[network]`</span><span class="sxs-lookup"><span data-stu-id="58e1c-263">Section label: `[network]`</span></span>

| <span data-ttu-id="58e1c-264">key</span><span class="sxs-lookup"><span data-stu-id="58e1c-264">key</span></span> | <span data-ttu-id="58e1c-265">value</span><span class="sxs-lookup"><span data-stu-id="58e1c-265">value</span></span> | <span data-ttu-id="58e1c-266">既定</span><span class="sxs-lookup"><span data-stu-id="58e1c-266">default</span></span> | <span data-ttu-id="58e1c-267">注</span><span class="sxs-lookup"><span data-stu-id="58e1c-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="58e1c-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="58e1c-268">generateHosts</span></span> | <span data-ttu-id="58e1c-269">boolean</span><span class="sxs-lookup"><span data-stu-id="58e1c-269">boolean</span></span> | `true` | <span data-ttu-id="58e1c-270">`true` にすると、`/etc/hosts` を生成するように WSL を設定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="58e1c-271">`hosts` ファイルには、IP アドレスに対応するホスト名の静的マップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="58e1c-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="58e1c-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="58e1c-272">generateResolvConf</span></span> | <span data-ttu-id="58e1c-273">boolean</span><span class="sxs-lookup"><span data-stu-id="58e1c-273">boolean</span></span> | `true` | <span data-ttu-id="58e1c-274">`true` にすると、`/etc/resolv.conf` を生成するように WSL を設定します。</span><span class="sxs-lookup"><span data-stu-id="58e1c-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="58e1c-275">`resolv.conf` には、指定されたホスト名をその IP アドレスに解決できる DNS リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="58e1c-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="58e1c-276">interop</span><span class="sxs-lookup"><span data-stu-id="58e1c-276">interop</span></span>

<span data-ttu-id="58e1c-277">セクションのラベル: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="58e1c-277">Section label: `[interop]`</span></span>

<span data-ttu-id="58e1c-278">次のオプションは、Insider Build 17713 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="58e1c-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="58e1c-279">key</span><span class="sxs-lookup"><span data-stu-id="58e1c-279">key</span></span> | <span data-ttu-id="58e1c-280">value</span><span class="sxs-lookup"><span data-stu-id="58e1c-280">value</span></span> | <span data-ttu-id="58e1c-281">既定</span><span class="sxs-lookup"><span data-stu-id="58e1c-281">default</span></span> | <span data-ttu-id="58e1c-282">注</span><span class="sxs-lookup"><span data-stu-id="58e1c-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="58e1c-283">enabled</span><span class="sxs-lookup"><span data-stu-id="58e1c-283">enabled</span></span> | <span data-ttu-id="58e1c-284">boolean</span><span class="sxs-lookup"><span data-stu-id="58e1c-284">boolean</span></span> | `true` | <span data-ttu-id="58e1c-285">このキーの設定により、WSL で Windows プロセスの起動をサポートするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="58e1c-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="58e1c-286">appendWindowsPath</span></span> | <span data-ttu-id="58e1c-287">boolean</span><span class="sxs-lookup"><span data-stu-id="58e1c-287">boolean</span></span> | `true` | <span data-ttu-id="58e1c-288">このキーの設定により、WSL が Windows パス要素を $PATH 環境変数に追加するかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="58e1c-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
