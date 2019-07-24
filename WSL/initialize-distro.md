---
title: 新しい WSL Linux ディストリビューションを初期化する
description: WSL 用の Linux ディストリビューションをインストールしたら、次の簡単な手順に従って初期化を完了します。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499297"
---
# <a name="initializing-a-newly-installed-distro"></a>新しくインストールされたディストリビューションの初期化
ディストリビューションをダウンロードしてインストールしたら、新しいディストリビューションの初期化を完了する必要があります。

## <a name="launch-a-distro"></a>ディストリビューションを起動する
新しくインストールされたディストリビューションの初期化を完了するには、新しいインスタンスを起動します。 これを行うには、Microsoft Store アプリの [起動] ボタンをクリックするか、[スタート] メニューから [ディストリビューション] を起動します。

> ヒント:最も頻繁に使用されるディストリビューションを [スタート] メニューやタスクバーにピン留めすることができます。

![[スタート] メニューからディストリビューションを起動する](media/start-menu.png)

> Windows Server では、ディストリビューションのインストールフォルダーから、ディストリビューション`<distro>.exe`のランチャー実行可能ファイルを起動できます。

新しくインストールされたディストリビューションを初めて実行すると、コンソールウィンドウが開き、インストールが完了するまで 1 ~ 2 分待つように求められます。

> インストールのこの最終段階では、ディストリビューションのファイルが圧縮解除され、PC に保存され、使用できるようになります。 PC の記憶装置のパフォーマンスによっては、約1分以上かかることがあります。 この初期インストール段階は、ディストリビューションがクリーンインストールされている場合にのみ必要です。今後のすべての起動には1秒未満の時間がかかります。

## <a name="setting-up-a-new-linux-user-account"></a>新しい Linux ユーザーアカウントの設定

インストールが完了すると、新しいユーザーアカウント (およびそのパスワード) を作成するように求められます。 

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

このユーザーアカウントは、通常の管理者以外のユーザーのために、ディストリビューションの起動時に既定でログインします。

> 任意のユーザー名とパスワードを選択できます。 Windows ユーザー名には影響しません。 

新しいディストリビューションインスタンスを開いたときに、パスワードの入力を求められることはありませんが、を **`sudo`使用してプロセスを昇格する場合は、パスワードを入力する必要**があるため、覚えやすいパスワードを選択してください。 詳細については、「[ユーザーサポート](user-support.md)」ページを参照してください。

## <a name="update--upgrade-your-distros-packages"></a>ディストリビューションのパッケージを更新 & アップグレードする

ほとんどのディストリビューションには、空/最小のパッケージカタログが付属しています。 パッケージカタログを定期的に更新し、ディストリビューションの優先パッケージマネージャーを使用して、インストールされているパッケージをアップグレードすることを強くお勧めします。 Debian/Ubuntu では、apt を使用します。

```bash
sudo apt update && sudo apt upgrade
```

> Linux ディストリビューションは、Windows によって自動的に更新またはアップグレードされません。これは、Linux ユーザーが自分で制御したいタスクです。

これで完了です。 WSL で新しい Linux ディストリビューションをご利用いただけます。 WSL の詳細については、他の[wsl ドキュメント](https://aka.ms/wsldocs)または[wsl learning のリソース](https://aka.ms/learnwsl)に関するページを参照してください。

![WSL で Linux を使用する](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>トラブルシューティング

関連するエラーと修正案を以下に示します。 その他の一般的なエラーとその解決策については、 [Wsl トラブルシューティングのページ](troubleshooting.md)を参照してください。

> **エラー0x8007007e が発生し、インストールに失敗しました**このエラーは、システムがストアから Linux をサポートしていない場合に発生します。  次のことを確認します。
> * Windows ビルド16215以降を実行しています。 [ビルドを確認](troubleshooting.md#check-your-build-number)します。
> * Windows Subsystem for Linux のオプションコンポーネントが有効になり、コンピューターが再起動されました。  [WSL が有効になっていることを確認して](troubleshooting.md#confirm-wsl-is-enabled)ください。
