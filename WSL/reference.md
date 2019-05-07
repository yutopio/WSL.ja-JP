---
title: Linux コマンド リファレンス用 Windows サブシステム
description: Linux 用 Windows サブシステムを管理するコマンドの一覧
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu 用 windows サブシステム
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063580"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="0d54f-104">Windows Subsystem for Linux のコマンド リファレンス</span><span class="sxs-lookup"><span data-stu-id="0d54f-104">Command Reference for Windows Subsystem for Linux</span></span>

> <span data-ttu-id="0d54f-105">`lxrun.exe` Windows 10 1803 の時点で非推奨以降。</span><span class="sxs-lookup"><span data-stu-id="0d54f-105">`lxrun.exe` is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="0d54f-106">コマンドは、`lxrun.exe`と対話するために使用できる、 [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)直接します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-106">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="0d54f-107">これらのコマンドにインストールされている、`\Windows\System32`ディレクトリ内での Windows コマンド プロンプトまたは PowerShell で実行する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0d54f-107">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

* <span data-ttu-id="0d54f-108">`lxrun.exe` WSL の管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d54f-108">`lxrun.exe` is used to manage WSL.</span></span>  <span data-ttu-id="0d54f-109">このコマンドは、インストールまたはアンインストールの Ubuntu イメージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d54f-109">This command can be used to install or uninstall the Ubuntu image.</span></span>


| <span data-ttu-id="0d54f-110">コマンド</span><span class="sxs-lookup"><span data-stu-id="0d54f-110">Command</span></span>                     | <span data-ttu-id="0d54f-111">説明</span><span class="sxs-lookup"><span data-stu-id="0d54f-111">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `bash`                      | <span data-ttu-id="0d54f-112">現在のディレクトリに Bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-112">Launches the Bash shell in the current directory.</span></span>  <span data-ttu-id="0d54f-113">Bash シェルが自動的にインストールされていない場合の実行します。 `lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="0d54f-113">If the Bash shell is not installed automatically runs `lxrun /install`</span></span> |
| `bash ~`                    | <span data-ttu-id="0d54f-114">Ubuntu のユーザーのホーム ディレクトリには、bash シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-114">Launches the bash shell into the user's Ubuntu home directory.</span></span>  <span data-ttu-id="0d54f-115">Cd の実行に似て ~</span><span class="sxs-lookup"><span data-stu-id="0d54f-115">Similar to running cd ~</span></span>            |
| `bash -c "<command>"`       | <span data-ttu-id="0d54f-116">コマンドを実行して、出力を印刷し、Windows コマンド プロンプトに終了します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-116">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="0d54f-117">例: **-c"ls"の bash**</span><span class="sxs-lookup"><span data-stu-id="0d54f-117">Example:  **bash -c "ls"**</span></span> |

<p>

| <span data-ttu-id="0d54f-118">コマンド</span><span class="sxs-lookup"><span data-stu-id="0d54f-118">Command</span></span>                     | <span data-ttu-id="0d54f-119">説明</span><span class="sxs-lookup"><span data-stu-id="0d54f-119">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="0d54f-120">Lxrun コマンドは、WSL インスタンスの管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d54f-120">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="0d54f-121">ダウンロードを開始し、プロセスをインストールします。</span><span class="sxs-lookup"><span data-stu-id="0d54f-121">Starts the download and install process.</span></span> <br/> <span data-ttu-id="0d54f-122">**/y**はすべてのプロンプトのバイパスに追加できます。</span><span class="sxs-lookup"><span data-stu-id="0d54f-122">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="0d54f-123">確認プロンプトが自動的に受け入れられるし、既定のユーザーがルートに設定されています。</span><span class="sxs-lookup"><span data-stu-id="0d54f-123">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="0d54f-124">アンインストールし、Ubuntu イメージを削除します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-124">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="0d54f-125">既定ではこれは、ユーザーの Ubuntu のホーム ディレクトリを削除されません。</span><span class="sxs-lookup"><span data-stu-id="0d54f-125">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="0d54f-126">**/y**自動的に確認のプロンプトを受け入れるように追加することがあります</span><span class="sxs-lookup"><span data-stu-id="0d54f-126">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="0d54f-127">**完全/** をアンインストールし、ユーザーの Ubuntu のホーム ディレクトリを削除します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-127">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="0d54f-128">Ubuntu のユーザーには、既定の Bash を設定します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-128">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="0d54f-129">指定したユーザーが存在しない場合、パスワードを求められます。</span><span class="sxs-lookup"><span data-stu-id="0d54f-129">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="0d54f-130">詳細については、次を参照してください。:https://aka.ms/wslusersします。</span><span class="sxs-lookup"><span data-stu-id="0d54f-130">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="0d54f-131">**/y**パスワードのバイパス promping します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-131">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="0d54f-132">パスワードを指定せず、ユーザーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0d54f-132">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="0d54f-133">サブシステムのパッケージのインデックスを更新します。</span><span class="sxs-lookup"><span data-stu-id="0d54f-133">Updates the subsystem's package index</span></span>          |
