---
title: ファイルのアクセス許可
description: WSL による Windows でのファイルアクセス許可の決定方法について
keywords: BashOnWindows、bash、wsl、wsl2、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10、file、permissions
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520861"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="c1359-104">WSL のファイルアクセス許可</span><span class="sxs-lookup"><span data-stu-id="c1359-104">File Permissions for WSL</span></span>

<span data-ttu-id="c1359-105">このページでは、linux ファイルのアクセス許可が Windows Subsystem for Linux でどのように解釈されるかについて詳しく説明します。これは特に NT ファイルシステムの Windows 内のリソースにアクセスする場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c1359-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="c1359-106">このドキュメントでは、 [Linux ファイルシステムの権限の構造](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)に関する基本的な知識があることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c1359-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span></span> <!--TODO: Double check that it's okay to add these links--> <span data-ttu-id="c1359-107">また、 [umask コマンド](https://en.wikipedia.org/wiki/Umask)を実行します。</span><span class="sxs-lookup"><span data-stu-id="c1359-107">and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="c1359-108">WSL から Windows ファイルにアクセスする場合、ファイルのアクセス許可は Windows のアクセス許可から計算されるか、WSL によってファイルに追加されたメタデータから読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="c1359-108">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="c1359-109">このメタデータは、既定では有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="c1359-109">This metadata is not enabled by default.</span></span> 

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="c1359-110">Windows ファイルの WSL メタデータ</span><span class="sxs-lookup"><span data-stu-id="c1359-110">WSL metadata on Windows files</span></span>

<span data-ttu-id="c1359-111">WSL でマウントオプションとしてメタデータを有効にすると、Windows NT ファイルの拡張属性を追加して解釈し、Linux ファイルシステムのアクセス許可を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="c1359-111">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span> 

<span data-ttu-id="c1359-112">WSL では、次の4つの NTFS 拡張属性を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c1359-112">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="c1359-113">属性名</span><span class="sxs-lookup"><span data-stu-id="c1359-113">Attribute Name</span></span> | <span data-ttu-id="c1359-114">説明</span><span class="sxs-lookup"><span data-stu-id="c1359-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="c1359-115">$LXUID</span><span class="sxs-lookup"><span data-stu-id="c1359-115">$LXUID</span></span> | <span data-ttu-id="c1359-116">ユーザー所有者 ID</span><span class="sxs-lookup"><span data-stu-id="c1359-116">User Owner ID</span></span> |
| <span data-ttu-id="c1359-117">$LXGID</span><span class="sxs-lookup"><span data-stu-id="c1359-117">$LXGID</span></span> | <span data-ttu-id="c1359-118">グループ所有者 ID</span><span class="sxs-lookup"><span data-stu-id="c1359-118">Group Owner ID</span></span> |
| <span data-ttu-id="c1359-119">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="c1359-119">$LXMOD</span></span> | <span data-ttu-id="c1359-120">ファイルモード (ファイルシステムのアクセス許可の octals と種類。例: 0777)</span><span class="sxs-lookup"><span data-stu-id="c1359-120">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="c1359-121">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="c1359-121">$LXDEV</span></span> | <span data-ttu-id="c1359-122">デバイス (デバイスファイルの場合)</span><span class="sxs-lookup"><span data-stu-id="c1359-122">Device, if it is a device file</span></span> |

<span data-ttu-id="c1359-123">また、通常のファイルまたはディレクトリではないファイル (例: symlink、Fifo、ブロックデバイス、unix ソケット、文字デバイス) には、NTFS[再解析ポイント](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)もあります。</span><span class="sxs-lookup"><span data-stu-id="c1359-123">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="c1359-124">これにより、拡張属性に対してクエリを実行しなくても、特定のディレクトリ内のファイルの種類をより速く特定できます。</span><span class="sxs-lookup"><span data-stu-id="c1359-124">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span> 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a><span data-ttu-id="c1359-125">ファイルアクセスのシナリオ</span><span class="sxs-lookup"><span data-stu-id="c1359-125">File Access Scenarios</span></span>

