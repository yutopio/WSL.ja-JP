---
title: WSL 2 Linux カーネルの更新
description: WSL 2 Linux カーネルを手動で更新するための手順
keywords: wsl, windows, linux カーネル, linux 用 windows サブシステム, カーネル
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153052"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>WSL 2 Linux カーネルの更新

WSL 2 内の Linux カーネルを手動で更新するには、次の手順に従ってください。

> [!NOTE] 
> インストーラーで WSL 1 が見つからない場合は、Linux カーネル更新プログラムのインストーラーを右クリックして [アンインストール] をクリックし、インストーラーを再実行します。

## <a name="download-the-linux-kernel-update-package"></a>Linux カーネル更新プログラム パッケージをダウンロードする

x64 マシン用の[最新の WSL2 Linux カーネル更新プログラム パッケージをダウンロード](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)してください。

> [!NOTE]
> ARM64 マシンを使用している場合は、代わりに [ARM64 パッケージ](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)をダウンロードしてください。

## <a name="install-the-linux-kernel-update-package"></a>Linux カーネル更新プログラム パッケージをインストールする

Linux カーネル更新パッケージをインストールするには、次の手順に従ってください。

  1. 前の手順でダウンロードした更新プログラム パッケージを実行します。

  2. 管理者特権のアクセス許可の入力が求められます。このインストールを承認するには、[はい] を選択します。

  3. インストールが完了したら、WSL2 の使用を開始できます。

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>WSL2 Linux カーネルの更新に関する今後の計画

詳細については、[Windows コマンドラインのブログ](https://aka.ms/cliblog)にある[WSL2 Linux カーネルの更新プログラムに対する変更](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)に関するページを参照してください。
