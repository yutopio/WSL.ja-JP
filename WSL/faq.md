---
title: よく寄せられる質問 (FAQ)
description: Windows Subsystem for Linux に関してよく寄せられる質問。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: e3376f8dff83262577bc52fb3ac368b70b21d922
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122763"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Windows Subsystem for Linux に関してよく寄せられる質問

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Windows Subsystem for Linux (WSL) とは何ですか。
Windows Subsystem for Linux (WSL) は、ネイティブ Linux コマンド ライン ツールを Windows で直接実行できる Windows 10 の新機能です。これは、従来の Windows デスクトップや最新のストア アプリと共存します。

詳しくは、[詳細ページ](./about.md)をご覧ください。

## <a name="who-is-wsl-for"></a>WSL の対象ユーザーは誰ですか。
これは、主に開発者向けのツールです。特に Web 開発者と、オープン ソース プロジェクトで作業している開発者が対象です。 これにより、Bash、一般的な Linux ツール (`sed`、 `awk` など)、および多くの Linux ファースト ツール (Ruby、Python など) を使用する必要があるユーザーは、Windows でそれらのツールチェーンを使用できます。

## <a name="what-can-i-do-with-wsl"></a>WSL で何ができますか。
WSL が提供する Bash.exe というアプリケーションを開始すると、Bash シェルを実行している Windows コンソールが開きます。 Bash を使用すると、コマンド ライン Linux ツールおよびアプリを実行できます。 たとえば、「`lsb_release -a`」と入力して Enter キーを押すと、現在実行中の Linux ディストリビューションの詳細が表示されます。

![ディストリビューションの詳細のスクリーンショット](media/distro.png)

Linux Bash シェル内からローカル コンピューターのファイル システムにアクセスすることもできます。ローカル ドライブは `/mnt` フォルダーの下にマウントされます。 たとえば、 `C:` ドライブは `/mnt/c` の下にマウントされます。  

![マウントされた C ドライブのスクリーンショット](media/ls.png)

## <a name="what-is-bash"></a>Bash とは何ですか。
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) は、広く使われているテキスト ベースのシェルおよびコマンド言語です。 これは、Ubuntu およびその他の Linux ディストリビューション内と macOS に含まれる既定のシェルです。 ユーザーは、シェルにコマンドを入力して、スクリプトを実行したり、コマンドやツールを実行したりして多くのタスクを行います。

