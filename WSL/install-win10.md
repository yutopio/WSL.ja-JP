---
title: Windows 10 に Windows Subsystem for Linux (WSL) をインストールする
description: Windows 10 の Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10、install
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499287"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="b1c7e-104">Windows 10 用 windows Subsystem for Linux インストールガイド</span><span class="sxs-lookup"><span data-stu-id="b1c7e-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="b1c7e-105">Windows Subsystem for Linux をインストールする</span><span class="sxs-lookup"><span data-stu-id="b1c7e-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="b1c7e-106">WSL 用の Linux ディストリビューションをインストールする前に、[Windows Subsystem for Linux] オプション機能が有効になっていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="b1c7e-107">管理者として PowerShell を開き、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="b1c7e-108">メッセージが表示されたら、コンピューターを再起動します。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="b1c7e-109">選択した Linux ディストリビューションをインストールする</span><span class="sxs-lookup"><span data-stu-id="b1c7e-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="b1c7e-110">優先するディストリビューションをダウンロードしてインストールするには、次の3つの選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="b1c7e-111">Microsoft Store からダウンロードしてインストールする (下記参照)</span><span class="sxs-lookup"><span data-stu-id="b1c7e-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="b1c7e-112">コマンドラインまたはスクリプトからダウンロードしてインストールする ([手動によるインストール手順を参照](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="b1c7e-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="b1c7e-113">をダウンロードして手動で展開してインストールする (Windows Server の場合-[手順](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="b1c7e-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="b1c7e-114">Windows 10 の作成者の更新プログラム以降:Microsoft Store からのインストール</span><span class="sxs-lookup"><span data-stu-id="b1c7e-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="b1c7e-115">このセクションは、Windows ビルド16215以降を対象としています。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="b1c7e-116">[ビルドを確認](troubleshooting.md#check-your-build-number)するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="b1c7e-117">Microsoft Store を開き、お気に入りの Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store の Linux ディストリビューションのビュー](media/store.png)

    <span data-ttu-id="b1c7e-119">次のリンクを使用すると、各ディストリビューションの Microsoft ストアページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="b1c7e-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="b1c7e-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="b1c7e-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="b1c7e-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="b1c7e-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="b1c7e-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="b1c7e-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="b1c7e-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="b1c7e-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="b1c7e-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="b1c7e-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="b1c7e-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="b1c7e-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="b1c7e-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="b1c7e-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="b1c7e-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="b1c7e-128">WSL の Fedora Remix</span><span class="sxs-lookup"><span data-stu-id="b1c7e-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="b1c7e-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="b1c7e-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="b1c7e-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="b1c7e-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="b1c7e-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="b1c7e-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="b1c7e-132">ディストリビューションのページで、[Get] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-132">From the distro's page, select "Get"</span></span>

    ![Microsoft ストアの Linux ディストリビューションの表示](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="b1c7e-134">ディストリビューションの初期化を完了する</span><span class="sxs-lookup"><span data-stu-id="b1c7e-134">Complete initialization of your distro</span></span>
<span data-ttu-id="b1c7e-135">Linux ディストリビューションがインストールされたので、[新しいディストリビューションインスタンス](initialize-distro.md)を使用するには、一度初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b1c7e-136">トラブルシューティング:</span><span class="sxs-lookup"><span data-stu-id="b1c7e-136">Troubleshooting:</span></span> 

<span data-ttu-id="b1c7e-137">関連するエラーと修正案を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="b1c7e-138">その他の一般的なエラーとその解決策については、 [Wsl トラブルシューティングのページ](troubleshooting.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="b1c7e-139">**エラー0x80070003 が発生し、インストールに失敗しました**</span><span class="sxs-lookup"><span data-stu-id="b1c7e-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="b1c7e-140">Windows Subsystem for Linux はシステムドライブ (通常は`C:`ドライブ) でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="b1c7e-141">ディストリビューションがシステムドライブに格納されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="b1c7e-142">[**設定** -> ] [**ストレージ** -> ][その他のストレージ設定]を開きます。**新しいコンテンツが保存**
    ![される場所の変更 C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="b1c7e-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="b1c7e-143">**WslRegisterDistribution がエラー0x8007019e で失敗しました**</span><span class="sxs-lookup"><span data-stu-id="b1c7e-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="b1c7e-144">Windows Subsystem for Linux のオプションコンポーネントが有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="b1c7e-145">[**コントロールパネル** -> の**プログラムと機能**]-> \* \* [windows の機能の有効化または無効化] \* \*-> **Linux 用 windows サブシステム**を確認するか、この記事の冒頭に記載されている PowerShell コマンドレットを使用して確認します。</span><span class="sxs-lookup"><span data-stu-id="b1c7e-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
