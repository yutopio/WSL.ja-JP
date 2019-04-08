---
title: Linux 用の Windows Susbystem のトラブルシューティング
description: 一般的なエラーの詳細について説明し、ユーザーに実行を発行 Linux 用 Windows Susbystem で Linux を実行中にします。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: 055bdc02dcf8f078caa014abd6dd755a47c99cfe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063300"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>トラブルシューティングの Windows Subsystem for Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash の VPN に接続すれば、ネットワーク接続を失った

Windows 上の VPN に接続したら、bash にネットワーク接続が切断されると、bash 内からこの回避策をお試しください。 この回避策で DNS 解決を手動でオーバーライドすることが`/etc/resolv.conf`します。

1. これから VPN の DNS サーバーのメモします。 `ipconfig.exe /all`
2. Resolv.conf を既存のコピーを作成します。 `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 現在の resolv.con のリンクを解除します。 `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. 開いている`/etc/resolv.conf`と <br/>
   a.  というファイルから最初の行を削除"\# WSL でのこのファイルを自動的に生成されました。 このファイルの自動生成を停止するには、この行を削除します。"です。 <br/>
   b.  DNS サーバーの一覧で最初のエントリとして (1) から上の DNS エントリを追加します。 <br/>
   c. ファイルを閉じます。 <br/>

変更を元に戻す必要があります、VPN を切断すると、`/etc/resolv.conf`します。 これを行うには、次の操作を行います。
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>WSL を開始またはディストリビューションのインストールは、エラー コードを返します

次の[手順](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)の詳細なログを収集し、GitHub で問題を報告します。

### <a name="updating-bash-on-ubuntu-on-windows"></a>Bash on Ubuntu on Windows を更新しています

Bash on Ubuntu on Windows の更新が必要になるの 2 つのコンポーネントがあります。 

