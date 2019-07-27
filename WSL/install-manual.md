---
title: Windows Subsystem for Linux (WSL) ディストリビューションを手動でダウンロードする
description: Windows Subsystem for Linux ディストリビューションを手動でダウンロードする方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、WSL、windows subsystem、ディストリビューション、ubuntu、openSUSE、SLES、debian、kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: bf2f2e24fb8a2db49270fb77558d4fda1828dedf
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/26/2019
ms.locfileid: "68523778"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Windows Subsystem for Linux ディストリビューションパッケージを手動でダウンロードする

Microsoft Store 経由で WSL Linux ディストリビューションをインストールすることはできない (または必要ない) シナリオがいくつかあります。 具体的には、Microsoft Store をサポートしていない Windows Server または長期的なサービス (LTSC) デスクトップ OS SKU を実行している可能性があります。また、環境内で Microsoft Store の使用を許可しないように企業ネットワークポリシーや管理者を指定することもできます。

このような場合は、WSL 自体を利用できますが、ストアにアクセスできない場合は、WSL で Linux ディストリビューションをダウンロードしてインストールするにはどうすればよいですか。

> 注:**Cmd、PowerShell、Linux/WSL ディストリビューションを含むコマンドラインシェル環境は、Windows 10 S モードでの実行が許可されていません**。 この制限は、によって提供される整合性と安全性の目標を確保するために存在します。詳細については、こちらの[投稿](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)をお読みください。

## <a name="downloading-distros"></a>ディストリビューションのダウンロード

Microsoft Store アプリが使用できない場合は、次のリンクをクリックして Linux ディストリビューションをダウンロードし、手動でインストールすることができます。
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [WSL の Fedora Remix](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

これにより、 `<distro>.appx`パッケージは選択したフォルダーにダウンロードされます。 [インストール手順](#Installing-your-distro)に従って、ダウンロードしたディストリビューションをインストールします。

## <a name="downloading-distros-via-the-command-line"></a>コマンドラインを使用したディストリビューションのダウンロード
必要に応じて、コマンドラインを使用して、優先するディストリビューションをダウンロードすることもできます。

 ### <a name="download-using-powershell"></a>PowerShell を使用してダウンロードする
 PowerShell を使用してディストリビューションをダウンロードするには、 [-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest)コマンドレットを使用します。 Ubuntu 16.04 をダウンロードするためのサンプル命令を次に示します。

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> ダウンロードに時間がかかる場合は、を設定して進行状況バーをオフにします。`$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Curl を使用してダウンロードする
Windows 10 Spring 2018 Update (またはそれ以降) には、コマンドラインから web 要求 (HTTP GET、POST、PUT などのコマンド) を呼び出すことができる、一般的な[curl コマンドラインユーティリティ](https://curl.haxx.se/)が含まれています。 を使用`curl.exe`すると、上記のディストリビューションをダウンロードできます。

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

上の例では`curl.exe` 、(だけで`curl`なく) が実行され、powershell では、[呼び出し](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)の powershell curl エイリアスではなく、実際の curl 実行可能ファイルが呼び出されるようにしています。

> 注:コマンド`curl`シェルやスクリプトを使用してダウンロード手順を呼び出したりスクリプトを作成したり`.bat`  /  `.cmd`する必要がある場合は、を使用することをお勧めします。

## <a name="installing-your-distro"></a>ディストリビューションのインストール
Windows 10 を使用している場合は、PowerShell を使用してディストリビューションをインストールできます。 上記の手順でダウンロードしたディストリビューションが格納されているフォルダーに移動し、その`app_name`ディレクトリで次のコマンドを実行します。ここで、は、ディストリビューションの .appx ファイルの名前です。  
```Powershell
Add-AppxPackage .\app_name.appx
```

Windows server を使用している場合は、 [Windows server](install-on-server.md)のドキュメントページでインストール手順を確認できます。

ディストリビューションがインストールされたら、Intilization の[手順](initialize-distro.md)ページを参照して、新しいディストリビューションを初期化します。
