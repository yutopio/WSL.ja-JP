---
title: Linux ユーザーアカウントとアクセス許可
description: Windows Subsystem for Linux を使用したユーザーアカウントとアクセス許可の管理のリファレンスです。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、ユーザーアカウント
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122682"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="37f7c-104">Windows Subsystem for Linux のユーザーアカウントとアクセス許可</span><span class="sxs-lookup"><span data-stu-id="37f7c-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="37f7c-105">Linux ユーザーの作成は、WSL で新しい Linux ディストリビューションを設定するための最初の手順です。</span><span class="sxs-lookup"><span data-stu-id="37f7c-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="37f7c-106">作成した最初のユーザーアカウントは、次のいくつかの特殊な属性で自動的に構成されます。</span><span class="sxs-lookup"><span data-stu-id="37f7c-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="37f7c-107">これは既定のユーザーであり、起動時に自動的にサインインします。</span><span class="sxs-lookup"><span data-stu-id="37f7c-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="37f7c-108">既定では、Linux 管理者 (sudo グループのメンバー) です。</span><span class="sxs-lookup"><span data-stu-id="37f7c-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="37f7c-109">Windows Subsystem for Linux で実行されている各 Linux ディストリビューションには、独自の Linux ユーザーアカウントとパスワードがあります。</span><span class="sxs-lookup"><span data-stu-id="37f7c-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="37f7c-110">ディストリビューションの追加、再インストール、またはリセットを行うたびに、Linux ユーザーアカウントを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f7c-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="37f7c-111">Linux ユーザーアカウントは、ディストリビューションごとに独立しているわけではなく、Windows ユーザーアカウントにも依存しません。</span><span class="sxs-lookup"><span data-stu-id="37f7c-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="37f7c-112">Linux パスワードをリセットしています</span><span class="sxs-lookup"><span data-stu-id="37f7c-112">Resetting your Linux password</span></span>

<span data-ttu-id="37f7c-113">Linux ユーザーアカウントへのアクセス権があり、現在のパスワードを把握している場合は、そのディストリビューション`passwd`の linux パスワードリセットツールを使用して変更してください。</span><span class="sxs-lookup"><span data-stu-id="37f7c-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="37f7c-114">このオプションが選択されていない場合は、ディストリビューションによっては、既定のユーザーをリセットすることによってパスワードをリセットできる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="37f7c-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="37f7c-115">WSL は、WSL を開始するときに自動的にログインするユーザーアカウントを識別するための既定のユーザータグを提供します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="37f7c-116">多くのディストリビューションには、既定のユーザーを root に設定するコマンドや、パスワードが設定されていないルートユーザーを設定するコマンドが含まれているため、既定のユーザーを root に変更すると、パスワードのリセットなどの便利なツールになります。</span><span class="sxs-lookup"><span data-stu-id="37f7c-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="37f7c-117">作成者の更新プログラム (以前のバージョンの場合)</span><span class="sxs-lookup"><span data-stu-id="37f7c-117">For Creators Update and earlier</span></span>
<span data-ttu-id="37f7c-118">Windows 10 の作成者更新プログラムまたはそれ以前のバージョンを実行している場合は、次のコマンドを実行して既定の Bash ユーザーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="37f7c-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="37f7c-119">既定のユーザーを次`root`のように変更します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="37f7c-120">今すぐ`bash.exe`実行する`root`ログイン:</span><span class="sxs-lookup"><span data-stu-id="37f7c-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="37f7c-121">ディストリビューションのパスワードコマンドを使用してパスワードをリセットし、Linux コンソールを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37f7c-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="37f7c-122">Windows CMD で、既定のユーザーをリセットし、通常の Linux ユーザーアカウントに戻します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="37f7c-123">秋に更新プログラムをインストールする場合</span><span class="sxs-lookup"><span data-stu-id="37f7c-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="37f7c-124">特定のディストリビューションで使用できるコマンドを確認するには`[distro.exe] /?`、を実行します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="37f7c-125">たとえば、Ubuntu がインストールされているとします。</span><span class="sxs-lookup"><span data-stu-id="37f7c-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="37f7c-126">Ubuntu を使用したステップバイステップの手順:</span><span class="sxs-lookup"><span data-stu-id="37f7c-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="37f7c-127">CMD を開く</span><span class="sxs-lookup"><span data-stu-id="37f7c-127">Open CMD</span></span>
1. <span data-ttu-id="37f7c-128">既定の Linux ユーザーを次`root`のように設定します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="37f7c-129">Linux ディストリビューション (`ubuntu`) を起動します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="37f7c-130">次のように自動的`root`にログインします。</span><span class="sxs-lookup"><span data-stu-id="37f7c-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="37f7c-131">次の`passwd`コマンドを使用してパスワードをリセットします。</span><span class="sxs-lookup"><span data-stu-id="37f7c-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="37f7c-132">Windows CMD で、既定のユーザーをリセットして、通常の Linux ユーザーアカウントに戻します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="37f7c-133">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="37f7c-133">Permissions</span></span>

