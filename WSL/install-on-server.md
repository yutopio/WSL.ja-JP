---
title: Windows Server に Linux サブシステムをインストールする
description: Windows Server 上の Linux サブシステムのインストール手順です。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269780"
---
# <a name="windows-server-installation-guide"></a>Windows Server インストールガイド

> Windows Server 2019 以降に適用されます

Microsoft は、windows [Server で](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)windows Subsystem for Linux を使用できるようになったことを、build2017 年に発表しました。  これらの手順では、windows Server 1709 以降で Windows Subsystem for Linux を実行する方法について説明します。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Windows Subsystem for Linux (WSL) を有効にする

Windows で Linux ディストリビューションを実行するには、[Windows Subsystem for Linux] オプション機能を有効にし、再起動する必要があります。

1. 管理者として PowerShell を開き、次のように実行します。
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. メッセージが表示されたら、コンピューターを再起動します。 **この再起動は**、wsl が信頼された実行環境を開始できるようにするために必要です。

## <a name="download-a-linux-distro"></a>Linux ディストリビューションをダウンロードする

お気に入りの Linux ディストリビューションをダウンロードするには、こちら[の手順](install-manual.md)に従ってください。

## <a name="extract-and-install-a-linux-distro"></a>Linux ディストリビューションを抽出してインストールする
これで、ディストリビューションをダウンロードしたので、その内容を抽出し、ディストリビューションを手動でインストールします。

1. PowerShell を使用して、パッケージの内容を抽出します。`<distro>.appx`

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. ディストリビューションランチャーを実行してインストールを完了し、という名前`<distro>.exe`のターゲットフォルダーでディストリビューションランチャーアプリケーションを実行します。 例: `ubuntu.exe`、など。

    ![Windows Server での Ubuntu ディストリビューションの拡張](media/server-appx-expand.png)

    > **トラブルシューティング**
    > * 次**のエラーによりインストールに失敗しました: 0x8007007e**:このエラーは、システムで WSL がサポートされていない場合に発生します。 次のことを確認します。
    >   * Windows ビルド16215以降を実行しています。 [ビルドを確認](troubleshooting.md#check-your-build-number)します。
    >   * Windows Subsystem for Linux のオプションコンポーネントが有効になり、コンピューターが再起動されました。  [WSL が有効になっていることを確認して](troubleshooting.md#confirm-wsl-is-enabled)ください。
    
3. ディストリビューションパスを Windows 環境パス (`C:\Users\Administrator\Ubuntu`この例では) に追加します。たとえば、Powershell を使用します。
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    を入力`<distro>.exe`して、任意のパスからディストリビューションを起動できるようになりました。 たとえば次のようになります。`ubuntu.exe`

Linux ディストリビューションがインストールされたので、ディストリビューションを使用する前に、[新しいディストリビューションインスタンスを初期化](initialize-distro.md)する必要があります。
