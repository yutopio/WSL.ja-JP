---
title: Linux 用 Windows サブシステム カーネルのリリース ノート
description: Windows Subsystem for Linux のリリース ノート。  毎月更新されます。
keywords: リリース ノート, wsl, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, カーネル
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 32b65bcde3df01b25f0361493a172e754e78e101
ms.sourcegitcommit: 43d4056eefe0c71ecd9a0fbd5a7a58dd18fa9829
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2020
ms.locfileid: "89615548"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="a107c-105">Linux 用 Windows サブシステム カーネルのリリース ノート</span><span class="sxs-lookup"><span data-stu-id="a107c-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="a107c-106">WSL 2 ディストリビューションのサポートが追加されました。ここでは、[完全な Linux カーネルが使用されます](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)。</span><span class="sxs-lookup"><span data-stu-id="a107c-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="a107c-107">この Linux カーネルはオープン ソースであり、そのソースコードは [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) リポジトリから入手できます。</span><span class="sxs-lookup"><span data-stu-id="a107c-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="a107c-108">この Linux カーネルは Microsoft Update を介してコンピューターに配信され、Windows イメージの一部として提供される Linux 用 Windows サブシステムの個別のリリース スケジュールに従います。</span><span class="sxs-lookup"><span data-stu-id="a107c-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="a107c-109">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="a107c-109">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="a107c-110">*リリース日*:プレリリース、手動インストールにより入手可能</span><span class="sxs-lookup"><span data-stu-id="a107c-110">*Release Date*: Prerelease and available via manual install</span></span>

<span data-ttu-id="a107c-111">[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard)。</span><span class="sxs-lookup"><span data-stu-id="a107c-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="a107c-112">これは 4.19.128 の安定リリースです</span><span class="sxs-lookup"><span data-stu-id="a107c-112">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="a107c-113">dxgkrnl ドライバーの IOCTL メモリの破損を修正</span><span class="sxs-lookup"><span data-stu-id="a107c-113">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="a107c-114">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="a107c-114">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="a107c-115">*リリース日*:プレリリース</span><span class="sxs-lookup"><span data-stu-id="a107c-115">*Release Date*: Prerelease</span></span>

<span data-ttu-id="a107c-116">[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard)。</span><span class="sxs-lookup"><span data-stu-id="a107c-116">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="a107c-117">ドライバー: hv: vmbus: dxgkrnl をフック</span><span class="sxs-lookup"><span data-stu-id="a107c-117">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="a107c-118">GPU コンピューティングに対するサポートの追加</span><span class="sxs-lookup"><span data-stu-id="a107c-118">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="a107c-119">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="a107c-119">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="a107c-120">*リリース日*:2020 年 6 月 9 日</span><span class="sxs-lookup"><span data-stu-id="a107c-120">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="a107c-121">[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard)。</span><span class="sxs-lookup"><span data-stu-id="a107c-121">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="a107c-122">4\.19.104 の WSL config を更新</span><span class="sxs-lookup"><span data-stu-id="a107c-122">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="a107c-123">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="a107c-123">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="a107c-124">*リリース日*:2019 年 11 月 12 日</span><span class="sxs-lookup"><span data-stu-id="a107c-124">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="a107c-125">[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard)。</span><span class="sxs-lookup"><span data-stu-id="a107c-125">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="a107c-126">これは 4.19.84 安定リリースです</span><span class="sxs-lookup"><span data-stu-id="a107c-126">This is the 4.19.84 stable release</span></span>

