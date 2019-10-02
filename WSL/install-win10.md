---
title: Windows Subsystem for Linux (WSL) を Windows 10 にインストールする
description: Windows 10 での Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c53c4507fb56f8e4a3456963b1d6f50ceac8ef37
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269813"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="b3a49-104">Windows 10 用 Windows Subsystem for Linux のインストール ガイド</span><span class="sxs-lookup"><span data-stu-id="b3a49-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="b3a49-105">Windows Subsystem for Linux のインストール</span><span class="sxs-lookup"><span data-stu-id="b3a49-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="b3a49-106">WSL 用の Linux ディストリビューションをインストールする前に、[Windows Subsystem for Linux] オプション機能が有効になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3a49-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="b3a49-107">管理者として PowerShell を開き、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="b3a49-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="b3a49-108">メッセージが表示されたら、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b3a49-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="b3a49-109">任意の Linux ディストリビューションのインストール</span><span class="sxs-lookup"><span data-stu-id="b3a49-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="b3a49-110">希望するディストリビューションをダウンロードしてインストールするには、次の 3 つの選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="b3a49-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="b3a49-111">Microsoft Store からダウンロードしてインストールする (下記参照)</span><span class="sxs-lookup"><span data-stu-id="b3a49-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="b3a49-112">コマンド ライン/スクリプトからダウンロードしてインストールする ([手動インストール手順を参照](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="b3a49-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="b3a49-113">ダウンロードして手動で展開し、インストールする (Windows Server の場合 - [こちらの手順](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="b3a49-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="b3a49-114">Windows 10 Fall Creators Update 以降:Microsoft Store からのインストール</span><span class="sxs-lookup"><span data-stu-id="b3a49-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="b3a49-115">このセクションは、Windows ビルド16215 以降が対象です。</span><span class="sxs-lookup"><span data-stu-id="b3a49-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="b3a49-116">[ビルドを確認する](troubleshooting.md#check-your-build-number)には、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b3a49-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="b3a49-117">Microsoft Store を開き、希望する Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3a49-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store の Linux ディストリビューションのビュー](media/store.png)

    <span data-ttu-id="b3a49-119">次のリンクを使用すると、各ディストリビューションの Microsoft Store ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b3a49-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="b3a49-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="b3a49-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="b3a49-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="b3a49-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="b3a49-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="b3a49-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="b3a49-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="b3a49-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="b3a49-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="b3a49-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="b3a49-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="b3a49-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="b3a49-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="b3a49-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="b3a49-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="b3a49-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="b3a49-128">WSL のための Fedora リミックス</span><span class="sxs-lookup"><span data-stu-id="b3a49-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="b3a49-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="b3a49-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="b3a49-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="b3a49-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="b3a49-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="b3a49-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="b3a49-132">ディストリビューションのページで、[入手] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3a49-132">From the distro's page, select "Get"</span></span>

    ![Microsoft Store の Linux ディストリビューションのビュー](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="b3a49-134">ディストリビューションの初期化を完了する</span><span class="sxs-lookup"><span data-stu-id="b3a49-134">Complete initialization of your distro</span></span>
<span data-ttu-id="b3a49-135">Linux ディストリビューションがインストールされたので、新しいディストリビューション インスタンスを使用する前に、一度[そのインスタンスを初期化する](initialize-distro.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3a49-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b3a49-136">トラブルシューティング:</span><span class="sxs-lookup"><span data-stu-id="b3a49-136">Troubleshooting:</span></span> 

<span data-ttu-id="b3a49-137">関連エラーと推奨される修正を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b3a49-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="b3a49-138">その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3a49-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="b3a49-139">**エラー 0x80070003 が発生してインストールに失敗しました**</span><span class="sxs-lookup"><span data-stu-id="b3a49-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="b3a49-140">Windows Subsystem for Linux はシステム ドライブ (通常、これは `C:` ドライブ) でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3a49-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="b3a49-141">ディストリビューションがシステム ドライブに格納されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b3a49-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="b3a49-142">**[設定]** -> **[ストレージ]** -> **[その他のストレージ設定:新しいコンテンツの保存先を変更する]** 
    を開きます。![C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="b3a49-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="b3a49-143">**WslRegisterDistribution failed with error 0x8007019e (エラー0x8007019e で WslRegisterDistribution が失敗しました)**</span><span class="sxs-lookup"><span data-stu-id="b3a49-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="b3a49-144">Windows Subsystem for Linux オプション コンポーネントが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="b3a49-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="b3a49-145">**[コントロール パネル]**  ->  **[プログラムと機能]**  ->  **[Windows の機能の有効化または無効化]** を開いて、 **[Windows Subsystem for Linux]** をチェックするか、またはこの記事の冒頭に記載した PowerShell コマンドレットを使用して有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="b3a49-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
