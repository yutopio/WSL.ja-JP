---
title: Linux (WSL) ディストリビューション用 Windows サブシステムを手動でダウンロードします。
description: Linux ディストリビューション用 Windows サブシステムを手動でダウンロードする方法の手順です。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、WSL では、windows サブシステム、ディストリビューション、ubuntu、openSUSE、SLES、debian、kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 669c017c97aba70c107484b32acd99296265d84a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035034"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Linux ディストリビューションのパッケージの Windows サブシステムを手動でダウンロードします。

いくつかのシナリオをする可能性がありますいないできる (または) を Microsoft Store を使用して WSL Linux ディストリビューションをインストールします。 具体的を実行して、Windows Server または Microsoft Store、または、企業のネットワーク ポリシーおよび admins 環境内で Microsoft Store の使用を許可しない場合にサポートされていない OS SKU デスクトップの 長期的なサービス (LTSB/LTSC)。

このような場合は、WSL 自体は、使用可能な方法はダウンロードしてインストールする Linux ディストリビューション WSL でストアにアクセスできない場合ですか。

> 注:**Windows 10 S モードで実行する Cmd、PowerShell、および Linux/WSL ディストリビューションをはじめとするコマンド ライン シェル環境は許可されていません**します。 この制限は、整合性と安全性の目標 S モードを提供することを確認するには存在します。読み取り[この投稿](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)詳細についてはします。

## <a name="downloading-distros"></a>ディストリビューションをダウンロード

Microsoft Store アプリが使用できない場合は、ダウンロードして、これらのリンクをクリックして、Linux ディストリビューションを手動でインストールします。
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [WSL の fedora Remix](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

これにより、`<distro>.appx`任意のフォルダーにダウンロードするパッケージ。 に従って、[インストール手順](#installing-your-distro)ダウンロードした distro(s) をインストールします。

## <a name="downloading-distros-via-the-command-line"></a>コマンドラインを使用してディストリビューションをダウンロード
場合は、コマンドラインを使用して、優先 distro(s) もダウンロードできます。

 ### <a name="download-using-powershell"></a>PowerShell を使用してダウンロードします。
 PowerShell を使用してディストリビューションをダウンロードするには、使用、 [Invoke-webrequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest)コマンドレット。 Ubuntu 16.04 をダウンロードするサンプル手順を次に示します。

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> ダウンロードにかかる時間が長いが場合、設定して、進行状況バーをオフに `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Curl を使用してダウンロードします。
Windows 10 のスプリング 2018 Update (またはそれ以降) を含む、一般的な[コマンド ライン ユーティリティを curl](https://curl.haxx.se/)をコマンドラインからの web 要求 (つまり HTTP GET、POST、PUT などのコマンド) を呼び出すことができます。 使用することができます`curl.exe`上記のディストリビューションをダウンロードします。

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

上記の例では、`curl.exe`が実行される (だけでなく`curl`)、PowerShell では、実際の curl の実行可能ファイルが呼び出されると、エイリアスの PowerShell curl ではない[Invoke-webrequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> 注:使用して`curl`が呼び出すスクリプト Cmd シェルを使用してダウンロード手順を実行する必要がある場合に適していますや`.bat`  /  `.cmd`スクリプト。

## <a name="installing-your-distro"></a>ディストリビューションをインストールします。
を、ダウンロードした distro(s) をインストールする方法については、を参照してください、 [Windows デスクトップ](install-win10.md)または[Windows Server](install-on-server.md)インストール手順。
