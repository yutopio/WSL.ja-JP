---
title: Linux ユーザーアカウントとアクセス許可
description: Windows Subsystem for Linux を使用したユーザーアカウントとアクセス許可の管理のリファレンスです。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、ユーザーアカウント
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122682"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のユーザーアカウントとアクセス許可

Linux ユーザーの作成は、WSL で新しい Linux ディストリビューションを設定するための最初の手順です。  作成した最初のユーザーアカウントは、次のいくつかの特殊な属性で自動的に構成されます。

1. これは既定のユーザーであり、起動時に自動的にサインインします。
1. 既定では、Linux 管理者 (sudo グループのメンバー) です。

Windows Subsystem for Linux で実行されている各 Linux ディストリビューションには、独自の Linux ユーザーアカウントとパスワードがあります。  ディストリビューションの追加、再インストール、またはリセットを行うたびに、Linux ユーザーアカウントを構成する必要があります。  Linux ユーザーアカウントは、ディストリビューションごとに独立しているわけではなく、Windows ユーザーアカウントにも依存しません。

## <a name="resetting-your-linux-password"></a>Linux パスワードをリセットしています

Linux ユーザーアカウントへのアクセス権があり、現在のパスワードを把握している場合は、そのディストリビューション`passwd`の linux パスワードリセットツールを使用して変更してください。

このオプションが選択されていない場合は、ディストリビューションによっては、既定のユーザーをリセットすることによってパスワードをリセットできる可能性があります。

WSL は、WSL を開始するときに自動的にログインするユーザーアカウントを識別するための既定のユーザータグを提供します。  多くのディストリビューションには、既定のユーザーを root に設定するコマンドや、パスワードが設定されていないルートユーザーを設定するコマンドが含まれているため、既定のユーザーを root に変更すると、パスワードのリセットなどの便利なツールになります。

### <a name="for-creators-update-and-earlier"></a>作成者の更新プログラム (以前のバージョンの場合)
Windows 10 の作成者更新プログラムまたはそれ以前のバージョンを実行している場合は、次のコマンドを実行して既定の Bash ユーザーを変更できます。

1. 既定のユーザーを次`root`のように変更します。

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 今すぐ`bash.exe`実行する`root`ログイン:

    ```console
    C:\> bash.exe
    ```

1. ディストリビューションのパスワードコマンドを使用してパスワードをリセットし、Linux コンソールを閉じます。

    ```BASH
    $ passwd username
    $ exit
    ```

1. Windows CMD で、既定のユーザーをリセットし、通常の Linux ユーザーアカウントに戻します。

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>秋に更新プログラムをインストールする場合
特定のディストリビューションで使用できるコマンドを確認するには`[distro.exe] /?`、を実行します。
    
たとえば、Ubuntu がインストールされているとします。

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

Ubuntu を使用したステップバイステップの手順:

1. CMD を開く
1. 既定の Linux ユーザーを次`root`のように設定します。

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Linux ディストリビューション (`ubuntu`) を起動します。  次のように自動的`root`にログインします。

1. 次の`passwd`コマンドを使用してパスワードをリセットします。

    ```BASH
    $ passwd username
    ```

1. Windows CMD で、既定のユーザーをリセットして、通常の Linux ユーザーアカウントに戻します。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>アクセス許可

WSL のアクセス許可に関しては、次の2つの重要な概念を念頭に置く必要があります。

1. Windows アクセス許可モデルは、Windows リソースに対するプロセスの権限を制御します。
2. Linux アクセス許可モデルは、Linux リソースに対するプロセスの権限を制御します。

WSL で Linux を実行すると、Linux はそれを起動するプロセスと同じ Windows アクセス許可を持ちます。 Linux は、次の2つのアクセス許可レベルのいずれかで起動できます。

* 標準 (昇格されていない):Linux は、ログインしているユーザーのアクセス許可で実行されます。
* 昇格された管理者:管理者特権での Windows のアクセス許可を使用して Linux を実行する

> 昇格されたプロセスはシステム全体の設定とシステム全体または保護されたデータにアクセスしたり、変更したりできます。そのため、Windows または Linux のアプリケーション/ツールであるかどうかにかかわらず、管理者特権のプロセスを起動しない**よう**にしてください。シェル!

上記の Windows アクセス許可は、Linux インスタンス内のアクセス許可とは無関係です。Linux の "Root 特権" は、Linux 環境 & ファイルシステム内のユーザーの権限にのみ影響します。付与された Windows 特権には影響しません。 したがって、linux プロセスをルートとして実行する`sudo`と (例: via)、linux 環境内のプロセス管理者権限のみが付与されます。

**例:**     
管理者特権のない bash セッションで " `cd /mnt/c/Users/Administrator`アクセス許可が拒否されました" というエラーが表示される場合、Windows 管理者特権を持つ bash セッションがアクセスする可能性があります。

Linux では、 `sudo cd /mnt/c/Users/Administrator` windows のアクセス許可は windows によって管理されているため、「」と入力すると、管理者のディレクトリへのアクセス権が付与されません。

Linux アクセス許可モデルは、linux 環境内で、ユーザーが現在の Linux ユーザーに基づいてアクセス許可を持っている場合に重要です。

**例:**  
Sudo グループ内のユーザーが実行`sudo apt update`される可能性があります。
