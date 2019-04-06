---
title: Linux ディストリビューションを管理します。
description: 一覧に表示され、Linux 用 Windows サブシステムで実行されている複数の Linux ディストリビューションの構成を参照します。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、wsl.conf wslconfig 用 windows サブシステム
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063500"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>管理および Linux 用の Windows サブシステムの構成

> Windows 10 Fall Creators Update 以降を適用します。  表示、更新された[インストール ガイド](./install_guide.md)新しい管理機能を Windows ストアからの複数の Linux ディストリビューションの実行を開始します。

## <a name="ways-to-run-wsl"></a>WSL を実行する方法

Linux 用 Windows サブシステムで Linux を実行する方法はたくさんあります。

1. `[distro]` IE `ubuntu`
1. `wsl.exe` または `bash.exe`
1. `wsl [command]` または `bash -c [command]`

使用する必要がありますメソッドは、何をしているに依存します。

### <a name="launch-wsl-by-distribution"></a>WSL を配布して起動します。

ディストリビューション固有のアプリケーションを使用してディストリビューションを実行して、独自のコンソール ウィンドウには、その配布を起動します。

![WSL を [スタート] メニューから起動します。](media/start-launch.png)

Windows ストアで「起動」をクリックすると同じです。

![Windows ストアから WSL を起動します。](media/store-launch.png)

実行して、コマンドラインから、配布を実行することも`[distribution].exe`します。

ディストリビューションを実行して、この方法でコマンドラインからの欠点はことには自動的に作業ディレクトリ現在のディレクトリからに変更配布のホーム ディレクトリ。

**以下に例を示します。**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>wsl と wsl [コマンド]

WSL をコマンドラインから実行する最善の方法を使用して`wsl.exe`します。

**以下に例を示します。**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

だけでなく`wsl`に現在の作業ディレクトリを維持、に沿って側の Windows のコマンドの 1 つのコマンドを実行できます。

**以下に例を示します。**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**以下に例を示します。**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a>複数の Linux ディストリビューションを管理します。

### <a name="windows-10-version-1903-and-later"></a>Windows 10 バージョンが 1903 以降

使用することができます`wsl.exe`ディストリビューション、Windows サブシステムでの Linux (WSL)、利用可能なディストリビューションの一覧を表示する既定のディストリビューションを設定、ディストリビューションをアンインストールするなどを管理します。

各 Linux ディストリビューションが独自の構成を個別に管理します。 ディストリビューション固有のコマンドを表示する実行`[distro.exe] /?`します。  たとえば、 `ubuntu /?`があります。

#### <a name="list-distributions"></a>ディストリビューションの一覧

`wsl -l` 、 `wsl --list`  
WSL を利用できる Linux ディストリビューションを使用可能なを一覧表示します。  分布が表示されている場合がインストールされ、使用する準備が完了します。

`wsl --list --all`   
現在使用するものも含め、すべてのディストリビューションの一覧を表示します。  これらは、アンインストール、インストールすると、処理中である可能性がありますや破損した状態では。  

`wsl --list --running`   
現在実行されているすべてのディストリビューションの一覧を表示します。

#### <a name="set-a-default-distribution"></a>既定の配布を設定します。

既定のディストリビューションで WSL を実行するときに実行される 1 つ`wsl`コマンド行にします。

`wsl -s <DistributionName>`、 `wsl --setdefault <DistributionName>`

既定の配布を設定`<DistributionName>`します。

**以下に例を示します。**  
`wsl -s Ubuntu` 既定のディストリビューションを Ubuntu に設定します。  今すぐ実行すると`wsl npm init`Ubuntu で実行されます。  実行した場合の`wsl`Ubuntu のセッションが開きます。

#### <a name="unregister-and-reinstall-a-distribution"></a>登録を解除して、配布を再インストール

Linux ディストリビューションは、Windows でインストールできるときにストアは、ストアからをアンインストールできません。  WSL 構成は、未登録のアンインストールに配布できます。

