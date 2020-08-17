---
title: WSL 2 と WSL 1 の比較
description: Linux 用 Windows サブシステムのバージョン 1 とバージョン 2 を比較します。 ヒント - バージョン 2 では、実際の Linux カーネルが実行され、パフォーマンスが向上し、より高速になりますが、Windows と Linux の両方のファイル システムで作業している場合は WSL 1 が適しています。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux, ubuntu, debian, suse, windows 10, UX の変更, WSL 2, linux カーネル, ネットワーク アプリケーション, localhost, IPv6, 仮想ハードウェア ディスク, VHD, VHD の制限, VHD エラー
ms.date: 07/22/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f64eff318ead5b74356a1b7db435952d4d4e669b
ms.sourcegitcommit: 90577817a9321949da2a3971b4c78bb00f6d977f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/10/2020
ms.locfileid: "88039425"
---
# <a name="comparing-wsl-1-and-wsl-2"></a><span data-ttu-id="53858-105">WSL 1 と WSL 2 の比較</span><span class="sxs-lookup"><span data-stu-id="53858-105">Comparing WSL 1 and WSL 2</span></span>

<span data-ttu-id="53858-106">Linux 用 Windows サブシステムを新しいバージョンに更新する主な目的は、**ファイル システムのパフォーマンスを向上させ**、**システム コールの完全な互換性**をサポートすることです。</span><span class="sxs-lookup"><span data-stu-id="53858-106">The primary goals of updating the Windows Subsystem for Linux to a new version are to **increase file system performance** and support **full system call compatibility**.</span></span> 

