---
title: Windows Subsystem for Linux のリリースノート
description: Windows Subsystem for Linux のリリースノートです。  毎週更新されました。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: d2d91db24c12fc674d695ccffc79eb5781a0721d
ms.sourcegitcommit: be00abbb170aa569e008b804f15949344b378999
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2019
ms.locfileid: "68501580"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のリリースノート


## <a name="build-18947"></a>ビルド18947
ビルド18947の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18947/)を参照してください。

### <a name="wsl"></a>WSL
* [WSL2]Localhost: port を使用して、WSL2 のリスニング tcp ソケットにホストからアクセスできるようにします
* [WSL2]インストール/変換エラーの修正と今後の問題を追跡するための追加の診断 [GH 4105] 
* [WSL2]Diagnosability WSL2 のネットワークの問題を改善する
* [WSL2]カーネルバージョンを4.19.55 に更新する
* [WSL2]Docker に必要な構成オプションを使用してカーネルを更新する [GH 4165]
* [WSL2]ライトウェイトユーティリティ VM に割り当てられた Cpu の数を、ホストと同じになるように増やします (以前はカーネル構成の CONFIG_NR_CPUS によって8個に制限されていました) [GH 4137]
* [WSL2]WSL2 ライトウェイト VM 用のスワップファイルを作成する
* [WSL2]Wsl $ \\ \\ディストリビューションを使用してユーザーのマウントを表示できるようにします (例 sshfs) [GH 4172]\\
* [WSL2]9p ファイルシステムのパフォーマンスの向上
* [WSL2]Vhd ACL が無制限に拡張されないようにする [GH 4126]
* [WSL2]Squashfs と xt_conntrack をサポートするようにカーネル構成を更新する [GH 4107, 4123]
* [WSL2]Interop の修正。 enabled/etc/wsl.conf オプション [GH 4140]
* [WSL2]ファイルシステムで EAs がサポートされていない場合は、ENOTSUP を返します。
* [WSL2]Wsl $ で\\CopyFile hang を\\修正します
* 既定の umask を0022に切り替え、/etc/wsl.conf にファイルシステムの umask 設定を追加します。
* シンボリックリンクを適切に解決するために wslpath を修正しました。これは19h1 で低下したました [GH 4078]
* WSL2 設定を調整\.するための% UserProfile% wslconfig ファイルの導入
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a>ビルド18917
ビルド18917の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)を参照してください。

### <a name="wsl"></a>WSL
* WSL 2 が利用可能になりました。 詳細については、[ブログ](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)を参照してください。
* シンボリックリンクを使用した Windows プロセスの起動が正常に機能しない回帰を修正する [GH 3999]
* Wsl--list--verbose, wsl--list--quiet, および wsl .exe--import--version オプションを wsl に追加します。
* Wsl--shutdown オプションを追加します。
* プラン 9:書き込み用のディレクトリを開くことを成功させる

## <a name="build-18890"></a>ビルド18890
ビルド18890の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)を参照してください。

### <a name="wsl"></a>WSL
* 非ブロッキングソケットリーク [GH 2913]
* ターミナルへの EOF 入力が後続の読み取りをブロックする可能性がある [GH 3421]
* Resolv.conf を参照するようにを更新する (GH 3928 で説明)
* Epoll delete コードでのデッドロック [GH 3922]
* --Import および– export の引数内のスペースを処理する [GH 3932]
* Mmap ファイルの拡張が正しく機能しない [GH 3939]
* ARM64 \\wsl $ アクセスが正常に動作しない問題を修正します
* Wsl のより適切な既定のアイコンを追加する

## <a name="build-18342"></a>ビルド18342
ビルド18342の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)を参照してください。

### <a name="wsl"></a>WSL
* Windows から WSL ディストリビューションの Linux ファイルにユーザーがアクセスできる機能が追加されました。 これらのファイルには、コマンドラインを使用してアクセスできます。また、ファイルエクスプローラーや VSCode などの Windows アプリもこれらのファイルと対話できます。 \\Wsl $ \\ \\ \\< distro_name > に移動してファイルにアクセスするか、wsl $ に移動して実行中のディストリビューションの一覧を表示します。\\
* CPU 情報タグを追加し、Cpus_allowed [リスト] の値を修正する [GH 2234]
* リーダー以外のスレッドからの exec のサポート [GH 3800]
* 構成の更新エラーを致命的でないものとして扱う [GH 3785]
* オフセットを正しく処理するように binfmt を更新する [GH 3768]
* プラン9のネットワークドライブのマッピングを有効にする [GH 3854]
* Windows > Linux および Linux をサポートする-bind マウント用の Windows パス変換 >
* 読み取り専用で開かれたファイルのマッピングの読み取り専用セクションを作成する

## <a name="build-18334"></a>ビルド18334
ビルド18334の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)を参照してください。

### <a name="wsl"></a>WSL
* Windows タイムゾーンを Linux タイムゾーンにマップする方法の設計 [GH 3747]
* メモリリークを修正し、新しい文字列変換関数を追加する [GH 3746]
* スレッドのない threadgroup の SIGCONT は、no op [GH 3741] 
* /Proc/self/fd にソケットと epoll ファイル記述子を正しく表示する

## <a name="build-18305"></a>ビルド18305
ビルド18305の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)を参照してください。

### <a name="wsl"></a>WSL
* pthreads プライマリスレッドが終了したときにファイルへのアクセスが失われる [GH 3589]
* TIOCSCTTY は、必要な場合を除き、"force" パラメーターを無視する必要があります [GH 3652]
* wsl コマンドラインの機能強化とインポート/エクスポート機能の追加。
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a>ビルド18277
ビルド18277の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)を参照してください。

### <a name="wsl"></a>WSL
* ビルド18272で導入された "そのようなインターフェイスがサポートされていません" というエラーを修正する [GH 3645]
* Umount syscall の MNT_FORCE フラグを無視する [GH 3605]
* WSL 相互運用機能を切り替えて、正式な Create擬似コンソール API を使用する
* FUTEX_WAIT の再起動時にタイムアウト値を保持しない

## <a name="build-18272"></a>ビルド18272
ビルド18272の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)を参照してください。

### <a name="wsl"></a>WSL
* **要する**このビルドには、WSL が動作しなくなる問題があります。 ディストリビューションを起動しようとすると、"そのようなインターフェイスはサポートされていません" というエラーが表示されます。 この問題は修正され、来週の Insider Fast ビルドに含まれるようになりました。 このビルドがインストールされている場合は、「設定-> Update & Security-> Recovery」の「以前のバージョンの Windows 10 に戻る」を使用して、以前の Windows ビルドにロールバックできます。

## <a name="build-18267"></a>ビルド18267
ビルド18267の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)を参照してください。

### <a name="wsl"></a>WSL
* ゾンビプロセスが reaped されず、無期限に保持される問題を修正します。
* エラーメッセージが最大長を超えた場合、WslRegisterDistribution がハングする [GH 3592]
* DrvFs で読み取り専用ファイルの fsync を正常に実行できるようにする [GH 3556]
* [GH 3584] 内にシンボリックリンクを作成する前に、/bin と/sbin ディレクトリが存在することを確認します。
* WSL インスタンスのインスタンス終了タイムアウトメカニズムが追加されました。 タイムアウトは現在15秒に設定されています。つまり、最後の WSL プロセスが終了してから15秒後にインスタンスが終了します。 ディストリビューションをすぐに終了するには、次のように使用します。
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>ビルド 17763 (1809)
ビルド17763の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)を参照してください。

### <a name="wsl"></a>WSL
* 同じスレッド優先順位を変更するための setpriority syscall アクセス許可チェックが strict すぎます [GH 1838]
* Clock_gettime (CLOCK_BOOTTIME) の負の値が返されないように、起動時間にバイアスをかけない割り込み時間を使用することを確認してください () [GH 3434]
* WSL binfmt インタープリターでのシンボリックリンクの処理 [GH 3424]
* Threadgroup リーダーファイル記述子のクリーンアップをより適切に処理します。
* KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用してオーバーフローを回避するように WSL を切り替える [GH 3252]
* Ptrace をアタッチすると、システムコールから無効な戻り値が返される [GH 1731]
* AF_UNIX 関連のいくつかの問題を修正する [GH 3371]
* 現在の作業ディレクトリの長さが5文字未満の場合に WSL 相互運用機能が失敗する原因となる問題を修正しました [GH 3379]
* 存在しないポートへのループバック接続で1秒間の遅延が発生しないようにする [GH 3286]
* /Proc/sys/fs/file-max スタブファイルの追加 [GH 2893]
* より正確な IPV6 スコープ情報。
* PR_SET_PTRACER のサポート [GH 3053]
* パイプファイルシステムがエッジトリガーの epoll イベントを誤って消去しています [GH 3276]
* NTFS シンボリックリンクによって起動された Win32 実行可能ファイルがシンボリックリンク名を尊重しない [GH 2909]
* 強化されたゾンビサポート [GH 1353]
* Windows 相互運用機能の動作を制御するための wsl のエントリを追加する [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 常に UNIX ソケットファミリの種類を返す getsockname でないことを修正する [GH 1774]
* TIOCSTI のサポートを追加する [GH 1863]
* 接続処理中の非ブロッキングソケットは、書き込み試行に EAGAIN を返します [GH 2846]
* マウントされた Vhd での相互運用のサポート [GH 3246, 3291]
* ルートフォルダーでのアクセス許可チェックの問題の修正 [GH 3304]
* TTY キーボード ioctl KDGKBTYPE、KDGKBMODE、および KDSKBMODE のサポートが制限されています。
* Windows UI アプリは、バックグラウンドで起動した場合でも実行する必要があります。
* Wsl-u または--user オプションを追加する [GH 1203]
* 高速スタートアップが有効になっているときの WSL 起動の問題を修正する [GH 2576]
* Unix ソケットが切断されたピア資格情報を保持する必要がある [GH 3183]
* EAGAIN で無制限の非ブロッキング Unix ソケットが失敗する [GH 3191]
* case = off は新しい既定の drvfs マウントの種類 [GH 2937, 3212, 3328]
    * 詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。
* Wslconfig/terminate を追加して、実行中のディストリビューションを停止します。
* スペースを含むパスを正しく処理しない WSL シェルコンテキストメニューエントリの問題を修正します。
* ディレクトリごとの大文字と小文字の区別を拡張属性として公開する
* ARM64: キャッシュメンテナンス操作をエミュレートします。 [Dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。
* DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみを unescape します。
* ELF パーサーインタープリターの長さの検証での1つずつのエラーの修正 [GH 3154]
* 過去の時間を持つ WSL 絶対タイマーが起動しない [GH 3091]
* 新しく作成された再解析ポイントが親ディレクトリに表示されていることを確認します。
* DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。
* ファイルが存在する場合でも、マルチスレッド操作が ENOENT を返す可能性のある追加の問題を修正しました。 [GH 2712]
* UMCI が有効になっているときの WSL 起動エラーを修正しました。 [GH 3020]
* WSL [GH 437, 603, 1836] を起動するには、エクスプローラーのコンテキストメニューを追加します。 を使用するには、エクスプローラーウィンドウで、shift キーを押しながら右クリックします。
* Unix ソケットの非ブロッキング動作の修正 [GH 2822、3100]
* GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正しました。
* マウント伝達フラグ [GH 2911] のサポートを追加します。
* Truncate で inotify イベントが発生しない問題を修正する [GH 2978]。
* シェルを使用せずに1つのバイナリを呼び出すには、wsl の--exec オプションを追加します。
* 特定のディストリビューションを選択するには、wsl のディストリビューションオプションを追加します。
* Dmesg のサポートが制限されています。 アプリケーションは、dmesg にログを記録できるようになりました。 WSL ドライバーは、制限された情報を dmesg に記録します。 将来は、この機能を拡張して、ドライバーから他の情報や診断情報を伝達することができます。
    * 注: 現在、 `/dev/kmsg` dmesg はデバイスインターフェイスでサポートされています。 `syslog`syscall インターフェイスはまだサポートされていません。 そのため、などの一部の`dmesg`コマンドラインオプション`-S` `-C`は機能しません。
* ネイティブと一致するように既定の gid とシリアルデバイスのモードを変更する [GH 3042]
* DrvFs は拡張属性をサポートするようになりました。
    * 注:DrvFs では、拡張属性の名前にいくつかの制限があります。 一部の文字 ('/'、': '、'\*' など) は使用できません。また、拡張属性名は、drvfs では大文字と小文字が区別されません。

## <a name="build-18252-skip-ahead"></a>ビルド 18252 (前へスキップ)
ビルド18252の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)を参照してください。

### <a name="wsl"></a>WSL
* Init と bsdtar のバイナリを lxssmanager dll から別のツールフォルダーに移動する
* CLONE_FILES を使用するときのファイル記述子の終了に関する競合を修正します。
* DrvFs パスを変換するときに/proc/pid/mountinfo の省略可能なフィールドを処理する
* S_IFREG のメタデータをサポートせずに DrvFs mknod を正常に実行できるようにする
* DrvFs で作成される readonly ファイルは、readonly 属性セットを持つ必要があります [GH 3411]
* DrvFs のマウントを処理する/sbin/mount.drvfs helper を追加する
* DrvFs で POSIX 名の変更を使用します。
* ボリューム GUID がないボリュームでパスの変換を許可します。

## <a name="build-17738-fast"></a>ビルド 17738 (高速)
ビルド17738の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)を参照してください。

