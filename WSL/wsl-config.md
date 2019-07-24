---
title: Linux ディストリビューションの管理
description: Windows Subsystem for Linux で実行されている複数の Linux ディストリビューションの一覧と構成については、こちらを参照してください。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、wsl. conf、wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: 0c9f9315b17d5156aa111e7619ee25534653b27e
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499280"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="cb30d-104">Windows Subsystem for Linux の管理と構成</span><span class="sxs-lookup"><span data-stu-id="cb30d-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="cb30d-105">Windows 10 の作成者の更新プログラム以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="cb30d-106">更新された[インストールガイド](./install_guide.md)を参照して、新しい管理機能を試し、Microsoft ストアから複数の Linux ディストリビューションの実行を開始してください。</span><span class="sxs-lookup"><span data-stu-id="cb30d-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="cb30d-107">WSL を実行する方法</span><span class="sxs-lookup"><span data-stu-id="cb30d-107">Ways to run WSL</span></span>

<span data-ttu-id="cb30d-108">Windows Subsystem for Linux を使用して Linux を実行するには、さまざまな方法があります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="cb30d-109">`[distro]`例えば`ubuntu`</span><span class="sxs-lookup"><span data-stu-id="cb30d-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="cb30d-110">`wsl.exe` または `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="cb30d-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="cb30d-111">`wsl [command]` または `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="cb30d-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="cb30d-112">どの方法を使用するかは、実行している内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="cb30d-113">ディストリビューションによる WSL の起動</span><span class="sxs-lookup"><span data-stu-id="cb30d-113">Launch WSL by distribution</span></span>

<span data-ttu-id="cb30d-114">ディストリビューション固有のアプリケーションを使用してディストリビューションを実行すると、その配布が独自のコンソールウィンドウで起動します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![[スタート] メニューから WSL を起動する](media/start-launch.png)

<span data-ttu-id="cb30d-116">これは、Microsoft ストアで [起動] をクリックすることと同じです。</span><span class="sxs-lookup"><span data-stu-id="cb30d-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Microsoft ストアから WSL を起動します](media/store-launch.png)

<span data-ttu-id="cb30d-118">を実行`[distribution].exe`してコマンドラインから配布を実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="cb30d-119">この方法でコマンドラインから配布を実行すると、作業ディレクトリが現在のディレクトリから配布のホームディレクトリに自動的に変更されるという欠点があります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="cb30d-120">**例:**</span><span class="sxs-lookup"><span data-stu-id="cb30d-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="cb30d-121">wsl および wsl [command]</span><span class="sxs-lookup"><span data-stu-id="cb30d-121">wsl and wsl [command]</span></span>

<span data-ttu-id="cb30d-122">コマンドラインから WSL を実行する最善の方法は、 `wsl.exe`を使用することです。</span><span class="sxs-lookup"><span data-stu-id="cb30d-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="cb30d-123">**例:**</span><span class="sxs-lookup"><span data-stu-id="cb30d-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="cb30d-124">現在の作業`wsl`ディレクトリをその場で保持するだけでなく、1つのコマンドを Windows コマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="cb30d-125">**例:**</span><span class="sxs-lookup"><span data-stu-id="cb30d-125">**Example:**</span></span>

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

<span data-ttu-id="cb30d-126">**例:**</span><span class="sxs-lookup"><span data-stu-id="cb30d-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="cb30d-127">複数の Linux ディストリビューションの管理</span><span class="sxs-lookup"><span data-stu-id="cb30d-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="cb30d-128">Windows 10 バージョン1903以降</span><span class="sxs-lookup"><span data-stu-id="cb30d-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="cb30d-129">を使用`wsl.exe`して、Windows Subsystem for Linux (wsl) でディストリビューションを管理できます。これには、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="cb30d-130">各 Linux ディストリビューションは、個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="cb30d-131">ディストリビューション固有のコマンドを表示するに`[distro.exe] /?`は、を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="cb30d-132">たとえば、 `ubuntu /?`があります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="cb30d-133">ディストリビューションの一覧表示</span><span class="sxs-lookup"><span data-stu-id="cb30d-133">List distributions</span></span>

<span data-ttu-id="cb30d-134">`wsl -l`,`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="cb30d-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="cb30d-135">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="cb30d-136">配布リストが表示されている場合は、インストールされており、使用準備ができています。</span><span class="sxs-lookup"><span data-stu-id="cb30d-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="cb30d-137">現在使用できないすべてのディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="cb30d-138">インストール、アンインストール、または破損した状態になっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="cb30d-139">現在実行中のすべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="cb30d-140">既定のディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="cb30d-140">Set a default distribution</span></span>

