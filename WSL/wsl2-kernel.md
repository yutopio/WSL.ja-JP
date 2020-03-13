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
# <a name="updating-the-wsl-2-linux-kernel"></a>WSL 2 Linux カーネルを更新しています

WSL 2 内の Linux カーネルを手動で更新するには、次の手順に従ってください。 

## <a name="download-the-linux-kernel-update-package"></a>Linux カーネル更新パッケージをダウンロードする

AMD64 マシン用の最新の WSL2 Linux カーネル更新パッケージをダウンロードするには、[このリンク](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)をクリックしてください。

> [!NOTE] ARM64 マシンを使用している場合は、代わりに[このパッケージ](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)をダウンロードしてください。

## <a name="install-the-linux-kernel-update-package"></a>Linux カーネル更新パッケージをインストールする

Linux カーネル更新パッケージをインストールするには、次のようにします。
    1. 前の手順でダウンロードした更新プログラムパッケージを実行します。
    2. 昇格したアクセス許可を求められます。このインストールを承認するには、[はい] を選択してください。
    3. インストールが完了したら、WSL2 の使用を開始できます。

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>WSL2 Linux カーネルを更新するための今後の計画

これらの変更の詳細については、 [Windows コマンドラインブログ](https://aka.ms/cliblog)のこちらの[ブログ](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)記事をお読みください。