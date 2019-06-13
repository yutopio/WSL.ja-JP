---
title: WSL 2 について
description: WSL 2 Windows Subsystem for Linux の新しいアーキテクチャについて
keywords: BashOnWindows、bash、wsl、wsl2、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステムのインストールします。
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b3b0b1ce0f55fed0b4cf223ccc18a509dcf81788
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038132"
---
WSL 2 では、新しいバージョンの Windows で ELF64 Linux バイナリを実行する Linux 用 Windows サブシステムが作動するアーキテクチャです。 その主な目標は、完全なシステムの呼び出しの互換性を追加するとともに、ファイル システムのパフォーマンスを向上させる。 この新しいアーキテクチャでは、これらの Linux バイナリが Windows およびコンピューターのハードウェアとやり取りする方法の変更が、WSL 1 (現在広く普及しているのバージョン) のように、同じユーザー エクスペリエンスが提供されます。 WSL 1 ディストリビューションの場合、または、WSL 2 ディストリビューションでは、ディストリビューションを実行できる個々 の Linux のアップグレードや、いつでもダウン グレードが可能し、サイド バイ サイドの WSL 1 と WSL 2 ディストリビューションを実行することができます。 WSL 2 では、実際の Linux カーネルを使用する、まったく新しいアーキテクチャを使用します。

## <a name="linux-kernel-in-wsl-2"></a>WSL 2 での Linux カーネル

WSL 2 での Linux カーネルは kernel.org で使用可能なソースに基づいた最新の安定したブランチから、社内で構築されています。このカーネルは WSL 2 特別に調整されています。 サイズとパフォーマンスを Windows を驚くほどの Linux のエクスペリエンスを提供するために最適化された、Windows 更新プログラムが処理されますので、自分で管理することがなく、最新のセキュリティ修正プログラムとカーネル機能強化が表示されます。

さらにこのカーネルは、オープン ソースになります。 完全なソース コードを検索するには、Linux カーネルの[ここ](https://thirdpartysource.microsoft.com/download/Windows%20Subsystem%20for%20Linux%20v2/May%202019/WSLv2-Linux-Kernel-master.zip)します。 詳細したい場合については、このカーネルをチェック アウトできます[このブログの投稿](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)のビルド チームによって書き込まれました。

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 アーキテクチャの概要

WSL 2 は、軽量なユーティリティ仮想マシン (VM) 内での Linux カーネルを実行するのに、最新かつ最高の仮想化テクノロジを使用します。 ただし、WSL 2 には、従来の VM エクスペリエンスはできません。 従来の VM のエクスペリエンスは、起動に時間がかかることができます、分離された、多数のリソースを消費、および、時間を管理する必要がありますを。 WSL 2 には、これらの属性はありません。 まだ WSL 1 の非常に大きなメリットが得られます。VM の構成または管理、高レベルの Windows と Linux、非常に高速起動時間、小規模リソースのフット プリント、およびすべての間の統合は必要ありません。 WSL 2 は、VM を使用して、これは、管理され WSL 1 と同じユーザー エクスペリエンスを終了するシーンの背後で実行されます。

## <a name="increased-file-io-performance"></a>ファイル IO パフォーマンスを向上

ファイルの処理を要する操作などの git クローン、npm のインストール、apt 更新プログラム、apt アップグレード、およびすべて非常に高速です。 どのアプリでは、実行して、ファイル システムとの対話方法をしている実際の速度の増加によって異なります。 WSL 2 の最初のバージョンの実行に最大 20 倍の速さの周りを zip 形式の tarball をアンパックし、WSL 1 と比べて 2 ~ 5 倍高速化するさまざまなプロジェクトで git クローン、npm のインストールおよび cmake を使用します。

## <a name="full-system-call-compatibility"></a>完全なシステムの呼び出しの互換性

Linux のバイナリは、ファイルへのアクセス、メモリを要求して、プロセス、および詳細の作成などの多くの機能を実行するのにシステム コールを使用します。 WSL 1 の WSL チームによって構築された変換レイヤーに対して、WSL 2 には、完全なシステムの呼び出しの互換性の独自の Linux カーネルが含まれます。 これには、Docker などの WSL 内で実行できるアプリのまったく新しいセットが導入されています。 さらに、それらを追加、変更を実装し、WSL チームを待つのではなく、Linux カーネルに更新プログラムをすぐに、コンピューターに追加することができます。