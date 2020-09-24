---
title: Windows Subsystem for Linux のコマンド リファレンス
description: Linux コマンドを実行するための引数など、Linux 用 Windows サブシステムを管理するコマンドの一覧をご覧ください。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 6f98cb7b238e4b38c1a931a0e77e419efbcc319d
ms.sourcegitcommit: ba3399a5ffeffd23551315acd04ea6848d30693b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2020
ms.locfileid: "90719170"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="76c1a-104">Windows Subsystem for Linux のコマンド リファレンス</span><span class="sxs-lookup"><span data-stu-id="76c1a-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="76c1a-105">Windows Subsystem for Linux を操作する最良の方法は、`wsl.exe` コマンドを使用することです。</span><span class="sxs-lookup"><span data-stu-id="76c1a-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span>

## <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="76c1a-106">WSL 2 を既定のバージョンとして設定する</span><span class="sxs-lookup"><span data-stu-id="76c1a-106">Set WSL 2 as your default version</span></span>

<span data-ttu-id="76c1a-107">PowerShell で次のコマンドを実行して、新しい Linux ディストリビューションをインストールするときに WSL 2 を既定のバージョンとして設定します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-107">Run the following command in Powershell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="76c1a-108">ディストリビューションのバージョンを WSL 1 または WSL 2 に設定する</span><span class="sxs-lookup"><span data-stu-id="76c1a-108">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="76c1a-109">インストールされている各 Linux ディストリビューションに割り当てられている WSL バージョンを確認するには、PowerShell コマンド ラインを開き、次のコマンドを入力します ([Windows ビルド 19041 以上](ms-settings:windowsupdate)でのみ使用可能): `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="76c1a-109">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```bash
wsl --list --verbose
```

<span data-ttu-id="76c1a-110">ディストリビューションで使用される WSL のバージョンを設定するには、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-110">To set a distribution to be backed by either version of WSL please run:</span></span>

```bash
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="76c1a-111">`<distribution name>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。`<versionNumber>` は、数字の "1" または "2" に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="76c1a-111">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="76c1a-112">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-112">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="76c1a-113">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-113">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```bash
wsl --set-default-version 2
```

<span data-ttu-id="76c1a-114">これにより、インストールされるすべての新しいディストリビューションのバージョンが WSL 2 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-114">This will set the version of any new distribution installed to WSL 2.</span></span>

## `wsl.exe`

<span data-ttu-id="76c1a-115">Windows バージョン 1903 以降で `wsl.exe` を使用する場合のすべてのオプションを含む一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-115">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="76c1a-116">使用法: `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="76c1a-116">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-commands"></a><span data-ttu-id="76c1a-117">Linux コマンドを実行するための引数</span><span class="sxs-lookup"><span data-stu-id="76c1a-117">Arguments for running Linux commands</span></span>

* <span data-ttu-id="76c1a-118">**引数なし**</span><span class="sxs-lookup"><span data-stu-id="76c1a-118">**Without arguments**</span></span>

  <span data-ttu-id="76c1a-119">コマンド ラインが指定されていない場合、wsl.exe で既定のシェルが起動されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-119">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="76c1a-120">**--exec、-e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-120">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="76c1a-121">既定の Linux シェルを使用せずに、指定したコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-121">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="76c1a-122">残りのコマンドラインをそのまま渡します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-122">Pass the remaining command line as is.</span></span>

<span data-ttu-id="76c1a-123">上記のコマンドでは、次のオプションも使用できます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-123">The above commands also accept the following options:</span></span>

* <span data-ttu-id="76c1a-124">**--distribution、-d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-124">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="76c1a-125">指定されたディストリビューションを実行します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-125">Run the specified distribution.</span></span>

* <span data-ttu-id="76c1a-126">**--user、-u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-126">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="76c1a-127">指定されたユーザーとして実行します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-127">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="76c1a-128">Windows Subsystem for Linux を管理するための引数</span><span class="sxs-lookup"><span data-stu-id="76c1a-128">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="76c1a-129">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-129">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="76c1a-130">ディストリビューションを tar ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="76c1a-130">Exports the distribution to a tar file.</span></span> <span data-ttu-id="76c1a-131">標準出力の場合、ファイル名は - でもかまいません。</span><span class="sxs-lookup"><span data-stu-id="76c1a-131">The filename can be - for standard output.</span></span>

