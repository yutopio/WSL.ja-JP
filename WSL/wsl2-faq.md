---
title: WSL 2 についてよく寄せられる質問
description: "\"仮想マシンで WSL 2 を実行できますか?\" などの、Linux 用 Windows サブシステム 2 についてよく寄せられる質問 (FAQ) への回答をご確認いただけます。"
keywords: BashOnWindows, bash, wsl, wsl2, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10, インストール
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: a021dc3c6c3c2a14fea631f2733d2b846c6fe3ad
ms.sourcegitcommit: 910845e9b3f980b2c5b9b4968331a706720603c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2020
ms.locfileid: "89058487"
---
# <a name="wsl-2-faqs"></a><span data-ttu-id="f2d9d-104">WSL 2 に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="f2d9d-104">WSL 2 FAQs</span></span>

<span data-ttu-id="f2d9d-105">Linux 用 Windows サブシステム 2 についてよく寄せられる質問 (FAQ) の一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-105">Below is a list of frequently asked questions (FAQ) about the Windows Subsystem for Linux 2.</span></span>

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a><span data-ttu-id="f2d9d-106">WSL 2 に Hyper-V は使用されていますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-106">Does WSL 2 use Hyper-V?</span></span> <span data-ttu-id="f2d9d-107">Windows 10 Home では使用できるようになりますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-107">Will it be available on Windows 10 Home?</span></span>

<span data-ttu-id="f2d9d-108">WSL 2 は、WSL を現在使用できるすべての SKU (Windows 10 Home を含む) 上で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-108">WSL 2 is available on all SKUs where WSL is currently available, including Windows 10 Home.</span></span>

<span data-ttu-id="f2d9d-109">最新バージョンの WSL では、仮想化を有効にするために、Hyper-V アーキテクチャが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-109">The newest version of WSL uses Hyper-V architecture to enable its virtualization.</span></span> <span data-ttu-id="f2d9d-110">このアーキテクチャは、"仮想マシン プラットフォーム" のオプション コンポーネントで使用できます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-110">This architecture will be available in the 'Virtual Machine Platform' optional component.</span></span> <span data-ttu-id="f2d9d-111">このオプションのコンポーネントは、すべての SKU 上で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-111">This optional component will be available on all SKUs.</span></span> <span data-ttu-id="f2d9d-112">WSL 2 は間もなくリリースされるため、このエクスペリエンスの詳細をすぐにご確認いただけます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-112">You can expect to see more details about this experience soon as we get closer to the WSL 2 release.</span></span>

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a><span data-ttu-id="f2d9d-113">WSL 1 はどうなりますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-113">What will happen to WSL 1?</span></span> <span data-ttu-id="f2d9d-114">廃止されますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-114">Will it be abandoned?</span></span>

<span data-ttu-id="f2d9d-115">現在、WSL 1 を廃止する予定はありません。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-115">We currently have no plans to deprecate WSL 1.</span></span> <span data-ttu-id="f2d9d-116">WSL 1 と WSL 2 のディストリビューションを並行して実行し、任意のディストリビューションをいつでもアップグレードおよびダウングレードできます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-116">You can run WSL 1 and WSL 2 distros side by side, and can upgrade and downgrade any distro at any time.</span></span> <span data-ttu-id="f2d9d-117">WSL 2 を新しいアーキテクチャとして追加すると、WSL チームにとって、WSL を利用して Windows で Linux 環境を実行する機能を提供するための優れたプラットフォームになります。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-117">Adding WSL 2 as a new architecture presents a better platform for the WSL team to deliver features that make WSL an amazing way to run a Linux environment in Windows.</span></span>

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a><span data-ttu-id="f2d9d-118">WSL 2 と、VMware や VirtualBox などの他のサード パーティの仮想化ツールを実行できますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-118">Will I be able to run WSL 2 and other 3rd party virtualization tools such as VMware, or VirtualBox?</span></span>

<span data-ttu-id="f2d9d-119">一部のサード パーティ アプリケーションは、Hyper-V が使用されている場合は機能しません。つまり、VMware や VirtualBox など、WSL 2 が有効な場合は実行できません。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-119">Some 3rd party applications cannot work when Hyper-V is in use, which means they will not be able to run when WSL 2 is enabled, such as VMware and VirtualBox.</span></span> <span data-ttu-id="f2d9d-120">しかし、VirtualBox と VMware の両方から、Hyper-v と WSL2 をサポートするバージョンが最近リリースされました。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-120">However, recently both VirtualBox and VMware have released versions that support Hyper-V and WSL2!</span></span> <span data-ttu-id="f2d9d-121">[VirtualBox の変更点についてはこちら][1]から、[VMware の変更点についてはこちら][4]から、それぞれ詳細をご確認いただけます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-121">You can learn more about [VirtualBox's changes here][1] and [VMware's changes here][4].</span></span>

<span data-ttu-id="f2d9d-122">Microsoft は、Hyper-V のサードパーティ統合をサポートするソリューションに一貫して取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-122">We are consistently working on solutions to support third-party integration of Hyper-V.</span></span> <span data-ttu-id="f2d9d-123">たとえば、[Hypervisor Platform][2] という一連の API を公開しています。サードパーティの仮想化プロバイダーはこれを使用してソフトウェアに Hyper-V との互換性を持たせることができます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-123">For example, we expose a set of APIs called [Hypervisor Platform][2] that third-party virtualization providers can use to make their software compatible with Hyper-V.</span></span> <span data-ttu-id="f2d9d-124">これにより、アプリケーションでは、[Google Android Emulator][3] や、Hyper-V と互換性のある VirtualBox 6 以降など、のエミュレーションに Hyper-V アーキテクチャを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-124">This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3], and VirtualBox 6 and above which are both now compatible with Hyper-V.</span></span>

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a><span data-ttu-id="f2d9d-125">WSL 2 の GPU にはアクセスできますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-125">Can I access the GPU in WSL 2?</span></span> <span data-ttu-id="f2d9d-126">ハードウェア サポートを強化する予定はありますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-126">Are there plans to increase hardware support?</span></span>

