---
title: WSL 2 Linux カーネルの更新
description: WSL 2 Linux カーネルを手動で更新するための手順
keywords: wsl, windows, linux カーネル, linux 用 windows サブシステム, カーネル
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 89e5755699938b7797aa65a5f3131f93e3e31796
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343834"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="3ec10-104">WSL 2 Linux カーネルの更新</span><span class="sxs-lookup"><span data-stu-id="3ec10-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="3ec10-105">WSL 2 内の Linux カーネルを手動で更新するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="3ec10-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="3ec10-106">インストーラーで WSL 1 が見つからない場合は、Linux カーネル更新プログラムのインストーラーを右クリックして [アンインストール] をクリックし、インストーラーを再実行します</span><span class="sxs-lookup"><span data-stu-id="3ec10-106">If the installer cant find WSL 1 right click the Linux kernel update installer, then press uninstall then rerun the installer</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="3ec10-107">Linux カーネル更新プログラム パッケージをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="3ec10-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="3ec10-108">x64 マシン用の[最新の WSL2 Linux カーネル更新プログラム パッケージをダウンロード](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)してください。</span><span class="sxs-lookup"><span data-stu-id="3ec10-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="3ec10-109">ARM64 マシンを使用している場合は、代わりに [ARM64 パッケージ](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="3ec10-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="3ec10-110">Linux カーネル更新プログラム パッケージをインストールする</span><span class="sxs-lookup"><span data-stu-id="3ec10-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="3ec10-111">Linux カーネル更新パッケージをインストールするには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="3ec10-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="3ec10-112">前の手順でダウンロードした更新プログラム パッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="3ec10-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="3ec10-113">管理者特権のアクセス許可の入力が求められます。このインストールを承認するには、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ec10-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="3ec10-114">インストールが完了したら、WSL2 の使用を開始できます。</span><span class="sxs-lookup"><span data-stu-id="3ec10-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="3ec10-115">WSL2 Linux カーネルの更新に関する今後の計画</span><span class="sxs-lookup"><span data-stu-id="3ec10-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="3ec10-116">詳細については、[Windows コマンドラインのブログ](https://aka.ms/cliblog)にある[WSL2 Linux カーネルの更新プログラムに対する変更](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ec10-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
