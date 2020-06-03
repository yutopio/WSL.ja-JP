---
title: Windows Subsystem for Linux (WSL) を Windows 10 にインストールする
description: Windows 10 での Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6ed12ba9d63d3f4038b67489035e13113a372928
ms.sourcegitcommit: 9f12e168b80775cd967f22f97376e51043c3667e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/02/2020
ms.locfileid: "84301203"
---
# <a name="install-windows-subsystem-for-linux"></a>Linux 用 Windows サブシステムをインストールする

次のガイドでは、Windows 10 を実行しているコンピューターに Linux 用 Windows サブシステム (WSL) をインストールするために必要な手順について説明します。

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a>Linux 用 Windows サブシステム オプション機能を有効にする

Linux ディストリビューションをインストールする前に、Windows 10 上で "Linux 用 Windows サブシステム" オプション機能を有効にする必要があります。

1. 管理者として PowerShell を開き、このスクリプトを入力します。

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. メッセージが表示されたら、コンピューターを再起動します。

## <a name="install-a-linux-distribution"></a>Linux ディストリビューションをインストールする

推奨される Linux ディストリビューションをダウンロードしてインストールするには、3 つの方法があります。

- Microsoft Store からダウンロードしてインストールする (下記参照)
- [コマンド ラインからダウンロードして手動でインストールする](install-manual.md)
- [Windows Server へのインストール](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a>Microsoft Store からのインストール

Linux ディストリビューションは、Windows 10 の Microsoft Store (Build 16215+) からインストールできます。

> [!NOTE]
> これらの手順に従って、[Windows 10 のビルド番号を確認](troubleshooting.md#check-your-build-number)します。

1. Microsoft Store を開き、希望する Linux ディストリビューションを選択します。

    ![Microsoft Store の Linux ディストリビューションのビュー](media/store.png)

    次のリンクを使用すると、各ディストリビューションの Microsoft Store ページが開きます。

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [WSL のための Fedora リミックス](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. [取得] を選択し、ディストリビューションのダウンロードが完了したら、[起動] を選択します。

    ![Microsoft Store の Linux ディストリビューションのビュー](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>ディストリビューションの初期化を完了する

Linux ディストリビューションを起動したら、画面の指示に従って、ディストリビューションを初期化します。

> [!NOTE]
> Windows Server の場合は、インストール フォルダーにある実行可能ファイル (`<distro>.exe`) を使用してディストリビューションを起動します。

新しくインストールされたディストリビューションを初めて実行すると、コンソール ウィンドウが開き、インストールが完了するまで 1、2 分待つように求められます。 インストールのこの最終段階で、ディストリビューションのファイルが圧縮解除されて PC に保存され、使用できるようになります。 PC の記憶装置のパフォーマンスによっては、約 1 分またはそれ以上かかることがあります。 この初回インストール段階は、ディストリビューションがクリーン インストールされる場合にのみ必要です。以降のすべての起動にかかる時間は 1 秒未満です。

## <a name="set-up-a-new-linux-user-account"></a>新しい Linux ユーザー アカウントの設定

インストールが完了すると、新しいユーザー アカウント (およびそのパスワード) を作成するように求められます。

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

このユーザー アカウントは、ディストリビューションの起動時に既定でログインする、管理者以外の通常ユーザー用です。 任意のユーザー名とパスワードを選択できます。Windows ユーザー名と関係はありません。

新しいディストリビューション インスタンスを開いたときに、パスワードの入力は求められませんが、 **`sudo` を使用してプロセスを昇格する場合は、パスワードを入力する必要があるため**、必ず覚えやすいパスワードを選択してください。 詳細については、[ユーザー サポート](user-support.md)に関するページを参照してください。

## <a name="update--upgrade-packages"></a>パッケージの更新とアップグレード

ほとんどのディストリビューションには、空または最小のパッケージ カタログが付属しています。 パッケージ カタログを定期的に更新し、ディストリビューションの推奨パッケージ マネージャーを使用して、インストールされているパッケージをアップグレードすることを強くお勧めします。 Debian または Ubuntu では、apt を使用します。

```bash
sudo apt update && sudo apt upgrade
```

Windows では、Linux ディストリビューションの更新やアップグレードは自動的に行われません。 これは、ほとんどの Linux ユーザーが自分で制御することを好むタスクです。

WSL で新しい Linux ディストリビューションをご利用ください。

## <a name="troubleshooting"></a>トラブルシューティング

関連インストール エラーと推奨される修正を次に示します。 その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。

### <a name="installation-failed-with-error-0x8007007e"></a>エラー 0x8007007e が発生してインストールに失敗しました

このエラーは、ストアからの Linux がサポートされていない場合に発生します。  次のことを確認します。

- Windows ビルド 16215 以降を実行している。 [ビルドを確認してください](troubleshooting.md#check-your-build-number)。
- Windows Subsystem for Linux オプション コンポーネントが有効になっていて、コンピューターが再起動されている。  [WSL が有効になっていることを確認してください](troubleshooting.md#confirm-wsl-is-enabled)。

### <a name="installation-failed-with-error-0x80070003"></a>エラー 0x80070003 が発生してインストールに失敗しました

Windows Subsystem for Linux はシステム ドライブ (通常、これは `C:` ドライブ) でのみ実行されます。 ディストリビューションがシステム ドライブに格納されていることを確認してください。

- **[設定]**  ->  **[ストレージ]**  ->  **[その他のストレージ設定:新しいコンテンツの保存先を変更する]** を開きます
  
    ![C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a>WslRegisterDistribution failed with error 0x8007019e (エラー 0x8007019e で WslRegisterDistribution が失敗しました)

Windows Subsystem for Linux オプション コンポーネントが有効になっていません。

- **[コントロール パネル]**  ->  **[プログラムと機能]**  ->  **[Windows の機能の有効化または無効化]** を開いて、 **[Windows Subsystem for Linux]** をチェックするか、またはこの記事の冒頭に記載した PowerShell コマンドレットを使用して有効にしてください。
