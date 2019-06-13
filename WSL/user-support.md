---
title: Linux ユーザー アカウントとアクセス許可
description: Windows Subsystem for Linux でのユーザー アカウントとアクセス許可の管理の参照。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、ユーザー アカウント用の windows サブシステム
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040824"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="6a3d4-104">ユーザー アカウントと Linux 用 Windows サブシステムのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="6a3d4-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="6a3d4-105">WSL での新しい Linux ディストリビューションを設定する最初の手順は、Linux ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="6a3d4-106">作成する最初のユーザー アカウントは自動的に、いくつかの特別な属性を持つ構成します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="6a3d4-107">既定のユーザーが--にサインインすると自動的に起動します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="6a3d4-108">既定では、Linux 管理者 (sudo グループのメンバー) になります。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="6a3d4-109">Linux 用 Windows サブシステムで実行されている各 Linux ディストリビューションでは、独自の Linux ユーザー アカウントとパスワードを持ちます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="6a3d4-110">Linux ユーザー アカウントを構成するには、いつでも、ディストリビューションを追加、再インストール、またはリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="6a3d4-111">Linux ユーザー アカウントには、ディストリビューションごとに独立した、Windows ユーザー アカウントから独立していることもできます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="6a3d4-112">Linux パスワードのリセット</span><span class="sxs-lookup"><span data-stu-id="6a3d4-112">Resetting your Linux password</span></span>

<span data-ttu-id="6a3d4-113">Linux ユーザー アカウントにアクセスして変更して、現在のパスワードを知っている Linux を使用してパスワードのリセット ツールである可能性が最も高い--そのディストリビューションの`passwd`します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="6a3d4-114">場合は、オプションではなく、ディストリビューションによっては、既定のユーザーをリセットすることでパスワードをリセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="6a3d4-115">WSL では、ユーザー アカウントを自動的に識別するために、既定のユーザー タグは、WSL を開始するときログを提供します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="6a3d4-116">多くのディストリビューションには、ルートともルート ユーザーにパスワードが設定されていない既定のユーザーを設定するためのコマンドが含まれている、ルートに既定のユーザーを変更するは、パスワードのリセットなどの便利なツールです。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="6a3d4-117">Creators Update 以降</span><span class="sxs-lookup"><span data-stu-id="6a3d4-117">For Creators Update and earlier</span></span>
<span data-ttu-id="6a3d4-118">実行している場合は、Windows 10 Creators update または以前では、次のコマンドを実行して既定の Bash のユーザーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="6a3d4-119">既定のユーザーを変更する`root`:</span><span class="sxs-lookup"><span data-stu-id="6a3d4-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="6a3d4-120">実行`bash.exe`として現在のログインに`root`:</span><span class="sxs-lookup"><span data-stu-id="6a3d4-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="6a3d4-121">ディストリビューションのパスワードのコマンドを使用してパスワードをリセットし、Linux コンソールを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="6a3d4-122">Windows コマンド プロンプトで、通常の Linux ユーザー アカウントに既定のユーザーをリセットします。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="6a3d4-123">Fall Creators Update 以降</span><span class="sxs-lookup"><span data-stu-id="6a3d4-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="6a3d4-124">どのようなコマンドは、特定の配布の使用については、次のように実行します。`[distro.exe] /?`します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="6a3d4-125">たとえば、Ubuntu のインストール。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="6a3d4-126">ステップ バイ ステップで Ubuntu を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="6a3d4-127">開いている CMD</span><span class="sxs-lookup"><span data-stu-id="6a3d4-127">Open CMD</span></span>
1. <span data-ttu-id="6a3d4-128">既定の Linux ユーザーを設定`root`:</span><span class="sxs-lookup"><span data-stu-id="6a3d4-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="6a3d4-129">Linux ディストリビューションを起動 (`ubuntu`)。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="6a3d4-130">自動的には、ログインとして`root`:</span><span class="sxs-lookup"><span data-stu-id="6a3d4-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="6a3d4-131">使用して、パスワードのリセット、`passwd`コマンド。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="6a3d4-132">Windows コマンド プロンプトで、通常の Linux ユーザー アカウントに既定のユーザーをリセットします。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="6a3d4-133">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="6a3d4-133">Permissions</span></span>

<span data-ttu-id="6a3d4-134">WSL でのアクセスを許可する際に留意する 2 つの重要な概念があります。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="6a3d4-135">Windows のアクセス許可モデルは、Windows リソースへのプロセスの権限を制御します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="6a3d4-136">Linux のアクセス許可モデルは、Linux リソースへのプロセスの権限を制御します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="6a3d4-137">WSL で Linux を実行するときに、Linux は、起動するプロセスと同じ Windows 権限があります。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="6a3d4-138">Linux は、2 つのアクセス許可レベルのいずれかで起動できます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="6a3d4-139">標準 (非特権):ログイン ユーザーのアクセス許可を持つ Linux が実行されます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="6a3d4-140">管理者特権で/管理者:管理者特権で/管理者の Windows アクセス許可を持つ Linux が実行されます。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="6a3d4-141">昇格されたプロセスできますアクセス/変更 (したがって損害を与える) システム全体の設定とシステム全体/保護対象のデータでは、**避け**を Windows または Linux いるかどうかが絶対にない限り、昇格されたプロセスを起動します。アプリケーション/tools/シェルです。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="6a3d4-142">上記の Windows アクセス許可は、Linux インスタンス内でアクセス許可に依存しません。Linux の「Root 特権」Linux 環境とファイルシステム内のユーザーの権限の影響のみ影響を与えるありませんに与えられている Windows 特権。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="6a3d4-143">そのため、ルートとして Linux プロセスを実行している (経由など`sudo`) Linux 環境内で管理者権限を処理するのみを付与します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="6a3d4-144">**例:**   </span><span class="sxs-lookup"><span data-stu-id="6a3d4-144">**Example:**  </span></span>  
<span data-ttu-id="6a3d4-145">管理者特権の Windows で Bash セッションがアクセスできる`cd /mnt/c/Users/Administrator`Bash セッションを管理者特権が「アクセス許可が拒否されました」エラーを表示せずにします。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="6a3d4-146">Linux では、入力`sudo cd /mnt/c/Users/Administrator`Windows 内でアクセス許可が Windows によって管理されるため、管理者のディレクトリへのアクセスを付与されませんが。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="6a3d4-147">Linux のアクセス許可モデルは、Linux 環境をユーザーが現在の Linux ユーザーに基づいて、アクセス許可を持っている内で重要です。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="6a3d4-148">**例:**</span><span class="sxs-lookup"><span data-stu-id="6a3d4-148">**Example:**</span></span>  
<span data-ttu-id="6a3d4-149">Sudo グループ内のユーザーが実行される可能性が`sudo apt update`します。</span><span class="sxs-lookup"><span data-stu-id="6a3d4-149">A user in the sudo group may run `sudo apt update`.</span></span>
