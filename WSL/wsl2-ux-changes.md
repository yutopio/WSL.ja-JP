---
title: WSL 1 と WSL 2 の間での UX の変更
description: WSL 1 と WSL 2 間のユーザーエクスペリエンスの変更
keywords: BashOnWindows、bash、wsl、wsl2、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3addfd27d777731bf92efab42c6bcd4be415779b
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020967"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="318a4-104">WSL 1 と WSL 2 間のユーザーエクスペリエンスの変更</span><span class="sxs-lookup"><span data-stu-id="318a4-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="318a4-105">このページでは、WSL 1 と WSL 2 preview のユーザーエクスペリエンスの違いについて紹介します。</span><span class="sxs-lookup"><span data-stu-id="318a4-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="318a4-106">注意すべき重要な変更点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="318a4-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="318a4-107">Linux アプリが Linux ルートファイルシステムにアクセスするファイルを配置して、ファイルのパフォーマンスを高速化します。</span><span class="sxs-lookup"><span data-stu-id="318a4-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="318a4-108">WSL 2 preview の初期ビルドでは、localhost を使用せずに IP アドレスを使用してネットワークアプリケーションにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="318a4-109">次に、その他の変更点の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="318a4-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="318a4-110">WSL 2 では、[仮想ハードウェアディスク](https://en.wikipedia.org/wiki/VHD_(file_format))(VHD) を使用してファイルを格納します。最大サイズに達した場合は、拡張が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="318a4-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="318a4-111">開始時に WSL 2 では、メモリの割合がわずかに使用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="318a4-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="318a4-112">最初のプレビュービルドで、OS 間のファイルアクセス速度が低下する</span><span class="sxs-lookup"><span data-stu-id="318a4-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="318a4-113">Linux のルートファイルシステムに Linux ファイルを配置する</span><span class="sxs-lookup"><span data-stu-id="318a4-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="318a4-114">ファイルのパフォーマンスを向上させるために、linux アプリケーションで頻繁にアクセスするファイルを linux ルートファイルシステム内に配置してください。</span><span class="sxs-lookup"><span data-stu-id="318a4-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="318a4-115">これらのファイルは、ファイルシステムへのアクセスを高速化するために、Linux ルートファイルシステム内に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="318a4-116">また、Windows アプリが Linux ルートファイルシステム (エクスプローラーなど) にアクセスできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="318a4-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="318a4-117">Linux ディストリビューションの`explorer.exe .`ホームディレクトリでを実行してみてください。これにより、この移行が大幅に簡単になります。</span><span class="sxs-lookup"><span data-stu-id="318a4-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="318a4-118">ネットワークアプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="318a4-118">Accessing network applications</span></span>
<span data-ttu-id="318a4-119">WSL 2 preview の最初のビルドでは、Linux ディストリビューションの IP アドレスと、ホストコンピューターの IP アドレスを使用して Linux から任意の Windows server を使用して、Windows から任意の Linux サーバーにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-119">In the initial builds of the WSL 2 preview, you will need to access any Linux server from Windows using the IP address of your Linux distro, and any Windows server from Linux using the IP address of your host machine.</span></span> <span data-ttu-id="318a4-120">これは一時的なものであり、修正する優先順位リストでは非常に高くなっています。</span><span class="sxs-lookup"><span data-stu-id="318a4-120">This is something that is temporary, and very high on our priority list to fix.</span></span>

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="318a4-121">Windows からの Linux アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="318a4-121">Accessing Linux applications from Windows</span></span>
<span data-ttu-id="318a4-122">WSL ディストリビューションにサーバーがある場合は、ディストリビューションの電源を入れている仮想マシンの IP アドレスを検索し、その IP アドレスを使用して接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-122">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="318a4-123">これを行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="318a4-123">You can do that by following these steps:</span></span>

- <span data-ttu-id="318a4-124">Wsl ディストリビューション内でコマンドを実行し、 `ip addr` `eth0`インターフェイスの`inet`値の下でそのコマンドを見つけることによって、ディストリビューションの IP アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="318a4-124">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="318a4-125">これは、のように`ip addr | grep eth0`grep を使用してコマンドの出力をフィルター処理することで、より簡単に見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="318a4-125">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="318a4-126">上記の IP を使用して、Linux サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="318a4-126">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="318a4-127">次の図は、Edge ブラウザーを使用して node.js サーバーに接続することによって、この例を示しています。</span><span class="sxs-lookup"><span data-stu-id="318a4-127">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![Windows からの Linux ネットワークアプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="318a4-129">Linux からの Windows アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="318a4-129">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="318a4-130">Windows ネットワークアプリケーションにアクセスするには、ホストコンピューターの IP アドレスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-130">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="318a4-131">これを行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="318a4-131">You can do so with these steps:</span></span>

- <span data-ttu-id="318a4-132">コマンド`cat /etc/resolv.conf`を実行し、という用語`nameserver`の後に ip アドレスをコピーして、ホストコンピューターの ip アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="318a4-132">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="318a4-133">コピーした IP アドレスを使用して、任意の Windows サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="318a4-133">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="318a4-134">次の図は、curl を介して Windows で実行されている node.js サーバーに接続することによって、この例を示しています。</span><span class="sxs-lookup"><span data-stu-id="318a4-134">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![Windows からの Linux ネットワークアプリケーションへのアクセス](media/wsl2-network-l2w.png)

### <a name="other-networking-considerations"></a><span data-ttu-id="318a4-136">ネットワークに関するその他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="318a4-136">Other networking considerations</span></span>

<span data-ttu-id="318a4-137">リモート IP アドレスを使用してアプリケーションに接続すると、ローカルエリアネットワーク (LAN) からの接続として扱われます。</span><span class="sxs-lookup"><span data-stu-id="318a4-137">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="318a4-138">つまり、アプリケーションが LAN 接続を受け入れることができることを確認する必要があります。次に例を示します。`0.0.0.0` の`127.0.0.1`代わりに、アプリケーションをにバインドすることが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-138">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="318a4-139">たとえば、flask を使用した python では、コマンド`app.run(host='0.0.0.0')`を使用してこれを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="318a4-139">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="318a4-140">これらの変更を行う場合は、LAN からの接続が許可されるため、セキュリティを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="318a4-140">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="318a4-141">WSL 2 を理解すると、VHD が使用され、最大サイズに達した場合の対処方法がわかります。</span><span class="sxs-lookup"><span data-stu-id="318a4-141">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="318a4-142">WSL 2 では、ext4 ファイルシステムを使用する VHD 内にすべての Linux ファイルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="318a4-142">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="318a4-143">この VHD は、ストレージのニーズに合わせて自動的にサイズ変更されます。</span><span class="sxs-lookup"><span data-stu-id="318a4-143">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="318a4-144">この VHD には、256 GB の初期の最大サイズもあります。</span><span class="sxs-lookup"><span data-stu-id="318a4-144">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="318a4-145">ディストリビューションのサイズが 256 GB よりも大きくなると、ディスク領域が不足していることを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="318a4-145">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="318a4-146">VHD のサイズを拡張することで、これらの問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="318a4-146">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="318a4-147">その方法については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="318a4-147">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="318a4-148">コマンドを使用してすべての`wsl --shutdown` wsl インスタンスを終了します</span><span class="sxs-lookup"><span data-stu-id="318a4-148">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="318a4-149">ディストリビューションのインストールパッケージ名 ' 整理 Efamilyname ' を検索します</span><span class="sxs-lookup"><span data-stu-id="318a4-149">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="318a4-150">Powershell プロンプトで、次のように入力します (' distribution ' は配布名です)。</span><span class="sxs-lookup"><span data-stu-id="318a4-150">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="318a4-151">WSL 2 のインストールで使用される VHD ファイルの場所を特定します。これは ' pathToVHD ' になります。</span><span class="sxs-lookup"><span data-stu-id="318a4-151">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="318a4-152">次のコマンドを実行して、WSL 2 VHD のサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="318a4-152">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="318a4-153">管理者特権でコマンドプロンプトウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="318a4-153">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="318a4-154">WSL ディストリビューションを起動します</span><span class="sxs-lookup"><span data-stu-id="318a4-154">Launch your WSL distro</span></span>
6. <span data-ttu-id="318a4-155">ファイルシステムのサイズを拡張できることを WSL に認識させる</span><span class="sxs-lookup"><span data-stu-id="318a4-155">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="318a4-156">WSL ディストリビューションで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="318a4-156">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="318a4-157">このエントリの名前をコピーします。次のようになります (X は他の文字を表します)。</span><span class="sxs-lookup"><span data-stu-id="318a4-157">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="318a4-158">前の手順`apt install resize2fs`でコピーした値を使用してください。を使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-158">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="318a4-159">注意:通常は、Windows のツールまたはエディターを使用して、AppData フォルダー内にある WSL 関連ファイルを変更、移動、またはアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="318a4-159">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="318a4-160">これにより、Linux ディストリビューションが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="318a4-160">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="318a4-161">WSL 2 は起動時にメモリを使用します</span><span class="sxs-lookup"><span data-stu-id="318a4-161">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="318a4-162">WSL 2 は、実際の Linux カーネル上で軽量のユーティリティ VM を使用して、優れたファイルシステムのパフォーマンスとシステムコールの完全な互換性を実現しながら、WSL 1 と同じようにライト、高速、統合、応答性を提供します。</span><span class="sxs-lookup"><span data-stu-id="318a4-162">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="318a4-163">このユーティリティ VM ではメモリフットプリントが小さく、起動時に仮想アドレスがサポートされるメモリが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="318a4-163">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="318a4-164">これは、メモリの合計のごく一部から開始するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="318a4-164">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="318a4-165">最初のプレビュービルドで、OS 間のファイル速度が遅くなる</span><span class="sxs-lookup"><span data-stu-id="318a4-165">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="318a4-166">Linux アプリケーションから Windows ファイルにアクセスする場合、または Windows アプリケーションから Linux ファイルにアクセスする場合は、WSL 1 と比較してファイルの速度が遅いことがわかります。</span><span class="sxs-lookup"><span data-stu-id="318a4-166">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="318a4-167">これは、WSL 2 でのアーキテクチャの変更の結果であり、WSL チームがこのエクスペリエンスを向上させる方法について積極的に調査しているものです。</span><span class="sxs-lookup"><span data-stu-id="318a4-167">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
