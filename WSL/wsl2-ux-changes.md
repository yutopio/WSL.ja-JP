---
title: WSL 1 と 2 WSL UX の変更点
description: WSL 1 と 2 の WSL の間のユーザー エクスペリエンスの変更
keywords: BashOnWindows、bash、wsl、wsl2、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステム
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038102"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 と 2 の WSL の間のユーザー エクスペリエンスの変更

このページ WSL 1 と WSL 2 プレビューのユーザー エクスペリエンスの違いを経由します。 注意すべき主な変更は。

- Linux ルート ファイル システムに高速ファイル パフォーマンスの速度は、Linux アプリにアクセスするファイルを配置します。
- WSL 2 プレビューの初期のビルドでは、IP アドレスを使用して、localhost を使用していないネットワーク アプリケーションにアクセスする必要があります。

お気付きの他の変更の完全な一覧を次に示します。

- WSL 2 は、VHD を使用してファイルを格納する、その最大サイズに達した場合は、展開する必要があります。
- WSL 2 がメモリの小さな割合を使用して今すぐ起動する場合、
- クロス OS ファイル アクセスの速度は初期のプレビュー ビルドの速度は遅くなります

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Linux ファイルを Linux のルート ファイル システムに配置します。
Linux で頻繁にアクセスするファイルを配置することを確認、Linux 内のアプリケーションのルート ファイル システム、ファイルのパフォーマンスのメリットを活用します。 これらのファイルは、ファイル システムより高速にアクセスするためには、Linux ルート ファイル システムの内側に配置する必要があります。 私たちがもできるように (ファイル エクスプ ローラーのような Linux ルート ファイル システムにアクセスする Windows アプリ! 実行してみてください: `explorer.exe /` bash シェルとどうなるでしょうか) この移行を大幅に簡素化することはできます。 

## <a name="accessing-network-applications"></a>ネットワーク アプリケーションにアクセスします。
WSL 2 プレビューの初期のビルドでは、Linux ディストリビューションと、ホスト コンピューターの IP アドレスを使用して Linux から任意の Windows サーバーの IP アドレスを使用して Windows から任意の Linux サーバーにアクセスする必要があります。 これは、一時、および、優先順位の一覧を修正するには非常に高いのあるものです。

### <a name="accessing-linux-applications-from-windows"></a>Windows から Linux アプリケーションへのアクセス
WSL ディストリビューションで、サーバーがある場合は、ディストリビューションの電源、仮想マシンの IP アドレスを見つけて、その IP アドレスで接続する必要があります。 次の手順で行うことができます。

- コマンドを実行して、ディストリビューションの IP アドレスを取得する`ip addr`、WSL ディストリビューションと下の検索の内部で、`inet`の値、`eth0`インターフェイス。
   - 正規表現を使用して、コマンドの出力のフィルター処理をより簡単に表示できるようになります:`ip addr | grep eth0`します。
- 上記で見つかった ip アドレスを使用して Linux サーバーに接続します。

次の図は、Edge ブラウザーを使って nodeJS サーバーに接続することで、この例を示します。

![Windows から Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>Linux から Windows アプリケーションにアクセスします。
Windows ネットワーク アプリケーションへのアクセスには、ホスト コンピューターの IP アドレスを使用する必要があります。 次の手順を行うことができます。

- コマンドを実行して、ホスト コンピューターの IP アドレスを取得`cat /etc/resolv.conf`という用語を次の IP アドレスをコピーおよび`nameserver`します。 
- コピー元の IP アドレスを使用して任意の Windows サーバーに接続します。

次の図は、curl を使用して、Windows で実行されている python のサーバーに接続して、この例を示します。 

![Windows から Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>VHD、およびその最大サイズに達した場合の対処方法を使用して WSL 2 を理解します。
WSL 2 では、ext4 ファイル システムを使用する VHD 内のすべての Linux ファイルを格納します。 この VHD は、記憶域のニーズを満たすために自動的にサイズ変更します。 この VHD には、256 GB の初期の最大サイズもあります。 256 GB を超えるサイズで、ディストリビューションが増加する場合は、ディスク領域不足を実行したことを示すエラーが表示されます。 VHD のサイズを拡張することで、これらを修正することができます。 これを行う方法については次に示します。

1. 使用してすべての WSL インスタンスを終了、`wsl --shutdown`コマンド
2. 次のコマンドを実行して、WSL 2 の VHD のサイズを変更します。
   - 管理者特権でコマンド プロンプト ウィンドウを開きし、次のコマンドを実行します。
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. WSL、ディストリビューションを起動します。
4. WSL のファイル システムのサイズを展開できることを認識します。
   - WSL ディストリビューションでは、これらのコマンドを実行します。
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - ようになりますが、このエントリの名前をコピー:/開発/sdXX (X 印が付いた他の任意の文字を表す)
      - `sudo resize2fs /dev/sdXX`
         - 値を使用して、先ほどコピーした、使用する必要があるかどうかを確認します。`apt install resize2fs`します。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 は、メモリの一部を使用して起動時には
WSL 2 では、実際の Linux カーネルで軽量ユーティリティ VM を使用して、優れたファイル システムのパフォーマンスとフル システム呼び出しがまだ中に、光と同様の互換性高速で統合や WSL 1 と応答性を提供します。 このユーティリティの VM は、メモリ使用量を備えは起動時にバックアップされた仮想アドレスのメモリを割り当てます。 合計メモリの小さな割合を開始する構成されます。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>クロス OS ファイルの速度は初期のプレビュー ビルドの速度は遅くなります
Linux アプリケーションの場合は、または Windows アプリケーションから Linux ファイルへのアクセスから Windows ファイルにアクセスするときに WSL 1 と比較ファイルの速度が遅くなることがわかります。 これは WSL 2 では、アーキテクチャの変更の結果であり、WSL チームが積極的には、このエクスペリエンスを向上させる方法を調査します。