### <a name="wsl"></a>WSL
* 同じスレッド優先順位を変更するための setpriority syscall アクセス許可チェックが strict すぎます [GH 1838]
* Clock_gettime (CLOCK_BOOTTIME) の負の値が返されないように、起動時間にバイアスをかけない割り込み時間を使用することを確認してください () [GH 3434]
* WSL binfmt インタープリターでのシンボリックリンクの処理 [GH 3424]
* Threadgroup リーダーファイル記述子のクリーンアップをより適切に処理します。

## <a name="build-17728-fast"></a>ビルド 17728 (高速)
ビルド17728の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)を参照してください。

### <a name="wsl"></a>WSL
* KeQueryPerformanceCounter ではなく KeQueryInterruptTimePrecise を使用してオーバーフローを回避するように WSL を切り替える [GH 3252]
* Ptrace をアタッチすると、システムコールから無効な戻り値が返される [GH 1731]
* AF_UNIX 関連のさまざまな問題を修正する [GH 3371]
* 現在の作業ディレクトリの長さが5文字未満の場合に WSL 相互運用機能が失敗する原因となる問題を修正しました [GH 3379]

## <a name="build-18204-skip-ahead"></a>ビルド 18204 (前へスキップ)
ビルド18204の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。

### <a name="wsl"></a>WSL
* パイプファイルシステム inadvertenly によるエッジトリガー epoll イベントの消去 [GH 3276]
* NTFS シンボリックリンクによって起動された Win32 実行可能ファイルがシンボリックリンク名を尊重しない [GH 2909]

## <a name="build-17723-fast"></a>ビルド 17723 (高速)
ビルド17723の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)を参照してください。

### <a name="wsl"></a>WSL
* 存在しないポートへのループバック接続で1秒間の遅延が発生しないようにする [GH 3286]
* /Proc/sys/fs/file-max スタブファイルの追加 [GH 2893]
* より正確な IPV6 スコープ情報。
* PR_SET_PTRACER のサポート [GH 3053]
* パイプファイルシステム inadvertenly によるエッジトリガー epoll イベントの消去 [GH 3276]
* NTFS シンボリックリンクによって起動された Win32 実行可能ファイルがシンボリックリンク名を尊重しない [GH 2909]

## <a name="build-17713"></a>ビルド17713
ビルド17713の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)を参照してください。

### <a name="wsl"></a>WSL
* 強化されたゾンビサポート [GH 1353]
* Windows 相互運用機能の動作を制御するための wsl のエントリを追加する [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 常に UNIX ソケットファミリの種類を返す getsockname でないことを修正する [GH 1774]
* TIOCSTI のサポートを追加する [GH 1863]
* 接続処理中の非ブロッキングソケットは、書き込み試行に EAGAIN を返します [GH 2846]
* マウントされた Vhd での相互運用のサポート [GH 3246, 3291]
* ルートフォルダーでのアクセス許可チェックの問題の修正 [GH 3304]
* TTY キーボード ioctl KDGKBTYPE、KDGKBMODE、および KDSKBMODE のサポートが制限されています。
* Windows UI アプリは、バックグラウンドで起動した場合でも実行する必要があります。

## <a name="build-17704"></a>ビルド17704
ビルド17704の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)を参照してください。

### <a name="wsl"></a>WSL
* Wsl-u または--user オプションを追加する [GH 1203]
* 高速スタートアップが有効になっているときの WSL 起動の問題を修正する [GH 2576]
* Unix ソケットが切断されたピア資格情報を保持する必要がある [GH 3183]
* EAGAIN で無制限の非ブロッキング Unix ソケットが失敗する [GH 3191]
* case = off は新しい既定の drvfs マウントの種類 [GH 2937, 3212, 3328]
    * 詳細については、[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)を参照してください。
* Wslconfig/terminate を追加して、実行中のディストリビューションを停止します。

## <a name="build-17692"></a>ビルド 17692
ビルド17692の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)を参照してください。

### <a name="wsl"></a>WSL
* スペースを含むパスを正しく処理しない WSL シェルコンテキストメニューエントリの問題を修正します。
* ディレクトリごとの大文字と小文字の区別を拡張属性として公開する
* ARM64: キャッシュメンテナンス操作をエミュレートします。 [Dotnet の問題](https://github.com/dotnet/core/issues/1561)を解決します。
* DrvFs: エスケープされた文字に対応するプライベート範囲内の文字のみを unescape します。

## <a name="build-17686"></a>ビルド 17686
ビルド17686の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)を参照してください。

### <a name="wsl"></a>WSL
* ELF パーサーインタープリターの長さの検証での1つずつのエラーの修正 [GH 3154]
* 過去の時間を持つ WSL 絶対タイマーが起動しない [GH 3091]
* 新しく作成された再解析ポイントが親ディレクトリに表示されていることを確認します。
* DrvFs に大文字と小文字を区別するディレクトリをアトミックに作成します。

## <a name="build-17677"></a>ビルド17677
ビルド17677の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)を参照してください。

### <a name="wsl"></a>WSL
* ファイルが存在する場合でも、マルチスレッド操作が ENOENT を返す可能性のある追加の問題を修正しました。 [GH 2712]
* UMCI が有効になっているときの WSL 起動エラーを修正しました。 [GH 3020]

## <a name="build-17666"></a>ビルド17666
ビルド17666の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)を参照してください。

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>警告:一部の AMD チップセットで WSL の実行を妨げる問題があります [GH 3134]。 修正の準備ができました。 Insider Build 分岐に変更することができます。
* WSL [GH 437, 603, 1836] を起動するには、エクスプローラーのコンテキストメニューを追加します。 [エクスプローラー] ウィンドウで [保留] をクリックして右クリックします。
* Unix ソケットの非ブロッキング動作の修正 [GH 2822、3100]
* GH 2026 で報告されているように、ハングしている NETLINK コマンドを修正しました。
* マウント伝達フラグ [GH 2911] のサポートを追加します。
* Truncate で inotify イベントが発生しない問題を修正する [GH 2978]。
* シェルを使用せずに1つのバイナリを呼び出すには、wsl の--exec オプションを追加します。
* 特定のディストリビューションを選択するには、wsl のディストリビューションオプションを追加します。

## <a name="build-17655-skip-ahead"></a>ビルド 17655 (前へスキップ)
ビルド17655の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)を参照してください。

### <a name="wsl"></a>WSL
* Dmesg のサポートが制限されています。 アプリケーションは、dmesg にログを記録できるようになりました。 WSL ドライバーは、制限された情報を dmesg に記録します。 将来は、この機能を拡張して、ドライバーから他の情報や診断情報を伝達することができます。
    * 注: 現在、 `/dev/kmsg` dmesg はデバイスインターフェイスでサポートされています。 `syslog`sycall インターフェイスは、まだサポートされていません。 そのため、などの一部の`dmesg`コマンドラインオプション`-S` `-C`は機能しません。
* ファイルが存在する場合でも、マルチスレッド操作で ENOENT が返される問題を修正しました。 [GH 2712]

## <a name="build-17639-skip-ahead"></a>ビルド 17639 (前へスキップ)
ビルド17639の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)を参照してください。

### <a name="wsl"></a>WSL
* ネイティブと一致するように既定の gid とシリアルデバイスのモードを変更する [GH 3042]
* DrvFs は拡張属性をサポートするようになりました。
    * 注:DrvFs では、拡張属性の名前にいくつかの制限があります。 特に、一部の文字 ('/'、': '、'\*' など) は使用できません。また、拡張属性名は、drvfs では大文字と小文字が区別されません。

