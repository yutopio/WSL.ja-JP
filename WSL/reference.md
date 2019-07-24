---
title: Linux 用 Windows サブシステムのコマンドリファレンス
description: Windows Subsystem for Linux を管理するコマンドの一覧
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307655"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="93824-104">Windows Subsystem for Linux のコマンドリファレンス</span><span class="sxs-lookup"><span data-stu-id="93824-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="93824-105">Windows Subsystem for Linux を操作する最良の方法は、 `wsl.exe`コマンドを使用することです。</span><span class="sxs-lookup"><span data-stu-id="93824-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="93824-106">Windows バージョン1903以降を使用して`wsl.exe`いる場合のすべてのオプションを含む一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="93824-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="93824-107">Linux バイナリを実行するための引数:</span><span class="sxs-lookup"><span data-stu-id="93824-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="93824-108">コマンドラインが指定されていない場合、既定のシェルが起動されます。</span><span class="sxs-lookup"><span data-stu-id="93824-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="93824-109">--exec、-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="93824-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="93824-110">既定の Linux シェルを使用せずに、指定したコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="93824-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="93824-111">残りのコマンドラインをそのまま渡します。</span><span class="sxs-lookup"><span data-stu-id="93824-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="93824-112">オプション:</span><span class="sxs-lookup"><span data-stu-id="93824-112">Options:</span></span>
    * <span data-ttu-id="93824-113">--distribution、-d<Distro></span><span class="sxs-lookup"><span data-stu-id="93824-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="93824-114">指定された分布を実行します。</span><span class="sxs-lookup"><span data-stu-id="93824-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="93824-115">--user、-u<UserName></span><span class="sxs-lookup"><span data-stu-id="93824-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="93824-116">指定されたユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="93824-116">Run as the specified user.</span></span>

