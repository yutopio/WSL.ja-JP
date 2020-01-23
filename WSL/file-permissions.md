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
# <a name="file-permissions-for-wsl"></a>WSL のファイルアクセス許可

このページでは、linux ファイルのアクセス許可が Windows Subsystem for Linux でどのように解釈されるかについて詳しく説明します。これは特に NT ファイルシステムの Windows 内のリソースにアクセスする場合に役立ちます。 このドキュメントでは、 [Linux ファイルシステムの権限の構造](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)に関する基本的な知識があることを前提としています。 <!--TODO: Double check that it's okay to add these links--> また、 [umask コマンド](https://en.wikipedia.org/wiki/Umask)を実行します。

WSL から Windows ファイルにアクセスする場合、ファイルのアクセス許可は Windows のアクセス許可から計算されるか、WSL によってファイルに追加されたメタデータから読み込まれます。 このメタデータは、既定では有効になっていません。 

## <a name="wsl-metadata-on-windows-files"></a>Windows ファイルの WSL メタデータ

WSL でマウントオプションとしてメタデータを有効にすると、Windows NT ファイルの拡張属性を追加して解釈し、Linux ファイルシステムのアクセス許可を与えることができます。 

WSL では、次の4つの NTFS 拡張属性を追加できます。

| 属性名 | 説明 |
| --- | --- |
| $LXUID | ユーザー所有者 ID |
| $LXGID | グループ所有者 ID |
| $LXMOD | ファイルモード (ファイルシステムのアクセス許可の octals と種類。例: 0777) |
| $LXDEV | デバイス (デバイスファイルの場合) |

また、通常のファイルまたはディレクトリではないファイル (例: symlink、Fifo、ブロックデバイス、unix ソケット、文字デバイス) には、NTFS[再解析ポイント](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)もあります。 これにより、拡張属性に対してクエリを実行しなくても、特定のディレクトリ内のファイルの種類をより速く特定できます。 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a>ファイルアクセスのシナリオ

Windows Subsystem for Linux を使用してさまざまな方法でファイルにアクセスする場合のアクセス許可の決定方法について、以下に説明します。

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Linux から Windows ドライブファイルシステム (DrvFS) のファイルにアクセスする

これらのシナリオは、WSL から Windows ファイルにアクセスする場合に発生します。ほとんどの場合 `/mnt/c`経由でアクセスします。 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>既存の Windows ファイルからのファイルのアクセス許可の読み取り

この結果は、ファイルに既にメタデータが存在するかどうかによって異なります。

##### <a name="the-file-does-not-have-metadata-default"></a>**ファイルにメタデータがありません (既定)。**

ファイルにメタデータが関連付けられていない場合は、Windows ユーザーの有効なアクセス許可を読み取り/書き込み/実行ビットに変換し、ユーザー、グループ、およびその他の同じ値として設定します。 たとえば、Windows ユーザーアカウントに読み取りと実行のアクセス権があり、ファイルへの書き込みアクセスが許可されていない場合は、ユーザー、グループ、およびその他の `r-x` として表示されます。 ファイルに Windows で ' 読み取り専用 ' 属性が設定されている場合、Linux では書き込みアクセス権は付与されません。

##### <a name="the-file-has-metadata"></a>ファイルにメタデータが含まれています

ファイルにメタデータが含まれている場合は、Windows ユーザーの有効なアクセス許可を変換する代わりに、これらのメタデータ値を使用するだけです。

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Chmod を使用して既存の Windows ファイルのファイルアクセス許可を変更する

この結果は、ファイルに既にメタデータが存在するかどうかによって異なります。

##### <a name="the-file-does-not-have-metadata-default"></a>**ファイルにメタデータがありません (既定)。**

Chmod の効果は1つだけです。ファイルのすべての書き込み属性を削除すると、Windows ファイルの ' 読み取り専用 ' 属性が設定されます。これは、Linux の SMB (サーバーメッセージブロック) クライアントである CIFS (Common Internet File System) と同じ動作であるためです。

