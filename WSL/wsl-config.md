---
title: Linux ディストリビューションの管理
description: Windows Subsystem for Linux で実行されている複数の Linux ディストリビューションの一覧表示と構成に関するリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e69810625d08baf734683ff06231f79132ce1519
ms.sourcegitcommit: e1cc2fe4de0fa03d5aea14f6b328f1bb9d0c59be
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2019
ms.locfileid: "71999393"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Windows Subsystem for Linux の管理と構成

> Windows 10 Fall Creators Update 以降に適用されます。  新しい管理機能を試して、Microsoft Store から複数の Linux ディストリビューションの実行を開始するには、更新された[インストール ガイド](./install_guide.md)を参照してください。

## <a name="ways-to-run-wsl"></a>WSL を実行する方法

Windows Subsystem for Linux での Linux の実行には、さまざまな方法があります。

1. `[distro]`、例えば `ubuntu`
1. `wsl.exe` または `bash.exe`
1. `wsl [command]` または `bash -c [command]`

どの方法を使用すべきかは、作業内容によって異なります。

### <a name="launch-wsl-by-distribution"></a>ディストリビューションによって WSL を起動する

ディストリビューション固有のアプリケーションを使用してディストリビューションを実行すると、そのディストリビューションが独自のコンソール ウィンドウで起動します。

![[スタート] メニューからの WSL の起動](media/start-launch.png)

これは、Microsoft Store で [起動] をクリックすることと同じです。

![Microsoft Store からの WSL の起動](media/store-launch.png)

`[distribution].exe` を実行して、コマンド ラインからディストリビューションを実行することもできます。

この方法でコマンド ラインからディストリビューションを実行すると、作業ディレクトリが現在のディレクトリからディストリビューションのホーム ディレクトリに自動的に変更されるという欠点があります。

**例:**

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

### <a name="wsl-and-wsl-command"></a>wsl および wsl [コマンド]

コマンド ラインから WSL を実行する最善の方法は、`wsl.exe` を使用することです。

**例:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

`wsl` は、現在の作業ディレクトリを適切に維持するだけでなく、1 つのコマンドを Windows コマンドとともに実行できます。

**例:**

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

**例:**

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


## <a name="managing-multiple-linux-distributions"></a>複数の Linux ディストリビューションの管理

### <a name="windows-10-version-1903-and-later"></a>Windows 10 バージョン 1903 以降

`wsl.exe` を使用して、Windows Subsystem for Linux (WSL) のディストリビューションを管理できます。これには、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、ディストリビューションのアンインストールが含まれます。

各 Linux ディストリビューションは、個別に独自の構成を管理します。 ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。  たとえば、`ubuntu /?` のように指定します。

#### <a name="list-distributions"></a>ディストリビューションの一覧表示

`wsl -l`、`wsl --list`  
WSL で利用可能な Linux ディストリビューションを一覧表示します。  一覧表示されているディストリビューションは、インストールされており、使用できる状態です。

`wsl --list --all`   
現在使用できないディストリビューションを含む、すべてのディストリビューションを一覧表示します。  インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。  

`wsl --list --running`   
現在実行中のディストリビューションをすべて一覧表示します。

#### <a name="set-a-default-distribution"></a>既定のディストリビューションの設定

既定の WSL ディストリビューションは、コマンド ラインで `wsl` を実行するときに実行されるものです。

`wsl -s <DistributionName>`、`wsl --setdefault <DistributionName>`

既定のディストリビューションを `<DistributionName>` に設定します。

**例:**  
`wsl -s Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。  これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。  `wsl` を実行すると、Ubuntu セッションが開きます。

#### <a name="unregister-and-reinstall-a-distribution"></a>ディストリビューションの登録解除と再インストール

Linux ディストリビューションは Microsoft Store を介してインストールできますが、そのストアを介してアンインストールすることはできません。  WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。

登録を解除すると、ディストリビューションを再インストールすることもできます。

> **注:** 登録が解除されると、そのディストリビューションに関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。  ストアから再インストールすると、ディストリビューションのクリーン コピーがインストールされます。

`wsl --unregister <DistributionName>`  
ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。

たとえば、`wsl --unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。  `wsl --list` を実行すると、それは一覧に表示されません。

