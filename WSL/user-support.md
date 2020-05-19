---
title: Linux ディストリビューションのユーザー アカウントを作成および更新する
description: Windows Subsystem for Linux を使用したユーザー アカウントとアクセス許可の管理のリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, ユーザー アカウント
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 551cc66b1648a66717163d1d8e19a78d28bff342
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235910"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a><span data-ttu-id="eb8cb-104">新しい Linux ディストリビューションのユーザー アカウントとパスワードを作成する</span><span class="sxs-lookup"><span data-stu-id="eb8cb-104">Create a user account and password for your new Linux distribution</span></span>

<span data-ttu-id="eb8cb-105">[WSL を有効にし、Microsoft Store から Linux ディストリビューションをインストール](./install-win10.md)したら、新しくインストールされた Linux ディストリビューションを開くときに最初に実行する必要がある手順は、**ユーザー名**および**パスワード**を含むアカウントを作成することです。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-105">Once you have [enabled WSL and installed a Linux distribution from the Microsoft Store](./install-win10.md), the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="eb8cb-106">この**ユーザー名**および**パスワード**は、お使いの Linux ディストリビューションに固有であり、Windows ユーザー名とは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="eb8cb-107">この**ユーザー名**および**パスワード**を作成すると、このアカウントがディストリビューションの既定のユーザーとなり、起動時に自動的にサインインされます。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="eb8cb-108">このアカウントは、Linux 管理者と見なされ、`sudo` (Super User Do) 管理コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="eb8cb-109">Windows Subsystem for Linux で実行されている各 Linux ディストリビューションには、独自の Linux ユーザー アカウントとパスワードがあります。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="eb8cb-110">ディストリビューションの追加、再インストール、再設定を行うたびに、Linux ユーザー アカウントを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a><span data-ttu-id="eb8cb-112">パッケージの更新とアップグレード</span><span class="sxs-lookup"><span data-stu-id="eb8cb-112">Update and upgrade packages</span></span>

<span data-ttu-id="eb8cb-113">ほとんどのディストリビューションには、空または最小のパッケージ カタログが付属しています。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-113">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="eb8cb-114">パッケージ カタログを定期的に更新し、ディストリビューションの推奨パッケージ マネージャーを使用して、インストールされているパッケージをアップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-114">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distribution's preferred package manager.</span></span> <span data-ttu-id="eb8cb-115">Debian または Ubuntu では、apt を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-115">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="eb8cb-116">Windows では、Linux ディストリビューションの更新やアップグレードは自動的に行われません。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-116">Windows does not automatically update or upgrade your Linux distribution(s).</span></span> <span data-ttu-id="eb8cb-117">これは、ほとんどの Linux ユーザーが自分で制御することを好むタスクです。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-117">This is a task that the most Linux users prefer to control themselves.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="eb8cb-118">Linux パスワードの再設定</span><span class="sxs-lookup"><span data-stu-id="eb8cb-118">Reset your Linux password</span></span>

<span data-ttu-id="eb8cb-119">パスワードを変更するには、Linux ディストリビューション (Ubuntu など) を開き、コマンド `passwd` を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-119">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="eb8cb-120">現在のパスワードを入力するよう求められ、新しいパスワードの入力を求められたら、新しいパスワードを確認します。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-120">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

## <a name="forgot-your-password"></a><span data-ttu-id="eb8cb-121">パスワードを忘れた場合</span><span class="sxs-lookup"><span data-stu-id="eb8cb-121">Forgot your password</span></span>

<span data-ttu-id="eb8cb-122">Linux ディストリビューションのパスワードを忘れた場合は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-122">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="eb8cb-123">PowerShell を開き、コマンド `wsl -u root` を使用して、既定の WSL ディストリビューションのルートを入力します。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-123">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

    > <span data-ttu-id="eb8cb-124">既定ではないディストリビューションで忘れたパスワードを更新する必要がある場合は、コマンド `wsl -d Debian -u root` を使用します。`Debian` は対象のディストリビューション名に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-124">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="eb8cb-125">PowerShell 内のルート レベルで WSL ディストリビューションが開かれたら、コマンド `passwd` を使用してパスワードを更新できます。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-125">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="eb8cb-126">新しい UNIX パスワードを入力し、そのパスワードを確認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-126">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="eb8cb-127">パスワードが正常に更新されたことを示す通知が表示されたら、コマンド `exit` を使用して PowerShell 内の WSL を閉じます。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-127">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="eb8cb-128">古いバージョン (1703 (Creators Update) または 1709 (Fall Creators Update) など) の Windows オペレーティング システムを実行している場合、[アーカイブされたバージョンのこのユーザー アカウントの更新に関するドキュメント](./user-support-archived.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb8cb-128">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