1. Windows Subsystem for Linux
  
   Bash on Ubuntu on Windows のこの部分をアップグレードするで、新しい修正アウトラインが有効になります、[リリース ノート](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)します。 Windows Insider Program にサブスクライブしていることと、ビルドが最新であることを確認します。 きめ細かいコントロール、Ubuntu のリセットを含むインスタンスのチェック アウト、[コマンド リファレンスのページ](https://msdn.microsoft.com/en-us/commandline/wsl/reference)します。

2. Ubuntu のユーザーのバイナリ 

   Bash on Ubuntu on Windows のこの部分をアップグレードすると、apt get を使用してインストールされているアプリケーションを含む Ubuntu ユーザー バイナリにすべての更新プログラムがインストールされます。 Bash で、次のコマンドの実行を更新します。
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt get アップグレード エラー
一部のパッケージはまだ実装されていない機能を使用します。 `udev`、たとえば、はまだサポートされていません、いくつかの原因`apt-get upgrade`エラー。

関連する問題を修正する`udev`、次の手順に従います。

1. 次のコードを記述`/usr/sbin/policy-rc.d`して変更を保存します。
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 追加するアクセス許可を実行 `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 次のコマンドを実行します
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"エラー。0x80040306"のインストール
これは、従来のコンソールはサポートされていません、という事実とにいます。
従来のコンソールをオフにするには。

1. Cmd.exe を開きます
1. タイトルを右クリックしてバー]-> [プロパティ]、[従来のコンソールを使用してのオフにします
1. [OK] をクリックします。

### <a name="error-0x80040154-after-windows-update"></a>"エラー。0x80040154"Windows の更新後
Linux の機能の Windows サブシステムが無効になっている Windows の更新中にします。 このような場合、Windows の機能が再度有効にする必要があります。 Linux が記載されているは、Windows サブシステムを有効にする手順、[インストール ガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)します。

### <a name="changing-the-display-language"></a>表示言語を変更します。
WSL インストールは自動的に Windows インストールのロケールに一致するように Ubuntu ロケールを変更しようとします。  この動作したくない場合は、インストールが完了した後は、Ubuntu ロケールを変更するには、このコマンドを実行できます。  この変更を有効にする bash.exe を再起動する必要があります。

次の例のロケールを EN-US に変更します。
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows システムの復元後のインストールの問題
1.  削除、`%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`フォルダー。 <br/>
  **注:そうしないと、省略可能な機能が完全にインストールされている場合と、操作します。**
2.  WSL の省略可能な機能を有効にする (まだ行っていない場合)
3.  再起動します
4.  lxrun/アンインストール/フル
5.  Bash をインストールします。

### <a name="no-internet-access-in-wsl"></a>WSL でインターネットにアクセスできません。
一部のユーザーには、WSL でインターネット アクセスをブロックする特定のファイアウォール アプリケーションで問題が報告します。  報告されるファイアウォールは次のとおりです。

1. Kaspersky
1. AVG
1. Avast

場合によっては、ファイアウォールを無効にすることに対するアクセス許可します。  アクセスをブロックするには、場合によっては、ファイアウォールをインストールしているだけで検索します。

### <a name="permission-denied-error-when-using-ping"></a>Ping を使用する場合のアクセス許可の拒否エラー
#### [<a name="anniversary-update"></a>Anniversary Update](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

WSL で ping を実行するには、Windows で管理者特権が必要です。  Ping を実行するには、Ubuntu 上で管理者は、Windows で Bash を実行または bash.exe を管理者特権での CMD または PowerShell プロンプトから実行します。

#### [<a name="build-14926"></a>ビルド 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  管理者特権が必要なくなりました。

### <a name="bash-is-hung"></a>Bash が停止しています。
Bash での作業中に見つかった場合、bash がハングしている (またはデッドロック) の入力に応答していない、ご意見をお reporting メモリ ダンプを収集して問題を診断します。 次の手順は、システムがクラッシュすることに注意してください。 これを実行する前に作業内容を保存するに慣れていない場合は、このチェック ボックスを行うにしないでください。  <br/>
メモリ ダンプを収集するには。
1. メモリ ダンプの種類を「完全メモリ ダンプ」に変更します。 ダンプの種類を変更するには、中に、現在の型のメモを実行します。
2. 使用して、[手順](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/)クラッシュを構成するキーボード コントロールを使用します。
3. デッドロック、ハングを再現します。
4. (2) からのキー シーケンスを使用して、システムがクラッシュします。
5. システムがクラッシュし、メモリ ダンプを収集します。
6. システムが再起動すると後のレポートに memory.dmpsecure@microsoft.comします。 ダンプ ファイルの既定の場所は、c: がシステム ドライブの場合は %SystemRoot%\memory.dmp または C:\Windows\memory.dmp します。 電子メールの WSL または Bash のダンプがあることに注意してください Windows チームです。
7. メモリ ダンプの種類を元の設定に復元します。

### <a name="check-your-build-number"></a>ビルド番号を確認します。

お客様の PC のアーキテクチャと Windows のビルド番号を見つけるには開きます  
**設定** > **システム** > **について**

探して、 **OS ビルド**と**システム型**フィールド。  
    ![ビルドのスクリーン ショットとシステムの種類のフィールド](media/system.png) 


Windows Server のビルド番号を検索するには、PowerShell で、次を実行します。  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>WSL が有効になっていることを確認します。
PowerShell で、次を実行して、Windows Subsystem for Linux が有効になっていることを確認できます。  
``` PowerShell
PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH サーバー接続の問題
SSH サーバーを接続しようとは、次のエラーで失敗しました。"接続を終了して 127.0.0.1 でポート 22"。
1. OpenSSH サーバーで実行されていることを確認します。
   ``` BASH
   sudo service ssh status
   ```
   このチュートリアルに従っています。 https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Sshd サービスを停止し、デバッグ モードで sshd を起動します。
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. スタートアップ ログを確認し、ログ メッセージが表示されない理由ホストキーが利用可能を: debug1: sshd バージョン OpenSSH_7.2、OpenSSL 1.0.2g 2016 年 3 月 1日 debug1: key_load_private: パスフレーズが正しくありませんが秘密キー debug1 を復号化に指定された: key_load_public:ファイルまたはディレクトリはホスト キーを読み込めません:/etc/ssh/ssh_host_rsa_key debug1: key_load_private:このようななしのファイルまたはディレクトリ debug1: key_load_public:ファイルまたはディレクトリはホスト キーを読み込めません:/etc/ssh/ssh_host_dsa_key debug1: key_load_private:このようななしのファイルまたはディレクトリ debug1: key_load_public:ファイルまたはディレクトリはホスト キーを読み込めません:/etc/ssh/ssh_host_ecdsa_key debug1: key_load_private:このようななしのファイルまたはディレクトリ debug1: key_load_public:ファイルまたはディレクトリはホスト キーを読み込めません:/etc/ssh/ssh_host_ed25519_key

このようなメッセージが表示され、キーは 不足している場合`/etc/ssh/`キーを再生成またはだけを消去して openssh サーバーをインストールする必要があります。
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