<span data-ttu-id="cb30d-141">既定の wsl ディストリビューションは、コマンドラインでを実行`wsl`するときに実行される分散です。</span><span class="sxs-lookup"><span data-stu-id="cb30d-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="cb30d-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="cb30d-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="cb30d-143">既定の分布をに`<DistributionName>`設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="cb30d-144">**例:**</span><span class="sxs-lookup"><span data-stu-id="cb30d-144">**Example:**</span></span>  
<span data-ttu-id="cb30d-145">`wsl -s Ubuntu`既定のディストリビューションを Ubuntu に設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="cb30d-146">実行`wsl npm init`すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="cb30d-147">これを実行`wsl`すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="cb30d-148">配布の登録解除と再インストール</span><span class="sxs-lookup"><span data-stu-id="cb30d-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="cb30d-149">Linux ディストリビューションは Microsoft ストアを介してインストールできますが、ストアを使用してアンインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cb30d-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="cb30d-150">WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="cb30d-151">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="cb30d-152">**注意:** 登録が解除されると、その配布に関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="cb30d-153">ストアから再インストールすると、配布のクリーンコピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="cb30d-154">WSL からのディストリビューションの登録を解除して、再インストールまたはクリーンアップできるようにします。</span><span class="sxs-lookup"><span data-stu-id="cb30d-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="cb30d-155">たとえば`wsl --unregister Ubuntu` 、は、wsl で使用可能なディストリビューションから Ubuntu を削除します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="cb30d-156">実行`wsl --list`すると、一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="cb30d-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="cb30d-157">を再インストールするには、Microsoft ストアで配布を見つけて、[Launch] \ (起動 \) を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="cb30d-158">特定のユーザーとして実行する</span><span class="sxs-lookup"><span data-stu-id="cb30d-158">Run as a specific user</span></span>

<span data-ttu-id="cb30d-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="cb30d-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="cb30d-160">指定されたユーザーとして WSL を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-160">Run WSL as the specified user.</span></span> <span data-ttu-id="cb30d-161">ユーザーは WSL 分布内に存在する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cb30d-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="cb30d-162">特定の配布を実行する</span><span class="sxs-lookup"><span data-stu-id="cb30d-162">Run a specific distribution</span></span>

