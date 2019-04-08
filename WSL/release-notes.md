---
title: Windows Subsystem for Linux のリリース ノート
description: Windows Subsystem for Linux のリリース ノート。  毎週更新されます。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu 用 windows サブシステム
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 3eee7ff6d1f8302e98cde84fccabf5d9113c83f2
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063630"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のリリース ノート

## <a name="build-18342"></a>ビルド 18342
一般的な Windows ビルド 18342 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)します。

### <a name="wsl"></a>WSL
* ユーザーが Windows から WSL ディストリビューションでの Linux ファイルにアクセスする機能が追加されました。 これらのファイルは、コマンドライン、およびもファイル エクスプ ローラー、VSCode のように、Windows アプリを使用アクセスできるなどは、これらのファイルと対話できます。 移動して、ファイルにアクセス\\ \\wsl$\\< distro_name > に移動してディストリビューションを実行しているの一覧を表示または\\ \\wsl$
* 追加の CPU 情報タグを追加し、[GH 2234] Cpus_allowed [リスト] の値を修正
* Exec 非リーダー スレッド [GH 3800] からのサポートします。
* 致命的でない [GH 3785] として構成の更新の失敗を扱う
* [GH 3768] のオフセットを正しく処理するために binfmt を更新します。
* 9 の計画 [GH 3854] のネットワーク ドライブのマッピングを有効にします。
* -> Linux のサポート Windows と Linux バインド マウント モードの Windows パスの変換を ->
* 読み取り専用、開かれたファイルに読み取り専用のセクションで、マッピングを作成します。

## <a name="build-18334"></a>ビルド 18334
一般的な Windows ビルド 18334 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)します。

### <a name="wsl"></a>WSL
* Windows タイム ゾーンが Linux のタイム ゾーン [GH 3747] にマップする方法を再設計します。
* メモリ リークを修正し、新しい文字列変換関数 [GH 3746] を追加
* ないスレッドで、threadgroup SIGCONT は no-op [GH 3741] 
* 正しく/proc/self/fd のソケットと epoll のファイル記述子を表示します。

## <a name="build-18305"></a>ビルド 18305
一般的な Windows ビルド 18305 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)します。

### <a name="wsl"></a>WSL
* pthreads プライマリ スレッドの終了 [GH 3589] 時にファイルへのアクセスが失われる
* 必要である場合を除き、TIOCSCTTY は"-force"パラメーターを無視する必要があります [GH 3652]
* wsl.exe コマンドラインの機能強化と加算のインポート/エクスポート機能。
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

## <a name="build-18277"></a>ビルド 18277
一般的な Windows ビルド 18277 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)します。

### <a name="wsl"></a>WSL
* ビルド 18272 [GH 3645] で導入された「インターフェイスがサポートされています」エラーを修正します。
* Umount syscall [GH 3605] の MNT_FORCE フラグを無視します。
* 公式の CreatePseudoConsole API を使用してスイッチ WSL 相互運用機能
* FUTEX_WAIT の再起動時には、タイムアウト値を管理なし

## <a name="build-18272"></a>ビルド 18272
一般的な Windows ビルド 18272 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)します。

### <a name="wsl"></a>WSL
* **警告:** WSL を使用できない、このビルドで問題があります。 お使いのディストリビューションを起動しようとするときは、「インターフェイスがサポートされています」エラーが表示されます。 問題は修正されており、次の週の高速 Insider ビルドになります。 インストールしている場合ことができますにロールバックする前に"以前のバージョンの Windows 10 に Go"を使用して Windows ビルド設定でこのビルドに更新プログラム]-> [& セキュリティ Recovery]-> [です。

## <a name="build-18267"></a>ビルド 18267
一般的な Windows ビルド 18267 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)します。

### <a name="wsl"></a>WSL
* ゾンビのプロセスを取得しない可能性があります、無期限に問題を修正します。
* エラー メッセージが [GH 3592] の最大長を超える場合、WslRegisterDistribution がハングします。
* Fsync DrvFs [GH 3556] で、読み取り専用のファイルが正常に許可します。
* [GH 3584] 内のシンボリック リンクを作成する前にディレクトリ/bin と/sbin ディレクトリが存在することを確認します。
* WSL インスタンスのインスタンスの終了タイムアウト メカニズムを追加します。 タイムアウトは 15 秒、つまり、インスタンスは、最後の WSL プロセスが終了した後、15 秒を終了して現在設定されます。 ディストリビューションをすぐに終了するには、次のように使用します。
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>ビルド 17763 (1809)
一般的な Windows ビルド 17763 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)します。

### <a name="wsl"></a>WSL
* Setpriority syscall アクセス許可のチェックが同じスレッドの優先順位 [GH 1838] を変更するためには厳格すぎます。
* バイアスをかけない割り込み時間が clock_gettime(CLOCK_BOOTTIME) [GH 3434] の負の値が返されないように、ブート時に使用されるように
* WSL binfmt インタープリター [GH 3424] でハンドルのシンボリック リンク
* Threadgroup リーダー ファイル記述子のクリーンアップの処理の改善。
* WSL KeQueryInterruptTimePrecise を KeQueryPerformanceCounter ではなく [GH 3252] のオーバーフローを回避するために使用するスイッチします。
* Ptrace アタッチ システム コール [GH 1731] から不適切な戻り値が発生します。
* 修正プログラムのいくつかの AF_UNIX 関連の問題 [GH 3371]
* WSL の相互運用機能を現在の作業ディレクトリが 5 より小さい文字長 [GH 3379] の場合は失敗を引き起こす可能性のある問題を修正します。
* 存在しないポート [GH 3286] へのループバック接続に失敗した 1 つの 2 つ目の遅延を防ぐ
* 書き込むスタブ ファイル [GH 2893] の追加します。
* 正確な IPV6 スコープ情報。
* PR_SET_PTRACER サポート [GH 3053]
* パイプのファイル システムが誤ってところイベント [GH 3276] の消去
* Win32 実行可能ファイルの NTFS シンボリック リンクを使用して起動のリンクをシンボリック名 [GH 2909] を順守していません
* ゾンビのサポート [GH 1353] の強化
* [GH 場合 1493] Windows の相互運用機能を制御するための wsl.conf エントリを追加します。
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 常にではありません UNIX ソケット ファミリの種類 [GH 1774] を返す getsockname 問題を修正しました
* TIOCSTI [GH 1863] のサポートを追加します。
* 接続処理中の非ブロッキング ソケットの書き込み試行 [GH 2846] EAGAIN を返す必要があります。
* [GH 3246、3291] のマウントされた Vhd での相互運用機能をサポートします。
* アクセス許可のチェックのルート フォルダー [GH 3304] 上の問題を修正します。
* TTY キーボード ioctl KDGKBTYPE、KDGKBMODE および KDSKBMODE の制限付きのサポート。
* バック グラウンドで起動された場合でも、Windows UI アプリを実行する必要があります。
* Wsl-u または - ユーザー オプション [GH 1203] の追加します。
* 高速スタートアップを有効にした場合、WSL 起動の問題を修正 [GH 2576]
* Unix ソケットが切断されているピア資格情報 [GH 3183] を保持する必要があります。
* 非ブロッキング Unix ソケット EAGAIN [GH 3191] で無期限に失敗しました。
* 場合 = off が新しい既定 drvfs マウントの種類 [GH 2937、3212、3328]
    * 参照してください[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)詳細についてはします。
* Wslconfig を追加/ディストリビューションの実行を停止する終了します。
* WSL シェルのコンテキストにスペースを含むパスを正しく処理しないメニュー エントリの問題を解決します。
* 拡張属性として大文字と小文字をディレクトリあたりの公開します。
* ARM64: キャッシュのメンテナンス操作をエミュレートします。 解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)します。
* DrvFs:、エスケープされた文字に対応するプライベートの範囲内の文字のみエスケープ解除します。
* ELF パーサー インタープリター長さの検証 [GH 3154] で 1 ではオフのエラーを修正します。
* WSL の絶対タイマー、過去の時刻では [GH 3091] が起動されません。
* 新しく作成した再解析ポイントはそのために一覧表示、親ディレクトリを確認します。
* アトミックに DrvFs で大文字と小文字のディレクトリを作成します。
* 追加の問題を修正しました、ファイルが存在するにもかかわらずに、マルチ スレッド操作で ENOENT に返すことができます。 [GH 2712]
* UMCI が有効にすると、固定 WSL はエラーを起動します。 [GH 3020]
* WSL [GH 437、603、1836] を起動するエクスプ ローラーのコンテキスト メニューを追加します。 を使用するには、shift キーを押しして、エクスプ ローラー ウィンドウで右クリックします。
* [GH 2822、3100] Unix ソケット非ブロッキング動作を修正します。
* GH 2026 で報告される NETLINK コマンドのハングを修正。
* マウント フラグと反映フラグ [GH 2911] のサポートを追加します。
* 切り捨てが発生しない inotify イベント [GH 2978] で問題を解決します。
* 追加 - wsl.exe シェルせず 1 つのバイナリを呼び出すための exec オプション。
* 追加 - 特定のディストリビューションを選択する wsl.exe の分散オプション。
* Dmesg の制限付きのサポート。 アプリケーションは、dmesg をログインできるようになりました。 WSL ドライバーでは、dmesg に限定された情報を記録します。 今後、このドライバーから他の情報診断/を実行するために拡張できます。
    * 注: dmesg は現在サポートされてから、`/dev/kmsg`デバイス インターフェイス。 `syslog` syscall インターフェイスはまだサポートされていません。 そのため、いくつかの`dmesg`などのコマンド ライン オプション`-S`、`-C`機能しません。
* 既定の gid およびネイティブ [GH 3042] に一致するようにシリアル デバイスのモードを変更します。
* DrvFs 拡張属性をサポートします。
    * 注:DrvFs では、拡張属性の名前をいくつかの制限があります。 一部の文字 (のように '/'、':' と '\*') を許可、および拡張がない属性名は DrvFs で大文字小文字を区別しません。

## <a name="build-18252-skip-ahead"></a>ビルド 18252 (スキップ先)
一般的な Windows ビルド 18252 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)します。

### <a name="wsl"></a>WSL
* Lxssmanager dll 外および個別のツールのフォルダーには、init と多くのバイナリを移動します。
* CLONE_FILES を使用する場合は、ファイル記述子を閉じる周囲の競合を修正します。
* DrvFs パスを変換するときに、/proc/pid/mountinfo で省略可能なフィールドを処理します。
* S_IFREG のメタデータのサポートなしに成功 DrvFs mknod を許可します。
* DrvFs に作成される読み取り専用ファイルは読み取り専用属性が [GH 3411] の設定が必要
* DrvFs マウントを処理するために/sbin/mount.drvfs ヘルパーを追加します。
* DrvFs の POSIX 名の変更を使用します。
* ボリューム GUID を除くボリュームでは、パスの変換を許可します。

