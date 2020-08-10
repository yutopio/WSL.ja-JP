---
title: Linux ディストリビューションの管理
description: Windows Subsystem for Linux で実行されている複数の Linux ディストリビューションの一覧表示と構成に関するリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: b8aa740233f3ac9517744212eb7b362a18378822
ms.sourcegitcommit: 90577817a9321949da2a3971b4c78bb00f6d977f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/10/2020
ms.locfileid: "88039415"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="012a8-104">WSL コマンドと起動構成</span><span class="sxs-lookup"><span data-stu-id="012a8-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="012a8-105">WSL を実行する方法</span><span class="sxs-lookup"><span data-stu-id="012a8-105">Ways to run WSL</span></span>

<span data-ttu-id="012a8-106">WSL を[インストール](install-win10.md)した Linux ディストリビューションを実行するには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="012a8-107">Windows の [スタート] メニューにアクセスし、インストールされているディストリビューションの名前を入力して、Linux ディストリビューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="012a8-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="012a8-108">たとえば、"Ubuntu" のようになります。</span><span class="sxs-lookup"><span data-stu-id="012a8-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="012a8-109">Windows のコマンドプロンプトまたは PowerShell から、インストールされている配布の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="012a8-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="012a8-110">例: `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="012a8-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="012a8-111">Windows コマンドプロンプトまたは PowerShell から、現在のコマンドライン内で既定の Linux ディストリビューションを開くには、「」と入力し `wsl.exe` ます。</span><span class="sxs-lookup"><span data-stu-id="012a8-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="012a8-112">Windows コマンドプロンプトまたは PowerShell から、現在のコマンドライン内で既定の Linux ディストリビューションを開くには、「」と入力し `wsl [command]` ます。</span><span class="sxs-lookup"><span data-stu-id="012a8-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="012a8-113">どの方法を使用すべきかは、作業内容によって異なります。</span><span class="sxs-lookup"><span data-stu-id="012a8-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="012a8-114">Windows プロンプトまたは PowerShell ウィンドウ内で WSL コマンドラインを開いて終了する場合は、コマンドを入力します `exit` 。</span><span class="sxs-lookup"><span data-stu-id="012a8-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="012a8-115">ディストリビューションによって WSL を起動する</span><span class="sxs-lookup"><span data-stu-id="012a8-115">Launch WSL by distribution</span></span>

<span data-ttu-id="012a8-116">ディストリビューション固有のアプリケーションを使用してディストリビューションを実行すると、そのディストリビューションが独自のコンソール ウィンドウで起動します。</span><span class="sxs-lookup"><span data-stu-id="012a8-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![[スタート] メニューからの WSL の起動](media/start-launch.png)

<span data-ttu-id="012a8-118">これは、Microsoft Store で [起動] をクリックすることと同じです。</span><span class="sxs-lookup"><span data-stu-id="012a8-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Microsoft Store からの WSL の起動](media/store-launch.png)

<span data-ttu-id="012a8-120">`[distribution].exe` を実行して、コマンド ラインからディストリビューションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="012a8-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="012a8-121">この方法でコマンド ラインからディストリビューションを実行すると、作業ディレクトリが現在のディレクトリからディストリビューションのホーム ディレクトリに自動的に変更されるという欠点があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="012a8-122">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="012a8-122">**Example: (using PowerShell)**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="012a8-123">wsl および wsl [コマンド]</span><span class="sxs-lookup"><span data-stu-id="012a8-123">wsl and wsl [command]</span></span>

<span data-ttu-id="012a8-124">コマンド ラインから WSL を実行する最善の方法は、`wsl.exe` を使用することです。</span><span class="sxs-lookup"><span data-stu-id="012a8-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="012a8-125">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="012a8-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="012a8-126">`wsl` は、現在の作業ディレクトリを適切に維持するだけでなく、1 つのコマンドを Windows コマンドとともに実行できます。</span><span class="sxs-lookup"><span data-stu-id="012a8-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="012a8-127">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="012a8-127">**Example: (using PowerShell)**</span></span>

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

