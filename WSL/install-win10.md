---
title: Windows 10 に Windows Subsystem for Linux (WSL) をインストールする
description: Windows 10 の Windows Subsystem for Linux のインストール手順。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10、install
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 218e3e652d0849f944e8aaceef3fb954294222be
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122775"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10 用 windows Subsystem for Linux インストールガイド

## <a name="install-the-windows-subsystem-for-linux"></a>Windows Subsystem for Linux をインストールする

WSL 用の Linux ディストリビューションをインストールする前に、[Windows Subsystem for Linux] オプション機能が有効になっていることを確認する必要があります。

1. 管理者として PowerShell を開き、次のように実行します。
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. メッセージが表示されたら、コンピューターを再起動します。

## <a name="install-your-linux-distribution-of-choice"></a>選択した Linux ディストリビューションをインストールする
優先するディストリビューションをダウンロードしてインストールするには、次の3つの選択肢があります。
1. Microsoft Store からダウンロードしてインストールする (下記参照)
1. コマンドラインまたはスクリプトからダウンロードしてインストールする ([手動によるインストール手順を参照](install-manual.md))
1. をダウンロードして手動で展開してインストールする (Windows Server の場合-[手順](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 の作成者の更新プログラム以降:Microsoft Store からのインストール

> このセクションは、Windows ビルド16215以降を対象としています。  [ビルドを確認](troubleshooting.md#check-your-build-number)するには、次の手順に従います。 

1. Microsoft Store を開き、お気に入りの Linux ディストリビューションを選択します。

    ![Microsoft Store の Linux ディストリビューションのビュー](media/store.png)

    次のリンクを使用すると、各ディストリビューションの Microsoft ストアページが開きます。

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [WSL の Fedora Remix](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. ディストリビューションのページで、[Get] を選択します。

    ![Microsoft ストアの Linux ディストリビューションの表示](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>ディストリビューションの初期化を完了する
Linux ディストリビューションがインストールされたので、[新しいディストリビューションインスタンス](initialize-distro.md)を使用するには、一度初期化する必要があります。

## <a name="troubleshooting"></a>トラブルシューティング: 

関連するエラーと修正案を以下に示します。 その他の一般的なエラーとその解決策については、 [Wsl トラブルシューティングのページ](troubleshooting.md)を参照してください。

* **エラー0x80070003 が発生し、インストールに失敗しました**
    * Windows Subsystem for Linux はシステムドライブ (通常は`C:`ドライブ) でのみ実行されます。 ディストリビューションがシステムドライブに格納されていることを確認します。  
    * [**設定** -> ] [**ストレージ** -> ][その他のストレージ設定]を開きます。**新しいコンテンツが保存**
    ![される場所の変更 C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)
    
    
 * **WslRegisterDistribution がエラー0x8007019e で失敗しました**   
  * Windows Subsystem for Linux のオプションコンポーネントが有効になっていません。 
   * [**コントロールパネル]**  -> の [**プログラムと機能** -> ] **[windows の機能の有効化または無効化**] を開くか、この記事の冒頭に記載されている PowerShell コマンドレットを使用して、windows**の**機能をオンまたはオフ > チェックします。
