---
title: Windows Subsystem for Linux (WSL) を Windows 10 にインストールする
description: Windows 10 での Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows, bash, wsl, windows, linux 用 windows サブシステム, windowssubsystem, ubuntu, debian, suse, windows 10, インストール, 有効にする, WSL2, バージョン 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 0f59fda8aa093487f09c1817acf47bd88eaae8cc
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336095"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="ea4ef-104">Windows 10 用 Windows Subsystem for Linux のインストール ガイド</span><span class="sxs-lookup"><span data-stu-id="ea4ef-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="ea4ef-105">Windows Subsystem for Linux のインストール</span><span class="sxs-lookup"><span data-stu-id="ea4ef-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="ea4ef-106">Windows 上に Linux ディストリビューションをインストールする前に、"Linux 用 Windows サブシステム" オプション機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-106">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="ea4ef-107">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-107">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="ea4ef-108">WSL 1 のみをインストールするには、お使いのマシンを再起動し、「[選択した Linux ディストリビューションをインストールする](./install-win10.md#install-your-linux-distribution-of-choice)」に進んでください。それ以外の場合は、再起動を待ってから WSL 2 への更新操作に進んでください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-108">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="ea4ef-109">詳細については、「[WSL 2 と WSL 1 の比較](./compare-versions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="ea4ef-110">WSL 2 に更新する</span><span class="sxs-lookup"><span data-stu-id="ea4ef-110">Update to WSL 2</span></span>

<span data-ttu-id="ea4ef-111">WSL 2 に更新するには、次の条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-111">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="ea4ef-112">[バージョン 2004](ms-settings:windowsupdate)、**ビルド 19041** 以上に更新された Windows 10 を実行している。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-112">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>

- <span data-ttu-id="ea4ef-113">Windows のバージョンを確認するには **Windows ロゴ キー + R** キーを押します。次に「**winver**」と入力し、 **[OK]** を選択します</span><span class="sxs-lookup"><span data-stu-id="ea4ef-113">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="ea4ef-114">(または、Windows コマンド プロンプトで `ver` コマンドを入力します)。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-114">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="ea4ef-115">お使いのビルドが 19041 より前の場合は、[最新の Windows バージョンに更新](ms-settings:windowsupdate)してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-115">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 19041.</span></span> <span data-ttu-id="ea4ef-116">[Windows 更新アシスタントを入手する](https://www.microsoft.com/software-download/windows10)。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-116">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="ea4ef-117">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="ea4ef-117">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="ea4ef-118">WSL 2 をインストールする前に、"仮想マシン プラットフォーム" オプション機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-118">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="ea4ef-119">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-119">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="ea4ef-120">お使いのマシンを**再起動**して WSL のインストールを完了し、WSL 2 に更新します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-120">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="ea4ef-121">WSL 2 を既定のバージョンとして設定する</span><span class="sxs-lookup"><span data-stu-id="ea4ef-121">Set WSL 2 as your default version</span></span>

<span data-ttu-id="ea4ef-122">PowerShell で次のコマンドを実行して、新しい Linux ディストリビューションをインストールするときに WSL 2 を既定のバージョンとして設定します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-122">Run the following command in PowerShell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="ea4ef-123">このメッセージは、コマンド `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel` を実行した後に表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-123">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="ea4ef-124">リンク ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) に従って、WSL 2 で使用する Linux カーネルをコンピューターにインストールするためのドキュメントのこのページから MSI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-124">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="ea4ef-125">カーネルをインストールしたら、コマンドを再度実行すると、メッセージが表示されることなく正常に完了します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-125">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="ea4ef-126">対象のディストリビューションのサイズによっては、WSL 1 から WSL 2 への更新が完了するまでに数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-126">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="ea4ef-127">Windows 10 Anniversary Update または Creators Update から WSL 1 の古い (レガシ) インストールを実行している場合は、更新エラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-127">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="ea4ef-128">次の手順に従って、[レガシ ディストリビューションをアンインストールして削除](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro)します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-128">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="ea4ef-129">選択した Linux ディストリビューションをインストールする</span><span class="sxs-lookup"><span data-stu-id="ea4ef-129">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="ea4ef-130">[Microsoft Store](https://aka.ms/wslstore) を開き、希望する Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-130">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Microsoft Store での Linux ディストリビューションの表示](media/store.png)

    <span data-ttu-id="ea4ef-132">次のリンクを使用すると、各ディストリビューションの Microsoft Store ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-132">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="ea4ef-133">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="ea4ef-133">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="ea4ef-134">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="ea4ef-134">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="ea4ef-135">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="ea4ef-135">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="ea4ef-136">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="ea4ef-136">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="ea4ef-137">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="ea4ef-137">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="ea4ef-138">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="ea4ef-138">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="ea4ef-139">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="ea4ef-139">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="ea4ef-140">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="ea4ef-140">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="ea4ef-141">WSL のための Fedora リミックス</span><span class="sxs-lookup"><span data-stu-id="ea4ef-141">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="ea4ef-142">Pengwin</span><span class="sxs-lookup"><span data-stu-id="ea4ef-142">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="ea4ef-143">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="ea4ef-143">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="ea4ef-144">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="ea4ef-144">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="ea4ef-145">ディストリビューションのページで、[入手] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-145">From the distribution's page, select "Get".</span></span>

    ![Microsoft Store での Linux ディストリビューション](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="ea4ef-147">新しいディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="ea4ef-147">Set up a new distribution</span></span>

<span data-ttu-id="ea4ef-148">新しくインストールした Linux ディストリビューションを初めて起動すると、コンソール ウィンドウが開き、ファイルが圧縮解除されて PC に格納されるまで 1、2 分待つように求められます。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-148">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="ea4ef-149">今後のすべての起動には、1 秒もかかりません。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-149">All future launches should take less than a second.</span></span>

<span data-ttu-id="ea4ef-150">次に、[新しい Linux ディストリビューションのユーザー アカウントとパスワードを作成する](./user-support.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-150">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="ea4ef-152">ディストリビューションのバージョンを WSL 1 または WSL 2 に設定する</span><span class="sxs-lookup"><span data-stu-id="ea4ef-152">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="ea4ef-153">インストールされている各 Linux ディストリビューションに割り当てられている WSL バージョンを確認するには、PowerShell コマンド ラインを開き、次のコマンドを入力します ([Windows ビルド 19041 以上](ms-settings:windowsupdate)でのみ使用可能): `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="ea4ef-153">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="ea4ef-154">ディストリビューションで使用される WSL のバージョンを設定するには、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-154">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="ea4ef-155">`<distribution name>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。`<versionNumber>` は、数字の "1" または "2" に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-155">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="ea4ef-156">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-156">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="ea4ef-157">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-157">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="ea4ef-158">これにより、インストールされるすべての新しいディストリビューションのバージョンが WSL 2 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-158">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="ea4ef-159">インストールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ea4ef-159">Troubleshooting installation</span></span>

<span data-ttu-id="ea4ef-160">関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-160">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="ea4ef-161">その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-161">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="ea4ef-162">**エラー 0x80070003 が発生してインストールに失敗しました**</span><span class="sxs-lookup"><span data-stu-id="ea4ef-162">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="ea4ef-163">Windows Subsystem for Linux はシステム ドライブ (通常、これは `C:` ドライブ) でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-163">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="ea4ef-164">ディストリビューションがシステム ドライブに格納されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-164">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="ea4ef-165">**[設定]** -> **[ストレージ]** -> **[その他のストレージ設定: 新しいコンテンツの保存先を変更する]** 
    を開きます。![C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="ea4ef-165">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="ea4ef-166">**WslRegisterDistribution failed with error 0x8007019e (エラー0x8007019e で WslRegisterDistribution が失敗しました)**</span><span class="sxs-lookup"><span data-stu-id="ea4ef-166">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="ea4ef-167">Windows Subsystem for Linux オプション コンポーネントが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-167">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="ea4ef-168">**[コントロール パネル]**  ->  **[プログラムと機能]**  ->  **[Windows の機能の有効化または無効化]** を開いて、 **[Linux 用 Windows サブシステム]** をチェックするか、またはこの記事の冒頭に記載した PowerShell コマンドレットを使用してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-168">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="ea4ef-169">**インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**</span><span class="sxs-lookup"><span data-stu-id="ea4ef-169">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="ea4ef-170">コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-170">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="ea4ef-171">これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-171">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="ea4ef-172">**アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="ea4ef-172">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="ea4ef-173">Linux 用 Windows サブシステムが有効になっていること、および Windows ビルド バージョン 19041 以降を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-173">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 19041 or higher.</span></span> <span data-ttu-id="ea4ef-174">WSL を有効にするには、PowerShell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-174">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="ea4ef-175">WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-175">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

- <span data-ttu-id="ea4ef-176">**仮想ディスク システムの制限があるため、要求された操作を完了できませんでした。仮想ハード ディスク ファイルは、圧縮と暗号化が解除されている必要があります。また、スパースにすることはできません。**</span><span class="sxs-lookup"><span data-stu-id="ea4ef-176">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="ea4ef-177">この問題の最新情報が追跡されている [WSL GitHub スレッド #4103](https://github.com/microsoft/WSL/issues/4103) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-177">Please check [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="ea4ef-178">**"wsl" という用語が、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。**</span><span class="sxs-lookup"><span data-stu-id="ea4ef-178">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="ea4ef-179">[Linux 用 Windows サブシステムのオプション コンポーネントがインストールされている](./install-win10.md#enable-the-virtual-machine-platform-optional-component)ことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-179">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="ea4ef-180">また、ARM64 デバイスを使用し、PowerShell からこのコマンドを実行している場合も、このエラーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-180">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="ea4ef-181">代わりに、`wsl.exe`PowerShell Core[ またはコマンド プロンプトから ](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) を実行します。</span><span class="sxs-lookup"><span data-stu-id="ea4ef-181">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
