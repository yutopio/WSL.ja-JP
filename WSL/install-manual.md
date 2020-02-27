---
title: Windows Subsystem for Linux (WSL) ディストリビューションを手動でダウンロードする
description: Windows Subsystem for Linux ディストリビューションを手動でダウンロードする方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、WSL、windows subsystem、ディストリビューション、ubuntu、openSUSE、SLES、debian、kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: aa0b42748115045105bb4e6eae91493bfee11d09
ms.sourcegitcommit: 467b6c8e9716d1a60dbf9f7658fd9579da365b58
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2020
ms.locfileid: "77624926"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Windows Subsystem for Linux ディストリビューションパッケージを手動でダウンロードする

Microsoft Store 経由で WSL Linux ディストリビューションをインストールすることはできない (または必要ない) シナリオがいくつかあります。 具体的には、Microsoft Store をサポートしていない Windows Server または長期的なサービス (LTSC) デスクトップ OS SKU を実行している可能性があります。また、環境内で Microsoft Store の使用を許可しないように企業ネットワークポリシーや管理者を指定することもできます。

このような場合は、WSL 自体を利用できますが、ストアにアクセスできない場合は、WSL で Linux ディストリビューションをダウンロードしてインストールするにはどうすればよいですか。

> 注:**コマンドラインシェル環境 (Cmd、PowerShell、Linux/WSL ディストリビューションを含む) は、Windows 10 S モードでの実行は許可されていません**。 この制限は、S モードで提供される整合性と安全性の目標を確保するために存在します。詳細については、[この投稿](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)を参照してください。

## <a name="downloading-distros"></a>ディストリビューションのダウンロード

Microsoft Store アプリが使用できない場合は、次のリンクをクリックして Linux ディストリビューションをダウンロードし、手動でインストールすることができます。
<!-- * [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm) -->
* Ubuntu 18.04
* Ubuntu 18.04 ARM
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [WSL のための Fedora リミックス](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

これにより、`<distro>.appx` パッケージが、選択したフォルダーにダウンロードされます。 [インストール手順](#installing-your-distro)に従って、ダウンロードしたディストリビューションをインストールします。

## <a name="downloading-distros-via-the-command-line"></a>コマンドラインを使用したディストリビューションのダウンロード
必要に応じて、コマンドラインを使用して、優先するディストリビューションをダウンロードすることもできます。

 ### <a name="download-using-powershell"></a>PowerShell を使用してダウンロードする
 PowerShell を使用してディストリビューションをダウンロードするには、 [-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest)コマンドレットを使用します。 Ubuntu 16.04 をダウンロードするためのサンプル命令を次に示します。

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> ダウンロードに時間がかかる場合は、を設定して進行状況バーをオフにし `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Curl を使用してダウンロードする
Windows 10 Spring 2018 Update (またはそれ以降) には、コマンドラインから web 要求 (HTTP GET、POST、PUT などのコマンド) を呼び出すことができる、一般的な[curl コマンドラインユーティリティ](https://curl.haxx.se/)が含まれています。 `curl.exe` を使用すると、上記のディストリビューションをダウンロードできます。

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

上の例では、(`curl`だけでなく) `curl.exe` が実行され、PowerShell によって実際の curl 実行可能ファイルが呼び出されます。これは、[呼び出し](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)の powershell curl エイリアスではありません。

> 注: `curl` を使用すると、Cmd シェルや `.bat` / `.cmd` スクリプトを使用してダウンロード手順を呼び出したりスクリプトを作成したりする必要がある場合に適しています。

## <a name="installing-your-distro"></a>ディストリビューションのインストール
Windows 10 を使用している場合は、PowerShell を使用してディストリビューションをインストールできます。 上記の手順でダウンロードしたディストリビューションが格納されているフォルダーに移動し、そのディレクトリで次のコマンドを実行します。 `app_name` は、ディストリビューションの .appx ファイル名です。  
```Powershell
Add-AppxPackage .\app_name.appx
```

Windows server を使用している場合は、 [Windows server](install-on-server.md)のドキュメントページでインストール手順を確認できます。

ディストリビューションがインストールされたら、初期化の[手順](initialize-distro.md)ページを参照して、新しいディストリビューションを初期化します。
