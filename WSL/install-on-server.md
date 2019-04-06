---
title: Windows Server で Linux サブシステムをインストールします。
description: Windows Server で Linux サブシステムのインストール手順。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、windows server 用 windows サブシステム
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063620"
---
# <a name="windows-server-installation-guide"></a>Windows Server インストール ガイド

> Windows Server 2019 以降に適用されます。

/Build2017、Windows Subsystem for Linux がなります、Microsoft が発表されました/ [Windows Server で使用可能な](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)します。  これらの手順は、Windows Server 1709 以降の Linux 用 Windows サブシステムを実行している説明します。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Linux (WSL) の Windows サブシステムを有効にします。

を Windows での Linux ディストリビューションを実行する前に、"Windows サブシステムの Linux"の省略可能な機能を有効にし、再起動する必要があります。

1. 管理者として PowerShell を開きを実行します。
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. コンピューターが表示されたら再起動します。 **この再起動は必要な**WSL が信頼できる実行環境を開始できることを保証するためにします。

## <a name="download-a-linux-distro"></a>Linux ディストリビューションをダウンロードします。

次の[手順](install-manual.md)お気に入りの Linux ディストリビューションをダウンロードします。

## <a name="extract-and-install-a-linux-distro"></a>抽出して、Linux ディストリビューションをインストールします。
これで、ディストリビューションをダウンロードすると、その内容を抽出およびディストリビューションを手動でインストールします。

1. 抽出、`<distro>.appx`例: PowerShell を使用して、パッケージの内容。

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. インストールを完了するには、ディストリビューションのランチャー アプリケーションをターゲット フォルダーで実行ディストリビューション ランチャーをという名前の実行`<distro>.exe`します。 例:`ubuntu.exe`など。

    ![Windows Server での展開の Ubuntu ディストリビューション](media/server-appx-expand.png)

    > **トラブルシューティング**
    > * **インストールに失敗しましたエラー 0x8007007e**:WSL をサポートしていないシステムでこのエラーが発生します。 次のことを確認します。
    >   * 16215 またはそれ以降は、Windows ビルドを実行しています。 [ビルド確認](troubleshooting.md#check-your-build-number)します。
    >   * Linux の省略可能なコンポーネント用 Windows サブシステムが有効になっており、コンピューターが再起動します。  [WSL が有効になっていることを確認](troubleshooting.md#confirm-wsl-is-enabled)します。
    
3. Windows 環境のパスに、ディストリビューションのパスを追加 (`C:\Users\Administrator\Ubuntu`この例では)、Powershell を使用するなど。
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    」と入力して任意のパスから、ディストリビューションを起動できるようになりました`<distro>.exe`します。 次に、例を示します。 `ubuntu.exe`

必要があります、Linux ディストリビューションがインストールされた[ディストリビューションの新しいインスタンスを初期化](initialize-distro.md)ディストリビューションを使用する前にします。