<span data-ttu-id="012a8-128">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="012a8-128">**Example: (using PowerShell)**</span></span>

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

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="012a8-129">複数の Linux ディストリビューションの管理</span><span class="sxs-lookup"><span data-stu-id="012a8-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="012a8-130">Windows 10 バージョン 1903[以降](ms-settings:windowsupdate)では、を使用して `wsl.exe` Windows Subsystem for Linux (wsl) でのディストリビューションを管理できます。これには、使用可能なディストリビューションの一覧表示、既定の配布の設定、およびディストリビューションのアンインストールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="012a8-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="012a8-131">各 Linux ディストリビューションは、個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="012a8-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="012a8-132">ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="012a8-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="012a8-133">たとえば、「 `ubuntu /?` 」のように指定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="012a8-134">ディストリビューションの一覧表示</span><span class="sxs-lookup"><span data-stu-id="012a8-134">List distributions</span></span>

<span data-ttu-id="012a8-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="012a8-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="012a8-136">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="012a8-137">一覧表示されているディストリビューションは、インストールされており、使用できる状態です。</span><span class="sxs-lookup"><span data-stu-id="012a8-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="012a8-138">`wsl --list --all`現在使用できないすべてのディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="012a8-139">インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="012a8-140">`wsl --list --running`現在実行中のすべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="012a8-141">既定のディストリビューションの設定</span><span class="sxs-lookup"><span data-stu-id="012a8-141">Set a default distribution</span></span>

<span data-ttu-id="012a8-142">既定の WSL ディストリビューションは、コマンド ラインで `wsl` を実行するときに実行されるものです。</span><span class="sxs-lookup"><span data-stu-id="012a8-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="012a8-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="012a8-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="012a8-144">既定のディストリビューションを `<DistributionName>` に設定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="012a8-145">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="012a8-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="012a8-146">`wsl -s Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="012a8-147">これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="012a8-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="012a8-148">`wsl` を実行すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="012a8-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="012a8-149">ディストリビューションの登録解除と再インストール</span><span class="sxs-lookup"><span data-stu-id="012a8-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="012a8-150">Linux ディストリビューションは Microsoft Store を介してインストールできますが、そのストアを介してアンインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="012a8-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="012a8-151">WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="012a8-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="012a8-152">登録を解除すると、ディストリビューションを再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="012a8-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="012a8-153">**注意:** 登録が解除されると、その配布に関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。</span><span class="sxs-lookup"><span data-stu-id="012a8-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="012a8-154">ストアから再インストールすると、ディストリビューションのクリーン コピーがインストールされます。</span><span class="sxs-lookup"><span data-stu-id="012a8-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="012a8-155">ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="012a8-156">たとえば、`wsl --unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="012a8-157">`wsl --list` を実行すると、それは一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="012a8-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="012a8-158">再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="012a8-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="012a8-159">特定のユーザーとしての実行</span><span class="sxs-lookup"><span data-stu-id="012a8-159">Run as a specific user</span></span>

<span data-ttu-id="012a8-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="012a8-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="012a8-161">指定されたユーザーとして WSL を実行します。</span><span class="sxs-lookup"><span data-stu-id="012a8-161">Run WSL as the specified user.</span></span> <span data-ttu-id="012a8-162">ユーザーは WSL ディストリビューション内に存在する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="012a8-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="change-the-default-user-for-a-distribution"></a><span data-ttu-id="012a8-163">配布の既定のユーザーを変更する</span><span class="sxs-lookup"><span data-stu-id="012a8-163">Change the default user for a distribution</span></span>

`<DistributionName> config --default-user <Username>`

<span data-ttu-id="012a8-164">ディストリビューションログインの既定のユーザーを変更します。</span><span class="sxs-lookup"><span data-stu-id="012a8-164">Change the default user that for your distribution log-in.</span></span> <span data-ttu-id="012a8-165">既定のユーザーになるには、ユーザーが既にディストリビューション内に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-165">The user has to already exist inside the distribution in order to become the default user.</span></span> 

<span data-ttu-id="012a8-166">たとえば、 `ubuntu config --default-user johndoe` Ubuntu ディストリビューションの既定のユーザーを "johndoe" ユーザーに変更します。</span><span class="sxs-lookup"><span data-stu-id="012a8-166">For example: `ubuntu config --default-user johndoe` would change the default user for the Ubuntu distribution to the "johndoe" user.</span></span>