<span data-ttu-id="f2d9d-127">WSL 2 ディストリビューション内の GPU にアクセスするためのサポートがリリースされました。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-127">We have released support for accessing the GPU inside of WSL 2 distros!</span></span> <span data-ttu-id="f2d9d-128">これは、ビッグ データ セットが関係している場合に、機械学習、人工知能、データ サイエンスのシナリオで WSL をより簡単に使用できるようになったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-128">This means you can now use WSL for machine learning, artificial intelligence, and data science scenarios more easily when big data sets are involved.</span></span> <span data-ttu-id="f2d9d-129">[こちらで、GPU サポートの概要](./tutorials/gpu-compute)に関するチュートリアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-129">You can find a tutorial to [get started with GPU support here](./tutorials/gpu-compute).</span></span> <span data-ttu-id="f2d9d-130">現時点では、WSL 2 にはシリアル サポートや USB デバイス サポートは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-130">As of right now WSL 2 does not include serial support, or USB device support.</span></span> <span data-ttu-id="f2d9d-131">Microsoft では、これらの機能を追加するための最適な方法を調査しています。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-131">We are investigating the best way to add these features.</span></span>

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a><span data-ttu-id="f2d9d-132">WSL 2 ではネットワーク アプリケーションを使用できるようになりますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-132">Will WSL 2 be able to use networking applications?</span></span>

<span data-ttu-id="f2d9d-133">はい。一般的にネットワーク アプリケーションにはシステム コールとの完全な互換性があるため、より高速に、より優れた機能で動作します。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-133">Yes, in general networking applications will be faster and work better since we have full system call compatibility.</span></span> <span data-ttu-id="f2d9d-134">ただし、新しいアーキテクチャには仮想化されたネットワーク コンポーネントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-134">However, the new architecture uses virtualized networking components.</span></span> <span data-ttu-id="f2d9d-135">つまり、初期のプレビュー ビルドでは、WSL 2 は仮想マシンと同様に動作します。たとえば、WSL 2 には、ホスト コンピューターとは異なる IP アドレスが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-135">This means that in initial preview builds WSL 2 will behave more similarly to a virtual machine, e.g: WSL 2 will have a different IP address than the host machine.</span></span> <span data-ttu-id="f2d9d-136">Microsoft では、WSL 2 のエクスペリエンスが WSL 1 と同じになるように取り組んでいます。これには、ネットワーク ストーリーの改善も含まれます。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-136">We are committed to making WSL 2 feel the same as WSL 1, and that includes improving our networking story.</span></span> 

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a><span data-ttu-id="f2d9d-137">仮想マシンで WSL 2 を実行できますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-137">Can I run WSL 2 in a virtual machine?</span></span>

<span data-ttu-id="f2d9d-138">はい。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-138">Yes!</span></span> <span data-ttu-id="f2d9d-139">仮想マシンで入れ子になった仮想化が有効なことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-139">You need to make sure that the virtual machine has nested virtualization enabled.</span></span> <span data-ttu-id="f2d9d-140">これを親 Hyper-V ホストで有効にするには、管理者特権を使用して PowerShell ウィンドウで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-140">This can be enabled in your parent Hyper-V host by running the following command in a PowerShell window with Administrator privileges:</span></span>

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

<span data-ttu-id="f2d9d-141">"&lt;VMName&gt;" は、実際の仮想マシンの名前に置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-141">Make sure to replace '&lt;VMName&gt;' with the name of your virtual machine.</span></span>

## <a name="can-i-use-wslconf-in-wsl-2"></a><span data-ttu-id="f2d9d-142">WSL 2 で wsl.conf を使用できますか?</span><span class="sxs-lookup"><span data-stu-id="f2d9d-142">Can I use wsl.conf in WSL 2?</span></span>

<span data-ttu-id="f2d9d-143">WSL 2 では、WSL 1 に使用されているものと同じ wsl.conf ファイルがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-143">WSL 2 supports the same wsl.conf file that WSL 1 uses.</span></span> <span data-ttu-id="f2d9d-144">つまり、Windows ドライブの自動マウント、相互運用の有効化または無効化、Windows ドライブのマウント先ディレクトリの変更など、WSL 1 ディストリビューションで設定した構成オプションは、すべて WSL 2 内で機能します。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-144">This means that any configuration options that you had set in a WSL 1 distro, such as automounting Windows drives, enabling or disabling interop, changing the directory where Windows drives will be mounted, etc. will all work inside of WSL 2.</span></span> <span data-ttu-id="f2d9d-145">WSL の構成オプションの詳細については、[ディストリビューションの管理](./wsl-config.md)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2d9d-145">You can learn more about the configuration options in WSL in the [Distro Management](./wsl-config.md) page.</span></span>

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
 [4]: https://blogs.vmware.com/workstation/2020/01/vmware-workstation-tech-preview-20h1.html
