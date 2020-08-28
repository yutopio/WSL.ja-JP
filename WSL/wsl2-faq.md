---
title: WSL 2 についてよく寄せられる質問
description: "\"仮想マシンで WSL 2 を実行できますか?\" などの、Linux 用 Windows サブシステム 2 についてよく寄せられる質問 (FAQ) への回答をご確認いただけます。"
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1a55ace547b27c949794db3a6c8f7e2eb7c4a52c
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866002"
---
# <a name="wsl-2-faqs"></a>WSL 2 に関する FAQ

Linux 用 Windows サブシステム 2 についてよく寄せられる質問 (FAQ) の一覧を次に示します。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 に Hyper-V は使用されていますか? Windows 10 Home では使用できるようになりますか?

WSL 2 は、WSL を現在使用できるすべての SKU (Windows 10 Home を含む) 上で使用できます。

最新バージョンの WSL では、仮想化を有効にするために、Hyper-V アーキテクチャが使用されます。 このアーキテクチャは、"仮想マシン プラットフォーム" のオプション コンポーネントで使用できます。 このオプションのコンポーネントは、すべての SKU 上で使用できます。 WSL 2 は間もなくリリースされるため、このエクスペリエンスの詳細をすぐにご確認いただけます。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 はどうなりますか? 廃止されますか?

現在、WSL 1 を廃止する予定はありません。 WSL 1 と WSL 2 のディストリビューションを並行して実行し、任意のディストリビューションをいつでもアップグレードおよびダウングレードできます。 WSL 2 を新しいアーキテクチャとして追加すると、WSL チームにとって、WSL を利用して Windows で Linux 環境を実行する機能を提供するための優れたプラットフォームになります。

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>WSL 2 と、VMware や VirtualBox などの他のサード パーティの仮想化ツールを実行できますか?

一部のサード パーティ アプリケーションは、Hyper-V が使用されている場合は機能しません。つまり、VMware や VirtualBox など、WSL 2 が有効な場合は実行できません。 しかし、VirtualBox と VMware の両方から、Hyper-v と WSL2 をサポートするバージョンが最近リリースされました。 [VirtualBox の変更点についてはこちら][1]から、[VMware の変更点についてはこちら][4]から、それぞれ詳細をご確認いただけます。

Microsoft は、Hyper-V のサードパーティ統合をサポートするソリューションに一貫して取り組んでいます。 たとえば、[Hypervisor Platform][2] という一連の API を公開しています。サードパーティの仮想化プロバイダーはこれを使用してソフトウェアに Hyper-V との互換性を持たせることができます。 これにより、アプリケーションでは、[Google Android Emulator][3] や、Hyper-V と互換性のある VirtualBox 6 以降など、のエミュレーションに Hyper-V アーキテクチャを使用できます。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>WSL 2 の GPU にはアクセスできますか? ハードウェア サポートを強化する予定はありますか?

WSL 2 の初期リリースでは、ハードウェア アクセスのサポートが制限されます。たとえば、GPU、シリアル、または USB デバイスにアクセスできなくなります。 ただし、これらのデバイスを操作したい開発者向けに、より多くのユース ケースが開かれているため、バックログではより優れたデバイス サポートが追加されています。 一方、シリアル ポートにアクセスできる WSL 1 はいつでも使用できます。 このブログと Twitter の WSL チーム メンバーに注目してインサイダー ビルドの最新機能に関する情報を入手し、操作したいデバイスについてフィードバックをお寄せください。

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 ではネットワーク アプリケーションを使用できるようになりますか?

はい。一般的にネットワーク アプリケーションにはシステム コールとの完全な互換性があるため、より高速に、より優れた機能で動作します。 ただし、新しいアーキテクチャには仮想化されたネットワーク コンポーネントが使用されます。 つまり、初期のプレビュー ビルドでは、WSL 2 は仮想マシンと同様に動作します。たとえば、WSL 2 には、ホスト コンピューターとは異なる IP アドレスが割り当てられます。 Microsoft では、WSL 2 のエクスペリエンスが WSL 1 と同じになるように取り組んでいます。これには、ネットワーク ストーリーの改善も含まれます。 localhost を使用して Linux または Windows からすべてのネットワーク アプリにアクセスできるようにするなど、できるだけ早く機能強化を追加する予定です。 WSL 2 のリリースに向けて、ネットワーク ストーリーと改善点に関する詳細を投稿する予定です。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>仮想マシンで WSL 2 を実行できますか?

はい。 仮想マシンで入れ子になった仮想化が有効なことを確認する必要があります。 これを親 Hyper-V ホストで有効にするには、管理者特権を使用して PowerShell ウィンドウで次のコマンドを実行します。

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

"&lt;VMName&gt;" は、実際の仮想マシンの名前に置き換えてください。

## <a name="can-i-use-wslconf-in-wsl-2"></a>WSL 2 で wsl.conf を使用できますか?

WSL 2 では、WSL 1 に使用されているものと同じ wsl.conf ファイルがサポートされています。 つまり、Windows ドライブの自動マウント、相互運用の有効化または無効化、Windows ドライブのマウント先ディレクトリの変更など、WSL 1 ディストリビューションで設定した構成オプションは、すべて WSL 2 内で機能します。 WSL の構成オプションの詳細については、[ディストリビューションの管理](./wsl-config.md)に関するページを参照してください。

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
 [4]: https://blogs.vmware.com/workstation/2020/01/vmware-workstation-tech-preview-20h1.html
