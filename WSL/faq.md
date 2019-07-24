---
title: よく寄せられる質問 (FAQ)
description: Windows Subsystem for Linux に関してよく寄せられる質問。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 2bbcec661146fcb570209fd895e6543657e98996
ms.sourcegitcommit: 939fe561d178454219adbee96c0ad3f768db2208
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2019
ms.locfileid: "67237391"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Windows Subsystem for Linux に関してよく寄せられる質問

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Windows Subsystem for Linux (WSL) とは
Windows Subsystem for Linux (WSL) は、windows 10 の新しい機能であり、従来の Windows デスクトップや最新のストアアプリと並行して、ネイティブの Linux コマンドラインツールを Windows で直接実行できます。

詳細については、[[バージョン情報] ページ](./about.md)を参照してください。

## <a name="who-is-wsl-for"></a>WSL の対象ユーザー
これは、主に開発者向けのツールであり、特に web 開発者と、オープンソースプロジェクトで作業している開発者を対象としています。 これにより、Bash、一般的な linux ツール (`sed`、 `awk`など) と多くの linux ファーストツール (Ruby、Python など) を使用する必要があるユーザーは、Windows でそのツールチェーンを使用できます。

## <a name="what-can-i-do-with-wsl"></a>WSL でできること
WSL は、Bash という名前のアプリケーションを提供します。このアプリケーションを開始すると、Bash シェルを実行している Windows コンソールが開きます。 Bash を使用すると、コマンドラインの Linux ツールとアプリを実行できます。 たとえば、「」 `lsb_release -a`と入力して enter キーを押すと、現在実行中の Linux ディストリビューションの詳細が表示されます。

![ディストリビューションの詳細のスクリーンショット](media/distro.png)

Linux Bash シェル内からローカルコンピューターのファイルシステムにアクセスすることもできます。ローカルドライブはフォルダーの`/mnt`下にマウントされています。 たとえば、 `C:`ドライブは`/mnt/c`次のようにマウントされます。  

![マウントされた C ドライブのスクリーンショット](media/ls.png)

## <a name="what-is-bash"></a>Bash とは
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)は、広く使われているテキストベースのシェルとコマンド言語です。 これは、Ubuntu とその他の Linux ディストリビューション、および macOS に含まれる既定のシェルです。 ユーザーは、シェルにコマンドを入力してスクリプトを実行したり、コマンドやツールを実行したりして、多くのタスクを実行します。