## <a name="build-17133-fast"></a>ビルド 17133 (高速)
ビルド17133の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)を参照してください。

### <a name="wsl"></a>WSL
* WSL のハングを修正します。 [GH 3039、3034]

## <a name="build-17128-fast"></a>ビルド 17128 (高速)
ビルド17128の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)を参照してください。

### <a name="wsl"></a>WSL
* なし

## <a name="build-17627-skip-ahead"></a>ビルド 17627 (前へスキップ)
ビルド17627の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)を参照してください。

### <a name="wsl"></a>WSL
* Futex pi 対応の操作のサポートを追加します。 [GH 1006]
    * 優先順位は現在サポートされている WSL 機能ではないため、制限がありますが、標準の使用をブロック解除する必要があります。
* WSL プロセス用の Windows ファイアウォールのサポート。 [GH 1852]
    * たとえば、WSL python プロセスが任意のポートでリッスンできるようにするには、管理者特権の Windows cmd を使用します。```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * ファイアウォール規則を追加する方法の詳細については、「[リンク](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)」を参照してください。
* Wsl を使用するときのユーザーの既定のシェルを尊重します。 [GH 2372]
* すべてのネットワークインターフェイスをイーサネットとして報告します。 [GH 2996]
* 破損した/etc/passwd ファイルの処理が改善されます。 [GH 3001]

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17618-skip-ahead"></a>ビルド 17618 (前へスキップ)
ビルド17618の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)を参照してください。

### <a name="wsl"></a>WSL
* NT interop の擬似コンソール機能の導入 [GH 988、1366、1433、1542、2370、2406]。
* レガシインストールメカニズム (lxrun) は非推奨となりました。 ディストリビューションのインストールに関してサポートされているメカニズムは、Microsoft Store を使用することです。

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17110"></a>ビルド 17110
ビルド17110の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)を参照してください。

### <a name="wsl"></a>WSL
* /Init を Windows から終了することを許可します [GH 2928]。
* DrvFs では、既定でディレクトリごとの大文字小文字の区別が使用されるようになりました ("case = dir" マウントオプションと同等)。
    * "Case = force" (以前の動作) を使用するには、レジストリキーを設定する必要があります。 次のコマンドを実行して、使用する必要がある場合は "case = force" を有効にします。 reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1
    * 以前のバージョンの Windows で wsl で作成された既存のディレクトリがあり、大文字と小文字を区別する必要がある場合は、fsutil を使用し<path>て大文字と小文字を区別するように指定します。 fsutil .exe ファイル setcasesensitiveinfo enable
* Uname syscall から返された NULL の終了文字列。

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17107"></a>ビルド17107
ビルド17107の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)を参照してください。

### <a name="wsl"></a>WSL
* マスター pty エンドポイントで TCSETSF と TCSETSF をサポートする [GH 2552]。
* 相互運用プロセスを同時に開始すると、EINVAL [GH 2813] になります。
* /Proc/pid/status. に適切なトレースの状態を表示するように PTRACE_ATTACH を修正します。
* CLEARTID フラグと SETTID フラグの両方で複製された短い有効期間のプロセスが、TID アドレスをクリアせずに終了する可能性がある競合を修正しました。
* 17093より前のビルドから移動するときに、Linux ファイルシステムディレクトリをアップグレードするときにメッセージを表示します。 17093ファイルシステムの変更の詳細については、 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)のリリースノートを参照してください。

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17101"></a>ビルド17101
ビルド17101の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)を参照してください。

### <a name="wsl"></a>WSL
* Signalfd のサポート。 [GH 129]
* ファイル名に無効な NTFS 文字を含むファイル名は、プライベート Unicode 文字としてエンコードすることによってサポートされます。 [GH 1514]
* 書き込みがサポートされていない場合、自動マウントは読み取り専用にフォールバックします。 [GH 2603]
* Unicode サロゲートペア (絵文字文字など) の貼り付けを許可します。 [GH 2765]
* /Proc および/sys の疑似ファイルは、select、poll、epoll、et al から読み取りおよび書き込み準備を返す必要があります。 [GH 2838]
* レジストリが改ざんされているか、または破損している場合に、サービスが無限ループに入る可能性のある問題を修正しました。
* Iproute2 の新しい (アップストリーム 4.14) バージョンで動作するように netlink メッセージを修正します。

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17093"></a>ビルド17093
ビルド17093の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)を参照してください。

#### <a name="important"></a>重要:
このビルドにアップグレードした後に初めて WSL を開始するときは、Linux ファイルシステムディレクトリをアップグレードする作業を実行する必要があります。 この処理には数分かかる場合があるため、WSL の開始に時間がかかることがあります。 これは、ストアからインストールされた各ディストリビューションにつき1回のみ発生します。
* DrvFs での大文字と小文字の区別のサポートが向上しました。
    * DrvFs では、ディレクトリごとの大文字小文字の区別がサポートされるようになりました。 これは、ディレクトリに設定できる新しいフラグで、これらのディレクトリ内のすべての操作を大文字と小文字を区別して扱う必要があることを示します。これにより、Windows アプリケーションでも大文字と小文字のみが異なるファイルを正しく開くことができます。
    * DrvFs には、ディレクトリごとに大文字と小文字の区別を制御する新しいマウントオプションがあります。
        * case = force: すべてのディレクトリは大文字と小文字を区別して処理されます (ドライブのルートを除く)。 WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。 これは、新しいディレクトリの大文字小文字の区別をマークする場合を除き、従来の動作です。
        * case = dir: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは大文字と小文字が区別されます。 WSL で作成された新しいディレクトリは、大文字と小文字が区別されます。
        * case = off: ディレクトリごとの大文字小文字の区別フラグを持つディレクトリのみが、大文字と小文字を区別して扱われます。他のディレクトリでは大文字と小文字が区別されます。 WSL で作成された新しいディレクトリは、大文字と小文字が区別されません。
    * 注: 以前のリリースで WSL によって作成されたディレクトリには、このフラグが設定されていないため、"case = dir" オプションを使用した場合、は大文字と小文字が区別されません。 既存のディレクトリにこのフラグを設定する方法は近日中に予定されています。
    * これらのオプションを使用してマウントする例 (既存のドライブの場合は、別のオプションでマウントする前にマウントを解除する必要があります): sudo mount-t drvfs C:/mnt/c case = dir
    * ここでは、case = force は引き続き既定のオプションです。 これは、将来、case = dir に変更されます。
* DrvFs をマウントするときに Windows パスでスラッシュを使用できるようになりました。例: sudo mount-t drvfs/server/mnt/share
* WSL は、インスタンスの開始時に/etc/fstab ファイルを処理するようになりました [GH 2636]。
    * これは、DrvFs ドライブを自動的にマウントする前に行われます。fstab によって既にマウントされているドライブは自動的には再マウントされないため、特定のドライブのマウントポイントを変更することができます。
    * この動作は、wsl を使用して無効にすることができます。
* Mount、mountinfo、および mountstats の各ファイルは、円記号やスペースなどの特殊文字を正しくエスケープします [GH 2799]
* WSL シンボリックリンクなどの DrvFs を使用して作成された特殊なファイル、またはメタデータが有効になっている場合は、fifo とソケットを使用して、Windows からコピーおよび移動できるようになりました。

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL は wsl. conf で構成可能
WSL で特定の機能を自動的に構成するためのメソッドを追加しました。これは、サブシステムを起動するたびに適用されます。 これには、自動マウントオプションとネットワーク構成が含まれます。 詳細については、次のブログ投稿を参照してください。 https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX は、WSL および Windows ネイティブプロセスでの Linux プロセス間のソケット接続を許可します。
WSL と Windows アプリケーションは、Unix ソケット経由で相互に通信できるようになりました。 Windows でサービスを実行し、Windows と WSL アプリの両方で使用できるようにする場合を考えてみましょう。 これは、Unix ソケットで可能です。 詳細については、ブログの投稿の「」を参照してください。 https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* MAP_NORESERVE を使用した mmap () のサポート [GH 121、2784]
* Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]
* 複製で SIGCHLD 以外の終了シグナルを処理する [GH 121, 2781]
* スタブ/proc/sys/fs/inotify/max_user_instances と/proc/sys/fs/inotify/max_user_watches [GH 1705]
* 0以外のオフセットで読み込みヘッダーを含む ELF バイナリの読み込み中にエラーが発生した [GH 1884]
* イメージの読み込み時に、ページの末尾のバイトをゼロアウトします。
* Execve がサイレントモードでプロセスを終了するケースを減らす

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17083"></a>ビルド 17083
ビルド17083の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)を参照してください。

### <a name="wsl"></a>WSL
* Epoll に関連するバグチェック (GH 2798、2801、2857) を修正します。
* ASLR をオフにするとハングを修正する [GH 1185, 2870]
* Mmap 操作がアトミックとして表示されることを確認する [GH 2732]

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17074"></a>ビルド17074
ビルド17074の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)を参照してください。

### <a name="wsl"></a>WSL
* DrvFs メタデータの固定ストレージ形式 [GH 2777] </br>
**重要:** このビルドの前に作成された DrvFs メタデータは、正しく表示されないか、まったく表示されません。 影響を受けるファイルを修正するには、chmod と chown を使用してメタデータを再適用します。
* 複数のシグナルと再開可能な syscall の問題を修正した。

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17063"></a>ビルド17063
ビルド17063の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)を参照してください。

### <a name="wsl"></a>WSL
* DrvFs は、追加の Linux メタデータをサポートします。 これにより、chmod/chown を使用してファイルの所有者とモードを設定できるほか、fifo、unix ソケット、デバイスファイルなどの特殊なファイルを作成することもできます。 現時点では、これはまだ試験段階であるため、既定では無効になっています。
**注:** DrvFs で使用されるメタデータ形式のバグを修正しています。 メタデータは実験のためにこのビルドで機能しますが、今後のビルドでは、このビルドによって作成されたメタデータを正しく読み取ることができません。  変更したファイルの所有者を手動で更新しなければならない場合があります。カスタムデバイス ID を持つデバイスを再作成する必要があります。

  有効にするには、メタデータオプションを使用して DrvFs をマウントします (既存のマウントで有効にするには、最初にマウントを解除する必要があります)。

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux のアクセス許可は、ファイルに追加のメタデータとして追加されます。Windows のアクセス許可には影響しません。  Windows エディターを使用してファイルを編集すると、メタデータが削除される場合があることに注意してください。 この場合、ファイルは既定のアクセス許可に戻ります。

* メタデータなしでファイルを制御するための、DrvFs にマウントオプションを追加しました。
  * uid: すべてのファイルの所有者に使用されるユーザー ID。
  * gid: すべてのファイルの所有者に使用されるグループ ID。
  * umask: すべてのファイルとディレクトリに対して除外するアクセス許可の8進数のマスク。
  * fmask: すべての標準ファイルに対して除外するアクセス許可の8進数のマスク。
  * dmask: すべてのディレクトリに対して除外するアクセス許可の8進数のマスク。

  以下に例を示します。
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  メタデータオプションと組み合わせて、メタデータのないファイルに対する既定のアクセス許可を指定します。

* では、wsl と`WSLENV`Win32 の間で環境変数がどのように流れるかを構成するために、新しい環境変数が導入されました。

  以下に例を示します。

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`は、wsl から Win32 または Win32 プロセスから WSL プロセスを起動するときに含めることができる環境変数のコロン区切りの一覧です。  各変数には、スラッシュとその後に続くフラグを付けて、変換方法を指定できます。
  * irtran-p値は、WSL パスと Win32 パスの間で変換されるパスです。
  * 左右値はパスの一覧です。 WSL では、コロンで区切られたリストです。 Win32 では、セミコロンで区切られたリストです。
  * u値は、Win32 から WSL を呼び出すときにのみ含める必要があります
  * リダイレクト値は、WSL から Win32 を呼び出すときにのみ含める必要があります

  ユーザーのカスタム`WSLENV` Windows 環境では、.bashrc またはを設定できます。