> [!NOTE]
> <span data-ttu-id="012a8-167">配布の名前を確認できない場合は、コマンドの [[ディストリビューションの一覧](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions)] を参照して、インストールされているディストリビューションの正式な名前を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-167">If you are having trouble figuring out the name of your distribution, see [List distributions](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) for the command to list the official name of the installed distributions.</span></span> 

## <a name="run-a-specific-distribution"></a><span data-ttu-id="012a8-168">特定のディストリビューションの実行</span><span class="sxs-lookup"><span data-stu-id="012a8-168">Run a specific distribution</span></span>

<span data-ttu-id="012a8-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="012a8-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="012a8-170">WSL の指定したディストリビューションの実行は、既定値を変更する必要なしに、特定のディストリビューションにコマンドを送信するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="012a8-170">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="012a8-171">以前のバージョンの Windows での複数の Linux ディストリビューションの管理</span><span class="sxs-lookup"><span data-stu-id="012a8-171">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="012a8-172">バージョン1903より前の Windows 10 では、WSL Config ( `wslconfig.exe` ) コマンドラインツールを使用して、Windows Subsystem For linux (wsl) で実行されている linux ディストリビューションを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-172">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="012a8-173">これにより、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="012a8-173">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="012a8-174">WSL Config はディストリビューションにまたがる設定やそれらを調整する設定に役立ちますが、各 Linux ディストリビューションは個別に独自の構成を管理します。</span><span class="sxs-lookup"><span data-stu-id="012a8-174">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="012a8-175">ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="012a8-175">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="012a8-176">たとえば、「 `ubuntu /?` 」のように指定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-176">For example `ubuntu /?`.</span></span>

<span data-ttu-id="012a8-177">wslconfig で使用可能なオプションをすべて表示するには、`wslconfig /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="012a8-177">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

<span data-ttu-id="012a8-178">ディストリビューションを一覧表示するには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="012a8-178">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="012a8-179">WSL で利用可能な Linux ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-179">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="012a8-180">一覧表示されているディストリビューションは、インストールされており、使用できる状態です。</span><span class="sxs-lookup"><span data-stu-id="012a8-180">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="012a8-181">現在使用できないディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-181">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="012a8-182">インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-182">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="012a8-183">コマンドラインでを実行したときに実行される既定のディストリビューションを設定するには、次のようにし `wsl` ます。</span><span class="sxs-lookup"><span data-stu-id="012a8-183">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="012a8-184">`wslconfig /setdefault <DistributionName>`既定の分布をに設定 `<DistributionName>` します。</span><span class="sxs-lookup"><span data-stu-id="012a8-184">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="012a8-185">**例: (PowerShell を使用)**</span><span class="sxs-lookup"><span data-stu-id="012a8-185">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="012a8-186">`wslconfig /setdefault Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-186">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="012a8-187">これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。</span><span class="sxs-lookup"><span data-stu-id="012a8-187">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="012a8-188">`wsl` を実行すると、Ubuntu セッションが開きます。</span><span class="sxs-lookup"><span data-stu-id="012a8-188">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="012a8-189">配布を登録解除して再インストールするには:</span><span class="sxs-lookup"><span data-stu-id="012a8-189">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="012a8-190">ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="012a8-191">たとえば、`wslconfig /unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="012a8-192">`wslconfig /list` を実行すると、それは一覧に表示されません。</span><span class="sxs-lookup"><span data-stu-id="012a8-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="012a8-193">再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="012a8-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="012a8-194">ディストリビューションごとの起動設定を wslconf で構成する</span><span class="sxs-lookup"><span data-stu-id="012a8-194">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="012a8-195">**Windows ビルド17093以降で使用可能**</span><span class="sxs-lookup"><span data-stu-id="012a8-195">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="012a8-196">`wsl.conf` を使用して、サブシステムを起動するたびに適用される、WSL の特定の機能を自動的に構成します。</span><span class="sxs-lookup"><span data-stu-id="012a8-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="012a8-197">現時点では、これには自動マウント オプションとネットワーク構成が含まれています。</span><span class="sxs-lookup"><span data-stu-id="012a8-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="012a8-198">`wsl.conf` は、`/etc/wsl.conf` 内の各 Linux ディストリビューションにあります。</span><span class="sxs-lookup"><span data-stu-id="012a8-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="012a8-199">そのファイルがそこになければ、自分で作成できます。</span><span class="sxs-lookup"><span data-stu-id="012a8-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="012a8-200">WSL は、ファイルの存在を検出し、その内容を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="012a8-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="012a8-201">ファイルが見つからないか、形式が正しくない (つまり、不適切なマークアップ形式である) 場合、WSL は通常どおりに起動を続けます。</span><span class="sxs-lookup"><span data-stu-id="012a8-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="012a8-202">`wsl.conf`ディストリビューションに追加できるサンプルファイルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-202">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="012a8-203">構成オプション</span><span class="sxs-lookup"><span data-stu-id="012a8-203">Configuration Options</span></span>