* <span data-ttu-id="76c1a-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="76c1a-133">指定した tar ファイルを新しいディストリビューションとしてインポートします。</span><span class="sxs-lookup"><span data-stu-id="76c1a-133">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="76c1a-134">標準入力の場合、ファイル名は - でもかまいません。</span><span class="sxs-lookup"><span data-stu-id="76c1a-134">The filename can be - for standard input.</span></span>

* <span data-ttu-id="76c1a-135">**--list、-l [Options]**</span><span class="sxs-lookup"><span data-stu-id="76c1a-135">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="76c1a-136">ディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-136">Lists distributions.</span></span>

  <span data-ttu-id="76c1a-137">オプション:</span><span class="sxs-lookup"><span data-stu-id="76c1a-137">Options:</span></span>
  * <span data-ttu-id="76c1a-138">**--all**</span><span class="sxs-lookup"><span data-stu-id="76c1a-138">**--all**</span></span>

    <span data-ttu-id="76c1a-139">現在インストール中またはアンインストール中のディストリビューションを含む、すべてのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-139">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="76c1a-140">**--running**</span><span class="sxs-lookup"><span data-stu-id="76c1a-140">**--running**</span></span>

    <span data-ttu-id="76c1a-141">現在実行中のディストリビューションのみを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-141">List only distributions that are currently running.</span></span>

* <span data-ttu-id="76c1a-142">**--set-default、-s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-142">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="76c1a-143">このディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-143">Sets the distribution as the default.</span></span>

* <span data-ttu-id="76c1a-144">**--terminate、-t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-144">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="76c1a-145">指定されたディストリビューションを終了します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-145">Terminates the specified distribution.</span></span>

* <span data-ttu-id="76c1a-146">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="76c1a-146">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="76c1a-147">ディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-147">Un-register the distribution.</span></span>

* <span data-ttu-id="76c1a-148">**--help** 使用方法に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-148">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="76c1a-149">その他のコマンド</span><span class="sxs-lookup"><span data-stu-id="76c1a-149">Additional Commands</span></span>

<span data-ttu-id="76c1a-150">Windows Subsystem for Linux を操作するための過去のコマンドもあります。</span><span class="sxs-lookup"><span data-stu-id="76c1a-150">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="76c1a-151">これらの機能は、`wsl.exe` 内に含まれますが、引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-151">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span>

### `wslconfig.exe`

<span data-ttu-id="76c1a-152">このコマンドでは、WSL ディストリビューションを構成できます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-152">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="76c1a-153">そのオプションの一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-153">Below is a list of its options.</span></span>

<span data-ttu-id="76c1a-154">使用法: `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="76c1a-154">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="76c1a-155">引数</span><span class="sxs-lookup"><span data-stu-id="76c1a-155">Arguments</span></span>

* <span data-ttu-id="76c1a-156">**/l、/list [Options]**</span><span class="sxs-lookup"><span data-stu-id="76c1a-156">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="76c1a-157">登録済みのディストリビューションを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-157">Lists registered distributions.</span></span>
  
<span data-ttu-id="76c1a-158">オプション:</span><span class="sxs-lookup"><span data-stu-id="76c1a-158">Options:</span></span>

* <span data-ttu-id="76c1a-159">**/all** 現在インストール中またはアンインストール中のディストリビューションを含む、すべてのディストリビューションをオプションで一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-159">**/all** Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

* <span data-ttu-id="76c1a-160">**/running** 現在実行中のディストリビューションのみを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-160">**/running** List only distributions that are currently running.</span></span>

* <span data-ttu-id="76c1a-161">**/s、/setdefault \<Distro>** このディストリビューションを既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-161">**/s, /setdefault \<Distro>** Sets the distribution as the default.</span></span>

* <span data-ttu-id="76c1a-162">**/t、/terminate \<Distro>** このディストリビューションを終了します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-162">**/t, /terminate \<Distro>** Terminates the distribution.</span></span>

* <span data-ttu-id="76c1a-163">**/u、/unregister \<Distro>** このディストリビューションの登録を解除します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-163">**/u, /unregister \<Distro>** Un-registers the distribution.</span></span>

* <span data-ttu-id="76c1a-164">**/upgrade \<Distro>** このディストリビューションを WslFs ファイル システム形式にアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="76c1a-164">**/upgrade \<Distro>** Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="76c1a-165">このコマンドは、bash シェルを開始するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-165">This command is used to start a bash shell.</span></span> <span data-ttu-id="76c1a-166">このコマンドで使用できるオプションを次に示します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-166">Below are the options you can use with this command.</span></span>

<span data-ttu-id="76c1a-167">使用法: `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="76c1a-167">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="76c1a-168">**オプションの指定なし**</span><span class="sxs-lookup"><span data-stu-id="76c1a-168">**No Option given**</span></span>
  
  <span data-ttu-id="76c1a-169">現在のディレクトリで Bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-169">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="76c1a-170">Bash シェルがインストールされていない場合は、`lxrun /install` が自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-170">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="76c1a-171">`bash ~` で、ユーザーのホームディレクトリに bash シェルが起動されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-171">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="76c1a-172">`cd ~` の実行と似ています。</span><span class="sxs-lookup"><span data-stu-id="76c1a-172">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="76c1a-173">**-c "\<command>"**</span><span class="sxs-lookup"><span data-stu-id="76c1a-173">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="76c1a-174">コマンドを実行し、出力を行って、Windows のコマンド プロンプトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="76c1a-174">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>

  <span data-ttu-id="76c1a-175">例: `bash -c "ls"` のようにします。</span><span class="sxs-lookup"><span data-stu-id="76c1a-175">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="76c1a-176">非推奨のコマンド</span><span class="sxs-lookup"><span data-stu-id="76c1a-176">Deprecated Commands</span></span>

