---
title: WSL 用、カスタムの Linux ディストリビューションでのビルドします。
description: Linux 用 Windows サブシステムのカスタムの Linux ディストリビューションを作成する方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows サブシステム、ディストリビューション、カスタム
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063260"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>WSL のカスタムの Linux ディストリビューションの作成

Microsoft Store の WSL ディストリビューションのパッケージをビルドおよびサイドロード用のカスタムの Linux ディストリビューションのパッケージを作成する、オープン ソース WSL サンプルを使用します。 検索することができます、[ディストリビューション ランチャー リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)GitHub でします。

このプロジェクトが有効にします。
* パッケージ化し、として、appx WSL で実行されている Linux ディストリビューションを送信する Linux ディストリビューションのメンテナンス
* 開発者は開発用コンピューターにサイドロードできるカスタムの Linux ディストリビューションの作成

## <a name="background"></a>背景
Microsoft Store 経由での UWP アプリケーションとして WSL の Linux ディストリビューションを配布します。 WSL - Windows カーネルに配置されるサブシステムで実行し、それらのアプリケーションをインストールすることができます。 この配信メカニズムは、以前のブログ投稿で説明したように、多くのメリットが。

## <a name="sideloading-a-custom-linux-distro-package"></a>カスタムの Linux ディストリビューションのパッケージのサイドロード
パーソナル コンピューターにサイドローディングするアプリケーションとして、カスタムの Linux ディストリビューションのパッケージを作成できます。 カスタム パッケージは配布されません Microsoft Store を介して配布 maintainer として送信する場合を除きに注意してください。
アプリをサイドロードするコンピューターを設定するには"For Developers"の下のシステム設定でこれを有効にする必要があります。  開発者モード、または選択したアプリのサイドロードをいずれかが必要

## <a name="for-linux-distro-maintainers"></a>Linux ディストリビューションで、管理者や
ストアに送信するには発行の承認を受信するという点で協力する必要があります。 Microsoft Store へのお使いのディストリビューションの追加対象の Linux ディストリビューションの所有者は場合に、お問い合わせくださいwslpartners@microsoft.comします。

## <a name="getting-started"></a>作業の開始
指示に従って、[ディストリビューション ランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)カスタム Linux ディストリビューションのパッケージを作成します。

 
## <a name="team-blogs"></a>チームのブログ
*  [Linux ディストリビューションのメンテナンスとサイドローディング カスタム Linux ディストリビューション用の WSL サンプルのソーシングを開く](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [コマンド ラインのブログ](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>ご意見とご感想
* [ディストリビューション ランチャー Gitub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)
* [WSL の GitHub の issue トラッカー](https://github.com/Microsoft/BashOnWindows/issues)
* [コマンド ライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
