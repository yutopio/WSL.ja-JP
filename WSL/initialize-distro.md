---
title: 新しい WSL Linux ディストリビューションの初期化
description: WSL 用の Linux ディストリビューションをインストールしたら、次の簡単な手順に従って初期化を完了します
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c33d349a6d39c325b079ccbf7ed6350bed796e33
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269589"
---
# <a name="initializing-a-newly-installed-distro"></a>新しくインストールされたディストリビューションの初期化
ディストリビューションをダウンロードしてインストールしたら、新しいディストリビューションの初期化を完了する必要があります。

## <a name="launch-a-distro"></a>ディストリビューションの起動
新しくインストールされたディストリビューションの初期化を完了するには、新しいインスタンスを起動します。 これを行うには、Microsoft Store アプリの [起動] ボタンをクリックするか、[スタート] メニューからそのディストリビューションを起動します。

> ヒント:最も頻繁に使用するディストリビューションを [スタート] メニューやタスク バーにピン留めすることができます。

![[スタート] メニューからディストリビューションを起動する](media/start-menu.png)

> Windows Server では、ディストリビューション インストール フォルダーから、ディストリビューションのランチャー実行可能ファイル `<distro>.exe` を起動できます。

新しくインストールされたディストリビューションを初めて実行すると、コンソール ウィンドウが開き、インストールが完了するまで 1、2 分待つように求められます。

> インストールのこの最終段階で、ディストリビューションのファイルが圧縮解除されて PC に保存され、使用できるようになります。 PC の記憶装置のパフォーマンスによっては、約 1 分またはそれ以上かかることがあります。 この初回インストール段階は、ディストリビューションがクリーン インストールされる場合にのみ必要です。以降のすべての起動にかかる時間は 1 秒未満です。

## <a name="setting-up-a-new-linux-user-account"></a>新しい Linux ユーザー アカウントの設定

インストールが完了すると、新しいユーザー アカウント (およびそのパスワード) を作成するように求められます。 

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

このユーザー アカウントは、ディストリビューションの起動時に既定でログインする、管理者以外の通常ユーザー用です。

> 任意のユーザー名とパスワードを選択できます。Windows ユーザー名と関係はありません。 

新しいディストリビューション インスタンスを開いたときに、パスワードの入力は求められませんが、 **`sudo` を使用してプロセスを昇格する場合は、パスワードを入力する必要があるため**、必ず覚えやすいパスワードを選択してください。 詳細については、[ユーザー サポート](user-support.md)に関するページを参照してください。

## <a name="update--upgrade-your-distros-packages"></a>ディストリビューションのパッケージの更新とアップグレード

ほとんどのディストリビューションには、空または最小のパッケージ カタログが付属しています。 パッケージ カタログを定期的に更新し、ディストリビューションの推奨パッケージ マネージャーを使用して、インストールされているパッケージをアップグレードすることを強くお勧めします。 Debian または Ubuntu では、apt を使用します。

```bash
sudo apt update && sudo apt upgrade
```

> Windows では、Linux ディストリビューションの更新やアップグレードは自動的に行われません。これは、Linux ユーザーが自分で制御することを好むタスクです。

これで完了です。 WSL で新しい Linux ディストリビューションをご利用ください。 WSL の詳細については、他の [WSL ドキュメント](https://aka.ms/wsldocs)または[WSL の学習リソースのページ](https://aka.ms/learnwsl)を参照してください。

![WSL で Linux を使用する](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>トラブルシューティング

関連エラーと推奨される修正を次に示します。 その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。

> **エラー 0x8007007e が発生してインストールに失敗しました** このエラーは、ストアの Linux をシステムがサポートしていない場合に発生します。  次のことを確認します。
> * Windows ビルド 16215 以降を実行している。 [ビルドを確認してください](troubleshooting.md#check-your-build-number)。
> * Windows Subsystem for Linux オプション コンポーネントが有効になっていて、コンピューターが再起動されている。  [WSL が有効になっていることを確認してください](troubleshooting.md#confirm-wsl-is-enabled)。