## <a name="how-does-this-work"></a>この処理のしくみ
基礎となるテクノロジの詳細については、[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください。

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>VM で Linux ではなく WSL を使用するのはなぜですか。
WSL は、必要なリソース (CPU、メモリ、およびストレージ) が完全な仮想マシンよりも少なくて済みます。 また、WSL を使用すると、Linux コマンド ライン ツールおよびアプリを Windows コマンド ライン、デスクトップおよびストア アプリと共に実行したり、Linux 内から Windows ファイルにアクセスしたりすることもできます。 これにより、必要に応じて、同じファイル セットに対して Windows アプリと Linux コマンド ライン ツールを使用できます。

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>たとえば、Windows ではなく Linux 上で Ruby を使用するのはなぜですか。
一部のクロスプラットフォーム ツールは、それらが実行される環境が Linux のように動作することを前提として構築されました。 たとえば、一部のツールでは、非常に長いファイル パスにアクセスできることや、特定のファイルまたはフォルダーが存在することを前提としています。 これにより、Linux とは動作が異なる事が多い Windows で問題が発生することがよくあります。

Ruby や node のような多くの言語は、たいていの場合、Windows に移植され、非常にうまく動作します。 ただし、すべての Ruby Gem または node/NPM ライブラリ所有者が、Windows をサポートするためにライブラリを移植するわけではなく、多くのものに Linux 固有の依存関係があります。 これにより、このようなツールやライブラリを使用して構築されたシステムはビルドから悪影響を受ける場合が多く、Windows で実行時エラーや望ましくない動作が発生することがあります。

これらは、多くのユーザーが Windows のコマンド ライン ツールの向上を Microsoft に依頼する原因となった問題の一部に過ぎません。また、こうした要因から、Microsoft が Canonical と提携して、ネイティブ Bash と Linux コマンド ライン ツールを Windows で実行できるようにすることになりました。

## <a name="what-does-this-mean-for-powershell"></a>PowerShell においてこれは何を意味しますか。
OSS プロジェクトでの作業中、PowerShell プロンプトから Bash を実行すると非常に役立つシナリオが多数あります。 Bash のサポートは補完的なものであり、Windows でのそのコマンド ラインの価値を高め、PowerShell と PowerShell コミュニティでその他の一般的なテクノロジを利用できるようにします。

詳細については、PowerShell チームのブログ「[Windows の Bash:それがすばらしい理由と PowerShell における意味](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)」をお読みください

## <a name="can-i-run-all-linux-apps-in-wsl"></a>WSL ですべての Linux アプリを実行できますか。
いいえ。 WSL は、Bash およびコア Linux コマンド ライン ツールを必要とするユーザーが Windows 上でそれらを実行できるようにすることを目的としたツールです。 

WSL は、GUI デスクトップやアプリケーション (例: Gnome、KDE など) をサポートすることを目的として**いません**。  

また、多くの一般的なサーバー アプリケーション (Redis など) を実行できる場合でも、実稼働サービスをホストする目的には WSL をお勧めしません。Microsoft は、Azure、Hyper-V、Docker で実稼働 Linux ワークロードを実行するためのさまざまなソリューションを提供しています。 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL はどの Windows SKU に含まれていますか。
Windows Subsystem for Linux は、Windows 10 Anniversary および Creators Update 以降の Windows デスクトップ バージョンで使用できます。

Fall Creators Update 以降では、WSL は Windows のデスクトップとサーバーの両方の SKU で使用できるようになります。

## <a name="what-processors-does-wsl-support"></a>WSL はどのようなプロセッサをサポートしていますか。
WSL は x64 および ARM の CPU をサポートしています。

## <a name="how-do-i-access-my-c-drive"></a>C: ドライブにアクセスするにはどうすればよいですか。
ローカル コンピューター上のハード ドライブのマウント ポイントが自動的に作成され、Windows ファイル システムに簡単にアクセスできるようになります。 
 
**/mnt/\<ドライブ文字>/**
 
使用例は、c:\ にアクセスする `cd /mnt/c` です。

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Linux アプリで Windows ファイルをどのように使用しますか。

WSL の利点の 1 つは、Windows と Linux の両方のアプリまたはツールを経由してファイルにアクセスできることです。 

WSL では、コンピューターの固定ドライブを Linux ディストリビューションの `/mnt/<drive>` フォルダーの下にマウントします。 たとえば、 `C:` ドライブは `/mnt/c/` の下にマウントされます。 

マウントされたドライブを使用すると、[Visual Studio](https://visualstudio.microsoft.com/vs/) または[VS Code](https://code.visualstudio.com/)を使用して、たとえば `C:\dev\myproj\` 内のコードを編集したり、`/mnt/c/dev/myproj` を介して同じファイルにアクセスして Linux でそのコードをビルド/テストしたりできます。

> **重要な注意**:WSL を使用する際の主な制限事項の 1 つは、Windows アプリまたはツールを使用して Linux ディストリビューションのファイル システム内のファイルに直接アクセスしたり、変更したりすることがサポートされていないことです。 以下をご覧ください。[Windows アプリやツールを使用して Linux ファイルを変更しない](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Linux ドライブのファイルはマウントされた Windows ドライブのものとは異なりますか。

1. Linux ルート (つまり `/`) の下にあるファイルは、Linux 固有の性質を模倣する WSL によって制御されます。次のようなものが含まれますが、これらに限定されません。
   * 無効な Windows ファイル名の文字を含むファイル
   * 管理者以外のユーザー用に作成されたシンボリック リンク
   * chmod および chown を使用したファイル属性の変更
   * ファイル/フォルダーの大文字と小文字の区別

2. マウントされたドライブのファイルは Windows によって制御され、次のように動作します。
   * 大文字と小文字の区別をサポート
   * すべてのアクセス許可は、Windows アクセス許可を最適に反映するように設定

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>apt-get upgrade を実行すると、多くのエラーが発生するのはなぜですか。
一部のパッケージでは、Microsoft がまだ実装していない機能が使用されています。 たとえば、`udev` はまだサポートされていないため、`apt-get upgrade` エラーがいくつか発生します。

`udev` に関連する問題を修正するには、次の手順に従います。

1. 次の内容を `/usr/sbin/policy-rc.d` に記述して、変更を保存します。

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 実行のアクセス許可を `/usr/sbin/policy-rc.d` に追加します

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 次のコマンドを実行します

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>WSL ディストリビューションをアンインストールするにはどうすればよいですか。

1709 (16299) より前のビルドでは、コマンド プロンプトを開き、次を実行します。
  ```batchfile
  lxrun /uninstall /full
  ```
  
ストアからインストールされた WSL ディストリビューションは、他の Windows アプリと同様に、アプリ タイルを右クリックして [アンインストール] をクリックするか、[`Remove-AppxPackage` コマンドレット](https://technet.microsoft.com/en-us/library/hh856038.aspx)を使用して PowerShell を介してアンインストールできます。

## <a name="why-does-ping-generate-permission-denied-errors"></a>ping によってアクセス拒否エラーが発生するのはなぜですか。
14926 より前の WSL ビルドでは、WSL で管理者特権のコンソールを使用して ping を実行する必要がありました。 この問題は、ビルド14926 以降で修正されました。

## <a name="how-do-i-run-an-openssh-server"></a>OpenSSH サーバーを実行するにはどうすればよいですか。
WSL で OpenSSH を実行するには、Windows の管理者特権が必要です。 OpenSSH サーバーを実行するには、管理者として Bash on Ubuntu on Windows を実行するか、管理者特権を使用して CMD/PowerShell プロンプトから bash.exe を実行します。

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>インストールしようとすると、"エラー: 0x80040306" が表示されるのはなぜですか。
WSL は、従来のコンソールでの実行をサポートしていません。 従来のコンソールをオフにするには、以下を実行します。

1. WSL、PowerShell、または Cmd を開きます
1. タイトル バーを右クリックして、[プロパティ] を選択し、[従来のコンソールを使う] をオフにします
1. [OK] をクリックします。

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Windows をアップグレードした後に bash.exe を実行すると、"エラー: 0x80040154" が表示されるのはなぜですか。
Windows Update 時に "Windows Subsystem for Linux" 機能が無効になる可能性があります。 その場合は、この Windows 機能を再度有効にする必要があります。 "Windows Subsystem for Linux" 機能を有効にする手順については、[インストール ガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)をご覧ください。

## <a name="how-do-i-change-the-display-language-of-wsl"></a>WSL の表示言語を変更するにはどうすればよいですか。
WSL インストールでは、Windows インストールのロケールに合わせて Ubuntu ロケールを自動的に変更しようとします。 この動作が不要な場合は、次のコマンドを実行して、インストールの完了後に Ubuntu ロケールを変更できます。 この変更を有効にするには、bash.exe を再起動する必要があります。

次の例は、ロケールを en-US に変更します。
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>WSL からインターネットにアクセスできないのはなぜですか。
一部のユーザーにより、WSL でのインターネット アクセスをブロックする特定のファイアウォール アプリケーションに関する問題が報告されています。 報告されているファイアウォールは次のとおりです。

1. Kaspersky
1. AVG
1. Avast

ファイアウォールをオフにすると、アクセスできる場合があります。 場合によっては、ファイアウォールをインストールするだけでアクセスがブロックされるようです。

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Windows の WSL からポートにアクセスするにはどうすればよいですか。
WSL は Windows で実行されているため、Windows の IP アドレスを共有します。 そのため、localhost 上の任意のポートにアクセスできます。たとえば、ポート 1234 に Web コンテンツがあるとすると、 https://localhost:1234 を Windows ブラウザーに入力できます。

## <a name="how-can-i-back-up-my-wsl-distros"></a>WSL ディストリビューションをバックアップするにはどうすればよいですか。

ディストリビューションをバックアップする最適な方法は、Windows バージョン1809 以降で使用できます。 `wsl --export` コマンドを使用して、ディストリビューション全体を tarball にエクスポートできます。 その後、`wsl --import` コマンドを使用してこのディストリビューションを WSL にインポートし直すことができます。これにより、WSL ディストリビューションの状態をバックアップして保存できます。 

Appdata フォルダーのファイルをバックアップする従来のバックアップ サービス (Windows バックアップなど) によって Linux ファイルが破損することはありません。 



## <a name="where-can-i-provide-feedback"></a>フィードバックはどこで提供できますか。

複数のチャネルを通じて、フィードバックを共有したり、質問したりできます。フィードバックや質問は以下宛てにお願いいたします。
* Microsoft の [GitHub の問題の追跡ツール](https://github.com/Microsoft/BashOnWindows/issues)
* Microsoft の[コマンド ライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Microsoft のコマンド ライン チームのブログ](https://blogs.msdn.microsoft.com/commandline/)
* Twitter 経由。 ニュース、更新などを確認するには、Twitter で [@richturn_ms](https://twitter.com/richturn_MS) をフォローしてください。