* drvfs マウントによって tar、cp-p からのタイムスタンプが正しく保持される (GH 1939)
* drvfs symlink は正しいサイズを報告します (GH 2641)
* I/O サイズが非常に大きい場合の読み取り/書き込みの機能 (GH 2653)
* waitpid はプロセスグループ Id と連動します (GH 2534)
* 大きな予約領域での mmap パフォーマンスが大幅に向上しました。ghc のパフォーマンスを向上させます (GH 1671)
* READ_IMPLIES_EXEC でのパーソナリティのサポート最大化 a と clisp (GH 1185) を修正します。
* mprotect は PROT_GROWSDOWN をサポートしています。clisp (GH 1128) を修正します。
* 過剰コミットモードでのページフォールトの修正sbcl (GH 1128) を修正します。
* 複製では、より多くのフラグの組み合わせがサポートされます
* Epoll ファイルの select/epoll (以前は no op) をサポートします。
* 未実装の syscall の ptrace を通知します。
* Resolv.conf を生成するときにアップしていないインターフェイスを無視する [GH 2694]
* 物理アドレスのないネットワークインターフェイスを列挙します。 [GH 2685]
* 追加のバグの修正と改善。

### <a name="linux-tools-available-to-developers-on-windows"></a>Windows の開発者が使用できる Linux ツール

* Windows コマンドラインツールチェーンには、bsdtar (tar) と curl が含まれています。
  この2つの新しいツールの追加の詳細と、Windows での開発者エクスペリエンスの整形方法を確認するには、[このブログ](https://aka.ms/tarcurlwindows)を参照してください。

*   `AF_UNIX`は、Windows Insider SDK (17061 +) で利用できます。
  の詳細と、Windows 上の`AF_UNIX`開発者が使用する方法については、[このブログ](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)を参照してください。

### <a name="console"></a>Console
* 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。


## <a name="build-17046"></a>ビルド17046

ビルド17046の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)を参照してください。

### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- アクティブなターミナルを使用せずにプロセスを実行できるようにします。 [GH 709、1007、1511、2252、2391、et al.]
- CLONE_VFORK と CLONE_VM のサポートの強化。 [GH 1878、2615]
- WSL ネットワーク操作の TDI フィルタードライバーをスキップします。 [GH 1554]
- DrvFs は、特定の条件が満たされたときに NT シンボリックリンクを作成します。 [GH 353、1475、2602]
    - リンク先は相対パスである必要があり、マウントポイントやシンボリックリンクを越えることはできず、存在する必要があります。
    - 開発者モードが有効になっていない場合は、ユーザーは SE_CREATE_SYMBOLIC_LINK_PRIVILEGE を持っている必要があります (通常は、管理者特権で起動する必要があります)。
    - それ以外の状況でも、DrvFs は WSL シンボリックリンクを作成します。
- 昇格および昇格されていない WSL インスタンスの同時実行を許可します。
- /Proc/sys/kernel/yama/ptrace_scope のサポート
- Wslpath を追加して、WSL <-> Windows パス変換を実行します。 [GH 522、1243、1834、2327、et al]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- 修正はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。


## <a name="build-17040"></a>ビルド17040

ビルド17040の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 17035以降の修正プログラムはありません。

#### <a name="console"></a>Console
- 17035以降の修正プログラムはありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17035"></a>ビルド17035

ビルド17035の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- DrvFs 上のファイルへのアクセスは、場合によっては、EINVAL で失敗することがあります。 [GH 2448]

#### <a name="console"></a>Console
- VT モードで行を挿入または削除するときに色が失われることがあります。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17025"></a>ビルド17025

ビルド17025の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 新しいフォアグラウンドプロセスグループで初期プロセスを開始します [GH 1653, 2510]。
- SIGHUP 配信の修正プログラム [GH 2496]。
- [GH 2497] が指定されていない場合は、既定の仮想ブリッジ名を生成します。
- /Proc/sys/kernel/random/boot_id [GH 2518] を実装します。
- 相互運用機能の stdout/stderr パイプの修正。
- Syncfs システム呼び出しをスタブします。

#### <a name="console"></a>Console
- サードパーティコンソールの入力 VT translation の修正 [GH 111]

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="build-17017"></a>ビルド17017

ビルド17017の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 空の ELF プログラムヘッダー [GH 330] を無視します。
- LxssManager が非対話型ユーザーの WSL インスタンスを作成できるようにします (ssh およびスケジュールされたタスクのサポート) [GH 777, 1602]。
- WSL-> Win32 > WSL ("設立") シナリオのサポート [GH 1228]。
- 相互運用機能によって起動されるコンソールアプリの終了の制限付きサポート [GH 1614]。
- Devpts のマウントオプション [GH 1948] をサポートします。
- Ptrace が子スタートアップをブロックしています [GH 2333]。
- EPOLLET には、一部のイベント [GH 2462] がありません。
- PTRACE_GETSIGINFO の他のデータを返します。
- Getdents と lseek では、正しくない結果が得られます。
- いくつかの Win32 相互運用アプリのハングを修正しました。これ以上データのないパイプで入力を待機しています。
- O_ASYNC は、tty/pty ファイルをサポートしています。
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- このリリースでは、コンソールに関連する変更はありません。

### <a name="ltp-results"></a>LTP の結果:
テストを実行中です。

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>ビルド16288

ビルド16288の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- ソケットファイル記述子の uid、gid、およびモードを正しく初期化して報告する [GH 2490]
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- このリリースでは、コンソールに関連する変更はありません。

### <a name="ltp-results"></a>LTP の結果:
16273以降の変更はありません

## <a name="build-16278"></a>ビルド16278

ビルド162738の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- LX MM 状態を解除するときに、ファイルによってサポートされるセクションのマップされたビューを明示的にマップ解除する [GH 2415]
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- このリリースでは、コンソールに関連する変更はありません。

### <a name="ltp-results"></a>LTP の結果:
16273以降の変更はありません

## <a name="build-16275"></a>ビルド16275

ビルド162735の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- このリリースでは、WSL 関連の変更はありません。

#### <a name="console"></a>Console
- このリリースでは、コンソールに関連する変更はありません。

### <a name="ltp-results"></a>LTP の結果:
16273以降の変更はありません

## <a name="build-16273"></a>ビルド16273

ビルド16273の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- DrvFs がディレクトリに対して正しくないファイルの種類を報告する場合があるという問題を修正しました [GH 2392]
- Uevent [GH 1121、2293、2242、2295、2235、648、637] を使用するプログラムのブロックを解除するための NETLINK_KOBJECT_UEVENT sockets の作成を許可します
- 非ブロッキング接続のサポートを追加する [GH 903、1391、1584、1585、1829、2290、2314]
- CLONE_FS CLONE システム呼び出しフラグを実装する [GH 2242]
- NT interop でタブまたは引用符を正しく処理しない問題を修正する [GH 1625, 2164]
- WSL インスタンスを再起動しようとしたときにアクセス拒否エラーを解決する [GH 651、2095]
- Futex FUTEX_REQUEUE と FUTEX_CMP_REQUEUE 操作の実装 [GH 2242]
- さまざまな SysFs ファイルのアクセス許可を修正する [GH 2214]
- セットアップ中に Haskell stack のハングを修正する [GH 2290]
- Binfmt_misc ' C ' ' O ' および ' P ' フラグを実装する [GH 2103]
- /Proc/sys/kernel/shmmax/shmmni & 追加する [GH 1753]
- Ioprio_set システム呼び出しの部分的なサポートを追加する [GH 498]
- スタブ SO_REUSEPORT & SO_PASSCRED for netlink sockets のサポートの追加 [GH 69]
- ディストリビューションが現在インストールまたはアンインストールされている場合は、RegisterDistribuiton から別のエラーコードを返します。
- Wslconfig .exe 経由で部分的にインストールされた WSL ディストリビューションの登録解除を許可する
- Udp:: msg_peek から python ソケットテストハングを修正します。
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- このリリースでは、コンソールに関連する変更はありません。

### <a name="ltp-results"></a>LTP の結果:
テストの合計:1904<br/>
スキップされたテストの合計数:209<br/>
合計エラー数:229<br/>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>ビルド 16257

ビルド16257の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- Prlimit64 システム呼び出しを実装する
- Ulimit-n (setrlimit RLIMIT_NOFILE) のサポートを追加する [GH 1688]
- TCP ソケットのスタブ MSG_MORE [GH 2351]
- 無効な AT_EXECFN 補助ベクター動作の修正 [GH 2133]
- コンソール/tty のコピー/貼り付け動作を修正し、完全なバッファー処理をさらに追加する [GH 2204, 2131]
- AT_SECURE プログラムと set-group-ID プログラムの補助ベクターでの設定 [GH 2031]
- Psuedo-ターミナルマスターエンドポイントが TIOCPGRP を処理しない [GH 1063]
- Lseek が LxFs のディレクトリを巻き戻していることを修正する [GH 2310]
- 大きな使用率が高くなった後の GH のロック [1882]
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- すべての場所で水平線/アンダースコアを修正する [GH 2168]
- プロセスの順序が変更されたことを修正し、NPM を閉じることが困難になる [GH 2170]
- 新しい配色を追加しました。 https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP の結果:
16251以降の変更はありません

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`prlimit64`<br/>

