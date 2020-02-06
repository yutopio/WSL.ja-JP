---
title: WSL ディストリビューションのユーザー アカウントを作成および更新する
description: Windows Subsystem for Linux を使用したユーザー アカウントとアクセス許可の管理のリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, ユーザー アカウント
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 30dea11adb68639f645ca800a695b0404661845a
ms.sourcegitcommit: e5fb773dd44abab7bcf289340da00f59528b88f7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "76973682"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a><span data-ttu-id="76385-104">WSL ディストリビューションのユーザー アカウントを作成および更新する</span><span class="sxs-lookup"><span data-stu-id="76385-104">Create and update user accounts for WSL distributions</span></span>

<span data-ttu-id="76385-105">WSL を有効にし、Microsoft Store から Linux ディストリビューションをインストールしたら、新しくインストールされた Linux ディストリビューションを開くときに最初に実行する必要がある手順は、**ユーザー名**および**パスワード**を含むアカウントを作成することです。</span><span class="sxs-lookup"><span data-stu-id="76385-105">Once you have enabled WSL and installed a Linux distribution from the Microsoft Store, the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="76385-106">この**ユーザー名**および**パスワード**は、お使いの Linux ディストリビューションに固有であり、Windows ユーザー名とは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="76385-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="76385-107">この**ユーザー名**および**パスワード**を作成すると、このアカウントがディストリビューションの既定のユーザーとなり、起動時に自動的にサインインされます。</span><span class="sxs-lookup"><span data-stu-id="76385-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="76385-108">このアカウントは、Linux 管理者と見なされ、`sudo` (Super User Do) 管理コマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="76385-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="76385-109">Windows Subsystem for Linux で実行されている各 Linux ディストリビューションには、独自の Linux ユーザー アカウントとパスワードがあります。</span><span class="sxs-lookup"><span data-stu-id="76385-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="76385-110">ディストリビューションの追加、再インストール、再設定を行うたびに、Linux ユーザー アカウントを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76385-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="76385-111">Linux パスワードの再設定</span><span class="sxs-lookup"><span data-stu-id="76385-111">Reset your Linux password</span></span>

<span data-ttu-id="76385-112">パスワードを変更するには、Linux ディストリビューション (Ubuntu など) を開き、コマンド `passwd` を入力します。</span><span class="sxs-lookup"><span data-stu-id="76385-112">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="76385-113">現在のパスワードを入力するよう求められ、新しいパスワードの入力を求められたら、新しいパスワードを確認します。</span><span class="sxs-lookup"><span data-stu-id="76385-113">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

### <a name="forgot-your-password"></a><span data-ttu-id="76385-114">パスワードを忘れた場合</span><span class="sxs-lookup"><span data-stu-id="76385-114">Forgot your password</span></span>

<span data-ttu-id="76385-115">Linux ディストリビューションのパスワードを忘れた場合は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="76385-115">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="76385-116">PowerShell を開き、コマンド `wsl -u root` を使用して、既定の WSL ディストリビューションのルートを入力します。</span><span class="sxs-lookup"><span data-stu-id="76385-116">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

> <span data-ttu-id="76385-117">既定ではないディストリビューションで忘れたパスワードを更新する必要がある場合は、コマンド `wsl -d Debian -u root` を使用します。`Debian` は対象のディストリビューション名に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="76385-117">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="76385-118">PowerShell 内のルート レベルで WSL ディストリビューションが開かれたら、コマンド `passwd` を使用してパスワードを更新できます。</span><span class="sxs-lookup"><span data-stu-id="76385-118">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="76385-119">新しい UNIX パスワードを入力し、そのパスワードを確認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="76385-119">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="76385-120">パスワードが正常に更新されたことを示す通知が表示されたら、コマンド `exit` を使用して PowerShell 内の WSL を閉じます。</span><span class="sxs-lookup"><span data-stu-id="76385-120">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="76385-121">古いバージョン (1703 (Creators Update) または 1709 (Fall Creators Update) など) の Windows オペレーティング システムを実行している場合、[アーカイブされたバージョンのこのユーザー アカウントの更新に関するドキュメント](./user-support-archived.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76385-121">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
