---
title: WSL 2 Linux カーネルの更新
description: WSL 2 Linux カーネルを手動で更新するための手順
keywords: wsl, windows, linux カーネル, linux 用 windows サブシステム, カーネル
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: a718c4a880e2c3147900143c24983835d269a4bc
ms.sourcegitcommit: a5534257c236cefeebe86e6b3fc4be0be8fac24e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/21/2020
ms.locfileid: "88714826"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="56150-104">WSL 2 Linux カーネルの更新</span><span class="sxs-lookup"><span data-stu-id="56150-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="56150-105">WSL 2 内の Linux カーネルを手動で更新するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="56150-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="56150-106">インストーラーで WSL 1 が見つからない場合は、Linux カーネル更新プログラムのインストーラーを右クリックして [アンインストール] をクリックし、インストーラーを再実行します。</span><span class="sxs-lookup"><span data-stu-id="56150-106">If the installer can't find WSL 1, right-click the Linux kernel update installer and press "Uninstall", then rerun the installer.</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="56150-107">Linux カーネル更新プログラム パッケージをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="56150-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="56150-108">x64 マシン用の[最新の WSL2 Linux カーネル更新プログラム パッケージをダウンロード](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)してください。</span><span class="sxs-lookup"><span data-stu-id="56150-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="56150-109">ARM64 マシンを使用している場合は、代わりに [ARM64 パッケージ](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="56150-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="56150-110">Linux カーネル更新プログラム パッケージをインストールする</span><span class="sxs-lookup"><span data-stu-id="56150-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="56150-111">Linux カーネル更新パッケージをインストールするには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="56150-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="56150-112">前の手順でダウンロードした更新プログラム パッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="56150-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="56150-113">管理者特権のアクセス許可の入力が求められます。このインストールを承認するには、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="56150-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="56150-114">インストールが完了したら、WSL2 の使用を開始できます。</span><span class="sxs-lookup"><span data-stu-id="56150-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="56150-115">WSL2 Linux カーネルの更新に関する今後の計画</span><span class="sxs-lookup"><span data-stu-id="56150-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="56150-116">詳細については、[Windows コマンドラインのブログ](https://aka.ms/cliblog)にある[WSL2 Linux カーネルの更新プログラムに対する変更](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="56150-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="56150-117">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="56150-117">Troubleshooting</span></span>

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a><span data-ttu-id="56150-118">この更新プログラムは、Linux 用 Windows サブシステムを搭載したコンピューターにのみ適用される</span><span class="sxs-lookup"><span data-stu-id="56150-118">This update only applies to machines with the Windows Subsystem for Linux</span></span>
<span data-ttu-id="56150-119">MSI カーネルをインストールするには、WSL が必要であり、最初に有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="56150-119">To install MSI kernel, WSL is required and should be enabled first.</span></span> <span data-ttu-id="56150-120">失敗した場合は、"`This update only applies to machines with the Windows Subsystem for Linux`" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="56150-120">If it fails, it you will see the message: `This update only applies to machines with the Windows Subsystem for Linux`.</span></span> 

<span data-ttu-id="56150-121">このメッセージが表示される理由として、次の 3 つが考えられます。</span><span class="sxs-lookup"><span data-stu-id="56150-121">There are three possible reason you see this message:</span></span>

1. <span data-ttu-id="56150-122">WSL 2 をサポートしていない古いバージョンの Windows を使用しています。</span><span class="sxs-lookup"><span data-stu-id="56150-122">You are still in old version of Windows which doesn't support WSL 2.</span></span> <span data-ttu-id="56150-123">[WSL 2 の要件](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2)を確認し、WSL 2 を使用するようにアップグレードしてください。</span><span class="sxs-lookup"><span data-stu-id="56150-123">Please check the [WSL 2 requirements](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) and upgrade to use WSL 2.</span></span> 
2. <span data-ttu-id="56150-124">`Windows Subsystem for Linux` が有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="56150-124">`Windows Subsystem for Linux` is not enabled.</span></span> <span data-ttu-id="56150-125">[Linux 用 Windows サブシステムのインストール ガイド](https://docs.microsoft.com/windows/wsl/install-win10)に従ってください。</span><span class="sxs-lookup"><span data-stu-id="56150-125">Please follow the [Windows Subsystem for Linux Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10).</span></span>
3. <span data-ttu-id="56150-126">`Windows Subsystem for Linux` を有効にした後は再起動が必要になります。コンピューターを再起動して、もう一度やり直してください。</span><span class="sxs-lookup"><span data-stu-id="56150-126">After you enabled `Windows Subsystem for Linux`, a reboot is required to take into effect, please reboot your machine and try again.</span></span>

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

<span data-ttu-id="56150-127">%SystemRoot%\system32\lxss\tools\, にカーネルがない場合、その都度上記のエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="56150-127">Each time kernel is missing in %SystemRoot%\system32\lxss\tools\, you may run into the above error.</span></span>

<span data-ttu-id="56150-128">これを解決するには、次のような方法があります。</span><span class="sxs-lookup"><span data-stu-id="56150-128">Here are some possible ways to resolve it:</span></span>

1. <span data-ttu-id="56150-129">Linux カーネルを、 https://aka.ms/wsl2kernel の手順に従って手動でインストールしてください</span><span class="sxs-lookup"><span data-stu-id="56150-129">Please install the Linux kernel manually by following the instructions at: https://aka.ms/wsl2kernel</span></span>
2. <span data-ttu-id="56150-130">[プログラムの追加と削除] から MSI をアンインストールしてから、もう一度インストールしてください</span><span class="sxs-lookup"><span data-stu-id="56150-130">Uninstall the MSI from 'Add or Remove Programs', and install it again</span></span>
