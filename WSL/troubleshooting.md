---
title: Windows Subsystem for Linux のトラブルシューティング
description: Linux を Windows Subsystem for Linux で実行しているときに発生する一般的なエラーと問題について詳しく説明します。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6a5fec8b8e054b4d3399ee9bcd903acebca7aace
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122694"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のトラブルシューティング

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>ネットワーク接続が VPN に接続されると、Bash が切断する

Windows で VPN に接続した後、bash がネットワーク接続を失った場合は、bash 内からこの回避策を試してください。 この回避策では、を使用して`/etc/resolv.conf`DNS 解決を手動で上書きすることができます。

1. VPN の DNS サーバーを実行しないように注意してください。`ipconfig.exe /all`
2. 既存の resolv.conf のコピーを作成します。`sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 現在の resolv.conf のリンクを解除します。`sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. および`/etc/resolv.conf`を開く <br/>
   a. ファイルから最初の行を削除します。 "\#このファイルは wsl によって自動的に生成されました。 このファイルの自動生成を停止するには、この行を削除します。 " <br/>
   b. DNS サーバーの一覧の最初のエントリとして、上記の DNS エントリ (1) を追加します。 <br/>
   c. ファイルを閉じます。 <br/>

VPN を切断したら、変更をに`/etc/resolv.conf`戻す必要があります。 これを行うには、次の手順を実行します。
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>WSL を開始するか、ディストリビューションをインストールするとエラーコードが返される

こちらの[手順](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)に従って、詳細なログを収集し、GitHub で問題をファイルに記録してください。

### <a name="updating-bash-on-ubuntu-on-windows"></a>Windows での Bash on Ubuntu の更新

Bash on Ubuntu on Windows では、更新が必要な2つのコンポーネントがあります。 

