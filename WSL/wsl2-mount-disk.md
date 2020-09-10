---
title: WSL 2 (プレビュー) で linux ディスクのマウントを開始する
description: WSL 2 でディスクマウントを設定する方法と、そのアクセス方法について説明します。
keywords: wsl、windows、windowssubsystem、gnu、linux、bash、disk、ext4、filesystem、mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 8053b817dab0639789401e2fcfb116f6f8e722a7
ms.sourcegitcommit: a949595f3947c733f0bcdc54b30ccda5ae61577c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/10/2020
ms.locfileid: "89671205"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a><span data-ttu-id="6c1a2-104">WSL 2 (プレビュー) で linux ディスクのマウントを開始する</span><span class="sxs-lookup"><span data-stu-id="6c1a2-104">Get started mounting a linux disk in WSL 2 (preview)</span></span>

<span data-ttu-id="6c1a2-105">Windows でサポートされていない Linux ディスクフォーマットにアクセスする場合は、WSL 2 を使用してディスクをマウントし、そのコンテンツにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-105">If you want to access a Linux disk format that isn't supported by Windows, you can use WSL 2 to mount your disk and access its content.</span></span>

<span data-ttu-id="6c1a2-106">このチュートリアルでは、WSL2 にアタッチするディスクとパーティションを識別する手順、それらをマウントする方法、およびそれらへのアクセス方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-106">This tutorial will cover the steps to identify the disk and partition to attach to WSL2, how to mount them, and how to access them.</span></span>

> [!NOTE]
> <span data-ttu-id="6c1a2-107">WSL 2 にディスクを接続するには、管理者アクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-107">Administrator access is required to attach a disk to WSL 2.</span></span>

## <a name="identify-the-disk"></a><span data-ttu-id="6c1a2-108">ディスクを識別する</span><span class="sxs-lookup"><span data-stu-id="6c1a2-108">Identify the disk</span></span>

<span data-ttu-id="6c1a2-109">Windows で使用可能なディスクを一覧表示するには、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-109">To list the available disks in Windows, run:</span></span>

```powershell
wmic diskdrive list brief
```

<span data-ttu-id="6c1a2-110">ディスクパスは、' DeviceID ' 列で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-110">The disks paths are available under the 'DeviceID' columns.</span></span> <span data-ttu-id="6c1a2-111">通常、の `\\.\PHYSICALDRIVE*` 形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-111">Usually under the `\\.\PHYSICALDRIVE*` format.</span></span>

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a><span data-ttu-id="6c1a2-112">WSL 2 でマウントするパーティションを一覧表示して選択します</span><span class="sxs-lookup"><span data-stu-id="6c1a2-112">List and select the partitions to mount in WSL 2</span></span>

<span data-ttu-id="6c1a2-113">ディスクが識別されたら、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-113">Once the disk is identified, run:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="6c1a2-114">これにより、WSL 2 でディスクを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-114">This will make the disk available in WSL 2.</span></span>

<span data-ttu-id="6c1a2-115">アタッチされたら、WSL 2 内で次のコマンドを実行してパーティションを一覧表示できます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-115">Once attached, the partition can be listed by running the following command inside WSL 2:</span></span>

```powershell
lsblk
```

<span data-ttu-id="6c1a2-116">これにより、使用可能なブロックデバイスとそのパーティションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-116">This will display the available block devices and their partitions.</span></span>

<span data-ttu-id="6c1a2-117">Linux 内部では、ブロックデバイスはとして識別され  `/dev/<Device><Partition>` ます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-117">Inside Linux, a block device is identified as  `/dev/<Device><Partition>`.</span></span> <span data-ttu-id="6c1a2-118">たとえば、次のように指定します。は、ディスクのパーティション番号3です `sdb` 。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-118">For example, /dev/sdb3, is the partition number 3 of disk `sdb`.</span></span>

<span data-ttu-id="6c1a2-119">出力例:</span><span class="sxs-lookup"><span data-stu-id="6c1a2-119">Example output:</span></span>

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a><span data-ttu-id="6c1a2-120">ファイルシステムの種類の識別</span><span class="sxs-lookup"><span data-stu-id="6c1a2-120">Identifying the filesystem type</span></span>

<span data-ttu-id="6c1a2-121">ディスクまたはパーティションのファイルシステムの種類がわからない場合は、次のコマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-121">If you don't know the type of filesystem of a disk or partition, you can use this command:</span></span>

```powershell
blkid <BlockDevice>
```

<span data-ttu-id="6c1a2-122">これにより、検出されたファイルシステムの種類 (形式の下) が出力され `TYPE="<Filesystem>"` ます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-122">This will output the detected filesystem type (under the `TYPE="<Filesystem>"` format).</span></span>

