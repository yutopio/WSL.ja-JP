---
title: 新しい WSL Linux ディストリビューションを初期化します。
description: WSL の Linux ディストリビューションをインストールした後、次の簡単な手順に従って初期化を完了します
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステム
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902049"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="f5e8b-104">新しくインストールされたディストリビューションの初期化</span><span class="sxs-lookup"><span data-stu-id="f5e8b-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="f5e8b-105">ディストリビューションをダウンロードしてインストールすると、新しいディストリビューションの初期化を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="f5e8b-106">ディストリビューションを起動します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-106">Launch a distro</span></span>
<span data-ttu-id="f5e8b-107">を、新しくインストールされたディストリビューションの初期化を完了するには、新しいインスタンスを起動します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="f5e8b-108">Windows ストア アプリでは、「起動」ボタンをクリックするか、[スタート] メニューからディストリビューションを起動して、これを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="f5e8b-109">ヒント:最もよく使用されるディストリビューションに、[スタート] メニューやタスク バーにピン留めすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![[スタート] メニューからディストリビューションを起動します。](media/start-menu.png)

> <span data-ttu-id="f5e8b-111">Windows Server で、実行可能ファイル、ディストリビューションのランチャーを起動できます`<distro>.exe`ディストリビューションのインストール フォルダーから。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="f5e8b-112">最初に、新しくインストールされたディストリビューションで、実行、ウィンドウが開き、コンソールと、インストールが完了するは、2 分の待機を求められます。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="f5e8b-113">インストールのこの最終ステージ中にディストリビューションのファイルが圧縮解除され、使用できるように、PC に保存されています。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="f5e8b-114">これは、に関するお客様の PC の記憶装置のパフォーマンスによっては 1 分以上かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="f5e8b-115">この最初のインストール フェーズは、ディストリビューションのクリーンアップ-installed - ときに必要なすべてから起動は 1 秒未満を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="f5e8b-116">新しい Linux ユーザー アカウントを設定します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="f5e8b-117">インストールが完了するとは、新しいユーザー アカウント (とそのパスワード) を作成する促されます。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows コンソールでアンパック Ubuntu](media/UbuntuInstall.png)

<span data-ttu-id="f5e8b-119">このユーザー アカウントである必要が通常の非管理者ユーザーのしますのログインとして既定では、ディストリビューションを起動するときにします。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="f5e8b-120">任意のユーザー名とパスワードを選択することができます - Windows ユーザー名に影響があるありません。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="f5e8b-121">ディストリビューションの新しいインスタンスを開くと、求められませんをパスワードが**プロセスを使用して、昇格する場合`sudo`、パスワードを入力する必要があります**ので、簡単に覚えやすいパスワードを選択することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="f5e8b-122">参照してください、[ユーザー サポート](user-support.md)詳細については、ページ。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="f5e8b-123">更新 (&)、ディストリビューションのパッケージのアップグレード</span><span class="sxs-lookup"><span data-stu-id="f5e8b-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="f5e8b-124">ほとんどのディストリビューションは、空または最小のパッケージのカタログで出荷されます。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="f5e8b-125">パッケージのカタログを定期的に更新し、ディストリビューションの推奨されるパッケージ マネージャーを使用して、インストールされているパッケージのアップグレードを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="f5e8b-126">Debian または Ubuntu 上には、apt が使用します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="f5e8b-127">Windows の更新またはアップグレード、Linux distro(s) は自動的に。これは、Linux ユーザーが自身を制御する優先するタスクです。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="f5e8b-128">これで完了です。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-128">You're done!</span></span> <span data-ttu-id="f5e8b-129">WSL で、新しい Linux ディストリビューションを使用してお楽しみください!</span><span class="sxs-lookup"><span data-stu-id="f5e8b-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="f5e8b-130">WSL の詳細については、他の確認[WSL docs](https://aka.ms/wsldocs)、または[WSL 学習リソース ページ](https://aka.ms/learnwsl)します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![WSL で Linux を使用してお楽しみください。](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="f5e8b-132">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f5e8b-132">Troubleshooting</span></span>

<span data-ttu-id="f5e8b-133">関連するエラーと推奨される修正方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="f5e8b-134">参照してください、 [WSL のトラブルシューティング ページ](troubleshooting.md)の他の一般的なエラーとその解決方法。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="f5e8b-135">**インストールに失敗しましたエラー 0x8007007e**システムがストアからの Linux をサポートしない場合、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="f5e8b-136">次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-136">Make sure that:</span></span>
> * <span data-ttu-id="f5e8b-137">16215 またはそれ以降は、Windows ビルドを実行しています。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="f5e8b-138">[ビルド確認](troubleshooting.md#check-your-build-number)します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="f5e8b-139">Linux の省略可能なコンポーネント用 Windows サブシステムが有効になっており、コンピューターが再起動します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="f5e8b-140">[WSL が有効になっていることを確認](troubleshooting.md#confirm-wsl-is-enabled)します。</span><span class="sxs-lookup"><span data-stu-id="f5e8b-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
