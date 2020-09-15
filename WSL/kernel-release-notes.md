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
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a>Linux 用 Windows サブシステム カーネルのリリース ノート

WSL 2 ディストリビューションのサポートが追加されました。ここでは、[完全な Linux カーネルが使用されます](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)。 この Linux カーネルはオープン ソースであり、そのソースコードは [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) リポジトリから入手できます。 この Linux カーネルは Microsoft Update を介してコンピューターに配信され、Windows イメージの一部として提供される Linux 用 Windows サブシステムの個別のリリース スケジュールに従います。

## <a name="419128-microsoft-standard"></a>4.19.128-microsoft-standard
*リリース日*:プレリリース、手動インストールにより入手可能

[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard)。

* これは 4.19.128 の安定リリースです
* dxgkrnl ドライバーの IOCTL メモリの破損を修正

## <a name="419121-microsoft-standard"></a>4.19.121-microsoft-standard
*リリース日*:プレリリース

[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard)。

* ドライバー: hv: vmbus: dxgkrnl をフック
* GPU コンピューティングに対するサポートの追加

## <a name="419104-microsoft-standard"></a>4.19.104-microsoft-standard
*リリース日*:2020 年 6 月 9 日 

[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard)。

* 4\.19.104 の WSL config を更新

## <a name="41984-microsoft-standard"></a>4.19.84-microsoft-standard
*リリース日*:2019 年 11 月 12 日 

[公式の GitHub リリース リンク](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard)。

* これは 4.19.84 安定リリースです