## <a name="build-17738-fast"></a>17738 (Fast) のビルドします。
一般的な Windows ビルド 17738 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)します。

### <a name="wsl"></a>WSL
* Setpriority syscall アクセス許可のチェックが同じスレッドの優先順位 [GH 1838] を変更するためには厳格すぎます。
* バイアスをかけない割り込み時間が clock_gettime(CLOCK_BOOTTIME) [GH 3434] の負の値が返されないように、ブート時に使用されるように
* WSL binfmt インタープリター [GH 3424] でハンドルのシンボリック リンク
* Threadgroup リーダー ファイル記述子のクリーンアップの処理の改善。

## <a name="build-17728-fast"></a>17728 (Fast) のビルドします。
一般的な Windows ビルド 17728 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)します。

### <a name="wsl"></a>WSL
* WSL KeQueryInterruptTimePrecise を KeQueryPerformanceCounter ではなく [GH 3252] のオーバーフローを回避するために使用するスイッチします。
* Ptrace アタッチ システム コール [GH 1731] から不適切な戻り値が発生します。
* AF_UNIX 数に関連する修正プログラムの問題 [GH 3371]
* WSL の相互運用機能を現在の作業ディレクトリが 5 より小さい文字長 [GH 3379] の場合は失敗を引き起こす可能性のある問題を修正します。

## <a name="build-18204-skip-ahead"></a>ビルド 18204 (スキップ先)
一般的な Windows ビルド 18204 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)します。

### <a name="wsl"></a>WSL
* パイプのところイベント [GH 3276] をオフにすると、ファイル システム inadvertenly
* Win32 実行可能ファイルの NTFS シンボリック リンクを使用して起動のリンクをシンボリック名 [GH 2909] を順守していません

## <a name="build-17723-fast"></a>17723 (Fast) のビルドします。
一般的な Windows ビルド 17723 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)します。

### <a name="wsl"></a>WSL
* 存在しないポート [GH 3286] へのループバック接続に失敗した 1 つの 2 つ目の遅延を防ぐ
* 書き込むスタブ ファイル [GH 2893] の追加します。
* 正確な IPV6 スコープ情報。
* PR_SET_PTRACER サポート [GH 3053]
* パイプのところイベント [GH 3276] をオフにすると、ファイル システム inadvertenly
* Win32 実行可能ファイルの NTFS シンボリック リンクを使用して起動のリンクをシンボリック名 [GH 2909] を順守していません

## <a name="build-17713"></a>ビルド 17713
一般的な Windows ビルド 17713 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)します。

### <a name="wsl"></a>WSL
* ゾンビのサポート [GH 1353] の強化
* [GH 場合 1493] Windows の相互運用機能を制御するための wsl.conf エントリを追加します。
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 常にではありません UNIX ソケット ファミリの種類 [GH 1774] を返す getsockname 問題を修正しました
* TIOCSTI [GH 1863] のサポートを追加します。
* 接続処理中の非ブロッキング ソケットの書き込み試行 [GH 2846] EAGAIN を返す必要があります。
* [GH 3246、3291] のマウントされた Vhd での相互運用機能をサポートします。
* アクセス許可のチェックのルート フォルダー [GH 3304] 上の問題を修正します。
* TTY キーボード ioctl KDGKBTYPE、KDGKBMODE および KDSKBMODE の制限付きのサポート。
* バック グラウンドで起動された場合でも、Windows UI アプリを実行する必要があります。

## <a name="build-17704"></a>ビルド 17704
一般的な Windows ビルド 17704 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)します。

### <a name="wsl"></a>WSL
* Wsl-u または - ユーザー オプション [GH 1203] の追加します。
* 高速スタートアップを有効にした場合、WSL 起動の問題を修正 [GH 2576]
* Unix ソケットが切断されているピア資格情報 [GH 3183] を保持する必要があります。
* 非ブロッキング Unix ソケット EAGAIN [GH 3191] で無期限に失敗しました。
* 場合 = off が新しい既定 drvfs マウントの種類 [GH 2937、3212、3328]
    * 参照してください[ブログ](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)詳細についてはします。
* Wslconfig を追加/ディストリビューションの実行を停止する終了します。

## <a name="build-17692"></a>ビルド 17692
一般的な Windows ビルド 17692 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)します。

### <a name="wsl"></a>WSL
* WSL シェルのコンテキストにスペースを含むパスを正しく処理しないメニュー エントリの問題を解決します。
* 拡張属性として大文字と小文字をディレクトリあたりの公開します。
* ARM64: キャッシュのメンテナンス操作をエミュレートします。 解決[dotnet 問題](https://github.com/dotnet/core/issues/1561)します。
* DrvFs:、エスケープされた文字に対応するプライベートの範囲内の文字のみエスケープ解除します。

## <a name="build-17686"></a>ビルド 17686
一般的な Windows ビルド 17686 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)します。

### <a name="wsl"></a>WSL
* ELF パーサー インタープリター長さの検証 [GH 3154] で 1 ではオフのエラーを修正します。
* WSL の絶対タイマー、過去の時刻では [GH 3091] が起動されません。
* 新しく作成した再解析ポイントはそのために一覧表示、親ディレクトリを確認します。
* アトミックに DrvFs で大文字と小文字のディレクトリを作成します。

## <a name="build-17677"></a>ビルド 17677
一般的な Windows ビルド 17677 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)します。

### <a name="wsl"></a>WSL
* 追加の問題を修正しました、ファイルが存在するにもかかわらずに、マルチ スレッド操作で ENOENT に返すことができます。 [GH 2712]
* UMCI が有効にすると、固定 WSL はエラーを起動します。 [GH 3020]

## <a name="build-17666"></a>ビルド 17666
一般的な Windows ビルド 17666 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)します。

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>警告:WSL がいくつか AMD チップセット [GH 3134] で実行されていることを防止、問題があります。 修正プログラムは、その方法 Insider ビルド ブランチ準備しです。
* WSL [GH 437、603、1836] を起動するエクスプ ローラーのコンテキスト メニューを追加します。 保留中の shift キーと、エクスプ ローラー ウィンドウで右クリックを使用します。
* [GH 2822、3100] unix ソケット非ブロッキング動作を修正します。
* GH 2026 で報告される NETLINK コマンドのハングを修正。
* マウント フラグと反映フラグ [GH 2911] のサポートを追加します。
* 切り捨てが発生しない inotify イベント [GH 2978] で問題を解決します。
* 追加 - wsl.exe シェルせず 1 つのバイナリを呼び出すための exec オプション。
* 追加 - 特定のディストリビューションを選択する wsl.exe の分散オプション。

## <a name="build-17655-skip-ahead"></a>ビルド 17655 (スキップ先)
一般的な Windows ビルド 17655 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)します。

### <a name="wsl"></a>WSL
* Dmesg の制限付きのサポート。 アプリケーションは、dmesg をログインできるようになりました。 WSL ドライバーでは、dmesg に限定された情報を記録します。 今後、このドライバーから他の情報診断/を実行するために拡張できます。
    * 注: dmesg は現在サポートされてから、`/dev/kmsg`デバイス インターフェイス。 `syslog` sycall インターフェイスはまだサポートされていません。 そのため、いくつかの`dmesg`などのコマンド ライン オプション`-S`、`-C`機能しません。
* ファイルが存在するにもかかわらずに、マルチ スレッド操作で ENOENT に返すことが問題を修正しました。 [GH 2712]

## <a name="build-17639-skip-ahead"></a>ビルド 17639 (スキップ先)
一般的な Windows ビルド 17639 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)します。

### <a name="wsl"></a>WSL
* 既定の gid およびネイティブ [GH 3042] に一致するようにシリアル デバイスのモードを変更します。
* DrvFs 拡張属性をサポートします。
    * 注:DrvFs では、拡張属性の名前をいくつかの制限があります。 具体的には、いくつかの文字 (のように '/'、':' と '\*') を許可、および拡張がない属性名は DrvFs で大文字小文字を区別しません。

## <a name="build-17133-fast"></a>17133 (Fast) のビルドします。
一般的な Windows ビルド 17133 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)します。

### <a name="wsl"></a>WSL
* WSL でハングを修正しました。 [GH 3039、3034]

## <a name="build-17128-fast"></a>17128 (Fast) のビルドします。
一般的な Windows ビルド 17128 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)します。

### <a name="wsl"></a>WSL
* なし

## <a name="build-17627-skip-ahead"></a>ビルド 17627 (スキップ先)
一般的な Windows ビルド 17627 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)します。

### <a name="wsl"></a>WSL
* Futex pi に対応した操作のサポートを追加します。 [GH 1006]
    * 優先順位いないこと現在サポートされている WSL 機能、制限がありますが、標準の使用状況ブロックを解除する必要がありますので注意してください。
* WSL プロセスの Windows ファイアウォールのサポート。 [GH 1852]
    * たとえば、WSL を許可するのには、任意のポートでリッスンするには、管理者特権で Windows cmd を使用に python が処理します。
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * ファイアウォール規則を追加する方法の詳細については、次を参照してください[リンク。](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Wsl.exe を使用する場合は、ユーザーの既定のシェルを尊重します。 [GH 2372]
* すべてのネットワーク インターフェイスは、イーサネットとして報告します。 [GH 2996]
* 破損している/etc/passwd ファイルの処理の改善。 [GH 3001]

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17618-skip-ahead"></a>ビルド 17618 (スキップ先)
一般的な Windows ビルド 17618 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)します。

### <a name="wsl"></a>WSL
* NT の相互運用機能 pseudoconsole 機能が導入 [GH 988、1366、1433、1542、2370、2406]。
* レガシ インストール メカニズム (lxrun.exe) は非推奨とされました。 ディストリビューションをインストールするためのサポートされているメカニズムは、Microsoft Store からです。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17110"></a>ビルド 17110
一般的な Windows ビルド 17110 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)します。

### <a name="wsl"></a>WSL
* Windows [GH 2928] から終了する/init を許可します。
* DrvFs は既定でディレクトリあたり大文字小文字の区別を使用するようになりました (に相当します"ケース dir ="マウント オプション)。
    * 使用して"ケース force ="(以前の動作) では、レジストリ キーを設定する必要があります。 有効にするのには、次のコマンドを実行"ケース force ="それを使用する必要がある場合: reg HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1 を追加します。
    * WSL で大文字と小文字を区別する必要がある Windows の以前のバージョンで作成された既存のディレクトリがある場合は、マークと小文字を区別する fsutil.exe を使用して: fsutil.exe ファイル setcasesensitiveinfo<path>を有効にします。
