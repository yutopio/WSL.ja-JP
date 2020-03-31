---
title: Windows Server に Linux サブシステムをインストールする
description: Windows Server 上の Linux サブシステムのインストール手順です。
keywords: BashOnWindows, bash, wsl, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256395"
---
# <a name="windows-server-installation-guide"></a>Windows Server インストール ガイド

> Windows Server 2019 以降に適用されます

Microsoft は、[Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/) 上で Linux 用 Windows サブシステムを利用できるようになったことを //Build2017 で発表しました。  以下の手順では、Windows Server 1709 以降で Linux 用 Windows サブシステムを実行する手順について説明します。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Linux 用 Windows サブシステム (WSL) を有効にする

Windows 上で Linux ディストリビューションを実行する前に、"Linux 用 Windows サブシステム" オプション機能を有効にして再起動する必要があります。

1. 管理者として PowerShell を開き、以下を実行します。
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. メッセージが表示されたら、コンピューターを再起動します。 WSL から信頼できる実行環境を開始できるようにするには、**この再起動が必要**です。

## <a name="download-a-linux-distro"></a>Linux ディストリビューションをダウンロードする

[これらの手順](install-manual.md)に従って、お気に入りの Linux ディストリビューションをダウンロードします。

## <a name="extract-and-install-a-linux-distro"></a>Linux ディストリビューションを抽出してインストールする
ディストリビューションをダウンロードしたので、その内容を抽出し、手動でディストリビューションをインストールします。

1. PowerShell を使用するなどして、`<distro>.appx` パッケージのコンテンツを抽出します。

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. ディストリビューション ランチャーを実行します。インストールを完了するには、`<distro>.exe` という名前のターゲット フォルダーでディストリビューション ランチャー アプリケーションを実行します。 例: `ubuntu.exe` など。

    ![Windows Server 上の展開された Ubuntu ディストリビューション](media/server-appx-expand.png)

    > **トラブルシューティング**
    > * **エラー 0x8007007e が発生してインストールに失敗しました**:このエラーは、システムで WSL がサポートされていない場合に発生します。 次のことを確認します。
    >   * Windows ビルド 16215 以降を実行している。 [ビルドを確認してください](troubleshooting.md#check-your-build-number)。
    >   * Windows Subsystem for Linux オプション コンポーネントが有効になっていて、コンピューターが再起動されている。  [WSL が有効になっていることを確認してください](troubleshooting.md#confirm-wsl-is-enabled)。
    
3. たとえば、Powershell を使用して、Windows 環境の PATH (この例では `C:\Users\Administrator\Ubuntu`) にディストリビューション パスを追加します。
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    これで、「`<distro>.exe`」と入力して任意のパスからディストリビューションを起動できるようになりました。 たとえば次のようになります。`ubuntu.exe`

Linux ディストリビューションがインストールされたので、ディストリビューションを使用する前に、一度[新しいディストリビューション インスタンスを初期化する](initialize-distro.md)必要があります。
