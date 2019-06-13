---
title: WSL 1 と 2 WSL UX の変更点
description: WSL 1 と 2 の WSL の間のユーザー エクスペリエンスの変更
keywords: BashOnWindows、bash、wsl、wsl2、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10 用 windows サブシステム
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038102"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="c34ab-104">WSL 1 と 2 の WSL の間のユーザー エクスペリエンスの変更</span><span class="sxs-lookup"><span data-stu-id="c34ab-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="c34ab-105">このページ WSL 1 と WSL 2 プレビューのユーザー エクスペリエンスの違いを経由します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="c34ab-106">注意すべき主な変更は。</span><span class="sxs-lookup"><span data-stu-id="c34ab-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="c34ab-107">Linux ルート ファイル システムに高速ファイル パフォーマンスの速度は、Linux アプリにアクセスするファイルを配置します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="c34ab-108">WSL 2 プレビューの初期のビルドでは、IP アドレスを使用して、localhost を使用していないネットワーク アプリケーションにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="c34ab-109">お気付きの他の変更の完全な一覧を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="c34ab-110">WSL 2 は、VHD を使用してファイルを格納する、その最大サイズに達した場合は、展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-110">WSL 2 uses a VHD to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="c34ab-111">WSL 2 がメモリの小さな割合を使用して今すぐ起動する場合、</span><span class="sxs-lookup"><span data-stu-id="c34ab-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="c34ab-112">クロス OS ファイル アクセスの速度は初期のプレビュー ビルドの速度は遅くなります</span><span class="sxs-lookup"><span data-stu-id="c34ab-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="c34ab-113">Linux ファイルを Linux のルート ファイル システムに配置します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="c34ab-114">Linux で頻繁にアクセスするファイルを配置することを確認、Linux 内のアプリケーションのルート ファイル システム、ファイルのパフォーマンスのメリットを活用します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="c34ab-115">これらのファイルは、ファイル システムより高速にアクセスするためには、Linux ルート ファイル システムの内側に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="c34ab-116">私たちがもできるように (ファイル エクスプ ローラーのような Linux ルート ファイル システムにアクセスする Windows アプリ!</span><span class="sxs-lookup"><span data-stu-id="c34ab-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="c34ab-117">実行してみてください: `explorer.exe /` bash シェルとどうなるでしょうか) この移行を大幅に簡素化することはできます。</span><span class="sxs-lookup"><span data-stu-id="c34ab-117">Try running: `explorer.exe /` in your bash shell and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="c34ab-118">ネットワーク アプリケーションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c34ab-118">Accessing network applications</span></span>
<span data-ttu-id="c34ab-119">WSL 2 プレビューの初期のビルドでは、Linux ディストリビューションと、ホスト コンピューターの IP アドレスを使用して Linux から任意の Windows サーバーの IP アドレスを使用して Windows から任意の Linux サーバーにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-119">In the initial builds of the WSL 2 preview, you will need to access any Linux server from Windows using the IP address of your Linux distro, and any Windows server from Linux using the IP address of your host machine.</span></span> <span data-ttu-id="c34ab-120">これは、一時、および、優先順位の一覧を修正するには非常に高いのあるものです。</span><span class="sxs-lookup"><span data-stu-id="c34ab-120">This is something that is temporary, and very high on our priority list to fix.</span></span>

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="c34ab-121">Windows から Linux アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="c34ab-121">Accessing Linux applications from Windows</span></span>
<span data-ttu-id="c34ab-122">WSL ディストリビューションで、サーバーがある場合は、ディストリビューションの電源、仮想マシンの IP アドレスを見つけて、その IP アドレスで接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-122">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="c34ab-123">次の手順で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c34ab-123">You can do that by following these steps:</span></span>

- <span data-ttu-id="c34ab-124">コマンドを実行して、ディストリビューションの IP アドレスを取得する`ip addr`、WSL ディストリビューションと下の検索の内部で、`inet`の値、`eth0`インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="c34ab-124">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="c34ab-125">正規表現を使用して、コマンドの出力のフィルター処理をより簡単に表示できるようになります:`ip addr | grep eth0`します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-125">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="c34ab-126">上記で見つかった ip アドレスを使用して Linux サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-126">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="c34ab-127">次の図は、Edge ブラウザーを使って nodeJS サーバーに接続することで、この例を示します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-127">The picture below shows an example of this by connecting to a nodeJS server using the Edge browser.</span></span>

![Windows から Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="c34ab-129">Linux から Windows アプリケーションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c34ab-129">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="c34ab-130">Windows ネットワーク アプリケーションへのアクセスには、ホスト コンピューターの IP アドレスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-130">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="c34ab-131">次の手順を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c34ab-131">You can do so with these steps:</span></span>

- <span data-ttu-id="c34ab-132">コマンドを実行して、ホスト コンピューターの IP アドレスを取得`cat /etc/resolv.conf`という用語を次の IP アドレスをコピーおよび`nameserver`します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-132">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="c34ab-133">コピー元の IP アドレスを使用して任意の Windows サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-133">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="c34ab-134">次の図は、curl を使用して、Windows で実行されている python のサーバーに接続して、この例を示します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-134">The picture below shows an example of this by connecting to a python server running in Windows via curl.</span></span> 

![Windows から Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="c34ab-136">VHD、およびその最大サイズに達した場合の対処方法を使用して WSL 2 を理解します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-136">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="c34ab-137">WSL 2 では、ext4 ファイル システムを使用する VHD 内のすべての Linux ファイルを格納します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-137">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="c34ab-138">この VHD は、記憶域のニーズを満たすために自動的にサイズ変更します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-138">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="c34ab-139">この VHD には、256 GB の初期の最大サイズもあります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-139">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="c34ab-140">256 GB を超えるサイズで、ディストリビューションが増加する場合は、ディスク領域不足を実行したことを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c34ab-140">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="c34ab-141">VHD のサイズを拡張することで、これらを修正することができます。</span><span class="sxs-lookup"><span data-stu-id="c34ab-141">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="c34ab-142">これを行う方法については次に示します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-142">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="c34ab-143">使用してすべての WSL インスタンスを終了、`wsl --shutdown`コマンド</span><span class="sxs-lookup"><span data-stu-id="c34ab-143">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="c34ab-144">次のコマンドを実行して、WSL 2 の VHD のサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-144">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="c34ab-145">管理者特権でコマンド プロンプト ウィンドウを開きし、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-145">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. <span data-ttu-id="c34ab-146">WSL、ディストリビューションを起動します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-146">Launch your WSL distro</span></span>
4. <span data-ttu-id="c34ab-147">WSL のファイル システムのサイズを展開できることを認識します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-147">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="c34ab-148">WSL ディストリビューションでは、これらのコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-148">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="c34ab-149">ようになりますが、このエントリの名前をコピー:/開発/sdXX (X 印が付いた他の任意の文字を表す)</span><span class="sxs-lookup"><span data-stu-id="c34ab-149">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="c34ab-150">値を使用して、先ほどコピーした、使用する必要があるかどうかを確認します。`apt install resize2fs`します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-150">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="c34ab-151">WSL 2 は、メモリの一部を使用して起動時には</span><span class="sxs-lookup"><span data-stu-id="c34ab-151">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="c34ab-152">WSL 2 では、実際の Linux カーネルで軽量ユーティリティ VM を使用して、優れたファイル システムのパフォーマンスとフル システム呼び出しがまだ中に、光と同様の互換性高速で統合や WSL 1 と応答性を提供します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-152">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="c34ab-153">このユーティリティの VM は、メモリ使用量を備えは起動時にバックアップされた仮想アドレスのメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="c34ab-153">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="c34ab-154">合計メモリの小さな割合を開始する構成されます。</span><span class="sxs-lookup"><span data-stu-id="c34ab-154">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="c34ab-155">クロス OS ファイルの速度は初期のプレビュー ビルドの速度は遅くなります</span><span class="sxs-lookup"><span data-stu-id="c34ab-155">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="c34ab-156">Linux アプリケーションの場合は、または Windows アプリケーションから Linux ファイルへのアクセスから Windows ファイルにアクセスするときに WSL 1 と比較ファイルの速度が遅くなることがわかります。</span><span class="sxs-lookup"><span data-stu-id="c34ab-156">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="c34ab-157">これは WSL 2 では、アーキテクチャの変更の結果であり、WSL チームが積極的には、このエクスペリエンスを向上させる方法を調査します。</span><span class="sxs-lookup"><span data-stu-id="c34ab-157">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>