* Uname syscall から返される文字列を NULL に終了します。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17107"></a>ビルド 17107
一般的な Windows ビルド 17107 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)します。

### <a name="wsl"></a>WSL
* マスター pty エンドポイント [GH 2552] 上の TCSETSF と TCSETSW をサポートします。
* 同時の相互運用プロセスの開始と、EINVAL [GH 2813] が発生することができます。
* メモリ stat に適切なトレースの状態を表示する PTRACE_ATTACH を修正します。
* CLEARTID と SETTID の両方のフラグでの有効期間が短いプロセスの複製、修正プログラムの競合はでした TID アドレスをクリアせずに終了します。
* Pre 17093 ビルドから移動するときに、Linux ファイル システムのディレクトリをアップグレードする場合は、メッセージを表示します。 17093 ファイル システムの変更の詳細については、のリリース ノートを参照してください。 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)します。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17101"></a>ビルド 17101
一般的な Windows ビルド 17101 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)します。

### <a name="wsl"></a>WSL
* Signalfd をサポートします。 [GH 129]
* ファイル名がプライベートの Unicode 文字としてエンコードすることによって、NTFS の無効な文字を含むをサポートします。 [GH 1514]
* 書き込みがサポートされていない場合、自動マウントは読み取り専用にフォールバックが。 [GH 2603]
* (絵文字の文字) などの Unicode サロゲート ペアの貼り付けを許可します。 [GH 2765]
* 擬似/proc と/sys が読み取りを返すし、select、ポーリング、epoll、副次的 [GH 2838] からの準備完了の書き込み
* レジストリが改ざんされてまたは破損するいると、無限ループに移動するサービスを引き起こす可能性のある問題を解決します。
* Iproute2 の新しい (4.14 アップ ストリーム) バージョンを使用する netlink メッセージを修正します。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17093"></a>ビルド 17093
一般的な Windows ビルド 17093 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)します。

#### <a name="important"></a>重要:
このビルドにアップグレードした後初めて WSL を開始するときに、Linux ファイル システムのディレクトリをアップグレードする作業の実行が必要です。 緩やかに変化を開始する WSL が表示されるようには、数分にかかるこの可能性があります。 これは、ストアからインストールする各配布とにのみ発生する必要があります。
* DrvFs での大文字小文字の区別のサポートが向上しました。
    * DrvFs は、ディレクトリあたり大文字小文字の区別をサポートします。 これは、新しいフラグ設定可能なディレクトリをそれらのディレクトリ内のすべての操作を扱う必要があるかを示すで小文字の区別、でも Windows アプリケーション大文字と小文字が異なるだけファイルを正しく開くことができます。
    * DrvFs がディレクトリ単位ごとに大文字小文字の区別を制御する新しいマウント オプション
        * ケース force =: すべてのディレクトリは小文字の区別 (ドライブのルート) を除くに扱われます。 WSL で作成された新しいディレクトリは、大文字小文字が区別としてマークされます。 これは、新しいディレクトリの大文字と小文字をマークすることを除く、従来の動作です。
        * ケース = dir: ディレクトリあたり大文字小文字の区別フラグを使用してディレクトリだけを小文字の区別; に扱われますその他のディレクトリは、大文字と小文字を区別しません。 WSL で作成された新しいディレクトリは、大文字小文字が区別としてマークされます。
        * ケース = オフ: ディレクトリあたり大文字小文字の区別フラグを使用してディレクトリだけを小文字の区別; に扱われますその他のディレクトリは、大文字と小文字を区別しません。 WSL で作成された新しいディレクトリは、大文字と小文字を区別しないとしてマークされます。
    * 注: 以前のリリースで WSL で作成されたディレクトリがないこのフラグが設定されるのでは扱われません小文字の区別を使用する場合、"ケース dir ="オプション。 既存のディレクトリにこのフラグを設定する方法は近日公開予定。
    * これらのオプションを使用してマウントの例 (既存のドライブをする必要がありますまずマウントを解除する前に、さまざまなオプションをマウントすることができます): sudo mount-t drvfs c:、/mnt/retention/o c ケース dir を =
    * ここでは、ケース = 強制は、既定のオプション。 これは、ケースに変更、将来 dir を = です。
* 例: DrvFs をマウントする際に Windows パスにスラッシュに使用することようになりましたことができます: sudo-t drvfs//server/share/mnt/share をマウントします。
* WSL は、今すぐ [GH 2636] インスタンスの起動中に、/etc/fstab ファイルを処理します。
    * これは自動的に DrvFs ドライブをマウントする前に行われますfstab によって既にマウントされていたすべてのドライブはいない再マウントする、自動的に特定のドライブのマウント ポイントを変更することができます。
    * この動作は wsl.conf を使用してオフにすることができます。
* /Proc でマウント、mountinfo mountstats ファイルは、バック スラッシュとスペース [GH 2799] などの特殊文字を正しくエスケープします。
* メタデータが有効にした場合、WSL シンボリック リンク、または fifo ソケットなど DrvFs で作成された特別なファイルのコピーし、Windows 間で移動ようになりましたことができます。

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL は wsl.conf でさらに構成できます。
サブシステムを起動するたびに適用される WSL で自動的に特定の機能を構成するためのメソッドを追加しました。 これには、自動マウント オプションおよびネットワークの構成が含まれます。 こちらのブログでの詳細については、について説明します。 https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX は、WSL 上の Linux プロセスと Windows のネイティブ プロセスの間のソケット接続を許可します。
WSL および Windows アプリケーションは、Unix ソケット上で互いと通信ようになりましたできます。 Windows でサービスを実行して、Windows と WSL の両方のアプリで使用できるようにする場合を考えます。 ここで、Unix ソケットでできることです。 読み取りでの詳細は私たちのブログ投稿 https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Mmap() MAP_NORESERVE [GH 121、2784] でのサポートします。
* CLONE_PTRACE と CLONE_UNTRACED [2781 GH 121、] をサポートします。
* [GH 121、2781] の複製で SIGCHLD 非終了のシグナルを処理します。
* スタブ/proc/sys/fs/inotify/max_user_instances と/proc/sys/fs/inotify/max_user_watches [GH 1705]
* [GH 1884] の非ゼロ オフセットを持つロード ヘッダーを含む ELF バイナリの読み込みエラー
* イメージの読み込み時に末尾のページのバイトをゼロにします。
* Execve プロセスが終了するサイレント モードでのケースを削減します。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17083"></a>ビルド 17083
一般的な Windows ビルド 17083 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)します。

### <a name="wsl"></a>WSL
* Epoll [GH 2798、2801 を報告しました 2857] に関連する固定のバグチェック
* ASLR [GH 1185、2870] をオフにするときに固定がハングします。
* Mmap 操作にアトミック [GH 2732] が表示されることを確認します。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17074"></a>ビルド 17074
一般的な Windows ビルド 17074 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)します。

### <a name="wsl"></a>WSL
* 固定のストレージ形式の DrvFs メタデータ [GH 2777] </br>
概要DrvFs メタデータがこのビルドは表示が正しくないかまったくない前に作成します。 影響を受けるファイルを修正するのにには、メタデータを再適用するのに chmod、chown を使用します。
* 複数の信号と再開可能な syscall で問題を修正しました。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17063"></a>ビルド 17063
一般的な Windows ビルド 17063 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)します。

### <a name="wsl"></a>WSL
* DrvFs には、Linux の追加のメタデータがサポートされています。 これにより、所有者と chmod/chown とも fifo、unix ソケット デバイス ファイルなどの特殊なファイルの作成を使用してファイルのモードを設定できます。 これは既定で無効にここではまだ実験段階であるためです。
**注:** DrvFs で使用されるメタデータ形式でバグを修正しました。 メタデータの実験用には、このビルドで動作しますが、将来のビルドのこのビルドによって作成されたメタデータが正しく読み取られない。  手動で変更されたファイルの所有者を更新する必要があり、カスタム デバイス ID を持つデバイスが再作成する必要があります。

  メタデータのオプションを使用してマウント DrvFs を有効にする (既存のマウントを有効にするにする必要がありますまずマウントを解除できます)。

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux のアクセス許可は、追加のメタデータとしては、ファイルに追加されます。Windows のアクセス許可には影響しません。  メタデータを削除 Windows エディターを使用してファイルを編集することがありますに注意してください。 この場合、ファイルは、その既定のアクセス許可に戻されます。

* メタデータなしのコントロール ファイルに追加されたマウント オプション DrvFs。
  * uid: すべてのファイルの所有者を使用するユーザーの ID。
  * gid: すべてのファイルの所有者のためのグループ ID。
  * umask: すべてのファイルとディレクトリを除外するアクセス許可の 8 進数のマスク。
  * fmask: すべての定期的なファイルを除外するアクセス許可の 8 進数のマスク。
  * dmask: すべてのディレクトリを除外するアクセス許可の 8 進数のマスク。

  次に、例を示します。
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  メタデータのないファイルの既定のアクセス許可を指定するメタデータのオプションとの組み合わせ。

