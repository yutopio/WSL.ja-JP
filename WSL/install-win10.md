---
title: Linux (WSL) 用の Windows サブシステムを Windows 10 上にインストールします。
description: Windows 10 での Linux 用 Windows サブシステムのインストール手順。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステムのインストールします。
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063290"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10 用の Linux インストール ガイド用 Windows サブシステム

## <a name="install-the-windows-subsystem-for-linux"></a>Linux 用の Windows サブシステムをインストールします。

WSL の任意の Linux ディストリビューションをインストールする前にすることが必要、"Windows サブシステムの Linux"省略可能な機能を有効にします。

1. 管理者として PowerShell を開きを実行します。
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. コンピューターが表示されたら再起動します。

## <a name="install-your-linux-distribution-of-choice"></a>任意の Linux ディストリビューションをインストールします。
をダウンロードして、優先 distro(s) をインストールするには、次の 3 つの選択肢があります。
1. Windows ストア (下記参照) からダウンロードしてインストール
1. コマンドのコマンドライン/スクリプトからダウンロードしてインストール ([手動インストールの指示を読み](install-manual.md))
1. ダウンロードして手動で展開し、インストール (for Windows Server -[こちら](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update 以降。Microsoft Store からインストールします。

> このセクションでは、Windows ビルド 16215 またはそれ以降は。  以下の手順に従って[ビルド確認](troubleshooting.md#check-your-build-number)します。 

1. Microsoft Store を開き、お気に入りの Linux ディストリビューションを選択します。

    ![Windows ストアでの Linux ディストリビューションのビュー](media/store.png)

    次のリンクには、各ディストリビューションの Windows ストア ページが開きます。

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [OpenSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. ディストリビューションのページで、"Get"を選択します

    ![Windows ストアでの Linux ディストリビューションのビュー](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>ディストリビューションの初期化を完了
必要があります、Linux ディストリビューションがインストールされた[ディストリビューションの新しいインスタンスを初期化](initialize-distro.md)1 回を使用します。

## <a name="troubleshooting"></a>トラブルシューティング: 

関連するエラーと推奨される修正方法を次に示します。 参照してください、 [WSL のトラブルシューティング ページ](troubleshooting.md)の他の一般的なエラーとその解決方法。

* **インストールに 0x80070003 のエラーで失敗しました**
    * Windows Subsystem for Linux は、システム ドライブでのみ実行されます (通常、これは、`C:`ドライブ)。 ディストリビューションの場合は、システム ドライブに格納されていることを確認します。  
    * 開いている**設定** -> **ストレージ** -> **以上の記憶域の設定。新しいコンテンツが保存されている変更**
    ![c: ドライブにアプリをインストールするシステム設定の画像](media/AppStorage.png)
