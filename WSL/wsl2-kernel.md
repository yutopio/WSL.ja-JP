---
title: WSL 2 Linux カーネルを更新しています
description: WSL 2 Linux カーネルを手動で更新する方法に関する手順
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138191"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="cccf4-104">WSL 2 Linux カーネルを更新しています</span><span class="sxs-lookup"><span data-stu-id="cccf4-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="cccf4-105">WSL 2 内の Linux カーネルを手動で更新するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="cccf4-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="cccf4-106">Linux カーネル更新パッケージをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="cccf4-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="cccf4-107">AMD64 マシン用の最新の WSL2 Linux カーネル更新パッケージをダウンロードするには、[このリンク](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="cccf4-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for AMD64 machines.</span></span>

> [!NOTE] <span data-ttu-id="cccf4-108">ARM64 マシンを使用している場合は、代わりに[このパッケージ](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="cccf4-108">if you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="cccf4-109">Linux カーネル更新パッケージをインストールする</span><span class="sxs-lookup"><span data-stu-id="cccf4-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="cccf4-110">Linux カーネル更新パッケージをインストールするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="cccf4-110">To install the Linux kernel update package:</span></span>
    1. <span data-ttu-id="cccf4-111">前の手順でダウンロードした更新プログラムパッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="cccf4-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="cccf4-112">昇格したアクセス許可を求められます。このインストールを承認するには、[はい] を選択してください。</span><span class="sxs-lookup"><span data-stu-id="cccf4-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="cccf4-113">インストールが完了したら、WSL2 の使用を開始できます。</span><span class="sxs-lookup"><span data-stu-id="cccf4-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="cccf4-114">WSL2 Linux カーネルを更新するための今後の計画</span><span class="sxs-lookup"><span data-stu-id="cccf4-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="cccf4-115">これらの変更の詳細については、 [Windows コマンドラインブログ](https://aka.ms/cliblog)のこちらの[ブログ](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)記事をお読みください。</span><span class="sxs-lookup"><span data-stu-id="cccf4-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>