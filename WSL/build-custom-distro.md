---
title: WSL 用のカスタム Linux ディストリビューションを構築する
description: Windows Subsystem for Linux のカスタム Linux ディストリビューションを作成する方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows サブシステム、ディストリビューション、カスタム
ms.date: 09/15/2020
ms.topic: article
ms.openlocfilehash: 2882cccac6c34cd52529dbf7e42c8d35907d8241
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818704"
---
# <a name="creating-a-custom-linux-distribution-for-wsl"></a>WSL 用のカスタム Linux ディストリビューションの作成

オープンソースの WSL サンプルを使用して、Microsoft Store 用の WSL ディストリビューションパッケージを構築したり、サイドローディング用のカスタム Linux ディストリビューションパッケージを作成したりすることができます。 [ディストリビューションランチャーリポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)は GitHub で入手できます。

このプロジェクトでは、次のことが可能です。

- Linux ディストリビューションの管理パックは、WSL で実行される appx として Linux ディストリビューションをパッケージ化して送信します。
- 開発者が開発用コンピューターにサイドロードできるカスタム Linux ディストリビューションを作成する

## <a name="background"></a>背景

Microsoft Store を通じて、WSL 用の Linux ディストリビューションを UWP アプリケーションとして配布します。 これらのアプリケーションは、WSL-Windows カーネル内にあるサブシステムで実行できます。 この配信メカニズムには、 [前のブログ記事](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)で説明したように多くの利点があります。

## <a name="sideloading-a-custom-linux-distro-package"></a>カスタム Linux ディストリビューションパッケージのサイドローディング

カスタム Linux ディストリビューションパッケージをアプリケーションとして作成し、パーソナルコンピューターでサイドロードすることができます。 配布のメンテナンスツールとして送信しない限り、カスタムパッケージは Microsoft Store を通じて配布されないことに注意してください。
アプリをサイドロードするようにコンピューターを設定するには、[開発者向け] の [システム設定] でこれを有効にする必要があります。  開発者モードまたはサイドロードアプリが選択されていることを確認してください

## <a name="for-linux-distro-maintainers"></a>Linux ディストリビューションの場合

ストアに送信するには、発行の承認を受けるために microsoft と協力する必要があります。 ディストリビューションを Microsoft Store に追加することに関心がある Linux ディストリビューションの所有者は、にお問い合わせください wslpartners@microsoft.com 。

## <a name="getting-started"></a>作業の開始

[ディストリビューションランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)の指示に従って、カスタム Linux ディストリビューションパッケージを作成します。

## <a name="team-blogs"></a>チームのブログ

-  [Linux ディストリビューションの WSL サンプルをオープンソーシングカスタム Linux ディストリビューションの展開とサイドローディング](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
- [コマンドラインのブログ](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>フィードバックの提供

- [ディストリビューションランチャー GitHub リポジトリ](https://github.com/Microsoft/WSL-DistroLauncher)
- [GitHub issue tracker for WSL](https://github.com/Microsoft/BashOnWindows/issues)