<span data-ttu-id="c1359-126">Windows Subsystem for Linux を使用してさまざまな方法でファイルにアクセスする場合のアクセス許可の決定方法について、以下に説明します。</span><span class="sxs-lookup"><span data-stu-id="c1359-126">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="c1359-127">Linux から Windows ドライブファイルシステム (DrvFS) のファイルにアクセスする</span><span class="sxs-lookup"><span data-stu-id="c1359-127">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="c1359-128">これらのシナリオは、WSL から Windows ファイルにアクセスする場合に発生します。ほとんどの場合 `/mnt/c`経由でアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c1359-128">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span> 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="c1359-129">既存の Windows ファイルからのファイルのアクセス許可の読み取り</span><span class="sxs-lookup"><span data-stu-id="c1359-129">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="c1359-130">この結果は、ファイルに既にメタデータが存在するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c1359-130">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="c1359-131">**ファイルにメタデータがありません (既定)。**</span><span class="sxs-lookup"><span data-stu-id="c1359-131">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="c1359-132">ファイルにメタデータが関連付けられていない場合は、Windows ユーザーの有効なアクセス許可を読み取り/書き込み/実行ビットに変換し、ユーザー、グループ、およびその他の同じ値として設定します。</span><span class="sxs-lookup"><span data-stu-id="c1359-132">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="c1359-133">たとえば、Windows ユーザーアカウントに読み取りと実行のアクセス権があり、ファイルへの書き込みアクセスが許可されていない場合は、ユーザー、グループ、およびその他の `r-x` として表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1359-133">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="c1359-134">ファイルに Windows で ' 読み取り専用 ' 属性が設定されている場合、Linux では書き込みアクセス権は付与されません。</span><span class="sxs-lookup"><span data-stu-id="c1359-134">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="c1359-135">ファイルにメタデータが含まれています</span><span class="sxs-lookup"><span data-stu-id="c1359-135">The file has metadata</span></span>

<span data-ttu-id="c1359-136">ファイルにメタデータが含まれている場合は、Windows ユーザーの有効なアクセス許可を変換する代わりに、これらのメタデータ値を使用するだけです。</span><span class="sxs-lookup"><span data-stu-id="c1359-136">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="c1359-137">Chmod を使用して既存の Windows ファイルのファイルアクセス許可を変更する</span><span class="sxs-lookup"><span data-stu-id="c1359-137">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="c1359-138">この結果は、ファイルに既にメタデータが存在するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c1359-138">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="c1359-139">**ファイルにメタデータがありません (既定)。**</span><span class="sxs-lookup"><span data-stu-id="c1359-139">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="c1359-140">Chmod の効果は1つだけです。ファイルのすべての書き込み属性を削除すると、Windows ファイルの ' 読み取り専用 ' 属性が設定されます。これは、Linux の SMB (サーバーメッセージブロック) クライアントである CIFS (Common Internet File System) と同じ動作であるためです。</span><span class="sxs-lookup"><span data-stu-id="c1359-140">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="c1359-141">ファイルにメタデータが含まれています</span><span class="sxs-lookup"><span data-stu-id="c1359-141">The file has metadata</span></span>

<span data-ttu-id="c1359-142">Chmod は、ファイルの既存のメタデータに応じて、メタデータを変更または追加します。</span><span class="sxs-lookup"><span data-stu-id="c1359-142">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="c1359-143">Windows の場合よりもアクセス権を追加することはできないことに注意してください。メタデータでは、そのような場合でも同様です。</span><span class="sxs-lookup"><span data-stu-id="c1359-143">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="c1359-144">たとえば、`chmod 777`を使用してファイルに対する書き込みアクセス許可があることを示すメタデータを設定できますが、そのファイルにアクセスしようとした場合でも、そのファイルに書き込むことはできません。</span><span class="sxs-lookup"><span data-stu-id="c1359-144">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="c1359-145">Windows ファイルに対するすべての読み取りまたは書き込みコマンドが Windows ユーザーのアクセス許可を通じてルーティングされるため、interopability に感謝します。</span><span class="sxs-lookup"><span data-stu-id="c1359-145">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="c1359-146">ドライブ Fs でのファイルの作成</span><span class="sxs-lookup"><span data-stu-id="c1359-146">Creating a file in DriveFS</span></span>

<span data-ttu-id="c1359-147">結果は、メタデータが有効になっているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c1359-147">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="c1359-148">メタデータが有効になっていません (既定)</span><span class="sxs-lookup"><span data-stu-id="c1359-148">Metadata is not enabled (default)</span></span>

<span data-ttu-id="c1359-149">新しく作成されたファイルの Windows アクセス許可は、特定のセキュリティ記述子を使用せずに Windows でファイルを作成した場合と同じになります。これは、親のアクセス許可を継承します。</span><span class="sxs-lookup"><span data-stu-id="c1359-149">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span> 