* 新しい環境変数を導入`WSLENV`WSL と Win32 の間の環境変数のフローを構成する。

  次に、例を示します。

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` 環境変数 Win32 から WSL プロセスまたは WSL から Win32 プロセスを起動するときに含めることができるコロンで区切られた一覧を示します。  各変数は、次の後が変換される方法を指定するフラグのスラッシュに付けることができます。
  * p:値は、Win32 のパスと WSL パスの間を変換するパスです。
  * L:値は、パスの一覧です。 WSL、コロンで区切られたリストを勧めします。 Win32 では、セミコロン区切りのリストを勧めします。
  * u:値は、必ず含まれる Win32 の WSL を呼び出すときに
  * 属性:値は、必ず含まれる WSL から Win32 を呼び出すときに

  設定できる`WSLENV`.bashrc や、ユーザーのカスタムの Windows 環境でします。

* drvfs マウントは、tar からのタイムスタンプを正しく保持 cp-p (GH 1939)
* drvfs シンボリック リンク レポートの適切なサイズ (GH 2641)
* 読み取り/書き込みの IO サイズが非常に大きな (GH 2653) のしくみ
* プロセス グループ Id (GH 2534) で未定義の動作します。
* 大規模な予約のリージョンの強化された mmap パフォーマンスが大幅にghc (GH 1671) のパフォーマンスが向上します。
* READ_IMPLIES_EXEC; のパーソナリティのサポート最大値および clisp (GH 1185) を修正します。
* mprotect PROT_GROWSDOWN; をサポートしています修正 clisp (GH 1128)
* オーバー コミット モードをページ フォールトを修正修正 sbcl (GH 1128)
* 複製は、複数のフラグの組み合わせをサポートしています
* 選択/epoll epoll ファイル (以前れません) をサポートします。
* 実装されていない syscall の ptrace を通知します。
* Resolv.conf nameservers [GH 2694] を生成するときのないインターフェイスを無視します。
* 物理アドレスなしのネットワーク インターフェイスを列挙します。 [GH 2685]
* 追加のバグ修正と機能強化。

### <a name="linux-tools-available-to-developers-on-windows"></a>Windows 上の開発者が利用できる Linux ツール

* Windows コマンド ライン ツール チェーンと curl の多く (tar) が含まれています。
  読み取り[このブログ](https://aka.ms/tarcurlwindows)をこれら 2 つの新しいツールの追加の詳細を学習し、Windows での開発者エクスペリエンスを形成している方法を参照してください。

*   `AF_UNIX` Windows Insider SDK (17061 +) で使用できます。
  読み取り[このブログ](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)について`AF_UNIX`および Windows の開発者が使用できる方法です。

### <a name="console"></a>Console
* バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。


## <a name="build-17046"></a>ビルド 17046

一般的な Windows ビルド 17046 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)します。

### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- アクティブなターミナルをせずに実行するプロセスを許可します。 [GH 709、1007、1511、2252、2391、et al]。
- CLONE_VFORK といなくて向上をサポートします。 [GH 1878、2615]
- WSL がネットワーク操作に TDI フィルター ドライバーをスキップします。 [GH 1554]
- DrvFs は、特定の条件が満たされたときに、NT シンボリック リンクを作成します。 [GH 353、1475、2602]
    - リンク先は相対である必要があります、マウント ポイントやシンボリック リンクを越える必要がありますいないや、存在する必要があります。
    - ユーザー必要があります (通常必要 wsl.exe 管理者特権でを起動すること) SE_CREATE_SYMBOLIC_LINK_PRIVILEGE、開発者モードがオンになっている場合を除き、します。
    - その他のすべての状況で DrvFs はまだ WSL シンボリック リンクを作成します。
- 管理者特権と、管理者特権以外の WSL インスタンスを同時に実行を許可します。
- /Proc/sys/kernel/yama/ptrace_scope をサポートします。
- WSL <> - Windows パスの変換を実行する wslpath を追加します。 [GH 522、1243、1834、2327、et al]。
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- バグ修正。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。


## <a name="build-17040"></a>ビルド 17040

一般的な Windows ビルド 17040 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 17035 以降の修正プログラムがありません。

#### <a name="console"></a>Console
- 17035 以降の修正プログラムがありません。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17035"></a>ビルド 17035

一般的な Windows ビルド 17035 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- DrvFs ファイルへのアクセスによって変更できる場合によっては失敗します。 [GH 2448]

#### <a name="console"></a>Console
- VT モード内の行の挿入/削除するときに色の一部が失われる。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17025"></a>ビルド 17025

一般的な Windows ビルド 17025 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 新しいフォア グラウンド プロセス グループ [GH 1653、2510] 内には、初期のプロセスを開始します。
- SIGHUP 配信では、[GH 2496] を修正します。
- [GH 2497] 何もない場合は、既定の仮想のブリッジの名前を生成します。
- /Proc/sys/kernel/random/boot_id [GH 2518] を実装します。
- 複数の相互運用機能の stdout と stderr のパイプを修正します。
- Syncfs システム コールをスタブします。

#### <a name="console"></a>Console
- サード パーティ製コンソール [GH 111] の入力の VT 翻訳を修正します。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="build-17017"></a>ビルド 17017

一般的な Windows ビルド 17017 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 空の [GH 330] ELF プログラム ヘッダーを無視します。
- 非対話型ユーザー用の WSL インスタンスを作成する LxssManager を許可する (ssh およびスケジュール タスクのサポート) [GH 777、1602]。
- サポート WSL Win32]-> [WSL (「開始」) のシナリオ [GH 1228]-> [です。
- [GH 1614] 相互運用機能を介して呼び出すコンソール アプリの終了の制限付きのサポート。
- Devpts [GH 1948] のマウント オプションをサポートします。
- Ptrace 子 [GH 2333] の起動をブロックします。
- EPOLLET [GH 2462] の一部のイベントがありません。
- PTRACE_GETSIGINFO 用のデータを返します。
- Lseek で Getdents には、正しくない結果が得られます。
- データがなくなったをパイプで入力を待機しているいくつかの Win32 相互運用機能アプリ ハングを修正します。
- Tty/pty ファイルの指定をサポートします。
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- コンソールには、このリリースで変更が関連付けられていません。

### <a name="ltp-results"></a>成る結果:
進行中のテスト。

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>ビルド 16288

一般的な Windows ビルド 16288 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 正しく初期化し、uid や gid、ソケット ファイル記述子の設定 [GH 2490] モードのレポート
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- コンソールには、このリリースで変更が関連付けられていません。

### <a name="ltp-results"></a>成る結果:
16273 以降変更なし

## <a name="build-16278"></a>ビルド 16278

一般的な Windows ビルド 162738 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- LX MM 状態 [GH 2415] 解除を行うときにバックアップ ファイルのセクションのマップ ビューを明示的にマップ解除します。
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- コンソールには、このリリースで変更が関連付けられていません。

### <a name="ltp-results"></a>成る結果:
16273 以降変更なし

## <a name="build-16275"></a>ビルド 16275

一般的な Windows ビルド 162735 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- このリリースで変更に関連付けられた WSL がありません。

#### <a name="console"></a>Console
- コンソールには、このリリースで変更が関連付けられていません。

### <a name="ltp-results"></a>成る結果:
16273 以降変更なし

## <a name="build-16273"></a>ビルド 16273

一般的な Windows ビルド 16273 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- DrvFs ディレクトリ [GH 2392] の正しくないファイルの種類が報告されることが問題を修正しました
- その使用 uevent プログラムのブロックを解除する NETLINK_KOBJECT_UEVENT ソケットの作成を許可する [GH 1121、2293、2242、2295、2235、648、637]
- 接続の非ブロッキングのサポートを追加 [GH 903、1391、1584、1585、1829、2290、2314]
- 実装 CLONE_FS 複製システム呼び出しフラグ [GH 2242]
- タブまたは NT の相互運用 [GH 1625、2164] で正しく引用符を処理しないに関する問題を修正します。
- 解決するには再 WSL を起動しようとするときにエラー [GH 651、2095] のインスタンスにアクセスが拒否されました
- Futex FUTEX_REQUEUE および FUTEX_CMP_REQUEUE 操作 [GH 2242] 実装します。
- さまざまな SysFs ファイル [GH 2214] のアクセス許可を修正します。
- [GH 2290] のセットアップ中に Haskell スタックのハングを修正します。
- Binfmt_misc 'C' の実装 'o' と 'P' フラグ [GH 2103]
- Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]
- Ioprio_set システム コール [GH 498] の部分的なサポートを追加します。
- スタブ SO_REUSEPORT SO_PASSCRED netlink ソケット [GH 69] のサポートを追加 (&)
- 現在、配布の場合、RegisterDistribuiton から別のエラー コードを返すインストールまたはアンインストールします。
- 部分的にインストールされている WSL ディストリビューション wslconfig.exe 経由での登録解除を許可します。
- Udp::msg_peek から python ソケット テスト ハングを修正します。
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- コンソールには、このリリースで変更が関連付けられていません。

### <a name="ltp-results"></a>成る結果:
合計テスト数:1904<br/>
合計には、テストがスキップされました。209<br/>
失敗の総数:229<br/>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>ビルド 16257

一般的な Windows ビルド 16257 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- Prlimit64 システム コールを実装します。
- Ulimit n (setrlimit RLIMIT_NOFILE) のサポートを追加する [GH 1688]
- スタブ MSG_MORE TCP ソケット [GH 2351]
- 無効な AT_EXECFN 補助ベクター動作 [GH 2133] を修正します。
- コンソール/tty のコピー/貼り付けの動作を修正しより優れたいっぱいバッファー処理 [GH 2204、2131] の追加
- ユーザー ID の設定およびグループ ID の設定のプログラム [GH 2031] 補助のベクトル内の AT_SECURE を設定します。
- 擬似端末のマスター エンドポイント TIOCPGRP [GH 1063] は処理されません。
- 修正プログラム lseek が LxFs [GH から 2310] 内のディレクトリを巻き戻すには
- 多量の使用 [GH 1882] 後に/dev/ptmx をロックします。
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- 水平方向の線/アンダー スコア Everywhere [GH 2168] の修正
- 注文処理の変更 [GH 2170] を終了するは困難加えたら NPM 問題の修正します。
- この新しい配色を追加するには。 https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>成る結果:
16251 以降変更なし

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`prlimit64`<br/>

### <a name="known-issues"></a>既知の問題
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>GitHub 問題 2392:Windows フォルダーが WSL で認識されない.](https://github.com/Microsoft/BashOnWindows/issues/2392)
WSL が経由で Windows のファイル/フォルダーを列挙中に問題が 16257 のビルドで`/mnt/c/...`します。
この問題は修正されておりで解放する必要がある 2017 年 8 月 14 の開始週に Insider のビルドします。

<br/>

## <a name="build-16251"></a>ビルド 16251

一般的な Windows ビルド 16251 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- WSL オプションのコンポーネントからベータ版のタグを削除しを参照してください[ブログの投稿](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)詳細についてはします。
- 保存された一連の uid と gid の exec [GH 962、1415、2072] でユーザー ID の設定とグループ ID の設定のバイナリを正しく初期化します。
- Ptrace PTRACE_O_TRACEEXIT [GH 555] のサポートが追加されました
- Ptrace サポートが追加されました PTRACE_GETFPREGS と PTRACE_GETREGSET NT_FPREGSET [GH 555] で
- Ptrace を固定を停止する場合は無視信号
- 追加の機能強化とバグ修正

#### <a name="console"></a>Console
- コンソールには、このリリースで変更が関連付けられていません。

### <a name="ltp-results"></a>成る結果:
渡すテスト数:768</br>
失敗したテスト数:244</br>
スキップされたテスト数:96</br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>ビルド 16241

一般的な Windows ビルド 16241 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)します。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- このリリースで変更に関連付けられた WSL がありません。

#### <a name="console"></a>Console
- 報告されていた、交差行 DEC の正しくない文字を出力するための修正プログラム[ここ](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- コード ページ 65001 (utf8) に表示されている出力テキストの修正
- 選択の変更、パレットの他の部分を 1 つの色の RGB 値に加えられた変更を転送することはありません。 これにより、コンソールのプロパティ シートを使用して、はるかに簡単です。
- Ctrl キーを押しながら S キーが正常に動作する表示されません。
- されていない太字/-Dim 不在であれば完全に ANSI エスケープ コード [GH 2174] から
- コンソールで Vim の配色テーマ [GH 1706] を正しくサポートしません。
- 特定の文字 [GH 2149] に貼り付けることはできません。
- 折り返しのサイズ変更が編集/コマンド ライン [GH ConEmu 1123] 機能がある場合は、bash ウィンドウをサイズ変更と対話妙
- Ctrl キーを押し、-l まま画面ダーティ [GH 1978]
- HDPI [GH 1907] で VT を表示するときに、コンソール表示バグ
- Japansese 文字が Unicode 文字 U + 30FB は奇妙に見える [GH 2146]
- 追加の機能強化とバグ修正

</br>

## <a name="build-16237"></a>ビルド 16237

一般的な Windows ビルド 16237 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)します。<br/>


### <a name="fixed"></a>固定
- 既定の属性を使用して、EAs のない lxfs (ルート、ルート、0000) でのファイル
- 拡張属性の使用のディストリビューションのサポートが追加されました
- 埋め込み getdents と getdents64 で返されるエントリを修正
- Shmctl するシステム コール [GH 2068] のアクセス許可チェックを修正します。
- Tty [GH 2231] の状態は固定の正しくない初期 epoll
- [GH 2077] のすべてのエントリが返されない DrvFs readdir を修正します。
- 修正 LxFs readdir ファイルが [GH 2077] のリンクを解除
- リンクされていない drvfs ファイルの詳しい情報を再度開くを許可します。
- WSL 機能を無効にするためのグローバル レジストリ キーのオーバーライドを追加 (相互運用機能/ドライブのマウント)
- DrvFs (および LxFs)「状態」での不正なブロックの数の修正 [GH 1894]
- 追加の機能強化とバグ修正

</br>

## <a name="build-16232"></a>ビルド 16232

一般的な Windows ビルド 16232 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)します。<br/>


### <a name="fixed"></a>固定
- このリリースで変更に関連付けられた WSL がありません。

</br>

## <a name="build-16226"></a>ビルド 16226

一般的な Windows ビルド 16226 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)します。<br/>


### <a name="fixed"></a>固定
- xattr 関連の syscall のサポート (getxattr、setxattr、listxattr、removexattr)。
- security.capablity xattr サポートします。
- 特定のファイル システム フィルター、ミリ秒以外の SMB サーバーを含むと互換性の強化。 [GH #1952]
- 圧縮されたファイルを OneDrive のプレース ホルダー、GVFS のプレース ホルダー、およびコンパクトな OS のサポートを強化します。
- 追加の機能強化とバグ修正

</br>

## <a name="build-16215"></a>ビルド 16215

一般的な Windows ビルド 16215 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)します。<br/>


### <a name="fixed"></a>固定
- WSL では、開発者モードが必要がなくなります。
- Drvfs でディレクトリ ジャンクションをサポートします。
- WSL 配布 appx パッケージのアンインストールを処理します。
- プライベートの表示に詳しい情報の更新プログラムとのマッピングを共有します。
- 配布が部分的にインストールまたはアンインストールをクリーンアップする wslconfig.exe の機能を追加します。
- TCP ソケット IP_MTU_DISCOVER のサポートを追加しました。 [GH 1639、2115、2205]
- AF_INADDR へのルートのプロトコル ファミリを推論します。
- シリアル デバイスの機能強化 [GH 1929]。

</br>

## <a name="build-16199"></a>ビルド 16199

一般的な Windows ビルド 16199 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)します。<br/>


### <a name="fixed"></a>固定
- これらのリリースで変更に関連付けられた WSL がありません。

</br>

## <a name="build-16193"></a>ビルド 16193

一般的な Windows ビルド 16193 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)します。<br/>


### <a name="fixed"></a>固定
- 送信 SIGCONT と終了 [GH 1973] threadgroup 間で競合状態
- レポート FILE_DEVICE_CONSOLE [GH 1840] ではなく FILE_DEVICE_NAMED_PIPE に tty および pty デバイスを変更します。
- なる用の SSH の修正プログラム
- Init デーモンに DrvFs マウントを移動する [GH 1862、1968 年に、1767、1933]
- 次の NT シンボリック リンク DrvFs でサポートが追加されました。

</br>

## <a name="build-16184"></a>ビルド 16184

一般的な Windows ビルド 16184 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)します。<br/>


### <a name="fixed"></a>固定
- Removed apt package maintenance task (lxrun.exe /update)
- 表示されない node.js [GH 1840] で、Windows プロセスから出力を修正
- Lxcore [GH 1794] のアラインメント要件を緩和します。
- システム呼び出し数の AT_EMPTY_PATH フラグの処理を修正しました。
- ハンドルを開いた DrvFs ファイルを削除して未定義の動作 [GH 544,966,1357,1535,1615] ファイルとが、問題を修正しました
- /etc/ホストは Windows ホスト ファイル (%windir%\system32\drivers\etc\hosts) からエントリを継承ようになりました [GH 1495]

</br>

## <a name="build-16179"></a>ビルド 16179

一般的な Windows ビルド 16179 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)します。<br/>


### <a name="fixed"></a>固定
- WSL 変更はこの 1 週間です。

</br>

## <a name="build-16176"></a>ビルド 16176

一般的な Windows ビルド 16176 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)します。<br/>


### <a name="fixed"></a>固定

- [シリアル サポートを有効になっています。](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- IP ソケット オプションなる [GH 1116] が追加されました
- (ファイルのアップロードに nginx/PHP-FPM) 中の pwritev 関数の実装 [GH 1506]
- IP ソケット オプション IP_MULTICAST_IF & IPV6_MULTICAST_IF の追加 [GH 990]
- IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP ソケット オプションのサポート [GH 1678]
- アプリのノード、traceroute、dig、nslookup、ホストの IP (V6) _MTU ソケット オプションが追加されました
- IP ソケット オプション IPV6_UNICAST_HOPS が追加されました
- [ファイル システムの機能強化](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * UNC パスをマウントをします。
    * Drvfs で CDFS サポートを有効にします。
    * Drvfs でネットワーク ファイル システムのアクセス許可を正しく処理します。
    * Drvfs にリモート ドライブのサポートを追加します。
    * FAT を有効にする drvfs のサポート
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果
15042 以降変更なし

</br>

## <a name="build-16170"></a>ビルド 16170

一般的な Windows ビルド 16170 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)します。<br/>

新しいリリースしました[ブログの投稿](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)WSL をテストする取り組みについて説明します。

### <a name="fixed"></a>固定

- サポートのソケット オプション IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- PTRACE_OLDSETOPTIONS のサポートを追加します。 [GH 1692]
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果
15042 以降変更なし

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>ビルドを Windows 10 15046 Creators Update
これ以上の WSL 修正プログラムや Windows 10 Creators Update に含める予定されている機能があります。 WSL のリリース ノートは、次の主要な Windows 更新プログラムを対象とする追加機能を今後数週間で再開されます。 一般的な Windows ビルド 15046 と将来の詳細についてはリリースのアクセス、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)します。 <br/><br/>
 <br/>

## <a name="build-15042"></a>ビルド 15042

一般的な Windows ビルド 15042 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)します。<br/>


### <a name="fixed"></a>固定

- 終わるパスを削除するときに、デッドロックの解決"..."
- 問題を修正しました、FIONBIO [GH 1683] 成功した場合に 0 が返されない
- Inet データグラム ソケットの長さが 0 の読み取りで問題を修正しました
- Drvfs inode 参照 [GH 1675] 内での競合状態が原因でデッドロックが発生を修正します。
- Unix ソケット補助的なデータの拡張サポートSCM_CREDENTIALS と SCM_RIGHTS [GH 514、613、1326]
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:737</br>
不合格数 (失敗、スキップされたなど.)。255

</br>

## <a name="build-15031"></a>ビルド 15031

一般的な Windows ビルド 15031 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)します。<br/>


### <a name="fixed"></a>固定

- Time(2) が誤動作が散発的バグを修正しました。
- 修正され、発行場所 * syscall を組み合わせて使用される信号のマスクが破損する可能性があります。
- WSL プロセスの作成の通知では、完全なコマンドラインの長さを返すようになりました。 [GH 1632]
- WSL は、今すぐ ptrace を GDB がハングすることによってスレッドの終了を報告します。 [GH 1196]
- 負荷の高い tmux IO 後 pty がハング、バグを修正しました。 [GH 1358]
- 多くのシステム コール (futex、semtimedop、参照のこと、sigtimedwait、itimer、timer_create) での固定のタイムアウトの検証
- 追加された eventfd EFD_SEMAPHORE サポート [GH 452]
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:737</br>
不合格数 (失敗、スキップされたなど.)。255 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>ビルド 15025

一般的な Windows ビルド 15025 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)します。<br/>


### <a name="fixed"></a>固定

- その壊れて grep 2.27 [GH 1578] バグの修正します。
- 実装された EFD_SEMAPHORE フラグ eventfd2 syscall [GH 452]
- /Proc/[pid]/net ipv6_route の実装 [GH 1608]
- シグナル ドリブン unix ストリーム ソケット [GH 393、68] の IO のサポート
- F_GETPIPE_SZ と F_SETPIPE_SZ [GH 1012] サポートします。
- Recvmmsg() syscall [GH 1531] の実装します。
- Epoll_wait() でした [GH 1609] を待っているバグを修正しました
- /Proc/version_signature を実装します。
- Tee syscall はエラーを両方のファイル記述子が同じパイプを参照している場合に返すようになりました
- Unix ソケット SO_PEERCRED に実装されている適切な動作
- 固定 tkill syscall 無効なパラメーターの処理
- Drvfs の preformace の増加への変更
- Ruby の IO のブロックの軽微な修正
- 固定の recvmsg() MSG_DONTWAIT フラグ inet ソケット [GH 1296] の EINVAL を返す
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:732</br>
不合格数 (失敗、スキップされたなど.)。255 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>ビルド 15019

一般的な Windows ビルド 15019 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)します。<br/>


### <a name="fixed"></a>固定

- CPU 使用率を正しく報告されるバグを修正したければ (945、971 は GH 823) などのツールの詳しい情報
- 既存の O_TRUNC で open() の呼び出し時にファイル inotify ようになりました IN_OPEN 前に、IN_MODIFY が生成されます。
- Unix ソケット getsockopt SO_ERROR postgress [GH 61、1354] を有効にするための修正します。
- GO 言語の実装の説明が
- Apt get パッケージ更新プログラムのバック グラウンド タスク今すぐ表示せずに実行ビューから
- Ipv6 localhost (Spring-Framework(Java) 失敗) のスコープをクリアします。
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:714 </br>
不合格数 (失敗、スキップされたなど.)。249 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>ビルド 15014

一般的な Windows ビルド 15014 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)します。<br/>


### <a name="fixed"></a>固定

- 意図したようになりました Ctrl + C
- たければと ps auxw ここで表示する適切なリソース使用率 (GH #516)
- NT 例外シグナルの基本的な変換です。 (GH #513)
- EINVAL (GH #1571) ではなく容量が不足した場合、この fallocate は、今すぐ ENOSPC で失敗しました。
- 追加された/proc/sys/kernel/sem します。
- 実装された semop と semtimedop システム コール
- IP_RECVTOS & IPV6_RECVTCLASS ソケット オプション (GH 69) を使用して固定 nslookup のエラー
- IP_RECVTTL と IPV6_RECVHOPLIMIT ソケット オプションのサポート
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:709 </br>
不合格数 (失敗、スキップされたなど.)。255 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall の概要
合計 Syscall:384 </br>
実装の合計:235 </br>
スタブの合計:22 </br>
合計が実装されていません。127 </br>
[詳細な内訳](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>ビルド 15007

一般的な Windows ビルド 15007 に関する情報を参照してください、 [Windows ブログ]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)します。<br/>


### <a name="known-issue"></a>既知の問題

- コンソールがいくつかの ctrl キーを認識しない既知のバグがある +<key>入力します。  これには、標準の 'c' keypress として機能するを ctrl キーを押しながら c コマンドが含まれます。

  - 対応策 :代替キーを Ctrl キーを押しながら C キーにマップします。 たとえば、マップに Ctrl + C には、Ctrl + K は:`stty intr \^k`します。  このマッピングは、ターミナルごとおよび実行する必要があります*すべて*時間 bash を起動します。 ユーザーを含めるには、このオプションを調べることができます、 `.bashrc`

### <a name="fixed"></a>固定

- WSL を実行して、CPU コアの 100% を消費は、問題を修正しました
- ソケットのオプション、IP_PKTINFO IPV6_RECVPKTINFO のようになりました。 (987 GH # の 851)
- Truncate lxcore 16 バイトにネットワーク インターフェイスの物理アドレス (GH #1452、1414、1343、468、308)
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:709 </br>
不合格数 (失敗、スキップされたなど.)。255 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>ビルド 15002

一般的な Windows ビルド 15002 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)します。<br/>


### <a name="known-issue"></a>既知の問題

2 つの既知の問題:
- コンソールがいくつかの ctrl キーを認識しない既知のバグがある +<key>入力します。  これには、標準の 'c' keypress として機能するを ctrl キーを押しながら c コマンドが含まれます。

  - 対応策 :代替キーを Ctrl キーを押しながら C キーにマップします。 たとえば、マップに Ctrl + C には、Ctrl + K は:`stty intr \^k`します。  このマッピングは、ターミナルごとおよび実行する必要があります*すべて*時間 bash を起動します。 ユーザーを含めるには、このオプションを調べることができます、 `.bashrc`

- WSL の実行中にシステム スレッドは CPU コアの 100% を消費します。  根本原因はアドレス指定され、内部的に固定します。

### <a name="fixed"></a>固定

- すべての bash セッションを同じアクセス許可レベルで作成されましたする必要があります。  さまざまなレベルでセッションを開始しようとしてがブロックされます。  つまり、管理者と管理者以外のコンソールを同時に実行できません。 (GH #626)
<br/>
- 次の NETLINK_ROUTE メッセージを実装 (Windows の管理者権限が必要)
     - RTM_NEWADDR (サポート`ip addr add`)
     - RTM_NEWROUTE (サポート`ip route add`)
     - RTM_DELADDR (サポート`ip addr del`)
     - RTM_DELROUTE (サポート`ip route del`)
- スケジュールされたタスクがパッケージを更新するためのチェックは、従量制課金接続 (GH #1371) では実行されなく
- パイプの取得が詰まっているつまり bash-c エラーを修正しました"ls alR/"|bash-c"cat"(GH #1214)
- 実装された TCP_KEEPCNT ソケット オプション (GH #843)
- 実装された IP_MTU_DISCOVER INET ソケット オプション (GH #720、717, 170, 69)
- NT パス参照を init から NT バイナリを実行する従来の機能を削除します。 (GH #1325)
- 開発/グループ/その他の読み取りアクセス (0644) (GH #1321) を許可する kmsg のモードを修正します。
- 実装された/proc/sys/kernel/random/uuid (GH #1092)
- プロセスの開始時刻が年 2432 (GH #974) を示すエラーを修正しました
- スイッチの既定環境変数を TERM xterm 256color (GH #1446) を
- 変更のコミットを処理する方法は、プロセスの分岐の中に計算されます。 (GH #1286)
- 実装された受け取る可能性があります。 (GH #1286)
- 実装された/proc/net/route ファイル (GH #69)
- ショートカット名がない正しくエラーを修正しました (GH #696) のローカライズ
- プログラムのヘッダーが正しく検証ロジックを解析する固定 elf 必要があります (以下に) 設定される。 します。 (GH #1048)
- 詳しい情報、sysfs、cgroupfs、および binfmtfs (GH #1378) 実装 statfs コールバック
- (GH #1184 も GH #1193 で説明) を閉じない固定の AptPackageIndexUpdate windows
- ASLR パーソナリティ ADDR_NO_RANDOMIZE サポートを追加します。 (GH #1148、1128)
- 強化された PTRACE_GETSIGINFO、AV (GH #875) 中に適切な gdb スタック トレースの SIGSEGV
- Patchelf バイナリ elf が不要になった解析が失敗します。 (GH #471)
- /Etc/resolv.conf (GH #416、1350) に VPN DNS が反映されます。
- TCP の機能強化より信頼性の高いデータの転送を閉じます。 (GH #610 616、1025、1335)
- 適切なエラーを返すようになりましたコード ファイルが多すぎる場合に、(EMFILE) が開かれます。 (GH #1126、2090)
- Windows の監査ログから報告プロセスで、イメージの名前は、監査を作成します。
- Bash ウィンドウ内から bash.exe を起動するときに正常に失敗します。
- 相互運用機能と、追加のエラー メッセージが LxFs (つまり notepad.exe .bashrc) の下の作業ディレクトリにアクセスできません。
- Windows のパスが WSL で切り捨てられました問題を修正しました
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:690 </br>
不合格数 (失敗、スキップされたなど.)。274 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>ビルド 14986

一般的な Windows ビルド 14986 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)します。<br/>


### <a name="fixed"></a>固定

- 固定のバグチェック Netlink と Pty Ioctl
- カーネルのバージョンが現在 4.4.0-43 Xenial との整合性を報告します。
- Bash.exe は入力の指示を起動 ' nul:' (GH #1259)
- 詳しい情報 (GH # の 967) で、スレッド Id を正しく今すぐ報告
- IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |IN_ISDIR フラグが inotify_add_watch() (GH #1280) でサポートされています
- 実装 timer_create と関連するシステムの呼び出し。  これにより、GHC サポート (GH #307)
- Ping が 0.000ms (GH #1296) の時刻を返す問題を修正しました
- ファイルが多すぎますが開かれたときに、適切なエラー コードを返します。
- WSL で Netlink の要求のネットワーク インターフェイスのデータは失敗によって変更できるインターフェイスのハードウェアのアドレスが 32 バイト (など、Teredo インターフェイス) の場合の問題を修正しました
   - Linux"ip"ユーティリティが WSL が 32 バイトのハードウェアのアドレスを報告する場合、クラッシュがバグを含むことに注意してください。 これは、"ip"、WSL ではないのバグです。 ハードウェアのアドレスを印刷する、"ip"ユーティリティ ハードコード化文字列バッファーの長さが使用し、そのバッファーが小さすぎる 32 バイトのハードウェアのアドレスを印刷します。
- 追加の修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:669 </br>
不合格数 (失敗、スキップされたなど.)。258 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>ビルド 14971

一般的な Windows ビルド 14971 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)します。<br/>


### <a name="fixed"></a>固定

 - コントロールが及ばないのための更新はありません Windows Subsystem for Linux のビルドでします。  次回のリリースでは、定期的にスケジュールされた更新プログラムが再開されます。

### <a name="ltp-results"></a>成る結果:
14965 から変更されていません </br>
テストの成功の数:664 </br>
不合格数 (失敗、スキップされたなど.)。263 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>ビルド 14965

一般的な Windows ビルド 14965 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)します。<br/>


### <a name="fixed"></a>固定

- Netlink のサポートはソケット NETLINK_ROUTE プロトコルの RTM_GETLINK と RTM_GETADDR (GH #468)
  - により、ネットワークの列挙体のコマンドを示している ifconfig と ip
  - 詳細についてを参照、 [WSL ネットワー キング ブログの投稿](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)します。

- /sbin が既定では、ユーザーの path に追加
- NT ユーザー パスのようになりました (つまりここで入力できます notepad.exe System32 を Linux パスに追加せずに) 既定で WSL パスに追加
- /Proc/sys/kernel/cap_last_cap サポートが追加されました
- 現在の作業ディレクトリには、ansi 以外の文字 (GH #1254) が含まれている場合は NT バイナリ WSL から起動することはようになりました
- 切断された unix ストリーム ソケットのシャット ダウンを許可します。
- PR_GET_PDEATHSIG サポートが追加されました。
- あるサポートが追加されました
- パイプの取得が詰まっているつまり bash-c エラーを修正しました"ls alR/"|bash-c"cat"(GH #1214)
- 現在のターミナルに接続する要求の処理。
- /Proc/のマーク<pid>/oom_score_adj を書き込み可能です。
- /Sys/fs/cgroup フォルダーを追加します。
- sched_setaffinity 関係ビット マスクの数を返す必要があります。
- インタープリターのパスより小さい 64 文字を指定する必要がありますと誤った前提を ELF 検証ロジックを修正します。 (GH #743)
- 開いているファイル記述子は、コンソール ウィンドウを開いて (GH #1187) を保持できます。
- 末尾にスラッシュをターゲットの名前 (GH #1008) rename() が失敗しました Fixeed エラー
- /Proc/net/dev ファイルを実装します。
- 固定 0.000ms タイマーの解決のために ping を実行します。
- 実装された/proc/self/environ (GH #730)
- 追加のバグ修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:664 </br>
不合格数 (失敗、スキップされたなど.)。263 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>ビルド 14959

一般的な Windows ビルド 14959 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)します。<br/>


### <a name="fixed"></a>固定

- Windows の Pico プロセス通知機能強化。  詳細情報について、 [WSL ブログ](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)します。
- Windows の相互運用性と安定性の向上
- 0x80070057 エンタープライズ データ保護 (EDP) を有効にすると、bash.exe を起動するときにエラーを修正しました
- 追加のバグ修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:665 </br>
不合格数 (失敗、スキップされたなど.)。263 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>ビルド 14955

一般的な Windows ビルド 14955 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)します。<br/>


### <a name="fixed"></a>固定

 - コントロールが及ばないのための更新はありません Windows Subsystem for Linux のビルドでします。  次回のリリースでは、定期的にスケジュールされた更新プログラムが再開されます。

### <a name="ltp-results"></a>成る結果:
テストの成功の数:665 </br>
不合格数 (失敗、スキップされたなど.)。263 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>ビルド 14951

一般的な Windows ビルド 14951 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)します。<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>新機能:Windows または Ubuntu の相互運用性
WSL のコマンドラインから直接 Windows バイナリを呼び出すようになりましたことができます。  これにより、ユーザーは、Windows 環境と考えられるされていない方法でシステムとやり取りできるようにします。  簡単な例として、次のコマンドを実行することはようになりました。

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

詳細についてにあります。

- [WSL の相互運用機能チームのブログ](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [相互運用機能の MSDN ドキュメント](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>固定

- WSL のすべての新しいインスタンスを Ubuntu 16.04 (Xenial) がインストールされているようになりました。  14.04 (頼りになる) の既存のインスタンスを持つユーザーは自動的にアップグレードされません。
- インストール中に設定されたロケールが表示されるようになりました
- バグが常にではありませんが、WSL プロセスをファイルにリダイレクトする場所のターミナル強化機能します。
- コンソールの有効期間は bash.exe 有効期間に関連付けられる必要があります。
- コンソール ウィンドウのサイズがバッファー サイズではなく、表示サイズを使用する必要があります。
- 追加のバグ修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:665 </br>
不合格数 (失敗、スキップされたなど.)。263 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>ビルド 14946

一般的な Windows ビルド 14946 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)します。<br/>


### <a name="fixed"></a>固定

- スペースや引用符が含まれている NT ユーザー名とユーザー用の WSL ユーザー アカウントの作成を妨げる問題を修正しました。 
- Stat でディレクトリのリンク数の場合は 0 を返すには、VolFs と DrvFs を変更します。
- IPV6_MULTICAST_HOPS ソケット オプションをサポートします。
- Tty あたりの I/O ループを 1 つのコンソールに制限されます。 例: 次のコマンドは、考えられる。
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- /proc/cpuinfo (GH #1115) にタブ スペースに置換します。
- Windows のマウントされたボリュームに一致する名前を持つ mountinfo に DrvFs が表示されます。
- /home と/root mountinfo 正しい名前で表示されます。
- 追加のバグ修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:665 </br>
不合格数 (失敗、スキップされたなど.)。263 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>ビルド 14942

一般的な Windows ビルド 14942 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/onefourninefourtwoooooo)します。<br/>


### <a name="fixed"></a>固定

- メモリを含む、"試行された実行の NOEXECUTE"SSH がブロックしてクラッシュのネットワークのアドレス指定、バグチェック数
- inotifiy サポート DrvFs 上の Windows アプリケーションから生成された通知がようになりました
- Mongod の TCP_KEEPIDLE と TCP_KEEPINTVL を実装します。 (GH #695)
- Pivot_root システム コールを実装します。
- SO_DONTROUTE のソケット オプションを実装します。
- 追加のバグ修正と機能強化


### <a name="ltp-results"></a>成る結果:
テストの成功の数:665 </br>
不合格数 (失敗、スキップされたなど.)。263 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>ビルド 14936

一般的な Windows ビルド 14936 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)します。<br/>


注:WSL では、Ubuntu バージョン 16.04 (Xenial) Ubuntu 14.04 (信頼性) ではなくを今後のリリースでインストールします。  この変更は、内部関係者が (lxrun.exe/install または bash.exe の最初の実行) の新しいインスタンスのインストールに適用されます。  信頼性と既存のインスタンスは自動的にアップグレードされません。 ユーザーは、do リリース-アップグレード コマンドを使用して Xenial に頼りになる、イメージをアップグレードできます。

### <a name="known-issue"></a>既知の問題
WSL でソケットの実装によって問題が発生します。  バグチェックでは、"試行された実行の NOEXECUTE MEMORY"のエラーでクラッシュとして出現します。  この問題の最も一般的な形では、ssh を使用する場合、クラッシュです。  根本原因は、内部のビルドでは固定され、内部関係者に、できるだけ早い機会にプッシュされます。

### <a name="fixed"></a>固定

- Chroot システム コールの実装
- Inotify 改善~~DrvFs 上の Windows アプリケーションから生成された通知のサポートを含む~~
  - 修正:Inotify は、この時点ではない Windows アプリケーションから送信された変更のサポートします。
- ソケットの IPV6 へのバインド::<port n> IPV6_V6ONLY ようになりました (GH #68、#157、#393、#460、#674、#740、#982、#996)
- Waitid systemcall の WNOWAIT 動作 (GH #638) を実装します。
- のでおよび IP_TTL IP ソケット オプションをサポートします。
- 長さ 0 の read() をすぐに返す必要があります (GH #975)
- .Tar ファイルで、NULL 終端文字が含まれていないファイル名とファイル名のプレフィックスを正しく処理します。
- /dev/null epoll のサポート
- /Dev/alarm タイム ソースを修正します。
- Bash-c をファイルにリダイレクトできるようになりました
- 追加のバグ修正と機能強化

### <a name="ltp-results"></a>成る結果:
テストの成功の数:664 </br>
不合格数 (失敗、スキップされたなど.)。264 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`chroot`<br/>
<br/>

## <a name="build-14931"></a>ビルド 14931

一般的な Windows ビルド 14931 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)します。<br/>


### <a name="fixed"></a>固定

 - コントロールが及ばないのための更新はありません Windows Subsystem for Linux のビルドでします。  次のリリースで定期的にスケジュールされた更新プログラムが再開されます。

<br/>

## <a name="build-14926"></a>ビルド 14926

一般的な Windows ビルド 14926 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)します。<br/>


### <a name="fixed"></a>固定

- Ping は管理者特権がないコンソール
- 現在サポートされても管理者特権のない Ping6
- WSL で変更されたファイルの Inotify サポート。 (GH #216)
  - サポートされているフラグ:
    - inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watch イベント:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch 属性:LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 出力を参照してください。LX_IN_ISDIR, LX_IN_IGNORED
  - 既知の問題:Windows アプリケーションからファイルを変更するすべてのイベントを生成しません
- Unix ソケットになりました SCM_CREDENTIALS

### <a name="ltp-results"></a>成る結果:
テストの成功の数:651 </br>
不合格数 (失敗、スキップされたなど.)。258 </br>
[成るテスト実行のログ](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>ビルド 14915

一般的な Windows ビルド 14915 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)します。<br/>


### <a name="fixed"></a>固定
-  Socketpair unix データグラム ソケット (GH #262)
- SO_REUSEADDR の Unix ソケットのサポート
- UNIX ソケット サポート:so_broadcast (GH #568)
- 型 (GH #758、#546) の Unix ソケットのサポート
- Unix データグラム ソケットの送信、受信、およびシャット ダウンのサポートの追加
- 非固定アドレスに無効な mmap パラメーターの検証のためのバグチェックを修正します。 (GH #847)
- 中断のサポート]、[ターミナル状態の再開
- TIOCPKT ioctl 画面ユーティリティ (GH #774) ブロックを解除するためのサポート
    - 既知の問題:関数キーが動作していません
- 解放されたメンバー 'ReaderReady' へのアクセスを LxpTimerFdWorkerRoutine (GH #814) を引き起こす可能性のある TimerFd するときの競合を修正しました
- Futex、アンケート、および同様の再開可能なシステムの呼び出しのサポートを有効にします。
- 追加されたバインド マウントのサポート
- マウントの名前空間のサポートの共有を解除します。
    - 既知の問題:新しいマウント名前空間を作成するときに`unshare(CLONE_NEWNS)`現在の作業ディレクトリは引き続き古い名前空間を指す
- 追加の機能強化とバグ修正

<br/>

## <a name="build-14905"></a>ビルド 14905

一般的な Windows ビルド 14905 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)します。<br/>


### <a name="fixed"></a>固定
- 呼び出しは今すぐ再起動可能なシステムには、(GH #349、GH #520) がサポートされています
- ディレクトリ]、[今すぐに運用を終了 (GH #650) へのシンボリック リンク
- /Dev/random の実装の RNDGETENTCNT ioctl
- /Proc/[pid] を実装/マウント、/proc/[pid]/mountinfo と/proc/[pid]/mountstats ファイル
- 追加のバグ修正と機能強化

</br>

## <a name="build-14901"></a>ビルド 14901
最初の内部関係者は、Windows 10 Anniversary Update のリリースの投稿に対してビルドします。

一般的な Windows ビルド 14901 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)します。<br/>


### <a name="fixed"></a>固定
- 末尾のスラッシュの問題を修正しました
    - などのコマンド`$ mv a/c/ a/b/`作業ようになりました
- Ubuntu のロケールは、Windows ロケールに設定する必要がある場合に要求をインストールするようになりました
- Ns フォルダーの詳しい情報のサポート
- マウントを追加し、tmpfs、詳しい情報と sysfs ファイル システムのマウントを解除
- [At] の 32 ビットの ABI 署名 mknod を修正します。
- Unix ソケットのディスパッチ モデルに移動
- INET ソケットの受信バッファー サイズ、setsockopt を使用して設定を適用する必要があります。
- 実装 MSG_CMSG_CLOEXEC unix ソケットの受信メッセージのフラグ
- Linux プロセス stdin と stdout パイプ リダイレクト (GH 2)
    - Cmd. で bash-c コマンドのパイプ処理では、します。  例: > dir |bash-c"grep foo"
- Bash は、複数のページファイル (GH #538、#358) をシステムにインストールするようになりましたことができます。
- INET ソケット バッファーの既定のサイズには、Ubuntu の既定の設定の一致する必要があります。
- Xattr syscall listxattr に揃える
- のみ SIOCGIFCONF から有効な IPv4 アドレスとのインターフェイスを返す
- Ptrace によって挿入されたときに既定のアクションを信号を修正します。
- implement /proc/sys/vm/min_free_kbytes
- Sigreturn でコンテキストを復元するときにコンピューター コンテキスト レジスタの値を使用します。
    - Java と javac に一部のユーザーの分岐がどこで問題が解決します。
- /Proc/sys/kernel/hostname を実装します。

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Windows 10 Anniversary Update に 14388 をビルドします。
一般的な Windows ビルド 14388 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/14388wip)します。 <br/>

### <a name="fixed"></a>固定
- 8/2 で、Windows 10 Anniversary Update の準備のための修正します。
  - WSL Anniversary update の詳細についてを参照できます、[ブログ](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>ビルド 14376
一般的な Windows ビルド 14376 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)します。 <br/>

### <a name="fixed"></a>固定
- Apt get が (GH #493) がハングするいくつかのインスタンスの削除
- 空のマウントが正しく処理されませんが、問題を修正しました
- 場所 ram ディスクがマウントされていない正しく問題を修正しました
- 変更の unix ソケットのフラグ (部分的な GH #451) をサポートするために受け入れ
- 固定の一般的なネットワーク関連のブルー スクリーン
- /Proc/[pid] にアクセスする場合は、ブルー スクリーンを固定/task (GH #523)
- 高の固定の CPU 使用率のいくつか pty シナリオ (GH #488、#504)
- 追加のバグ修正と機能強化

<br/>

## <a name="build-14371"></a>ビルド 14371
一般的な Windows ビルド 14371 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)します。 <br/>

### <a name="fixed"></a>固定
- Ptrace を使用する場合は、SIGCHLD wait() とタイミングの競合を修正しました
- パスは、末尾がある場合は、いくつかの動作を修正/(GH #432)
- 名前の変更/リンク解除の子に開いているハンドルのために失敗したと問題を修正しました
- 追加のバグ修正と機能強化

<br/>

## <a name="build-14366"></a>ビルド 14366
一般的な Windows ビルド 14366 に関する情報を参照してください、 [Windows ブログ](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)します。 <br/>

### <a name="fixed"></a>固定
- シンボリック リンクをファイルの作成を修正します。
-   追加された listxattr for Python (GH 385)
-   追加のバグ修正と機能強化

### <a name="syscall-support"></a>Syscall サポート
-   WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>ビルド 14361
一般的な Windows ビルド 14361 に情報を参照してください、 [Windows ブログ](https://aka.ms/wip14361)します。 <br/>

### <a name="fixed"></a>固定
- Windows 上の Ubuntu 上で Bash で実行する場合、DrvFs は大文字小文字が区別ようになりました。
  - ユーザーが case.txt とケース。TXT、/mnt/retention/c ドライブします。
  - 大文字小文字の区別は、Bash on Ubuntu on Windows 内でのみサポートされます。 NTFS の Bash の外側では、ファイルを正しく報告されますが、予期しない動作には、Windows からファイルとの対話が発生する場合。
  - 各ボリューム (つまり/mnt/c) のルートは大文字小文字を区別しません。
  - Windows でこれらのファイルの処理の詳細についてはあります[ここ](https://support.microsoft.com/en-us/kb/100625)します。
- Pty を大幅に強化/tty をサポートします。  TMUX などのアプリケーションがサポートされています (GH #40)
- ユーザー アカウントが常にではありません作成の固定のインストールの問題
- コマンド ライン arg 構造が非常に長い引数リストに最適化されています。 (GH #153)
- Read_only は、DrvFs からファイルを削除して chmod を行うようになりました
- ターミナルのハングが (GH #43) を切断するいくつかのインスタンスを修正しました
- chmod、chown tty を作業ようになりました
- 0.0.0.0 への接続を許可して:: localhost (GH #388) として
- Sendmsg/検知の IO ベクターの長さを処理するようになりました > 1 (部分的な GH #376)
- ユーザーできるようになりましたオプトアウトのホストの自動生成されたファイル (GH #398)
- 自動的にインストール (GH 11) 中に NT ロケールに Linux ロケールと一致します。
- /Proc/sys/vm/swappiness ファイル (GH #306) の追加
- strace が正しく終了ようになりました
- /Proc/self/fd (GH #222) を再度開くをパイプを許可します。
- %LOCALAPPDATA%\lxss DrvFs (GH #270) から下のディレクトリを非表示にします。
- Bash.exe の処理の改善 ~。  などのコマンド"bash ~-c %.*ls"(GH #467) をサポートするようになりました
- ソケットは epoll を通知するようになりました (GH #271) をシャット ダウン中に使用可能な読み取り
- lxrun/uninstall 的確ファイルとフォルダーを削除します。
- 修正された ps f (GH #246)
- X11 のサポート強化 xEmacs (GH #481) などのアプリ
- Ubuntu の既定の設定と get_rlimit syscall (GH #172、#258) にサイズを正しく報告を照合する最初のスレッドのスタック サイズを更新
- Pico プロセスのイメージ名 (例: 監査) 用のレポート機能の強化
- 実装された/proc/mountinfo df コマンド
- 子の名前のエラー コードのシンボリック リンクを修正しました。 そして。
- 追加の機能強化のバグ修正と機能強化

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>ビルド 14352
一般的な Windows ビルド 14352 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/wip14352)します。<br/>


### <a name="fixed"></a>固定
- 大きなファイルが非ダウンロード/正常に作成された問題を修正しました。  これは、npm その他のシナリオ (GH 3、GH #313) ブロックを解除する必要があります。
- ソケットのハングをいくつかのインスタンスの削除
- 一部の ptrace エラーを修正しました
- WSL が 255 文字より長いファイル名を許可すると問題を修正しました
- 英語以外の文字のサポート強化
- 現在の Windows タイム ゾーン データを追加し、既定値として設定
- 一意のデバイス id のそれぞれのマウント ポイント (jre の修正 – GH 番号 49)
- パスを格納している問題を修正"します"。 および"."
- Fifo サポートが追加されました (GH #71)
- Ubuntu のネイティブ形式を一致するように resolv.conf の更新の形式
- いくつかの詳しい情報のクリーンアップ
- 管理コンソール (GH #18) の ping を有効になっています。

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>ビルド 14342
一般的な Windows についてビルド 14342、 [Windows ブログ](https://aka.ms/wip14342)します。 <br/>

VolFs と DriveFs に関する情報が見つかりません、 [WSL ブログ](https://blogs.msdn.microsoft.com/wsl)します。 <br/>

### <a name="fixed"></a>固定
- Windows ユーザーは、ユーザー名に Unicode 文字がある場合に、インストールの問題を修正しました
- FAQ の apt-get と更新プログラムの udev 回避策が初回実行時の既定値によって提供されるようになりました
- DriveFs にシンボリック リンクを有効になっている (/mnt/<drive>) ディレクトリ
- シンボリック リンクが DriveFs と VolFs 間で作業するようになりました
- 解析の問題、アドレス指定された最上位レベル パス: %.*ls/期待どおりに、正しく動作/。
- DriveFs に npm をインストールし、-g オプションが有効になった
- PHP サーバーが起動できない問題を修正しました
- Ubuntu のネイティブに近い一致を $PATH などの最新の既定環境値
- Apt パッケージ キャッシュを更新する Windows で、毎週のメンテナンス タスクを追加
- ELF ヘッダーの検証で問題を修正しました、WSL なりました Melkor のすべてのオプション
- Zsh シェルが機能
- Go のプリコンパイル済みのバイナリはサポートされています
- 最初に実行 Bash.exe で入力を求めるは正しくローカライズされています
- proc/meminfo 返します情報を修正するようになりました
- ソケットの VFS でサポートされています
- tempfs として/dev がマウントされました
- Fifo のようになりました
- Proc/cpuinfo で正しく表示されて、マルチコア システム
- さらなる改良とエラー メッセージが最初の実行中にダウンロード
- Syscall の機能強化とバグ修正。 以下のサポートされている syscall 一覧。
- 追加のバグ修正と機能強化

### <a name="known-issues"></a>既知の問題
- 解決されていません '… ' 場合によっては DriveFs で正しく

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を持つ新しいまたは強化された syscall の一覧を以下に示します。 少なくとも 1 つのシナリオではこの一覧に syscall がサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点で。

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

## <a name="build-14332"></a>ビルド 14332

一般的な Windows ビルド 14332 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/wip14332)します。 <br/>


### <a name="fixed"></a>固定
- DNS エントリの優先順位付けを含む resolv.conf 生成の向上
- /Mnt 間と非ファイルおよびディレクトリの移動に関する問題-mnt ドライブ/
- Tar ファイル、シンボリック リンクは作成できます。
- インスタンスの作成時に追加された既定/run/lock ディレクトリ
- 適切な統計情報を返すこと/dev/null を更新します。
- 最初の実行中にダウンロードするときにその他のエラー
- Syscall の機能強化とバグ修正。 以下のサポートされている syscall 一覧。
- 追加の機能強化のバグ修正と機能強化

### <a name="syscall-support"></a>Syscall サポート
WSL でいくつかの実装を含む新しい syscall を次に示します。 少なくとも 1 つのシナリオではこの一覧にシステム コールがサポートされているが場合がありますがすべてのパラメーター サポートされていませんこの時点でします。

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>ビルド 14328

一般的な Windows ビルド 14332 に関する情報を参照してください、 [Windows ブログ](https://aka.ms/wip14328)します。 <br/>


### <a name="new-features"></a>新機能
* Linux ユーザーをサポートします。  Ubuntu on Windows での Bash のインストールは、Linux ユーザーの作成を求められます。  詳細については、次を参照してください。 https://aka.ms/wslusers
* ホスト名がない設定を Windows コンピューター名にようになりました @localhost
* 詳細については、ビルド 14328 を参照してください。 https://aka.ms/wip14328

### <a name="fixed"></a>固定
* 非/mnt/のシンボリック リンクの機能強化<drive>ファイル
    * npm インストール機能
    * jdk jre を今すぐインストール可能な命令を使用して[ここ](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)します。
    * 既知の問題: Windows のマウントのシンボリック リンクが機能しません。  機能は今後のビルドで使用できます。
* top としたければが表示されます。
* インストール エラーのいくつかの追加のエラー メッセージ
* Syscall の機能強化とバグ修正。  以下のサポートされている syscall 一覧。
* 追加の機能強化のバグ修正と機能強化

### <a name="syscall-support"></a>Syscall サポート
WSL でのいくつかの実装を持って syscall の一覧を次に示します。  Syscall この一覧には少なくとも 1 つのシナリオでサポートされてが可能性がありますがパラメーターをすべてサポートされていませんこの時点でします。

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
