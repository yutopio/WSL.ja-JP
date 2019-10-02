---
title: Linux ユーザー アカウントとアクセス許可
description: Windows Subsystem for Linux を使用したユーザー アカウントとアクセス許可の管理のリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, ユーザー アカウント
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122682"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="048ca-104">Windows Subsystem for Linux のユーザー アカウントとアクセス許可</span><span class="sxs-lookup"><span data-stu-id="048ca-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="048ca-105">Linux ユーザーの作成は、WSL で新しい Linux ディストリビューションを設定する際の最初の手順です。</span><span class="sxs-lookup"><span data-stu-id="048ca-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="048ca-106">作成した最初のユーザー アカウントは、次のいくつかの特殊な属性で自動的に構成されます。</span><span class="sxs-lookup"><span data-stu-id="048ca-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="048ca-107">これは既定のユーザーであり、起動時に自動的にサインインします。</span><span class="sxs-lookup"><span data-stu-id="048ca-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="048ca-108">既定では、Linux 管理者 (sudo グループのメンバー) です。</span><span class="sxs-lookup"><span data-stu-id="048ca-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="048ca-109">Windows Subsystem for Linux で実行されている各 Linux ディストリビューションには、独自の Linux ユーザー アカウントとパスワードがあります。</span><span class="sxs-lookup"><span data-stu-id="048ca-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="048ca-110">ディストリビューションの追加、再インストール、または再設定を行うたびに、Linux ユーザー アカウントを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="048ca-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="048ca-111">Linux ユーザー アカウントは、ディストリビューションごとに独立しているだけではなく、Windows ユーザー アカウントにも依存しません。</span><span class="sxs-lookup"><span data-stu-id="048ca-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="048ca-112">Linux パスワードの再設定</span><span class="sxs-lookup"><span data-stu-id="048ca-112">Resetting your Linux password</span></span>

<span data-ttu-id="048ca-113">Linux ユーザー アカウントへのアクセス権があり、現在のパスワードを知っている場合は、そのディストリビューションの Linux パスワード再設定ツール (最も一般的なのは `passwd`) を使用して変更してください。</span><span class="sxs-lookup"><span data-stu-id="048ca-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="048ca-114">これを実行できない場合、ディストリビューションによっては、既定のユーザーを再設定することでパスワードを再設定できることがあります。</span><span class="sxs-lookup"><span data-stu-id="048ca-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="048ca-115">WSL では、WSL を開始するときに自動的にログインするユーザー アカウントを識別するための既定のユーザー タグが用意されています。</span><span class="sxs-lookup"><span data-stu-id="048ca-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="048ca-116">多くのディストリビューションには、既定のユーザーをルートに設定するコマンドや、パスワードが設定されていないルート ユーザーを設定するコマンドが含まれているため、既定のユーザーのルートへの変更は、パスワードの再設定などのための便利なツールになります。</span><span class="sxs-lookup"><span data-stu-id="048ca-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="048ca-117">Creators Update 以前の場合</span><span class="sxs-lookup"><span data-stu-id="048ca-117">For Creators Update and earlier</span></span>
<span data-ttu-id="048ca-118">Windows 10 Creators Update 以前を実行している場合は、次のコマンドを実行して既定の Bash ユーザーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="048ca-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="048ca-119">既定のユーザーを `root` に変更します。</span><span class="sxs-lookup"><span data-stu-id="048ca-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="048ca-120">`bash.exe` を実行して、今度は `root` としてログインします。</span><span class="sxs-lookup"><span data-stu-id="048ca-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="048ca-121">ディストリビューションのパスワード コマンドを使用してパスワードを再設定し、Linux コンソールを閉じます。</span><span class="sxs-lookup"><span data-stu-id="048ca-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="048ca-122">Windows CMD で、既定のユーザーを通常の Linux ユーザー アカウントに再設定して戻します。</span><span class="sxs-lookup"><span data-stu-id="048ca-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="048ca-123">Fall Creators Update 以降の場合</span><span class="sxs-lookup"><span data-stu-id="048ca-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="048ca-124">特定のディストリビューションで使用できるコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="048ca-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="048ca-125">たとえば、Ubuntu がインストールされているとします。</span><span class="sxs-lookup"><span data-stu-id="048ca-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="048ca-126">Ubuntu を使用したステップ バイ ステップの手順:</span><span class="sxs-lookup"><span data-stu-id="048ca-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="048ca-127">CMD を開きます。</span><span class="sxs-lookup"><span data-stu-id="048ca-127">Open CMD</span></span>
1. <span data-ttu-id="048ca-128">既定の Linux ユーザーを `root` に設定します。</span><span class="sxs-lookup"><span data-stu-id="048ca-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="048ca-129">Linux ディストリビューション (`ubuntu`) を起動します。</span><span class="sxs-lookup"><span data-stu-id="048ca-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="048ca-130">`root` として自動的にログインします。</span><span class="sxs-lookup"><span data-stu-id="048ca-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="048ca-131">`passwd` コマンドを使用してパスワードを再設定します。</span><span class="sxs-lookup"><span data-stu-id="048ca-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="048ca-132">Windows CMD で、既定のユーザーを通常の Linux ユーザー アカウントに再設定して戻します。</span><span class="sxs-lookup"><span data-stu-id="048ca-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="048ca-133">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="048ca-133">Permissions</span></span>