<span data-ttu-id="cb30d-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="cb30d-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="cb30d-164">指定した WSL の分布を実行すると、既定値を変更しなくても、特定のディストリビューションにコマンドを送信できます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="cb30d-165">Windows 10 バージョン1903より前のバージョン</span><span class="sxs-lookup"><span data-stu-id="cb30d-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="cb30d-166">Wsl Config (`wslconfig.exe`) は、Windows Subsystem for linux (wsl) で実行されている linux ディストリビューションを管理するためのコマンドラインツールです。</span><span class="sxs-lookup"><span data-stu-id="cb30d-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="cb30d-167">これにより、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="cb30d-168">WSL Config は分布にまたがる設定に役立ちますが、各 Linux ディストリビューションは個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="cb30d-169">ディストリビューション固有のコマンドを表示するに`[distro.exe] /?`は、を実行します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="cb30d-170">たとえば、 `ubuntu /?`があります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="cb30d-171">Wslconfig で使用可能なすべてのオプションを表示するには、次のように実行します。`wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="cb30d-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="cb30d-172">ディストリビューションの一覧表示</span><span class="sxs-lookup"><span data-stu-id="cb30d-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="cb30d-173">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="cb30d-174">配布リストが表示されている場合は、インストールされており、使用準備ができています。</span><span class="sxs-lookup"><span data-stu-id="cb30d-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="cb30d-175">現在使用できないすべてのディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="cb30d-176">インストール、アンインストール、または破損した状態になっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="cb30d-177">既定のディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="cb30d-177">Set a default distribution</span></span>

<span data-ttu-id="cb30d-178">既定の wsl ディストリビューションは、コマンドラインでを実行`wsl`するときに実行される分散です。</span><span class="sxs-lookup"><span data-stu-id="cb30d-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="cb30d-179">既定の分布をに`<DistributionName>`設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="cb30d-180">**例:**</span><span class="sxs-lookup"><span data-stu-id="cb30d-180">**Example:**</span></span>  
<span data-ttu-id="cb30d-181">`wslconfig /setdefault Ubuntu`既定のディストリビューションを Ubuntu に設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="cb30d-182">実行`wsl npm init`すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="cb30d-183">これを実行`wsl`すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="cb30d-184">配布の登録解除と再インストール</span><span class="sxs-lookup"><span data-stu-id="cb30d-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="cb30d-185">Linux ディストリビューションは Microsoft ストアを介してインストールできますが、ストアを使用してアンインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cb30d-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="cb30d-186">WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="cb30d-187">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="cb30d-188">**注意:** 登録が解除されると、その配布に関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="cb30d-189">ストアから再インストールすると、配布のクリーンコピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="cb30d-190">WSL からのディストリビューションの登録を解除して、再インストールまたはクリーンアップできるようにします。</span><span class="sxs-lookup"><span data-stu-id="cb30d-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="cb30d-191">たとえば`wslconfig /unregister Ubuntu` 、は、wsl で使用可能なディストリビューションから Ubuntu を削除します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="cb30d-192">実行`wslconfig /list`すると、一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="cb30d-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="cb30d-193">を再インストールするには、Microsoft ストアで配布を見つけて、[Launch] \ (起動 \) を選択します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="cb30d-194">WSL 起動設定の設定</span><span class="sxs-lookup"><span data-stu-id="cb30d-194">Set WSL launch settings</span></span>

> <span data-ttu-id="cb30d-195">**Windows Insider Build 17093 以降で使用可能**</span><span class="sxs-lookup"><span data-stu-id="cb30d-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="cb30d-196">を使用して`wsl.conf`サブシステムを起動するたびに適用される、wsl の特定の機能を自動的に構成します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="cb30d-197">現時点では、これには自動マウントオプションとネットワーク構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb30d-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="cb30d-198">`wsl.conf`は、の`/etc/wsl.conf`各 Linux ディストリビューションにあります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="cb30d-199">ファイルが存在しない場合は、自分で作成できます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="cb30d-200">WSL は、ファイルの存在を検出し、その内容を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="cb30d-201">ファイルが見つからないか、形式が正しくない (つまり、不適切なマークアップ形式である) 場合、WSL は通常どおりに起動し続けます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="cb30d-202">ディストリビューションに追加できる`wsl.conf`サンプルファイルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="cb30d-203">構成オプション</span><span class="sxs-lookup"><span data-stu-id="cb30d-203">Configuration Options</span></span>

<span data-ttu-id="cb30d-204">.Ini 規則に従うと、キーはセクションの下で宣言されます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="cb30d-205">Wsl では`automount` 、との`network`2 つのセクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="cb30d-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="cb30d-206">オートマ</span><span class="sxs-lookup"><span data-stu-id="cb30d-206">automount</span></span>

<span data-ttu-id="cb30d-207">下`[automount]`</span><span class="sxs-lookup"><span data-stu-id="cb30d-207">Section: `[automount]`</span></span>


| <span data-ttu-id="cb30d-208">キー (key)</span><span class="sxs-lookup"><span data-stu-id="cb30d-208">key</span></span>        | <span data-ttu-id="cb30d-209">value</span><span class="sxs-lookup"><span data-stu-id="cb30d-209">value</span></span>                          | <span data-ttu-id="cb30d-210">既定値 (default)</span><span class="sxs-lookup"><span data-stu-id="cb30d-210">default</span></span>      | <span data-ttu-id="cb30d-211">注記</span><span class="sxs-lookup"><span data-stu-id="cb30d-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb30d-212">enabled</span><span class="sxs-lookup"><span data-stu-id="cb30d-212">enabled</span></span>    | <span data-ttu-id="cb30d-213">boolean</span><span class="sxs-lookup"><span data-stu-id="cb30d-213">boolean</span></span>                        | <span data-ttu-id="cb30d-214">true</span><span class="sxs-lookup"><span data-stu-id="cb30d-214">true</span></span>         | <span data-ttu-id="cb30d-215">`true`固定ドライブ (つまり、</span><span class="sxs-lookup"><span data-stu-id="cb30d-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="cb30d-216">`C:/`また`D:/`は) の場合、 `/mnt`drvfs で自動的にマウントされます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="cb30d-217">`false`ドライブは自動的にマウントされませんが、手動またはを使用`fstab`してマウントすることもできます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="cb30d-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="cb30d-218">mountFsTab</span></span> | <span data-ttu-id="cb30d-219">boolean</span><span class="sxs-lookup"><span data-stu-id="cb30d-219">boolean</span></span>                        | <span data-ttu-id="cb30d-220">true</span><span class="sxs-lookup"><span data-stu-id="cb30d-220">true</span></span>         | <span data-ttu-id="cb30d-221">`true`wsl start で処理されるように設定`/etc/fstab`します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="cb30d-222">/etc/fstab は、SMB 共有などの他のファイルシステムを宣言できるファイルです。</span><span class="sxs-lookup"><span data-stu-id="cb30d-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="cb30d-223">そのため、これらのファイルシステムは起動時に WSL に自動的にマウントできます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="cb30d-224">ルート</span><span class="sxs-lookup"><span data-stu-id="cb30d-224">root</span></span>       | <span data-ttu-id="cb30d-225">String</span><span class="sxs-lookup"><span data-stu-id="cb30d-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="cb30d-226">固定ドライブが自動的にマウントされるディレクトリを設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="cb30d-227">たとえば、wsl at `/windir/`にディレクトリがあり、それをルートとして指定すると、固定ドライブがにマウントされていることがわかります。`/windir/c`</span><span class="sxs-lookup"><span data-stu-id="cb30d-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="cb30d-228">options</span><span class="sxs-lookup"><span data-stu-id="cb30d-228">options</span></span>    | <span data-ttu-id="cb30d-229">値のコンマ区切りのリスト</span><span class="sxs-lookup"><span data-stu-id="cb30d-229">comma-separated list of values</span></span> | <span data-ttu-id="cb30d-230">空の文字列</span><span class="sxs-lookup"><span data-stu-id="cb30d-230">empty string</span></span> | <span data-ttu-id="cb30d-231">この値は、既定の DrvFs マウントオプション文字列に追加されます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="cb30d-232">**DrvFs 固有のオプションのみを指定できます。**</span><span class="sxs-lookup"><span data-stu-id="cb30d-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="cb30d-233">通常、マウントバイナリがフラグに解析するオプションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cb30d-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="cb30d-234">これらのオプションを明示的に指定する場合は、/etc/fstab で使用するすべてのドライブを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="cb30d-235">既定では、WSL は uid と gid を既定のユーザーの値に設定します (Ubuntu ディストリビューションでは、既定のユーザーは uid = 1000, gid = 1000 で作成されます)。</span><span class="sxs-lookup"><span data-stu-id="cb30d-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="cb30d-236">ユーザーがこのキーを使用して gid または uid オプションを明示的に指定した場合、関連付けられている値は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="cb30d-237">それ以外の場合は、既定値が常に追加されます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="cb30d-238">**注:** これらのオプションは、自動的にマウントされたすべてのドライブのマウントオプションとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="cb30d-239">特定のドライブのオプションのみを変更するには、代わりに/etc/fstab を使用します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="cb30d-240">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="cb30d-240">network</span></span>

<span data-ttu-id="cb30d-241">セクションラベル:`[network]`</span><span class="sxs-lookup"><span data-stu-id="cb30d-241">Section label: `[network]`</span></span>

| <span data-ttu-id="cb30d-242">キー (key)</span><span class="sxs-lookup"><span data-stu-id="cb30d-242">key</span></span> | <span data-ttu-id="cb30d-243">value</span><span class="sxs-lookup"><span data-stu-id="cb30d-243">value</span></span> | <span data-ttu-id="cb30d-244">既定値 (default)</span><span class="sxs-lookup"><span data-stu-id="cb30d-244">default</span></span> | <span data-ttu-id="cb30d-245">注記</span><span class="sxs-lookup"><span data-stu-id="cb30d-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="cb30d-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="cb30d-246">generateHosts</span></span> | <span data-ttu-id="cb30d-247">boolean</span><span class="sxs-lookup"><span data-stu-id="cb30d-247">boolean</span></span> | `true` | <span data-ttu-id="cb30d-248">`true`生成`/etc/hosts`する wsl を設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="cb30d-249">この`hosts`ファイルには、ホスト名に対応する IP アドレスの静的マップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb30d-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="cb30d-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="cb30d-250">generateResolvConf</span></span> | <span data-ttu-id="cb30d-251">boolean</span><span class="sxs-lookup"><span data-stu-id="cb30d-251">boolean</span></span> | `true` | <span data-ttu-id="cb30d-252">`true`生成`/etc/resolv.conf`するように wsl を設定します。</span><span class="sxs-lookup"><span data-stu-id="cb30d-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="cb30d-253">に`resolv.conf`は、指定されたホスト名を IP アドレスに解決できる DNS リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb30d-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="cb30d-254">固有</span><span class="sxs-lookup"><span data-stu-id="cb30d-254">interop</span></span>

<span data-ttu-id="cb30d-255">セクションラベル:`[interop]`</span><span class="sxs-lookup"><span data-stu-id="cb30d-255">Section label: `[interop]`</span></span>

<span data-ttu-id="cb30d-256">これらのオプションは、Insider Build 17713 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="cb30d-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="cb30d-257">キー (key)</span><span class="sxs-lookup"><span data-stu-id="cb30d-257">key</span></span> | <span data-ttu-id="cb30d-258">value</span><span class="sxs-lookup"><span data-stu-id="cb30d-258">value</span></span> | <span data-ttu-id="cb30d-259">既定値 (default)</span><span class="sxs-lookup"><span data-stu-id="cb30d-259">default</span></span> | <span data-ttu-id="cb30d-260">注記</span><span class="sxs-lookup"><span data-stu-id="cb30d-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="cb30d-261">enabled</span><span class="sxs-lookup"><span data-stu-id="cb30d-261">enabled</span></span> | <span data-ttu-id="cb30d-262">boolean</span><span class="sxs-lookup"><span data-stu-id="cb30d-262">boolean</span></span> | `true` | <span data-ttu-id="cb30d-263">このキーを設定すると、WSL が Windows プロセスの起動をサポートするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="cb30d-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="cb30d-264">appendWindowsPath</span></span> | <span data-ttu-id="cb30d-265">boolean</span><span class="sxs-lookup"><span data-stu-id="cb30d-265">boolean</span></span> | `true` | <span data-ttu-id="cb30d-266">このキーを設定すると、WSL が Windows パス要素を $PATH 環境変数に追加するかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="cb30d-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