<span data-ttu-id="37f7c-134">WSL のアクセス許可に関しては、次の2つの重要な概念を念頭に置く必要があります。</span><span class="sxs-lookup"><span data-stu-id="37f7c-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="37f7c-135">Windows アクセス許可モデルは、Windows リソースに対するプロセスの権限を制御します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="37f7c-136">Linux アクセス許可モデルは、Linux リソースに対するプロセスの権限を制御します。</span><span class="sxs-lookup"><span data-stu-id="37f7c-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="37f7c-137">WSL で Linux を実行すると、Linux はそれを起動するプロセスと同じ Windows アクセス許可を持ちます。</span><span class="sxs-lookup"><span data-stu-id="37f7c-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="37f7c-138">Linux は、次の2つのアクセス許可レベルのいずれかで起動できます。</span><span class="sxs-lookup"><span data-stu-id="37f7c-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="37f7c-139">標準 (昇格されていない):Linux は、ログインしているユーザーのアクセス許可で実行されます。</span><span class="sxs-lookup"><span data-stu-id="37f7c-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="37f7c-140">昇格された管理者:管理者特権での Windows のアクセス許可を使用して Linux を実行する</span><span class="sxs-lookup"><span data-stu-id="37f7c-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="37f7c-141">昇格されたプロセスはシステム全体の設定とシステム全体または保護されたデータにアクセスしたり、変更したりできます。そのため、Windows または Linux のアプリケーション/ツールであるかどうかにかかわらず、管理者特権のプロセスを起動しない**よう**にしてください。シェル!</span><span class="sxs-lookup"><span data-stu-id="37f7c-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="37f7c-142">上記の Windows アクセス許可は、Linux インスタンス内のアクセス許可とは無関係です。Linux の "Root 特権" は、Linux 環境 & ファイルシステム内のユーザーの権限にのみ影響します。付与された Windows 特権には影響しません。</span><span class="sxs-lookup"><span data-stu-id="37f7c-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="37f7c-143">したがって、linux プロセスをルートとして実行する`sudo`と (例: via)、linux 環境内のプロセス管理者権限のみが付与されます。</span><span class="sxs-lookup"><span data-stu-id="37f7c-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="37f7c-144">**例:**   </span><span class="sxs-lookup"><span data-stu-id="37f7c-144">**Example:**  </span></span>  
<span data-ttu-id="37f7c-145">管理者特権のない bash セッションで " `cd /mnt/c/Users/Administrator`アクセス許可が拒否されました" というエラーが表示される場合、Windows 管理者特権を持つ bash セッションがアクセスする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="37f7c-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="37f7c-146">Linux では、 `sudo cd /mnt/c/Users/Administrator` windows のアクセス許可は windows によって管理されているため、「」と入力すると、管理者のディレクトリへのアクセス権が付与されません。</span><span class="sxs-lookup"><span data-stu-id="37f7c-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="37f7c-147">Linux アクセス許可モデルは、linux 環境内で、ユーザーが現在の Linux ユーザーに基づいてアクセス許可を持っている場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="37f7c-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="37f7c-148">**例:**</span><span class="sxs-lookup"><span data-stu-id="37f7c-148">**Example:**</span></span>  
<span data-ttu-id="37f7c-149">Sudo グループ内のユーザーが実行`sudo apt update`される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="37f7c-149">A user in the sudo group may run `sudo apt update`.</span></span>
