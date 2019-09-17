---
title: WSL 1 と WSL 2 の間での UX の変更
description: WSL 1 と WSL 2 間のユーザーエクスペリエンスの変更
keywords: BashOnWindows、bash、wsl、wsl2、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3addfd27d777731bf92efab42c6bcd4be415779b
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020967"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 と WSL 2 間のユーザーエクスペリエンスの変更

このページでは、WSL 1 と WSL 2 preview のユーザーエクスペリエンスの違いについて紹介します。 注意すべき重要な変更点は次のとおりです。

- Linux アプリが Linux ルートファイルシステムにアクセスするファイルを配置して、ファイルのパフォーマンスを高速化します。
- WSL 2 preview の初期ビルドでは、localhost を使用せずに IP アドレスを使用してネットワークアプリケーションにアクセスする必要があります。

次に、その他の変更点の一覧を示します。

- WSL 2 では、[仮想ハードウェアディスク](https://en.wikipedia.org/wiki/VHD_(file_format))(VHD) を使用してファイルを格納します。最大サイズに達した場合は、拡張が必要になることがあります。
- 開始時に WSL 2 では、メモリの割合がわずかに使用されるようになりました。
- 最初のプレビュービルドで、OS 間のファイルアクセス速度が低下する

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Linux のルートファイルシステムに Linux ファイルを配置する
ファイルのパフォーマンスを向上させるために、linux アプリケーションで頻繁にアクセスするファイルを linux ルートファイルシステム内に配置してください。 これらのファイルは、ファイルシステムへのアクセスを高速化するために、Linux ルートファイルシステム内に存在する必要があります。 また、Windows アプリが Linux ルートファイルシステム (エクスプローラーなど) にアクセスできるようになりました。 Linux ディストリビューションの`explorer.exe .`ホームディレクトリでを実行してみてください。これにより、この移行が大幅に簡単になります。 

## <a name="accessing-network-applications"></a>ネットワークアプリケーションへのアクセス
WSL 2 preview の最初のビルドでは、Linux ディストリビューションの IP アドレスと、ホストコンピューターの IP アドレスを使用して Linux から任意の Windows server を使用して、Windows から任意の Linux サーバーにアクセスする必要があります。 これは一時的なものであり、修正する優先順位リストでは非常に高くなっています。

### <a name="accessing-linux-applications-from-windows"></a>Windows からの Linux アプリケーションへのアクセス
WSL ディストリビューションにサーバーがある場合は、ディストリビューションの電源を入れている仮想マシンの IP アドレスを検索し、その IP アドレスを使用して接続する必要があります。 これを行うには、次の手順を実行します。

- Wsl ディストリビューション内でコマンドを実行し、 `ip addr` `eth0`インターフェイスの`inet`値の下でそのコマンドを見つけることによって、ディストリビューションの IP アドレスを取得します。
   - これは、のように`ip addr | grep eth0`grep を使用してコマンドの出力をフィルター処理することで、より簡単に見つけることができます。
- 上記の IP を使用して、Linux サーバーに接続します。

次の図は、Edge ブラウザーを使用して node.js サーバーに接続することによって、この例を示しています。

![Windows からの Linux ネットワークアプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>Linux からの Windows アプリケーションへのアクセス
Windows ネットワークアプリケーションにアクセスするには、ホストコンピューターの IP アドレスを使用する必要があります。 これを行うには、次の手順を実行します。

- コマンド`cat /etc/resolv.conf`を実行し、という用語`nameserver`の後に ip アドレスをコピーして、ホストコンピューターの ip アドレスを取得します。 
- コピーした IP アドレスを使用して、任意の Windows サーバーに接続します。

次の図は、curl を介して Windows で実行されている node.js サーバーに接続することによって、この例を示しています。 

![Windows からの Linux ネットワークアプリケーションへのアクセス](media/wsl2-network-l2w.png)

### <a name="other-networking-considerations"></a>ネットワークに関するその他の考慮事項

リモート IP アドレスを使用してアプリケーションに接続すると、ローカルエリアネットワーク (LAN) からの接続として扱われます。 つまり、アプリケーションが LAN 接続を受け入れることができることを確認する必要があります。次に例を示します。`0.0.0.0` の`127.0.0.1`代わりに、アプリケーションをにバインドすることが必要になる場合があります。 たとえば、flask を使用した python では、コマンド`app.run(host='0.0.0.0')`を使用してこれを行うことができます。 これらの変更を行う場合は、LAN からの接続が許可されるため、セキュリティを考慮してください。 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>WSL 2 を理解すると、VHD が使用され、最大サイズに達した場合の対処方法がわかります。
WSL 2 では、ext4 ファイルシステムを使用する VHD 内にすべての Linux ファイルが格納されます。 この VHD は、ストレージのニーズに合わせて自動的にサイズ変更されます。 この VHD には、256 GB の初期の最大サイズもあります。 ディストリビューションのサイズが 256 GB よりも大きくなると、ディスク領域が不足していることを示すエラーが表示されます。 VHD のサイズを拡張することで、これらの問題を解決できます。 その方法については、以下を参照してください。

1. コマンドを使用してすべての`wsl --shutdown` wsl インスタンスを終了します
2. ディストリビューションのインストールパッケージ名 ' 整理 Efamilyname ' を検索します
   - Powershell プロンプトで、次のように入力します (' distribution ' は配布名です)。
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. WSL 2 のインストールで使用される VHD ファイルの場所を特定します。これは ' pathToVHD ' になります。
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. 次のコマンドを実行して、WSL 2 VHD のサイズを変更します。
   - 管理者特権でコマンドプロンプトウィンドウを開き、次のコマンドを実行します。
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. WSL ディストリビューションを起動します
6. ファイルシステムのサイズを拡張できることを WSL に認識させる
   - WSL ディストリビューションで次のコマンドを実行します。
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - このエントリの名前をコピーします。次のようになります (X は他の文字を表します)。
      - `sudo resize2fs /dev/sdXX`
         - 前の手順`apt install resize2fs`でコピーした値を使用してください。を使用する必要がある場合があります。

注意:通常は、Windows のツールまたはエディターを使用して、AppData フォルダー内にある WSL 関連ファイルを変更、移動、またはアクセスしないでください。 これにより、Linux ディストリビューションが破損する可能性があります。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 は起動時にメモリを使用します
WSL 2 は、実際の Linux カーネル上で軽量のユーティリティ VM を使用して、優れたファイルシステムのパフォーマンスとシステムコールの完全な互換性を実現しながら、WSL 1 と同じようにライト、高速、統合、応答性を提供します。 このユーティリティ VM ではメモリフットプリントが小さく、起動時に仮想アドレスがサポートされるメモリが割り当てられます。 これは、メモリの合計のごく一部から開始するように構成されています。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>最初のプレビュービルドで、OS 間のファイル速度が遅くなる
Linux アプリケーションから Windows ファイルにアクセスする場合、または Windows アプリケーションから Linux ファイルにアクセスする場合は、WSL 1 と比較してファイルの速度が遅いことがわかります。 これは、WSL 2 でのアーキテクチャの変更の結果であり、WSL チームがこのエクスペリエンスを向上させる方法について積極的に調査しているものです。