再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。

#### <a name="run-as-a-specific-user"></a>特定のユーザーとしての実行

`wsl -u <Username>`、`wsl --user <Username>`

指定されたユーザーとして WSL を実行します。 ユーザーは WSL ディストリビューション内に存在する必要があることに注意してください。

#### <a name="run-a-specific-distribution"></a>特定のディストリビューションの実行

`wsl -d <DistributionName>`、`wsl --distribution <DistributionName>`

WSL の指定したディストリビューションの実行は、既定値を変更する必要なしに、特定のディストリビューションにコマンドを送信するために使用できます。

### <a name="versions-earlier-than-windows-10-version-1903"></a>Windows 10 バージョン 1903 より前のバージョン

WSL Config (`wslconfig.exe`) は、Windows Subsystem for Linux (WSL) で実行されている Linux ディストリビューションを管理するためのコマンド ライン ツールです。  これにより、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールを行うことができます。

WSL Config はディストリビューションにまたがる設定やそれらを調整する設定に役立ちますが、各 Linux ディストリビューションは個別に独自の構成を管理します。  ディストリビューション固有のコマンドを確認するには、`[distro.exe] /?` を実行します。  たとえば、`ubuntu /?` のように指定します。

wslconfig で使用可能なオプションをすべて表示するには、`wslconfig /?` を実行します。

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

#### <a name="list-distributions"></a>ディストリビューションの一覧表示

`wslconfig /list`  
WSL で利用可能な Linux ディストリビューションを一覧表示します。  一覧表示されているディストリビューションは、インストールされており、使用できる状態です。

`wslconfig /list /all`  
現在使用できないディストリビューションを含む、すべてのディストリビューションを一覧表示します。  インストールのプロセス中、アンインストールのプロセス中、または破損した状態の可能性があります。  

#### <a name="set-a-default-distribution"></a>既定のディストリビューションの設定

既定の WSL ディストリビューションは、コマンド ラインで `wsl` を実行するときに実行されるものです。

`wslconfig /setdefault <DistributionName>`

既定のディストリビューションを `<DistributionName>` に設定します。

**例:**  
`wslconfig /setdefault Ubuntu` の場合、既定のディストリビューションが Ubuntu に設定されます。  これで、`wsl npm init` を実行すると、Ubuntu で実行されるようになります。  `wsl` を実行すると、Ubuntu セッションが開きます。

#### <a name="unregister-and-reinstall-a-distribution"></a>ディストリビューションの登録解除と再インストール

Linux ディストリビューションは Microsoft Store を介してインストールできますが、そのストアを介してアンインストールすることはできません。  WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。

登録を解除すると、ディストリビューションを再インストールすることもできます。

> **注:** 登録が解除されると、そのディストリビューションに関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。  ストアから再インストールすると、ディストリビューションのクリーン コピーがインストールされます。

`wslconfig /unregister <DistributionName>`  
ディストリビューションを再インストールまたはクリーンアップできるように、WSL からその登録が解除されます。

たとえば、`wslconfig /unregister Ubuntu` の場合、WSL で使用可能なディストリビューションから Ubuntu が削除されます。  `wslconfig /list` を実行すると、それは一覧に表示されません。

再インストールするには、Microsoft Store でディストリビューションを見つけて、[起動] を選択します。

## <a name="set-wsl-launch-settings"></a>WSL 起動設定の実行

> **Windows Insider Build 17093 以降で使用可能**

`wsl.conf` を使用して、サブシステムを起動するたびに適用される、WSL の特定の機能を自動的に構成します。 

現時点では、これには自動マウント オプションとネットワーク構成が含まれています。

`wsl.conf` は、`/etc/wsl.conf` 内の各 Linux ディストリビューションにあります。 そのファイルがそこになければ、自分で作成できます。 WSL は、ファイルの存在を検出し、その内容を読み取ります。 ファイルが見つからないか、形式が正しくない (つまり、不適切なマークアップ形式である) 場合、WSL は通常どおりに起動を続けます。

ディストリビューションに追加できる `wsl.conf` サンプル ファイルを次に示します。

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

