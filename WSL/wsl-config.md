---
title: Linux ディストリビューションの管理
description: Windows Subsystem for Linux で実行されている複数の Linux ディストリビューションの一覧表示と構成に関するリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: 59419919be138a20ab57e1a6d26a411e1531bf9f
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235900"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="d14ba-104">WSL コマンドと起動構成</span><span class="sxs-lookup"><span data-stu-id="d14ba-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="d14ba-105">WSL を実行する方法</span><span class="sxs-lookup"><span data-stu-id="d14ba-105">Ways to run WSL</span></span>

<span data-ttu-id="d14ba-106">WSL を[インストール](install-win10.md)した Linux ディストリビューションを実行するには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="d14ba-107">Windows の [スタート] メニューにアクセスし、インストールされているディストリビューションの名前を入力して、Linux ディストリビューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="d14ba-108">たとえば、"Ubuntu" のようになります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="d14ba-109">Windows のコマンドプロンプトまたは PowerShell から、インストールされている配布の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="d14ba-110">例: `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="d14ba-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="d14ba-111">Windows コマンドプロンプトまたは PowerShell から、現在のコマンドライン内で既定の Linux ディストリビューションを開くには、「」と入力し `wsl.exe` ます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="d14ba-112">Windows コマンドプロンプトまたは PowerShell から、現在のコマンドライン内で既定の Linux ディストリビューションを開くには、「」と入力し `wsl [command]` ます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="d14ba-113">どの方法を使用すべきかは、作業内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="d14ba-114">Windows プロンプトまたは PowerShell ウィンドウ内で WSL コマンドラインを開いて終了する場合は、コマンドを入力します `exit` 。</span><span class="sxs-lookup"><span data-stu-id="d14ba-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="d14ba-115">ディストリビューションによって WSL を起動する</span><span class="sxs-lookup"><span data-stu-id="d14ba-115">Launch WSL by distribution</span></span>

<span data-ttu-id="d14ba-116">ディストリビューション固有のアプリケーションを使用してディストリビューションを実行すると、そのディストリビューションが独自のコンソール ウィンドウで起動します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![[スタート] メニューからの WSL の起動](media/start-launch.png)

<span data-ttu-id="d14ba-118">これは、Microsoft Store で [起動] をクリックすることと同じです。</span><span class="sxs-lookup"><span data-stu-id="d14ba-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Microsoft Store からの WSL の起動](media/store-launch.png)

<span data-ttu-id="d14ba-120">`[distribution].exe` を実行して、コマンド ラインからディストリビューションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="d14ba-121">この方法でコマンド ラインからディストリビューションを実行すると、作業ディレクトリが現在のディレクトリからディストリビューションのホーム ディレクトリに自動的に変更されるという欠点があります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="d14ba-122">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="d14ba-122">**Example: (using PowerShell)**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="d14ba-123">wsl および wsl [コマンド]</span><span class="sxs-lookup"><span data-stu-id="d14ba-123">wsl and wsl [command]</span></span>

<span data-ttu-id="d14ba-124">コマンド ラインから WSL を実行する最善の方法は、`wsl.exe` を使用することです。</span><span class="sxs-lookup"><span data-stu-id="d14ba-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="d14ba-125">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="d14ba-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="d14ba-126">`wsl` は、現在の作業ディレクトリを適切に維持するだけでなく、1 つのコマンドを Windows コマンドとともに実行できます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="d14ba-127">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="d14ba-127">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

<span data-ttu-id="d14ba-128">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="d14ba-128">**Example: (using PowerShell)**</span></span>

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

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="d14ba-129">複数の Linux ディストリビューションの管理</span><span class="sxs-lookup"><span data-stu-id="d14ba-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="d14ba-130">Windows 10 バージョン 1903[以降](ms-settings:windowsupdate)では、を使用して `wsl.exe` Windows Subsystem for Linux (wsl) でのディストリビューションを管理できます。これには、使用可能なディストリビューションの一覧表示、既定の配布の設定、およびディストリビューションのアンインストールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="d14ba-131">各 Linux ディストリビューションは、個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="d14ba-132">ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="d14ba-133">たとえば、「 `ubuntu /?` 」のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="d14ba-134">ディストリビューションの一覧表示</span><span class="sxs-lookup"><span data-stu-id="d14ba-134">List distributions</span></span>

<span data-ttu-id="d14ba-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="d14ba-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="d14ba-136">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="d14ba-137">一覧表示されているディストリビューションは、インストールされており、使用できる状態です。</span><span class="sxs-lookup"><span data-stu-id="d14ba-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="d14ba-138">`wsl --list --all`現在使用できないすべてのディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="d14ba-139">インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="d14ba-140">`wsl --list --running`現在実行中のすべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="d14ba-141">既定のディストリビューションの設定</span><span class="sxs-lookup"><span data-stu-id="d14ba-141">Set a default distribution</span></span>

<span data-ttu-id="d14ba-142">既定の WSL ディストリビューションは、コマンド ラインで `wsl` を実行するときに実行されるものです。</span><span class="sxs-lookup"><span data-stu-id="d14ba-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="d14ba-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="d14ba-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="d14ba-144">既定のディストリビューションを `<DistributionName>` に設定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="d14ba-145">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="d14ba-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="d14ba-146">`wsl -s Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="d14ba-147">これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="d14ba-148">`wsl` を実行すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="d14ba-149">ディストリビューションの登録解除と再インストール</span><span class="sxs-lookup"><span data-stu-id="d14ba-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="d14ba-150">Linux ディストリビューションは Microsoft Store を介してインストールできますが、そのストアを介してアンインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d14ba-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="d14ba-151">WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="d14ba-152">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="d14ba-153">**注意:** 登録が解除されると、その配布に関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="d14ba-154">ストアから再インストールすると、ディストリビューションのクリーン コピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="d14ba-155">ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="d14ba-156">たとえば、`wsl --unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="d14ba-157">`wsl --list` を実行すると、それは一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="d14ba-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="d14ba-158">再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="d14ba-159">特定のユーザーとしての実行</span><span class="sxs-lookup"><span data-stu-id="d14ba-159">Run as a specific user</span></span>

