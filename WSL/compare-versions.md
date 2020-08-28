---
title: WSL 2 と WSL 1 の比較
description: Linux 用 Windows サブシステムのバージョン 1 とバージョン 2 を比較します。 WSL 2 は、実際の Linux カーネルを実行し、速度とシステム コールの完全な互換性を高めます。 WSL 1 は、Windows と Linux の両方のファイル システムで作業している場合に適しています。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux, ubuntu, debian, suse, windows 10, UX の変更, WSL 2, linux カーネル, ネットワーク アプリケーション, localhost, IPv6, 仮想ハードウェア ディスク, VHD, VHD の制限, VHD エラー
ms.date: 07/22/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 15f1528332345f0bea829b9606372ed7346e6dff
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866026"
---
# <a name="comparing-wsl-1-and-wsl-2"></a><span data-ttu-id="e5ca8-106">WSL 1 と WSL 2 の比較</span><span class="sxs-lookup"><span data-stu-id="e5ca8-106">Comparing WSL 1 and WSL 2</span></span>

<span data-ttu-id="e5ca8-107">Linux 用 Windows サブシステムを新しいバージョンに更新する主な目的は、**ファイル システムのパフォーマンスを向上させ**、**システム コールの完全な互換性**をサポートすることです。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-107">The primary goals of updating the Windows Subsystem for Linux to a new version are to **increase file system performance** and support **full system call compatibility**.</span></span> 