<span data-ttu-id="012a8-204">.ini 規則に従って、キーはセクションの下で宣言されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="012a8-205">WSL では、`automount` と `network` の 2 つのセクションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="012a8-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="012a8-206">automount</span><span class="sxs-lookup"><span data-stu-id="012a8-206">automount</span></span>

<span data-ttu-id="012a8-207">セクション: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="012a8-207">Section: `[automount]`</span></span>

| <span data-ttu-id="012a8-208">key</span><span class="sxs-lookup"><span data-stu-id="012a8-208">key</span></span>        | <span data-ttu-id="012a8-209">value</span><span class="sxs-lookup"><span data-stu-id="012a8-209">value</span></span>                          | <span data-ttu-id="012a8-210">既定</span><span class="sxs-lookup"><span data-stu-id="012a8-210">default</span></span>      | <span data-ttu-id="012a8-211">注</span><span class="sxs-lookup"><span data-stu-id="012a8-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="012a8-212">enabled</span><span class="sxs-lookup"><span data-stu-id="012a8-212">enabled</span></span>    | <span data-ttu-id="012a8-213">boolean</span><span class="sxs-lookup"><span data-stu-id="012a8-213">boolean</span></span>                        | <span data-ttu-id="012a8-214">true</span><span class="sxs-lookup"><span data-stu-id="012a8-214">true</span></span>         | <span data-ttu-id="012a8-215">`true` にすると、固定ドライブ (つまり、</span><span class="sxs-lookup"><span data-stu-id="012a8-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="012a8-216">`C:/` または`D:/`) は `/mnt` の下に DrvFs で自動的にマウントされます。</span><span class="sxs-lookup"><span data-stu-id="012a8-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="012a8-217">`false`ドライブは自動的にマウントされませんが、手動またはを使用してマウントすることもでき `fstab` ます。</span><span class="sxs-lookup"><span data-stu-id="012a8-217">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="012a8-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="012a8-218">mountFsTab</span></span> | <span data-ttu-id="012a8-219">boolean</span><span class="sxs-lookup"><span data-stu-id="012a8-219">boolean</span></span>                        | <span data-ttu-id="012a8-220">true</span><span class="sxs-lookup"><span data-stu-id="012a8-220">true</span></span>         | <span data-ttu-id="012a8-221">`true` にすると、WSL 開始時に処理されるように `/etc/fstab` を設定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="012a8-222">/etc/fstab は、SMB 共有などの他のファイル システムを宣言できるファイルです。</span><span class="sxs-lookup"><span data-stu-id="012a8-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="012a8-223">そのため、起動時にこれらのファイル システムを WSL 内で自動的にマウントできます。</span><span class="sxs-lookup"><span data-stu-id="012a8-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="012a8-224">root</span><span class="sxs-lookup"><span data-stu-id="012a8-224">root</span></span>       | <span data-ttu-id="012a8-225">String</span><span class="sxs-lookup"><span data-stu-id="012a8-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="012a8-226">固定ドライブが自動的にマウントされるディレクトリを設定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="012a8-227">たとえば、`/windir/` に WSL のディレクトリがあり、それをルートとして指定すると、固定ドライブは `/windir/c` でマウントされることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="012a8-228">オプション</span><span class="sxs-lookup"><span data-stu-id="012a8-228">options</span></span>    | <span data-ttu-id="012a8-229">値のコンマ区切りのリスト</span><span class="sxs-lookup"><span data-stu-id="012a8-229">comma-separated list of values</span></span> | <span data-ttu-id="012a8-230">空の文字列</span><span class="sxs-lookup"><span data-stu-id="012a8-230">empty string</span></span> | <span data-ttu-id="012a8-231">この値は、既定の DrvFs マウント オプション文字列に追加されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="012a8-232">**DrvFs 固有のオプションのみを指定できます。**</span><span class="sxs-lookup"><span data-stu-id="012a8-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="012a8-233">マウント バイナリが通常、フラグに解析するオプションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="012a8-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="012a8-234">これらのオプションを明示的に指定する場合は、それを行う対象のドライブすべてを /etc/fstab に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="012a8-235">既定では、WSL は uid と gid を既定のユーザーの値に設定します (Ubuntu ディストリビューションでは、既定のユーザーは uid = 1000、gid = 1000 で作成されます)。</span><span class="sxs-lookup"><span data-stu-id="012a8-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="012a8-236">ユーザーがこのキーを使用して gid または uid オプションを明示的に指定した場合、関連する値は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="012a8-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="012a8-237">それ以外の場合は、既定値が常に追加されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="012a8-238">**注:** これらのオプションは、自動的にマウントされたドライブすべてのマウント オプションとして適用されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="012a8-239">特定のドライブのみのオプションを変更するには、代わりに /etc/fstab を使用します。</span><span class="sxs-lookup"><span data-stu-id="012a8-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="012a8-240">マウント オプション</span><span class="sxs-lookup"><span data-stu-id="012a8-240">Mount options</span></span>

