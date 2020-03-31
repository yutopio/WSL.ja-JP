---
title: WSL 1 から WSL 2 の UX の変更点
description: WSL 1 から WSL 2 のユーザー エクスペリエンスの変更点
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1965a22a2e290777b207d9ded099ce4a79e1ed38
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256335"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 から WSL 2 のユーザー エクスペリエンスの変更点

このページでは、WSL 1 と WSL 2 プレビューのユーザー エクスペリエンスの違いについて説明します。 注意すべき重要な変更点は次のとおりです。

- ファイルのパフォーマンスを高速化するには、Linux アプリからアクセスするファイルを Linux ルート ファイル システムに配置します
- WSL 2 プレビューの初期ビルドでは、localhost を使用せずに IP アドレスを使用してネットワーク アプリケーションにアクセスする必要があります

その他の変更の詳細な一覧は次のとおりです。

- WSL 2 には、ファイルの格納に [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) が使用されており、最大サイズに達した場合は拡張が必要になることがあります
- WSL 2 では、起動時に使用されるメモリが少なくなります
- 初期のプレビュー ビルドでは、OS 間のファイル アクセス速度が低下します

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Linux ルート ファイル システムに Linux ファイルを配置する
ファイルのパフォーマンスを向上させるには、Linux アプリケーションで頻繁にアクセスするファイルを Linux ルート ファイル システム内に配置します。 ファイル システムへのアクセスを高速化するには、このようなファイルを Linux ルート ファイル システム内に配置する必要があります。 また、Windows アプリから Linux ルート ファイル システムにアクセスできるようになりました (たとえば、エクスプローラーなどです。 Linux ディストリビューションのホーム ディレクトリで `explorer.exe .` を実行し、結果を確認してみてください)。この移行が非常に簡単になります。 

## <a name="accessing-network-applications"></a>ネットワーク アプリケーションへのアクセス
WSL 2 プレビューの初期ビルドでは、ホスト コンピューターの IP アドレスを使用して、Linux から Windows サーバーにアクセスする必要があります。

### <a name="accessing-windows-applications-from-linux"></a>Linux から Windows アプリケーションへのアクセス
Windows ネットワーク アプリケーションにアクセスするには、ホスト コンピューターの IP アドレスを使用する必要があります。 これを行うには、次の手順を実行します。

- コマンド `cat /etc/resolv.conf` を実行し、用語 `nameserver` に続く IP アドレスをコピーして、ホスト コンピューターの IP アドレスを取得します。 
- コピーした IP アドレスを使用して、Windows サーバーに接続します。

次の図は、これを実行するために、curl を介して Windows で実行されている Node.js サーバーに接続する例です。 

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a>Windows からの Linux アプリケーションへのアクセス

使用している Windows のバージョンによっては、仮想マシンの IP アドレスを取得する必要があります。 ビルドが 18945 以降の場合は、通常と同様に `localhost` を使用できます。 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a>[18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/) よりも前のビルドでの Linux へのアクセス

WSL ディストリビューションにサーバーがある場合は、ディストリビューションをホストしている仮想マシンの IP アドレスを見つけて、その IP アドレスで接続する必要があります。 これを行うには、次の手順を実行します。

- WSL ディストリビューション内でコマンド `ip addr` を実行して、ディストリビューションの IP アドレスを取得します。`eth0` インターフェイスの `inet` 値の下に表示されます。
   - この簡単に見つけるには、`ip addr | grep eth0` のように grep を使用してコマンドの出力をフィルター処理します。
- 前述の手順で見つけた IP を使用して Linux サーバーに接続します。

次の図は、これを実行するために、Edge ブラウザーを使用して Node.js サーバーに接続する例です。

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a>ネットワークに関するその他の考慮事項

#### <a name="connecting-via-remote-ip-addresses"></a>リモート IP アドレスを使用した接続

