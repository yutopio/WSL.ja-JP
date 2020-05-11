---
title: WSL 2 Linux カーネルの更新
description: WSL 2 Linux カーネルを手動で更新するための手順
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: a1a2f23fb05c426f80878e12e82026a96c71354e
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "79447742"
---
# WSL 2 Linux カーネルの更新

WSL 2 内の Linux カーネルを手動で更新するには、次の手順に従ってください。

## Linux カーネル更新プログラム パッケージをダウンロードする

[このリンク](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)をクリックして、x64 マシン用の最新の WSL2 Linux カーネル更新プログラム パッケージをダウンロードしてください。

> [!NOTE] 
> ARM64 マシンを使用している場合は、代わりに[このパッケージ](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)をダウンロードしてください。

## Linux カーネル更新プログラム パッケージをインストールする

Linux カーネル更新パッケージをインストールするには、次の手順に従ってください。

    1. 前の手順でダウンロードした更新プログラム パッケージを実行します。
    2. 管理者特権のアクセス許可の入力が求められます。このインストールを承認するには、[はい] を選択します。
    3. インストールが完了したら、WSL2 の使用を開始できます。
    
## WSL2 Linux カーネルの更新に関する今後の計画

これらの変更の詳細については、[Windows コマンド ライン ブログ](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)の[このブログ記事](https://aka.ms/cliblog)をお読みください。
