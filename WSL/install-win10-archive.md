---
title: Windows Subsystem for Linux (WSL) を Windows 10 にインストールする
description: Windows 10 での Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6ed12ba9d63d3f4038b67489035e13113a372928
ms.sourcegitcommit: 9f12e168b80775cd967f22f97376e51043c3667e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/02/2020
ms.locfileid: "84301203"
---
# <a name="install-windows-subsystem-for-linux"></a><span data-ttu-id="98a69-104">Linux 用 Windows サブシステムをインストールする</span><span class="sxs-lookup"><span data-stu-id="98a69-104">Install Windows Subsystem for Linux</span></span>

<span data-ttu-id="98a69-105">次のガイドでは、Windows 10 を実行しているコンピューターに Linux 用 Windows サブシステム (WSL) をインストールするために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="98a69-105">The following guide will walk through the steps required to install the Windows Subsystem for Linux (WSL) on a computer running Windows 10.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a><span data-ttu-id="98a69-106">Linux 用 Windows サブシステム オプション機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="98a69-106">Enable the Windows Subsystem for Linux optional feature</span></span>

<span data-ttu-id="98a69-107">Linux ディストリビューションをインストールする前に、Windows 10 上で "Linux 用 Windows サブシステム" オプション機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98a69-107">Before installing a Linux distribution, you must enable the "Windows Subsystem for Linux" optional feature on Windows 10:</span></span>

1. <span data-ttu-id="98a69-108">管理者として PowerShell を開き、このスクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="98a69-108">Open PowerShell as Administrator and enter this script:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. <span data-ttu-id="98a69-109">メッセージが表示されたら、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="98a69-109">Restart your computer when prompted.</span></span>

## <a name="install-a-linux-distribution"></a><span data-ttu-id="98a69-110">Linux ディストリビューションをインストールする</span><span class="sxs-lookup"><span data-stu-id="98a69-110">Install a Linux distribution</span></span>

<span data-ttu-id="98a69-111">推奨される Linux ディストリビューションをダウンロードしてインストールするには、3 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="98a69-111">There are three ways to download and install your preferred Linux distribution(s):</span></span>

