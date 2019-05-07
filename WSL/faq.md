---
title: よく寄せられる質問 (FAQ)
description: に関してよく寄せられる質問 Windows サブシステム for Linux。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、よく寄せられる質問
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063270"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Linux 用 Windows サブシステムに関するよく寄せられる質問

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Windows Subsystem for Linux (WSL) とは何ですか。
Windows Subsystem for Linux (WSL) は、Windows 10 の新機能を使用すると、Windows 上で直接ネイティブの Linux コマンド ライン ツールを実行、と共に、従来の Windows デスクトップおよび最新のストア アプリです。

参照してください、[ページに関する](./about.md)の詳細。

## <a name="who-is-wsl-for"></a>用の WSL は誰ですか。
これは、主に開発者--特に web 開発者と人とでまたはオープン ソース プロジェクトの作業のツールです。 これによりする/、Bash、Linux の一般的なツールを使用する必要がある人 (`sed`、`awk`など) と多くの Linux 最初ツール (Ruby、Python など) で Windows のツール チェーンを使用します。

## <a name="what-can-i-do-with-wsl"></a>WSL では、どうすればでしょうか。
WSL では、アプリケーションと呼ばれる Bash.exe、起動するが開き、Bash シェルを実行する Windows コンソールを提供します。 Bash を使用して、Linux のコマンド ライン ツールとアプリを実行できます。 たとえば、「`lsb_release -a`し、enter キーを押します。 現在実行されている Linux ディストリビューション詳細が表示されます。

![ディストリビューションの詳細のスクリーン ショット](media/distro.png)

Linux の Bash シェル内からローカル コンピューターのファイル システムにもアクセスできます: ローカル ドライブでマウントされていることがわかります、`/mnt`フォルダー。 たとえば、`C:`下ドライブがマウントされて`/mnt/c`:  

![マウントの C ドライブのスクリーン ショット](media/ls.png)

## <a name="what-is-bash"></a>Bash とは何ですか。
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)は、一般的なテキスト ベースのシェルおよびコマンド言語。 Ubuntu およびその他の Linux ディストリビューション内および macOS に含まれる既定のシェルになります。 ユーザーは、スクリプトを実行したり、多くのタスクを実行するには、コマンドとツールを実行するシェルにコマンドを入力します。