.ini 規則に従って、キーはセクションの下で宣言されます。 

WSL では、`automount` と `network` の 2 つのセクションがサポートされています。

#### <a name="automount"></a>automount

セクション: `[automount]`


| key        | value                          | 既定      | 注                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` にすると、固定ドライブ (つまり、 `C:/` または`D:/`) は `/mnt` の下に DrvFs で自動的にマウントされます。  `false` にすると、ドライブは自動的にマウントされませんが、依然として手動または `fstab` を使用してマウントできます。                                                                                                             |
| mountFsTab | boolean                        | true         | `true` にすると、WSL 開始時に処理されるように `/etc/fstab` を設定します。 /etc/fstab は、SMB 共有などの他のファイル システムを宣言できるファイルです。 そのため、起動時にこれらのファイル システムを WSL 内で自動的にマウントできます。                                                                                                                |
| root       | String                         | `/mnt/`      | 固定ドライブが自動的にマウントされるディレクトリを設定します。 たとえば、`/windir/` に WSL のディレクトリがあり、それをルートとして指定すると、固定ドライブは `/windir/c` でマウントされることが予想されます。                                                                                              |
| オプション    | 値のコンマ区切りのリスト | 空の文字列 | この値は、既定の DrvFs マウント オプション文字列に追加されます。 **DrvFs 固有のオプションのみを指定できます。** マウント バイナリが通常、フラグに解析するオプションはサポートされていません。 これらのオプションを明示的に指定する場合は、それを行う対象のドライブすべてを /etc/fstab に含める必要があります。 |

既定では、WSL は uid と gid を既定のユーザーの値に設定します (Ubuntu ディストリビューションでは、既定のユーザーは uid = 1000、gid = 1000 で作成されます)。 ユーザーがこのキーを使用して gid または uid オプションを明示的に指定した場合、関連する値は上書きされます。 それ以外の場合は、既定値が常に追加されます。

**注:** これらのオプションは、自動的にマウントされたドライブすべてのマウント オプションとして適用されます。 特定のドライブのみのオプションを変更するには、代わりに /etc/fstab を使用します。

##### <a name="mount-options"></a>マウント オプション

Windows ドライブ (DrvFs) にさまざまなマウント オプションを設定すると、Windows ファイルのファイルのアクセス許可を計算する方法を制御できます。 次のオプションが使用できます。

| キー | 説明 | 既定 |
|:----|:----|:----|
|uid| すべてのファイルの所有者に使用するユーザー ID | WSL ディストリビューションの既定のユーザー ID (初回インストールの場合、既定値は 1000)
|gid| すべてのファイルの所有者に使用するグループ ID | WSL ディストリビューションの既定のグループ ID (初回インストールの場合、既定値は 1000)
|umask | すべてのファイルとディレクトリに対して除外するアクセス許可の 8 進数のマスク | 000
|fmask | すべてのファイルに対して除外するアクセス許可の 8 進数のマスク | 000
|dmask | すべてのディレクトリに対して除外するアクセス許可の 8 進数のマスク | 000

**注:** アクセス許可のマスクは、ファイルまたはディレクトリに適用される前に論理 OR 演算によって配置されます。 

#### <a name="network"></a>ネットワーク

セクションのラベル: `[network]`

| key | value | 既定 | 注|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` にすると、`/etc/hosts` を生成するように WSL を設定します。 `hosts` ファイルには、IP アドレスに対応するホスト名の静的マップが含まれています。 |
| generateResolvConf | boolean | `true` | `true` にすると、`/etc/resolv.conf` を生成するように WSL を設定します。 `resolv.conf` には、指定されたホスト名をその IP アドレスに解決できる DNS リストが含まれています。 | 

#### <a name="interop"></a>interop

セクションのラベル: `[interop]`

次のオプションは、Insider Build 17713 以降で使用できます。

| key | value | 既定 | 注|
|:----|:----|:----|:----|
| enabled | boolean | `true` | このキーの設定により、WSL で Windows プロセスの起動をサポートするかどうかが決まります。 |
| appendWindowsPath | boolean | `true` | このキーの設定により、WSL が Windows パス要素を $PATH 環境変数に追加するかどうかが決まります。 | 
