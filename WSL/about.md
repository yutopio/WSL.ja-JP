---
title: Linux 用 Windows サブシステムの概要
description: Linux 用 Windows サブシステムとそのさまざまなバージョン、およびそれらの使用方法について説明します。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 75da6389beec4af7ac684ec7ee2ef31431e14071
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336065"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a>Linux 用 Windows サブシステムとは

Linux 用 Windows サブシステムを使用すると、開発者は、従来の仮想マシンまたはデュアルブート セットアップのオーバーヘッドなしで、ほとんどのコマンド ライン ツール、ユーティリティ、アプリケーションを含む GNU/Linux 環境を変更せずそのまま Windows 上で直接実行できます。

次の操作を行います。

* [Microsoft Store から](https://aka.ms/wslstore)好みの GNU/Linux ディストリビューションを選択します。
* `grep`、`sed`、`awk` などの一般的なコマンドライン ツールや、その他の ELF-64 バイナリを実行します。
* 以下のような Bash シェル スクリプトや GNU/Linux コマンド ライン アプリケーションを実行します。  
    * ツール: vim、emacs、tmux
    * 言語:[Node.js](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2)、JavaScript、[Python](https://docs.microsoft.com/windows/python/web-frameworks)、Ruby、C/C++、C# & F#、Rust、Go など
    * サービス:SSHD、MySQL、Apache、lighttpd、[MongoDB](https://docs.microsoft.com/windows/nodejs/databases)、[PostgreSQL](https://docs.microsoft.com/windows/python/databases)。
* 独自の GNU/Linux ディストリビューション パッケージ マネージャーを使用して、追加のソフトウェアをインストールします。
* Unix に似たコマンド ライン シェルを使用して Windows アプリケーションを起動します。
* Windows で GNU/Linux アプリケーションを起動します。

## <a name="what-is-wsl-2"></a>WSL 2 とは

WSL 2 は、Linux 用 Windows サブシステムが Windows 上で ELF64 Linux バイナリを実行できるようにする、Linux 用 Windows サブシステム アーキテクチャの新しいバージョンです。 その主な目標は、**ファイル システムのパフォーマンスを向上させること**と、**システム コールの完全な互換性**を追加することです。

この新しいアーキテクチャによって、こうした Linux バイナリと、Windows やお使いのコンピューターのハードウェアとの対話方法は変わりますが、ユーザー エクスペリエンスは WSL 1 (現在幅広く利用されているバージョン) と同じです。

個々の Linux ディストリビューションは、WSL 1 または WSL 2 アーキテクチャで実行できます。 各ディストリビューションはいつでもアップグレードまたはダウングレードできます。また、WSL 1 ディストリビューションと WSL 2 ディストリビューションをサイド バイ サイドで実行することができます。 WSL 2 には、実際の Linux カーネルを実行することによるメリットが得られるまったく新しいアーキテクチャが使用されています。

## <a name="next-steps"></a>次の手順

* [WSL 1 をインストールし、WSL 2 に更新する](./install-win10.md)

* [WSL 2 と WSL 1 を比較する](./compare-versions.md)

* [新しい Linux ディストリビューションのユーザー アカウントとパスワードを作成する](./user-support.md)

* [よく寄せられる質問を読む](./faq.md)

* [WSL 2 に関してよく寄せられる質問を読む](./wsl2-faq.md)

* [トラブルシューティング](./troubleshooting.md)

* [Windows と Linux の間で相互運用性コマンドを実行する](./interop.md)

* [起動コマンドと構成を実行する](./wsl-config.md)

* [ファイルのアクセス許可を設定する](./file-permissions.md)

* [エンタープライズ向けの WSL を設定する](./enterprise.md)

* [WSL コマンドのリファレンスを見る](./reference.md)

* [カスタム ディストリビューションを作成する](./build-custom-distro.md)

* [WSL のリリース ノートを読む](./release-notes.md)