<span data-ttu-id="e5ca8-108">軽量のユーティリティ仮想マシン (VM) 内で Linux カーネルを実行するために、WSL 2 には最新の優れた仮想化テクノロジが使用されています。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-108">WSL 2 uses the latest and greatest in virtualization technology to run a Linux kernel inside of a lightweight utility virtual machine (VM).</span></span> <span data-ttu-id="e5ca8-109">ただし、WSL 2 は従来の VM エクスペリエンスではありません。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-109">However, WSL 2 is not a traditional VM experience.</span></span> <span data-ttu-id="e5ca8-110">[WSL 2 アーキテクチャの詳細については、こちらをご覧ください](#wsl-2-architecture)。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-110">[Learn more about the WSL 2 architecture](#wsl-2-architecture).</span></span>

## <a name="comparing-features"></a><span data-ttu-id="e5ca8-111">機能の比較</span><span class="sxs-lookup"><span data-stu-id="e5ca8-111">Comparing features</span></span>

<span data-ttu-id="e5ca8-112">機能</span><span class="sxs-lookup"><span data-stu-id="e5ca8-112">Feature</span></span> | <span data-ttu-id="e5ca8-113">WSL 1</span><span class="sxs-lookup"><span data-stu-id="e5ca8-113">WSL 1</span></span> | <span data-ttu-id="e5ca8-114">WSL 2</span><span class="sxs-lookup"><span data-stu-id="e5ca8-114">WSL 2</span></span>
--- | --- | ---
 <span data-ttu-id="e5ca8-115">Windows と Linux の統合</span><span class="sxs-lookup"><span data-stu-id="e5ca8-115">Integration between Windows and Linux</span></span>| ✅|✅
 <span data-ttu-id="e5ca8-116">高速の起動時間</span><span class="sxs-lookup"><span data-stu-id="e5ca8-116">Fast boot times</span></span>| ✅ | ✅
 <span data-ttu-id="e5ca8-117">小さなリソース フット プリント</span><span class="sxs-lookup"><span data-stu-id="e5ca8-117">Small resource foot print</span></span>| ✅ |✅
 <span data-ttu-id="e5ca8-118">現在のバージョンの VMware と VirtualBox での実行</span><span class="sxs-lookup"><span data-stu-id="e5ca8-118">Runs with current versions of VMWare and VirtualBox</span></span>| ✅ | ✅
 <span data-ttu-id="e5ca8-119">マネージド VM</span><span class="sxs-lookup"><span data-stu-id="e5ca8-119">Managed VM</span></span>| ❌ | ✅
 <span data-ttu-id="e5ca8-120">完全な Linux カーネル</span><span class="sxs-lookup"><span data-stu-id="e5ca8-120">Full Linux Kernel</span></span>| ❌ |✅
 <span data-ttu-id="e5ca8-121">システム コールの完全な互換性</span><span class="sxs-lookup"><span data-stu-id="e5ca8-121">Full system call compatibility</span></span>| ❌ | ✅
 <span data-ttu-id="e5ca8-122">OS ファイル システム間でのパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="e5ca8-122">Performance across OS file systems</span></span>| ✅ | ❌

<span data-ttu-id="e5ca8-123">WSL 1 を既に使用していて、WSL 2 にアップグレードする場合は、</span><span class="sxs-lookup"><span data-stu-id="e5ca8-123">Already using WSL 1 and want to upgrade to WSL 2?</span></span> <span data-ttu-id="e5ca8-124">手順に従って [WSL 2 に更新](./install-win10.md#update-to-wsl-2)してください。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-124">Follow the instructions to [update to WSL 2](./install-win10.md#update-to-wsl-2)!</span></span>

<span data-ttu-id="e5ca8-125">WSL 2 は、Windows 10、バージョン 2004、ビルド 19041 以上でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-125">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="e5ca8-126">Windows のバージョンを確認するには **Windows ロゴ キー + R** キーを押します。次に「**winver**」と入力し、 **[OK]** を選択します</span><span class="sxs-lookup"><span data-stu-id="e5ca8-126">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="e5ca8-127">(または、Windows コマンド プロンプトで `ver` コマンドを入力します)。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-127">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="e5ca8-128">[最新の Windows バージョンに更新する](ms-settings:windowsupdate)必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-128">You may need to [update to the latest Windows version](ms-settings:windowsupdate).</span></span> <span data-ttu-id="e5ca8-129">19041 より前のビルドでは、WSL はまったくサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-129">For builds lower than 19041, WSL is not supported at all.</span></span>

> [!NOTE]
> <span data-ttu-id="e5ca8-130">WSL 2 は [VMWare 15.5.5+](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) と [VirtualBox 6+](https://www.virtualbox.org/wiki/Changelog-6.0) で動作します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-130">WSL 2 will work with [VMWare 15.5.5+](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) and [VirtualBox 6+](https://www.virtualbox.org/wiki/Changelog-6.0).</span></span>

## <a name="use-the-linux-file-system-for-faster-performance"></a><span data-ttu-id="e5ca8-131">Linux ファイル システムを使用してパフォーマンスを向上させる</span><span class="sxs-lookup"><span data-stu-id="e5ca8-131">Use the Linux file system for faster performance</span></span>

<span data-ttu-id="e5ca8-132">最速のパフォーマンス速度を実現するために最適化するには、プロジェクト ファイルを (Windows ファイル システムではなく) Linux ファイル システムに格納してください。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-132">In order to optimize for the fastest performance speed, be sure to store your project files in the Linux file system (not the Windows file system).</span></span>

<span data-ttu-id="e5ca8-133">たとえば、WSL プロジェクト ファイルを格納する場合は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-133">For example, when storing your WSL project files:</span></span>

* <span data-ttu-id="e5ca8-134">Linux ファイル システムのルート ディレクトリを使用します: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-134">Use the Linux file system root directory: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span></span>
* <span data-ttu-id="e5ca8-135">Windows ファイル システムのルート ディレクトリではありません: `C:\Users\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-135">Not the Windows file system root directory: `C:\Users\<user name>\Project`</span></span>

<span data-ttu-id="e5ca8-136">WSL ディストリビューション (Ubuntu など) を使用して作業しているプロジェクト ファイルは、より高速なファイル システム アクセスを利用するために、Linux ルート ファイル システムに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-136">Project files that you are working with using a WSL distribution (like Ubuntu) must be in the Linux root file system to take advantage of faster file system access.</span></span>

<span data-ttu-id="e5ca8-137">Linux ルート ファイル システムには、エクスプローラーなどの Windows アプリやツールを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-137">You can access your Linux root file system with Windows apps and tools like File Explorer.</span></span> <span data-ttu-id="e5ca8-138">Linux ディストリビューション (Ubuntu など) を開いてみてください。また、次のコマンドを入力して、Linux ホーム ディレクトリにいることを確認してください: `cd ~`。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-138">Try opening a Linux distribution (like Ubuntu), be sure that you are in the Linux home directory by entering this command: `cd ~`.</span></span> <span data-ttu-id="e5ca8-139">次に、以下を入力して、エクスプローラーで Linux ファイル システムを開きます " *(末尾のピリオドを忘れないでください)* ": `explorer.exe .`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-139">Then open your Linux file system in File Explorer by entering *(don't forget the period at the end)*: `explorer.exe .`</span></span>

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a><span data-ttu-id="e5ca8-140">例外的に WSL 2 ではなく WSL 1 を使用する場合</span><span class="sxs-lookup"><span data-stu-id="e5ca8-140">Exceptions for using WSL 1 rather than WSL 2</span></span>

<span data-ttu-id="e5ca8-141">WSL2 ではより高速なパフォーマンスと 100% のシステム コールの互換性が提供されるため、WSL 2 を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-141">We recommend that you use WSL 2 as it offers faster performance and 100% system call compatibility.</span></span> <span data-ttu-id="e5ca8-142">ただし、WSL 1 を使用する方が好ましいシナリオもいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-142">However, there are a few specific scenarios where you might prefer using WSL 1.</span></span> <span data-ttu-id="e5ca8-143">次の場合は、WSL 1 の使用を検討してください。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-143">Consider using WSL 1 if:</span></span>

* <span data-ttu-id="e5ca8-144">プロジェクト ファイルを Windows ファイル システムに格納する必要がある。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-144">Your project files must be stored in the Windows file system.</span></span>
  * <span data-ttu-id="e5ca8-145">WSL Linux ディストリビューションを使用して Windows ファイル システム上のプロジェクト ファイルにアクセスする予定で、これらのファイルを Linux ファイル システムに格納できない場合は、WSL 1 を使用することにより、OS ファイル システム間でより高速なパフォーマンスを実現できます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-145">If you will be using your WSL Linux distribution to access project files on the Windows file system, and these files cannot be stored on the Linux file system, you will achieve faster performance across the OS files systems by using WSL 1.</span></span>
* <span data-ttu-id="e5ca8-146">同じファイルに対して Windows と Linux の両方のツールを使用したクロスコンパイルを必要とするプロジェクト。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-146">A project which requires cross-compilation using both Windows and Linux tools on the same files.</span></span>
  * <span data-ttu-id="e5ca8-147">Windows オペレーティング システムと Linux オペレーティング システムの間のファイル パフォーマンスは WSL 1 の方が WSL 2 よりも高速です。そのため、Windows アプリケーションを使用して Linux ファイルにアクセスする場合、現時点では WSL 1 を使用する方がより高速なパフォーマンスを得られます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-147">File performance across the Windows and Linux operating systems is faster in WSL 1 than WSL 2, so if you are using Windows applications to access Linux files, you will currently achieve faster performance with WSL 1.</span></span>

> [!NOTE]
> <span data-ttu-id="e5ca8-148">VS Code [Remote WSL 拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)を試すことを検討してください。Linux コマンド ライン ツールを使用してプロジェクト ファイルを Linux ファイル システム上に格納できるだけでなく、Windows 上で VS Code を使用して、インターネット ブラウザーでプロジェクトを作成、編集、デバッグ、実行できるようになります。Linux ファイル システムと Windows ファイル システムをまたぐ処理に伴うパフォーマンスの低下は発生しません。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-148">Consider trying the VS Code [Remote WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) to enable you to store your project files on the Linux file system, using Linux command line tools, but also using VS Code on Windows to author, edit, debug, or run your project in an internet browser without any of the performance slow-downs associated with working across the Linux and Windows file systems.</span></span> <span data-ttu-id="e5ca8-149">[詳しくはこちらをご覧ください](https://code.visualstudio.com/docs/remote/wsl)。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-149">[Learn more](https://code.visualstudio.com/docs/remote/wsl).</span></span>

## <a name="wsl-2-architecture"></a><span data-ttu-id="e5ca8-150">WSL 2 のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="e5ca8-150">WSL 2 architecture</span></span>

<span data-ttu-id="e5ca8-151">従来の VM エクスペリエンスは起動に時間がかかり、分離され、大量のリソースが消費され、管理に時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-151">A traditional VM experience can be slow to boot up, is isolated, consumes lots of resources, and requires your time to manage it.</span></span> <span data-ttu-id="e5ca8-152">WSL 2 にこのような特徴はありません。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-152">WSL 2 does not have these attributes.</span></span>

<span data-ttu-id="e5ca8-153">WSL 2 には、Windows と Linux の間のシームレスな統合、高速な起動時間、小さなリソース フットプリントをはじめとする WSL 1 の利点があるうえ、VM の構成や管理が必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-153">WSL 2 provides the benefits of WSL 1, including seamless integration between Windows and Linux, fast boot times, a small resource footprint, and requires no VM configuration or management.</span></span> <span data-ttu-id="e5ca8-154">WSL 2 には VM が使用されますが、バックグラウンドで管理および実行されるため、WSL 1 とユーザー エクスペリエンスは同じです。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-154">While WSL 2 does use a VM, it is managed and run behind the scenes, leaving you with the same user experience as WSL 1.</span></span>

### <a name="full-linux-kernel"></a><span data-ttu-id="e5ca8-155">完全な Linux カーネル</span><span class="sxs-lookup"><span data-stu-id="e5ca8-155">Full Linux kernel</span></span>

<span data-ttu-id="e5ca8-156">WSL 2 の Linux カーネルは、kernel.org で入手できるソースに基づいて、最新の安定したブランチから Microsoft によって構築されています。このカーネルは WSL 2 向けに特別にチューニングされており、サイズとパフォーマンスの最適化によって Windows 上で優れた Linux エクスペリエンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-156">The Linux kernel in WSL 2 is built by Microsoft from the latest stable branch, based on the source available at kernel.org. This kernel has been specially tuned for WSL 2, optimizing for size and performance to provide an amazing Linux experience on Windows.</span></span> <span data-ttu-id="e5ca8-157">カーネルは、Windows の更新プログラムによって保守されます。つまり、自分で管理しなくても、最新のセキュリティ修正プログラムとカーネルの機能強化を利用できます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-157">The kernel will be serviced by Windows updates, which means you will get the latest security fixes and kernel improvements without needing to manage it yourself.</span></span>

<span data-ttu-id="e5ca8-158">[WSL 2 Linux カーネルはオープン ソースです](https://github.com/microsoft/WSL2-Linux-Kernel)。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-158">The [WSL 2 Linux kernel is open source](https://github.com/microsoft/WSL2-Linux-Kernel).</span></span> <span data-ttu-id="e5ca8-159">詳細については、カーネルを構築したチームによって書かれたブログ投稿「[Windows に Linux カーネルを同梱する](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-159">If you'd like to learn more, check out the blog post [Shipping a Linux Kernel with Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) written by the team that built it.</span></span>

### <a name="increased-file-io-performance"></a><span data-ttu-id="e5ca8-160">ファイル IO パフォーマンスの向上</span><span class="sxs-lookup"><span data-stu-id="e5ca8-160">Increased file IO performance</span></span>

<span data-ttu-id="e5ca8-161">WSL 2 を使用すると、git clone、npm install、apt update、apt upgrade などのあらゆるファイル集約型の操作が大きく高速化されます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-161">File intensive operations like git clone, npm install, apt update, apt upgrade, and more are all noticeably faster with WSL 2.</span></span>

<span data-ttu-id="e5ca8-162">実際どのくらい高速になるかは、実行しているアプリと、ファイル システムとのやり取りの方法によって変わります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-162">The actual speed increase will depend on which app you're running and how it is interacting with the file system.</span></span> <span data-ttu-id="e5ca8-163">初期バージョンの WSL 2 は、zip 圧縮された tarball を展開する場合、WSL 1 と比べて最大 20 倍速くなります。また、さまざまなプロジェクトで git clone、npm install、および cmake を使用する場合は、約 2 倍から 5 倍速くなります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-163">Initial versions of WSL 2 run up to 20x faster compared to WSL 1 when unpacking a zipped tarball, and around 2-5x faster when using git clone, npm install and cmake on various projects.</span></span>

### <a name="full-system-call-compatibility"></a><span data-ttu-id="e5ca8-164">システム コールの完全な互換性</span><span class="sxs-lookup"><span data-stu-id="e5ca8-164">Full system call compatibility</span></span>

<span data-ttu-id="e5ca8-165">Linux バイナリでは、システム コールを使用して、ファイルへのアクセス、メモリの要求、プロセスの作成などの機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-165">Linux binaries use system calls to perform functions such as accessing files, requesting memory, creating processes, and more.</span></span> <span data-ttu-id="e5ca8-166">WSL 1 では WSL チームが構築した変換レイヤーが使用されていましたが、WSL 2 にはシステム コールの完全な互換性を持つ独自の Linux カーネルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-166">Whereas WSL 1 used a translation layer that was built by the WSL team, WSL 2 includes its own Linux kernel with full system call compatibility.</span></span> <span data-ttu-id="e5ca8-167">次のような利点があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-167">Benefits include:</span></span>

* <span data-ttu-id="e5ca8-168">**[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** など、WSL 内で実行できるまったく新しいアプリのセット。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-168">A whole new set of apps that you can run inside of WSL, such as **[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** and more.</span></span>

* <span data-ttu-id="e5ca8-169">Linux カーネルに対する更新プログラムがすぐに使用可能になります</span><span class="sxs-lookup"><span data-stu-id="e5ca8-169">Any updates to the Linux kernel are immediately ready for use.</span></span> <span data-ttu-id="e5ca8-170">(WSL チームが更新プログラムを実装して変更を追加するまで待つ必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-170">(You don't have to wait for the WSL team to implement updates and add the changes).</span></span>

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a><span data-ttu-id="e5ca8-171">WSL 2 は起動時のメモリ使用量が少ない</span><span class="sxs-lookup"><span data-stu-id="e5ca8-171">WSL 2 uses a smaller amount of memory on startup</span></span>

<span data-ttu-id="e5ca8-172">WSL 2 では、メモリ フットプリントが小さな実際の Linux カーネル上で軽量のユーティリティ VM を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-172">WSL 2 uses a lightweight utility VM on a real Linux kernel with a small memory footprint.</span></span> <span data-ttu-id="e5ca8-173">このユーティリティは、仮想アドレスが使用されるメモリを起動時に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-173">The utility will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="e5ca8-174">これは、WSL 1 で必要とされていたよりも少ない割合の合計メモリで起動するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-174">It is configured to start with a smaller proportion of your total memory that what was required for WSL 1.</span></span>

## <a name="accessing-network-applications"></a><span data-ttu-id="e5ca8-175">ネットワーク アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="e5ca8-175">Accessing network applications</span></span>

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a><span data-ttu-id="e5ca8-176">Windows からの Linux ネットワーク アプリへのアクセス (localhost)</span><span class="sxs-lookup"><span data-stu-id="e5ca8-176">Accessing Linux networking apps from Windows (localhost)</span></span>

<span data-ttu-id="e5ca8-177">Linux ディストリビューションでネットワーク アプリ (たとえば、Node.js または SQL Server で実行されるアプリ) を構築する場合、(通常の場合と同様に) `localhost` を使用して (Microsoft Edge または Chrome インターネット ブラウザーなどの) Windows アプリからアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-177">If you are building a networking app (for example an app running on a NodeJS or SQL server) in your Linux distribution, you can access it from a Windows app (like your Edge or Chrome internet browser) using `localhost` (just like you normally would).</span></span>

<span data-ttu-id="e5ca8-178">ただし、Windows の古いバージョン (ビルド 18945 以下) を実行している場合は、Linux ホスト VM の IP アドレスを取得する (または[最新の Windows バージョンに更新する](ms-settings:windowsupdate)) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-178">However, if you are running an older version of Windows (Build 18945 or less), you will need to get the IP address of the Linux host VM (or [update to the latest Windows version](ms-settings:windowsupdate)).</span></span>

<span data-ttu-id="e5ca8-179">Linux ディストリビューションが動作する仮想マシンの IP アドレスを確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-179">To find the IP address of the virtual machine powering your Linux distribution:</span></span>

* <span data-ttu-id="e5ca8-180">WSL ディストリビューション (つまり、Ubuntu) から、次のコマンドを実行します: `ip addr`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-180">From your WSL distribution (ie Ubuntu), run the command: `ip addr`</span></span>
* <span data-ttu-id="e5ca8-181">`eth0` インターフェイスの `inet` 値の下で目的のアドレスを見つけてコピーします。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-181">Find and copy the address under the `inet` value of the `eth0` interface.</span></span>
* <span data-ttu-id="e5ca8-182">grep ツールがインストールされている場合は、次のコマンドを使用して出力をフィルター処理することにより、これをより簡単に見つけることができます: `ip addr | grep eth0`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-182">If you have the grep tool installed, find this more easily by filtering the output with the command: `ip addr | grep eth0`</span></span>
* <span data-ttu-id="e5ca8-183">この IP アドレスを使用して Linux サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-183">Connect to your Linux server using this IP address.</span></span>

<span data-ttu-id="e5ca8-184">次の図は、これを実行するために、Edge ブラウザーを使用して Node.js サーバーに接続する例です。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-184">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a><span data-ttu-id="e5ca8-186">Linux からの Windows ネットワーク アプリへのアクセス (ホスト IP)</span><span class="sxs-lookup"><span data-stu-id="e5ca8-186">Accessing Windows networking apps from Linux (host IP)</span></span>

<span data-ttu-id="e5ca8-187">Linux ディストリビューション (つまり、Ubuntu) から Windows 上で実行されているネットワーク アプリ (たとえば、Node.js または SQL Server で実行されるアプリ) にアクセスする場合は、ホスト マシンの IP アドレスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-187">If you want to access a networking app running on Windows (for example an app running on a NodeJS or SQL server) from your Linux distribution (ie Ubuntu), then you need to use the IP address of your host machine.</span></span> <span data-ttu-id="e5ca8-188">これは一般的なシナリオではありませんが、次の手順に従ってこれを実現できます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-188">While this is not a common scenario, you can follow these steps to make it work.</span></span>
    - <span data-ttu-id="e5ca8-189">Linux ディストリビューションから次のコマンドを実行して、ホスト マシンの IP アドレスを取得します: `cat /etc/resolv.conf`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-189">Obtain the IP address of your host machine by running this command from your Linux distribution: `cat /etc/resolv.conf`</span></span>
    - <span data-ttu-id="e5ca8-190">次の語句の後に IP アドレスをコピーします: `nameserver`。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-190">Copy the IP address following the term: `nameserver`.</span></span>
    - <span data-ttu-id="e5ca8-191">コピーした IP アドレスを使用して、Windows サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-191">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="e5ca8-192">次の図は、これを実行するために、curl を介して Windows で実行されている Node.js サーバーに接続する例です。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-192">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span>

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a><span data-ttu-id="e5ca8-194">ネットワークに関する追加の考慮事項</span><span class="sxs-lookup"><span data-stu-id="e5ca8-194">Additional networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="e5ca8-195">リモート IP アドレスを使用した接続</span><span class="sxs-lookup"><span data-stu-id="e5ca8-195">Connecting via remote IP addresses</span></span>

<span data-ttu-id="e5ca8-196">リモート IP アドレスを使用してアプリケーションに接続すると、ローカル エリア ネットワーク (LAN) からの接続として扱われます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-196">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="e5ca8-197">これは、アプリケーションで LAN 接続を受け入れることができるようにする必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-197">This means that you will need to make sure your application can accept LAN connections.</span></span>

<span data-ttu-id="e5ca8-198">たとえば、場合によっては、`127.0.0.1` ではなく `0.0.0.0` にアプリケーションをバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-198">For example, you may need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="e5ca8-199">Flask を使用する Python アプリの例では、次のコマンドを使用してこれを実行できます: `app.run(host='0.0.0.0')`。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-199">In the example of a Python app using Flask, this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="e5ca8-200">これらの変更を行うと、LAN からの接続が許可されるため、セキュリティに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-200">Please keep security in mind when making these changes as this will allow connections from your LAN.</span></span>

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a><span data-ttu-id="e5ca8-201">ローカル エリア ネットワーク (LAN) からの WSL 2 ディストリビューションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="e5ca8-201">Accessing a WSL 2 distribution from your local area network (LAN)</span></span>

<span data-ttu-id="e5ca8-202">WSL 1 ディストリビューションを使用している場合、LAN からアクセスできるようにコンピューターが設定されていれば、WSL で実行されているアプリケーションに LAN からもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-202">When using a WSL 1 distribution, if your computer was set up to be accessed by your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span>

<span data-ttu-id="e5ca8-203">WSL 2 では、これは既定の動作ではありません。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-203">This isn't the default case in WSL 2.</span></span> <span data-ttu-id="e5ca8-204">WSL 2 には、独自の一意の IP アドレスを持つ仮想化されたイーサネット アダプターがあります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-204">WSL 2 has a virtualized ethernet adapter with its own unique IP address.</span></span> <span data-ttu-id="e5ca8-205">現在、このワークフローを有効にするには、通常の仮想マシンの場合と同じ手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-205">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="e5ca8-206">(Microsoft は、このエクスペリエンスを改善する方法を検討しています)。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-206">(We are looking into ways to improve this experience.)</span></span>

<span data-ttu-id="e5ca8-207">次に、ホスト上のポート 4000 でリッスンし、それを IP アドレス 192.168.101.100 の WSL 2 VM のポート 4000 に接続するポート プロキシを追加する PowerShell コマンドの例を示します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-207">Here's an example PowerShell command to add a port proxy that listens on port 4000 on the host and connects it to port 4000 to the WSL 2 VM with IP address 192.168.101.100.</span></span>
```powershell
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.101.100
```

#### <a name="ipv6-access"></a><span data-ttu-id="e5ca8-208">IPv6 アクセス</span><span class="sxs-lookup"><span data-stu-id="e5ca8-208">IPv6 access</span></span>

<span data-ttu-id="e5ca8-209">WSL 2 ディストリビューションは、現在、IPv6 のみのアドレスに到達できません。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-209">WSL 2 distributions currently cannot reach IPv6-only addresses.</span></span> <span data-ttu-id="e5ca8-210">Microsoft は、この機能の追加に取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-210">We are working on adding this feature.</span></span>

## <a name="expanding-the-size-of-your-wsl-2-virtual-hardware-disk"></a><span data-ttu-id="e5ca8-211">WSL 2 仮想ハードウェア ディスクのサイズの拡張</span><span class="sxs-lookup"><span data-stu-id="e5ca8-211">Expanding the size of your WSL 2 Virtual Hardware Disk</span></span>

<span data-ttu-id="e5ca8-212">WSL 2 では、仮想ハードウェア ディスク (VHD) を使用して Linux ファイルを格納します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-212">WSL 2 uses a Virtual Hardware Disk (VHD) to store your Linux files.</span></span> <span data-ttu-id="e5ca8-213">場合によっては、その最大サイズに達したときにサイズを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-213">If you reach its max size you may need to expand it.</span></span>

<span data-ttu-id="e5ca8-214">WSL 2 VHD では、ext4 ファイル システムが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-214">The WSL 2 VHD uses the ext4 file system.</span></span> <span data-ttu-id="e5ca8-215">この VHD は、ストレージのニーズに合わせて自動的にサイズが変更されます。初期の最大サイズは 256 GB です。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-215">This VHD automatically resizes to meet your storage needs and has an initial maximum size of 256GB.</span></span> <span data-ttu-id="e5ca8-216">ディストリビューションが 256 GB を超えるサイズになると、ディスク領域が不足していることを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-216">If your distribution grows in size to be greater than 256GB, you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="e5ca8-217">このエラーは、VHD サイズを拡張することで修正できます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-217">You can fix this error by expanding the VHD size.</span></span>

<span data-ttu-id="e5ca8-218">256 GB を超えて VHD の最大サイズを拡張するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-218">To expand your maximum VHD size beyond 256GB:</span></span>

1. <span data-ttu-id="e5ca8-219">次のコマンドを使用して、すべての WSL インスタンスを終了します: `wsl --shutdown`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-219">Terminate all WSL instances using the command: `wsl --shutdown`</span></span>

2. <span data-ttu-id="e5ca8-220">ディストリビューションのインストール パッケージ名 ("PackageFamilyName") を見つけます</span><span class="sxs-lookup"><span data-stu-id="e5ca8-220">Find your distribution installation package name ('PackageFamilyName')</span></span>
    * <span data-ttu-id="e5ca8-221">PowerShell を使用して、次のコマンドを入力します ("distro" はディストリビューション名です):</span><span class="sxs-lookup"><span data-stu-id="e5ca8-221">Using PowerShell (where 'distro' is your distribution name) enter the command:</span></span>
    * `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. <span data-ttu-id="e5ca8-222">WSL 2 のインストールで使用される VHD ファイルの `fullpath` を特定します。これが `pathToVHD` になります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-222">Locate the VHD file `fullpath` used by your WSL 2 installation, this will be your `pathToVHD`:</span></span>
     * `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. <span data-ttu-id="e5ca8-223">次のコマンドを実行して、WSL 2 VHD のサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-223">Resize your WSL 2 VHD by completing the following commands:</span></span>
   * <span data-ttu-id="e5ca8-224">管理者特権で Windows コマンド プロンプトを開き、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-224">Open Windows Command Prompt with admin privileges and enter:</span></span>
      * `diskpart`
      * `Select vdisk file="<pathToVHD>"`
      * `expand vdisk maximum="<sizeInMegaBytes>"`

5. <span data-ttu-id="e5ca8-225">WSL ディストリビューション (たとえば、Ubuntu) を起動します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-225">Launch your WSL distribution (Ubuntu, for example).</span></span>

6. <span data-ttu-id="e5ca8-226">Linux ディストリビューションのコマンド ラインから次のコマンドを実行して、ファイル システムのサイズを拡張できることを WSL に認識させます。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-226">Make WSL aware that it can expand its file system's size by running these commands from your Linux distribution command line:</span></span>
    * `sudo mount -t devtmpfs none /dev`
    * `mount | grep ext4`
    * <span data-ttu-id="e5ca8-227">`/dev/sdXX` のようなこのエントリの名前をコピーします (X は他の文字を表します)</span><span class="sxs-lookup"><span data-stu-id="e5ca8-227">Copy the name of this entry, which will look like: `/dev/sdXX` (with the X representing any other character)</span></span>
    * `sudo resize2fs /dev/sdXX`
    * <span data-ttu-id="e5ca8-228">前の手順でコピーした値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-228">Use the value you copied earlier.</span></span> <span data-ttu-id="e5ca8-229">resize2fs のインストールが必要になる場合もあります: `apt install resize2fs`</span><span class="sxs-lookup"><span data-stu-id="e5ca8-229">You may also need to install resize2fs: `apt install resize2fs`</span></span>

> [!NOTE]
> <span data-ttu-id="e5ca8-230">通常、Windows ツールまたはエディターを使用して、AppData フォルダー内にある WSL 関連ファイルを変更、移動、またはアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-230">In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="e5ca8-231">そうすると、Linux ディストリビューションが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e5ca8-231">Doing so could cause your Linux distribution to become corrupted.</span></span>