## <a name="how-does-this-work"></a>この処理のしくみ
基になるテクノロジの詳細については、こちらの[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください。

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>VM で Linux ではなく WSL を使用するのはなぜですか。
WSL が必要とするリソース (CPU、メモリ、およびストレージ) は、完全な仮想マシンよりも少なくなります。 また、WSL を使用すると、Linux のコマンドラインツールとアプリを Windows コマンドライン、デスクトップアプリ、ストアアプリと共に実行し、Linux 内から Windows ファイルにアクセスすることもできます。 これにより、必要に応じて、同じファイルセットで Windows アプリと Linux コマンドラインツールを使用できます。

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>たとえば、Windows ではなく Linux で Ruby を使用するのはなぜですか。
一部のクロスプラットフォームツールは、それらが実行される環境が Linux のように動作することを前提として構築されました。 たとえば、一部のツールでは、非常に長いファイルパスにアクセスできること、または特定のファイルやフォルダーが存在することを前提としています。 多くの場合、Linux とは動作が異なる Windows で問題が発生します。

多くの場合、Ruby や node のような多くの言語は、Windows 上ではに移植され、優れた動作をします。 ただし、すべての Ruby Gem または node/NPM ライブラリ所有者が、Windows をサポートするためにライブラリを移植するわけではありません。また、多くの場合、Linux 固有の依存関係があります。 多くの場合、このようなツールやライブラリを使用して構築されたシステムは、ビルドから悪影響を受ける可能性があります。また、Windows で実行時エラーや望ましくない動作が発生することも

これらの問題の一部は、Windows のコマンドラインツールを改善するために Microsoft に依頼することがあります。また、ネイティブの Bash と Linux のコマンドラインツールを Windows で実行できるようにするために、パートナーに正規のパートナーとして機能します。

## <a name="what-does-this-mean-for-powershell"></a>PowerShell の意味
OSS プロジェクトの作業中に、PowerShell プロンプトから Bash に非常ことができるシナリオは多数あります。 Bash のサポートは補完的で、Windows のコマンドラインの価値を強化し、PowerShell と PowerShell コミュニティで他の一般的なテクノロジを利用できるようにします。

詳細については、PowerShell チームブログ[の「Bash for Windows:それがすばらしい理由と PowerShell の意味](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>WSL ですべての Linux アプリを実行できますか。
違います！ WSL は、Windows 上で Bash およびコア Linux コマンドラインツールを実行する必要があるユーザーを有効にすることを目的としたツールです。 

WSL は、GUI デスクトップやアプリケーション (例: Gnome、KDE など) をサポートすることを目的とし**ていません**。  

また、多くの一般的なサーバーアプリケーション (Redis など) を実行できる場合でも、運用サービスをホストするための WSL はお勧めしません。 Microsoft は、Azure、Hyper-v、Docker で運用環境の Linux ワークロードを実行するためのさまざまなソリューションを提供しています。 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL はどのような Windows Sku に含まれていますか。
Windows Subsystem for Linux は、windows 10 記念日および作成者更新以降の windows のデスクトップバージョンで使用できます。

Windows のデスクトップとサーバーの両方の Sku で、秋の更新プログラム WSL が使用できるようになります。

## <a name="what-processors-does-wsl-support"></a>WSL はどのようなプロセッサをサポートしていますか。
WSL は、x64 および ARM の Cpu をサポートしています。

## <a name="how-do-i-access-my-c-drive"></a>C: ドライブにアクセス操作方法
ローカルコンピューター上のハードドライブのマウントポイントが自動的に作成され、Windows ファイルシステムに簡単にアクセスできるようになります。 
 
**/mnt/\<ドライブ文字 >/**
 
使用例は c:\ `cd /mnt/c`にアクセスすることになります。

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Linux アプリで Windows ファイルを使用操作方法には

WSL の利点の1つは、Windows と Linux の両方のアプリまたはツールでファイルにアクセスできることです。 

Wsl は、コンピューターの固定ドライブを Linux `/mnt/<drive>`ディストリビューションのフォルダーの下にマウントします。 たとえば、 `C:`ドライブは次のようにマウントされます。`/mnt/c/` 

マウントされたドライブを使用する`C:\dev\myproj\`と、たとえば、 [Visual Studio](https://visualstudio.microsoft.com/vs/) /または[VS Code](https://code.visualstudio.com/)を使用してコードを編集したり、を介し`/mnt/c/dev/myproj`て同じファイルにアクセスして Linux でコードをビルド/テストしたりできます。

> **重要な注意**:WSL を使用する際の主な制限事項の1つは、Windows アプリまたはツールを使用して Linux ディストリビューション ' ファイルシステム内のファイルに直接アクセスしたり変更したりすることがサポートされていないことです。 参照トピック[Windows アプリとツールを使用して Linux ファイルを変更しない](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Linux ドライブのファイルはマウントされた Windows ドライブとは別のものですか。

1. Linux ルートの下にあるファイル ( `/`つまり) は、linux 固有の動作を模倣する wsl によって制御されます。次に例を示します。
   * 無効な Windows ファイル名文字を含むファイル
   * 管理者以外のユーザーに対して作成されたシンボリックリンク
   * Chmod および chown を使用したファイル属性の変更
   * ファイル/フォルダーの大文字と小文字の区別

2. マウントされたドライブのファイルは Windows によって制御され、次の動作があります。
   * 大文字と小文字の区別のサポート
   * すべてのアクセス許可は、Windows のアクセス許可を最適に反映するように設定されます。

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Apt-upgrade upgrade を実行すると、多くのエラーが発生するのはなぜですか。
一部のパッケージでは、まだ実装していない機能が使用されています。 `udev`たとえば、はまだサポートされていない`apt-get upgrade`ため、いくつかのエラーが発生します。

に`udev`関連する問題を修正するには、次の手順に従います。

1. に次のもの`/usr/sbin/policy-rc.d`を書き込んで、変更を保存します。

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 実行アクセス許可の追加先`/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 次のコマンドを実行します。

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>WSL 配布操作方法アンインストールしますか?

1709 (16299) より前のビルドでは、コマンドプロンプトを開き、次を実行します。
  ```batchfile
  lxrun /uninstall /full
  ```
  
ストアからインストールされた wsl ディストリビューションは、他の Windows アプリと同様にアンインストールできます。そのためには、アプリタイルを右クリックして [アンインストール] をクリックするか、 [ `Remove-AppxPackage`コマンドレット](https://technet.microsoft.com/en-us/library/hh856038.aspx)を使用して PowerShell を使用します。

## <a name="why-does-ping-generate-permission-denied-errors"></a>Ping によってアクセス拒否エラーが生成されるのはなぜですか。
WSL ビルド < 14926 では、管理者特権のコンソールを使用して実行するために必要な WSL を ping します。 この問題は、ビルド14926以降で修正されました。

## <a name="how-do-i-run-an-openssh-server"></a>OpenSSH サーバーを実行操作方法ますか?
Windows の管理者特権は、WSL で OpenSSH を実行するために必要です。 OpenSSH サーバーを実行するには、管理者として Windows 上で Bash on Ubuntu を実行するか、管理者特権を使用して CMD/PowerShell プロンプトから bash を実行します。

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>"エラー:0x80040306 "をインストールしようとすると、
WSL は、従来のコンソールでの実行をサポートしていません。 レガシコンソールをオフにするには:

1. WSL、PowerShell、または Cmd を開く
1. タイトルバーを右クリックし > プロパティ-> レガシコンソールを使用する をオフにします。
1. [OK] をクリックします。

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>"エラー:Windows をアップグレードした後に bash を実行する場合の0x80040154 が
Windows update で windows Subsystem for Linux 機能が無効になっている可能性があります。 この問題が発生した場合は、Windows の機能を再度有効にする必要があります。 "Windows Subsystem for Linux" 機能を有効にする手順については、[インストールガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)を参照してください。

## <a name="how-do-i-change-the-display-language-of-wsl"></a>WSL の表示言語を変更操作方法には
WSL install は、Windows インストールのロケールに合わせて Ubuntu のロケールを自動的に変更しようとします。 この動作が不要な場合は、このコマンドを実行して、インストールの完了後に Ubuntu のロケールを変更することができます。 この変更を有効にするには、bash を再起動する必要があります。

次の例では、ロケールを en-us に変更します。
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>WSL からインターネットにアクセスできないのはなぜですか。
一部のユーザーが、WSL でのインターネットアクセスをブロックする特定のファイアウォールアプリケーションに関する問題を報告しています。 報告されるファイアウォールは次のとおりです。

1. Kaspersky
1. AVG
1. Avast

場合によっては、ファイアウォールをオフにすることでアクセスできます。 場合によっては、ファイアウォールをインストールするだけでアクセスがブロックされます。

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Windows の WSL からポートにアクセス操作方法には、
WSL は windows で実行されているため、Windows の IP アドレスを共有します。 このように、localhost 上の任意のポートにアクセスできます。たとえば、ポート 1234 https://localhost:1234 に web コンテンツがあった場合は、Windows ブラウザーを使用できます。

## <a name="how-can-i-back-up-my-wsl-distros"></a>WSL ディストリビューションをバックアップするにはどうすればよいですか。

ディストリビューションをバックアップする最適な方法は、Windows バージョン1809以降で使用できます。 `wsl --export`コマンドを使用して、配布全体を tar にエクスポートできます。 その後、 `wsl --import`コマンドを使用してこのディストリビューションを wsl にインポートし直すことができます。これにより、wsl ディストリビューションの状態をバックアップして保存することができます。 

Appdata フォルダー (Windows バックアップなど) のファイルをバックアップする従来のバックアップサービスでは、Linux ファイルが破損しないことに注意してください。 



## <a name="where-can-i-provide-feedback"></a>フィードバックはどこで提供できますか。

複数のチャネルを通じて、フィードバックを共有したり質問したりすることができます。フィードバックと質問は次のようになります。
* [GitHub の問題の追跡ツール](https://github.com/Microsoft/BashOnWindows/issues)
* Microsoft[のコマンドライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Microsoft[のコマンドラインチームのブログ](https://blogs.msdn.microsoft.com/commandline/)
* Twitter 経由。 ニュース、 [@richturn_ms](https://twitter.com/richturn_MS)更新プログラムなどの詳細については、Twitter でフォローしてください。
