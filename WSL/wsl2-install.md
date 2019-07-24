---
title: WSL 2 のインストール
description: WSL 2 のインストール手順
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3ad180ecc9deaa1566e9870700b26f82f631c7f1
ms.sourcegitcommit: 9ad7a54668f39677e9660186e4f5172ea2597e2b
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2019
ms.locfileid: "68246864"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 のインストール手順

WSL 2 をインストールして使用を開始するには、次の手順を実行します。

- "仮想マシン プラットフォーム" のオプション コンポーネントを有効にする
- コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する
- 現在のディストリビューションが使用している WSL のバージョンを確認する

WSL 2 を使用するには Windows 10 ビルド 18917 以降を実行している必要があり、また WSL が既にインストールされている必要があることに注意してください(そのようにするための手順については、[こちら](./install-win10.md)を参照してください)。 

## <a name="enable-the-virtual-machine-platform-optional-component"></a>"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする

管理者として PowerShell を開き、以下を実行します。

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

これらの変更を有効にした後、コンピューターを再起動する必要があります。

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>コマンド ラインを使用して、WSL 2 によってサポートされるようにディストリビューションを設定する

PowerShell で、以下を実行します。

`wsl --set-version <Distro> 2`

`<Distro>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。 (これらは、コマンド `wsl -l` を使用して確認できます)。 上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。

また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。

`wsl --set-default-version 2`

これにより、インストールする新しいディストリビューションはすべて WSL 2 ディストリビューションとして初期化されます。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>現在のディストリビューションが使用している WSL のバージョンを確認して終了する

各ディストリビューションでどのバージョンの WSL が使用されているかを確認するには、次のコマンドを使用します。

`wsl --list --verbose` または `wsl -l -v`

上記で選択したディストリビューションで、 [version] 列に "2" と表示されるはずです。 これで、WSL 2 ディストリビューションを自由に使い始めることができます。 

## <a name="troubleshooting"></a>トラブルシューティング: 

WSL2 のインストール時の関連エラーと推奨される修正を次に示します。 その他の一般的な WSL エラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。

* **インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**
    * コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。 これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。
   
* **アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Windows Subsystem for Linux が有効になっていること、および Windows ビルド バージョン 18917 以降を使用していることを確認してください。 WSL を有効にするには、Powershell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。 WSL のインストール手順の詳細については、[こちら](./install-win10.md)を参照してください。