- <span data-ttu-id="98a69-112">Microsoft Store からダウンロードしてインストールする (下記参照)</span><span class="sxs-lookup"><span data-stu-id="98a69-112">Download and install from the Microsoft Store (see below)</span></span>
- [<span data-ttu-id="98a69-113">コマンド ラインからダウンロードして手動でインストールする</span><span class="sxs-lookup"><span data-stu-id="98a69-113">Download and manually install from command line</span></span>](install-manual.md)
- [<span data-ttu-id="98a69-114">Windows Server へのインストール</span><span class="sxs-lookup"><span data-stu-id="98a69-114">Install on Windows Server</span></span>](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a><span data-ttu-id="98a69-115">Microsoft Store からのインストール</span><span class="sxs-lookup"><span data-stu-id="98a69-115">Install from the Microsoft Store</span></span>

<span data-ttu-id="98a69-116">Linux ディストリビューションは、Windows 10 の Microsoft Store (Build 16215+) からインストールできます。</span><span class="sxs-lookup"><span data-stu-id="98a69-116">Linux distributions can be installed from the Microsoft Store on Windows 10 (Build 16215+).</span></span>

> [!NOTE]
> <span data-ttu-id="98a69-117">これらの手順に従って、[Windows 10 のビルド番号を確認](troubleshooting.md#check-your-build-number)します。</span><span class="sxs-lookup"><span data-stu-id="98a69-117">Follow these steps to [check your Windows 10 build number](troubleshooting.md#check-your-build-number).</span></span>

1. <span data-ttu-id="98a69-118">Microsoft Store を開き、希望する Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="98a69-118">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store の Linux ディストリビューションのビュー](media/store.png)

    <span data-ttu-id="98a69-120">次のリンクを使用すると、各ディストリビューションの Microsoft Store ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="98a69-120">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="98a69-121">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="98a69-121">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="98a69-122">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="98a69-122">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="98a69-123">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="98a69-123">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [<span data-ttu-id="98a69-124">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="98a69-124">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [<span data-ttu-id="98a69-125">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="98a69-125">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [<span data-ttu-id="98a69-126">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="98a69-126">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [<span data-ttu-id="98a69-127">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="98a69-127">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="98a69-128">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="98a69-128">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="98a69-129">WSL のための Fedora リミックス</span><span class="sxs-lookup"><span data-stu-id="98a69-129">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="98a69-130">Pengwin</span><span class="sxs-lookup"><span data-stu-id="98a69-130">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="98a69-131">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="98a69-131">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="98a69-132">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="98a69-132">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="98a69-133">[取得] を選択し、ディストリビューションのダウンロードが完了したら、[起動] を選択します。</span><span class="sxs-lookup"><span data-stu-id="98a69-133">Select "Get" and once the distribution has finished downloading, select "Launch".</span></span>

    ![Microsoft Store の Linux ディストリビューションのビュー](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="98a69-135">ディストリビューションの初期化を完了する</span><span class="sxs-lookup"><span data-stu-id="98a69-135">Complete initialization of your distro</span></span>

<span data-ttu-id="98a69-136">Linux ディストリビューションを起動したら、画面の指示に従って、ディストリビューションを初期化します。</span><span class="sxs-lookup"><span data-stu-id="98a69-136">After launching your Linux distribution, follow the onscreen instructions to initialize your distro.</span></span>

> [!NOTE]
> <span data-ttu-id="98a69-137">Windows Server の場合は、インストール フォルダーにある実行可能ファイル (`<distro>.exe`) を使用してディストリビューションを起動します。</span><span class="sxs-lookup"><span data-stu-id="98a69-137">For Windows Server, launch your distribution using the executable, `<distro>.exe`, in the installation folder.</span></span>

<span data-ttu-id="98a69-138">新しくインストールされたディストリビューションを初めて実行すると、コンソール ウィンドウが開き、インストールが完了するまで 1、2 分待つように求められます。</span><span class="sxs-lookup"><span data-stu-id="98a69-138">The first time a newly installed distribution runs, a console window will open and you'll be asked to wait for a minute or two for the installation to complete.</span></span> <span data-ttu-id="98a69-139">インストールのこの最終段階で、ディストリビューションのファイルが圧縮解除されて PC に保存され、使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="98a69-139">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="98a69-140">PC の記憶装置のパフォーマンスによっては、約 1 分またはそれ以上かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="98a69-140">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="98a69-141">この初回インストール段階は、ディストリビューションがクリーン インストールされる場合にのみ必要です。以降のすべての起動にかかる時間は 1 秒未満です。</span><span class="sxs-lookup"><span data-stu-id="98a69-141">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="set-up-a-new-linux-user-account"></a><span data-ttu-id="98a69-142">新しい Linux ユーザー アカウントの設定</span><span class="sxs-lookup"><span data-stu-id="98a69-142">Set up a new Linux user account</span></span>

<span data-ttu-id="98a69-143">インストールが完了すると、新しいユーザー アカウント (およびそのパスワード) を作成するように求められます。</span><span class="sxs-lookup"><span data-stu-id="98a69-143">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

<span data-ttu-id="98a69-145">このユーザー アカウントは、ディストリビューションの起動時に既定でログインする、管理者以外の通常ユーザー用です。</span><span class="sxs-lookup"><span data-stu-id="98a69-145">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span> <span data-ttu-id="98a69-146">任意のユーザー名とパスワードを選択できます。Windows ユーザー名と関係はありません。</span><span class="sxs-lookup"><span data-stu-id="98a69-146">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="98a69-147">新しいディストリビューション インスタンスを開いたときに、パスワードの入力は求められませんが、 **`sudo` を使用してプロセスを昇格する場合は、パスワードを入力する必要があるため**、必ず覚えやすいパスワードを選択してください。</span><span class="sxs-lookup"><span data-stu-id="98a69-147">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="98a69-148">詳細については、[ユーザー サポート](user-support.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="98a69-148">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-packages"></a><span data-ttu-id="98a69-149">パッケージの更新とアップグレード</span><span class="sxs-lookup"><span data-stu-id="98a69-149">Update & upgrade packages</span></span>

<span data-ttu-id="98a69-150">ほとんどのディストリビューションには、空または最小のパッケージ カタログが付属しています。</span><span class="sxs-lookup"><span data-stu-id="98a69-150">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="98a69-151">パッケージ カタログを定期的に更新し、ディストリビューションの推奨パッケージ マネージャーを使用して、インストールされているパッケージをアップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98a69-151">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="98a69-152">Debian または Ubuntu では、apt を使用します。</span><span class="sxs-lookup"><span data-stu-id="98a69-152">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="98a69-153">Windows では、Linux ディストリビューションの更新やアップグレードは自動的に行われません。</span><span class="sxs-lookup"><span data-stu-id="98a69-153">Windows does not automatically update or upgrade your Linux distro(s).</span></span> <span data-ttu-id="98a69-154">これは、ほとんどの Linux ユーザーが自分で制御することを好むタスクです。</span><span class="sxs-lookup"><span data-stu-id="98a69-154">This is a task that the most Linux users prefer to control themselves.</span></span>

<span data-ttu-id="98a69-155">WSL で新しい Linux ディストリビューションをご利用ください。</span><span class="sxs-lookup"><span data-stu-id="98a69-155">Enjoy using your new Linux distro on WSL!</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="98a69-156">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="98a69-156">Troubleshooting</span></span>

<span data-ttu-id="98a69-157">関連インストール エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="98a69-157">Below are related installation errors and suggested fixes.</span></span> <span data-ttu-id="98a69-158">その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98a69-158">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

### <a name="installation-failed-with-error-0x8007007e"></a><span data-ttu-id="98a69-159">エラー 0x8007007e が発生してインストールに失敗しました</span><span class="sxs-lookup"><span data-stu-id="98a69-159">Installation failed with error 0x8007007e</span></span>

<span data-ttu-id="98a69-160">このエラーは、ストアからの Linux がサポートされていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="98a69-160">This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="98a69-161">次のことを確認します。</span><span class="sxs-lookup"><span data-stu-id="98a69-161">Make sure that:</span></span>

- <span data-ttu-id="98a69-162">Windows ビルド 16215 以降を実行している。</span><span class="sxs-lookup"><span data-stu-id="98a69-162">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="98a69-163">[ビルドを確認してください](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="98a69-163">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
- <span data-ttu-id="98a69-164">Windows Subsystem for Linux オプション コンポーネントが有効になっていて、コンピューターが再起動されている。</span><span class="sxs-lookup"><span data-stu-id="98a69-164">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="98a69-165">[WSL が有効になっていることを確認してください](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="98a69-165">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>

### <a name="installation-failed-with-error-0x80070003"></a><span data-ttu-id="98a69-166">エラー 0x80070003 が発生してインストールに失敗しました</span><span class="sxs-lookup"><span data-stu-id="98a69-166">Installation failed with error 0x80070003</span></span>

<span data-ttu-id="98a69-167">Windows Subsystem for Linux はシステム ドライブ (通常、これは `C:` ドライブ) でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="98a69-167">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="98a69-168">ディストリビューションがシステム ドライブに格納されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="98a69-168">Make sure that distros are stored on your system drive:</span></span>

- <span data-ttu-id="98a69-169">**[設定]**  ->  **[ストレージ]**  ->  **[その他のストレージ設定:新しいコンテンツの保存先を変更する]** を開きます</span><span class="sxs-lookup"><span data-stu-id="98a69-169">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**</span></span>
  
    ![C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a><span data-ttu-id="98a69-171">WslRegisterDistribution failed with error 0x8007019e (エラー 0x8007019e で WslRegisterDistribution が失敗しました)</span><span class="sxs-lookup"><span data-stu-id="98a69-171">WslRegisterDistribution failed with error 0x8007019e</span></span>

<span data-ttu-id="98a69-172">Windows Subsystem for Linux オプション コンポーネントが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="98a69-172">The Windows Subsystem for Linux optional component is not enabled:</span></span>

- <span data-ttu-id="98a69-173">**[コントロール パネル]**  ->  **[プログラムと機能]**  ->  **[Windows の機能の有効化または無効化]** を開いて、 **[Windows Subsystem for Linux]** をチェックするか、またはこの記事の冒頭に記載した PowerShell コマンドレットを使用して有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="98a69-173">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