<span data-ttu-id="d14ba-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="d14ba-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="d14ba-161">指定されたユーザーとして WSL を実行します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-161">Run WSL as the specified user.</span></span> <span data-ttu-id="d14ba-162">ユーザーは WSL ディストリビューション内に存在する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d14ba-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="run-a-specific-distribution"></a><span data-ttu-id="d14ba-163">特定のディストリビューションの実行</span><span class="sxs-lookup"><span data-stu-id="d14ba-163">Run a specific distribution</span></span>

<span data-ttu-id="d14ba-164">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="d14ba-164">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="d14ba-165">WSL の指定したディストリビューションの実行は、既定値を変更する必要なしに、特定のディストリビューションにコマンドを送信するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-165">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="d14ba-166">以前のバージョンの Windows での複数の Linux ディストリビューションの管理</span><span class="sxs-lookup"><span data-stu-id="d14ba-166">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="d14ba-167">バージョン1903より前の Windows 10 では、WSL Config ( `wslconfig.exe` ) コマンドラインツールを使用して、Windows Subsystem For linux (wsl) で実行されている linux ディストリビューションを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-167">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="d14ba-168">これにより、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-168">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="d14ba-169">WSL Config はディストリビューションにまたがる設定やそれらを調整する設定に役立ちますが、各 Linux ディストリビューションは個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-169">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="d14ba-170">ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-170">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="d14ba-171">たとえば、「 `ubuntu /?` 」のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-171">For example `ubuntu /?`.</span></span>

