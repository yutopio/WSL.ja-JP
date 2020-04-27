---
title: Windows Subsystem for Linux (WSL) を Windows 10 にインストールする
description: Windows 10 での Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "74200231"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10 用 Windows Subsystem for Linux のインストール ガイド

## <a name="install-the-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のインストール

WSL 用の Linux ディストリビューションをインストールする前に、[Windows Subsystem for Linux] オプション機能が有効になっていることを確認する必要があります。

1. 管理者として PowerShell を開き、以下を実行します。
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. メッセージが表示されたら、コンピューターを再起動します。

## <a name="install-your-linux-distribution-of-choice"></a>任意の Linux ディストリビューションのインストール
希望するディストリビューションをダウンロードしてインストールするには、次の 3 つの選択肢があります。
* Microsoft Store からダウンロードしてインストールする (下記参照)
* コマンド ライン/スクリプトからダウンロードしてインストールする ([手動インストール手順を参照](install-manual.md))
* ダウンロードして手動で展開し、インストールする (Windows Server の場合 - [こちらの手順](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update 以降:Microsoft Store からのインストール

> このセクションは、Windows ビルド16215 以降が対象です。  [ビルドを確認する](troubleshooting.md#check-your-build-number)には、次の手順に従います。 

1. Microsoft Store を開き、希望する Linux ディストリビューションを選択します。

    ![Microsoft Store の Linux ディストリビューションのビュー](media/store.png)

    次のリンクを使用すると、各ディストリビューションの Microsoft Store ページが開きます。

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [WSL のための Fedora リミックス](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. ディストリビューションのページで、[入手] を選択します。

    ![Microsoft Store の Linux ディストリビューションのビュー](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>ディストリビューションの初期化を完了する
Linux ディストリビューションがインストールされたので、新しいディストリビューション インスタンスを使用する前に、一度[そのインスタンスを初期化する](initialize-distro.md)必要があります。

## <a name="troubleshooting"></a>トラブルシューティング : 

関連エラーと推奨される修正を次に示します。 その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。

* **エラー 0x80070003 が発生してインストールに失敗しました**
    * Windows Subsystem for Linux はシステム ドライブ (通常、これは `C:` ドライブ) でのみ実行されます。 ディストリビューションがシステム ドライブに格納されていることを確認してください。  
    * **[設定]** -> **[ストレージ]** -> **[その他のストレージ設定: 新しいコンテンツの保存先を変更する]** 
    を開きます。![C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)
    
    
 * **WslRegisterDistribution failed with error 0x8007019e (エラー0x8007019e で WslRegisterDistribution が失敗しました)**   
  * Windows Subsystem for Linux オプション コンポーネントが有効になっていません。 
   * **[コントロール パネル]**  ->  **[プログラムと機能]**  ->  **[Windows の機能の有効化または無効化]** を開いて、 **[Windows Subsystem for Linux]** をチェックするか、またはこの記事の冒頭に記載した PowerShell コマンドレットを使用して有効にしてください。
