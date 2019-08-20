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
ms.openlocfilehash: 018b02b43e859476f7ee38f54df8efa0ca0e652b
ms.sourcegitcommit: 62c49d435a91f2e390c3c495f3e09e62b5ada13c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "69578842"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="df231-104">Windows Subsystem for Linux のコマンドリファレンス</span><span class="sxs-lookup"><span data-stu-id="df231-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="df231-105">Windows Subsystem for Linux を操作する最良の方法は、 `wsl.exe`コマンドを使用することです。</span><span class="sxs-lookup"><span data-stu-id="df231-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="df231-106">Windows バージョン1903以降を使用して`wsl.exe`いる場合のすべてのオプションを含む一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="df231-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="df231-107">従っ`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="df231-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="df231-108">Linux バイナリを実行するための引数</span><span class="sxs-lookup"><span data-stu-id="df231-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="df231-109">**引数なし**</span><span class="sxs-lookup"><span data-stu-id="df231-109">**Without arguments**</span></span>

  <span data-ttu-id="df231-110">コマンドラインが指定されていない場合、既定のシェルが起動されます。</span><span class="sxs-lookup"><span data-stu-id="df231-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="df231-111">**--exec、-e \<コマンドライン >**</span><span class="sxs-lookup"><span data-stu-id="df231-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="df231-112">既定の Linux シェルを使用せずに、指定したコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="df231-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="df231-113">残りのコマンドラインをそのまま渡します。</span><span class="sxs-lookup"><span data-stu-id="df231-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="df231-114">上記のコマンドでは、次のオプションも使用できます。</span><span class="sxs-lookup"><span data-stu-id="df231-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="df231-115">**--distribution、-d \<ディストリビューション >**</span><span class="sxs-lookup"><span data-stu-id="df231-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="df231-116">指定された分布を実行します。</span><span class="sxs-lookup"><span data-stu-id="df231-116">Run the specified distribution.</span></span>

* <span data-ttu-id="df231-117">**--user、-u \<UserName >**</span><span class="sxs-lookup"><span data-stu-id="df231-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="df231-118">指定されたユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="df231-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="df231-119">Linux 用 Windows サブシステムを管理するための引数</span><span class="sxs-lookup"><span data-stu-id="df231-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="df231-120">**--ディストリビューション\<> \<ファイル名 > をエクスポートします**</span><span class="sxs-lookup"><span data-stu-id="df231-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="df231-121">配布を tar ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="df231-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="df231-122">ファイル名には、標準出力の場合はを指定できます。</span><span class="sxs-lookup"><span data-stu-id="df231-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="df231-123">**--ディストリビューション\<> \<InstallLocation > \<FileName > をインポートします**</span><span class="sxs-lookup"><span data-stu-id="df231-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="df231-124">指定した tar ファイルを新しいディストリビューションとしてインポートします。</span><span class="sxs-lookup"><span data-stu-id="df231-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="df231-125">ファイル名には、標準入力の場合はを指定できます。</span><span class="sxs-lookup"><span data-stu-id="df231-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="df231-126">**--list、-l [Options]**</span><span class="sxs-lookup"><span data-stu-id="df231-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="df231-127">ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="df231-127">Lists distributions.</span></span>

  <span data-ttu-id="df231-128">オプション:</span><span class="sxs-lookup"><span data-stu-id="df231-128">Options:</span></span>
  * <span data-ttu-id="df231-129">**--すべて**</span><span class="sxs-lookup"><span data-stu-id="df231-129">**--all**</span></span>
      
    <span data-ttu-id="df231-130">現在インストール中またはアンインストール中のディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="df231-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="df231-131">**--実行中**</span><span class="sxs-lookup"><span data-stu-id="df231-131">**--running**</span></span>
      
    <span data-ttu-id="df231-132">現在実行中のディストリビューションのみを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="df231-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="df231-133">**--set-既定値、- \<s ディストリビューション >**</span><span class="sxs-lookup"><span data-stu-id="df231-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="df231-134">ディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="df231-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="df231-135">**--terminate、-t \<ディストリビューション >**</span><span class="sxs-lookup"><span data-stu-id="df231-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="df231-136">指定された分布を終了します。</span><span class="sxs-lookup"><span data-stu-id="df231-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="df231-137">**--ディストリビューション\<の登録を解除 >**</span><span class="sxs-lookup"><span data-stu-id="df231-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="df231-138">ディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="df231-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="df231-139">**--help**使用状況に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="df231-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="df231-140">その他のコマンド</span><span class="sxs-lookup"><span data-stu-id="df231-140">Additional Commands</span></span>

<span data-ttu-id="df231-141">Windows Subsystem for Linux と対話するための履歴コマンドもあります。</span><span class="sxs-lookup"><span data-stu-id="df231-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="df231-142">これらの機能はに`wsl.exe`含まれていますが、引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="df231-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="df231-143">このコマンドでは、WSL 分布を構成できます。</span><span class="sxs-lookup"><span data-stu-id="df231-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="df231-144">そのオプションの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="df231-144">Below is a list of its options.</span></span>