<span data-ttu-id="012a8-241">Windows ドライブ (DrvFs) にさまざまなマウント オプションを設定すると、Windows ファイルのファイルのアクセス許可を計算する方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="012a8-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="012a8-242">次のオプションが使用できます。</span><span class="sxs-lookup"><span data-stu-id="012a8-242">The following options are available:</span></span>

| <span data-ttu-id="012a8-243">キー</span><span class="sxs-lookup"><span data-stu-id="012a8-243">Key</span></span> | <span data-ttu-id="012a8-244">説明</span><span class="sxs-lookup"><span data-stu-id="012a8-244">Description</span></span> | <span data-ttu-id="012a8-245">既定</span><span class="sxs-lookup"><span data-stu-id="012a8-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="012a8-246">uid</span><span class="sxs-lookup"><span data-stu-id="012a8-246">uid</span></span>| <span data-ttu-id="012a8-247">すべてのファイルの所有者に使用するユーザー ID</span><span class="sxs-lookup"><span data-stu-id="012a8-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="012a8-248">WSL ディストリビューションの既定のユーザー ID (初回インストールの場合、既定値は 1000)</span><span class="sxs-lookup"><span data-stu-id="012a8-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="012a8-249">gid</span><span class="sxs-lookup"><span data-stu-id="012a8-249">gid</span></span>| <span data-ttu-id="012a8-250">すべてのファイルの所有者に使用するグループ ID</span><span class="sxs-lookup"><span data-stu-id="012a8-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="012a8-251">WSL ディストリビューションの既定のグループ ID (初回インストールの場合、既定値は 1000)</span><span class="sxs-lookup"><span data-stu-id="012a8-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="012a8-252">umask</span><span class="sxs-lookup"><span data-stu-id="012a8-252">umask</span></span> | <span data-ttu-id="012a8-253">すべてのファイルとディレクトリに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="012a8-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="012a8-254">000</span><span class="sxs-lookup"><span data-stu-id="012a8-254">000</span></span>
|<span data-ttu-id="012a8-255">fmask</span><span class="sxs-lookup"><span data-stu-id="012a8-255">fmask</span></span> | <span data-ttu-id="012a8-256">すべてのファイルに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="012a8-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="012a8-257">000</span><span class="sxs-lookup"><span data-stu-id="012a8-257">000</span></span>
|<span data-ttu-id="012a8-258">dmask</span><span class="sxs-lookup"><span data-stu-id="012a8-258">dmask</span></span> | <span data-ttu-id="012a8-259">すべてのディレクトリに対して除外するアクセス許可の 8 進数のマスク</span><span class="sxs-lookup"><span data-stu-id="012a8-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="012a8-260">000</span><span class="sxs-lookup"><span data-stu-id="012a8-260">000</span></span>