<span data-ttu-id="d14ba-172">wslconfig で使用可能なオプションをすべて表示するには、`wslconfig /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-172">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

<span data-ttu-id="d14ba-173">ディストリビューションを一覧表示するには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-173">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="d14ba-174">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-174">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="d14ba-175">一覧表示されているディストリビューションは、インストールされており、使用できる状態です。</span><span class="sxs-lookup"><span data-stu-id="d14ba-175">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="d14ba-176">現在使用できないディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-176">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="d14ba-177">インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-177">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="d14ba-178">コマンドラインでを実行したときに実行される既定のディストリビューションを設定するには、次のようにし `wsl` ます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-178">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="d14ba-179">`wslconfig /setdefault <DistributionName>`既定の分布をに設定 `<DistributionName>` します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-179">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="d14ba-180">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="d14ba-180">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="d14ba-181">`wslconfig /setdefault Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="d14ba-182">これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="d14ba-183">`wsl` を実行すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-183">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="d14ba-184">配布を登録解除して再インストールするには:</span><span class="sxs-lookup"><span data-stu-id="d14ba-184">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="d14ba-185">ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-185">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="d14ba-186">たとえば、`wslconfig /unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-186">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="d14ba-187">`wslconfig /list` を実行すると、それは一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="d14ba-187">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="d14ba-188">再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-188">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="d14ba-189">ディストリビューションごとの起動設定を wslconf で構成する</span><span class="sxs-lookup"><span data-stu-id="d14ba-189">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="d14ba-190">**Windows ビルド17093以降で使用可能**</span><span class="sxs-lookup"><span data-stu-id="d14ba-190">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="d14ba-191">`wsl.conf` を使用して、サブシステムを起動するたびに適用される、WSL の特定の機能を自動的に構成します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-191">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="d14ba-192">現時点では、これには自動マウント オプションとネットワーク構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d14ba-192">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="d14ba-193">`wsl.conf` は、`/etc/wsl.conf` 内の各 Linux ディストリビューションにあります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-193">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="d14ba-194">そのファイルがそこになければ、自分で作成できます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-194">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="d14ba-195">WSL は、ファイルの存在を検出し、その内容を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-195">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="d14ba-196">ファイルが見つからないか、形式が正しくない (つまり、不適切なマークアップ形式である) 場合、WSL は通常どおりに起動を続けます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-196">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="d14ba-197">`wsl.conf`ディストリビューションに追加できるサンプルファイルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-197">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="d14ba-198">構成オプション</span><span class="sxs-lookup"><span data-stu-id="d14ba-198">Configuration Options</span></span>

<span data-ttu-id="d14ba-199">.ini 規則に従って、キーはセクションの下で宣言されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-199">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="d14ba-200">WSL では、`automount` と `network` の 2 つのセクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d14ba-200">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="d14ba-201">automount</span><span class="sxs-lookup"><span data-stu-id="d14ba-201">automount</span></span>

<span data-ttu-id="d14ba-202">セクション: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="d14ba-202">Section: `[automount]`</span></span>

| <span data-ttu-id="d14ba-203">key</span><span class="sxs-lookup"><span data-stu-id="d14ba-203">key</span></span>        | <span data-ttu-id="d14ba-204">value</span><span class="sxs-lookup"><span data-stu-id="d14ba-204">value</span></span>                          | <span data-ttu-id="d14ba-205">default</span><span class="sxs-lookup"><span data-stu-id="d14ba-205">default</span></span>      | <span data-ttu-id="d14ba-206">notes</span><span class="sxs-lookup"><span data-stu-id="d14ba-206">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d14ba-207">enabled</span><span class="sxs-lookup"><span data-stu-id="d14ba-207">enabled</span></span>    | <span data-ttu-id="d14ba-208">boolean</span><span class="sxs-lookup"><span data-stu-id="d14ba-208">boolean</span></span>                        | <span data-ttu-id="d14ba-209">true</span><span class="sxs-lookup"><span data-stu-id="d14ba-209">true</span></span>         | <span data-ttu-id="d14ba-210">`true` にすると、固定ドライブ (つまり、</span><span class="sxs-lookup"><span data-stu-id="d14ba-210">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="d14ba-211">`C:/` または`D:/`) は `/mnt` の下に DrvFs で自動的にマウントされます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-211">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="d14ba-212">`false`ドライブは自動的にマウントされませんが、手動またはを使用してマウントすることもでき `fstab` ます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-212">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="d14ba-213">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="d14ba-213">mountFsTab</span></span> | <span data-ttu-id="d14ba-214">boolean</span><span class="sxs-lookup"><span data-stu-id="d14ba-214">boolean</span></span>                        | <span data-ttu-id="d14ba-215">true</span><span class="sxs-lookup"><span data-stu-id="d14ba-215">true</span></span>         | <span data-ttu-id="d14ba-216">`true` にすると、WSL 開始時に処理されるように `/etc/fstab` を設定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-216">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="d14ba-217">/etc/fstab は、SMB 共有などの他のファイル システムを宣言できるファイルです。</span><span class="sxs-lookup"><span data-stu-id="d14ba-217">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="d14ba-218">そのため、起動時にこれらのファイル システムを WSL 内で自動的にマウントできます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-218">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="d14ba-219">root</span><span class="sxs-lookup"><span data-stu-id="d14ba-219">root</span></span>       | <span data-ttu-id="d14ba-220">String</span><span class="sxs-lookup"><span data-stu-id="d14ba-220">String</span></span>                         | `/mnt/`      | <span data-ttu-id="d14ba-221">固定ドライブが自動的にマウントされるディレクトリを設定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-221">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="d14ba-222">たとえば、`/windir/` に WSL のディレクトリがあり、それをルートとして指定すると、固定ドライブは `/windir/c` でマウントされることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-222">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="d14ba-223">options</span><span class="sxs-lookup"><span data-stu-id="d14ba-223">options</span></span>    | <span data-ttu-id="d14ba-224">値のコンマ区切りのリスト</span><span class="sxs-lookup"><span data-stu-id="d14ba-224">comma-separated list of values</span></span> | <span data-ttu-id="d14ba-225">空の文字列</span><span class="sxs-lookup"><span data-stu-id="d14ba-225">empty string</span></span> | <span data-ttu-id="d14ba-226">この値は、既定の DrvFs マウント オプション文字列に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-226">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="d14ba-227">**DrvFs 固有のオプションのみを指定できます。**</span><span class="sxs-lookup"><span data-stu-id="d14ba-227">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="d14ba-228">マウント バイナリが通常、フラグに解析するオプションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d14ba-228">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="d14ba-229">これらのオプションを明示的に指定する場合は、それを行う対象のドライブすべてを /etc/fstab に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-229">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="d14ba-230">既定では、WSL は uid と gid を既定のユーザーの値に設定します (Ubuntu ディストリビューションでは、既定のユーザーは uid = 1000、gid = 1000 で作成されます)。</span><span class="sxs-lookup"><span data-stu-id="d14ba-230">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="d14ba-231">ユーザーがこのキーを使用して gid または uid オプションを明示的に指定した場合、関連する値は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-231">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="d14ba-232">それ以外の場合は、既定値が常に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-232">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="d14ba-233">**注:** これらのオプションは、自動的にマウントされたすべてのドライブのマウントオプションとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-233">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="d14ba-234">特定のドライブのみのオプションを変更するには、代わりに /etc/fstab を使用します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-234">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="d14ba-235">マウント オプション</span><span class="sxs-lookup"><span data-stu-id="d14ba-235">Mount options</span></span>

<span data-ttu-id="d14ba-236">Windows ドライブ (DrvFs) にさまざまなマウント オプションを設定すると、Windows ファイルのファイルのアクセス許可を計算する方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-236">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="d14ba-237">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-237">The following options are available:</span></span>

| <span data-ttu-id="d14ba-238">Key</span><span class="sxs-lookup"><span data-stu-id="d14ba-238">Key</span></span> | <span data-ttu-id="d14ba-239">説明</span><span class="sxs-lookup"><span data-stu-id="d14ba-239">Description</span></span> | <span data-ttu-id="d14ba-240">Default</span><span class="sxs-lookup"><span data-stu-id="d14ba-240">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="d14ba-241">uid</span><span class="sxs-lookup"><span data-stu-id="d14ba-241">uid</span></span>| <span data-ttu-id="d14ba-242">すべてのファイルの所有者に使用するユーザー ID</span><span class="sxs-lookup"><span data-stu-id="d14ba-242">The User ID used for the owner of all files</span></span> | <span data-ttu-id="d14ba-243">WSL ディストリビューションの既定のユーザー ID (初回インストールの場合、既定値は 1000)</span><span class="sxs-lookup"><span data-stu-id="d14ba-243">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="d14ba-244">gid</span><span class="sxs-lookup"><span data-stu-id="d14ba-244">gid</span></span>| <span data-ttu-id="d14ba-245">すべてのファイルの所有者に使用するグループ ID</span><span class="sxs-lookup"><span data-stu-id="d14ba-245">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="d14ba-246">WSL ディストリビューションの既定のグループ ID (初回インストールの場合、既定値は 1000)</span><span class="sxs-lookup"><span data-stu-id="d14ba-246">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="d14ba-247">umask</span><span class="sxs-lookup"><span data-stu-id="d14ba-247">umask</span></span> | <span data-ttu-id="d14ba-248">すべてのファイルとディレクトリに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="d14ba-248">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="d14ba-249">000</span><span class="sxs-lookup"><span data-stu-id="d14ba-249">000</span></span>
|<span data-ttu-id="d14ba-250">fmask</span><span class="sxs-lookup"><span data-stu-id="d14ba-250">fmask</span></span> | <span data-ttu-id="d14ba-251">すべてのファイルに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="d14ba-251">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="d14ba-252">000</span><span class="sxs-lookup"><span data-stu-id="d14ba-252">000</span></span>
|<span data-ttu-id="d14ba-253">dmask</span><span class="sxs-lookup"><span data-stu-id="d14ba-253">dmask</span></span> | <span data-ttu-id="d14ba-254">すべてのディレクトリに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="d14ba-254">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="d14ba-255">000</span><span class="sxs-lookup"><span data-stu-id="d14ba-255">000</span></span>

<span data-ttu-id="d14ba-256">**注:** アクセス許可マスクは、ファイルまたはディレクトリに適用される前に論理 OR 演算によって配置されます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-256">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="d14ba-257">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="d14ba-257">network</span></span>

<span data-ttu-id="d14ba-258">セクションのラベル: `[network]`</span><span class="sxs-lookup"><span data-stu-id="d14ba-258">Section label: `[network]`</span></span>

| <span data-ttu-id="d14ba-259">key</span><span class="sxs-lookup"><span data-stu-id="d14ba-259">key</span></span> | <span data-ttu-id="d14ba-260">value</span><span class="sxs-lookup"><span data-stu-id="d14ba-260">value</span></span> | <span data-ttu-id="d14ba-261">default</span><span class="sxs-lookup"><span data-stu-id="d14ba-261">default</span></span> | <span data-ttu-id="d14ba-262">notes</span><span class="sxs-lookup"><span data-stu-id="d14ba-262">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d14ba-263">generateHosts</span><span class="sxs-lookup"><span data-stu-id="d14ba-263">generateHosts</span></span> | <span data-ttu-id="d14ba-264">boolean</span><span class="sxs-lookup"><span data-stu-id="d14ba-264">boolean</span></span> | `true` | <span data-ttu-id="d14ba-265">`true` にすると、`/etc/hosts` を生成するように WSL を設定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-265">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="d14ba-266">`hosts` ファイルには、IP アドレスに対応するホスト名の静的マップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d14ba-266">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="d14ba-267">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="d14ba-267">generateResolvConf</span></span> | <span data-ttu-id="d14ba-268">boolean</span><span class="sxs-lookup"><span data-stu-id="d14ba-268">boolean</span></span> | `true` | <span data-ttu-id="d14ba-269">`true` にすると、`/etc/resolv.conf` を生成するように WSL を設定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-269">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="d14ba-270">`resolv.conf` には、指定されたホスト名をその IP アドレスに解決できる DNS リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d14ba-270">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="d14ba-271">interop</span><span class="sxs-lookup"><span data-stu-id="d14ba-271">interop</span></span>

<span data-ttu-id="d14ba-272">セクションのラベル: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="d14ba-272">Section label: `[interop]`</span></span>

<span data-ttu-id="d14ba-273">次のオプションは、Insider Build 17713 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-273">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="d14ba-274">key</span><span class="sxs-lookup"><span data-stu-id="d14ba-274">key</span></span> | <span data-ttu-id="d14ba-275">value</span><span class="sxs-lookup"><span data-stu-id="d14ba-275">value</span></span> | <span data-ttu-id="d14ba-276">default</span><span class="sxs-lookup"><span data-stu-id="d14ba-276">default</span></span> | <span data-ttu-id="d14ba-277">notes</span><span class="sxs-lookup"><span data-stu-id="d14ba-277">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d14ba-278">enabled</span><span class="sxs-lookup"><span data-stu-id="d14ba-278">enabled</span></span> | <span data-ttu-id="d14ba-279">boolean</span><span class="sxs-lookup"><span data-stu-id="d14ba-279">boolean</span></span> | `true` | <span data-ttu-id="d14ba-280">このキーの設定により、WSL で Windows プロセスの起動をサポートするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-280">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="d14ba-281">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="d14ba-281">appendWindowsPath</span></span> | <span data-ttu-id="d14ba-282">boolean</span><span class="sxs-lookup"><span data-stu-id="d14ba-282">boolean</span></span> | `true` | <span data-ttu-id="d14ba-283">このキーの設定により、WSL が Windows パス要素を $PATH 環境変数に追加するかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="d14ba-283">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="d14ba-284">user</span><span class="sxs-lookup"><span data-stu-id="d14ba-284">user</span></span>

<span data-ttu-id="d14ba-285">セクションのラベル: `[user]`</span><span class="sxs-lookup"><span data-stu-id="d14ba-285">Section label: `[user]`</span></span>

<span data-ttu-id="d14ba-286">これらのオプションは、ビルド18980以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-286">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="d14ba-287">key</span><span class="sxs-lookup"><span data-stu-id="d14ba-287">key</span></span> | <span data-ttu-id="d14ba-288">value</span><span class="sxs-lookup"><span data-stu-id="d14ba-288">value</span></span> | <span data-ttu-id="d14ba-289">default</span><span class="sxs-lookup"><span data-stu-id="d14ba-289">default</span></span> | <span data-ttu-id="d14ba-290">notes</span><span class="sxs-lookup"><span data-stu-id="d14ba-290">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d14ba-291">default</span><span class="sxs-lookup"><span data-stu-id="d14ba-291">default</span></span> | <span data-ttu-id="d14ba-292">string</span><span class="sxs-lookup"><span data-stu-id="d14ba-292">string</span></span> | <span data-ttu-id="d14ba-293">最初の実行時に作成された最初のユーザー名</span><span class="sxs-lookup"><span data-stu-id="d14ba-293">The initial username created on first run</span></span> | <span data-ttu-id="d14ba-294">このキーを設定すると、最初に WSL セッションを開始したときに実行するユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-294">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="d14ba-295">Wslconfig を使用してグローバルオプションを構成する</span><span class="sxs-lookup"><span data-stu-id="d14ba-295">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="d14ba-296">**Windows ビルド19041以降で使用可能**</span><span class="sxs-lookup"><span data-stu-id="d14ba-296">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="d14ba-297">グローバル WSL オプションを構成するには、 `.wslconfig` ユーザーフォルダーのルートディレクトリにファイルを配置し `C:\Users\<yourUserName>\.wslconfig` ます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-297">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="d14ba-298">このファイルには、次のオプションを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-298">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="d14ba-299">WSL 2 の設定</span><span class="sxs-lookup"><span data-stu-id="d14ba-299">WSL 2 Settings</span></span>

<span data-ttu-id="d14ba-300">これらの設定は、WSL 2 ディストリビューションを電源にする VM に影響します。</span><span class="sxs-lookup"><span data-stu-id="d14ba-300">These settings affect the VM that powers any WSL 2 distribution.</span></span> 

| <span data-ttu-id="d14ba-301">key</span><span class="sxs-lookup"><span data-stu-id="d14ba-301">key</span></span> | <span data-ttu-id="d14ba-302">value</span><span class="sxs-lookup"><span data-stu-id="d14ba-302">value</span></span> | <span data-ttu-id="d14ba-303">default</span><span class="sxs-lookup"><span data-stu-id="d14ba-303">default</span></span> | <span data-ttu-id="d14ba-304">notes</span><span class="sxs-lookup"><span data-stu-id="d14ba-304">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d14ba-305">kernel</span><span class="sxs-lookup"><span data-stu-id="d14ba-305">kernel</span></span> | <span data-ttu-id="d14ba-306">string</span><span class="sxs-lookup"><span data-stu-id="d14ba-306">string</span></span> | <span data-ttu-id="d14ba-307">Microsoft が構築したカーネルの受信トレイ</span><span class="sxs-lookup"><span data-stu-id="d14ba-307">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="d14ba-308">カスタム Linux カーネルへの絶対 Windows パス。</span><span class="sxs-lookup"><span data-stu-id="d14ba-308">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="d14ba-309">memory</span><span class="sxs-lookup"><span data-stu-id="d14ba-309">memory</span></span> | <span data-ttu-id="d14ba-310">size</span><span class="sxs-lookup"><span data-stu-id="d14ba-310">size</span></span> | <span data-ttu-id="d14ba-311">Windows 上の合計メモリの80%</span><span class="sxs-lookup"><span data-stu-id="d14ba-311">80% of your total memory on Windows</span></span> | <span data-ttu-id="d14ba-312">WSL 2 VM に割り当てるメモリの量。</span><span class="sxs-lookup"><span data-stu-id="d14ba-312">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="d14ba-313">状況</span><span class="sxs-lookup"><span data-stu-id="d14ba-313">processors</span></span> | <span data-ttu-id="d14ba-314">number</span><span class="sxs-lookup"><span data-stu-id="d14ba-314">number</span></span> | <span data-ttu-id="d14ba-315">Windows 上の同じプロセッサ数</span><span class="sxs-lookup"><span data-stu-id="d14ba-315">The same number of processors on Windows</span></span> | <span data-ttu-id="d14ba-316">WSL 2 VM に割り当てるプロセッサの数。</span><span class="sxs-lookup"><span data-stu-id="d14ba-316">How many processors to assign ot the WSL 2 VM.</span></span> |
| <span data-ttu-id="d14ba-317">localhostForwarding</span><span class="sxs-lookup"><span data-stu-id="d14ba-317">localhostForwarding</span></span> | <span data-ttu-id="d14ba-318">boolean</span><span class="sxs-lookup"><span data-stu-id="d14ba-318">boolean</span></span> | `true` | <span data-ttu-id="d14ba-319">WSL 2 VM のワイルドカードまたは localhost にバインドされたポートが localhost: port を介してホストから接続可能である必要があるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="d14ba-319">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="d14ba-320">カーネルコマンドライン</span><span class="sxs-lookup"><span data-stu-id="d14ba-320">kernelCommandLine</span></span> | <span data-ttu-id="d14ba-321">string</span><span class="sxs-lookup"><span data-stu-id="d14ba-321">string</span></span> | <span data-ttu-id="d14ba-322">空白</span><span class="sxs-lookup"><span data-stu-id="d14ba-322">Blank</span></span> | <span data-ttu-id="d14ba-323">追加のカーネルコマンドライン引数。</span><span class="sxs-lookup"><span data-stu-id="d14ba-323">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="d14ba-324">swap</span><span class="sxs-lookup"><span data-stu-id="d14ba-324">swap</span></span> | <span data-ttu-id="d14ba-325">size</span><span class="sxs-lookup"><span data-stu-id="d14ba-325">size</span></span> | <span data-ttu-id="d14ba-326">Windows 上のメモリサイズの25% が最も近い GB に切り上げられます</span><span class="sxs-lookup"><span data-stu-id="d14ba-326">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="d14ba-327">WSL 2 VM に追加するスワップ領域の大きさ。スワップファイルがない場合は0です。</span><span class="sxs-lookup"><span data-stu-id="d14ba-327">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="d14ba-328">スワップ</span><span class="sxs-lookup"><span data-stu-id="d14ba-328">swapFile</span></span> | <span data-ttu-id="d14ba-329">size</span><span class="sxs-lookup"><span data-stu-id="d14ba-329">size</span></span> | <span data-ttu-id="d14ba-330">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span><span class="sxs-lookup"><span data-stu-id="d14ba-330">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="d14ba-331">スワップバーチャルハードディスクへの絶対 Windows パス。</span><span class="sxs-lookup"><span data-stu-id="d14ba-331">An absolute Windows path to the swap virtual hard disk.</span></span> |

<span data-ttu-id="d14ba-332">値がのエントリは `path` 、エスケープされた円記号を含む Windows パスである必要があります。次に例を示します。`C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="d14ba-332">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="d14ba-333">値を持つエントリは、 `size` サイズの後に単位 (やなど) が続く必要があり `8GB` `512MB` ます。</span><span class="sxs-lookup"><span data-stu-id="d14ba-333">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>