<span data-ttu-id="048ca-134">WSL のアクセス許可に関しては、留意すべき重要な概念が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="048ca-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="048ca-135">Windows アクセス許可モデルは、Windows リソースに対するプロセスの権限を管理します</span><span class="sxs-lookup"><span data-stu-id="048ca-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="048ca-136">Linux アクセス許可モデルは、Linux リソースに対するプロセスの権限を制御します</span><span class="sxs-lookup"><span data-stu-id="048ca-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="048ca-137">WSL で Linux を実行すると、Linux はそれを起動するプロセスと同じ Windows アクセス許可を持ちます。</span><span class="sxs-lookup"><span data-stu-id="048ca-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="048ca-138">Linux は、次の 2 つのアクセス許可レベルのいずれかで起動できます。</span><span class="sxs-lookup"><span data-stu-id="048ca-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="048ca-139">通常 (管理者特権でない):Linux は、ログインしているユーザーのアクセス許可を使用して実行されます</span><span class="sxs-lookup"><span data-stu-id="048ca-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="048ca-140">管理者特権/管理者:Linux は、管理者特権/管理者の Windows アクセス許可を使用して実行されます</span><span class="sxs-lookup"><span data-stu-id="048ca-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="048ca-141">昇格されたプロセスはシステム全体の設定やシステム全体にわたるデータまたは保護されているデータへのアクセスや変更が可能であり、結果として破損させる可能性があるため、Windows と Linux のどちらのアプリケーション/ツール/シェルであるかに関係なく、どうしても必要でない限りは昇格されたプロセスを起動**しないようにしてください**。</span><span class="sxs-lookup"><span data-stu-id="048ca-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="048ca-142">上記の Windows アクセス許可は、Linux インスタンス内のアクセス許可とは無関係です。Linux の "ルート権限" は、Linux 環境およびファイル システム内のユーザーの権限にのみ影響し、付与されている Windows 特権には影響しません。</span><span class="sxs-lookup"><span data-stu-id="048ca-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="048ca-143">したがって、(たとえば、`sudo` を使用して) Linux プロセスをルートとして実行すると、Linux 環境内でそのプロセス管理者権限のみが付与されます。</span><span class="sxs-lookup"><span data-stu-id="048ca-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="048ca-144">**例:**   </span><span class="sxs-lookup"><span data-stu-id="048ca-144">**Example:**  </span></span>  
<span data-ttu-id="048ca-145">Windows 管理特権がある Bash セッションでは `cd /mnt/c/Users/Administrator` にアクセスできる一方で、管理特権のない Bash セッションでは "アクセス許可が拒否されました" というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="048ca-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="048ca-146">Windows 内のアクセス許可は Windows によって管理されているため、Linux では、「`sudo cd /mnt/c/Users/Administrator`」と入力しても、管理者のディレクトリへのアクセス権が付与されません。</span><span class="sxs-lookup"><span data-stu-id="048ca-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="048ca-147">Linux アクセス許可モデルは、Linux 環境内で、ユーザーが現在の Linux ユーザーに基づいたアクセス許可を持っている場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="048ca-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="048ca-148">**例:**</span><span class="sxs-lookup"><span data-stu-id="048ca-148">**Example:**</span></span>  
<span data-ttu-id="048ca-149">sudo グループ内のユーザーは `sudo apt update` を実行できます。</span><span class="sxs-lookup"><span data-stu-id="048ca-149">A user in the sudo group may run `sudo apt update`.</span></span>
