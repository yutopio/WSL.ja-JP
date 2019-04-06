---
title: Linux ユーザー アカウントとアクセス許可
description: Windows Subsystem for Linux でのユーザー アカウントとアクセス許可の管理の参照。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、ユーザー アカウント用の windows サブシステム
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063600"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>ユーザー アカウントと Linux 用 Windows サブシステムのアクセス許可

WSL での新しい Linux ディストリビューションを設定する最初の手順は、Linux ユーザーを作成します。  作成する最初のユーザー アカウントは自動的に、いくつかの特別な属性を持つ構成します。

1. 既定のユーザーが--にサインインすると自動的に起動します。
1. 既定では、Linux 管理者 (sudo グループのメンバー) になります。

Linux 用 Windows サブシステムで実行されている各 Linux ディストリビューションでは、独自の Linux ユーザー アカウントとパスワードを持ちます。  Linux ユーザー アカウントを構成するには、いつでも、ディストリビューションを追加、再インストール、またはリセットする必要があります。  Linux ユーザー アカウントには、ディストリビューションごとに独立した、Windows ユーザー アカウントから独立していることもできます。

## <a name="resetting-your-linux-password"></a>Linux パスワードのリセット

Linux ユーザー アカウントにアクセスして変更して、現在のパスワードを知っている Linux を使用してパスワードのリセット ツールである可能性が最も高い--そのディストリビューションの`passwd`します。

場合は、オプションではなく、ディストリビューションによっては、既定のユーザーをリセットすることでパスワードをリセットすることができます。

WSL では、ユーザー アカウントを自動的に識別するために、既定のユーザー タグは、WSL を開始するときログを提供します。  多くのディストリビューションには、ルートともルート ユーザーにパスワードが設定されていない既定のユーザーを設定するためのコマンドが含まれている、ルートに既定のユーザーを変更するは、パスワードのリセットなどの便利なツールです。

### <a name="for-creators-update-and-earlier"></a>Creators Update 以降
実行している場合は、Windows 10 Creators update または以前では、次のコマンドを実行して既定の Bash のユーザーを変更できます。

1. 既定のユーザーを変更する`root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 実行`bash.exe`として現在のログインに`root`:

    ```console
    C:\> bash.exe
    ```

1. ディストリビューションのパスワードのコマンドを使用してパスワードをリセットし、Linux コンソールを閉じます。

    ```BASH
    $ passwd username
    $ exit
    ```

1. Windows コマンド プロンプトで、通常の Linux ユーザー アカウントに既定のユーザーをリセットします。

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update 以降
どのようなコマンドは、特定の配布の使用については、次のように実行します。`[distro.exe] /?`します。
    
たとえば、Ubuntu のインストール。

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

ステップ バイ ステップで Ubuntu を使用します。

1. 開いている CMD
1. 既定の Linux ユーザーを設定`root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Linux ディストリビューションを起動 (`ubuntu`)。  自動的には、ログインとして`root`:

1. 使用して、パスワードのリセット、`passwd`コマンド。

    ```BASH
    $ passwd username
    ```

1. Windows コマンド プロンプトで、通常の Linux ユーザー アカウントに既定のユーザーをリセットします。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>アクセス許可

WSL でのアクセスを許可する際に留意する 2 つの重要な概念があります。

1. Windows のアクセス許可モデルは、Windows リソースへのプロセスの権限を制御します。
2. Linux のアクセス許可モデルは、Linux リソースへのプロセスの権限を制御します。

WSL で Linux を実行するときに、Linux は、起動するプロセスと同じ Windows 権限があります。 Linux は、2 つのアクセス許可レベルのいずれかで起動できます。

* 標準 (非特権):ログイン ユーザーのアクセス許可を持つ Linux が実行されます。
* 管理者特権で/管理者:管理者特権で/管理者の Windows アクセス許可を持つ Linux が実行されます。

> 昇格するため、プロセスできます変更/損傷システム全体の設定と、データとファイルとフォルダー、保護されているアクセス/変更できます**避け**が絶対に - Windows いるかどうかにない限り、プロセスを管理者特権を起動するか、Linux アプリケーション/tools/シェルです。

上記の Windows アクセス許可は、Linux インスタンス内でアクセス許可に依存しません。Linux の「Root 特権」Linux 環境とファイルシステム内のユーザーの権限の影響のみ影響を与えるありませんに与えられている Windows 特権。 そのため、ルートとして Linux プロセスを実行している (経由など`sudo`) Linux 環境内で管理者権限を処理するのみを付与します。

**以下に例を示します。**    
管理者特権の Windows で Bash セッションがアクセスできる`cd /mnt/c/Users/Administrator`Bash セッションを管理者特権が「アクセス許可が拒否されました」エラーを表示せずにします。

Linux では、入力`sudo cd /mnt/c/Users/Administrator`Windows 内でアクセス許可が Windows によって管理されるため、管理者のディレクトリへのアクセスを付与されませんが。

Linux のアクセス許可モデルは、Linux 環境をユーザーが現在の Linux ユーザーに基づいて、アクセス許可を持っている内で重要です。

**以下に例を示します。**  
Sudo グループ内のユーザーが実行される可能性が`sudo apt update`します。