1. Windows Subsystem for Linux
  
   Bash on Ubuntu on Windows でこの部分をアップグレードすると、[リリースノート](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)の新しい修正のアウトラインが有効になります。 Windows Insider プログラムをサブスクライブしていること、およびビルドが最新であることを確認します。 Ubuntu インスタンスをリセットするなど、より細かな制御を行うには、[コマンドリファレンスページを参照](https://msdn.microsoft.com/en-us/commandline/wsl/reference)してください。

2. Ubuntu ユーザーバイナリ 

   Bash on Ubuntu on Windows でこの部分をアップグレードすると、apt でインストールしたアプリケーションを含め、Ubuntu ユーザーバイナリに更新プログラムがインストールされます。 更新するには、Bash で次のコマンドを実行します。
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt-アップグレードエラーの取得
一部のパッケージでは、まだ実装していない機能が使用されています。 `udev`たとえば、はまだサポートされていない`apt-get upgrade`ため、いくつかのエラーが発生します。

に`udev`関連する問題を修正するには、次の手順に従います。

1. に次のもの`/usr/sbin/policy-rc.d`を書き込んで、変更を保存します。
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 実行アクセス許可の追加先`/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 次のコマンドを実行します。
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>エラー0x80040306 "インストール時
これは、従来のコンソールをサポートしていないという点で必要になります。
レガシコンソールをオフにするには:

1. Cmd.exe を開きます。
1. タイトルバーを右クリックし > プロパティ-> レガシコンソールを使用する をオフにする
1. [OK] をクリックします。

### <a name="error-0x80040154-after-windows-update"></a>エラーWindows update 後の0x80040154 が
Windows update で Windows Subsystem for Linux 機能が無効になっている可能性があります。 この問題が発生した場合は、Windows の機能を再度有効にする必要があります。 Windows Subsystem for Linux を有効にする手順については、[インストールガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)を参照してください。

### <a name="changing-the-display-language"></a>表示言語の変更
WSL install は、Windows インストールのロケールに合わせて Ubuntu のロケールを自動的に変更しようとします。  この動作が不要な場合は、このコマンドを実行して、インストールの完了後に Ubuntu のロケールを変更することができます。  この変更を有効にするには、bash を再起動する必要があります。

次の例では、ロケールを en-us に変更します。
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows システムの復元後のインストールに関する問題
1.  フォルダーを`%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`削除します。 <br/>
  **注:オプションの機能が完全にインストールされ、動作している場合は、この操作を行わないでください。**
2.  WSL オプション機能を有効にします (まだ設定されていない場合)
3.  再起動します
4.  lxrun/uninstall の場合
5.  Bash をインストールする

### <a name="no-internet-access-in-wsl"></a>WSL でインターネットにアクセスできない
一部のユーザーが、WSL でのインターネットアクセスをブロックする特定のファイアウォールアプリケーションに関する問題を報告しています。  報告されるファイアウォールは次のとおりです。

1. Kaspersky
1. AVG
1. Avast

場合によっては、ファイアウォールをオフにすることでアクセスできます。  場合によっては、ファイアウォールをインストールするだけでアクセスがブロックされます。

### <a name="permission-denied-error-when-using-ping"></a>Ping の使用時にアクセス許可拒否エラーが発生する
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14388-to-windows-10-anniversary-update"></a>[記念日の更新](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

WSL で ping を実行するには、Windows の管理者特権が必要です。  Ping を実行するには、管理者として Windows 上で Bash on Ubuntu を実行するか、管理者特権を使用して CMD/PowerShell プロンプトから bash を実行します。

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14926"></a>[ビルド 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  管理者特権は不要になりました。

### <a name="bash-is-hung"></a>Bash がハングしています
Bash を使用しているときに bash がハングしている (またはデッドロックされている) ことが検出され、入力に応答していない場合は、メモリダンプを収集して報告することによって問題を診断してください。 これらの手順はシステムをクラッシュさせることに注意してください。 これに慣れていない場合や、作業を保存する前に作業を保存していない場合は、この操作を行わないでください。  <br/>
メモリダンプを収集するには:
1. メモリダンプの種類を "完全なメモリダンプ" に変更します。 ダンプの種類を変更するときに、現在の型をメモしておきます。
2. キーボードコントロールを使用してクラッシュを構成する[手順](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/)を使用します。
3. ハングまたはデッドロックを再現します。
4. (2) のキーシーケンスを使用してシステムをクラッシュさせる。
5. システムはクラッシュし、メモリダンプを収集します。
6. システムが再起動したら、memory.dmp をにsecure@microsoft.com報告します。 ダンプファイルの既定の場所は、C:\Windows\memory.dmp、または C: がシステムドライブである場合は、になります。 電子メールでは、ダンプは WSL または Bash on Windows チーム用です。
7. メモリダンプの種類を元の設定に復元します。

### <a name="check-your-build-number"></a>ビルド番号を確認する

PC のアーキテクチャと Windows ビルド番号を確認するには、を開きます。  
**設定** > システムに > **ついて**

**[OS ビルド]** フィールドと **[システムの種類]** フィールドを探します。  
    ![ビルドとシステムの種類のフィールドのスクリーンショット](media/system.png) 


Windows Server のビルド番号を確認するには、PowerShell で次のように実行します。  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>WSL が有効になっていることを確認する
Windows Subsystem for Linux が有効になっていることを確認するには、PowerShell で次のように実行します。  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH-サーバー接続に関する問題
SSH サーバーに接続しようとしましたが、次のエラーで失敗しました:"127.0.0.1 ポート22によって接続が切断されました。"
1. OpenSSH サーバーが実行されていることを確認します。
   ``` BASH
   sudo service ssh status
   ```
   次に、このチュートリアルに従っています。 https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Sshd サービスを停止し、デバッグモードで sshd を開始します。
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. スタートアップログを確認し、HostKeys が使用可能であり、次のようなログメッセージが表示されていないことを確認します。
   ```
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

このようなメッセージが表示されていて、 `/etc/ssh/`キーがにない場合は、キーを再生成するか、または & を削除するだけで openssh-server をインストールする必要があります。
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

