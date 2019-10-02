---
title: Linux との Windows の相互運用性
description: Windows Subsystem for Linux で実行されている Linux ディストリビューションとの Windows の相互運用性について説明します。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122731"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows との Windows Subsystem for Linux の相互運用性

> **Fall Creators Update 向けに更新されました。**  
Creators Update または Anniversary Update を実行している場合は、[Creators/Anniversary Update に関するセクション](interop.md#creators-update-and-anniversary-update)に移動してください。

Windows Subsystem for Linux (WSL) は、Windows と Linux 間の統合を継続的に向上させています。  以下が可能です。

1. Linux コンソールから Windows バイナリを起動します。
1. Windows コンソールから Linux バイナリを起動します。
1. **Windows Insiders Build 17063 以降**では、Linux と Windows の間で環境変数を共有します。

これにより、Windows と WSL の間でシームレスなエクスペリエンスが提供されます。  技術的な詳細については、[WSL のブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)をご覧ください。

## <a name="run-linux-tools-from-a-windows-command-line"></a>Windows コマンド ラインからの Linux ツールの実行

`wsl.exe <command>` を使用して、Windows コマンド プロンプト (CMD または PowerShell) から Linux バイナリを実行します。

この方法で起動されるバイナリには、次の特性があります。

1. 現在の CMD または PowerShell プロンプトと同じ作業ディレクトリを使用します。
1. WSL の既定のユーザーとして実行されます。
1. 呼び出し元のプロセスおよびターミナルと同じ Windows 管理者権限を持ちます。

次に、例を示します。

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

`wsl.exe` の後の Linux コマンドは、WSL での任意のコマンド実行と同様に処理されます。  sudo、パイプ処理、ファイル リダイレクトなどが機能します。

sudo を使用した例:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

WSL コマンドと Windows コマンドを組み合わせた例:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

`wsl.exe` に渡されるコマンドは、変更なしで WSL プロセスに転送されます。  ファイル パスは WSL 形式で指定する必要があります。

パスを指定した例:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL からの Windows ツールの実行

WSL では、`[binary name].exe` を使用して、WSL コマンド ラインから Windows バイナリを直接起動することができます。  たとえば、`notepad.exe` と記述します。  Windows 実行可能ファイルの実行を容易にするために、Fall Creators Update では Windows のパスは Linux `$PATH` に含まれています。

この方法で実行されるアプリケーションには、次の特性があります。

1. ほとんどの場合、作業ディレクトリを WSL コマンド プロンプトとして保持します (例外については後述します)。
1. WSL プロセスと同じアクセス許可権限が与えられています。
1. アクティブな Windows ユーザーとして実行されます。
1. CMD プロンプトから直接実行されたかのように、Windows タスク マネージャーに表示されます。

以下に例を示します。

``` BASH
$ notepad.exe
```

WSL で実行される Windows 実行可能ファイルは、ネイティブの Linux 実行可能ファイルと同様に処理されます。パイプ処理、リダイレクト、さらにバックグラウンド処理も想定どおりに機能します。

パイプを使用した例:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Windows コマンドと WSL コマンドの組み合わせを使用した例:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows バイナリは、ファイル拡張子を含み、ファイルの大文字と小文字が一致し、実行可能である必要があります。  非実行可能ファイルにはバッチ スクリプトが含まれます。  `dir` などの CMD ネイティブ コマンドは、`cmd.exe /C` コマンドを使用して実行できます。

例:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

パラメーターは、変更されずに Windows バイナリに渡されます。

たとえば、次のコマンドによって `notepad.exe` で `C:\temp\foo.txt` が開きます。

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

WSL の Windows アプリケーションを使用して、VolFs にあるファイル (`/mnt/<x>` の下にないファイル) を変更することはサポートされていません。

既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻ります。

たとえば、`wsl.exe` が最初に `C:\temp` から起動され、現在の WSL ディレクトリがユーザーのホームに変更されているとします。  `notepad.exe` がユーザーのホーム ディレクトリからが呼び出されると、WSL は notepad.exe の作業ディレクトリとして `C:\temp` に自動的に戻ります。

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows と WSL の間での環境変数の共有

> Windows Insider Build 17063 以降で使用可能です。

17063 より前では、WSL がアクセスできる唯一の Windows 環境変数は `PATH` でした (そのため、WSL で Win32 実行可能ファイルを起動できました)。

17063 以降、WSL と Windows は `WSLENV` を共有します。これは、WSL で実行される Windows と Linux のディストリビューションをつなぐために作成された特殊な環境変数です。

`WSLENV` の特性:

* 共有され、Windows と WSL の両方の環境に存在します。
* Windows と WSL の間で共有する環境変数の一覧です。
* Windows と WSL で適切に機能するように環境変数をフォーマットできます。

環境変数の変換方法に影響する、`WSLENV` で利用可能な 4 つのフラグがあります。

`WSLENV` のフラグ:

* `/p` - WSL/Linux スタイル パスと Win32 パスの間でパスを変換します。
* `/l` - 環境変数がパスのリストであることを示します。
* `/u` - Win32 から WSL を実行する場合にのみ、この環境変数を含める必要があることを示します。
* `/w` - WSL から Win32 を実行する場合にのみ、この環境変数を含める必要があることを示します。

フラグは、必要に応じて組み合わせることができます。

## <a name="disable-interop"></a>相互運用の無効化

ユーザーは、ルートとして次のコマンドを実行することで、1 つの WSL セッションに対して Windows バイナリを実行する機能を無効にできます。

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Windows バイナリを再び有効にするには、すべての WSL セッションを終了して bash.exe を再実行するか、ルートとして次のコマンドを実行します。

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

相互運用の無効化は、WSL セッション間で保持されません。新しいセッションが開始されると、相互運用は再び有効になります。

## <a name="creators-update-and-anniversary-update"></a>Creators Update と Anniversary Update

Fall Creators Update 以前の相互運用エクスペリエンスは、より新しい相互運用エクスペリエンスに似ていますが、いくつかの大きな違いがあります。

要約すると、以下のようになります。

* `bash.exe` は非推奨となり、`wsl.exe` に置き換えられました。
* 1 つのコマンドを実行する場合の `-c` オプションは、`wsl.exe` で必要ありません。
* Windows パスは WSL `$PATH` に含まれています。

相互運用を無効にするプロセスは変更されていません。

### <a name="invoking-wsl-from-the-windows-command-line"></a>Windows コマンド ラインからの WSL の起動

Linux バイナリは、Windows コマンド プロンプトまたは PowerShell から起動できます。  この方法で起動されるバイナリには、次の特性があります。

1. CMD または PowerShell プロンプトと同じ作業ディレクトリを使用します。
1. WSL の既定のユーザーとして実行されます。
1. 呼び出し元のプロセスおよびターミナルと同じ Windows 管理者権限を持ちます。

以下に例を示します。

```console
C:\temp> bash -c "ls -la"
```

この方法で呼び出された Linux コマンドは、他の Windows アプリケーションと同様に処理されます。  sudo、パイプ処理、ファイル リダイレクトなどが想定どおりに機能します。

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

`bash -c` に渡される WSL コマンドは、変更なしで WSL プロセスに転送されます。  ファイル パスは WSL 形式で指定する必要があり、関連文字をエスケープするように注意する必要があります。 以下に例を示します。

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>WSL からの Windows バイナリの起動

Windows Subsystem for Linux では、WSL コマンド ラインから Windows バイナリを直接起動することができます。  この方法で実行されるアプリケーションには、次の特性があります。

1. 作業ディレクトリを WSL コマンド プロンプトとして保持します。ただし、以降で説明するシナリオを除きます。
1. `bash.exe` プロセスと同じアクセス許可権限を持ちます。 
1. アクティブな Windows ユーザーとして実行されます。
1. CMD プロンプトから直接実行されたかのように、Windows タスク マネージャーに表示されます。

以下に例を示します。

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

WSL では、これらの実行可能ファイルはネイティブの Linux 実行可能ファイルと同様に処理されます。  これは、Linux パスへのディレクトリの追加や、コマンド間でのパイプ処理が想定どおりに機能することを意味します。  例:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows バイナリは、ファイル拡張子を含み、ファイルの大文字と小文字が一致し、実行可能である必要があります。  バッチ スクリプトや `dir` などのコマンドを含む非実行可能ファイルは、`/mnt/c/Windows/System32/cmd.exe /C` コマンドを使用して実行できます。

例:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

パラメーターは、変更されずに Windows バイナリに渡されます。  

たとえば、次のコマンドによって `notepad.exe` で `C:\temp\foo.txt` が開きます。

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Windows アプリケーションを使用して、VolFs にあるファイル (`/mnt/<x>` の下にないファイル) を変更することはサポートされていません。  既定では、WSL は Windows バイナリの作業ディレクトリを現在の WSL ディレクトリとして保持しようとしますが、作業ディレクトリが VolFs にある場合はインスタンス作成ディレクトリに戻ります。

たとえば、`bash.exe` が最初に `C:\temp` から起動され、現在の WSL ディレクトリがユーザーのホームに変更されているとします。  `notepad.exe` がユーザーのホーム ディレクトリからが呼び出されると、WSL は notepad.exe の作業ディレクトリとして `C:\temp` に自動的に戻ります。

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