登録を解除すると、ディストリビューションを再インストールすることもできます。

> **注:**、登録を解除するとすべてのデータ、設定、およびそのディストリビューションに関連付けられているソフトウェアは完全に失われます。  ストアから再インストールすると、分布のクリーンなコピーがインストールされます。

`wsl --unregister <DistributionName>`  
WSL から配布を再インストールまたはクリーンアップできるように登録を解除します。

例: `wsl -unregister Ubuntu` WSL で使用可能なディストリビューションから Ubuntu を削除します。  実行すると`wsl --list`表示されません。

を再インストールするには、Windows ストアで、分布を検索し、「起動」を選択します。

#### <a name="run-as-a-specific-user"></a>特定のユーザーとして実行します。

`wsl -u <Username>`、 `wsl --user <Username>`

WSL は、指定したユーザーとして実行します。 WSL 配布内でそのユーザーが存在する必要がありますに注意してください。

#### <a name="run-a-specific-distribution"></a>特定の配布を実行します。

`wsl --d <DistributionName>`、 `wsl --distribution <DistributionName>`

WSL の指定した配布を実行する、既定値を変更することがなく特定の配布のコマンドを送信するために使用できます。

### <a name="versions-earlier-than-windows-10-version-1903"></a>Windows 10 バージョンが 1903 より前のバージョン

WSL Config (`wslconfig.exe`) for Linux (WSL) Windows サブシステムで実行されている Linux ディストリビューションを管理するためのコマンド ライン ツールです。  利用可能なディストリビューションを一覧表示、設定の既定のディストリビューションおよびディストリビューションをアンインストールすることができます。

WSL Config は span またはディストリビューションの調整設定の場合に便利ですが、各 Linux ディストリビューション個別に管理しない独自構成します。  ディストリビューション固有のコマンドを表示する実行`[distro.exe] /?`します。  たとえば、 `ubuntu /?`があります。

