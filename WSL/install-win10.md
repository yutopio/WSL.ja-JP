---
title: Windows 10 での Linux (WSL) 用の Windows サブシステムをインストールします。
description: Windows 10 での Linux 用 Windows サブシステムのインストール手順。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステムのインストールします。
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035052"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="8538e-104">Windows 10 用の Linux インストール ガイド用 Windows サブシステム</span><span class="sxs-lookup"><span data-stu-id="8538e-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="8538e-105">Linux 用の Windows サブシステムをインストールします。</span><span class="sxs-lookup"><span data-stu-id="8538e-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="8538e-106">WSL の任意の Linux ディストリビューションをインストールする前にすることが必要、"Windows サブシステムの Linux"省略可能な機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8538e-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="8538e-107">管理者として PowerShell を開きを実行します。</span><span class="sxs-lookup"><span data-stu-id="8538e-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="8538e-108">コンピューターが表示されたら再起動します。</span><span class="sxs-lookup"><span data-stu-id="8538e-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="8538e-109">任意の Linux ディストリビューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="8538e-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="8538e-110">をダウンロードして、優先 distro(s) をインストールするには、次の 3 つの選択肢があります。</span><span class="sxs-lookup"><span data-stu-id="8538e-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="8538e-111">Windows ストア (下記参照) からダウンロードしてインストール</span><span class="sxs-lookup"><span data-stu-id="8538e-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="8538e-112">コマンドのコマンドライン/スクリプトからダウンロードしてインストール ([手動インストールの指示を読み](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="8538e-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="8538e-113">ダウンロードして手動で展開し、インストール (for Windows Server -[こちら](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="8538e-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="8538e-114">Windows 10 Fall Creators Update 以降。Microsoft Store からインストールします。</span><span class="sxs-lookup"><span data-stu-id="8538e-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="8538e-115">このセクションでは、Windows ビルド 16215 またはそれ以降は。</span><span class="sxs-lookup"><span data-stu-id="8538e-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="8538e-116">以下の手順に従って[ビルド確認](troubleshooting.md#check-your-build-number)します。</span><span class="sxs-lookup"><span data-stu-id="8538e-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="8538e-117">Microsoft Store を開き、お気に入りの Linux ディストリビューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8538e-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Windows ストアでの Linux ディストリビューションのビュー](media/store.png)

    <span data-ttu-id="8538e-119">次のリンクには、各ディストリビューションの Windows ストア ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="8538e-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="8538e-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="8538e-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="8538e-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="8538e-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="8538e-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="8538e-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="8538e-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="8538e-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="8538e-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="8538e-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="8538e-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="8538e-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="8538e-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="8538e-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="8538e-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="8538e-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="8538e-128">WSL の fedora Remix</span><span class="sxs-lookup"><span data-stu-id="8538e-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="8538e-129">WLinux</span><span class="sxs-lookup"><span data-stu-id="8538e-129">WLinux</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="8538e-130">WLinux Enterprise</span><span class="sxs-lookup"><span data-stu-id="8538e-130">WLinux Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="8538e-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="8538e-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="8538e-132">ディストリビューションのページで、"Get"を選択します</span><span class="sxs-lookup"><span data-stu-id="8538e-132">From the distro's page, select "Get"</span></span>

    ![Windows ストアでの Linux ディストリビューションのビュー](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="8538e-134">ディストリビューションの初期化を完了</span><span class="sxs-lookup"><span data-stu-id="8538e-134">Complete initialization of your distro</span></span>
<span data-ttu-id="8538e-135">必要があります、Linux ディストリビューションがインストールされた[ディストリビューションの新しいインスタンスを初期化](initialize-distro.md)1 回を使用します。</span><span class="sxs-lookup"><span data-stu-id="8538e-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8538e-136">トラブルシューティング:</span><span class="sxs-lookup"><span data-stu-id="8538e-136">Troubleshooting:</span></span> 

<span data-ttu-id="8538e-137">関連するエラーと推奨される修正方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8538e-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="8538e-138">参照してください、 [WSL のトラブルシューティング ページ](troubleshooting.md)の他の一般的なエラーとその解決方法。</span><span class="sxs-lookup"><span data-stu-id="8538e-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="8538e-139">**インストールに 0x80070003 のエラーで失敗しました**</span><span class="sxs-lookup"><span data-stu-id="8538e-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="8538e-140">Windows Subsystem for Linux は、システム ドライブでのみ実行されます (通常、これは、`C:`ドライブ)。</span><span class="sxs-lookup"><span data-stu-id="8538e-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="8538e-141">ディストリビューションの場合は、システム ドライブに格納されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8538e-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="8538e-142">開いている**設定** -> **ストレージ** -> **以上の記憶域の設定。新しいコンテンツが保存されている変更**
    ![c: ドライブにアプリをインストールするシステム設定の画像](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="8538e-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="8538e-143">**WslRegisterDistribution 0x8007019e エラーで失敗しました**</span><span class="sxs-lookup"><span data-stu-id="8538e-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="8538e-144">省略可能なコンポーネントが有効でない Linux 用 Windows サブシステム:</span><span class="sxs-lookup"><span data-stu-id="8538e-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="8538e-145">開いている**コントロール パネルの**  -> **プログラムと機能**-> \* \* Windows の機能を有効にする」オンまたはオフ \* \* チェック->  **Windows Subsystem for Linux**またはを使用して、この記事の冒頭で説明されている PowerShell コマンドレット。</span><span class="sxs-lookup"><span data-stu-id="8538e-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
