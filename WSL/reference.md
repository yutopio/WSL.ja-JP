---
title: Windows Subsystem for Linux のコマンド リファレンス
description: Windows Subsystem for Linux を管理するコマンドの一覧
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: edd4b8216a25f519e36b8b99b626b0a4315f6039
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122742"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="8beeb-104">Windows Subsystem for Linux のコマンド リファレンス</span><span class="sxs-lookup"><span data-stu-id="8beeb-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="8beeb-105">Windows Subsystem for Linux を操作する最良の方法は、`wsl.exe` コマンドを使用することです。</span><span class="sxs-lookup"><span data-stu-id="8beeb-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="8beeb-106">Windows バージョン 1903 以降で `wsl.exe` を使用する場合のすべてのオプションを含む一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="8beeb-107">使用法: `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="8beeb-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="8beeb-108">Linux バイナリを実行するための引数</span><span class="sxs-lookup"><span data-stu-id="8beeb-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="8beeb-109">**引数なし**</span><span class="sxs-lookup"><span data-stu-id="8beeb-109">**Without arguments**</span></span>

  <span data-ttu-id="8beeb-110">コマンド ラインが指定されていない場合、wsl.exe で既定のシェルが起動されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="8beeb-111">**--exec、-e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="8beeb-112">既定の Linux シェルを使用せずに、指定したコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="8beeb-113">残りのコマンドラインをそのまま渡します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="8beeb-114">上記のコマンドでは、次のオプションも使用できます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="8beeb-115">**--distribution、-d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="8beeb-116">指定されたディストリビューションを実行します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-116">Run the specified distribution.</span></span>

* <span data-ttu-id="8beeb-117">**--user、-u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="8beeb-118">指定されたユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="8beeb-119">Windows Subsystem for Linux を管理するための引数</span><span class="sxs-lookup"><span data-stu-id="8beeb-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="8beeb-120">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="8beeb-121">ディストリビューションを tar ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="8beeb-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="8beeb-122">標準出力の場合、ファイル名は - でもかまいません。</span><span class="sxs-lookup"><span data-stu-id="8beeb-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="8beeb-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="8beeb-124">指定した tar ファイルを新しいディストリビューションとしてインポートします。</span><span class="sxs-lookup"><span data-stu-id="8beeb-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="8beeb-125">標準入力の場合、ファイル名は - でもかまいません。</span><span class="sxs-lookup"><span data-stu-id="8beeb-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="8beeb-126">**--list、-l [Options]**</span><span class="sxs-lookup"><span data-stu-id="8beeb-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="8beeb-127">ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-127">Lists distributions.</span></span>

  <span data-ttu-id="8beeb-128">オプション:</span><span class="sxs-lookup"><span data-stu-id="8beeb-128">Options:</span></span>
  * <span data-ttu-id="8beeb-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="8beeb-129">**--all**</span></span>
      
    <span data-ttu-id="8beeb-130">現在インストール中またはアンインストール中のディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="8beeb-131">**--running**</span><span class="sxs-lookup"><span data-stu-id="8beeb-131">**--running**</span></span>
      
    <span data-ttu-id="8beeb-132">現在実行中のディストリビューションのみを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="8beeb-133">**--set-default、-s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="8beeb-134">このディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="8beeb-135">**--terminate、-t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="8beeb-136">指定されたディストリビューションを終了します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="8beeb-137">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="8beeb-138">ディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="8beeb-139">**--help** 使用方法に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="8beeb-140">その他のコマンド</span><span class="sxs-lookup"><span data-stu-id="8beeb-140">Additional Commands</span></span>

<span data-ttu-id="8beeb-141">Windows Subsystem for Linux を操作するための過去のコマンドもあります。</span><span class="sxs-lookup"><span data-stu-id="8beeb-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="8beeb-142">これらの機能は、`wsl.exe` 内に含まれますが、引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="8beeb-143">このコマンドでは、WSL ディストリビューションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="8beeb-144">そのオプションの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-144">Below is a list of its options.</span></span>