<span data-ttu-id="df231-145">従っ`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="df231-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="df231-146">引数</span><span class="sxs-lookup"><span data-stu-id="df231-146">Arguments</span></span>
* <span data-ttu-id="df231-147">**/l、/list [オプション]**</span><span class="sxs-lookup"><span data-stu-id="df231-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="df231-148">登録済みのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="df231-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="df231-149">オプション:</span><span class="sxs-lookup"><span data-stu-id="df231-149">Options:</span></span>
    * <span data-ttu-id="df231-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="df231-150">**/all**</span></span>
    
      <span data-ttu-id="df231-151">必要に応じて、現在インストール中またはアンインストール中のディストリビューションも含め、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="df231-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="df231-152">**/実行中**</span><span class="sxs-lookup"><span data-stu-id="df231-152">**/running**</span></span>
      
      <span data-ttu-id="df231-153">現在実行中のディストリビューションのみを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="df231-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="df231-154">**/s、/setdefault \<のディストリビューション >**</span><span class="sxs-lookup"><span data-stu-id="df231-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="df231-155">ディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="df231-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="df231-156">**/t、または\<ディストリビューションを終了し >**</span><span class="sxs-lookup"><span data-stu-id="df231-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="df231-157">分布を終了します。</span><span class="sxs-lookup"><span data-stu-id="df231-157">Terminates the distribution.</span></span>

* <span data-ttu-id="df231-158">**/u、/unregister \<のディストリビューション >**</span><span class="sxs-lookup"><span data-stu-id="df231-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="df231-159">ディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="df231-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="df231-160">**/upgrade \<のディストリビューション >**</span><span class="sxs-lookup"><span data-stu-id="df231-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="df231-161">分散を WslFs ファイルシステム形式にアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="df231-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="df231-162">このコマンドは、bash シェルを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="df231-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="df231-163">このコマンドで使用できるオプションを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="df231-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="df231-164">従っ`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="df231-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="df231-165">**オプションが指定されていません**</span><span class="sxs-lookup"><span data-stu-id="df231-165">**No Option given**</span></span>
  
  <span data-ttu-id="df231-166">現在のディレクトリで Bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="df231-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="df231-167">Bash シェルがインストールされていない場合は、自動的に実行されます。`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="df231-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="df231-168">`bash ~`ユーザーのホームディレクトリに bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="df231-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="df231-169">の実行`cd ~`と同様です。</span><span class="sxs-lookup"><span data-stu-id="df231-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="df231-170">**-c "\<command >"**</span><span class="sxs-lookup"><span data-stu-id="df231-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="df231-171">コマンドを実行し、出力を出力して、Windows のコマンドプロンプトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="df231-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="df231-172">例: `bash -c "ls"`。</span><span class="sxs-lookup"><span data-stu-id="df231-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="df231-173">非推奨のコマンド</span><span class="sxs-lookup"><span data-stu-id="df231-173">Deprecated Commands</span></span>

<span data-ttu-id="df231-174">は`lxrun.exe` 、Windows Subsystem for Linux をインストールして管理するために使用される最初のコマンドでした。</span><span class="sxs-lookup"><span data-stu-id="df231-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="df231-175">Windows 10 1803 以降では非推奨とされます。</span><span class="sxs-lookup"><span data-stu-id="df231-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="df231-176">コマンド`lxrun.exe`を使用して、 [Windows Subsystem for Linux (wsl)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)と直接やり取りできます。</span><span class="sxs-lookup"><span data-stu-id="df231-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="df231-177">これらのコマンドは`\Windows\System32`ディレクトリにインストールされ、Windows コマンドプロンプトまたは PowerShell 内で実行できます。</span><span class="sxs-lookup"><span data-stu-id="df231-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="df231-178">Command</span><span class="sxs-lookup"><span data-stu-id="df231-178">Command</span></span>                     | <span data-ttu-id="df231-179">説明</span><span class="sxs-lookup"><span data-stu-id="df231-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="df231-180">Lxrun コマンドは、WSL インスタンスを管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="df231-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="df231-181">ダウンロードとインストールのプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="df231-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="df231-182">すべてのプロンプトをバイパスするには、 **/y**を追加します。</span><span class="sxs-lookup"><span data-stu-id="df231-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="df231-183">確認プロンプトが自動的に受け入れられ、既定のユーザーは root に設定されます。</span><span class="sxs-lookup"><span data-stu-id="df231-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="df231-184">Ubuntu イメージをアンインストールおよび削除します。</span><span class="sxs-lookup"><span data-stu-id="df231-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="df231-185">既定では、ユーザーの Ubuntu ホームディレクトリは削除されません。</span><span class="sxs-lookup"><span data-stu-id="df231-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="df231-186">**/y**を追加して確認プロンプトを自動的に受け入れることができます</span><span class="sxs-lookup"><span data-stu-id="df231-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="df231-187">のユーザーの Ubuntu ホームディレクトリをアンインストールおよび削除します。</span><span class="sxs-lookup"><span data-stu-id="df231-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="df231-188">Ubuntu ユーザーの既定の Bash を設定します。</span><span class="sxs-lookup"><span data-stu-id="df231-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="df231-189">指定されたユーザーが存在しない場合は、パスワードの入力を求められます。</span><span class="sxs-lookup"><span data-stu-id="df231-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="df231-190">詳細については https://aka.ms/wslusers 、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df231-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="df231-191">**/y**パスワードの promping をバイパスします。</span><span class="sxs-lookup"><span data-stu-id="df231-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="df231-192">ユーザーはパスワードなしで作成されます。</span><span class="sxs-lookup"><span data-stu-id="df231-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="df231-193">サブシステムのパッケージインデックスを更新します</span><span class="sxs-lookup"><span data-stu-id="df231-193">Updates the subsystem's package index</span></span>          |
