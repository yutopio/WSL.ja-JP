---
title: Linux ユーザー アカウントとアクセス許可
description: Windows Subsystem for Linux を使用したユーザー アカウントとアクセス許可の管理のリファレンス。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, ユーザー アカウント
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122682"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のユーザー アカウントとアクセス許可

Linux ユーザーの作成は、WSL で新しい Linux ディストリビューションを設定する際の最初の手順です。  作成した最初のユーザー アカウントは、次のいくつかの特殊な属性で自動的に構成されます。

1. これは既定のユーザーであり、起動時に自動的にサインインします。
1. 既定では、Linux 管理者 (sudo グループのメンバー) です。

Windows Subsystem for Linux で実行されている各 Linux ディストリビューションには、独自の Linux ユーザー アカウントとパスワードがあります。  ディストリビューションの追加、再インストール、または再設定を行うたびに、Linux ユーザー アカウントを構成する必要があります。  Linux ユーザー アカウントは、ディストリビューションごとに独立しているだけではなく、Windows ユーザー アカウントにも依存しません。

## <a name="resetting-your-linux-password"></a>Linux パスワードの再設定

Linux ユーザー アカウントへのアクセス権があり、現在のパスワードを知っている場合は、そのディストリビューションの Linux パスワード再設定ツール (最も一般的なのは `passwd`) を使用して変更してください。

これを実行できない場合、ディストリビューションによっては、既定のユーザーを再設定することでパスワードを再設定できることがあります。

WSL では、WSL を開始するときに自動的にログインするユーザー アカウントを識別するための既定のユーザー タグが用意されています。  多くのディストリビューションには、既定のユーザーをルートに設定するコマンドや、パスワードが設定されていないルート ユーザーを設定するコマンドが含まれているため、既定のユーザーのルートへの変更は、パスワードの再設定などのための便利なツールになります。

### <a name="for-creators-update-and-earlier"></a>Creators Update 以前の場合
Windows 10 Creators Update 以前を実行している場合は、次のコマンドを実行して既定の Bash ユーザーを変更できます。

1. 既定のユーザーを `root` に変更します。

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. `bash.exe` を実行して、今度は `root` としてログインします。

    ```console
    C:\> bash.exe
    ```

1. ディストリビューションのパスワード コマンドを使用してパスワードを再設定し、Linux コンソールを閉じます。

    ```BASH
    $ passwd username
    $ exit
    ```

1. Windows CMD で、既定のユーザーを通常の Linux ユーザー アカウントに再設定して戻します。

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update 以降の場合
特定のディストリビューションで使用できるコマンドを確認するには、`[distro.exe] /?` を実行します。
    
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

Ubuntu を使用したステップ バイ ステップの手順:

1. CMD を開きます。
1. 既定の Linux ユーザーを `root` に設定します。

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Linux ディストリビューション (`ubuntu`) を起動します。  `root` として自動的にログインします。

1. `passwd` コマンドを使用してパスワードを再設定します。

    ```BASH
    $ passwd username
    ```

1. Windows CMD で、既定のユーザーを通常の Linux ユーザー アカウントに再設定して戻します。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>アクセス許可

WSL のアクセス許可に関しては、留意すべき重要な概念が 2 つあります。

1. Windows アクセス許可モデルは、Windows リソースに対するプロセスの権限を管理します
2. Linux アクセス許可モデルは、Linux リソースに対するプロセスの権限を制御します

WSL で Linux を実行すると、Linux はそれを起動するプロセスと同じ Windows アクセス許可を持ちます。 Linux は、次の 2 つのアクセス許可レベルのいずれかで起動できます。

* 通常 (管理者特権でない):Linux は、ログインしているユーザーのアクセス許可を使用して実行されます
* 管理者特権/管理者:Linux は、管理者特権/管理者の Windows アクセス許可を使用して実行されます

> 昇格されたプロセスはシステム全体の設定やシステム全体にわたるデータまたは保護されているデータへのアクセスや変更が可能であり、結果として破損させる可能性があるため、Windows と Linux のどちらのアプリケーション/ツール/シェルであるかに関係なく、どうしても必要でない限りは昇格されたプロセスを起動**しないようにしてください**。

上記の Windows アクセス許可は、Linux インスタンス内のアクセス許可とは無関係です。Linux の "ルート権限" は、Linux 環境およびファイル システム内のユーザーの権限にのみ影響し、付与されている Windows 特権には影響しません。 したがって、(たとえば、`sudo` を使用して) Linux プロセスをルートとして実行すると、Linux 環境内でそのプロセス管理者権限のみが付与されます。

**例:**     
Windows 管理特権がある Bash セッションでは `cd /mnt/c/Users/Administrator` にアクセスできる一方で、管理特権のない Bash セッションでは "アクセス許可が拒否されました" というエラーが表示されます。

Windows 内のアクセス許可は Windows によって管理されているため、Linux では、「`sudo cd /mnt/c/Users/Administrator`」と入力しても、管理者のディレクトリへのアクセス権が付与されません。

Linux アクセス許可モデルは、Linux 環境内で、ユーザーが現在の Linux ユーザーに基づいたアクセス許可を持っている場合に重要です。

**例:**  
sudo グループ内のユーザーは `sudo apt update` を実行できます。
