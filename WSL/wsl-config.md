---
title: Linux ディストリビューションの管理
description: Windows Subsystem for Linux で実行されている複数の Linux ディストリビューションの一覧と構成については、こちらを参照してください。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、wsl. conf、wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: ca65cf6fde3e0ba4750ffc44f5aec542be6cfabf
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122703"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Windows Subsystem for Linux の管理と構成

> Windows 10 の作成者の更新プログラム以降に適用されます。  更新された[インストールガイド](./install_guide.md)を参照して、新しい管理機能を試し、Microsoft ストアから複数の Linux ディストリビューションの実行を開始してください。

## <a name="ways-to-run-wsl"></a>WSL を実行する方法

Windows Subsystem for Linux を使用して Linux を実行するには、さまざまな方法があります。

1. `[distro]`例えば`ubuntu`
1. `wsl.exe` または `bash.exe`
1. `wsl [command]` または `bash -c [command]`

どの方法を使用するかは、実行している内容によって異なります。

### <a name="launch-wsl-by-distribution"></a>ディストリビューションによる WSL の起動

ディストリビューション固有のアプリケーションを使用してディストリビューションを実行すると、その配布が独自のコンソールウィンドウで起動します。

![[スタート] メニューから WSL を起動する](media/start-launch.png)

これは、Microsoft ストアで [起動] をクリックすることと同じです。

![Microsoft ストアから WSL を起動します](media/store-launch.png)

を実行`[distribution].exe`してコマンドラインから配布を実行することもできます。

この方法でコマンドラインから配布を実行すると、作業ディレクトリが現在のディレクトリから配布のホームディレクトリに自動的に変更されるという欠点があります。

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

### <a name="wsl-and-wsl-command"></a>wsl および wsl [command]

コマンドラインから WSL を実行する最善の方法は、 `wsl.exe`を使用することです。

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

現在の作業`wsl`ディレクトリをその場で保持するだけでなく、1つのコマンドを Windows コマンドで実行できます。

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

### <a name="windows-10-version-1903-and-later"></a>Windows 10 バージョン1903以降

を使用`wsl.exe`して、Windows Subsystem for Linux (wsl) でディストリビューションを管理できます。これには、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールが含まれます。

各 Linux ディストリビューションは、個別に独自の構成を管理します。 ディストリビューション固有のコマンドを表示するに`[distro.exe] /?`は、を実行します。  たとえば、 `ubuntu /?`があります。

#### <a name="list-distributions"></a>ディストリビューションの一覧表示

`wsl -l`,`wsl --list`  
WSL で利用可能な Linux ディストリビューションを一覧表示します。  配布リストが表示されている場合は、インストールされており、使用準備ができています。

`wsl --list --all`   
現在使用できないすべてのディストリビューションを含む、すべてのディストリビューションを一覧表示します。  インストール、アンインストール、または破損した状態になっている可能性があります。  

`wsl --list --running`   
現在実行中のすべてのディストリビューションを一覧表示します。

#### <a name="set-a-default-distribution"></a>既定のディストリビューションを設定する

既定の wsl ディストリビューションは、コマンドラインでを実行`wsl`するときに実行される分散です。

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

既定の分布をに`<DistributionName>`設定します。

**例:**  
`wsl -s Ubuntu`既定のディストリビューションを Ubuntu に設定します。  実行`wsl npm init`すると、Ubuntu で実行されるようになります。  これを実行`wsl`すると、Ubuntu セッションが開きます。

#### <a name="unregister-and-reinstall-a-distribution"></a>配布の登録解除と再インストール

Linux ディストリビューションは Microsoft ストアを介してインストールできますが、ストアを使用してアンインストールすることはできません。  WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。

登録を解除すると、ディストリビューションを再インストールすることもできます。

> **注意:** 登録が解除されると、その配布に関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。  ストアから再インストールすると、配布のクリーンコピーがインストールされます。

`wsl --unregister <DistributionName>`  
WSL からのディストリビューションの登録を解除して、再インストールまたはクリーンアップできるようにします。

たとえば`wsl --unregister Ubuntu` 、は、wsl で使用可能なディストリビューションから Ubuntu を削除します。  実行`wsl --list`すると、一覧に表示されません。

を再インストールするには、Microsoft ストアで配布を見つけて、[Launch] \ (起動 \) を選択します。

#### <a name="run-as-a-specific-user"></a>特定のユーザーとして実行する

`wsl -u <Username>`, `wsl --user <Username>`

指定されたユーザーとして WSL を実行します。 ユーザーは WSL 分布内に存在する必要があることに注意してください。

#### <a name="run-a-specific-distribution"></a>特定の配布を実行する

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

指定した WSL の分布を実行すると、既定値を変更しなくても、特定のディストリビューションにコマンドを送信できます。

### <a name="versions-earlier-than-windows-10-version-1903"></a>Windows 10 バージョン1903より前のバージョン

Wsl Config (`wslconfig.exe`) は、Windows Subsystem for linux (wsl) で実行されている linux ディストリビューションを管理するためのコマンドラインツールです。  これにより、使用可能なディストリビューションの一覧表示、既定のディストリビューションの設定、およびディストリビューションのアンインストールを行うことができます。

WSL Config は分布にまたがる設定に役立ちますが、各 Linux ディストリビューションは個別に独自の構成を管理します。  ディストリビューション固有のコマンドを表示するに`[distro.exe] /?`は、を実行します。  たとえば、 `ubuntu /?`があります。

Wslconfig で使用可能なすべてのオプションを表示するには、次のように実行します。`wslconfig /?`

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
WSL で利用可能な Linux ディストリビューションを一覧表示します。  配布リストが表示されている場合は、インストールされており、使用準備ができています。