<span data-ttu-id="012a8-261">**注:** アクセス許可のマスクは、ファイルまたはディレクトリに適用される前に論理 OR 演算によって配置されます。</span><span class="sxs-lookup"><span data-stu-id="012a8-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="012a8-262">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="012a8-262">network</span></span>

<span data-ttu-id="012a8-263">セクションのラベル: `[network]`</span><span class="sxs-lookup"><span data-stu-id="012a8-263">Section label: `[network]`</span></span>

| <span data-ttu-id="012a8-264">key</span><span class="sxs-lookup"><span data-stu-id="012a8-264">key</span></span> | <span data-ttu-id="012a8-265">value</span><span class="sxs-lookup"><span data-stu-id="012a8-265">value</span></span> | <span data-ttu-id="012a8-266">既定</span><span class="sxs-lookup"><span data-stu-id="012a8-266">default</span></span> | <span data-ttu-id="012a8-267">注</span><span class="sxs-lookup"><span data-stu-id="012a8-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="012a8-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="012a8-268">generateHosts</span></span> | <span data-ttu-id="012a8-269">boolean</span><span class="sxs-lookup"><span data-stu-id="012a8-269">boolean</span></span> | `true` | <span data-ttu-id="012a8-270">`true` にすると、`/etc/hosts` を生成するように WSL を設定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="012a8-271">`hosts` ファイルには、IP アドレスに対応するホスト名の静的マップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="012a8-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="012a8-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="012a8-272">generateResolvConf</span></span> | <span data-ttu-id="012a8-273">boolean</span><span class="sxs-lookup"><span data-stu-id="012a8-273">boolean</span></span> | `true` | <span data-ttu-id="012a8-274">`true` にすると、`/etc/resolv.conf` を生成するように WSL を設定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="012a8-275">`resolv.conf` には、指定されたホスト名をその IP アドレスに解決できる DNS リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="012a8-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="012a8-276">interop</span><span class="sxs-lookup"><span data-stu-id="012a8-276">interop</span></span>

<span data-ttu-id="012a8-277">セクションのラベル: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="012a8-277">Section label: `[interop]`</span></span>

<span data-ttu-id="012a8-278">次のオプションは、Insider Build 17713 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="012a8-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="012a8-279">key</span><span class="sxs-lookup"><span data-stu-id="012a8-279">key</span></span> | <span data-ttu-id="012a8-280">value</span><span class="sxs-lookup"><span data-stu-id="012a8-280">value</span></span> | <span data-ttu-id="012a8-281">既定</span><span class="sxs-lookup"><span data-stu-id="012a8-281">default</span></span> | <span data-ttu-id="012a8-282">注</span><span class="sxs-lookup"><span data-stu-id="012a8-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="012a8-283">enabled</span><span class="sxs-lookup"><span data-stu-id="012a8-283">enabled</span></span> | <span data-ttu-id="012a8-284">boolean</span><span class="sxs-lookup"><span data-stu-id="012a8-284">boolean</span></span> | `true` | <span data-ttu-id="012a8-285">このキーの設定により、WSL で Windows プロセスの起動をサポートするかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="012a8-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="012a8-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="012a8-286">appendWindowsPath</span></span> | <span data-ttu-id="012a8-287">boolean</span><span class="sxs-lookup"><span data-stu-id="012a8-287">boolean</span></span> | `true` | <span data-ttu-id="012a8-288">このキーの設定により、WSL が Windows パス要素を $PATH 環境変数に追加するかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="012a8-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="012a8-289">user</span><span class="sxs-lookup"><span data-stu-id="012a8-289">user</span></span>

<span data-ttu-id="012a8-290">セクションのラベル: `[user]`</span><span class="sxs-lookup"><span data-stu-id="012a8-290">Section label: `[user]`</span></span>

