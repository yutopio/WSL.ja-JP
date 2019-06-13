---
title: WSL 2 をインストールします。
description: WSL 2 のインストール手順
keywords: BashOnWindows、bash、wsl、wsl2、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステムのインストールします。
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038082"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 のインストール手順

インストールして開始には、WSL 2 は、次の手順を完了します。

- '仮想マシン プラットフォーム' オプションのコンポーネントを有効にします。
- WSL 2 のコマンドラインを使用してバックアップするディストリビューションを設定します。
- 使用している WSL、ディストリビューションのバージョン確認します。

## <a name="enable-the-virtual-machine-platform-optional-component"></a>'仮想マシン プラットフォーム' オプションのコンポーネントを有効にします。

管理者として PowerShell を開きを実行します。

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

これらの変更が有効にした後、コンピューターを再起動する必要があります。

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>WSL 2 のコマンドラインを使用してバックアップするディストリビューションを設定します。

Powershell を実行します。

`wsl --set-version <Distro> 2`

置き換えてくださいと`<Distro>`ディストリビューションの実際の名前に置き換えます。 (これらは、コマンドを使用して: `wsl -l`)。 上記と同じコマンドを実行して、' 2' で ' 1' に置き換えることによって WSL 1 にいつでも変更することができます。

さらに、WSL 2 に、既定のアーキテクチャを作成する場合は、これを行う次のコマンドで。

`wsl --set-default-version 2`

これにより、いずれかをインストールする新しいディストリビューション WSL 2 ディストリビューションとして初期化します。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>使用している WSL、ディストリビューションのバージョンの確認が完了します。

次のコマンドを使用して、各ディストリビューションを使用して WSL のバージョンを確認します。

`wsl --list --verbose` または `wsl -l -v`

上の選択したディストリビューションは、'2'、'version' 列の下を表示する必要があります。 完了したら、WSL 2 ディストリビューションを使用する自由! 