<span data-ttu-id="8beeb-145">使用法: `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="8beeb-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="8beeb-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="8beeb-146">Arguments</span></span>
* <span data-ttu-id="8beeb-147">**/l、/list [Options]**</span><span class="sxs-lookup"><span data-stu-id="8beeb-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="8beeb-148">登録済みのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="8beeb-149">オプション:</span><span class="sxs-lookup"><span data-stu-id="8beeb-149">Options:</span></span>
    * <span data-ttu-id="8beeb-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="8beeb-150">**/all**</span></span>
    
      <span data-ttu-id="8beeb-151">現在インストール中またはアンインストール中のディストリビューションを含む、すべてのディストリビューションをオプションで一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="8beeb-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="8beeb-152">**/running**</span></span>
      
      <span data-ttu-id="8beeb-153">現在実行中のディストリビューションのみを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="8beeb-154">**/s、/setdefault \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="8beeb-155">このディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="8beeb-156">**/t、/terminate \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="8beeb-157">ディストリビューションを終了します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-157">Terminates the distribution.</span></span>

* <span data-ttu-id="8beeb-158">**/u、/unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="8beeb-159">ディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="8beeb-160">**/upgrade \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="8beeb-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="8beeb-161">ディストリビューションを WslFs ファイル システム形式にアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="8beeb-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="8beeb-162">このコマンドは、bash シェルを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="8beeb-163">このコマンドで使用できるオプションを次に示します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="8beeb-164">使用法: `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="8beeb-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="8beeb-165">**オプションの指定なし**</span><span class="sxs-lookup"><span data-stu-id="8beeb-165">**No Option given**</span></span>
  
  <span data-ttu-id="8beeb-166">現在のディレクトリで Bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="8beeb-167">Bash シェルがインストールされていない場合は、`lxrun /install` が自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="8beeb-168">`bash ~` で、ユーザーのホームディレクトリに bash シェルが起動されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="8beeb-169">`cd ~` の実行と似ています。</span><span class="sxs-lookup"><span data-stu-id="8beeb-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="8beeb-170">**-c "\<command>"**</span><span class="sxs-lookup"><span data-stu-id="8beeb-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="8beeb-171">コマンドを実行し、出力を行って、Windows のコマンド プロンプトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="8beeb-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="8beeb-172">例: `bash -c "ls"` のようにします。</span><span class="sxs-lookup"><span data-stu-id="8beeb-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="8beeb-173">非推奨のコマンド</span><span class="sxs-lookup"><span data-stu-id="8beeb-173">Deprecated Commands</span></span>

<span data-ttu-id="8beeb-174">`lxrun.exe` は、Windows Subsystem for Linux をインストールして管理するために使用された最初のコマンドでした。</span><span class="sxs-lookup"><span data-stu-id="8beeb-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="8beeb-175">これは、Windows 10 1803 以降では非推奨です。</span><span class="sxs-lookup"><span data-stu-id="8beeb-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="8beeb-176">`lxrun.exe` コマンドは、[Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) を直接操作するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="8beeb-177">これらのコマンドは `\Windows\System32` ディレクトリにインストールされ、Windows コマンド プロンプトまたは PowerShell 内で実行できます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="8beeb-178">コマンド</span><span class="sxs-lookup"><span data-stu-id="8beeb-178">Command</span></span>                     | <span data-ttu-id="8beeb-179">説明</span><span class="sxs-lookup"><span data-stu-id="8beeb-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="8beeb-180">lxrun コマンドは、WSL インスタンスの管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="8beeb-181">ダウンロードとインストールのプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="8beeb-182">**/y** を追加すると、すべてのプロンプトを省略できます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="8beeb-183">確認プロンプトが自動的に受け入れられ、既定のユーザーはルートに設定されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="8beeb-184">Ubuntu イメージをアンインストールして削除します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="8beeb-185">既定では、これで、ユーザーの Ubuntu ホーム ディレクトリは削除されません。</span><span class="sxs-lookup"><span data-stu-id="8beeb-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="8beeb-186">**/y** を追加すると、確認プロンプトを自動的に受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="8beeb-187">**/full** を指定すると、ユーザーの Ubuntu ホーム ディレクトリをアンインストールして削除します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="8beeb-188">Ubuntu ユーザーの既定の Bash を設定します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="8beeb-189">指定されたユーザーが存在しない場合は、パスワードの入力が求められます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="8beeb-190">詳細については、 https://aka.ms/wslusers をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="8beeb-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="8beeb-191">**/y** を指定すると、パスワードの入力を求めるプロンプトは省略されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="8beeb-192">ユーザーはパスワードなしで作成されます。</span><span class="sxs-lookup"><span data-stu-id="8beeb-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="8beeb-193">サブシステムのパッケージ インデックスを更新します。</span><span class="sxs-lookup"><span data-stu-id="8beeb-193">Updates the subsystem's package index</span></span>          |