## <a name="how-does-this-work"></a>この処理のしくみ
チェック アウト、[ブログ](https://blogs.msdn.microsoft.com/wsl/)基になるテクノロジについての詳細を参照してください。

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>使用する理由を Linux ではなく、WSL vm ですか。
WSL では、完全な仮想マシンよりも少ないリソース (CPU、メモリ、および記憶域) が必要です。 また、WSL では、アプリと共に、Windows コマンドライン、デスクトップ アプリとストア アプリ、および Linux コマンド ライン ツールを実行して、Linux 内から Windows ファイルにアクセスすることもできます。 これにより、希望する場合、同じファイルのセットでアプリを Windows および Linux コマンド ライン ツールを使用することができます。

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>使用する理由をたとえば、Windows 上の代わりに Linux で Ruby でしょうか。
Linux のように実行される環境が動作すると仮定すると、いくつかのクロス プラットフォーム ツールを構築しました。 たとえば、いくつかのツールは、非常に長いファイル パスにアクセスできるか、特定のファイル/フォルダーが存在するとします。 多くの場合、問題が生じます動作では多くの場合、Windows の異なる方法で Linux から。

Ruby とノードのような多くの言語は多くの場合、移植し、優れた、Windows 上で実行します。 ただし、ポート、Windows をサポートするために、ライブラリのすべての Ruby Gem またはノード/NPM ライブラリの所有者と、Linux 固有の依存関係を持つ多くします。 このようなツールとライブラリのビルドと場合によっては実行時エラーまたは Windows 上の望ましくない動作の影響を受けてを使用して構築されたシステムでその多くの場合、結果します。

これらは、Windows のコマンド ライン ツールとどのようなネイティブ Bash および Linux コマンド ライン ツールを Windows 上で実行を有効にする Canonical によるパートナーを推進したほかを向上させるために Microsoft に依頼する多くの人々 を原因となった問題の一部です。

## <a name="what-does-this-mean-for-powershell"></a>これはどういう PowerShell のでしょうか。
OSS プロジェクトで作業中には、PowerShell から Bash にドロップすると非常に便利なさまざまなシナリオがプロンプトです。 Bash のサポートは、補完的な人気のあるその他のテクノロジを活用するには、PowerShell と PowerShell コミュニティを許可する Windows 上のコマンドラインの値を強化します。

詳細については、PowerShell チームのブログ - [Bash for Windows:すばらしいことが理由と、PowerShell の意味](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>WSL では、すべての Linux アプリを実行できますか。
違います！ WSL は、Bash を実行し、Windows 上の Linux コマンド ライン ツールのコアする必要があるユーザーの有効化を目的としたツールです。 

WSL は**いない**GUI デスクトップまたはアプリケーション (例: Gnome、KDE など) をサポートする目的  

また、たとえできなく多くの人気のあるサーバー アプリケーションを実行する (例: Redis)、運用環境のサービスをホストするため WSL お勧めしません – Microsoft はさまざまな Azure では、実稼働 Linux ワークロードを実行するためのソリューションを提供、HYPER-V、および Docker。 

## <a name="what-windows-skus-is-wsl-included-in"></a>どのような Windows Sku が WSL には含まれますか。
Windows Subsystem for Linux は、Windows 10 Anniversary の Windows と Creators update 以降のデスクトップ バージョンで利用できます。

以降で Fall Creators update WSL は Sku の Windows デスクトップおよびサーバーの両方で提供されます。

## <a name="what-processors-does-wsl-support"></a>WSL はどのようなプロセッサをサポートしますか。
WSL では、x64 と ARM Cpu をサポートします。

## <a name="how-do-i-access-my-c-drive"></a>C: ドライブをアクセスする方法はありますか
ローカル コンピューターのハード ドライブのマウント ポイントが自動的に作成し、Windows ファイル システムに簡単にアクセスを提供します。 
 
**/mnt/\<ドライブ文字 >/**
 
使用例`cd /mnt/c`c:\ にアクセスするには

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Linux アプリと Windows ファイルを使用する方法

WSL の利点の 1 つは、Windows と Linux の両方のアプリまたはツールを使用して、ファイルにアクセスできることです。 

WSL が コンピューターの固定ドライブをマウント、 `/mnt/<drive>` Linux ディストリビューションでのフォルダー。 たとえば、`C:`下ドライブがマウントされて `/mnt/c/` 

マウントされたドライブを使用して、コードを編集できます、たとえば、`C:\dev\myproj\`を使用して[Visual Studio](https://visualstudio.microsoft.com/vs/) /または[VS Code](https://code.visualstudio.com/)とを使用して同じファイルにアクセスして Linux では、そのコードのビルドおよびテスト`\mnt\c\dev\myproj`します。

> **重要な注意事項**:WSL を使用する主な制限事項の 1 つは、直接へのアクセスまたは変更する、Windows アプリケーションやツールを使用して Linux ディストリビューションのファイル システム内のファイルがサポートされていないことです。 参照トピック[Windows アプリケーションおよびツールを使用して Linux ファイルを変更しないでください。](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Windows のマウントされたドライブからさまざまな Linux ドライブにファイルがでしょうか。

1. Linux ルートの下のファイル (つまり`/`) を含むこれらに限定されませんが、Linux 特定の動作を模倣 WSL によって制御されます。
   * 無効な Windows ファイル名の文字が含まれるファイル
   * 管理者以外のユーザー用に作成されたシンボリック リンク
   * Chmod、chown によるファイルの属性を変更します。
   * ファイル/フォルダー大文字小文字の区別

2. マウントされたドライブ内のファイルは、Windows によって制御され、次の動作します。
   * 大文字小文字の区別をサポートします。
   * すべてのアクセス許可が最適な Windows のアクセス許可を反映するように設定されます。

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>なぜエラーがある非常に多く apt-get とアップグレードを実行するとしますか。
一部のパッケージはまだ実装されていない機能を使用します。 `udev`、たとえば、はまだサポートされていません、いくつかの原因`apt-get upgrade`エラー。

関連する問題を修正する`udev`、次の手順に従います。

1. 次のコードを記述`/usr/sbin/policy-rc.d`して変更を保存します。

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 追加するアクセス許可を実行 `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 次のコマンドを実行します

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>WSL 配布のアンインストール方法

ビルド 1709 (16299) オープンする前に、コマンド プロンプトし実行します。
  ```batchfile
  lxrun /uninstall /full
  ```
  
アプリのタイルを右クリックし、[アンインストール] をクリックすると、または PowerShell を使用して他の Windows アプリのようなストアからインストール WSL ディストリビューションをアンインストールする、 [ `Remove-AppxPackage`コマンドレット](https://technet.microsoft.com/en-us/library/hh856038.aspx)します。

## <a name="why-does-ping-generate-permission-denied-errors"></a>Ping が権限拒否エラーを生成する理由
WSL で構築されます < 14926、ping WSL を管理者特権でのコンソールを使用して実行するために必要な。 14926 のビルド以降、この問題が修正されました。

## <a name="how-do-i-run-an-openssh-server"></a>OpenSSH server を実行する方法はありますか
WSL で OpenSSH を実行するには、Windows で管理者特権が必要です。 OpenSSH server を実行するには、Ubuntu 上で管理者は、Windows で Bash を実行または bash.exe を管理者特権での CMD または PowerShell プロンプトから実行します。

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>なぜ"エラー。0x80040306"をインストールしようとするとしますか?
WSL では、従来のコンソールで実行することはできません。 従来のコンソールをオフにするには。

1. WSL、PowerShell、または Cmd を開きます
1. タイトルを右クリックしてバー]-> [プロパティ]、[「従来のコンソールを使用して」をオフにします
1. [OK] をクリックします。

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>なぜ"エラー。0x80040154"Windows をアップグレードした後 bash.exe を実行するとしますか?
"Linux 用 Windows サブシステム"機能が無効になっている Windows の更新中にします。 このような場合、Windows の機能が再度有効にする必要があります。 "Linux 用 Windows サブシステム"機能を有効にする手順が記載されて、[インストール ガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)します。

## <a name="how-do-i-change-the-display-language-of-wsl"></a>WSL の表示言語を変更する方法はありますか
WSL インストールは自動的に Windows インストールのロケールに一致するように Ubuntu ロケールを変更しようとします。 この動作したくない場合は、インストールが完了した後は、Ubuntu ロケールを変更するには、このコマンドを実行できます。 この変更を有効にする bash.exe を再起動する必要があります。

次の例のロケールを EN-US に変更します。
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>理由はアクセスできないインターネット WSL からでしょうか。
一部のユーザーには、WSL でインターネット アクセスをブロックする特定のファイアウォール アプリケーションで問題が報告します。 報告されるファイアウォールは次のとおりです。

1. Kaspersky
1. AVG
1. Avast

場合によっては、ファイアウォールを無効にすることに対するアクセス許可します。 アクセスをブロックするには、場合によっては、ファイアウォールをインストールしているだけで検索します。

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>ポートを Windows で WSL からアクセスする方法
WSL は、Windows で実行されているように、Windows の IP アドレスを共有します。 例: localhost 上の任意のポートをアクセスするようポート 1234 できますで web コンテンツをした https://localhost:1234Windows ブラウザーにします。

## <a name="where-can-i-provide-feedback"></a>フィードバックを提供する場所は?

フィードバックを共有し、複数のチャネルを通じてに関する質問をしたりできます。フィードバックや質問が表示する必要があります。
* この[GitHub の issue トラッカー](https://github.com/Microsoft/BashOnWindows/issues)
* この[コマンド ライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* この[コマンド ライン チームのブログ](https://blogs.msdn.microsoft.com/commandline/)
* Twitter。 従ってください[ @richturn_ms ](https://twitter.com/richturn_MS)についてのニュース、更新プログラム、twitter など。
