---
title: WSL 1 から WSL 2 の UX の変更点
description: WSL 1 から WSL 2 のユーザー エクスペリエンスの変更点
keywords: BashOnWindows, bash, wsl, wsl2, windows, Linux 用 Windows サブシステム, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1965a22a2e290777b207d9ded099ce4a79e1ed38
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256335"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="74e4f-104">WSL 1 から WSL 2 のユーザー エクスペリエンスの変更点</span><span class="sxs-lookup"><span data-stu-id="74e4f-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="74e4f-105">このページでは、WSL 1 と WSL 2 プレビューのユーザー エクスペリエンスの違いについて説明します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="74e4f-106">注意すべき重要な変更点は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="74e4f-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="74e4f-107">ファイルのパフォーマンスを高速化するには、Linux アプリからアクセスするファイルを Linux ルート ファイル システムに配置します</span><span class="sxs-lookup"><span data-stu-id="74e4f-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="74e4f-108">WSL 2 プレビューの初期ビルドでは、localhost を使用せずに IP アドレスを使用してネットワーク アプリケーションにアクセスする必要があります</span><span class="sxs-lookup"><span data-stu-id="74e4f-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="74e4f-109">その他の変更の詳細な一覧は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="74e4f-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="74e4f-110">WSL 2 には、ファイルの格納に [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) が使用されており、最大サイズに達した場合は拡張が必要になることがあります</span><span class="sxs-lookup"><span data-stu-id="74e4f-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="74e4f-111">WSL 2 では、起動時に使用されるメモリが少なくなります</span><span class="sxs-lookup"><span data-stu-id="74e4f-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="74e4f-112">初期のプレビュー ビルドでは、OS 間のファイル アクセス速度が低下します</span><span class="sxs-lookup"><span data-stu-id="74e4f-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="74e4f-113">Linux ルート ファイル システムに Linux ファイルを配置する</span><span class="sxs-lookup"><span data-stu-id="74e4f-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="74e4f-114">ファイルのパフォーマンスを向上させるには、Linux アプリケーションで頻繁にアクセスするファイルを Linux ルート ファイル システム内に配置します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="74e4f-115">ファイル システムへのアクセスを高速化するには、このようなファイルを Linux ルート ファイル システム内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="74e4f-116">また、Windows アプリから Linux ルート ファイル システムにアクセスできるようになりました (たとえば、エクスプローラーなどです。</span><span class="sxs-lookup"><span data-stu-id="74e4f-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="74e4f-117">Linux ディストリビューションのホーム ディレクトリで `explorer.exe .` を実行し、結果を確認してみてください)。この移行が非常に簡単になります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="74e4f-118">ネットワーク アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="74e4f-118">Accessing network applications</span></span>
<span data-ttu-id="74e4f-119">WSL 2 プレビューの初期ビルドでは、ホスト コンピューターの IP アドレスを使用して、Linux から Windows サーバーにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-119">In the initial builds of the WSL 2 preview, you will need to access any Windows server from Linux using the IP address of your host machine.</span></span>

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="74e4f-120">Linux から Windows アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="74e4f-120">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="74e4f-121">Windows ネットワーク アプリケーションにアクセスするには、ホスト コンピューターの IP アドレスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-121">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="74e4f-122">これを行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-122">You can do so with these steps:</span></span>

- <span data-ttu-id="74e4f-123">コマンド `cat /etc/resolv.conf` を実行し、用語 `nameserver` に続く IP アドレスをコピーして、ホスト コンピューターの IP アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-123">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="74e4f-124">コピーした IP アドレスを使用して、Windows サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-124">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="74e4f-125">次の図は、これを実行するために、curl を介して Windows で実行されている Node.js サーバーに接続する例です。</span><span class="sxs-lookup"><span data-stu-id="74e4f-125">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="74e4f-127">Windows からの Linux アプリケーションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="74e4f-127">Accessing Linux applications from Windows</span></span>

<span data-ttu-id="74e4f-128">使用している Windows のバージョンによっては、仮想マシンの IP アドレスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-128">Depending on which version of Windows you're using, you might need to retrieve the IP address of the virtual machine.</span></span> <span data-ttu-id="74e4f-129">ビルドが 18945 以降の場合は、通常と同様に `localhost` を使用できます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-129">If your build is 18945 or higher, you can use `localhost` just like normal.</span></span> 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a><span data-ttu-id="74e4f-130">[18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/) よりも前のビルドでの Linux へのアクセス</span><span class="sxs-lookup"><span data-stu-id="74e4f-130">Accessing Linux on Builds lower than [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)</span></span>

<span data-ttu-id="74e4f-131">WSL ディストリビューションにサーバーがある場合は、ディストリビューションをホストしている仮想マシンの IP アドレスを見つけて、その IP アドレスで接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-131">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="74e4f-132">これを行うには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-132">You can do that by following these steps:</span></span>

- <span data-ttu-id="74e4f-133">WSL ディストリビューション内でコマンド `ip addr` を実行して、ディストリビューションの IP アドレスを取得します。`eth0` インターフェイスの `inet` 値の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-133">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="74e4f-134">この簡単に見つけるには、`ip addr | grep eth0` のように grep を使用してコマンドの出力をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-134">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="74e4f-135">前述の手順で見つけた IP を使用して Linux サーバーに接続します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-135">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="74e4f-136">次の図は、これを実行するために、Edge ブラウザーを使用して Node.js サーバーに接続する例です。</span><span class="sxs-lookup"><span data-stu-id="74e4f-136">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![Windows からの Linux ネットワーク アプリケーションへのアクセス](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a><span data-ttu-id="74e4f-138">ネットワークに関するその他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="74e4f-138">Other networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="74e4f-139">リモート IP アドレスを使用した接続</span><span class="sxs-lookup"><span data-stu-id="74e4f-139">Connecting via remote IP addresses</span></span>

<span data-ttu-id="74e4f-140">リモート IP アドレスを使用してアプリケーションに接続すると、ローカル エリア ネットワーク (LAN) からの接続として扱われます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-140">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="74e4f-141">これは、アプリケーションで LAN 接続を受け入れることができるようにする必要があることを意味します。つまり、必要に応じて、`127.0.0.1` ではなく `0.0.0.0` にアプリケーションをバインドします。</span><span class="sxs-lookup"><span data-stu-id="74e4f-141">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="74e4f-142">たとえば、flask を使用する python では、コマンド `app.run(host='0.0.0.0')` を使用してこれを実行できます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-142">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="74e4f-143">これらの変更を行うと、LAN からの接続が許可されるため、セキュリティに注意してください。</span><span class="sxs-lookup"><span data-stu-id="74e4f-143">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a><span data-ttu-id="74e4f-144">ローカル エリア ネットワーク (LAN) からの WSL2 ディストリビューションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="74e4f-144">Accessing a WSL2 distro from your local area network (LAN)</span></span>

<span data-ttu-id="74e4f-145">WSL1 ディストリビューションを使用している場合、LAN からアクセスできるようにコンピューターが設定されていれば、WSL で実行されているアプリケーションに LAN からもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-145">When using a WSL1 distro, if your computer was set up to be accessed by in your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span> <span data-ttu-id="74e4f-146">これは WSL2 の既定の場合には該当しません。WSL2 には独自の IP アドレスを持つ仮想化されたイーサネット アダプターがあるからです。</span><span class="sxs-lookup"><span data-stu-id="74e4f-146">This isn't the default case in WSL2, as WSL2 has a virtualized ethernet adapter with its own IP address.</span></span> <span data-ttu-id="74e4f-147">現在、このワークフローを有効にするには、通常の仮想マシンの場合と同じ手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-147">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="74e4f-148">Microsoft は、このエクスペリエンスを改善する方法を検討しています。</span><span class="sxs-lookup"><span data-stu-id="74e4f-148">We are looking into ways to improve this experience!</span></span>

#### <a name="ipv6-access"></a><span data-ttu-id="74e4f-149">IPv6 アクセス</span><span class="sxs-lookup"><span data-stu-id="74e4f-149">IPv6 access</span></span>

<span data-ttu-id="74e4f-150">WSL2 ディストリビューションは、現在、IPv6 のみのアドレスに到達できません。</span><span class="sxs-lookup"><span data-stu-id="74e4f-150">WSL2 distros currently cannot reach IPv6 only addresses.</span></span> <span data-ttu-id="74e4f-151">Microsoft は、この機能の追加に取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-151">We are working on adding this feature.</span></span>

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="74e4f-152">WSL 2 による VHD の使用と、最大サイズに達した場合の対処方法の概要</span><span class="sxs-lookup"><span data-stu-id="74e4f-152">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="74e4f-153">WSL 2 では、ext4 ファイル システムを使用する VHD 内にすべての Linux ファイルが格納されています。</span><span class="sxs-lookup"><span data-stu-id="74e4f-153">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="74e4f-154">この VHD は、ストレージのニーズに合わせて自動的にサイズが変更されます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-154">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="74e4f-155">この VHD には、256 GB という初期の最大サイズもあります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-155">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="74e4f-156">ディストリビューションが 256 GB を超えるサイズになると、ディスク領域が不足していることを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-156">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="74e4f-157">VHD のサイズを拡張することで、これらの問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-157">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="74e4f-158">その方法の手順は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="74e4f-158">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="74e4f-159">`wsl --shutdown` コマンドを使用してすべての WSL インスタンスを終了します</span><span class="sxs-lookup"><span data-stu-id="74e4f-159">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="74e4f-160">"PackageFamilyName" というディストリビューションのインストール パッケージ名を見つけます</span><span class="sxs-lookup"><span data-stu-id="74e4f-160">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="74e4f-161">powershell プロンプトで、次のように入力します ("distro" はディストリビューション名です)。</span><span class="sxs-lookup"><span data-stu-id="74e4f-161">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="74e4f-162">WSL 2 のインストールで使用される VHD ファイルのファイルパスを特定します。これは "pathToVHD" になります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-162">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="74e4f-163">次のコマンドを実行して、WSL 2 VHD のサイズを変更します</span><span class="sxs-lookup"><span data-stu-id="74e4f-163">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="74e4f-164">管理者特権でコマンド プロンプト ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-164">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="74e4f-165">WSL ディストリビューションを起動します</span><span class="sxs-lookup"><span data-stu-id="74e4f-165">Launch your WSL distro</span></span>
6. <span data-ttu-id="74e4f-166">ファイル システムのサイズを拡張できることを WSL に認識させます</span><span class="sxs-lookup"><span data-stu-id="74e4f-166">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="74e4f-167">WSL ディストリビューションで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="74e4f-167">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="74e4f-168">/dev/sdXX のようなこのエントリの名前をコピーします (X は他の文字を表します)</span><span class="sxs-lookup"><span data-stu-id="74e4f-168">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="74e4f-169">以前の手順でコピーした値を必ず使用します。必要に応じて `apt install resize2fs` を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-169">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="74e4f-170">注意: 通常、Windows ツールまたはエディターを使用して、AppData フォルダー内にある WSL 関連ファイルを変更、移動、またはアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="74e4f-170">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="74e4f-171">そうすると、Linux ディストリビューションが破損する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-171">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="74e4f-172">起動時に WSL 2 に使用されるメモリ</span><span class="sxs-lookup"><span data-stu-id="74e4f-172">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="74e4f-173">WSL 2 では、実際の Linux カーネル上で軽量のユーティリティ VM が使用されており、ファイル システムの優れたパフォーマンスとシステム コールの完全な互換性を実現しているだけでなく、WSL 1 と同様の軽量、高速で、統合、応答性を備えています。</span><span class="sxs-lookup"><span data-stu-id="74e4f-173">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="74e4f-174">このユーティリティ VM のメモリ フットプリントは小さく、起動時に仮想アドレスでサポートされるメモリが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="74e4f-174">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="74e4f-175">これは総メモリのごく一部から始まるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="74e4f-175">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="74e4f-176">初期のプレビュー ビルドでは、OS 間のファイル速度が低下します</span><span class="sxs-lookup"><span data-stu-id="74e4f-176">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="74e4f-177">Linux アプリケーションから Windows ファイルにアクセスする場合、または Windows アプリケーションから Linux ファイルにアクセスする場合、WSL 1 と比較してファイル速度は遅いことがわかります。</span><span class="sxs-lookup"><span data-stu-id="74e4f-177">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="74e4f-178">これは WSL 2 のアーキテクチャの変更の結果であり、WSL チームはこのエクスペリエンスを改善する方法について積極的に調査しています。</span><span class="sxs-lookup"><span data-stu-id="74e4f-178">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