### <a name="known-issues"></a>既知の問題
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub の問題 2392:Windows フォルダーは WSL によって認識されません...](https://github.com/Microsoft/BashOnWindows/issues/2392)
ビルド16257では、を介し`/mnt/c/...`て Windows ファイル/フォルダーを列挙するときに、wsl に問題があります。
この問題は修正されており、8/14/2017 の実行時に、Insider ビルドでリリースされる必要があります。

<br/>

## <a name="build-16251"></a>ビルド16251

ビルド16251の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- WSL オプションコンポーネントからベータタグを削除します。詳細については、[ブログの投稿](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)を参照してください。
- Set-ユーザー ID および set-ID バイナリが exec で正しく初期化されました。 exec [GH 962, 1415, 2072]
- Ptrace PTRACE_O_TRACEEXIT のサポートを追加しました [GH 555]
- NT_FPREGSET を使用した ptrace PTRACE_GETFPREGS と PTRACE_GETREGSET のサポートを追加しました [GH 555]
- 無視されたシグナルで停止する ptrace を修正しました
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- このリリースでは、コンソールに関連する変更はありません。

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:768</br>
失敗したテストの数:244</br>
スキップされたテストの数:96</br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>ビルド16241

ビルド16241の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- このリリースでは、WSL 関連の変更はありません。

#### <a name="console"></a>Console
- [ここで](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)最初に報告された、10進線に誤った文字を出力するように修正しました。
- コードページ 65001 (utf8) に出力テキストが表示されないように修正します。
- ある色の RGB 値に対して行われた変更を、選択の変更時にパレットの他の部分に転送しないでください。 これにより、コンソールプロパティシートが非常に使いやすいようになります。
- Ctrl + S が正しく動作していません
- ANSI エスケープコードに完全に存在しない太字/-Dim [GH 2174]
- コンソールが Vim 色のテーマを正しくサポートしていない [GH 1706]
- 特定の文字を貼り付けることはできません [GH 2149]
- 編集/コマンドライン上にあるときに bash ウィンドウのサイズを変更すると、リフローサイズの変更がおかしくなる [GH ConEmu 1123]
- Ctrl + L を押したまま画面をダーティにする [GH 1978]
- HDPI で VT を表示するときのコンソールレンダリングのバグ [GH 1907]
- Unicode 文字 U + 30FB で Japansese 文字が奇妙に見える [GH 2146]
- 追加の機能強化とバグ修正

</br>

## <a name="build-16237"></a>ビルド 16237

ビルド16237の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定
- Lxfs に EAs がないファイルの既定の属性を使用する (ルート、ルート、0000)
- 拡張属性を使用するディストリビューションのサポートを追加しました
- Getdents と getdents64 によって返されるエントリの埋め込みを修正する
- Shmctl SHM_STAT システム呼び出しのアクセス許可チェックを修正する [GH 2068]
- Tty の初期 epoll 状態が正しくないことを修正した [GH 2231]
- すべてのエントリを返さないように DrvFs readdir を修正する [GH 2077]
- ファイルのリンクが解除されたときに LxFs readdir を修正する [GH 2077]
- Procfs を使用して、リンクされていない drvfs ファイルを再び開くことを許可する
- WSL 機能を無効にするためのグローバルレジストリキーの上書き (相互運用/ドライブのマウント) を追加しました
- DrvFs (および LxFs) の "stat" で間違ったブロックカウントを修正する [GH 1894]
- 追加の機能強化とバグ修正

</br>

## <a name="build-16232"></a>ビルド16232

ビルド16232の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
- このリリースでは、WSL 関連の変更はありません。

</br>

## <a name="build-16226"></a>ビルド16226

ビルド16226の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定
- xattr 関連の syscall サポート (getxattr、setxattr、listxattr、removexattr)。
- capablity xattr のサポート。
- 特定のファイルシステムとフィルター (MS 以外の SMB サーバーを含む) との互換性が向上しました。 [GH #1952]
- OneDrive プレースホルダー、GVFS プレースホルダー、および圧縮された OS 圧縮ファイルのサポートが強化されました。
- 追加の機能強化とバグ修正

</br>

## <a name="build-16215"></a>ビルド16215

ビルド16215の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
- WSL には開発者モードが不要になりました。
- Drvfs のディレクトリの接合をサポートします。
- WSL distribution appx パッケージのアンインストールを処理します。
- Procfs を更新して、プライベートと共有のマッピングを表示します。
- Wslconfig .exe を追加して、部分的にインストールまたはアンインストールされたディストリビューションをクリーンアップします。
- TCP ソケット用の IP_MTU_DISCOVER のサポートを追加しました。 [GH 1639、2115、2205]
- AF_INADDR へのルートのプロトコルファミリを推定します。
- シリアルデバイスの機能強化 [GH 1929]。

</br>

## <a name="build-16199"></a>ビルド16199

ビルド16199の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
- これらのリリースでは、WSL 関連の変更はありません。

</br>

## <a name="build-16193"></a>ビルド16193

ビルド16193の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
- 送信 SIGCONT と threadgroup 終了の間の競合状態 [GH 1973]
- tty および pty デバイスを FILE_DEVICE_CONSOLE ではなくレポート FILE_DEVICE_NAMED_PIPE に変更する [GH 1840]
- IP_OPTIONS の SSH 修正
- DrvFs を init デーモンにマウントしました [GH 1862、1968、1767、1933]
- 次の NT シンボリックリンクに対する DrvFs のサポートが追加されました。

</br>

## <a name="build-16184"></a>ビルド16184

ビルド16184の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
- Apt パッケージのメンテナンスタスク (lxrun/update) を削除しました
- Node.js の Windows プロセスからに表示されない修正済みの出力 [GH 1840]
- Lxcore での調整要件の緩和 [GH 1794]
- システム呼び出しの数値における AT_EMPTY_PATH フラグの処理を修正した。
- 開いているハンドルを持つ DrvFs ファイルを削除すると、ファイルに未定義の動作が発生する問題を修正した (GH 544、966、1357、1535、1615)
- /etc/hosts は Windows hosts ファイル (%windir%\system32\drivers\etc\hosts) からエントリを継承するようになりました [GH 1495]

</br>

## <a name="build-16179"></a>ビルド16179

ビルド16179の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
- 今週、WSL の変更はありません。

</br>

## <a name="build-16176"></a>ビルド16176

ビルド16176の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定

- [有効なシリアルサポート](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- 追加された IP ソケットオプション IP_OPTIONS [GH 1116]
- Pwritev 関数の実装 (nginx/PHP-FPM へのファイルのアップロード) [GH 1506]
- 追加された IP ソケットオプション IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- ソケットオプション IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP のサポート [GH 1678]
- Apps ノード、traceroute、掘り下げ、nslookup、host の IP (V6) MTU socket オプションを追加しました
- 追加された IP ソケットオプション IPV6_UNICAST_HOPS
- [ファイルシステムの機能強化](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * UNC パスのマウントを許可する
    * Drvfs で CDF サポートを有効にする
    * Drvfs でネットワークファイルシステムのアクセス許可を正しく処理する
    * Drvfs にリモートドライブのサポートを追加する
    * Drvfs での FAT サポートを有効にする
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果
15042以降の変更はありません

</br>

## <a name="build-16170"></a>ビルド16170

ビルド16170の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)を参照してください。<br/>

WSL のテストの取り組みについて説明する新しい[ブログ投稿](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)をリリースしました。

### <a name="fixed"></a>固定

- サポートソケットオプション IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- PTRACE_OLDSETOPTIONS のサポートを追加します。 [GH 1692]
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果
15042以降の変更はありません

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>ビルド15046から Windows 10 の作成者への更新
Windows 10 の作成者の更新プログラムに含まれるように計画されている WSL 修正プログラムや機能はこれ以上ありません。 WSL のリリースノートは、次の主要な Windows Update を対象とした追加のために、今後数週間にわたって再開されます。 ビルド15046および今後の Insider リリースに関する一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)を参照してください。 <br/><br/>
 <br/>

## <a name="build-15042"></a>ビルド15042

ビルド15042の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定

- "." で終わるパスの削除時にデッドロックが発生する問題を修正します。
- FIONBIO が成功時に0を返さないという問題を修正した [GH 1683]
- Inet データグラムソケットの長さゼロの読み取りに関する問題を修正した
- Drvfs inode 参照で競合状態が発生したことが原因でデッドロックが発生する可能性を修正する [GH 1675]
- Unix ソケットの補助データの拡張サポートSCM_CREDENTIALS および SCM_RIGHTS [GH 514, 613, 1326]
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:737</br>
非パッシング (失敗、スキップされたなど) の数:255

</br>

## <a name="build-15031"></a>ビルド15031

ビルド15031の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定

- Time (2) が散発的に不適切な動作するバグを修正しています。
- \* SIGSYSCALL MASK がシグナルマスクを破壊する可能性がある問題を修正しました。
- WSL プロセス作成通知でコマンドラインの完全な長さを返すようになりました。 [GH 1632]
- WSL は、GDB がハングした場合に ptrace を介してスレッドの終了を報告するようになりました。 [GH 1196]
- Tmux IO が大量に発生した後に ptys がハングするバグを修正します。 [GH 1358]
- 多くのシステムコールでタイムアウトの検証を修正 (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create)
- 追加された eventfd EFD_SEMAPHORE サポート [GH 452]
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:737</br>
非パッシング (失敗、スキップされたなど) の数:255 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>ビルド15025

ビルド15025の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定

- Grep 2.27 を破損したバグの修正 [GH 1578]
- Eventfd2 syscall の EFD_SEMAPHORE フラグの実装 [GH 452]
- 実装された/proc/[pid]/net/ipv6_route [GH 1608]
- Unix ストリームソケットに対するシグナル駆動型 IO のサポート [GH 393, 68]
- F_GETPIPE_SZ と F_SETPIPE_SZ のサポート [GH 1012]
- Recvmmsg () syscall の実装 [GH 1531]
- Epoll_wait () が待機していないバグを修正 [GH 1609]
- /Proc/version_signature を実装する
- T syscall は、両方のファイル記述子が同じパイプを参照している場合にエラーを返すようになりました
- Unix ソケット用の SO_PEERCRED の正しい動作を実装しています
- Tkill syscall の無効なパラメーター処理を修正した
- Drvfs の preformace を増やすための変更
- Ruby IO ブロックの軽微な修正
- Inet sockets の MSG_DONTWAIT フラグの EINVAL を返す recvmsg () を修正した [GH 1296]
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:732</br>
非パッシング (失敗、スキップされたなど) の数:255 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>ビルド15019

ビルド15019の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定

- Htop (GH 823、945、971) などのツールに対して procfs の CPU 使用率が誤って報告されたバグを修正しました
- 既存のファイルに対して O_TRUNC を使用して open () を呼び出すと、IN_OPEN の前に IN_MODIFY が生成されるようになりました。
- Unix socket getsockopt SO_ERROR で postgress [GH 61, 1354] を有効にするための修正
- /Proc/sys/net/core/somaxconn を実装する
- Apt-パッケージ更新のバックグラウンドタスクをビューから非表示にするようになりました
- Ipv6 localhost のスコープをクリアします (Spring Framework (Java) エラー)。
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:714 </br>
非パッシング (失敗、スキップされたなど) の数:249 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>ビルド15014

ビルド15014の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)を参照してください。<br/>


### <a name="fixed"></a>固定

- Ctrl + C は意図したとおりに動作するようになりました
- htop と ps auxw で、正しいリソース使用率 (GH #516) が表示されるようになりました
- NT 例外からシグナルへの基本的な変換です。 (GH #513)
- fallocate は、EINVAL (GH #1571) ではなく領域が不足しているときに、ENOSPC で失敗するようになりました。
- 追加された/proc/sys/kernel/sem.
- Semop および semtimedop システム呼び出しを実装します。
- IP_RECVTOS & IPV6_RECVTCLASS socket オプションで nslookup エラーを修正した (GH 69)
- ソケットオプションの IP_RECVTTL と IPV6_RECVHOPLIMIT のサポート
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:709 </br>
非パッシング (失敗、スキップされたなど) の数:255 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall の概要
合計 Syscall:384 </br>
実装された合計:235 </br>
スタブの合計数:22 </br>
未実装の合計数:127 </br>
[詳細な内訳](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>ビルド15007

ビルド15007の一般的な Windows 情報については、 [windows のブログ]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)を参照してください。<br/>


### <a name="known-issue"></a>既知の問題

- コンソールが一部の Ctrl + <key>入力を認識しないという既知のバグがあります。  これには、通常の "c" キーの押下として機能する ctrl + c コマンドが含まれます。

  - 回避策:代替キーを Ctrl + C にマップします。 たとえば、ctrl + K を Ctrl + C キーにマップするに`stty intr \^k`は、次のようにします。  このマッピングはターミナル単位で行われ、bash が起動されるたび*に実行さ*れる必要があります。 ユーザーは、オプションを調べて、`.bashrc`

### <a name="fixed"></a>固定

- WSL を実行すると CPU コアの 100% が消費される問題を修正しました
- ソケットオプション IP_PKTINFO、IPV6_RECVPKTINFO がサポートされるようになりました。 (GH #851、987)
- Lxcore でネットワークインターフェイスの物理アドレスを16バイトに切り捨てる (GH #1452、1414、1343、468、308)
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:709 </br>
非パッシング (失敗、スキップされたなど) の数:255 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>ビルド15002

ビルド15002の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)を参照してください。<br/>


### <a name="known-issue"></a>既知の問題

2つの既知の問題:
- コンソールが一部の Ctrl + <key>入力を認識しないという既知のバグがあります。  これには、通常の "c" キーの押下として機能する ctrl + c コマンドが含まれます。

  - 回避策:代替キーを Ctrl + C にマップします。 たとえば、ctrl + K を Ctrl + C キーにマップするに`stty intr \^k`は、次のようにします。  このマッピングはターミナル単位で行われ、bash が起動されるたび*に実行さ*れる必要があります。 ユーザーは、オプションを調べて、`.bashrc`

- WSL が実行されている間、システムスレッドは CPU コアの 100% を消費します。  根本原因は、内部的に解決されています。

### <a name="fixed"></a>固定

- すべての bash セッションは、同じアクセス許可レベルで作成する必要があります。  別のレベルでセッションを開始しようとすると、ブロックされます。  つまり、管理者コンソールと管理者以外のコンソールを同時に実行することはできません。 (GH #626)
<br/>
- 次の NETLINK_ROUTE メッセージを実装した (Windows 管理者が必要)
     - RTM_NEWADDR (サポート`ip addr add`)
     - RTM_NEWROUTE (サポート`ip route add`)
     - RTM_DELADDR (サポート`ip addr del`)
     - RTM_DELROUTE (サポート`ip route del`)
- 更新するパッケージのスケジュールされたタスクは、従量制課金接続では実行されなくなります (GH #1371)
- パイプがスタックした場合のエラーを修正します。 bash-c "ls-alR/" |bash-c "cat" (GH #1214)
- 実装された TCP_KEEPCNT socket オプション (GH #843)
- IP_MTU_DISCOVER INET socket オプション (GH #720、717、170、69) を実装しています
- Nt パス参照を使用して init から NT バイナリを実行する従来の機能を削除しました。 (GH #1325)
- グループまたはその他の読み取りアクセスを許可するように更新モードを修正する (0644) (GH #1321)
- 実装された/proc/sys/kernel/random/uuid (GH #1092)
- プロセスの開始時刻が2432年 (GH #974) と表示されたエラーを修正しました
- 既定の用語環境変数を xterm-256 色に切り替えました (GH #1446)
- プロセスフォーク中にコミットが計算される方法を変更しました。 (GH #1286)
- /Proc/sys/vm/overcommit_memory. の実装 (GH #1286)
- 実装された/proc/net/route ファイル (GH #69)
- ショートカット名が正しくローカライズされていないエラーを修正しました (GH #696)
- プログラムヘッダーの検証に誤りのある elf 解析ロジックを修正した場合は、PATH_MAX 未満である必要があります。 (GH #1048)
- Procfs、sysfs、cgroupfs、および binfmtfs (GH #1378) の statfs コールバックを実装します。
- 閉じることのできない AptPackageIndexUpdate ウィンドウを修正しました (GH #1184、GH #1193 で説明)
- ASLR パーソナリティ ADDR_NO_RANDOMIZE のサポートを追加しました。 (GH #1148、1128)
- AV 中に適切な gdb スタックトレースを実現するための PTRACE_GETSIGINFO、SIGSEGV が改善されました (GH #875)
- Elf の解析は、パッチ elf バイナリでは失敗します。 (GH #471)
- /Etc/resolv.conf に反映された VPN DNS (GH #416、1350)
- より信頼性の高いデータ転送のための TCP close の機能強化。 (GH #610、616、1025、1335)
- 開いているファイルが多すぎる場合 (EMFILE)、適切なエラーコードを返すようになりました。 (GH #1126、2090)
- Windows 監査ログで、プロセス作成の監査でイメージ名が報告されるようになりました。
- Bash ウィンドウ内から bash を起動すると、正常に失敗する
- 相互運用機能が LxFs で作業ディレクトリにアクセスできないときにエラーメッセージが追加されました (例: .bashrc)
- WSL で Windows パスが切り捨てられた問題を修正しました
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:690 </br>
非パッシング (失敗、スキップされたなど) の数:274 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>ビルド14986

ビルド14986の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定

- Netlink および Pty Ioctl を使用したバグチェックの修正
- カーネルのバージョンが Xenial との一貫性のために 4.4.0-43 を報告するようになりました
- "Nul:" にリダイレクトされたときに Bash が起動するようになりました (GH #1259)
- Procfs (GH #967) でスレッド Id が正しくレポートされるようになりました
- IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |IN_ISDIR フラグが inotify_add_watch () でサポートされるようになりました (GH #1280)
- Timer_create と関連するシステムコールを実装します。  これにより、GHC サポート (GH #307) が可能になります。
- Ping によって 0.000 m の時間 (GH #1296) が返された問題を修正しました。
- 開いているファイルが多すぎる場合は、正しいエラーコードを返します。
- WSL の Netlink 要求が、インターフェイスのハードウェアアドレスが32バイト (Teredo インターフェイスなど) の場合は EINVAL で失敗する問題を修正した。
   - Linux の "ip" ユーティリティには、WSL が32バイトのハードウェアアドレスを報告した場合にクラッシュするバグが含まれていることに注意してください。 これは、WSL ではなく、"ip" のバグです。 "Ip" ユーティリティは、ハードウェアアドレスの印刷に使用される文字列バッファーの長さをハードコーディングします。また、32バイトのハードウェアアドレスを出力するには、バッファーが小さすぎます。
- その他の修正プログラムと機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:669 </br>
非パッシング (失敗、スキップされたなど) の数:258 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>ビルド14971

ビルド14971の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定

 - Windows Subsystem for Linux では、コントロールを超える状況により、このビルドには更新プログラムがありません。  定期的にスケジュールされた更新は、次回のリリースで再開されます。

### <a name="ltp-results"></a>LTP の結果:
14965から変更されていません </br>
成功したテストの数:664 </br>
非パッシング (失敗、スキップされたなど) の数:263 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>ビルド14965

ビルド14965の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定

- Netlink sockets NETLINK_ROUTE protocol の RTM_GETLINK および RTM_GETADDR (GH #468) のサポート
  - ネットワーク列挙に対する ifconfig および ip コマンドを有効にします
  - 詳細については、 [Wsl ネットワークに関するブログ記事](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)を参照してください。

- /sbin がユーザーのパスに既定で含まれるようになりました。
- NT ユーザーパスが既定で WSL パスに追加されました (つまり、Linux パスに System32 を追加せずに notepad.exe を入力できるようになりました)
- /Proc/sys/kernel/cap_last_cap のサポートを追加しました
- 現在の作業ディレクトリに ansi 以外の文字が含まれている場合、WSL から NT バイナリを起動できるようになりました (GH #1254)
- 切断された unix ストリームソケットでのシャットダウンを許可します。
- PR_GET_PDEATHSIG のサポートを追加しました。
- CLONE_PARENT のサポートを追加しました
- パイプがスタックした場合のエラーを修正します。 bash-c "ls-alR/" |bash-c "cat" (GH #1214)
- 現在のターミナルに接続するための要求を処理します。
- /Proc/<pid>/oom_score_adj を書き込み可能としてマークします。
- /Fs フォルダーを追加します。
- sched_setaffinity は、関係ビットマスクの数を返す必要があります
- インタープリターパスの長さが64文字未満であることを誤って想定している ELF 検証ロジックを修正します。 (GH #743)
- 開いているファイル記述子は、コンソールウィンドウを開いたままにすることができます (GH #1187)
- 名前の変更 () がターゲット名の末尾のスラッシュで失敗した Fixeed エラー (GH #1008)
- /Proc/net/dev ファイルを実装する
- タイマー精度による 0.000 ms ping を修正します。
- 実装された/proc/self/environ (GH #730)
- その他のバグ修正と機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:664 </br>
非パッシング (失敗、スキップされたなど) の数:263 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>ビルド14959

ビルド14959の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)を参照してください。<br/>


### <a name="fixed"></a>固定

- Windows の Pico Process 通知が改善されました。  [Wsl ブログ](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)に記載されている追加情報。
- Windows の相互運用性による安定性の向上
- エンタープライズデータ保護 (EDP) が有効になっている場合に bash を起動したときのエラー0x80070057 を修正しました
- その他のバグ修正と機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:665 </br>
非パッシング (失敗、スキップされたなど) の数:263 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>ビルド14955

ビルド14955の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)を参照してください。<br/>


### <a name="fixed"></a>固定

 - Windows Subsystem for Linux では、コントロールを超える状況により、このビルドには更新プログラムがありません。  定期的にスケジュールされた更新は、次回のリリースで再開されます。

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:665 </br>
非パッシング (失敗、スキップされたなど) の数:263 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>ビルド14951

ビルド14951の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)を参照してください。<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>新機能:Windows/Ubuntu の相互運用性
Windows バイナリを WSL コマンドラインから直接呼び出すことができるようになりました。  これにより、ユーザーは Windows 環境とシステムを、不可能な方法で操作できるようになります。  簡単な例として、ユーザーが次のコマンドを実行できるようになりました。

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

詳細については、以下を参照してください。

- [相互運用のための WSL チームブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN Interop のドキュメント](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>固定

- Ubuntu 16.04 (Xenial) が、すべての新しい WSL インスタンスにインストールされるようになりました。  既存の 14.04 (Trusty) インスタンスを持つユーザーは自動的にアップグレードされません。
- インストール中に設定されたロケールが表示されるようになりました
- WSL プロセスをファイルにリダイレクトする場合のバグを含むターミナルの機能強化
- コンソールの有効期間は、bash の有効期間に関連付けられている必要があります
- コンソールウィンドウのサイズは、バッファーサイズではなく表示サイズを使用する必要があります
- その他のバグ修正と機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:665 </br>
非パッシング (失敗、スキップされたなど) の数:263 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>ビルド14946

ビルド14946の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)を参照してください。<br/>


### <a name="fixed"></a>固定

- スペースまたは引用符を含む NT ユーザー名を持つユーザーの WSL ユーザーアカウントを作成できない問題を修正しています。 
- ディレクトリのリンク数が stat で0を返すように、VolFs と DrvFs を変更します。
- IPV6_MULTICAST_HOPS socket オプションをサポートします。
- Tty ごとに1つのコンソール i/o ループに制限します。 例: 次のコマンドを実行できます。
  - bash-c "echo data" |bash-c "ssh user@example.com " cat > foo .txt ""

- /proc/cpuinfo のタブでスペースを置換する (GH #1115)
- Mountinfo に DrvFs が、マウントされた Windows ボリュームと一致する名前で表示されるようになりました。
- /home と/root が mountinfo に正しい名前で表示されるようになりました
- その他のバグ修正と機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:665 </br>
非パッシング (失敗、スキップされたなど) の数:263 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>ビルド14942

ビルド14942の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/onefourninefourtwoooooo)を参照してください。<br/>


### <a name="fixed"></a>固定

- SSH をブロックしていた "NOEXECUTE MEMORY の実行を試行しました" というネットワーククラッシュを含む、いくつかのバグを解決しました。
- DrvFs の Windows アプリケーションから生成された通知の inotifiy サポートがになりました。
- TCP_KEEPIDLE と TCP_KEEPINTVL を mongod 用に実装します。 (GH #695)
- Pivot_root システムコールを実装する
- SO_DONTROUTE のソケットの実装オプション
- その他のバグ修正と機能強化


### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:665 </br>
非パッシング (失敗、スキップされたなど) の数:263 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>ビルド14936

ビルド14936の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)を参照してください。<br/>


注:WSL は、今後のリリースで Ubuntu 14.04 (Trusty) ではなく、Ubuntu バージョン 16.04 (Xenial) をインストールします。  この変更は、新しいインスタンスをインストールする場合に適用されます (lxrun/install または bash の最初の実行)。  Trusty を使用した既存のインスタンスは自動的にはアップグレードされません。 ユーザーは、Trusty コマンドを使用して、自分のイメージを Xenial にアップグレードできます。

### <a name="known-issue"></a>既知の問題
WSL でいくつかのソケット実装に問題が発生しています。  "NOEXECUTE MEMORY の実行を試行しました" というエラーが発生すると、バグチェックはクラッシュします。  この問題の最も一般的な取り組みは、ssh を使用する場合のクラッシュです。  根本原因は内部ビルドで固定されており、最も早い機会に Insider にプッシュされます。

### <a name="fixed"></a>固定

- Chroot システム呼び出しを実装します。
- ~~DrvFs の Windows アプリケーションから生成された通知のサポートを含む~~inotify の機能強化
  - 量現時点では利用できない Windows アプリケーションからの変更については、Inotify のサポートが提供されています。
- IPV6 へのソケットバインド:<port n> : で IPV6_V6ONLY (GH #68、#157、#393、#460、#674、#740、#982、#996) がサポートされるようになりました。
- Waitid systemcall が実装された WNOWAIT 動作 (GH #638)
- IP ソケットオプション IP_HDRINCL と IP_TTL のサポート
- 長さ0の読み取り () はすぐに返される必要があります (GH #975)
- Tar ファイルに NULL 終端文字を含まないファイル名とファイル名プレフィックスを正しく処理します。
- /dev/null の epoll サポート
- 更新プログラムのタイムソースを修正する
- Bash-c がファイルにリダイレクトできるようになりました
- その他のバグ修正と機能強化

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:664 </br>
非パッシング (失敗、スキップされたなど) の数:264 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`chroot`<br/>
<br/>

## <a name="build-14931"></a>ビルド14931

ビルド14931の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定

 - Windows Subsystem for Linux では、コントロールを超える状況により、このビルドには更新プログラムがありません。  定期的にスケジュールされた更新は、次のリリースで再開されます。

<br/>

## <a name="build-14926"></a>ビルド14926

ビルド14926の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定

- 管理者特権を持たないコンソールで Ping が機能するようになりました。
- Ping6 がサポートされるようになりました。管理者特権も必要ありません
- WSL によって変更されたファイルの Inotify サポート。 (GH #216)
  - サポートされているフラグ:
    - inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watch イベント:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch 属性 (i):LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 出力の読み取り:LX_IN_ISDIR, LX_IN_IGNORED
  - 既知の問題:Windows アプリケーションからファイルを変更してもイベントが生成されない
- Unix ソケットで SCM_CREDENTIALS がサポートされるようになりました。

### <a name="ltp-results"></a>LTP の結果:
成功したテストの数:651 </br>
非パッシング (失敗、スキップされたなど) の数:258 </br>
[LTP テストの実行ログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>ビルド14915

ビルド14915の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)を参照してください。<br/>


### <a name="fixed"></a>固定
-  Unix データグラムソケットの socketpair (GH #262)
- SO_REUSEADDR の Unix ソケットサポート
- SO_BROADCAST の UNIX ソケットサポート (GH #568)
- SOCK_SEQPACKET の Unix ソケットサポート (GH #758、#546)
- Unix データグラムソケットの送信、受信、およびシャットダウンのサポートの追加
- 非固定アドレスに対する mmap パラメーターの検証が無効なため、バグチェックを修正します。 (GH #847)
- ターミナル状態の中断/再開のサポート
- 画面ユーティリティのブロックを解除する TIOCPKT ioctl のサポート (GH #774)
    - 既知の問題:関数キーが動作していません
- TimerFd の競合を修正しました。これにより、解放されたメンバー ' ReaderReady ' が Lxp Timerfdworkspace Erroutine (GH #814) によってアクセスされる可能性があります
- Futex、投票、clock_nanosleep の再起動可能なシステムコールのサポートを有効にする
- バインドマウントサポートを追加しました
- マウントの名前空間のサポートの共有を解除する
    - 既知の問題:現在の作業ディレクトリを使用し`unshare(CLONE_NEWNS)`て新しいマウント名前空間を作成すると、引き続き古い名前空間が参照されます。
- 追加の機能強化とバグ修正

<br/>

## <a name="build-14905"></a>ビルド14905

ビルド14905の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)を参照してください。<br/>


### <a name="fixed"></a>固定
- 再開可能なシステムコールがサポートされるようになりました (GH #349、GH #520)
- 現在操作中のディレクトリへのシンボリックリンク (GH #650)
- /Dev/random の RNDGETENTCNT ioctl を実装します。
- /Proc/[pid]/マウント,/proc/[pid]/mountinfo および/proc/[pid]/mountstats ファイルを実装します。
- その他のバグ修正と機能強化

</br>

## <a name="build-14901"></a>ビルド14901
Windows 10 記念日更新リリースの最初の Insider ビルド。

ビルド14901の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)を参照してください。<br/>


### <a name="fixed"></a>固定
- 末尾のスラッシュの問題を修正した
    - などのコマンドが動作するようになりました`$ mv a/c/ a/b/`
- Ubuntu ロケールを Windows ロケールに設定するかどうかを確認するメッセージが表示されるようになりました
- Ns フォルダーの Procfs サポート
- Tmpfs、procfs、および sysfs ファイルシステムのマウントとマウント解除を追加しました
- Mknod [at] 32 ビット ABI 署名の修正
- Unix ソケットをディスパッチモデルに移行
- Setsockopt を使用して、INET ソケットの recv バッファーサイズを設定する必要があります
- MSG_CMSG_CLOEXEC unix socket receive message フラグを実装する
- Linux プロセス stdin/stdout パイプのリダイレクト (GH #2)
    - CMD で bash-c コマンドのパイプを使用できるようにします。  例: > dir |bash-c "grep foo"
- Bash を複数のシステムにインストールできるようになりました (GH #538、#358)
- 既定の INET ソケットバッファーサイズは、既定の Ubuntu セットアップのものと一致している必要があります。
- Xattr syscall を listxattr に揃える
- SIOCGIFCONF から有効な IPv4 アドレスを持つインターフェイスのみを返す
- Ptrace によって挿入されるときのシグナルの既定の動作を修正する
- /proc/sys/vm/min_free_kbytes を実装する
- Sigreturn でコンテキストを復元するときにマシンコンテキストレジスタの値を使用する
    - これにより、一部のユーザーに対して java と javac がハングした問題が解決されます。
- /Proc/sys/kernel/hostname を実装する

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>14388を Windows 10 記念日更新プログラムにビルドする
ビルド14388の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/14388wip)を参照してください。 <br/>

### <a name="fixed"></a>固定
- 8/2 で Windows 10 記念日更新プログラムを準備するための修正プログラム
  - 記念日の更新に関する詳細については、こちらの[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください。

<br/>

## <a name="build-14376"></a>ビルド14376
ビルド14376の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)を参照してください。 <br/>

### <a name="fixed"></a>固定
- Apt-get がハングするインスタンスをいくつか削除しました (GH #493)
- 空のマウントが正しく処理されない問題を修正しました
- Ramdisks が正しくマウントされていない問題を修正しました
- Unix ソケットの受け入れをサポートフラグに変更する (partial GH #451)
- 一般的なネットワーク関連のブルースクリーンを修正した
- /Proc/[pid]/task (GH #523) にアクセスするときにブルースクリーンを修正
- 一部の pty シナリオ (GH #488、#504) の高 CPU 使用率を修正した
- その他のバグ修正と機能強化

<br/>

## <a name="build-14371"></a>ビルド14371
ビルド14371の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)を参照してください。 <br/>

### <a name="fixed"></a>固定
- Ptrace を使用するときに SIGCHLD と wait () を使用してタイミングレースを修正しました
- パスの末尾に/(GH #432) がある場合の動作を修正しました
- 子へのハンドルが開いているため、名前の変更とリンク解除に失敗する問題を修正した
- その他のバグ修正と機能強化

<br/>

## <a name="build-14366"></a>ビルド14366
ビルド14366の一般的な Windows 情報については、 [windows のブログ](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)を参照してください。 <br/>

### <a name="fixed"></a>固定
- シンボリックリンクを使用したファイル作成時の修正
-   Python 用 listxattr (GH 385) が追加されました
-   その他のバグ修正と機能強化

### <a name="syscall-support"></a>Syscall のサポート
-   次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>ビルド14361
ビルド14361の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14361)を参照してください。 <br/>

### <a name="fixed"></a>固定
- Windows 上で Bash on Ubuntu を実行すると、DrvFs の大文字と小文字が区別されるようになりました。
  - ユーザーは .txt と大文字小文字を区別することができます。/Mnt/c ドライブ上の TXT
  - 大文字小文字の区別は、Bash on Ubuntu on Windows でのみサポートされています。 Bash の外部では、ファイルが正しく報告されますが、予期しない動作が Windows からのファイルの操作で発生する場合があります。
  - 各ボリュームのルート (つまり/mnt/c) は大文字と小文字が区別されません。
  - これらのファイルを Windows で処理する方法の詳細については、[こちら](https://support.microsoft.com/en-us/kb/100625)を参照してください。
- Pty/tty のサポートが大幅に強化されました。  TMUX のようなアプリケーションがサポートされるようになりました (GH #40)
- ユーザーアカウントが常に作成されていないインストールの問題を修正しました
- 非常に長い引数リストを許可する最適化されたコマンドライン arg 構造体。 (GH #153)
- DrvFs からファイルを削除することができるようになりました。
- 切断時にターミナルがハングする一部のインスタンスを修正した (GH #43)
- chmod と chown が tty デバイスで動作するようになりました
- 0\.0.0.0 および:: as localhost (GH #388) への接続を許可します
- Sendmsg/recvmsg が > 1 (partial GH #376) の IO ベクターの長さを処理するようになりました
- ユーザーは、自動生成された hosts ファイル (GH #398) をオプトアウトできるようになりました。
- インストール中に Linux ロケールを NT ロケールに自動的に一致させる (GH #11)
- /Proc/sys/vm/swappiness ファイル (GH #306) が追加されました。
- strace が正常に終了するようになりました
- /Proc/self/fd を使用してパイプを再度開くことを許可する (GH #222)
- DrvFs から%LOCALAPPDATA%\lxss の下にあるディレクトリを非表示にする (GH #270)
- Bash の処理の強化 ~.  などのコマンド"bash ~-c %.ls"(GH #467) をサポートするようになりました
- ソケットはシャットダウン中に使用可能な epoll read を通知するようになりました (GH #271)
- lxrun/uninstall では、ファイルとフォルダーを削除する機能が改善されています。
- 修正された ps-f (GH #246)
- XEmacs (GH #481) などの x11 アプリのサポートの強化
- 既定の Ubuntu 設定に一致するように初期スレッドスタックサイズを更新し、get_rlimit syscall (GH #172、#258) にサイズを正しく報告しました
- Pico プロセスのイメージ名 (監査のためなど) のレポートが改善されました。
- Df コマンドの/proc/mountinfo を実装します。
- 子名のシンボリックリンクエラーコードを修正した。 そして。
- 追加の改善バグ修正と改善

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>ビルド14352
ビルド14352の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14352)を参照してください。<br/>


### <a name="fixed"></a>固定
- 大きなファイルが正しくダウンロードまたは作成されなかった問題を修正しました。  これにより、npm とその他のシナリオ (GH #3、GH #313) のブロックが解除されます。
- ソケットがハングする一部のインスタンスを削除しました
- いくつかの ptrace エラーを修正しました
- 255文字を超えるファイル名を許可する WSL の問題を修正しました
- 英語以外の文字のサポートの強化
- 現在の Windows タイムゾーンデータを追加し、既定として設定する
- 各マウントポイントの一意のデバイス id (jre fix – GH #49)
- "." を含むパスの問題を修正してください。 および "."
- 追加された Fifo サポート (GH #71)
- ネイティブ Ubuntu 形式に一致するように resolv.conf の形式を更新しました
- 一部の procfs クリーンアップ
- 管理者コンソールの ping を有効にする (GH #18)

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>ビルド14342
ビルド14342の一般的な Windows 情報については、 [Windows ブログ](https://aka.ms/wip14342)を参照してください。 <br/>

VolFs とドライブ Fs に関する情報は、 [Wsl ブログ](https://blogs.msdn.microsoft.com/wsl)を参照してください。 <br/>

### <a name="fixed"></a>固定
- Windows ユーザーのユーザー名に Unicode 文字が含まれている場合のインストールの問題を修正しました
- FAQ の apt get 更新 udev の回避策は、最初の実行時に既定で提供されるようになりました。
- ドライブ fs (/mnt/<drive>) ディレクトリでのシンボリックリンクの有効化
- シンボリックリンクがドライブ Fs と VolFs 間で機能するようになりました
- 解析の問題、アドレス指定された最上位レベル パス: %.ls/期待どおりに、正しく動作/。
- npm がドライブ Fs にインストールされ、-g オプションが機能するようになりました。
- PHP サーバーの起動を妨げている問題を修正した
- ネイティブ Ubuntu に近い $PATH など、既定の環境値が更新されました
- Apt パッケージキャッシュを更新するための週単位のメンテナンスタスクが Windows に追加されました
- ELF ヘッダーの検証に関する問題を修正しました。 WSL ですべての Melkor オプションがサポートされるようになりました
- Zsh シェルが機能しています
- プリコンパイル済みのジャンプバイナリがサポートされるようになりました
- Bash の初回実行時のプロンプトが正しくローカライズされるようになりました
- /proc/meminfo が正しい情報を返すようになりました
- VFS でソケットがサポートされるようになりました
- /dev が tempfs としてマウントされるようになりました
- Fifo がサポートされるようになりました
- /Proc/cpuinfo で、マルチコアシステムが正しく表示されるようになりました。
- 初回実行時の追加の改善とエラーメッセージのダウンロード
- Syscall の機能強化とバグ修正。 以下のサポートされている syscall 一覧。
- その他のバグ修正と機能強化

### <a name="known-issues"></a>既知の問題
- '. ' を解決できません 場合によっては、ドライブ Fs で正しく動作します。

### <a name="syscall-support"></a>Syscall のサポート
次に示すのは、WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a>ビルド14332

ビルド14332の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14332)を参照してください。 <br/>


### <a name="fixed"></a>固定
- DNS エントリの優先順位を含む resolv.conf の生成の向上
- /Mnt ドライブと/mnt 以外のドライブの間でファイルとディレクトリを移動する場合の問題
- シンボリックリンクを使用して Tar ファイルを作成できるようになりました。
- インスタンスの作成時に既定の/run/lock ディレクトリが追加されました
- /Dev/null を更新して適切な stat 情報を返す
- 初回実行時のダウンロード時の追加エラー
- Syscall の機能強化とバグ修正。 以下のサポートされている syscall 一覧。
- 追加の改善バグ修正と改善

### <a name="syscall-support"></a>Syscall のサポート
以下は、WSL で実装がいくつかある新しい syscall です。 この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>ビルド14328

ビルド14332の一般的な Windows 情報については、 [windows のブログ](https://aka.ms/wip14328)を参照してください。 <br/>


### <a name="new-features"></a>新機能
* Linux ユーザーがサポートされるようになりました。  Bash on Ubuntu on Windows をインストールすると、Linux ユーザーの作成を求めるメッセージが表示されます。  詳細については、「」を参照してください。 https://aka.ms/wslusers
* ホスト名が Windows コンピューター名に設定されました@localhost
* ビルド14328の詳細については、次を参照してください。 https://aka.ms/wip14328

### <a name="fixed"></a>固定
* 非/mnt/<drive>ファイルのシンボリックリンクの機能強化
    * npm のインストールが機能するようになりました
    * jdk/jre[はここ](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)に記載されている手順に従ってインストールできるようになりました。
    * 既知の問題: symlink は Windows マウントでは機能しません。  機能は、後のビルドで使用できるようになります
* 上部と htop が表示されるようになりました
* 一部のインストールエラーに関する追加のエラーメッセージ
* Syscall の機能強化とバグ修正。  以下のサポートされている syscall 一覧。
* 追加の改善バグ修正と改善

### <a name="syscall-support"></a>Syscall のサポート
WSL で実装がいくつかある syscall の一覧を次に示します。  この一覧の syscall は、少なくとも1つのシナリオでサポートされていますが、現時点では一部のパラメーターがサポートされていない可能性があります。

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
