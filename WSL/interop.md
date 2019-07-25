---
title: Windows と Linux の相互運用性
description: Windows Subsystem for Linux で実行されている Linux ディストリビューションとの Windows の相互運用性について説明します。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040819"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows と Linux の相互運用性のための windows サブシステム

> **秋の作成者の更新に関する情報が更新されました。**  
作成者の更新プログラムまたは記念日の更新プログラムを実行している場合は、[作成者[/記念日] セクション](interop.md#creators-update-and-anniversary-update)に移動します。

Windows Subsystem for Linux (WSL) は、Windows と Linux 間の統合を継続的に改善しています。  可能な代替手段としては以下の方法があります。

1. Linux コンソールから Windows バイナリを呼び出します。
1. Windows コンソールから Linux バイナリを起動します。
1. **Windows Insider ビルド 17063 +** Linux と Windows の間で環境変数を共有します。

これにより、Windows と WSL の間でシームレスなエクスペリエンスが提供されます。  技術的な詳細については、 [Wsl ブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)をご覧ください。

## <a name="run-linux-tools-from-a-windows-command-line"></a>Windows コマンドラインからの Linux ツールの実行

を使用して`wsl.exe <command>`、Windows コマンドプロンプト (CMD または PowerShell) から Linux バイナリを実行します。

バイナリは次の方法で呼び出されます。

1. 現在のコマンドプロンプトまたは PowerShell プロンプトと同じ作業ディレクトリを使用します。
1. WSL の既定のユーザーとして実行します。
1. 呼び出しプロセスとターミナルと同じ Windows 管理者権限を持っている。

以下に例を示します。

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

次に示す`wsl.exe` Linux コマンドは、wsl でのコマンド実行と同様に処理されます。  Sudo、パイプ、ファイルリダイレクトなどが機能します。

Sudo を使用した例:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

WSL コマンドと Windows コマンドを混在させた例を次に示します。

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

に`wsl.exe`渡されるコマンドは、変更せずに wsl プロセスに転送されます。  ファイルパスは WSL 形式で指定する必要があります。

パスを使用した例:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL から Windows ツールを実行する

WSL は、を使用して`[binary name].exe`、wsl コマンドラインから直接 Windows バイナリを呼び出すことができます。  たとえば、`notepad.exe` のようにします。  Windows の実行可能ファイルの実行を容易にするために、windows `$PATH`のパスは、Linux では、[作成者] の更新プログラムに含まれています。

この方法で実行されるアプリケーションには、次のプロパティがあります。

1. 作業ディレクトリを WSL コマンドプロンプトとして保持します (ほとんどの場合、例外については後述します)。
1. WSL プロセスと同じ権限が与えられている。
1. をアクティブな Windows ユーザーとして実行します。
1. コマンドプロンプトから直接実行されたかのように、Windows タスクマネージャーに表示されます。

例:

``` BASH
$ notepad.exe
```

WSL で実行される Windows 実行可能ファイルは、ネイティブの Linux 実行可能ファイルと同様に処理されます (パイプ、リダイレクト、バックグラウンド処理が想定どおりに動作します)。

パイプを使用した例:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

混合ウィンドウと WSL コマンドを使用する例:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows バイナリには、ファイル拡張子が含まれている必要があります。また、ファイルの大文字と小文字が一致している必要があります  バッチスクリプトを含む非実行可能ファイル。  コマンドを使用し`dir`て、の`cmd.exe /C`ような CMD ネイティブコマンドを実行できます。

例 :

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

パラメーターは、変更されていない Windows バイナリに渡されます。

例として、で`C:\temp\foo.txt` `notepad.exe`は次のコマンドが開きます。

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Wsl の Windows アプリケーションを使用して、 `/mnt/<x>`volfs (下にないファイル) にあるファイルを変更することはサポートされていません。

既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻されます。

例を次に示します。が最初に`C:\temp`起動され、現在の wsl ディレクトリがユーザーのホームに変更されます。 `wsl.exe`  ユーザー `notepad.exe`のホームディレクトリからが呼び出されると、wsl は notepad.exe 作業`C:\temp`ディレクトリとして自動的にに戻ります。

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows と WSL の間で環境変数を共有する

> Windows Insider ビルド17063以降で使用できます。

17063より前では、wsl がアクセスできる Windows 環境変数`PATH`のみが使用されていました (したがって、wsl の下から Win32 実行可能ファイルを起動できます)。

17063以降、wsl および windows share `WSLENV`は、wsl で実行される Windows および Linux ディストリビューションをブリッジするために作成された特殊な環境変数です。

次の`WSLENV`プロパティ:

* これは共有されています。Windows と WSL の両方の環境に存在します。
* これは、Windows と WSL の間で共有する環境変数の一覧です。
* 環境変数の書式を設定して、Windows および WSL で適切に動作させることができます。

で`WSLENV`は、環境変数の変換方法に影響を与える4つのフラグが用意されています。

`WSLENV`示す

* `/p`-WSL/Linux スタイルパスと Win32 パス間のパスを変換します。
* `/l`-環境変数がパスのリストであることを示します。
* `/u`-Win32 から WSL を実行する場合にのみ、この環境変数を含める必要があることを示します。
* `/w`-WSL から Win32 を実行する場合にのみ、この環境変数を含める必要があることを示します。

フラグは、必要に応じて組み合わせることができます。

## <a name="disable-interop"></a>相互運用を無効にする

ユーザーは、次のコマンドを root として実行することで、1つの WSL セッションに対して Windows バイナリを実行する機能を無効にすることができます。

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Windows バイナリを再び有効にするには、すべての WSL セッションを終了し、bash を再実行するか、ルートとして次のコマンドを実行します。

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

相互運用機能の無効化は、WSL セッション間では保持されません。新しいセッションが開始されると、相互運用が再び有効になります。

## <a name="creators-update-and-anniversary-update"></a>作成者の更新プログラムと記念日の更新

相互運用機能の更新は、より新しい相互運用エクスペリエンスに似ていますが、いくつかの大きな違いがあります。

要約すると、以下のようになります。

* `bash.exe`は非推奨とされ`wsl.exe`、に置き換えられました。
* `-c`で`wsl.exe`は、単一のコマンドを実行するオプションは必要ありません。
* Windows パスは WSL に含まれています`$PATH`

相互運用を無効にするプロセスは変更されていません。

### <a name="invoking-wsl-from-the-windows-command-line"></a>Windows コマンドラインからの WSL の呼び出し

Linux バイナリは、Windows コマンドプロンプトまたは PowerShell から呼び出すことができます。  この方法で呼び出されるバイナリには、次のプロパティがあります。

1. CMD または PowerShell プロンプトと同じ作業ディレクトリを使用します。
1. WSL の既定のユーザーとして実行します。
1. 呼び出しプロセスとターミナルと同じ Windows 管理者権限を持っている。

例:

```console
C:\temp> bash -c "ls -la"
```

この方法で呼び出された Linux コマンドは、他の Windows アプリケーションと同様に処理されます。  入力、パイプ、ファイルリダイレクトなどが想定どおりに動作します。

例 :

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

に`bash -c`渡される wsl コマンドは、変更せずに wsl プロセスに転送されます。  ファイルパスは WSL 形式で指定する必要があり、関連する文字をエスケープするために注意する必要があります。 例:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>WSL からの Windows バイナリの呼び出し

Windows Subsystem for Linux は、WSL コマンドラインから直接 Windows バイナリを呼び出すことができます。  この方法で実行されるアプリケーションには、次のプロパティがあります。

1. 以下で説明するシナリオを除き、作業ディレクトリは WSL コマンドプロンプトとして保持してください。
1. `bash.exe`プロセスと同じ権限を持っている。 
1. をアクティブな Windows ユーザーとして実行します。
1. コマンドプロンプトから直接実行されたかのように、Windows タスクマネージャーに表示されます。

例:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

WSL では、これらの実行可能ファイルはネイティブの Linux 実行可能ファイルと同様に処理されます。  これは、Linux パスにディレクトリを追加し、コマンド間でパイプを使用して正常に動作することを意味します。  例 :

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows バイナリには、ファイル拡張子が含まれている必要があります。ファイルの大文字と小文字の区別、および実行可能ファイルです。  バッチスクリプトやコマンド`dir`などを含む非実行可能ファイルは、コマンドを使用して`/mnt/c/Windows/System32/cmd.exe /C`実行できます。

例 :

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

パラメーターは、変更されていない Windows バイナリに渡されます。  

例として、で`C:\temp\foo.txt` `notepad.exe`は次のコマンドが開きます。

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Windows アプリケーションを使用して、volfs ( `/mnt/<x>`下にないファイル) にあるファイルを変更することはできません。  既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻されます。

例を次に示します。が最初に`C:\temp`起動され、現在の wsl ディレクトリがユーザーのホームに変更されます。 `bash.exe`  ユーザー `notepad.exe`のホームディレクトリからが呼び出されると、wsl は notepad.exe 作業`C:\temp`ディレクトリとして自動的にに戻ります。

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
