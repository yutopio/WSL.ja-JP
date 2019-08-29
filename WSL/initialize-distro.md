---
title: 新しい WSL Linux ディストリビューションを初期化する
description: WSL 用の Linux ディストリビューションをインストールしたら、次の簡単な手順に従って初期化を完了します。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122715"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="ae0ca-104">新しくインストールされたディストリビューションの初期化</span><span class="sxs-lookup"><span data-stu-id="ae0ca-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="ae0ca-105">ディストリビューションをダウンロードしてインストールしたら、新しいディストリビューションの初期化を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="ae0ca-106">ディストリビューションを起動する</span><span class="sxs-lookup"><span data-stu-id="ae0ca-106">Launch a distro</span></span>
<span data-ttu-id="ae0ca-107">新しくインストールされたディストリビューションの初期化を完了するには、新しいインスタンスを起動します。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="ae0ca-108">これを行うには、Microsoft Store アプリの [起動] ボタンをクリックするか、[スタート] メニューから [ディストリビューション] を起動します。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="ae0ca-109">ヒント:最も頻繁に使用されるディストリビューションを [スタート] メニューやタスクバーにピン留めすることができます。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![[スタート] メニューからディストリビューションを起動する](media/start-menu.png)

> <span data-ttu-id="ae0ca-111">Windows Server では、ディストリビューションのインストールフォルダーから、ディストリビューション`<distro>.exe`のランチャー実行可能ファイルを起動できます。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="ae0ca-112">新しくインストールされたディストリビューションを初めて実行すると、コンソールウィンドウが開き、インストールが完了するまで 1 ~ 2 分待つように求められます。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="ae0ca-113">インストールのこの最終段階では、ディストリビューションのファイルが圧縮解除され、PC に保存され、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="ae0ca-114">PC の記憶装置のパフォーマンスによっては、約1分以上かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="ae0ca-115">この初期インストール段階は、ディストリビューションがクリーンインストールされている場合にのみ必要です。今後のすべての起動には1秒未満の時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="ae0ca-116">新しい Linux ユーザーアカウントの設定</span><span class="sxs-lookup"><span data-stu-id="ae0ca-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="ae0ca-117">インストールが完了すると、新しいユーザーアカウント (およびそのパスワード) を作成するように求められます。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

<span data-ttu-id="ae0ca-119">このユーザーアカウントは、通常の管理者以外のユーザーのために、ディストリビューションの起動時に既定でログインします。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="ae0ca-120">任意のユーザー名とパスワードを選択できます。 Windows ユーザー名には影響しません。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="ae0ca-121">新しいディストリビューションインスタンスを開いたときに、パスワードの入力を求められることはありませんが、を **`sudo`使用してプロセスを昇格する場合は、パスワードを入力する必要**があるため、覚えやすいパスワードを選択してください。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="ae0ca-122">詳細については、「[ユーザーサポート](user-support.md)」ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="ae0ca-123">ディストリビューションのパッケージを更新 & アップグレードする</span><span class="sxs-lookup"><span data-stu-id="ae0ca-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="ae0ca-124">ほとんどのディストリビューションには、空/最小のパッケージカタログが付属しています。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="ae0ca-125">パッケージカタログを定期的に更新し、ディストリビューションの優先パッケージマネージャーを使用して、インストールされているパッケージをアップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="ae0ca-126">Debian/Ubuntu では、apt を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="ae0ca-127">Linux ディストリビューションは、Windows によって自動的に更新またはアップグレードされません。これは、Linux ユーザーが自分で制御したいタスクです。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="ae0ca-128">これで完了です。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-128">You're done!</span></span> <span data-ttu-id="ae0ca-129">WSL で新しい Linux ディストリビューションをご利用いただけます。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="ae0ca-130">WSL の詳細については、他の[wsl ドキュメント](https://aka.ms/wsldocs)または[wsl learning のリソース](https://aka.ms/learnwsl)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![WSL で Linux を使用する](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="ae0ca-132">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ae0ca-132">Troubleshooting</span></span>

<span data-ttu-id="ae0ca-133">関連するエラーと修正案を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="ae0ca-134">その他の一般的なエラーとその解決策については、 [Wsl トラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="ae0ca-135">**エラー0x8007007e が発生し、インストールに失敗しました**このエラーは、システムがストアから Linux をサポートしていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="ae0ca-136">次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-136">Make sure that:</span></span>
> * <span data-ttu-id="ae0ca-137">Windows ビルド16215以降を実行しています。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="ae0ca-138">[ビルドを確認](troubleshooting.md#check-your-build-number)します。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="ae0ca-139">Windows Subsystem for Linux のオプションコンポーネントが有効になり、コンピューターが再起動されました。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="ae0ca-140">[WSL が有効になっていることを確認して](troubleshooting.md#confirm-wsl-is-enabled)ください。</span><span class="sxs-lookup"><span data-stu-id="ae0ca-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
