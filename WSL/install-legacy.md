---
title: インストールまたは Windows 10 Anniversary Update または Creators Update の削除
description: 従来、Windows 10 Anniversary Update または Creators Update のベータ版のディストリビューションのインストールとアンインストールの手順
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10、レガシ、ベータ版の windows サブシステムのインストール、削除、アンインストール、アンインストール、削除、非推奨とされます
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040837"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>インストールまたは Windows 10 Anniversary Update および Creators Update での Linux 用 Windows サブシステムをアンインストール ガイド 

Windows 10 Creators Update を実行しているか、後で、ください[Windows 10 のインストール手順に従って](install-win10.md)します。

<strong><em><span style="color: #f28014">次の手順は Windows 10 Anniversary Update または Windows 10 Creators Update を実行しているユーザーです。</span></em></strong>

Windows 10 Fall Creators Update (バージョン 1709)、前に、WSL は、ベータ機能としてリリースされましたし、"Bash で Ubuntu の Windows"(または Bash.exe) を最初に実行時に、1 つの Ubuntu インスタンスをインストールします。

> WSL を使用して、以前の Windows 10 リリースでは、このベータ版「レガシ ディストリビューション」を古いと見なされますようになりました。 使用可能な Windows 10 の最新バージョンを実行すること強く勧めします。 新しい Windows 10 リリースには、これまで以上の Linux ツールと WSL では正しく動作するアプリを許可するだけで、WSL で何百も修正プログラムと機能強化にはが含まれています。

Fall Creators Update 以降をアップグレードできない場合は、有効にして WSL を使用するのには、次の手順に従います。

1. 開発者モード WSL またはで実行する Windows 10 Anniversary Update Creators Update を有効に、開発者モードを有効にする必要があります。

    開いている**設定** -> **更新とセキュリティ** -> **開発者向け**

    開発者モードのオプション ボタンを選択します。  
    ![開発者モードを有効にする](media/updateAndSecurity.png)

    > 開発者モードを有効にするための要件が[Windows 10 Fall Creators Update での削除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. コマンド プロンプトを開きます。  型`bash`し、enter キーを押します

    初めてでは、Windows、Ubuntu 上で Bash を実行する、Canonical のライセンスに同意するよう求めします。 同意すると、WSL はダウンロードして、コンピューター上に Ubuntu インスタンスをインストールし、"Bash で Ubuntu の Windows"ショートカットが [スタート] メニューに追加します。

    ![Ubuntu をインストールするプロンプト](media/bashShellInstall.png)

    初めての Windows、Ubuntu 上で Bash を実行するは促さ UNIX ユーザー名とパスワードを作成します。 に従って、[ディストリビューション インスタンスの新しい命令](initialize-distro.md)インストールを完了するには

1. いずれかで、新しい Ubuntu シェルを起動します。
    * 実行している`bash`コマンド プロンプトから
    * [スタート] メニューの"Bash で Ubuntu の Windows"ショートカットをクリックします。

    
## <a name="uninstallingremoving-the-legacy-distro"></a>従来のディストリビューションをアンインストール/削除
WSL をインストールした以前の Windows 10 リリースから Windows 10 Fall Creators Update にアップグレードする場合、既存のディストリビューションがそのまま残ります。 ただし、厳密にストアによって提供される新しいディストリビューション至急をインストールすることをお勧めし、必要なファイル、データなどを従来のディストリビューションから、新しいディストリビューションに移行します。

従来のディストリビューションをコンピューターからを削除するには、コマンドラインまたは PowerShell のインスタンスから、次を実行します。

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>従来のディストリビューションを手動で削除します。
希望されない場合、従来のインスタンスを手動で削除することができます。 これは、必要がありますを使用して、従来のディストリビューションのアンインストールで問題が発生した場合`lxrun.exe`、または Windows 10 のスプリング 2018 Update を実行している (またはそれ以降) でこれを出荷しません`lxrun.exe`します。

従来、WSL ディストリビューションを強制的に削除するには、削除、`%localappdata%\lxss\`フォルダー (すべてとサブフォルダーの内容の) Windows のエクスプ ローラーまたはコマンドラインを使用して。

PowerShell を使用する
```powershell
rm -Recurse $env:localappdata/lxss/
```

Cmd を使用します。
```console
DEL /S %localappdata%\lxss\
```