##### <a name="the-file-has-metadata"></a>ファイルにメタデータが含まれています

Chmod は、ファイルの既存のメタデータに応じて、メタデータを変更または追加します。 

Windows の場合よりもアクセス権を追加することはできないことに注意してください。メタデータでは、そのような場合でも同様です。 たとえば、`chmod 777`を使用してファイルに対する書き込みアクセス許可があることを示すメタデータを設定できますが、そのファイルにアクセスしようとした場合でも、そのファイルに書き込むことはできません。 Windows ファイルに対するすべての読み取りまたは書き込みコマンドが Windows ユーザーのアクセス許可を通じてルーティングされるため、interopability に感謝します。

#### <a name="creating-a-file-in-drivefs"></a>ドライブ Fs でのファイルの作成

結果は、メタデータが有効になっているかどうかによって異なります。

##### <a name="metadata-is-not-enabled-default"></a>メタデータが有効になっていません (既定)

新しく作成されたファイルの Windows アクセス許可は、特定のセキュリティ記述子を使用せずに Windows でファイルを作成した場合と同じになります。これは、親のアクセス許可を継承します。 

##### <a name="metadata-is-enabled"></a>メタデータが有効

ファイルのアクセス許可ビットは、Linux umask に従うように設定され、ファイルはメタデータと共に保存されます。

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>どの Linux ユーザーおよび Linux グループがファイルを所有していますか。 

この結果は、ファイルに既にメタデータが存在するかどうかによって異なります。

##### <a name="the-file-does-not-have-metadata-default"></a>**ファイルにメタデータがありません (既定)。**
既定のシナリオでは、Windows ドライブを automounting するときに、任意のファイルのユーザー ID (UID) が WSL ユーザーのユーザー ID に設定され、グループ ID (GID) が WSL ユーザーのプリンシパルグループ ID に設定されることを指定します。 

##### <a name="the-file-has-metadata"></a>ファイルにメタデータが含まれています

メタデータに指定されている UID および GID は、ファイルのユーザー所有者とグループ所有者として適用されます。 

### <a name="accessing-linux-files-from-windows-using-wsl"></a>`\\wsl$` を使用した Windows からの Linux ファイルへのアクセス

`\\wsl$` 経由で Linux ファイルにアクセスする場合は、WSL ディストリビューションの既定のユーザーが使用されます。 そのため、Linux ファイルにアクセスするすべての Windows アプリは、既定のユーザーと同じアクセス許可を持ちます。

#### <a name="creating-a-new-file"></a>新しいファイルの作成

既定の umask は、Windows から WSL ディストリビューション内に新しいファイルを作成するときに適用されます。 既定の umask は `022`であるか、またはグループと他のユーザーに対する書き込み権限以外のすべての権限を許可することを意味します。 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Linux から Linux ルートファイルシステムのファイルにアクセスする

Linux ルートファイルシステムで作成、変更、またはアクセスされるすべてのファイルは、新しく作成されたファイルに umask を適用するなど、標準的な Linux 規則に従います。

## <a name="configuring-file-permissions"></a>ファイルのアクセス許可の構成

Wsl のマウントオプションを使用して、Windows ドライブ内でファイルのアクセス許可を構成できます。 マウントオプションを使用すると、`umask`、`dmask`、および `fmask` のアクセス許可マスクを設定できます。 `umask` がすべてのファイルに適用されます。 `dmask` はディレクトリだけに適用され、`fmask` はファイルにのみ適用されます。 これらのアクセス許可マスクは、ファイルに適用されるときに論理 OR 演算によって設定されます。たとえば、`umask` の値が `023` で `fmask` 値が `022` の場合、ファイルの結果として得られるアクセス許可マスクは `023`されます。 

これを行う方法については、「 [Linux ディストリビューションの管理」](./wsl-config.md)ドキュメントを参照してください。
<!-- TODO: Add # to the link-->

