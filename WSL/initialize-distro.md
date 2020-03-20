---
title: 新しい WSL Linux ディストリビューションの初期化
description: WSL 用の Linux ディストリビューションをインストールしたら、次の簡単な手順に従って初期化を完了します
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c33d349a6d39c325b079ccbf7ed6350bed796e33
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269589"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="315b6-104">新しくインストールされたディストリビューションの初期化</span><span class="sxs-lookup"><span data-stu-id="315b6-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="315b6-105">ディストリビューションをダウンロードしてインストールしたら、新しいディストリビューションの初期化を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="315b6-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="315b6-106">ディストリビューションの起動</span><span class="sxs-lookup"><span data-stu-id="315b6-106">Launch a distro</span></span>
<span data-ttu-id="315b6-107">新しくインストールされたディストリビューションの初期化を完了するには、新しいインスタンスを起動します。</span><span class="sxs-lookup"><span data-stu-id="315b6-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="315b6-108">これを行うには、Microsoft Store アプリの [起動] ボタンをクリックするか、[スタート] メニューからそのディストリビューションを起動します。</span><span class="sxs-lookup"><span data-stu-id="315b6-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="315b6-109">ヒント:最も頻繁に使用するディストリビューションを [スタート] メニューやタスク バーにピン留めすることができます。</span><span class="sxs-lookup"><span data-stu-id="315b6-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![[スタート] メニューからディストリビューションを起動する](media/start-menu.png)

> <span data-ttu-id="315b6-111">Windows Server では、ディストリビューション インストール フォルダーから、ディストリビューションのランチャー実行可能ファイル `<distro>.exe` を起動できます。</span><span class="sxs-lookup"><span data-stu-id="315b6-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="315b6-112">新しくインストールされたディストリビューションを初めて実行すると、コンソール ウィンドウが開き、インストールが完了するまで 1、2 分待つように求められます。</span><span class="sxs-lookup"><span data-stu-id="315b6-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="315b6-113">インストールのこの最終段階で、ディストリビューションのファイルが圧縮解除されて PC に保存され、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="315b6-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="315b6-114">PC の記憶装置のパフォーマンスによっては、約 1 分またはそれ以上かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="315b6-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="315b6-115">この初回インストール段階は、ディストリビューションがクリーン インストールされる場合にのみ必要です。以降のすべての起動にかかる時間は 1 秒未満です。</span><span class="sxs-lookup"><span data-stu-id="315b6-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="315b6-116">新しい Linux ユーザー アカウントの設定</span><span class="sxs-lookup"><span data-stu-id="315b6-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="315b6-117">インストールが完了すると、新しいユーザー アカウント (およびそのパスワード) を作成するように求められます。</span><span class="sxs-lookup"><span data-stu-id="315b6-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

<span data-ttu-id="315b6-119">このユーザー アカウントは、ディストリビューションの起動時に既定でログインする、管理者以外の通常ユーザー用です。</span><span class="sxs-lookup"><span data-stu-id="315b6-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="315b6-120">任意のユーザー名とパスワードを選択できます。Windows ユーザー名と関係はありません。</span><span class="sxs-lookup"><span data-stu-id="315b6-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="315b6-121">新しいディストリビューション インスタンスを開いたときに、パスワードの入力は求められませんが、 **`sudo` を使用してプロセスを昇格する場合は、パスワードを入力する必要があるため**、必ず覚えやすいパスワードを選択してください。</span><span class="sxs-lookup"><span data-stu-id="315b6-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="315b6-122">詳細については、[ユーザー サポート](user-support.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="315b6-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="315b6-123">ディストリビューションのパッケージの更新とアップグレード</span><span class="sxs-lookup"><span data-stu-id="315b6-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="315b6-124">ほとんどのディストリビューションには、空または最小のパッケージ カタログが付属しています。</span><span class="sxs-lookup"><span data-stu-id="315b6-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="315b6-125">パッケージ カタログを定期的に更新し、ディストリビューションの推奨パッケージ マネージャーを使用して、インストールされているパッケージをアップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="315b6-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="315b6-126">Debian または Ubuntu では、apt を使用します。</span><span class="sxs-lookup"><span data-stu-id="315b6-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="315b6-127">Windows では、Linux ディストリビューションの更新やアップグレードは自動的に行われません。これは、Linux ユーザーが自分で制御することを好むタスクです。</span><span class="sxs-lookup"><span data-stu-id="315b6-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="315b6-128">これで完了です。</span><span class="sxs-lookup"><span data-stu-id="315b6-128">You're done!</span></span> <span data-ttu-id="315b6-129">WSL で新しい Linux ディストリビューションをご利用ください。</span><span class="sxs-lookup"><span data-stu-id="315b6-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="315b6-130">WSL の詳細については、他の [WSL ドキュメント](https://aka.ms/wsldocs)または[WSL の学習リソースのページ](https://aka.ms/learnwsl)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="315b6-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![WSL で Linux を使用する](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="315b6-132">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="315b6-132">Troubleshooting</span></span>

<span data-ttu-id="315b6-133">関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="315b6-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="315b6-134">その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="315b6-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="315b6-135">**エラー 0x8007007e が発生してインストールに失敗しました** このエラーは、ストアの Linux をシステムがサポートしていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="315b6-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="315b6-136">次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="315b6-136">Make sure that:</span></span>
> * <span data-ttu-id="315b6-137">Windows ビルド 16215 以降を実行している。</span><span class="sxs-lookup"><span data-stu-id="315b6-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="315b6-138">[ビルドを確認してください](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="315b6-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="315b6-139">Windows Subsystem for Linux オプション コンポーネントが有効になっていて、コンピューターが再起動されている。</span><span class="sxs-lookup"><span data-stu-id="315b6-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="315b6-140">[WSL が有効になっていることを確認してください](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="315b6-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
