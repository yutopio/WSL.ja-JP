---
title: WSL 2 について
description: WSL 2 について Windows Subsystem for Linux の新しいアーキテクチャ
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 983699c26a21af7b81ba31067316ba3bbf1601af
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020934"
---
# <a name="about-wsl-2"></a>WSL 2 について

WSL 2 は、windows Subsystem for Linux が Windows 上で ELF64 Linux バイナリを実行できるようにする、アーキテクチャの新しいバージョンです。 主な目的は、ファイルシステムのパフォーマンスを向上させたり、システムコールの完全な互換性を追加したりすることです。 この新しいアーキテクチャは、これらの Linux バイナリが Windows とコンピューターのハードウェアとどのように対話するかを変更しますが、WSL 1 (現在幅広く使用可能なバージョン) と同じユーザーエクスペリエンスを提供します。 個々の Linux ディストリビューションは WSL 1 ディストリビューションとして実行するか、WSL 2 ディストリビューションとして実行できます。また、いつでもアップグレードまたはダウングレードできます。 WSL 1 と WSL 2 ディストリビューションを並行して実行できます。 WSL 2 は、実際の Linux カーネルを使用するまったく新しいアーキテクチャを使用します。

## <a name="linux-kernel-in-wsl-2"></a>WSL 2 の Linux カーネル

WSL 2 の Linux カーネルは、kernel.org で入手できるソースに基づいて、最新の安定したブランチから社内に構築されています。このカーネルは WSL 2 用に特別に調整されています。 サイズとパフォーマンスのために最適化されており、Windows での優れた Linux エクスペリエンスを提供し、Windows の更新プログラムによってサービスを提供します。つまり、自分で管理することなく、最新のセキュリティ修正とカーネルの改善を受けることができます。

さらに、このカーネルはオープンソースになります。 Linux カーネルの完全なソースコードについては、[こちら](https://github.com/microsoft/WSL2-Linux-Kernel)を参照してください。 このカーネルの詳細については、このカーネルを構築したチームによって記述された[このブログ記事](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)をご覧ください。

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 アーキテクチャの概要

WSL 2 では、仮想化テクノロジの最新で最高のものを使用して、ライトウェイトユーティリティ仮想マシン (VM) 内で Linux カーネルを実行します。 ただし、WSL 2 は従来の VM エクスペリエンスではありません。 従来の VM エクスペリエンスは起動に時間がかかり、分離され、大量のリソースを消費するため、管理に時間がかかることがあります。 WSL 2 には、これらの属性はありません。 WSL 1 には次のような利点があります。Windows と Linux の間の高いレベルの統合、非常に高速な起動時間、小規模なリソースフットプリント、最大限のメリットを実現するには、VM の構成または管理は必要ありません。 WSL 2 では VM を使用しますが、WSL 1 と同じユーザーエクスペリエンスが得られるように、管理され、バックグラウンドで実行されます。

## <a name="increased-file-io-performance"></a>ファイル IO パフォーマンスの向上

Git clone、npm install、apt update、apt upgrade など、ファイルを多用する操作はすべて、非常に高速になります。 実際の速度の増加は、実行しているアプリとファイルシステムとの対話方法によって異なります。 最初のバージョンの WSL 2 は、zip 圧縮された tar を開梱する場合は WSL 1、git clone を使用する場合は約2倍速、さまざまなプロジェクトでは npm install と cmake の方が、20倍まで高速に実行できます。

## <a name="full-system-call-compatibility"></a>システムコールの完全な互換性

Linux バイナリでは、システム呼び出しを使用して、ファイルへのアクセス、メモリの要求、プロセスの作成など、さまざまな機能を実行します。 Wsl 1 では、WSL チームによって作成された翻訳レイヤーが使用されていましたが、WSL 2 には、システムコールの完全な互換性を備えた独自の Linux カーネルが含まれています。 これにより、Docker などの WSL 内で実行できるアプリの完全なセットが導入されます。 また、Linux カーネルに対する更新は、WSL チームが変更を実装して追加するのを待機するのではなく、すぐにコンピューターに追加することができます。