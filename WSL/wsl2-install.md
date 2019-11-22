---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a53e6a986813809d0c355b80b3fe3028adb21375
ms.sourcegitcommit: 73f4cc6ac9482ea9727f3cda0ec5c3572e164256
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2019
ms.locfileid: "74309048"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 のインストール手順

WSL 2 をインストールして使用を開始するには、次の手順を実行します。

> WSL 2 is only available in Windows 10 builds 18917 or higher

- Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher
   - To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring. 
   - You can check your Windows version by opening Command Prompt and running the `ver` command.
- "仮想マシン プラットフォーム" のオプション コンポーネントを有効にする
- コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する
- 現在のディストリビューションが使用している WSL のバージョンを確認する

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled

You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed. You can do that by running the following command in PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Please restart your machine to finish installing both components.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する

If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one. 

To set a distro please run: 

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

To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):

`wsl --list --verbose` または `wsl -l -v`

上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。 これで、WSL 2 ディストリビューションを自由に使い始めることができます。 

## <a name="troubleshooting"></a>トラブルシューティング: 

WSL2 のインストール時の関連エラーと推奨される修正を次に示します。 その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。

* **インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**
    * コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。 これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。
   
* **アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。 WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。 WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。

* **The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**
    * Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.

* **The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.** 
    * Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error. Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt. 
