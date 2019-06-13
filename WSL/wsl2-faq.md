---
title: WSL 2 についてよく寄せられる質問
description: Linux 2 用 Windows サブシステムに関するよく寄せられる質問
keywords: BashOnWindows、bash、wsl、wsl2、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステムのインストールします。
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038092"
---
# <a name="wsl-2-faq"></a>WSL 2 に関する FAQ

よく寄せられる質問 (FAQ)、Windows サブシステム Linux 2 の一覧を以下に示します。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 は、HYPER-V を使用しますか。 リリースされる予定の Windows 10 Home でしょうか。

WSL 2 は、WSL が現在使用可能な Windows 10 Home を含む、すべての Sku で利用可能なであるされます。

WSL の最新のバージョンでは、仮想化を有効にするのに HYPER-V のアーキテクチャを使用します。 このアーキテクチャは、HYPER-V 機能のサブセットであるオプションのコンポーネントで使用できるになります。 このオプションのコンポーネントは、すべての Sku で利用できるになります。 WSL 2 リリースに近づくにつれてすぐにこのエクスペリエンスについての詳細情報を確認したいことができます。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 になるか。 その見向きもされなくなりますか。

います現在ある WSL 1 を廃止する予定はありません。 WSL 1 と 2 の WSL ディストリビューション サイド バイ サイドで実行しできますアップグレードでき、いつでもすべてのディストリビューションをダウン グレードできます。 新しいアーキテクチャとして WSL 2 を追加するには、WSL を驚くような方法で Windows、Linux 環境を実行するようにする機能を提供する、WSL チームに適したプラットフォームについて説明します。

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>ある WSL 2 と VMware、VirtualBox などその他のサード パーティ製の仮想化ツールを実行するでしょうか。

HYPER-V が、WSL 2 が有効になっているときに実行できない、使用されている場合、一部のサード パーティ アプリケーションは使用できません。 残念ながら、これは、VMware と VirtualBox VirtualBox 6 以前のバージョン (VirtualBox 2018 の年 12 月にリリースされた 6.0.0 [Windows ホスト上のフォールバック実行コアとして HYPER-V を今すぐサポート][ 1]!)

この問題を解決するための方法を調査しています。 たとえばと呼ばれる Api のセットを公開します[ハイパーバイザー プラットフォーム][ 2]サード パーティ製の仮想化のプロバイダーを使用して、そのソフトウェアと HYPER-V の互換性のあること これにより、アプリケーションなど、エミュレーションの HYPER-V のアーキテクチャを使用して[Google Android Emulator][3]と 6 およびこれを超える VirtualBox の両方の HYPER-V と互換性のあるようになりました。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>WSL 2 での GPU にアクセスできますか。 ハードウェアのサポートを向上する計画はありますか。

WSL 2 ハードウェアへのアクセスの最初のリリースでサポートが限られておりにある例:: GPU、シリアル アクセスまたは Usb ができないことができます。 ただしより優れたデバイス サポートを追加するは、バックログで高いようにこれらのデバイスとの対話を希望する開発者の多くの複数のユース ケースが開きます。 それまでは、シリアル ポート、および USB のアクセスを持つ WSL 1 を必ず使用することができます。 このブログと内部関係者に、最新の機能について把握する twitter WSL チーム メンバーに引き続き注目がビルドし、対話するにはどのようなデバイスについてフィードバックを提供することにご連絡ください!

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 はネットワーク アプリケーションを使用できますか。

はい、アプリケーションを一般にネットワークが高速で、互換性を呼び出す完全なシステムがあるために、適しています。 ただし、新しいアーキテクチャは、仮想化されたネットワーク コンポーネントを使用します。 つまり、初期のプレビュー ビルド WSL 2 は、仮想マシンと同様により動作が例。WSL 2 では、ホスト コンピューターは異なる IP アドレスがあります。 WSL 1 と同じと感じる WSL 2 の提供に取り組んでいますが、ネットワーク アジャイル チームのストーリーの向上が含まれます。 Linux または localhost を使用して Windows からネットワークのすべてのアプリへのアクセスなど、することが簡単に機能強化を追加する予定です。 WSL 2 のリリースに近いので、ネットワーク、ストーリーと機能強化についての詳細について掲載する予定です。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>仮想マシンで WSL 2 を実行できますか。

うん！ 仮想マシンに仮想化が有効に入れ子になったことを確認する必要があります。 これは、管理者特権で PowerShell ウィンドウで、次のコマンドを実行して、HYPER-V で有効ことができます。

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

置き換えてください '&lt;VMName&gt;' 仮想マシンの名前に置き換えます。

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/