---
title: 新しい WSL Linux ディストリビューションを初期化します。
description: WSL の Linux ディストリビューションをインストールした後、次の簡単な手順に従って初期化を完了します
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステム
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063610"
---
# <a name="initializing-a-newly-installed-distro"></a>新しくインストールされたディストリビューションの初期化
ディストリビューションをダウンロードしてインストールすると、新しいディストリビューションの初期化を完了する必要があります。

## <a name="launch-a-distro"></a>ディストリビューションを起動します。
を、新しくインストールされたディストリビューションの初期化を完了するには、新しいインスタンスを起動します。 Windows ストア アプリでは、「起動」ボタンをクリックするか、[スタート] メニューからディストリビューションを起動して、これを行うことができます。

> ヒント:最もよく使用されるディストリビューションに、[スタート] メニューやタスク バーにピン留めすることもできます。

![[スタート] メニューからディストリビューションを起動します。](media/start-menu.png)

> Windows Server で、実行可能ファイル、ディストリビューションのランチャーを起動できます`<distro>.exe`ディストリビューションのインストール フォルダーから。

最初に、新しくインストールされたディストリビューションで、実行、ウィンドウが開き、コンソールと、インストールが完了するは、2 分の待機を求められます。

> インストールのこの最終ステージ中にディストリビューションのファイルが圧縮解除され、使用できるように、PC に保存されています。 これは、に関するお客様の PC の記憶装置のパフォーマンスによっては 1 分以上かかる場合があります。 この最初のインストール フェーズは、ディストリビューションのクリーンアップ-installed - ときに必要なすべてから起動は 1 秒未満を実行する必要があります。

## <a name="setting-up-a-new-linux-user-account"></a>新しい Linux ユーザー アカウントを設定します。

インストールが完了するとは、新しいユーザー アカウント (とそのパスワード) を作成する促されます。 

![Windows コンソールでアンパック Ubuntu](media/UbuntuInstall.png)

このユーザー アカウントである必要が通常の非管理者ユーザーのしますのログインとして既定では、ディストリビューションを起動するときにします。

> 任意のユーザー名とパスワードを選択することができます - Windows ユーザー名に影響があるありません。 

ディストリビューションの新しいインスタンスを開くと、求められませんをパスワードが**プロセスを使用して、昇格する場合`sudo`、パスワードを入力する必要があります**ので、簡単に覚えやすいパスワードを選択することを確認します。 参照してください、[ユーザー サポート](user-support.md)詳細については、ページ。

## <a name="update--upgrade-your-distros-packages"></a>更新 (&)、ディストリビューションのパッケージのアップグレード

ほとんどのディストリビューションは、空または最小のパッケージのカタログで出荷されます。 パッケージのカタログを定期的に更新し、ディストリビューションの推奨されるパッケージ マネージャーを使用して、インストールされているパッケージのアップグレードを強くお勧めします。 Debian または Ubuntu 上には、apt が使用します。

```bash
sudo apt update && sudo apt upgrade
```

> Windows の更新またはアップグレード、Linux distro(s) は自動的に。これは、Linux ユーザーが自身を制御する優先するタスクです。

これで完了です。 WSL で、新しい Linux ディストリビューションを使用してお楽しみください! WSL の詳細については、他の確認[WSL docs](https://aka.ms/wsldocs)、または[WSL 学習リソース ページ](https://aka.ms/learnwsl)します。

![WSL で Linux を使用してお楽しみください。](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>トラブルシューティング

関連するエラーと推奨される修正方法を次に示します。 参照してください、 [WSL のトラブルシューティング ページ](troubleshooting.md)の他の一般的なエラーとその解決方法。

> **インストールに失敗しましたエラー 0x8007007e**システムがストアからの Linux をサポートしない場合、このエラーが発生します。  次のことを確認します。
> * 16215 またはそれ以降は、Windows ビルドを実行しています。 [ビルド確認](troubleshooting.md#check-your-build-number)します。
> * Linux の省略可能なコンポーネント用 Windows サブシステムが有効になっており、コンピューターが再起動します。  [WSL が有効になっていることを確認](troubleshooting.md#confirm-wsl-is-enabled)します。
