---
title: Windows Subsystem for Linux (WSL) を Windows 10 にインストールする
description: Windows 10 での Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows, bash, wsl, windows, linux 用 windows サブシステム, windowssubsystem, ubuntu, debian, suse, windows 10, インストール, 有効にする, WSL2, バージョン 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 73e3b982cd29558fdc86bd499f9a4c51a9d22e83
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948696"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="a1efb-104">Windows 10 用 Windows Subsystem for Linux のインストール ガイド</span><span class="sxs-lookup"><span data-stu-id="a1efb-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="a1efb-105">Windows Subsystem for Linux のインストール</span><span class="sxs-lookup"><span data-stu-id="a1efb-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="a1efb-106">Windows 上に Linux ディストリビューションをインストールする前に、"Linux 用 Windows サブシステム" オプション機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-106">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="a1efb-107">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-107">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="a1efb-108">WSL 1 のみをインストールするには、お使いのマシンを再起動し、「[選択した Linux ディストリビューションをインストールする](./install-win10.md#install-your-linux-distribution-of-choice)」に進んでください。それ以外の場合は、再起動を待ってから WSL 2 への更新操作に進んでください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-108">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="a1efb-109">詳細については、「[WSL 2 と WSL 1 の比較](./compare-versions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="a1efb-110">WSL 2 に更新する</span><span class="sxs-lookup"><span data-stu-id="a1efb-110">Update to WSL 2</span></span>

<span data-ttu-id="a1efb-111">WSL 2 に更新するには、次の条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-111">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="a1efb-112">[バージョン 2004](ms-settings:windowsupdate)、**ビルド 19041** 以上に更新された Windows 10 を実行している。</span><span class="sxs-lookup"><span data-stu-id="a1efb-112">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>

- <span data-ttu-id="a1efb-113">Windows のバージョンを確認するには **Windows ロゴ キー + R** キーを押します。次に「**winver**」と入力し、 **[OK]** を選択します</span><span class="sxs-lookup"><span data-stu-id="a1efb-113">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="a1efb-114">(または、Windows コマンド プロンプトで `ver` コマンドを入力します)。</span><span class="sxs-lookup"><span data-stu-id="a1efb-114">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="a1efb-115">お使いのビルドが 19041 より前の場合は、[最新の Windows バージョンに更新](ms-settings:windowsupdate)してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-115">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 19041.</span></span> <span data-ttu-id="a1efb-116">[Windows 更新アシスタントを入手する](https://www.microsoft.com/software-download/windows10)。</span><span class="sxs-lookup"><span data-stu-id="a1efb-116">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="a1efb-117">"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする</span><span class="sxs-lookup"><span data-stu-id="a1efb-117">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="a1efb-118">WSL 2 をインストールする前に、"仮想マシン プラットフォーム" オプション機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-118">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="a1efb-119">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-119">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="a1efb-120">お使いのマシンを**再起動**して WSL のインストールを完了し、WSL 2 に更新します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-120">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="a1efb-121">WSL 2 を既定のバージョンとして設定する</span><span class="sxs-lookup"><span data-stu-id="a1efb-121">Set WSL 2 as your default version</span></span>

<span data-ttu-id="a1efb-122">管理者として PowerShell を開いて次のコマンドを実行し、新しい Linux ディストリビューションをインストールする際の既定のバージョンとして WSL 2 を設定します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-122">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="a1efb-123">このメッセージは、コマンド `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel` を実行した後に表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-123">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="a1efb-124">リンク ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) に従って、WSL 2 で使用する Linux カーネルをコンピューターにインストールするためのドキュメントのこのページから MSI をインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-124">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="a1efb-125">カーネルをインストールしたら、コマンドを再度実行すると、メッセージが表示されることなく正常に完了します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-125">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="a1efb-126">対象のディストリビューションのサイズによっては、WSL 1 から WSL 2 への更新が完了するまでに数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-126">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="a1efb-127">Windows 10 Anniversary Update または Creators Update から WSL 1 の古い (レガシ) インストールを実行している場合は、更新エラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-127">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="a1efb-128">次の手順に従って、[レガシ ディストリビューションをアンインストールして削除](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro)します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-128">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span> 
>
> <span data-ttu-id="a1efb-129">`wsl --set-default-version` の結果が無効なコマンドである場合は、「`wsl --help`」と入力してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-129">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="a1efb-130">`--set-default-version` が表示されない場合は、お使いの OS によってサポートされていないことを意味しているため、バージョン 2004 ビルド 19041 以降に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-130">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 2004, Build 19041 or higher.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="a1efb-131">選択した Linux ディストリビューションをインストールする</span><span class="sxs-lookup"><span data-stu-id="a1efb-131">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="a1efb-132">[Microsoft Store](https://aka.ms/wslstore) を開き、希望する Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-132">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Microsoft Store での Linux ディストリビューションの表示](media/store.png)

    <span data-ttu-id="a1efb-134">次のリンクを使用すると、各ディストリビューションの Microsoft Store ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="a1efb-134">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="a1efb-135">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="a1efb-135">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="a1efb-136">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="a1efb-136">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="a1efb-137">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="a1efb-137">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="a1efb-138">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="a1efb-138">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="a1efb-139">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="a1efb-139">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="a1efb-140">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="a1efb-140">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="a1efb-141">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="a1efb-141">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="a1efb-142">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="a1efb-142">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="a1efb-143">WSL のための Fedora リミックス</span><span class="sxs-lookup"><span data-stu-id="a1efb-143">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="a1efb-144">Pengwin</span><span class="sxs-lookup"><span data-stu-id="a1efb-144">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="a1efb-145">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="a1efb-145">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="a1efb-146">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="a1efb-146">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="a1efb-147">ディストリビューションのページで、[入手] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-147">From the distribution's page, select "Get".</span></span>

    ![Microsoft Store での Linux ディストリビューション](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="a1efb-149">新しいディストリビューションを設定する</span><span class="sxs-lookup"><span data-stu-id="a1efb-149">Set up a new distribution</span></span>

<span data-ttu-id="a1efb-150">新しくインストールした Linux ディストリビューションを初めて起動すると、コンソール ウィンドウが開き、ファイルが圧縮解除されて PC に格納されるまで 1、2 分待つように求められます。</span><span class="sxs-lookup"><span data-stu-id="a1efb-150">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="a1efb-151">今後のすべての起動には、1 秒もかかりません。</span><span class="sxs-lookup"><span data-stu-id="a1efb-151">All future launches should take less than a second.</span></span>

<span data-ttu-id="a1efb-152">次に、[新しい Linux ディストリビューションのユーザー アカウントとパスワードを作成する](./user-support.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-152">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="a1efb-154">ディストリビューションのバージョンを WSL 1 または WSL 2 に設定する</span><span class="sxs-lookup"><span data-stu-id="a1efb-154">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="a1efb-155">インストールされている各 Linux ディストリビューションに割り当てられている WSL バージョンを確認するには、PowerShell コマンド ラインを開き、次のコマンドを入力します ([Windows ビルド 19041 以上](ms-settings:windowsupdate)でのみ使用可能): `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="a1efb-155">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="a1efb-156">ディストリビューションで使用される WSL のバージョンを設定するには、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-156">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="a1efb-157">`<distribution name>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。`<versionNumber>` は、数字の "1" または "2" に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-157">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="a1efb-158">上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="a1efb-158">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="a1efb-159">また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。</span><span class="sxs-lookup"><span data-stu-id="a1efb-159">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="a1efb-160">これにより、インストールされるすべての新しいディストリビューションのバージョンが WSL 2 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a1efb-160">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="a1efb-161">インストールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a1efb-161">Troubleshooting installation</span></span>

<span data-ttu-id="a1efb-162">関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-162">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="a1efb-163">その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-163">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="a1efb-164">**エラー 0x80070003 が発生してインストールに失敗しました**</span><span class="sxs-lookup"><span data-stu-id="a1efb-164">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="a1efb-165">Windows Subsystem for Linux はシステム ドライブ (通常、これは `C:` ドライブ) でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="a1efb-165">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="a1efb-166">ディストリビューションがシステム ドライブに格納されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-166">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="a1efb-167">**[設定]** -> **[ストレージ]** -> **[その他のストレージ設定: 新しいコンテンツの保存先を変更する]** 
    を開きます。![C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="a1efb-167">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="a1efb-168">**WslRegisterDistribution failed with error 0x8007019e (エラー0x8007019e で WslRegisterDistribution が失敗しました)**</span><span class="sxs-lookup"><span data-stu-id="a1efb-168">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="a1efb-169">Windows Subsystem for Linux オプション コンポーネントが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="a1efb-169">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="a1efb-170">**[コントロール パネル]**  ->  **[プログラムと機能]**  ->  **[Windows の機能の有効化または無効化]** を開いて、 **[Linux 用 Windows サブシステム]** をチェックするか、またはこの記事の冒頭に記載した PowerShell コマンドレットを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-170">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="a1efb-171">**インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**</span><span class="sxs-lookup"><span data-stu-id="a1efb-171">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="a1efb-172">コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-172">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="a1efb-173">これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。</span><span class="sxs-lookup"><span data-stu-id="a1efb-173">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="a1efb-174">**アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="a1efb-174">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="a1efb-175">Linux 用 Windows サブシステムが有効になっていること、および Windows ビルド バージョン 19041 以降を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-175">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 19041 or higher.</span></span> <span data-ttu-id="a1efb-176">WSL を有効にするには、PowerShell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="a1efb-176">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="a1efb-177">WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-177">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

- <span data-ttu-id="a1efb-178">**仮想ディスク システムの制限があるため、要求された操作を完了できませんでした。仮想ハード ディスク ファイルは、圧縮と暗号化が解除されている必要があります。また、スパースにすることはできません。**</span><span class="sxs-lookup"><span data-stu-id="a1efb-178">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="a1efb-179">この問題の最新情報が追跡されている [WSL GitHub スレッド #4103](https://github.com/microsoft/WSL/issues/4103) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-179">Please check [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="a1efb-180">**"wsl" という用語が、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。**</span><span class="sxs-lookup"><span data-stu-id="a1efb-180">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="a1efb-181">[Linux 用 Windows サブシステムのオプション コンポーネントがインストールされている](./install-win10.md#enable-the-virtual-machine-platform-optional-component)ことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a1efb-181">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="a1efb-182">また、ARM64 デバイスを使用し、PowerShell からこのコマンドを実行している場合も、このエラーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a1efb-182">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="a1efb-183">代わりに、`wsl.exe`PowerShell Core[ またはコマンド プロンプトから ](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) を実行します。</span><span class="sxs-lookup"><span data-stu-id="a1efb-183">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