* <span data-ttu-id="93824-117">Linux 用 Windows サブシステムを管理するための引数:</span><span class="sxs-lookup"><span data-stu-id="93824-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="93824-118">--export <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="93824-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="93824-119">配布を tar ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="93824-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="93824-120">ファイル名には、標準出力の場合はを指定できます。</span><span class="sxs-lookup"><span data-stu-id="93824-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="93824-121">--import <Distro> <InstallLocation>[Options <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="93824-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="93824-122">指定した tar ファイルを新しいディストリビューションとしてインポートします。</span><span class="sxs-lookup"><span data-stu-id="93824-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="93824-123">ファイル名には、標準入力の場合はを指定できます。</span><span class="sxs-lookup"><span data-stu-id="93824-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="93824-124">オプション:</span><span class="sxs-lookup"><span data-stu-id="93824-124">Options:</span></span>
            * <span data-ttu-id="93824-125">--version <Version>新しいディストリビューションに使用するバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="93824-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="93824-126">--list、-l [Options]</span><span class="sxs-lookup"><span data-stu-id="93824-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="93824-127">ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="93824-127">Lists distributions.</span></span>

        * <span data-ttu-id="93824-128">オプション:</span><span class="sxs-lookup"><span data-stu-id="93824-128">Options:</span></span>
            * <span data-ttu-id="93824-129">--すべて</span><span class="sxs-lookup"><span data-stu-id="93824-129">--all</span></span>
                * <span data-ttu-id="93824-130">現在インストール中またはアンインストール中のディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="93824-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="93824-131">--実行中</span><span class="sxs-lookup"><span data-stu-id="93824-131">--running</span></span>
                * <span data-ttu-id="93824-132">現在実行中のディストリビューションのみを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="93824-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="93824-133">--set-既定値、-s<Distro></span><span class="sxs-lookup"><span data-stu-id="93824-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="93824-134">ディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="93824-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="93824-135">--設定-既定-バージョン<Version></span><span class="sxs-lookup"><span data-stu-id="93824-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="93824-136">新しいディストリビューションの既定のインストールバージョンを変更します。</span><span class="sxs-lookup"><span data-stu-id="93824-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="93824-137">--set-バージョン<Distro><Version></span><span class="sxs-lookup"><span data-stu-id="93824-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="93824-138">指定された分布のバージョンを変更します。</span><span class="sxs-lookup"><span data-stu-id="93824-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="93824-139">--terminate、-t<Distro></span><span class="sxs-lookup"><span data-stu-id="93824-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="93824-140">指定された分布を終了します。</span><span class="sxs-lookup"><span data-stu-id="93824-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="93824-141">--登録解除<Distro></span><span class="sxs-lookup"><span data-stu-id="93824-141">--unregister <Distro></span></span>
        * <span data-ttu-id="93824-142">ディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="93824-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="93824-143">--help</span><span class="sxs-lookup"><span data-stu-id="93824-143">--help</span></span>
        * <span data-ttu-id="93824-144">使用状況に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="93824-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="93824-145">その他のコマンド</span><span class="sxs-lookup"><span data-stu-id="93824-145">Additional Commands</span></span>

<span data-ttu-id="93824-146">Windows Subsystem for Linux と対話するための履歴コマンドもあります。</span><span class="sxs-lookup"><span data-stu-id="93824-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="93824-147">これらの機能はに`wsl.exe`含まれていますが、引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="93824-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="93824-148">このコマンドでは、WSL 分布を構成できます。</span><span class="sxs-lookup"><span data-stu-id="93824-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="93824-149">そのオプションの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="93824-149">Below is a list of its options.</span></span>

* <span data-ttu-id="93824-150">/l、/list [オプション]</span><span class="sxs-lookup"><span data-stu-id="93824-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="93824-151">登録済みのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="93824-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="93824-152">/all-オプションで、現在インストール中またはアンインストール中のディストリビューションも含め、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="93824-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="93824-153">実行中-現在実行中のディストリビューションだけを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="93824-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="93824-154">/s、/setdefault<DistributionName></span><span class="sxs-lookup"><span data-stu-id="93824-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="93824-155">ディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="93824-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="93824-156">/t、/terminate<DistributionName></span><span class="sxs-lookup"><span data-stu-id="93824-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="93824-157">分布を終了します。</span><span class="sxs-lookup"><span data-stu-id="93824-157">Terminates the distribution.</span></span>

* <span data-ttu-id="93824-158">/u、/unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="93824-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="93824-159">ディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="93824-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="93824-160">このコマンドは、bash シェルを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93824-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="93824-161">このコマンドで使用できるオプションを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="93824-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="93824-162">オプションが指定されていません</span><span class="sxs-lookup"><span data-stu-id="93824-162">No Option given</span></span>
    * <span data-ttu-id="93824-163">現在のディレクトリで Bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="93824-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="93824-164">Bash シェルがインストールされていない場合は、自動的に実行されます。`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="93824-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="93824-165">bash ~</span><span class="sxs-lookup"><span data-stu-id="93824-165">bash ~</span></span>
    * <span data-ttu-id="93824-166">ユーザーのホームディレクトリに bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="93824-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="93824-167">の実行`cd ~`と同様です。</span><span class="sxs-lookup"><span data-stu-id="93824-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="93824-168">bash-c "&lt;command&gt;"</span><span class="sxs-lookup"><span data-stu-id="93824-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="93824-169">コマンドを実行し、出力を出力して、Windows のコマンドプロンプトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="93824-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="93824-170">よう`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="93824-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="93824-171">非推奨のコマンド</span><span class="sxs-lookup"><span data-stu-id="93824-171">Deprecated Commands</span></span>

<span data-ttu-id="93824-172">は`lxrun.exe` 、Windows Subsystem for Linux をインストールして管理するために使用される最初のコマンドでした。</span><span class="sxs-lookup"><span data-stu-id="93824-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="93824-173">Windows 10 1803 以降では非推奨とされます。</span><span class="sxs-lookup"><span data-stu-id="93824-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="93824-174">コマンド`lxrun.exe`を使用して、 [Windows Subsystem for Linux (wsl)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)と直接やり取りできます。</span><span class="sxs-lookup"><span data-stu-id="93824-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="93824-175">これらのコマンドは`\Windows\System32`ディレクトリにインストールされ、Windows コマンドプロンプトまたは PowerShell 内で実行できます。</span><span class="sxs-lookup"><span data-stu-id="93824-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="93824-176">Command</span><span class="sxs-lookup"><span data-stu-id="93824-176">Command</span></span>                     | <span data-ttu-id="93824-177">説明</span><span class="sxs-lookup"><span data-stu-id="93824-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="93824-178">Lxrun コマンドは、WSL インスタンスを管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93824-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="93824-179">ダウンロードとインストールのプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="93824-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="93824-180">すべてのプロンプトをバイパスするには、 **/y**を追加します。</span><span class="sxs-lookup"><span data-stu-id="93824-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="93824-181">確認プロンプトが自動的に受け入れられ、既定のユーザーは root に設定されます。</span><span class="sxs-lookup"><span data-stu-id="93824-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="93824-182">Ubuntu イメージをアンインストールおよび削除します。</span><span class="sxs-lookup"><span data-stu-id="93824-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="93824-183">既定では、ユーザーの Ubuntu ホームディレクトリは削除されません。</span><span class="sxs-lookup"><span data-stu-id="93824-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="93824-184">**/y**を追加して確認プロンプトを自動的に受け入れることができます</span><span class="sxs-lookup"><span data-stu-id="93824-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="93824-185">のユーザーの Ubuntu ホームディレクトリ**をアンインストールおよび**削除します。</span><span class="sxs-lookup"><span data-stu-id="93824-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="93824-186">Ubuntu ユーザーの既定の Bash を設定します。</span><span class="sxs-lookup"><span data-stu-id="93824-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="93824-187">指定されたユーザーが存在しない場合は、パスワードの入力を求められます。</span><span class="sxs-lookup"><span data-stu-id="93824-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="93824-188">詳細については https://aka.ms/wslusers 、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93824-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="93824-189">**/y**パスワードの promping をバイパスします。</span><span class="sxs-lookup"><span data-stu-id="93824-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="93824-190">ユーザーはパスワードなしで作成されます。</span><span class="sxs-lookup"><span data-stu-id="93824-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="93824-191">サブシステムのパッケージインデックスを更新します</span><span class="sxs-lookup"><span data-stu-id="93824-191">Updates the subsystem's package index</span></span>          |
