---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91bd479e922fc29bf11b89dcfe06fa381632c4fa
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520551"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 のインストール手順

WSL2 をインストールする方法については、以下のビデオをご覧になるか、この記事を参照してください。 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

WSL 2 をインストールして使用を開始するには、次の手順を実行します。

> WSL 2 は、Windows 10 ビルド 18917 以降でのみ使用できます

- WSL がインストールされていることを確認し (実行手順は[こちら](./install-win10.md)です)、Windows 10 **ビルド 18917** 以降を実行していることを確認します
   - ビルド 18917 以降を使用していることを確認するには、[Windows Insider Program](https://insider.windows.com/en-us/) に参加し、"ファスト" リングまたは "スロー" リングを選択します。 
   - Windows のバージョンを確認するには、コマンド プロンプトを開き、`ver` コマンドを実行します。
- "仮想マシン プラットフォーム" のオプション コンポーネントを有効にする
- コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する
- 現在のディストリビューションが使用している WSL のバージョンを確認する

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>"仮想マシン プラットフォーム" のオプション コンポーネントを有効にし、WSL が有効であることを確認する

Linux 用 Windows サブシステムと仮想マシン プラットフォームのオプション コンポーネントの両方がインストールされていることを確認する必要があります。 これを行うには、PowerShell で次のコマンドを実行します。 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

両方のコンポーネントのインストールを完了するために、コンピューターを再起動してください。


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する

Linux ディストリビューションがインストールされていない場合は、[Windows 10 へのインストール](./install-win10.md#install-your-linux-distribution-of-choice)に関するドキュメント ページのインストール手順を参照してください。 

ディストリビューションを設定するには、以下を実行します。 

```
wsl --set-version <Distro> 2
```

`<Distro>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。 (これらは、コマンド `wsl -l` を使用して確認できます)。 上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。

また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。

```
wsl --set-default-version 2
```

これにより、インストールする新しいディストリビューションはすべて WSL 2 ディストリビューションとして初期化されます。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>現在のディストリビューションが使用している WSL のバージョンを確認して終了する

各ディストリビューションが使用している WSL のバージョンを確認するには、次のコマンドを使用します (Windows ビルド 18917 以降でのみ使用できます)。

`wsl --list --verbose` または `wsl -l -v`

上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。 これで、WSL 2 ディストリビューションを自由に使い始めることができます。 

## <a name="troubleshooting"></a>トラブルシューティング : 

WSL2 のインストール時の関連エラーと推奨される修正を次に示します。 その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。

* **インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**
    * コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。 これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。
   
* **アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。 WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。 WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。

* **仮想ディスク システムの制限があるため、要求された操作を完了できませんでした。仮想ハード ディスク ファイルは、圧縮と暗号化が解除されている必要があります。また、スパースにすることはできません。**
    * この問題の最新情報が追跡されている [WSL Github スレッド #4103](https://github.com/microsoft/WSL/issues/4103) を参照してください。

* **"wsl" という用語が、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。** 
    * [Linux 用 Windows サブシステムのオプション コンポーネントがインストールされている](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled)ことを確認してください。<br> また、Arm64 デバイスを使用し、PowerShell からこのコマンドを実行している場合も、このエラーを受け取ります。 代わりに、`wsl.exe`PowerShell Core[ またはコマンド プロンプトから ](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) を実行します。 