<span data-ttu-id="012a8-291">これらのオプションは、ビルド18980以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="012a8-291">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="012a8-292">key</span><span class="sxs-lookup"><span data-stu-id="012a8-292">key</span></span> | <span data-ttu-id="012a8-293">value</span><span class="sxs-lookup"><span data-stu-id="012a8-293">value</span></span> | <span data-ttu-id="012a8-294">default</span><span class="sxs-lookup"><span data-stu-id="012a8-294">default</span></span> | <span data-ttu-id="012a8-295">notes</span><span class="sxs-lookup"><span data-stu-id="012a8-295">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="012a8-296">default</span><span class="sxs-lookup"><span data-stu-id="012a8-296">default</span></span> | <span data-ttu-id="012a8-297">string</span><span class="sxs-lookup"><span data-stu-id="012a8-297">string</span></span> | <span data-ttu-id="012a8-298">最初の実行時に作成された最初のユーザー名</span><span class="sxs-lookup"><span data-stu-id="012a8-298">The initial username created on first run</span></span> | <span data-ttu-id="012a8-299">このキーを設定すると、最初に WSL セッションを開始したときに実行するユーザーを指定します。</span><span class="sxs-lookup"><span data-stu-id="012a8-299">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="012a8-300">Wslconfig を使用してグローバルオプションを構成する</span><span class="sxs-lookup"><span data-stu-id="012a8-300">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="012a8-301">**Windows ビルド19041以降で使用可能**</span><span class="sxs-lookup"><span data-stu-id="012a8-301">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="012a8-302">グローバル WSL オプションを構成するには、 `.wslconfig` ユーザーフォルダーのルートディレクトリにファイルを配置し `C:\Users\<yourUserName>\.wslconfig` ます。</span><span class="sxs-lookup"><span data-stu-id="012a8-302">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="012a8-303">これらのファイルの多くは WSL 2 に関連しています。そのため、 `wsl --shutdown` wsl 2 VM をシャットダウンしてから wsl インスタンスを再起動して変更を反映するために、を実行することが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-303">Many of these files are related to WSL 2, please keep in mind you may need to run `wsl --shutdown` to shut down the WSL 2 VM and then restart your WSL instance for these changes to take affect.</span></span>

<span data-ttu-id="012a8-304">サンプルの wslconfig ファイルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="012a8-304">Here is a sample .wslconfig file:</span></span>

```console
[wsl2]
kernel=C:\\temp\\myCustomKernel
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
```

<span data-ttu-id="012a8-305">このファイルには、次のオプションを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="012a8-305">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="012a8-306">WSL 2 の設定</span><span class="sxs-lookup"><span data-stu-id="012a8-306">WSL 2 Settings</span></span>

<span data-ttu-id="012a8-307">セクションのラベル: `[wsl2]`</span><span class="sxs-lookup"><span data-stu-id="012a8-307">Section label: `[wsl2]`</span></span>

<span data-ttu-id="012a8-308">これらの設定は、WSL 2 ディストリビューションを電源にする VM に影響します。</span><span class="sxs-lookup"><span data-stu-id="012a8-308">These settings affect the VM that powers any WSL 2 distribution.</span></span>