`wslconfig /list /all`  
現在使用できないすべてのディストリビューションを含む、すべてのディストリビューションを一覧表示します。  インストール、アンインストール、または破損した状態になっている可能性があります。  

#### <a name="set-a-default-distribution"></a>既定のディストリビューションを設定する

既定の wsl ディストリビューションは、コマンドラインでを実行`wsl`するときに実行される分散です。

`wslconfig /setdefault <DistributionName>`

既定の分布をに`<DistributionName>`設定します。

**例:**  
`wslconfig /setdefault Ubuntu`既定のディストリビューションを Ubuntu に設定します。  実行`wsl npm init`すると、Ubuntu で実行されるようになります。  これを実行`wsl`すると、Ubuntu セッションが開きます。

#### <a name="unregister-and-reinstall-a-distribution"></a>配布の登録解除と再インストール

Linux ディストリビューションは Microsoft ストアを介してインストールできますが、ストアを使用してアンインストールすることはできません。  WSL Config を使用すると、ディストリビューションの登録解除/アンインストールを行うことができます。

登録を解除すると、ディストリビューションを再インストールすることもできます。

> **注意:** 登録が解除されると、その配布に関連付けられているすべてのデータ、設定、およびソフトウェアが完全に失われます。  ストアから再インストールすると、配布のクリーンコピーがインストールされます。

`wslconfig /unregister <DistributionName>`  
WSL からのディストリビューションの登録を解除して、再インストールまたはクリーンアップできるようにします。

たとえば`wslconfig /unregister Ubuntu` 、は、wsl で使用可能なディストリビューションから Ubuntu を削除します。  実行`wslconfig /list`すると、一覧に表示されません。

を再インストールするには、Microsoft ストアで配布を見つけて、[Launch] \ (起動 \) を選択します。

## <a name="set-wsl-launch-settings"></a>WSL 起動設定の設定

> **Windows Insider Build 17093 以降で使用可能**

を使用して`wsl.conf`サブシステムを起動するたびに適用される、wsl の特定の機能を自動的に構成します。 

現時点では、これには自動マウントオプションとネットワーク構成が含まれています。

`wsl.conf`は、の`/etc/wsl.conf`各 Linux ディストリビューションにあります。 ファイルが存在しない場合は、自分で作成できます。 WSL は、ファイルの存在を検出し、その内容を読み取ります。 ファイルが見つからないか、形式が正しくない (つまり、不適切なマークアップ形式である) 場合、WSL は通常どおりに起動し続けます。

ディストリビューションに追加できる`wsl.conf`サンプルファイルを次に示します。

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

.Ini 規則に従うと、キーはセクションの下で宣言されます。 

Wsl では`automount` 、との`network`2 つのセクションがサポートされています。

#### <a name="automount"></a>オートマ

下`[automount]`


| キー (key)        | value                          | 既定値 (default)      | 注記                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true`固定ドライブ (つまり、 `C:/`また`D:/`は) の場合、 `/mnt`drvfs で自動的にマウントされます。  `false`ドライブは自動的にマウントされませんが、手動またはを使用`fstab`してマウントすることもできます。                                                                                                             |
| mountFsTab | boolean                        | true         | `true`wsl start で処理されるように設定`/etc/fstab`します。 /etc/fstab は、SMB 共有などの他のファイルシステムを宣言できるファイルです。 そのため、これらのファイルシステムは起動時に WSL に自動的にマウントできます。                                                                                                                |
| ルート       | String                         | `/mnt/`      | 固定ドライブが自動的にマウントされるディレクトリを設定します。 たとえば、wsl at `/windir/`にディレクトリがあり、それをルートとして指定すると、固定ドライブがにマウントされていることがわかります。`/windir/c`                                                                                              |
| options    | 値のコンマ区切りのリスト | 空の文字列 | この値は、既定の DrvFs マウントオプション文字列に追加されます。 **DrvFs 固有のオプションのみを指定できます。** 通常、マウントバイナリがフラグに解析するオプションはサポートされていません。 これらのオプションを明示的に指定する場合は、/etc/fstab で使用するすべてのドライブを含める必要があります。 |

既定では、WSL は uid と gid を既定のユーザーの値に設定します (Ubuntu ディストリビューションでは、既定のユーザーは uid = 1000, gid = 1000 で作成されます)。 ユーザーがこのキーを使用して gid または uid オプションを明示的に指定した場合、関連付けられている値は上書きされます。 それ以外の場合は、既定値が常に追加されます。

**注:** これらのオプションは、自動的にマウントされたすべてのドライブのマウントオプションとして適用されます。 特定のドライブのオプションのみを変更するには、代わりに/etc/fstab を使用します。

#### <a name="network"></a>ネットワーク

セクションラベル:`[network]`

| キー (key) | value | 既定値 (default) | 注記|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true`生成`/etc/hosts`する wsl を設定します。 この`hosts`ファイルには、ホスト名に対応する IP アドレスの静的マップが含まれています。 |
| generateResolvConf | boolean | `true` | `true`生成`/etc/resolv.conf`するように wsl を設定します。 に`resolv.conf`は、指定されたホスト名を IP アドレスに解決できる DNS リストが含まれています。 | 

#### <a name="interop"></a>固有

セクションラベル:`[interop]`

これらのオプションは、Insider Build 17713 以降で使用できます。

| キー (key) | value | 既定値 (default) | 注記|
|:----|:----|:----|:----|
| enabled | boolean | `true` | このキーを設定すると、WSL が Windows プロセスの起動をサポートするかどうかが決まります。 |
| appendWindowsPath | boolean | `true` | このキーを設定すると、WSL が Windows パス要素を $PATH 環境変数に追加するかどうかが決まります。 | 
