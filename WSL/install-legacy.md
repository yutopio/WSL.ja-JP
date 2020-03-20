---
title: Windows 10 記念日更新プログラムまたは作成者更新プログラムのインストールまたは削除
description: Windows 10 記念日更新プログラムまたは作成者更新プログラムのインストールとインストール解除の手順 (従来のベータディストリビューション)
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10、legacy、beta、install、remove、uninstall、un/install、delete、deprecated
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 416bed3ed3a0470da2eb5e6beb75e73eb6836200
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269771"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="ead7c-104">Windows 10 記念日更新プログラムおよび作成者の更新プログラムで Windows Subsystem for Linux をインストールまたはアンインストールするためのガイド</span><span class="sxs-lookup"><span data-stu-id="ead7c-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="ead7c-105">Windows 10 の作成者の更新プログラムまたはそれ以降を実行している場合は、 [windows 10 のインストール手順に従っ](install-win10.md)てください。</span><span class="sxs-lookup"><span data-stu-id="ead7c-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="ead7c-106"><strong><em><span style="color: #f28014">次の手順は、Windows 10 周年更新プログラムまたは Windows 10 の作成者更新プログラムを実行しているユーザーを対象としています。</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="ead7c-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="ead7c-107">Windows 10 秋の更新プログラム (バージョン 1709) より前のバージョンでは、WSL はベータ機能としてリリースされ、"Bash on Ubuntu on Windows" (または Bash) が最初に実行されたときに1つの Ubuntu インスタンスをインストールしました。</span><span class="sxs-lookup"><span data-stu-id="ead7c-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="ead7c-108">以前の Windows 10 リリースでは WSL を使用できますが、このベータ版の "レガシディストリビューション" は廃止されたと見なされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ead7c-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="ead7c-109">使用可能な Windows 10 の最新バージョンを実行することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ead7c-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="ead7c-110">新しい Windows 10 のリリースには、WSL 単独で数百の修正と改善が加えられており、WSL でより多くの Linux ツールとアプリが正常に実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ead7c-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="ead7c-111">更新プログラムの適用後にアップグレードできない場合は、次の手順に従って、WSL を有効にして使用します。</span><span class="sxs-lookup"><span data-stu-id="ead7c-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="ead7c-112">開発者モードを有効にして、Windows 10 の記念日更新または作成者の更新で WSL を実行するには、開発者モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ead7c-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="ead7c-113">**開発者のための**[**設定** -> **更新とセキュリティ** -> を開く]</span><span class="sxs-lookup"><span data-stu-id="ead7c-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="ead7c-114">[開発者モード] オプションボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ead7c-114">Select the Developer Mode radio button</span></span>  
    ![開発者モードを有効にする](media/updateAndSecurity.png)

    > <span data-ttu-id="ead7c-116">開発者モードを有効にするための要件は、 [Windows 10 の作成者の更新プログラムで削除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)されました</span><span class="sxs-lookup"><span data-stu-id="ead7c-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="ead7c-117">コマンド プロンプトを開きます。</span><span class="sxs-lookup"><span data-stu-id="ead7c-117">Open a command prompt.</span></span>  <span data-ttu-id="ead7c-118">「`bash`」と入力し、enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="ead7c-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="ead7c-119">Windows で Bash on Ubuntu を初めて実行すると、正規のライセンスに同意するように求められます。</span><span class="sxs-lookup"><span data-stu-id="ead7c-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="ead7c-120">承諾すると、WSL は Ubuntu インスタンスをコンピューターにダウンロードしてインストールします。また、[Windows の Bash on Ubuntu] ショートカットが [スタート] メニューに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ead7c-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Ubuntu のインストールを確認する](media/bashShellInstall.png)

    <span data-ttu-id="ead7c-122">Windows で Bash on Ubuntu を初めて実行するときに、UNIX ユーザー名とパスワードの作成を求められます。</span><span class="sxs-lookup"><span data-stu-id="ead7c-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="ead7c-123">[新しいディストリビューションインスタンスの指示](initialize-distro.md)に従って、インストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="ead7c-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="ead7c-124">次のいずれかの方法で新しい Ubuntu シェルを起動します。</span><span class="sxs-lookup"><span data-stu-id="ead7c-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="ead7c-125">コマンドプロンプトからの `bash` の実行</span><span class="sxs-lookup"><span data-stu-id="ead7c-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="ead7c-126">[スタート] メニューの [Bash on Ubuntu on Windows] のショートカット</span><span class="sxs-lookup"><span data-stu-id="ead7c-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="ead7c-127">レガシディストリビューションのアンインストール/削除</span><span class="sxs-lookup"><span data-stu-id="ead7c-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="ead7c-128">WSL をインストールした以前の Windows 10 リリースから Windows 10 にアップグレードすると、既存のディストリビューションはそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="ead7c-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="ead7c-129">ただし、ストアによって配信される新しいディストリビューションをすぐにインストールし、必要なファイルやデータなどをレガシディストリビューションから新しいディストリビューションに移行することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ead7c-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="ead7c-130">レガシディストリビューションをコンピューターから削除するには、コマンドラインまたは PowerShell インスタンスから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ead7c-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
wsl --unregister Legacy
```

<span data-ttu-id="ead7c-131">Windows バージョン1903以降を使用していない場合は、代わりに `wslconfig /u Legacy` または `lxrun /uninstall /full` を実行する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="ead7c-131">If you are not using Windows Version 1903 or higher, you may need to run `wslconfig /u Legacy` or `lxrun /uninstall /full` instead.</span></span> 

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="ead7c-132">レガシディストリビューションを手動で削除する</span><span class="sxs-lookup"><span data-stu-id="ead7c-132">Manually deleting the legacy distro</span></span>
<span data-ttu-id="ead7c-133">必要に応じて、レガシインスタンスを手動で削除できます。</span><span class="sxs-lookup"><span data-stu-id="ead7c-133">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="ead7c-134">これは、`lxrun.exe`を使用したレガシディストリビューションのアンインストールで問題が発生した場合、または `lxrun.exe`で出荷されていない Windows 10 Spring 2018 Update (またはそれ以降) を実行している場合に必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="ead7c-134">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="ead7c-135">従来の WSL ディストリビューションを強制的に削除するには、Windows のエクスプローラーまたはコマンドラインを使用して、`%localappdata%\lxss\` フォルダー (およびそのすべてのサブコンテンツ) を削除します。</span><span class="sxs-lookup"><span data-stu-id="ead7c-135">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="ead7c-136">PowerShell の使用</span><span class="sxs-lookup"><span data-stu-id="ead7c-136">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="ead7c-137">Cmd を使用する:</span><span class="sxs-lookup"><span data-stu-id="ead7c-137">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
