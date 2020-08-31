---
title: WSL 2 について
description: Linux 用 Windows サブシステムの新しいアーキテクチャである WSL 2 について説明します。 このアーキテクチャの概要および Linux カーネルに関する情報をお読みください。
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: bfb0e14ce53d3022dba06340630cc97a1286a13f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866120"
---
# <a name="about-wsl-2"></a>WSL 2 について

WSL 2 は、Windows 上の Linux 用 Windows サブシステムで ELF64 Linux バイナリを実行できるようになる新しいバージョンのアーキテクチャです。 その主な目標は、ファイル システムのパフォーマンスを向上させることと、システム コールの完全な互換性を追加することです。 この新しいアーキテクチャによって、こうした Linux バイナリと、Windows やお使いのコンピューターのハードウェアとの対話方法は変わりますが、ユーザー エクスペリエンスは WSL 1 (現在幅広く利用されているバージョン) と同じです。 個々の Linux ディストリビューションは、WSL 1 ディストリビューションまたは WSL 2 ディストリビューションとして実行でき、いつでもアップグレードまたはダウングレードできます。また、WSL 1 ディストリビューションと WSL 2 ディストリビューションを並行して実行できます。 WSL 2 には、実際の Linux カーネルを使用するまったく新しいアーキテクチャが使用されています。

## <a name="linux-kernel-in-wsl-2"></a>WSL 2 の Linux カーネル

WSL 2 の Linux カーネルは、kernel.org で入手できるソースに基づいて、最新の安定したブランチから Microsoft 内で構築されています。このカーネルは、WSL 2 用に特別に調整されています。 サイズとパフォーマンスが最適化されており、Windows 上で優れた Linux エクスペリエンスを実現できます。また、Windows の更新プログラムを介してサービスが提供されます。つまり、自分で管理することなく、最新のセキュリティ修正プログラムとカーネルの機能強化を利用できます。

さらに、このカーネルはオープン ソースになります。 Linux カーネルの完全なソース コードについては、[こちら](https://github.com/microsoft/WSL2-Linux-Kernel)を参照してください。 このカーネルの詳細については、構築したチームが執筆した[このブログ投稿](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)を参照してください。

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 アーキテクチャの概要

軽量のユーティリティ仮想マシン (VM) 内で Linux カーネルを実行するために、WSL 2 には最新かつ最高の仮想化テクノロジが使用されています。 ただし、WSL 2 は従来の VM エクスペリエンスではありません。 従来の VM エクスペリエンスは起動に時間がかかり、分離され、大量のリソースが消費され、管理に時間がかかります。 WSL 2 にこのような特徴はありません。 それでも WSL 1 には次のような利点があります。Windows と Linux 間の高度な統合、非常に高速な起動時間、小規模なリソース フットプリント、そして何よりも VM の構成や管理が不要であることです。 WSL 2 には VM が使用されますが、バックグラウンドで管理および実行されるので、WSL 1 とユーザー エクスペリエンスは同じです。

## <a name="increased-file-io-performance"></a>ファイル IO パフォーマンスの向上

`git clone`、`npm install`、`apt update`、`apt upgrade` などのファイル集中型の操作は、いずれも非常に高速になります。 実際どのくらい高速になるかは、実行しているアプリと、ファイル システムとの対話方法によって変わります。 初期バージョンの WSL 2 は、zip 圧縮された tarball を展開する場合、WSL 1 と比べて最大 20 倍速く、さまざまなプロジェクトで `git clone`、`npm install`、および `cmake` を使用する場合、約 2 倍から 5 倍速くなります。

## <a name="full-system-call-compatibility"></a>システム コールの完全な互換性

ファイルへのアクセス、メモリの要求、プロセスの作成など、多くの機能を実行するために、Linux バイナリにはシステム コールを使用されています。 WSL 1 では WSL チームが構築した変換レイヤーが使用されていましたが、WSL 2 にはシステム コールの完全な互換性を持つ独自の Linux カーネルが含まれています。 これにより、Docker など、WSL 内で実行できる一連のアプリが一新されました。 さらに、Linux カーネルの更新プログラムがリリースされると、すぐにコンピューターに追加できます。WSL チームが変更を実装して追加するまで待つ必要はありません。
