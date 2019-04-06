---
title: Linux と Windows の相互運用
description: Linux 用 Windows サブシステムで実行されている Linux ディストリビューションでは、Windows の相互運用性をについて説明します。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063250"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows と Linux の相互運用性用 Windows サブシステム

> **For Fall Creators Update が更新されます。**  
Creators Update または Anniversary Update を実行している場合にジャンプ、 [Creators/Anniversary Update セクション](interop.md#creators-update-and-anniversary-update)します。

Windows Subsystem for Linux (WSL) は、Windows と Linux 間の統合を継続的に向上です。  可能な代替手段としては以下の方法があります。

1. Linux コンソールから Windows バイナリを呼び出します。
1. Windows コンソールから Linux 向けのバイナリを呼び出します。
1. **Windows Insider のビルド 17063 +** Linux と Windows 環境変数を共有します。

これは、Windows と WSL の間のシームレスなエクスペリエンスを提供します。  技術的な詳細は、 [WSL ブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)します。

## <a name="run-linux-tools-from-a-windows-command-line"></a>Windows コマンドラインから Linux ツールを実行します。

Windows コマンド プロンプト (CMD または PowerShell) を使用して、Linux のバイナリを実行する`wsl.exe <command>`します。

バイナリをこの方法で呼び出されます。

1. 現在の CMD または PowerShell プロンプトとして同じ作業ディレクトリを使用します。
1. WSL の既定のユーザーとして実行します。
1. 呼び出し元のプロセスとターミナルとして同じ Windows 管理者権限を持ちます。

次に、例を示します。

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Linux コマンド次`wsl.exe`WSL で実行する任意のコマンドのように処理されます。  Sudo、パイプ、およびファイルのリダイレクトなどの機能は、次の動作します。

Sudo の使用例:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

WSL と Windows のコマンドを混在させる例:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

渡されるコマンド`wsl.exe`変更しなくても、WSL プロセスに転送されます。  WSL 形式でファイル パスを指定する必要があります。

パスの例:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL から Windows ツールを実行します。

WSL が使用して、WSL コマンドラインから直接 Windows バイナリを呼び出すことができます`[binary name].exe`します。  たとえば、`notepad.exe` と記述します。  Linux の Windows 実行可能ファイルを簡単に実行させるには、Windows のパスが含まれている`$PATH`Fall Creators Update でします。

この方法で実行するアプリケーションでは、次のプロパティがあります。

1. WSL のコマンド プロンプトとして作業ディレクトリを保持 (ほとんどの場合--例外について以下に説明)。
1. WSL プロセスと同じアクセス許可権限を持っています。
1. アクティブな Windows ユーザーとして実行します。
1. Windows タスク マネージャーに表示される場合に、コマンド プロンプトから直接実行します。

以下に例を示します。

``` BASH
$ notepad.exe
```

WSL で実行、Windows 実行可能ファイルは、ネイティブの Linux 実行可能ファイル: リダイレクトのパイプとも想定どおりに作業するバック グラウンド処理を同様に処理されます。

パイプを使用する例:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Windows と WSL の混在のコマンドを使用する例:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows バイナリでは、ファイル拡張子を含める、ファイルの場合も、一致、および実行可能する必要があります。  などの非-実行可能ファイルは、スクリプトをバッチ処理します。  などのネイティブ コマンドを CMD`dir`で実行できる`cmd.exe /C`コマンド。

例:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

パラメーターは、変更されていない Windows バイナリに渡されます。

次のコマンドを開く例として、`C:\temp\foo.txt`で`notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

VolFs 上にあるファイルの変更 (ファイルのない`/mnt/<x>`) WSL でのアプリケーションはサポートされていません、Windows とします。

既定では、WSL バイナリ WSL の現在のディレクトリとして、Windows の作業ディレクトリを保持しようとするは代替インスタンス作成のディレクトリで VolFs 作業ディレクトリがある場合。

たとえば;`wsl.exe`が最初に起動される`C:\temp`され、現在の WSL ディレクトリは、ユーザーのホームに変更されます。  ときに`notepad.exe`と呼ばれますが、ユーザーのホーム ディレクトリから WSL に自動的に戻ります`C:\temp`notepad.exe の作業ディレクトリとして。

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows と WSL の間の環境変数を共有します。

> Windows Insider ビルド 17063 以降で使用できます。

WSL にアクセスできる Windows 環境変数のみが 17063、前に`PATH`(したがって、WSL 下から Win32 実行可能ファイルを起動する可能性があります)。

17063 以降、WSL と Windows 共有`WSLENV`、特殊な環境変数が WSL で実行されている Windows と Linux のディストリビューションをブリッジするために作成します。

プロパティの`WSLENV`:

* 共有します。これは、Windows と WSL の両方の環境に存在します。
* これは、Windows と WSL 間で共有する環境変数の一覧です。
* Windows と WSL で問題なく動作する環境変数を書式設定できます。

使用できる 4 つのフラグがあります`WSLENV`その環境変数が変換される方法に影響を与える。

`WSLENV` フラグ:

* `/p` -WSL/Linux 形式のパスと Win32 のパスの間のパスを変換します。
* `/l` -環境変数がパスの一覧を示します。
* `/u` -Win32 から WSL を実行する場合にこの環境変数を含めるだけあることを示します。
* `/w` -WSL から Win32 を実行する場合にこの環境変数を含めるだけあることを示します。

必要に応じて、フラグを組み合わせることができます。

## <a name="disable-interop"></a>相互運用機能を無効にします。

ユーザーには、ルートとして、次のコマンドを実行して、単一の WSL セッションの Windows バイナリを実行する機能が無効にすることがあります。

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Windows を再度有効にするには、バイナリ WSL のすべてのセッションを終了し、bash.exe を再実行またはルートとして次のコマンドを実行します。

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

WSL セッション間で相互運用機能を無効化は永続化されません--新しいセッションを起動するときに、相互運用機能を再度有効になります。

## <a name="creators-update-and-anniversary-update"></a>Creators Update と Anniversary Update

相互運用エクスペリエンスの事前 Fall Creators Update は、相互運用機能の最新のエクスペリエンスに似ていますが、中には、handfull の主な相違点があります。

要約。

* `bash.exe` 非推奨とされ、置き換え`wsl.exe`します。
* `-c` オプションでは必要ありません、1 つのコマンドを実行しているを`wsl.exe`します。
* Windows のパスが、WSL に含まれる `$PATH`

相互運用機能を無効にするためのプロセスは変更されません。

### <a name="invoking-wsl-from-the-windows-command-line"></a>WSL Windows コマンドラインからの呼び出し

Linux のバイナリは、Windows コマンド プロンプトから、または PowerShell から起動できます。  この方法で呼び出されたバイナリの次のプロパティがあります。

1. CMD または PowerShell プロンプトとして同じ作業ディレクトリを使用します。
1. WSL の既定のユーザーとして実行します。
1. 呼び出し元のプロセスとターミナルとして同じ Windows 管理者権限を持ちます。

以下に例を示します。

```console
C:\temp> bash -c "ls -la"
```

この方法で呼び出す Linux コマンドは、その他の Windows アプリケーションのように処理されます。  入力、パイプ、およびファイルのリダイレクトなどは、期待どおりに動作します。

例:

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

渡される WSL コマンド`bash -c`変更しなくても、WSL プロセスに転送されます。  WSL 形式でファイル パスを指定する必要があり、関連する文字をエスケープする注意おく必要があります。 以下に例を示します。

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>WSL から呼び出し元の Windows バイナリ

Windows Subsystem for Linux は、WSL コマンドラインから直接 Windows バイナリを呼び出すことができます。  この方法で実行するアプリケーションでは、次のプロパティがあります。

1. 以下で説明するシナリオでは除く WSL コマンド プロンプトとして作業ディレクトリを保持します。
1. 同じアクセス許可権限を持ち、`bash.exe`プロセス。 
1. アクティブな Windows ユーザーとして実行します。
1. Windows タスク マネージャーに表示される場合に、コマンド プロンプトから直接実行します。

以下に例を示します。

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

WSL では、この実行可能ファイルはネイティブの Linux の実行可能ファイルのような処理されます。  これは、Linux パスにディレクトリを追加して、期待どおりのコマンド間でパイプを意味します。  例:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows バイナリは、ファイル拡張子を含めるし、ファイルの場合も、一致、実行可能します。  などの非-実行可能ファイルのバッチのスクリプトおよびコマンドのような`dir`で実行できる`/mnt/c/Windows/System32/cmd.exe /C`コマンド。

例:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

パラメーターは、変更されていない Windows バイナリに渡されます。  

次のコマンドを開く例として、`C:\temp\foo.txt`で`notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

VolFs 上にあるファイルの変更 (ファイルのない`/mnt/<x>`)、Windows のアプリケーションはサポートされていません。  既定では、WSL バイナリ WSL の現在のディレクトリとして、Windows の作業ディレクトリを保持しようは代替インスタンス作成のディレクトリの作業ディレクトリが VolFs にある場合。

たとえば;`bash.exe`が最初に起動される`C:\temp`され、現在の WSL ディレクトリは、ユーザーのホームに変更されます。  ときに`notepad.exe`と呼ばれますが、ユーザーのホーム ディレクトリから WSL に自動的に戻ります`C:\temp`notepad.exe の作業ディレクトリとして。

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
