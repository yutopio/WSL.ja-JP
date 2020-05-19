---
title: Windows Server に Linux サブシステムをインストールする
description: Windows Server 上の Linux サブシステムのインストール手順です。
keywords: BashOnWindows, bash, wsl, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 86fd7de0ef45af760f46bb2a18932f513b813609
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270886"
---
# <a name="windows-server-installation-guide"></a>Windows Server インストール ガイド

Linux 用 Windows サブシステムは、Windows Server 2019 (バージョン 1709) 以降にインストールできます。 このガイドでは、お使いのマシンで WSL を有効にする手順について説明します。

## <a name="enable-the-windows-subsystem-for-linux"></a>Linux 用 Windows サブシステムを有効にする

Windows 上で Linux ディストリビューションを実行する前に、"Linux 用 Windows サブシステム" オプション機能を有効にして再起動する必要があります。

管理者として PowerShell を開き、以下を実行します。

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

**100% のシステム コールの互換性とより高速な IO パフォーマンスが必要な場合は、以下を読んで WSL 2 をインストールしてください。**

WSL 2 は、Windows 10、バージョン 2004、ビルド 19041 以上でのみ使用できます。 [Windows バージョンを更新](ms-settings:windowsupdate)し、5 月下旬にパブリック リリースされるまで [リリース プレビュー] リングで [Windows Insider プログラムに参加](https://insider.windows.com/insidersigninboth/)する必要があります。

**WSL 1 から続ける場合は、プロンプトが表示されたらマシンを再起動し、[こちら](./install-on-server.md#download-a-linux-distribution)** に従ってインストールを続行してください

## <a name="enable-the-virtual-machine-platform-optional-component"></a>仮想マシン プラットフォームのオプション コンポーネントを有効にする

"仮想マシン プラットフォーム" のオプション コンポーネントがインストールされていることを確認します。 これを行うには、PowerShell で次のコマンドを実行します。

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a>Linux ディストリビューションをダウンロードする

[これらの手順](install-manual.md)に従って、お気に入りの Linux ディストリビューションをダウンロードします。

## <a name="extract-and-install-a-linux-distribution"></a>Linux ディストリビューションを展開してインストールする

Linux ディストリビューションをダウンロードしたら、その内容を展開して手動でインストールするために、次の手順に従います。

1. PowerShell を使用して、`<distro>.appx` パッケージの内容を展開します。

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. ターゲット フォルダーでディストリビューション ランチャー アプリケーションを実行します。 ランチャーには、通常、`<distro>.exe` という名前が付けられます (たとえば、`ubuntu.exe`)。

    ![Windows Server 上の展開された Ubuntu ディストリビューション](media/server-appx-expand.png)

> [!CAUTION]
> **エラー 0x8007007e が発生してインストールに失敗しました**:このエラーが発生した場合、お使いのシステムは WSL をサポートしていません。 Windows ビルド 16215 以降を実行していることを確認してください。 [ビルドを確認してください](troubleshooting.md#check-your-build-number)。 さらに、[WSL が有効になっていることを確認](troubleshooting.md#confirm-wsl-is-enabled)し、この機能を有効にした後にコンピューターが再起動されていることを確認してください。  

3. PowerShell を使用して、Windows 環境の PATH (この例では `C:\Users\Administrator\Ubuntu`) にディストリビューション パスを追加します。

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

これで、「`<distro>.exe`」と入力して任意のパスからディストリビューションを起動できるようになりました。 たとえば、 `ubuntu.exe`と指定します。

インストールされたら、使用する前に[新しいディストリビューション インスタンスを初期化する](initialize-distro.md)必要があります。
