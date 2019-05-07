---
title: インストールまたは Windows 10 Anniversary Update または Creators Update の削除
description: 従来、Windows 10 Anniversary Update または Creators Update のベータ版のディストリビューションのインストールとアンインストールの手順
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10、レガシ、ベータ版の windows サブシステムのインストール、削除、アンインストール、アンインストール、削除、非推奨とされます
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063590"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="dd9d6-104">インストールまたは Windows 10 Anniversary Update および Creators Update での Linux 用 Windows サブシステムをアンインストール ガイド</span><span class="sxs-lookup"><span data-stu-id="dd9d6-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="dd9d6-105">Windows 10 Creators Update を実行しているか、後で、ください[Windows 10 のインストール手順に従って](install-win10.md)します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="dd9d6-106"><strong><em><span style="color: #f28014">次の手順は Windows 10 Anniversary Update または Windows 10 Creators Update を実行しているユーザーです。</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="dd9d6-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="dd9d6-107">Windows 10 Fall Creators Update (バージョン 1709)、前に、WSL は、ベータ機能としてリリースされましたし、"Bash で Ubuntu の Windows"(または Bash.exe) を最初に実行時に、1 つの Ubuntu インスタンスをインストールします。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="dd9d6-108">WSL を使用して、以前の Windows 10 リリースでは、このベータ版「レガシ ディストリビューション」を古いと見なされますようになりました。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="dd9d6-109">使用可能な Windows 10 の最新バージョンを実行すること強く勧めします。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="dd9d6-110">新しい Windows 10 リリースには、これまで以上の Linux ツールと WSL では正しく動作するアプリを許可するだけで、WSL で何百も修正プログラムと機能強化にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="dd9d6-111">Fall Creators Update 以降をアップグレードできない場合は、有効にして WSL を使用するのには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="dd9d6-112">開発者モード WSL またはで実行する Windows 10 Anniversary Update Creators Update を有効に、開発者モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="dd9d6-113">開いている**設定** -> **更新とセキュリティ** -> **開発者向け**</span><span class="sxs-lookup"><span data-stu-id="dd9d6-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="dd9d6-114">開発者モードのオプション ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-114">Select the Developer Mode radio button</span></span>  
    ![開発者モードを有効にする](media/updateAndSecurity.png)

    > <span data-ttu-id="dd9d6-116">開発者モードを有効にするための要件が[Windows 10 Fall Creators Update での削除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="dd9d6-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="dd9d6-117">コマンド プロンプトを開きます。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-117">Open a command prompt.</span></span>  <span data-ttu-id="dd9d6-118">型`bash`し、enter キーを押します</span><span class="sxs-lookup"><span data-stu-id="dd9d6-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="dd9d6-119">初めてでは、Windows、Ubuntu 上で Bash を実行する、Canonical のライセンスに同意するよう求めします。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="dd9d6-120">1 回 accpted、WSL はダウンロードして、コンピューター上に Ubuntu インスタンスをインストールし、"Bash で Ubuntu の Windows"ショートカットを [スタート] メニューに追加されます。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-120">Once accpted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Ubuntu をインストールするプロンプト](media/bashShellInstall.png)

    <span data-ttu-id="dd9d6-122">初めての Windows、Ubuntu 上で Bash を実行するは促さ UNIX ユーザー名とパスワードを作成します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="dd9d6-123">に従って、[ディストリビューション インスタンスの新しい命令](initialize-distro.md)インストールを完了するには</span><span class="sxs-lookup"><span data-stu-id="dd9d6-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="dd9d6-124">いずれかで、新しい Ubuntu シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="dd9d6-125">実行している`bash`コマンド プロンプトから</span><span class="sxs-lookup"><span data-stu-id="dd9d6-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="dd9d6-126">[スタート] メニューの"Bash で Ubuntu の Windows"ショートカットをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="dd9d6-127">従来のディストリビューションをアンインストール/削除</span><span class="sxs-lookup"><span data-stu-id="dd9d6-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="dd9d6-128">WSL をインストールした以前の Windows 10 リリースから Windows 10 Fall Creators Update にアップグレードする場合、既存のディストリビューションがそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="dd9d6-129">ただし、厳密にストアによって提供される新しいディストリビューション至急をインストールすることをお勧めし、必要なファイル、データなどを従来のディストリビューションから、新しいディストリビューションに移行します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="dd9d6-130">従来のディストリビューションをコンピューターからを削除するには、コマンドラインまたは PowerShell のインスタンスから、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="dd9d6-131">従来のディストリビューションを手動で削除します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="dd9d6-132">希望されない場合、従来のインスタンスを手動で削除することができます。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="dd9d6-133">これは、必要がありますを使用して、従来のディストリビューションのアンインストールで問題が発生した場合`lxrun.exe`、または Windows 10 のスプリング 2018 Update を実行している (またはそれ以降) でこれを出荷しません`lxrun.exe`します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="dd9d6-134">従来、WSL ディストリビューションを強制的に削除するには、削除、`%localappdata%\lxss\`フォルダー (すべてとサブフォルダーの内容の) Windows のエクスプ ローラーまたはコマンドラインを使用して。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="dd9d6-135">PowerShell を使用する</span><span class="sxs-lookup"><span data-stu-id="dd9d6-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="dd9d6-136">Cmd を使用します。</span><span class="sxs-lookup"><span data-stu-id="dd9d6-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