##### <a name="metadata-is-enabled"></a><span data-ttu-id="c1359-150">メタデータが有効</span><span class="sxs-lookup"><span data-stu-id="c1359-150">Metadata is enabled</span></span>

<span data-ttu-id="c1359-151">ファイルのアクセス許可ビットは、Linux umask に従うように設定され、ファイルはメタデータと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="c1359-151">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="c1359-152">どの Linux ユーザーおよび Linux グループがファイルを所有していますか。</span><span class="sxs-lookup"><span data-stu-id="c1359-152">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="c1359-153">この結果は、ファイルに既にメタデータが存在するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c1359-153">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="c1359-154">**ファイルにメタデータがありません (既定)。**</span><span class="sxs-lookup"><span data-stu-id="c1359-154">**The file does not have metadata (default)**</span></span>
<span data-ttu-id="c1359-155">既定のシナリオでは、Windows ドライブを automounting するときに、任意のファイルのユーザー ID (UID) が WSL ユーザーのユーザー ID に設定され、グループ ID (GID) が WSL ユーザーのプリンシパルグループ ID に設定されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="c1359-155">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span> 

##### <a name="the-file-has-metadata"></a><span data-ttu-id="c1359-156">ファイルにメタデータが含まれています</span><span class="sxs-lookup"><span data-stu-id="c1359-156">The file has metadata</span></span>

<span data-ttu-id="c1359-157">メタデータに指定されている UID および GID は、ファイルのユーザー所有者とグループ所有者として適用されます。</span><span class="sxs-lookup"><span data-stu-id="c1359-157">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span> 

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="c1359-158">`\\wsl$` を使用した Windows からの Linux ファイルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="c1359-158">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="c1359-159">`\\wsl$` 経由で Linux ファイルにアクセスする場合は、WSL ディストリビューションの既定のユーザーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c1359-159">Accessing Linux files via `\\wsl$` will use the default user of your WSL distro.</span></span> <span data-ttu-id="c1359-160">そのため、Linux ファイルにアクセスするすべての Windows アプリは、既定のユーザーと同じアクセス許可を持ちます。</span><span class="sxs-lookup"><span data-stu-id="c1359-160">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="c1359-161">新しいファイルの作成</span><span class="sxs-lookup"><span data-stu-id="c1359-161">Creating a new file</span></span>

<span data-ttu-id="c1359-162">既定の umask は、Windows から WSL ディストリビューション内に新しいファイルを作成するときに適用されます。</span><span class="sxs-lookup"><span data-stu-id="c1359-162">The default umask is applied when creating a new file inside of a WSL distro from Windows.</span></span> <span data-ttu-id="c1359-163">既定の umask は `022`であるか、またはグループと他のユーザーに対する書き込み権限以外のすべての権限を許可することを意味します。</span><span class="sxs-lookup"><span data-stu-id="c1359-163">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="c1359-164">Linux から Linux ルートファイルシステムのファイルにアクセスする</span><span class="sxs-lookup"><span data-stu-id="c1359-164">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="c1359-165">Linux ルートファイルシステムで作成、変更、またはアクセスされるすべてのファイルは、新しく作成されたファイルに umask を適用するなど、標準的な Linux 規則に従います。</span><span class="sxs-lookup"><span data-stu-id="c1359-165">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="c1359-166">ファイルのアクセス許可の構成</span><span class="sxs-lookup"><span data-stu-id="c1359-166">Configuring file permissions</span></span>

<span data-ttu-id="c1359-167">Wsl のマウントオプションを使用して、Windows ドライブ内でファイルのアクセス許可を構成できます。</span><span class="sxs-lookup"><span data-stu-id="c1359-167">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="c1359-168">マウントオプションを使用すると、`umask`、`dmask`、および `fmask` のアクセス許可マスクを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c1359-168">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="c1359-169">`umask` がすべてのファイルに適用されます。 `dmask` はディレクトリだけに適用され、`fmask` はファイルにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="c1359-169">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="c1359-170">これらのアクセス許可マスクは、ファイルに適用されるときに論理 OR 演算によって設定されます。たとえば、`umask` の値が `023` で `fmask` 値が `022` の場合、ファイルの結果として得られるアクセス許可マスクは `023`されます。</span><span class="sxs-lookup"><span data-stu-id="c1359-170">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span> 

<span data-ttu-id="c1359-171">これを行う方法については、「 [Linux ディストリビューションの管理」](./wsl-config.md)ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1359-171">Please see the ['Manage Linux Distributions'](./wsl-config.md) document page for instructions on how to do this.</span></span>
<!-- TODO: Add # to the link-->