## <a name="mount-the-selected-partitions"></a><span data-ttu-id="6c1a2-123">選択したパーティションをマウントします</span><span class="sxs-lookup"><span data-stu-id="6c1a2-123">Mount the selected partitions</span></span>

<span data-ttu-id="6c1a2-124">マウントするパーティションを特定したら、各パーティションで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-124">Once you have identified the partitions you want to mount, run this command on each partition:</span></span> 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> <span data-ttu-id="6c1a2-125">ディスク全体を1つのボリュームとしてマウントする場合 (つまり、ディスクがパーティション分割されていない場合) は、を `--partition` 省略できます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-125">If you wish to mount the entire disk as a single volume (i.e. if the disk isn't partitioned), `--partition` can be omitted.</span></span>
> 
> <span data-ttu-id="6c1a2-126">省略した場合、既定のファイルシステムの種類は "ext4" になります。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-126">If omitted, the default filesystem type is "ext4".</span></span>

## <a name="access-the-disk-content"></a><span data-ttu-id="6c1a2-127">ディスクコンテンツにアクセスする</span><span class="sxs-lookup"><span data-stu-id="6c1a2-127">Access the disk content</span></span>

<span data-ttu-id="6c1a2-128">マウントされると、構成値が指すパスでディスクにアクセスできるように `automount.root` なります。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-128">Once mounted, the disk can be accessed under the path pointed to by the config value: `automount.root`.</span></span> <span data-ttu-id="6c1a2-129">既定値は `/mnt/wsl` です。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-129">The default value is `/mnt/wsl`.</span></span>

<span data-ttu-id="6c1a2-130">Windows では、ファイルエクスプローラーから: `\\wsl$\\<Distro>\\<Mountpoint>` (任意の Linux ディストリビューションを選択) に移動して、ディスクにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-130">From Windows, the disk can be accessed from File Explorer by navigating to: `\\wsl$\\<Distro>\\<Mountpoint>` (pick any Linux distribution).</span></span>

## <a name="unmount-the-disk"></a><span data-ttu-id="6c1a2-131">ディスクのマウント解除</span><span class="sxs-lookup"><span data-stu-id="6c1a2-131">Unmount the disk</span></span>

<span data-ttu-id="6c1a2-132">WSL 2 からディスクのマウントを解除して切断する場合は、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-132">If you want to unmount and detach the disk from WSL 2, run:</span></span>

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a><span data-ttu-id="6c1a2-133">コマンド ライン リファレンス</span><span class="sxs-lookup"><span data-stu-id="6c1a2-133">Command line reference</span></span>

### <a name="mouting-a-specific-filesystem"></a><span data-ttu-id="6c1a2-134">特定のファイルシステムの場合</span><span class="sxs-lookup"><span data-stu-id="6c1a2-134">Mouting a specific filesystem</span></span>

<span data-ttu-id="6c1a2-135">既定では、WSL 2 は ext4 としてデバイスをマウントしようとします。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-135">By default, WSL 2 will attempt to mount the device as ext4.</span></span> <span data-ttu-id="6c1a2-136">別のファイルシステムを指定するには、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-136">To specify another filesystem, run:</span></span>

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

<span data-ttu-id="6c1a2-137">たとえば、ディスクを fat としてマウントするには、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-137">For example, to mount a disk as fat, run:</span></span>

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> <span data-ttu-id="6c1a2-138">WSL2 で使用可能なファイルシステムを一覧表示するには、次のように実行します。 `cat /proc/filesystems`</span><span class="sxs-lookup"><span data-stu-id="6c1a2-138">To list the available filesystems in WSL2, run: `cat /proc/filesystems`</span></span>

### <a name="mouting-a-specific-partition"></a><span data-ttu-id="6c1a2-139">特定のパーティションを指定する</span><span class="sxs-lookup"><span data-stu-id="6c1a2-139">Mouting a specific partition</span></span>

<span data-ttu-id="6c1a2-140">既定では、WSL 2 はディスク全体をマウントしようとします。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-140">By default, WSL 2 attempts to mount the entire disk.</span></span> <span data-ttu-id="6c1a2-141">特定のパーティションをマウントするには、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-141">To mount a specific partition, run:</span></span>

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

<span data-ttu-id="6c1a2-142">これは、ディスクが MBR (マスターブートレコード) または GPT (GUID パーティションテーブル) のいずれかである場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-142">This only works if the disk is either MBR (Master Boot Record) or GPT (GUID Partition Table).</span></span> <span data-ttu-id="6c1a2-143">[パーティションスタイルについては、「MBR と GPT](https://docs.microsoft.com/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-143">[Read about partition styles - MBR and GPT](https://docs.microsoft.com/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span></span>

### <a name="specifying-mount-options"></a><span data-ttu-id="6c1a2-144">マウントオプションの指定</span><span class="sxs-lookup"><span data-stu-id="6c1a2-144">Specifying mount options</span></span>

<span data-ttu-id="6c1a2-145">マウントオプションを指定するには、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-145">To specify mount options, run:</span></span>

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

<span data-ttu-id="6c1a2-146">例:</span><span class="sxs-lookup"><span data-stu-id="6c1a2-146">Example:</span></span>

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> <span data-ttu-id="6c1a2-147">現時点では、ファイルシステム固有のオプションのみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-147">Only filesystem specific options are supported at this time.</span></span> <span data-ttu-id="6c1a2-148">などの汎用オプション `ro, rw, noatime, ...` はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-148">Generic options such as `ro, rw, noatime, ...` are not supported.</span></span>

### <a name="attaching-the-disk-without-mounting-it"></a><span data-ttu-id="6c1a2-149">マウントせずにディスクを接続する</span><span class="sxs-lookup"><span data-stu-id="6c1a2-149">Attaching the disk without mounting it</span></span>

<span data-ttu-id="6c1a2-150">ディスク構成が上記のいずれのオプションでもサポートされていない場合は、を実行してディスクをマウントせずに WSL 2 に接続できます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-150">If the disk scheme isn't supported by any of the above options, you can attach the disk to WSL 2 without mounting it by running:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="6c1a2-151">これにより、ブロックデバイスは WSL 2 内で使用できるようになり、そこから手動でマウントすることができます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-151">This will make the block device available inside WSL 2 so it can be mounted manually from there.</span></span> <span data-ttu-id="6c1a2-152">`lsblk`WSL 2 内で利用可能なブロックデバイスを一覧表示するには、を使用します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-152">Use `lsblk` to list the available block devices inside WSL 2.</span></span>

### <a name="detaching-a-disk"></a><span data-ttu-id="6c1a2-153">ディスクのデタッチ</span><span class="sxs-lookup"><span data-stu-id="6c1a2-153">Detaching a disk</span></span>

<span data-ttu-id="6c1a2-154">WSL 2 からディスクを切断するには、次のように実行します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-154">To detach a disk from WSL 2, run:</span></span>

```powershell
wsl --unmount [DiskPath]
```

<span data-ttu-id="6c1a2-155">`Diskpath`を省略すると、接続されているすべてのディスクがマウント解除され、デタッチされます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-155">If `Diskpath` is omitted, all attached disks are unmounted and detached.</span></span>

> [!NOTE]
> <span data-ttu-id="6c1a2-156">1つのディスクのマウント解除に失敗した場合は、を実行して WSL 2 を強制的に終了させることができ `wsl --shutdown` ます。これにより、ディスクが切断されます。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-156">If one disk fails to unmount, WSL 2 can be forced to exit by running `wsl --shutdown`, which will detach the disk.</span></span>

## <a name="limitations"></a><span data-ttu-id="6c1a2-157">制限事項</span><span class="sxs-lookup"><span data-stu-id="6c1a2-157">Limitations</span></span>

- <span data-ttu-id="6c1a2-158">現時点では、ディスク全体のみを WSL 2 に接続できます。つまり、パーティションのみをアタッチすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-158">At this time, only entire disks can be attached to WSL 2, meaning that it's not possible to attach only a partition.</span></span> <span data-ttu-id="6c1a2-159">具体的にでは、このデバイスは Windows からデタッチできないため、を使用して `wsl --mount` ブートデバイスのパーティションを読み取ることはできません。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-159">Concretely, this means that it's not possible to use `wsl --mount` to read a partition on the boot device, because that device can't be detached from Windows.</span></span>

- <span data-ttu-id="6c1a2-160">USB フラッシュドライブは現時点ではサポートされていないため、WSL 2 へのアタッチに失敗します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-160">USB flash drives are not supported at this time and will fail to attach to WSL 2.</span></span> <span data-ttu-id="6c1a2-161">ただし、USB ディスクはサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-161">USB disks are supported though.</span></span>

- <span data-ttu-id="6c1a2-162">によってマウントできるのは、カーネルでネイティブでサポートされているファイルシステムだけ `wsl --mount` です。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-162">Only filesystems that are natively supported in the kernel can be mounted by `wsl --mount`.</span></span> <span data-ttu-id="6c1a2-163">これは、を呼び出すことによって、インストールされているファイルシステムドライバー (たとえば、ntfs 3g など) を使用できないことを意味 `wsl --mount` します。</span><span class="sxs-lookup"><span data-stu-id="6c1a2-163">This means that it's not possible to use installed filesystem drivers (such as ntfs-3g for example) by calling `wsl --mount`.</span></span>
