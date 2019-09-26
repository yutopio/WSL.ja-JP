---
title: WSL 2 に関してよく寄せられる質問
description: Windows Subsystem for Linux 2 に関してよく寄せられる質問
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c4a8c02db6563d7ad572917578c1a49d419f1756
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269571"
---
# <a name="wsl-2-faq"></a>WSL 2 に関する FAQ

Windows Subsystem for Linux 2 に関してよく寄せられる質問 (FAQ) の一覧を次に示します。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 は Hyper-v を使用しますか? Windows 10 Home で使用できるようになりますか。

WSL 2 は、WSL が現在利用可能なすべての Sku (Windows 10 Home を含む) で利用できます。

最新バージョンの WSL は、Hyper-v アーキテクチャを使用して仮想化を有効にします。 このアーキテクチャは、"仮想マシンプラットフォーム" のオプションコンポーネントで使用できます。 このオプションのコンポーネントは、すべての Sku で使用できます。 WSL 2 リリースに近いほど、このエクスペリエンスの詳細をすぐに確認できます。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 はどうなりますか。 破棄されますか。

現在、WSL 1 を廃止する予定はありません。 WSL 1 と WSL 2 ディストリビューションを並行して実行し、任意のディストリビューションをいつでもアップグレードおよびダウングレードできます。 WSL 2 を新しいアーキテクチャとして追加すると、wsl チームが Windows で Linux 環境を実行するための優れた方法を提供する機能を提供できるようになります。

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>WSL 2 およびその他のサードパーティの仮想化ツール (VMware や VirtualBox など) を実行できますか?

Hyper-v が使用されている場合、一部のサードパーティアプリケーションが動作しないことを意味します。これは、WSL 2 が有効になっている場合、これらのアプリケーションを実行できないことを意味します。 残念なことに、これには VMware と、VirtualBox 6 より前の VirtualBox のバージョンが含まれます (2018 年12月にリリースされた VirtualBox 6.0.0 では、 [Windows ホストでのフォールバック実行コアとして hyper-v がサポートされるようになりました][1])。

この問題を解決するための方法を調査しています。 たとえば、サードパーティの仮想化プロバイダーが Hyper-v のと互換性のあるソフトウェアを作成するために使用できる[ハイパーバイザープラットフォーム][2]と呼ばれる一連の api を公開しています。 これにより、アプリケーションは、 [Google Android Emulator][3]、virtualbox 6、およびその両方が hyper-v と互換性があるように、そのエミュレーションに hyper-v アーキテクチャを使用できるようになります。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>WSL 2 の GPU にアクセスできますか。 ハードウェアサポートを強化する予定はありますか。

WSL 2 ハードウェアアクセスサポートの初回リリースでは、GPU、serial、USBs にアクセスできなくなる場合があります。 ただし、より優れたデバイスサポートを追加すると、バックログが高くなります。これにより、これらのデバイスとの対話を希望する開発者にとって、より多くのユースケースが開かれます。 それまでの間は、シリアルポートと USB アクセスを持つ WSL 1 をいつでも使用できます。 Twitter でこのブログや WSL チームのメンバーに継続的にご連絡ください。また、対話するデバイスについてのフィードバックをお寄せいただくために、内部で公開されている最新の機能に関する情報を常に入手できます。

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 がネットワークアプリケーションを使用できるようになりますか。

はい。一般的なネットワークアプリケーションでは、システムコールの完全な互換性があるため、より高速で動作します。 ただし、新しいアーキテクチャでは、仮想化されたネットワークコンポーネントが使用されます。 これは、最初のプレビュービルドでは、WSL 2 が仮想マシンに似た動作をすることを意味します。次に例を示します。WSL 2 には、ホストコンピューターとは異なる IP アドレスが割り当てられます。 Wsl 2 を WSL 1 と同じ感覚にすることができます。これには、ネットワークのストーリーの改善が含まれています。 Linux または Windows から localhost を使用してすべてのネットワークアプリにアクセスするなど、可能な限り迅速に機能強化を追加する予定です。 ここでは、WSL 2 のリリースに向けたネットワークの事例と改善点について詳しく説明します。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>仮想マシンで WSL 2 を実行できますか。

はい。 仮想マシンで、入れ子になった仮想化が有効になっていることを確認する必要があります。 これは、管理者特権のある PowerShell ウィンドウで次のコマンドを実行して、親 Hyper-v ホストで有効にすることができます。

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

必ず '&lt;VMName&gt;' を仮想マシンの名前に置き換えてください。

## <a name="can-i-use-wslconf-in-wsl-2"></a>WSL 2 で wsl を使用できますか。

WSL 2 は、WSL 1 が使用するのと同じ wsl conf ファイルをサポートしています。 これは、WSL 1 ディストリビューションで設定されたすべての構成オプション (Windows ドライブの automounting、相互運用の有効化または無効化、Windows ドライブがマウントされるディレクトリの変更など) が wsl 2 の内部で動作することを意味します。 WSL の構成オプションの詳細については、「[ディストリビューション管理](./wsl-config.md)」ページを参照してください。 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
