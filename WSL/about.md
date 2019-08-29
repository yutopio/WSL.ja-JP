---
title: Windows Subsystem for Linux の詳細
description: Windows Subsystem for Linux の動作の詳細については、こちらを参照してください。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、gnu、linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c8e3b3f7ec13109485d7efa29739dadc8bfacf7
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122668"
---
# <a name="windows-subsystem-for-linux-documentation"></a>Linux 用 Windows サブシステムのドキュメント

Windows Subsystem for Linux を使用すると、開発者は、ほとんどのコマンドラインツール、ユーティリティ、アプリケーションを含む GNU/Linux 環境を、変更されていない状態で、仮想マシンのオーバーヘッドなしで、Windows 上で直接実行できます。  

可能な代替手段としては以下の方法があります。

1. [Microsoft Store から、使い慣れた](https://aka.ms/wslstore)GNU/Linux ディストリビューションを選択します。
1. 、、 `sed`、またはその他の ELF-64 バイナリなどの一般的なコマンドラインフリーソフトウェアを実行します。 `awk` `grep` 
1. 次のような Bash シェルスクリプトと GNU/Linux コマンドラインアプリケーションを実行します。  
    * ツール: vim、emacs、tmux
    * 言語：Javascript/node.js、Ruby、Python、C/C++、 C# & F#、Rust、ゴーなど。
    * サービス: sshd、MySQL、Apache、ライト tpd
1. 独自の GNU/Linux ディストリビューションパッケージマネージャーを使用して、追加のソフトウェアをインストールします。
1. Unix に似たコマンドラインシェルを使用して Windows アプリケーションを起動します。
1. Windows で GNU/Linux アプリケーションを起動します。

## <a name="getting-started"></a>作業の開始

* [Windows 10 に Linux をインストールする](install-win10.md)
* [コマンドリファレンスを参照してください。](reference.md)
* [よく寄せられる質問を読む](faq.md)

## <a name="team-blogs"></a>チームのブログ
*  [ビデオとブログのコレクションを使用した投稿の概要](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* [コマンドラインのブログ](https://blogs.msdn.microsoft.com/commandline/)能動的
* [Linux 用 Windows サブシステムのブログ](https://blogs.msdn.microsoft.com/wsl/)経緯

## <a name="posts--articles"></a>投稿 & 記事
* [Windows で Bash on Ubuntu を実行する](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [開発者は Windows 10 で Bash およびモード Ubuntu Linux バイナリを実行できます。](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [Windows 上の ubuntu – Windows 開発者向けの Ubuntu](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a>ご意見とご感想
* [GitHub の問題の追跡ツール](https://github.com/Microsoft/BashOnWindows/issues)
* [コマンドライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
