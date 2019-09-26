---
title: WSL 用のカスタム Linux ディストリビューションを構築する
description: Windows Subsystem for Linux のカスタム Linux ディストリビューションを作成する方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows サブシステム、ディストリビューション、カスタム
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 181badd4ee2f69e904099c12b54dfbdf3a37e294
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269700"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>WSL 用のカスタム Linux ディストリビューションの作成

オープンソースの WSL サンプルを使用して、Microsoft Store 用の WSL ディストリビューションパッケージを構築したり、サイドローディング用のカスタム Linux ディストリビューションパッケージを作成したりすることができます。 [ディストリビューションランチャーリポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)は GitHub で入手できます。

このプロジェクトでは、次のことが可能です。
* Linux ディストリビューションの管理パックは、WSL で実行される appx として Linux ディストリビューションをパッケージ化して送信します。
* 開発者が開発用コンピューターにサイドロードできるカスタム Linux ディストリビューションを作成する

## <a name="background"></a>背景情報
Microsoft Store を通じて、WSL 用の Linux ディストリビューションを UWP アプリケーションとして配布します。 これらのアプリケーションは、WSL-Windows カーネル内にあるサブシステムで実行できます。 この配信メカニズムには、[前のブログ記事](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)で説明したように多くの利点があります。

## <a name="sideloading-a-custom-linux-distro-package"></a>カスタム Linux ディストリビューションパッケージのサイドローディング
カスタム Linux ディストリビューションパッケージをアプリケーションとして作成し、パーソナルコンピューターでサイドロードすることができます。 配布のメンテナンスツールとして送信しない限り、カスタムパッケージは Microsoft Store を通じて配布されないことに注意してください。
アプリをサイドロードするようにコンピューターを設定するには、[開発者向け] の [システム設定] でこれを有効にする必要があります。  開発者モードまたはサイドロードアプリが選択されていることを確認してください

## <a name="for-linux-distro-maintainers"></a>Linux ディストリビューションの場合
ストアに送信するには、発行の承認を受けるために microsoft と協力する必要があります。 ディストリビューションを Microsoft Store に追加することに関心がある Linux ディストリビューションの所有者は、 wslpartners@microsoft.comにお問い合わせください。

## <a name="getting-started"></a>作業の開始
[ディストリビューションランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)の指示に従って、カスタム Linux ディストリビューションパッケージを作成します。

 
## <a name="team-blogs"></a>チームのブログ
*  [Linux ディストリビューションの WSL サンプルをオープンソーシングカスタム Linux ディストリビューションの展開とサイドローディング](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [コマンドラインのブログ](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>ご意見とご感想
* [ディストリビューションランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)
* [GitHub issue tracker for WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [コマンドライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