リモート IP アドレスを使用してアプリケーションに接続すると、ローカル エリア ネットワーク (LAN) からの接続として扱われます。 これは、アプリケーションで LAN 接続を受け入れることができるようにする必要があることを意味します。つまり、必要に応じて、`127.0.0.1` ではなく `0.0.0.0` にアプリケーションをバインドします。 たとえば、flask を使用する python では、コマンド `app.run(host='0.0.0.0')` を使用してこれを実行できます。 これらの変更を行うと、LAN からの接続が許可されるため、セキュリティに注意してください。 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>ローカル エリア ネットワーク (LAN) からの WSL2 ディストリビューションへのアクセス

WSL1 ディストリビューションを使用している場合、LAN からアクセスできるようにコンピューターが設定されていれば、WSL で実行されているアプリケーションに LAN からもアクセスできます。 これは WSL2 の既定の場合には該当しません。WSL2 には独自の IP アドレスを持つ仮想化されたイーサネット アダプターがあるからです。 現在、このワークフローを有効にするには、通常の仮想マシンの場合と同じ手順を実行する必要があります。 Microsoft は、このエクスペリエンスを改善する方法を検討しています。

#### <a name="ipv6-access"></a>IPv6 アクセス

WSL2 ディストリビューションは、現在、IPv6 のみのアドレスに到達できません。 Microsoft は、この機能の追加に取り組んでいます。

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>WSL 2 による VHD の使用と、最大サイズに達した場合の対処方法の概要
WSL 2 では、ext4 ファイル システムを使用する VHD 内にすべての Linux ファイルが格納されています。 この VHD は、ストレージのニーズに合わせて自動的にサイズが変更されます。 この VHD には、256 GB という初期の最大サイズもあります。 ディストリビューションが 256 GB を超えるサイズになると、ディスク領域が不足していることを示すエラーが表示されます。 VHD のサイズを拡張することで、これらの問題を解決できます。 その方法の手順は以下のとおりです。

1. `wsl --shutdown` コマンドを使用してすべての WSL インスタンスを終了します
2. "PackageFamilyName" というディストリビューションのインストール パッケージ名を見つけます
   - powershell プロンプトで、次のように入力します ("distro" はディストリビューション名です)。
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. WSL 2 のインストールで使用される VHD ファイルのファイルパスを特定します。これは "pathToVHD" になります。
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. 次のコマンドを実行して、WSL 2 VHD のサイズを変更します
   - 管理者特権でコマンド プロンプト ウィンドウを開き、次のコマンドを実行します。
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. WSL ディストリビューションを起動します
6. ファイル システムのサイズを拡張できることを WSL に認識させます
   - WSL ディストリビューションで次のコマンドを実行します。
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - /dev/sdXX のようなこのエントリの名前をコピーします (X は他の文字を表します)
      - `sudo resize2fs /dev/sdXX`
         - 以前の手順でコピーした値を必ず使用します。必要に応じて `apt install resize2fs` を使用する必要があります。

注意: 通常、Windows ツールまたはエディターを使用して、AppData フォルダー内にある WSL 関連ファイルを変更、移動、またはアクセスしないでください。 そうすると、Linux ディストリビューションが破損する可能性があります。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>起動時に WSL 2 に使用されるメモリ
WSL 2 では、実際の Linux カーネル上で軽量のユーティリティ VM が使用されており、ファイル システムの優れたパフォーマンスとシステム コールの完全な互換性を実現しているだけでなく、WSL 1 と同様の軽量、高速で、統合、応答性を備えています。 このユーティリティ VM のメモリ フットプリントは小さく、起動時に仮想アドレスでサポートされるメモリが割り当てられます。 これは総メモリのごく一部から始まるように構成されています。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>初期のプレビュー ビルドでは、OS 間のファイル速度が低下します
Linux アプリケーションから Windows ファイルにアクセスする場合、または Windows アプリケーションから Linux ファイルにアクセスする場合、WSL 1 と比較してファイル速度は遅いことがわかります。 これは WSL 2 のアーキテクチャの変更の結果であり、WSL チームはこのエクスペリエンスを改善する方法について積極的に調査しています。