Wslconfig のすべての使用可能なオプションを表示するには、次のコマンドを実行します。  `wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a>ディストリビューションの一覧

`wslconfig /list`  
WSL を利用できる Linux ディストリビューションを使用可能なを一覧表示します。  分布が表示されている場合がインストールされ、使用する準備が完了します。

`wslconfig /list /all`  
現在使用するものも含め、すべてのディストリビューションの一覧を表示します。  これらは、アンインストール、インストールすると、処理中である可能性がありますや破損した状態では。  

#### <a name="set-a-default-distribution"></a>既定の配布を設定します。

既定のディストリビューションで WSL を実行するときに実行される 1 つ`wsl`コマンド行にします。

`wslconfig /setdefault <DistributionName>`

既定の配布を設定`<DistributionName>`します。

**以下に例を示します。**  
`wslconfig /setdefault Ubuntu` 既定のディストリビューションを Ubuntu に設定します。  今すぐ実行すると`wsl npm init`Ubuntu で実行されます。  実行した場合の`wsl`Ubuntu のセッションが開きます。

#### <a name="unregister-and-reinstall-a-distribution"></a>登録を解除して、配布を再インストール

Linux ディストリビューションは、Windows でインストールできるときにストアは、ストアからをアンインストールできません。  WSL 構成は、未登録のアンインストールに配布できます。

登録を解除すると、ディストリビューションを再インストールすることもできます。

> **注:**、登録を解除するとすべてのデータ、設定、およびそのディストリビューションに関連付けられているソフトウェアは完全に失われます。  ストアから再インストールすると、分布のクリーンなコピーがインストールされます。

`wslconfig /unregister <DistributionName>`  
WSL から配布を再インストールまたはクリーンアップできるように登録を解除します。

例: `wslconfig /unregister Ubuntu` WSL で使用可能なディストリビューションから Ubuntu を削除します。  実行すると`wslconfig /list`表示されません。

を再インストールするには、Windows ストアで、分布を検索し、「起動」を選択します。

## <a name="set-wsl-launch-settings"></a>WSL 起動を設定します。

> **Windows Insider ビルド 17093 で使用でき、それ以降**

サブシステムを使用して、起動するたびに適用される WSL で特定の機能を自動構成`wsl.conf`します。 

右にはここで、これが含まれていますに対する自動マウント オプションおよびネットワークの構成。

`wsl.conf` 場合は、各 Linux ディストリビューションである`/etc/wsl.conf`します。 ファイルがない場合を自分でその作成できます。 WSL では、ファイルの存在が検出され、その内容を読み取る。 ファイルが見つからないか、形式が正しくない場合 (つまり、不適切なマークアップの書式設定)、WSL は引き続き通常どおり起動します。

サンプルを次に示します`wsl.conf`ファイルは、ディストリビューションに追加できます。

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>構成オプション

.Ini の表記規則、合わせてセクション、キーとして宣言されます。 

WSL は、2 つのセクションをサポートしています:`automount`と`network`します。

#### <a name="automount"></a>自動マウント

セクションの内容: `[automount]`


| key        | value                          | 既定値 (default)      | ノート                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` 固定ドライブ (つまり、エラーの原因 `C:/` または`D:/`) DrvFs 下で自動的にマウントする`/mnt`します。  `false` ドライブを自動的にマウントしないを手動でまたはを使用してに引き続きマウントしてでした`fstab`します。                                                                                                             |
| mountFsTab | boolean                        | true         | `true` 設定`/etc/fstab`処理する WSL 開始します。 /etc/fstab は、SMB 共有のように、その他のファイル システムを宣言するファイルです。 したがっての開始時に WSL で自動的にこれらのファイル システムをマウントできます。                                                                                                                |
| ルート       | String                         | `/mnt/`      | 固定ドライブが自動的にマウントされます、ディレクトリを設定します。 WSL でのディレクトリがある場合など`/windir/`指定こととして、ルートには必要でマウントされている固定ドライブを参照してください。 `/windir/c`                                                                                              |
| オプション    | 値のコンマ区切りの一覧 | 空の文字列 | この値は、既定 DrvFs マウント オプション文字列に追加されます。 **DrvFs 固有のオプションのみを指定することができます。** バイナリのマウントがフラグに解析は通常のオプションがサポートされていません。 これらのオプションを明示的に指定する場合は、/etc/fstab で実行するすべてのドライブを含める必要があります。 |

既定では、WSL uid と gid 値に設定の既定のユーザー (uid を使用した Ubuntu ディストリビューションでは、既定のユーザーが作成 = 1000、gid = 1000)。 ユーザーは、このキーを使用して明示的に gid または uid オプションを指定する場合、関連付けられている値が上書きされます。 それ以外の場合、既定値は常に追加されます。

**注:** これらのオプションは、すべて自動的にマウントされたドライブのマウント オプションとして適用されます。 特定のドライブのみのオプションを変更するには、/etc/fstab を代わりに使用します。

#### <a name="network"></a>ネットワーク

セクション ラベル: `[network]`

| key | value | 既定値 (default) | ノート|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` 設定を生成する WSL`/etc/hosts`します。 `hosts`ファイルには、ホスト名の対応する IP アドレスの静的なマップが含まれています。 |
| generateResolvConf | boolean | `true` | `true` 設定を生成する WSL`/etc/resolv.conf`します。 `resolv.conf`特定のホスト名をその IP アドレスに解決することができる DNS の一覧が含まれています。 | 

#### <a name="interop"></a>相互運用機能

セクション ラベル: `[interop]`

これらのオプションとは、以降 Insider ビルド 17713 で利用可能です。

| key | value | 既定値 (default) | ノート|
|:----|:----|:----|:----|
| enabled | boolean | `true` | このキーの設定で、WSL が Windows の起動プロセスをサポートするかどうかを決定します。 |
| appendWindowsPath | boolean | `true` | このキーの設定で、WSL が $PATH 環境変数に Windows のパス要素を追加するかどうかを決定します。 | 