<span data-ttu-id="76c1a-177">`lxrun.exe` は、Windows Subsystem for Linux をインストールして管理するために使用された最初のコマンドでした。</span><span class="sxs-lookup"><span data-stu-id="76c1a-177">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="76c1a-178">これは、Windows 10 1803 以降では非推奨です。</span><span class="sxs-lookup"><span data-stu-id="76c1a-178">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="76c1a-179">`lxrun.exe` コマンドは、Windows Subsystem for Linux (WSL) を直接操作するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-179">The command `lxrun.exe` can be used to interact with the Windows Subsystem for Linux (WSL) directly.</span></span>  <span data-ttu-id="76c1a-180">これらのコマンドは `\Windows\System32` ディレクトリにインストールされ、Windows コマンド プロンプトまたは PowerShell 内で実行できます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-180">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="76c1a-181">コマンド</span><span class="sxs-lookup"><span data-stu-id="76c1a-181">Command</span></span>                     | <span data-ttu-id="76c1a-182">説明</span><span class="sxs-lookup"><span data-stu-id="76c1a-182">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="76c1a-183">lxrun コマンドは、WSL インスタンスの管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-183">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="76c1a-184">ダウンロードとインストールのプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-184">Starts the download and install process.</span></span> <br/> <span data-ttu-id="76c1a-185">**/y** を追加すると、すべてのプロンプトを省略できます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-185">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="76c1a-186">確認プロンプトが自動的に受け入れられ、既定のユーザーはルートに設定されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-186">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="76c1a-187">Ubuntu イメージをアンインストールして削除します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-187">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="76c1a-188">既定では、これで、ユーザーの Ubuntu ホーム ディレクトリは削除されません。</span><span class="sxs-lookup"><span data-stu-id="76c1a-188">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="76c1a-189">**/y** を追加すると、確認プロンプトを自動的に受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-189">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="76c1a-190">**/full** を指定すると、ユーザーの Ubuntu ホーム ディレクトリをアンインストールして削除します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-190">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="76c1a-191">Ubuntu ユーザーの既定の Bash を設定します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-191">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="76c1a-192">指定されたユーザーが存在しない場合は、パスワードの入力が求められます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-192">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="76c1a-193">詳細については、 https://aka.ms/wslusers をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="76c1a-193">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="76c1a-194">**/y** を指定すると、パスワードの入力を求めるプロンプトは省略されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-194">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="76c1a-195">ユーザーはパスワードなしで作成されます。</span><span class="sxs-lookup"><span data-stu-id="76c1a-195">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="76c1a-196">サブシステムのパッケージ インデックスを更新します。</span><span class="sxs-lookup"><span data-stu-id="76c1a-196">Updates the subsystem's package index</span></span>          |
