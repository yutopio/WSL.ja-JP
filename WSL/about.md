---
title: Linux 用 Windows サブシステムについて説明します
description: Windows Subsystem for Linux が動作する方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、gnu、linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: ad582d1b3a3d4277ee1b9b7adb0dc63a644abce9
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "59529066"
---
# <a name="windows-subsystem-for-linux-documentation"></a>Linux のドキュメント用の Windows サブシステム

Windows Subsystem for Linux では、Windows、未変更の状態で仮想マシンのオーバーヘッドなしで直接開発者のほとんどのコマンド ライン ツール、ユーティリティ、およびアプリケーションを含む--Gnu/linux 環境を実行することができます。  

可能な代替手段としては以下の方法があります。

1. お気に入りの GNU/Linux ディストリビューションを選択[Windows ストアから](https://aka.ms/wslstore)します。
1. 一般的なコマンド ライン無料のソフトウェアを実行します。 `grep`、 `sed`、 `awk`、またはその他の ELF 64 バイナリ。 
1. Bash シェル スクリプトとを含む Gnu/linux コマンド ライン アプリケーションを実行します。  
    * ツール: vim、emacs、tmux
    * 言語：Javascript/node.js、Ruby、Python、C/C++、 C# & F#、信頼、移動など。
    * サービス: sshd、MySQL、Apache、lighttpd
1. 独自の GNU/Linux 配布パッケージ マネージャーを使用して追加のソフトウェアをインストールします。
1. Unix のようなコマンド ライン シェルを使用して Windows アプリケーションを起動します。
1. Windows 上の Gnu/linux アプリケーションを呼び出します。

## <a name="getting-started"></a>概要

* [Windows 上の Linux をインストールします。](install_guide.md)
* [コマンドのリファレンスを参照してください。](reference.md)
* [読み取りについてよく寄せられる質問](faq.md)

## <a name="team-blogs"></a>チームのブログ
*  [ビデオとブログのコレクションでの概要の投稿](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* [コマンド ライン ブログ](https://blogs.msdn.microsoft.com/commandline/)(アクティブ)
* [Linux ブログ用 Windows サブシステム](https://blogs.msdn.microsoft.com/wsl/)(履歴)

## <a name="posts--articles"></a>投稿と記事
* [実行の Bash on Ubuntu on Windows](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [開発者は Windows 10 の Bash と Usermode Ubuntu Linux のバイナリを実行できます。](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [Ubuntu on Windows: Windows 開発者向けの Ubuntu 空間](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a>ご意見とご感想
* [GitHub の issue トラッカー](https://github.com/Microsoft/BashOnWindows/issues)
* [コマンド ライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