| <span data-ttu-id="012a8-309">key</span><span class="sxs-lookup"><span data-stu-id="012a8-309">key</span></span> | <span data-ttu-id="012a8-310">value</span><span class="sxs-lookup"><span data-stu-id="012a8-310">value</span></span> | <span data-ttu-id="012a8-311">default</span><span class="sxs-lookup"><span data-stu-id="012a8-311">default</span></span> | <span data-ttu-id="012a8-312">notes</span><span class="sxs-lookup"><span data-stu-id="012a8-312">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="012a8-313">kernel</span><span class="sxs-lookup"><span data-stu-id="012a8-313">kernel</span></span> | <span data-ttu-id="012a8-314">string</span><span class="sxs-lookup"><span data-stu-id="012a8-314">string</span></span> | <span data-ttu-id="012a8-315">Microsoft が構築したカーネルの受信トレイ</span><span class="sxs-lookup"><span data-stu-id="012a8-315">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="012a8-316">カスタム Linux カーネルへの絶対 Windows パス。</span><span class="sxs-lookup"><span data-stu-id="012a8-316">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="012a8-317">メモリ</span><span class="sxs-lookup"><span data-stu-id="012a8-317">memory</span></span> | <span data-ttu-id="012a8-318">size</span><span class="sxs-lookup"><span data-stu-id="012a8-318">size</span></span> | <span data-ttu-id="012a8-319">Windows 上の合計メモリの 80% \*</span><span class="sxs-lookup"><span data-stu-id="012a8-319">80% of your total memory on Windows \*</span></span> | <span data-ttu-id="012a8-320">WSL 2 VM に割り当てるメモリの量。</span><span class="sxs-lookup"><span data-stu-id="012a8-320">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="012a8-321">状況</span><span class="sxs-lookup"><span data-stu-id="012a8-321">processors</span></span> | <span data-ttu-id="012a8-322">number</span><span class="sxs-lookup"><span data-stu-id="012a8-322">number</span></span> | <span data-ttu-id="012a8-323">Windows 上の同じプロセッサ数</span><span class="sxs-lookup"><span data-stu-id="012a8-323">The same number of processors on Windows</span></span> | <span data-ttu-id="012a8-324">WSL 2 VM に割り当てるプロセッサの数。</span><span class="sxs-lookup"><span data-stu-id="012a8-324">How many processors to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="012a8-325">localhostForwarding</span><span class="sxs-lookup"><span data-stu-id="012a8-325">localhostForwarding</span></span> | <span data-ttu-id="012a8-326">boolean</span><span class="sxs-lookup"><span data-stu-id="012a8-326">boolean</span></span> | `true` | <span data-ttu-id="012a8-327">WSL 2 VM のワイルドカードまたは localhost にバインドされたポートが localhost: port を介してホストから接続可能である必要があるかどうかを指定するブール値。</span><span class="sxs-lookup"><span data-stu-id="012a8-327">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="012a8-328">カーネルコマンドライン</span><span class="sxs-lookup"><span data-stu-id="012a8-328">kernelCommandLine</span></span> | <span data-ttu-id="012a8-329">string</span><span class="sxs-lookup"><span data-stu-id="012a8-329">string</span></span> | <span data-ttu-id="012a8-330">新規</span><span class="sxs-lookup"><span data-stu-id="012a8-330">Blank</span></span> | <span data-ttu-id="012a8-331">追加のカーネルコマンドライン引数。</span><span class="sxs-lookup"><span data-stu-id="012a8-331">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="012a8-332">swap</span><span class="sxs-lookup"><span data-stu-id="012a8-332">swap</span></span> | <span data-ttu-id="012a8-333">size</span><span class="sxs-lookup"><span data-stu-id="012a8-333">size</span></span> | <span data-ttu-id="012a8-334">Windows 上のメモリサイズの25% が最も近い GB に切り上げられます</span><span class="sxs-lookup"><span data-stu-id="012a8-334">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="012a8-335">WSL 2 VM に追加するスワップ領域の大きさ。スワップファイルがない場合は0です。</span><span class="sxs-lookup"><span data-stu-id="012a8-335">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="012a8-336">スワップ</span><span class="sxs-lookup"><span data-stu-id="012a8-336">swapFile</span></span> | <span data-ttu-id="012a8-337">string</span><span class="sxs-lookup"><span data-stu-id="012a8-337">string</span></span> | <span data-ttu-id="012a8-338">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span><span class="sxs-lookup"><span data-stu-id="012a8-338">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="012a8-339">スワップバーチャルハードディスクへの絶対 Windows パス。</span><span class="sxs-lookup"><span data-stu-id="012a8-339">An absolute Windows path to the swap virtual hard disk.</span></span> |

* <span data-ttu-id="012a8-340">メモ: この値は Windows ビルド19041では true であり、Insider プログラムの Windows ビルドでは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="012a8-340">Note: This value is true for Windows Build 19041 and may be different in Windows builds in the Insiders program</span></span>

<span data-ttu-id="012a8-341">値がのエントリは `path` 、エスケープされた円記号を含む Windows パスである必要があります。次に例を示します。`C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="012a8-341">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="012a8-342">値を持つエントリは、 `size` サイズの後に単位 (やなど) が続く必要があり `8GB` `512MB` ます。</span><span class="sxs-lookup"><span data-stu-id="012a8-342">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>