<span data-ttu-id="53858-107">軽量のユーティリティ仮想マシン (VM) 内で Linux カーネルを実行するために、WSL 2 には最新の優れた仮想化テクノロジが使用されています。</span><span class="sxs-lookup"><span data-stu-id="53858-107">WSL 2 uses the latest and greatest in virtualization technology to run a Linux kernel inside of a lightweight utility virtual machine (VM).</span></span> <span data-ttu-id="53858-108">ただし、WSL 2 は従来の VM エクスペリエンスではありません。</span><span class="sxs-lookup"><span data-stu-id="53858-108">However, WSL 2 is not a traditional VM experience.</span></span> <span data-ttu-id="53858-109">[WSL 2 アーキテクチャの詳細については、こちらをご覧ください](#wsl-2-architecture)。</span><span class="sxs-lookup"><span data-stu-id="53858-109">[Learn more about the WSL 2 architecture](#wsl-2-architecture).</span></span>

## <a name="comparing-features"></a><span data-ttu-id="53858-110">機能の比較</span><span class="sxs-lookup"><span data-stu-id="53858-110">Comparing features</span></span>

<span data-ttu-id="53858-111">機能</span><span class="sxs-lookup"><span data-stu-id="53858-111">Feature</span></span> | <span data-ttu-id="53858-112">WSL 1</span><span class="sxs-lookup"><span data-stu-id="53858-112">WSL 1</span></span> | <span data-ttu-id="53858-113">WSL 2</span><span class="sxs-lookup"><span data-stu-id="53858-113">WSL 2</span></span>
--- | --- | ---
 <span data-ttu-id="53858-114">Windows と Linux の統合</span><span class="sxs-lookup"><span data-stu-id="53858-114">Integration between Windows and Linux</span></span>| ✅|✅
 <span data-ttu-id="53858-115">高速の起動時間</span><span class="sxs-lookup"><span data-stu-id="53858-115">Fast boot times</span></span>| ✅ | ✅
 <span data-ttu-id="53858-116">小さなリソース フット プリント</span><span class="sxs-lookup"><span data-stu-id="53858-116">Small resource foot print</span></span>| ✅ |✅
 <span data-ttu-id="53858-117">現在のバージョンの VMware と VirtualBox での実行</span><span class="sxs-lookup"><span data-stu-id="53858-117">Runs with current versions of VMWare and VirtualBox</span></span>| ✅ | ✅
 <span data-ttu-id="53858-118">マネージド VM</span><span class="sxs-lookup"><span data-stu-id="53858-118">Managed VM</span></span>| ❌ | ✅
 <span data-ttu-id="53858-119">完全な Linux カーネル</span><span class="sxs-lookup"><span data-stu-id="53858-119">Full Linux Kernel</span></span>| ❌ |✅
 <span data-ttu-id="53858-120">システム コールの完全な互換性</span><span class="sxs-lookup"><span data-stu-id="53858-120">Full system call compatibility</span></span>| ❌ | ✅
 <span data-ttu-id="53858-121">OS ファイル システム間でのパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="53858-121">Performance across OS file systems</span></span>| ✅ | ❌

<span data-ttu-id="53858-122">WSL 1 を既に使用していて、WSL 2 にアップグレードする場合は、</span><span class="sxs-lookup"><span data-stu-id="53858-122">Already using WSL 1 and want to upgrade to WSL 2?</span></span> <span data-ttu-id="53858-123">手順に従って [WSL 2 に更新](./install-win10.md#update-to-wsl-2)してください。</span><span class="sxs-lookup"><span data-stu-id="53858-123">Follow the instructions to [update to WSL 2](./install-win10.md#update-to-wsl-2)!</span></span>

<span data-ttu-id="53858-124">WSL 2 は、Windows 10、バージョン 2004、ビルド 19041 以上でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="53858-124">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="53858-125">Windows のバージョンを確認するには **Windows ロゴ キー + R** キーを押します。次に「**winver**」と入力し、 **[OK]** を選択します</span><span class="sxs-lookup"><span data-stu-id="53858-125">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="53858-126">(または、Windows コマンド プロンプトで `ver` コマンドを入力します)。</span><span class="sxs-lookup"><span data-stu-id="53858-126">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="53858-127">[最新の Windows バージョンに更新する](ms-settings:windowsupdate)必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="53858-127">You may need to [update to the latest Windows version](ms-settings:windowsupdate).</span></span> <span data-ttu-id="53858-128">19041 より前のビルドでは、WSL はまったくサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="53858-128">For builds lower than 19041, WSL is not supported at all.</span></span>

> [!NOTE]
> <span data-ttu-id="53858-129">WSL 2 は [VMWare 15.5.5+](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) と [VirtualBox 6+](https://www.virtualbox.org/wiki/Changelog-6.0) で動作します。</span><span class="sxs-lookup"><span data-stu-id="53858-129">WSL 2 will work with [VMWare 15.5.5+](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) and [VirtualBox 6+](https://www.virtualbox.org/wiki/Changelog-6.0).</span></span>

## <a name="use-the-linux-file-system-for-faster-performance"></a><span data-ttu-id="53858-130">Linux ファイル システムを使用してパフォーマンスを向上させる</span><span class="sxs-lookup"><span data-stu-id="53858-130">Use the Linux file system for faster performance</span></span>

<span data-ttu-id="53858-131">最速のパフォーマンス速度を実現するために最適化するには、プロジェクト ファイルを (Windows ファイル システムではなく) Linux ファイル システムに格納してください。</span><span class="sxs-lookup"><span data-stu-id="53858-131">In order to optimize for the fastest performance speed, be sure to store your project files in the Linux file system (not the Windows file system).</span></span>

<span data-ttu-id="53858-132">たとえば、WSL プロジェクト ファイルを格納する場合は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="53858-132">For example, when storing your WSL project files:</span></span>

* <span data-ttu-id="53858-133">Linux ファイル システムのルート ディレクトリを使用します: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="53858-133">Use the Linux file system root directory: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span></span>
* <span data-ttu-id="53858-134">Windows ファイル システムのルート ディレクトリではありません: `C:\Users\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="53858-134">Not the Windows file system root directory: `C:\Users\<user name>\Project`</span></span>

<span data-ttu-id="53858-135">WSL ディストリビューション (Ubuntu など) を使用して作業しているプロジェクト ファイルは、より高速なファイル システム アクセスを利用するために、Linux ルート ファイル システムに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53858-135">Project files that you are working with using a WSL distribution (like Ubuntu) must be in the Linux root file system to take advantage of faster file system access.</span></span>

<span data-ttu-id="53858-136">Linux ルート ファイル システムには、エクスプローラーなどの Windows アプリやツールを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="53858-136">You can access your Linux root file system with Windows apps and tools like File Explorer.</span></span> <span data-ttu-id="53858-137">Linux ディストリビューション (Ubuntu など) を開いてみてください。また、次のコマンドを入力して、Linux ホーム ディレクトリにいることを確認してください: `cd ~`。</span><span class="sxs-lookup"><span data-stu-id="53858-137">Try opening a Linux distribution (like Ubuntu), be sure that you are in the Linux home directory by entering this command: `cd ~`.</span></span> <span data-ttu-id="53858-138">次に、以下を入力して、エクスプローラーで Linux ファイル システムを開きます " *(末尾のピリオドを忘れないでください)* ": `explorer.exe .`</span><span class="sxs-lookup"><span data-stu-id="53858-138">Then open your Linux file system in File Explorer by entering *(don't forget the period at the end)*: `explorer.exe .`</span></span>

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a><span data-ttu-id="53858-139">例外的に WSL 2 ではなく WSL 1 を使用する場合</span><span class="sxs-lookup"><span data-stu-id="53858-139">Exceptions for using WSL 1 rather than WSL 2</span></span>

<span data-ttu-id="53858-140">WSL2 ではより高速なパフォーマンスと 100% のシステム コールの互換性が提供されるため、WSL 2 を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="53858-140">We recommend that you use WSL 2 as it offers faster performance and 100% system call compatibility.</span></span> <span data-ttu-id="53858-141">ただし、WSL 1 を使用する方が好ましいシナリオもいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="53858-141">However, there are a few specific scenarios where you might prefer using WSL 1.</span></span> <span data-ttu-id="53858-142">次の場合は、WSL 1 の使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="53858-142">Consider using WSL 1 if:</span></span>

* <span data-ttu-id="53858-143">プロジェクト ファイルを Windows ファイル システムに格納する必要がある。</span><span class="sxs-lookup"><span data-stu-id="53858-143">Your project files must be stored in the Windows file system.</span></span>
  * <span data-ttu-id="53858-144">WSL Linux ディストリビューションを使用して Windows ファイル システム上のプロジェクト ファイルにアクセスする予定で、これらのファイルを Linux ファイル システムに格納できない場合は、WSL 1 を使用することにより、OS ファイル システム間でより高速なパフォーマンスを実現できます。</span><span class="sxs-lookup"><span data-stu-id="53858-144">If you will be using your WSL Linux distribution to access project files on the Windows file system, and these files cannot be stored on the Linux file system, you will achieve faster performance across the OS files systems by using WSL 1.</span></span>
* <span data-ttu-id="53858-145">同じファイルに対して Windows と Linux の両方のツールを使用したクロスコンパイルを必要とするプロジェクト。</span><span class="sxs-lookup"><span data-stu-id="53858-145">A project which requires cross-compilation using both Windows and Linux tools on the same files.</span></span>
  * <span data-ttu-id="53858-146">Windows オペレーティング システムと Linux オペレーティング システムの間のファイル パフォーマンスは WSL 1 の方が WSL 2 よりも高速です。そのため、Windows アプリケーションを使用して Linux ファイルにアクセスする場合、現時点では WSL 1 を使用する方がより高速なパフォーマンスを得られます。</span><span class="sxs-lookup"><span data-stu-id="53858-146">File performance across the Windows and Linux operating systems is faster in WSL 1 than WSL 2, so if you are using Windows applications to access Linux files, you will currently achieve faster performance with WSL 1.</span></span>

> [!NOTE]
> <span data-ttu-id="53858-147">VS Code [Remote WSL 拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)を試すことを検討してください。Linux コマンド ライン ツールを使用してプロジェクト ファイルを Linux ファイル システム上に格納できるだけでなく、Windows 上で VS Code を使用して、インターネット ブラウザーでプロジェクトを作成、編集、デバッグ、実行できるようになります。Linux ファイル システムと Windows ファイル システムをまたぐ処理に伴うパフォーマンスの低下は発生しません。</span><span class="sxs-lookup"><span data-stu-id="53858-147">Consider trying the VS Code [Remote WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) to enable you to store your project files on the Linux file system, using Linux command line tools, but also using VS Code on Windows to author, edit, debug, or run your project in an internet browser without any of the performance slow-downs associated with working across the Linux and Windows file systems.</span></span> <span data-ttu-id="53858-148">[詳しくはこちらをご覧ください](https://code.visualstudio.com/docs/remote/wsl)。</span><span class="sxs-lookup"><span data-stu-id="53858-148">[Learn more](https://code.visualstudio.com/docs/remote/wsl).</span></span>

## <a name="wsl-2-architecture"></a><span data-ttu-id="53858-149">WSL 2 のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="53858-149">WSL 2 architecture</span></span>

<span data-ttu-id="53858-150">従来の VM エクスペリエンスは起動に時間がかかり、分離され、大量のリソースが消費され、管理に時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="53858-150">A traditional VM experience can be slow to boot up, is isolated, consumes lots of resources, and requires your time to manage it.</span></span> <span data-ttu-id="53858-151">WSL 2 にこのような特徴はありません。</span><span class="sxs-lookup"><span data-stu-id="53858-151">WSL 2 does not have these attributes.</span></span>

<span data-ttu-id="53858-152">WSL 2 には、Windows と Linux の間のシームレスな統合、高速な起動時間、小さなリソース フットプリントをはじめとする WSL 1 の利点があるうえ、VM の構成や管理が必要ありません。</span><span class="sxs-lookup"><span data-stu-id="53858-152">WSL 2 provides the benefits of WSL 1, including seamless integration between Windows and Linux, fast boot times, a small resource footprint, and requires no VM configuration or management.</span></span> <span data-ttu-id="53858-153">WSL 2 には VM が使用されますが、バックグラウンドで管理および実行されるため、WSL 1 とユーザー エクスペリエンスは同じです。</span><span class="sxs-lookup"><span data-stu-id="53858-153">While WSL 2 does use a VM, it is managed and run behind the scenes, leaving you with the same user experience as WSL 1.</span></span>

### <a name="full-linux-kernel"></a><span data-ttu-id="53858-154">完全な Linux カーネル</span><span class="sxs-lookup"><span data-stu-id="53858-154">Full Linux kernel</span></span>

<span data-ttu-id="53858-155">WSL 2 の Linux カーネルは、kernel.org で入手できるソースに基づいて、最新の安定したブランチから Microsoft によって構築されています。このカーネルは WSL 2 向けに特別にチューニングされており、サイズとパフォーマンスの最適化によって Windows 上で優れた Linux エクスペリエンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="53858-155">The Linux kernel in WSL 2 is built by Microsoft from the latest stable branch, based on the source available at kernel.org. This kernel has been specially tuned for WSL 2, optimizing for size and performance to provide an amazing Linux experience on Windows.</span></span> <span data-ttu-id="53858-156">カーネルは、Windows の更新プログラムによって保守されます。つまり、自分で管理しなくても、最新のセキュリティ修正プログラムとカーネルの機能強化を利用できます。</span><span class="sxs-lookup"><span data-stu-id="53858-156">The kernel will be serviced by Windows updates, which means you will get the latest security fixes and kernel improvements without needing to manage it yourself.</span></span>

<span data-ttu-id="53858-157">[WSL 2 Linux カーネルはオープン ソースです](https://github.com/microsoft/WSL2-Linux-Kernel)。</span><span class="sxs-lookup"><span data-stu-id="53858-157">The [WSL 2 Linux kernel is open source](https://github.com/microsoft/WSL2-Linux-Kernel).</span></span> <span data-ttu-id="53858-158">詳細については、カーネルを構築したチームによって書かれたブログ投稿「[Windows に Linux カーネルを同梱する](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53858-158">If you'd like to learn more, check out the blog post [Shipping a Linux Kernel with Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) written by the team that built it.</span></span>

### <a name="increased-file-io-performance"></a><span data-ttu-id="53858-159">ファイル IO パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="53858-159">Increased file IO performance</span></span>

<span data-ttu-id="53858-160">WSL 2 を使用すると、git clone、npm install、apt update、apt upgrade などのあらゆるファイル集約型の操作が大きく高速化されます。</span><span class="sxs-lookup"><span data-stu-id="53858-160">File intensive operations like git clone, npm install, apt update, apt upgrade, and more are all noticeably faster with WSL 2.</span></span>

<span data-ttu-id="53858-161">実際どのくらい高速になるかは、実行しているアプリと、ファイル システムとのやり取りの方法によって変わります。</span><span class="sxs-lookup"><span data-stu-id="53858-161">The actual speed increase will depend on which app you're running and how it is interacting with the file system.</span></span> <span data-ttu-id="53858-162">初期バージョンの WSL 2 は、zip 圧縮された tarball を展開する場合、WSL 1 と比べて最大 20 倍速くなります。また、さまざまなプロジェクトで git clone、npm install、および cmake を使用する場合は、約 2 倍から 5 倍速くなります。</span><span class="sxs-lookup"><span data-stu-id="53858-162">Initial versions of WSL 2 run up to 20x faster compared to WSL 1 when unpacking a zipped tarball, and around 2-5x faster when using git clone, npm install and cmake on various projects.</span></span>

### <a name="full-system-call-compatibility"></a><span data-ttu-id="53858-163">システム コールの完全な互換性</span><span class="sxs-lookup"><span data-stu-id="53858-163">Full system call compatibility</span></span>

<span data-ttu-id="53858-164">Linux バイナリでは、システム コールを使用して、ファイルへのアクセス、メモリの要求、プロセスの作成などの機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="53858-164">Linux binaries use system calls to perform functions such as accessing files, requesting memory, creating processes, and more.</span></span> <span data-ttu-id="53858-165">WSL 1 では WSL チームが構築した変換レイヤーが使用されていましたが、WSL 2 にはシステム コールの完全な互換性を持つ独自の Linux カーネルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="53858-165">Whereas WSL 1 used a translation layer that was built by the WSL team, WSL 2 includes its own Linux kernel with full system call compatibility.</span></span> <span data-ttu-id="53858-166">次のような利点があります。</span><span class="sxs-lookup"><span data-stu-id="53858-166">Benefits include:</span></span>

* <span data-ttu-id="53858-167">**[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** など、WSL 内で実行できるまったく新しいアプリのセット。</span><span class="sxs-lookup"><span data-stu-id="53858-167">A whole new set of apps that you can run inside of WSL, such as **[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** and more.</span></span>

* <span data-ttu-id="53858-168">Linux カーネルに対する更新プログラムがすぐに使用可能になります</span><span class="sxs-lookup"><span data-stu-id="53858-168">Any updates to the Linux kernel are immediately ready for use.</span></span> <span data-ttu-id="53858-169">(WSL チームが更新プログラムを実装して変更を追加するまで待つ必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="53858-169">(You don't have to wait for the WSL team to implement updates and add the changes).</span></span>

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a><span data-ttu-id="53858-170">WSL 2 は起動時のメモリ使用量が少ない</span><span class="sxs-lookup"><span data-stu-id="53858-170">WSL 2 uses a smaller amount of memory on startup</span></span>

<span data-ttu-id="53858-171">WSL 2 では、メモリ フットプリントが小さな実際の Linux カーネル上で軽量のユーティリティ VM を使用します。</span><span class="sxs-lookup"><span data-stu-id="53858-171">WSL 2 uses a lightweight utility VM on a real Linux kernel with a small memory footprint.</span></span> <span data-ttu-id="53858-172">このユーティリティは、仮想アドレスが使用されるメモリを起動時に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="53858-172">The utility will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="53858-173">これは、WSL 1 で必要とされていたよりも少ない割合の合計メモリで起動するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="53858-173">It is configured to start with a smaller proportion of your total memory that what was required for WSL 1.</span></span>

## <a name="accessing-network-applications"></a><span data-ttu-id="53858-174">ネットワーク アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="53858-174">Accessing network applications</span></span>

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a><span data-ttu-id="53858-175">Windows からの Linux ネットワーク アプリへのアクセス (localhost)</span><span class="sxs-lookup"><span data-stu-id="53858-175">Accessing Linux networking apps from Windows (localhost)</span></span>

<span data-ttu-id="53858-176">Linux ディストリビューションでネットワーク アプリ (たとえば、Node.js または SQL Server で実行されるアプリ) を構築する場合、(通常の場合と同様に) `localhost` を使用して (Microsoft Edge または Chrome インターネット ブラウザーなどの) Windows アプリからアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="53858-176">If you are building a networking app (for example an app running on a NodeJS or SQL server) in your Linux distribution, you can access it from a Windows app (like your Edge or Chrome internet browser) using `localhost` (just like you normally would).</span></span>

<span data-ttu-id="53858-177">ただし、Windows の古いバージョン (ビルド 18945 以下) を実行している場合は、Linux ホスト VM の IP アドレスを取得する (または[最新の Windows バージョンに更新する](ms-settings:windowsupdate)) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="53858-177">However, if you are running an older version of Windows (Build 18945 or less), you will need to get the IP address of the Linux host VM (or [update to the latest Windows version](ms-settings:windowsupdate)).</span></span>

<span data-ttu-id="53858-178">Linux ディストリビューションが動作する仮想マシンの IP アドレスを確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="53858-178">To find the IP address of the virtual machine powering your Linux distribution:</span></span>

* <span data-ttu-id="53858-179">WSL ディストリビューション (つまり、Ubuntu) から、次のコマンドを実行します: `ip addr`</span><span class="sxs-lookup"><span data-stu-id="53858-179">From your WSL distribution (ie Ubuntu), run the command: `ip addr`</span></span>
* <span data-ttu-id="53858-180">`eth0` インターフェイスの `inet` 値の下で目的のアドレスを見つけてコピーします。</span><span class="sxs-lookup"><span data-stu-id="53858-180">Find and copy the address under the `inet` value of the `eth0` interface.</span></span>
* <span data-ttu-id="53858-181">grep ツールがインストールされている場合は、次のコマンドを使用して出力をフィルター処理することにより、これをより簡単に見つけることができます: `ip addr | grep eth0`</span><span class="sxs-lookup"><span data-stu-id="53858-181">If you have the grep tool installed, find this more easily by filtering the output with the command: `ip addr | grep eth0`</span></span>
* <span data-ttu-id="53858-182">この IP アドレスを使用して Linux サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="53858-182">Connect to your Linux server using this IP address.</span></span>

<span data-ttu-id="53858-183">次の図は、これを実行するために、Edge ブラウザーを使用して Node.js サーバーに接続する例です。</span><span class="sxs-lookup"><span data-stu-id="53858-183">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a><span data-ttu-id="53858-185">Linux からの Windows ネットワーク アプリへのアクセス (ホスト IP)</span><span class="sxs-lookup"><span data-stu-id="53858-185">Accessing Windows networking apps from Linux (host IP)</span></span>

<span data-ttu-id="53858-186">Linux ディストリビューション (つまり、Ubuntu) から Windows 上で実行されているネットワーク アプリ (たとえば、Node.js または SQL Server で実行されるアプリ) にアクセスする場合は、ホスト マシンの IP アドレスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53858-186">If you want to access a networking app running on Windows (for example an app running on a NodeJS or SQL server) from your Linux distribution (ie Ubuntu), then you need to use the IP address of your host machine.</span></span> <span data-ttu-id="53858-187">これは一般的なシナリオではありませんが、次の手順に従ってこれを実現できます。</span><span class="sxs-lookup"><span data-stu-id="53858-187">While this is not a common scenario, you can follow these steps to make it work.</span></span>
    - <span data-ttu-id="53858-188">Linux ディストリビューションから次のコマンドを実行して、ホスト マシンの IP アドレスを取得します: `cat /etc/resolv.conf`</span><span class="sxs-lookup"><span data-stu-id="53858-188">Obtain the IP address of your host machine by running this command from your Linux distribution: `cat /etc/resolv.conf`</span></span>
    - <span data-ttu-id="53858-189">次の語句の後に IP アドレスをコピーします: `nameserver`。</span><span class="sxs-lookup"><span data-stu-id="53858-189">Copy the IP address following the term: `nameserver`.</span></span>
    - <span data-ttu-id="53858-190">コピーした IP アドレスを使用して、Windows サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="53858-190">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="53858-191">次の図は、これを実行するために、curl を介して Windows で実行されている Node.js サーバーに接続する例です。</span><span class="sxs-lookup"><span data-stu-id="53858-191">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span>

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a><span data-ttu-id="53858-193">ネットワークに関する追加の考慮事項</span><span class="sxs-lookup"><span data-stu-id="53858-193">Additional networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="53858-194">リモート IP アドレスを使用した接続</span><span class="sxs-lookup"><span data-stu-id="53858-194">Connecting via remote IP addresses</span></span>

<span data-ttu-id="53858-195">リモート IP アドレスを使用してアプリケーションに接続すると、ローカル エリア ネットワーク (LAN) からの接続として扱われます。</span><span class="sxs-lookup"><span data-stu-id="53858-195">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="53858-196">これは、アプリケーションで LAN 接続を受け入れることができるようにする必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="53858-196">This means that you will need to make sure your application can accept LAN connections.</span></span>

<span data-ttu-id="53858-197">たとえば、場合によっては、`127.0.0.1` ではなく `0.0.0.0` にアプリケーションをバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53858-197">For example, you may need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="53858-198">Flask を使用する Python アプリの例では、次のコマンドを使用してこれを実行できます: `app.run(host='0.0.0.0')`。</span><span class="sxs-lookup"><span data-stu-id="53858-198">In the example of a Python app using Flask, this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="53858-199">これらの変更を行うと、LAN からの接続が許可されるため、セキュリティに注意してください。</span><span class="sxs-lookup"><span data-stu-id="53858-199">Please keep security in mind when making these changes as this will allow connections from your LAN.</span></span>

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a><span data-ttu-id="53858-200">ローカル エリア ネットワーク (LAN) からの WSL 2 ディストリビューションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="53858-200">Accessing a WSL 2 distribution from your local area network (LAN)</span></span>

<span data-ttu-id="53858-201">WSL 1 ディストリビューションを使用している場合、LAN からアクセスできるようにコンピューターが設定されていれば、WSL で実行されているアプリケーションに LAN からもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="53858-201">When using a WSL 1 distribution, if your computer was set up to be accessed by your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span>

<span data-ttu-id="53858-202">WSL 2 では、これは既定の動作ではありません。</span><span class="sxs-lookup"><span data-stu-id="53858-202">This isn't the default case in WSL 2.</span></span> <span data-ttu-id="53858-203">WSL 2 には、独自の一意の IP アドレスを持つ仮想化されたイーサネット アダプターがあります。</span><span class="sxs-lookup"><span data-stu-id="53858-203">WSL 2 has a virtualized ethernet adapter with its own unique IP address.</span></span> <span data-ttu-id="53858-204">現在、このワークフローを有効にするには、通常の仮想マシンの場合と同じ手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53858-204">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="53858-205">(Microsoft は、このエクスペリエンスを改善する方法を検討しています)。</span><span class="sxs-lookup"><span data-stu-id="53858-205">(We are looking into ways to improve this experience.)</span></span>

<span data-ttu-id="53858-206">次に、ホスト上のポート 4000 でリッスンし、それを IP アドレス 192.168.101.100 の WSL 2 VM のポート 4000 に接続するポート プロキシを追加する PowerShell コマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="53858-206">Here's an example PowerShell command to add a port proxy that listens on port 4000 on the host and connects it to port 4000 to the WSL 2 VM with IP address 192.168.101.100.</span></span>
```powershell
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.101.100
```

#### <a name="ipv6-access"></a><span data-ttu-id="53858-207">IPv6 アクセス</span><span class="sxs-lookup"><span data-stu-id="53858-207">IPv6 access</span></span>

<span data-ttu-id="53858-208">WSL 2 ディストリビューションは、現在、IPv6 のみのアドレスに到達できません。</span><span class="sxs-lookup"><span data-stu-id="53858-208">WSL 2 distributions currently cannot reach IPv6-only addresses.</span></span> <span data-ttu-id="53858-209">Microsoft は、この機能の追加に取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="53858-209">We are working on adding this feature.</span></span>

## <a name="expanding-the-size-of-your-wsl-2-virtual-hardware-disk"></a><span data-ttu-id="53858-210">WSL 2 仮想ハードウェア ディスクのサイズの拡張</span><span class="sxs-lookup"><span data-stu-id="53858-210">Expanding the size of your WSL 2 Virtual Hardware Disk</span></span>

<span data-ttu-id="53858-211">WSL 2 では、仮想ハードウェア ディスク (VHD) を使用して Linux ファイルを格納します。</span><span class="sxs-lookup"><span data-stu-id="53858-211">WSL 2 uses a Virtual Hardware Disk (VHD) to store your Linux files.</span></span> <span data-ttu-id="53858-212">場合によっては、その最大サイズに達したときにサイズを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53858-212">If you reach its max size you may need to expand it.</span></span>

<span data-ttu-id="53858-213">WSL 2 VHD では、ext4 ファイル システムが使用されます。</span><span class="sxs-lookup"><span data-stu-id="53858-213">The WSL 2 VHD uses the ext4 file system.</span></span> <span data-ttu-id="53858-214">この VHD は、ストレージのニーズに合わせて自動的にサイズが変更されます。初期の最大サイズは 256 GB です。</span><span class="sxs-lookup"><span data-stu-id="53858-214">This VHD automatically resizes to meet your storage needs and has an initial maximum size of 256GB.</span></span> <span data-ttu-id="53858-215">ディストリビューションが 256 GB を超えるサイズになると、ディスク領域が不足していることを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="53858-215">If your distribution grows in size to be greater than 256GB, you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="53858-216">このエラーは、VHD サイズを拡張することで修正できます。</span><span class="sxs-lookup"><span data-stu-id="53858-216">You can fix this error by expanding the VHD size.</span></span>

<span data-ttu-id="53858-217">256 GB を超えて VHD の最大サイズを拡張するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="53858-217">To expand your maximum VHD size beyond 256GB:</span></span>

1. <span data-ttu-id="53858-218">次のコマンドを使用して、すべての WSL インスタンスを終了します: `wsl --shutdown`</span><span class="sxs-lookup"><span data-stu-id="53858-218">Terminate all WSL instances using the command: `wsl --shutdown`</span></span>

2. <span data-ttu-id="53858-219">ディストリビューションのインストール パッケージ名 ("PackageFamilyName") を見つけます</span><span class="sxs-lookup"><span data-stu-id="53858-219">Find your distribution installation package name ('PackageFamilyName')</span></span>
    * <span data-ttu-id="53858-220">PowerShell を使用して、次のコマンドを入力します ("distro" はディストリビューション名です):</span><span class="sxs-lookup"><span data-stu-id="53858-220">Using PowerShell (where 'distro' is your distribution name) enter the command:</span></span>
    * `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. <span data-ttu-id="53858-221">WSL 2 のインストールで使用される VHD ファイルの `fullpath` を特定します。これが `pathToVHD` になります。</span><span class="sxs-lookup"><span data-stu-id="53858-221">Locate the VHD file `fullpath` used by your WSL 2 installation, this will be your `pathToVHD`:</span></span>
     * `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. <span data-ttu-id="53858-222">次のコマンドを実行して、WSL 2 VHD のサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="53858-222">Resize your WSL 2 VHD by completing the following commands:</span></span>
   * <span data-ttu-id="53858-223">管理者特権で Windows コマンド プロンプトを開き、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="53858-223">Open Windows Command Prompt with admin privileges and enter:</span></span>
      * `diskpart`
      * `Select vdisk file="<pathToVHD>"`
      * `expand vdisk maximum="<sizeInMegaBytes>"`

5. <span data-ttu-id="53858-224">WSL ディストリビューション (たとえば、Ubuntu) を起動します。</span><span class="sxs-lookup"><span data-stu-id="53858-224">Launch your WSL distribution (Ubuntu, for example).</span></span>

6. <span data-ttu-id="53858-225">Linux ディストリビューションのコマンド ラインから次のコマンドを実行して、ファイル システムのサイズを拡張できることを WSL に認識させます。</span><span class="sxs-lookup"><span data-stu-id="53858-225">Make WSL aware that it can expand its file system's size by running these commands from your Linux distribution command line:</span></span>
    * `sudo mount -t devtmpfs none /dev`
    * `mount | grep ext4`
    * <span data-ttu-id="53858-226">`/dev/sdXX` のようなこのエントリの名前をコピーします (X は他の文字を表します)</span><span class="sxs-lookup"><span data-stu-id="53858-226">Copy the name of this entry, which will look like: `/dev/sdXX` (with the X representing any other character)</span></span>
    * `sudo resize2fs /dev/sdXX`
    * <span data-ttu-id="53858-227">前の手順でコピーした値を使用します。</span><span class="sxs-lookup"><span data-stu-id="53858-227">Use the value you copied earlier.</span></span> <span data-ttu-id="53858-228">resize2fs のインストールが必要になる場合もあります: `apt install resize2fs`</span><span class="sxs-lookup"><span data-stu-id="53858-228">You may also need to install resize2fs: `apt install resize2fs`</span></span>

> [!NOTE]
> <span data-ttu-id="53858-229">通常、Windows ツールまたはエディターを使用して、AppData フォルダー内にある WSL 関連ファイルを変更、移動、またはアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="53858-229">In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="53858-230">そうすると、Linux ディストリビューションが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="53858-230">Doing so could cause your Linux distribution to become corrupted.</span></span>
