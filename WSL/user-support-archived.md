---
title: 以前のバージョンの Windows での WSL ユーザーアカウントの更新
description: Windows Subsystem for Linux を使用して Linux ユーザーアカウントを更新するための、以前のバージョンの Windows のリファレンスです。
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 406158d769c4b465b6168d7cca45b48ff1f201fe
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520841"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a><span data-ttu-id="1be59-103">以前のバージョンの Windows での WSL ユーザーアカウントの更新</span><span class="sxs-lookup"><span data-stu-id="1be59-103">WSL User Account updates on Previous Windows Versions</span></span>

<span data-ttu-id="1be59-104">このコンテンツは、Linux 用サブシステムをサポートし、Linux ユーザーアカウントの更新をサポートする必要がある以前のバージョンの Windows オペレーティングシステムのユーザー向けにアーカイブされています。</span><span class="sxs-lookup"><span data-stu-id="1be59-104">This content is archived for users of earlier versions of Windows operating system that support the subsystem for Linux and need support with updating Linux user accounts.</span></span>

<span data-ttu-id="1be59-105">最新のドキュメントについては、「 [Windows Subsystem For Linux のユーザーアカウント](../user-support.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1be59-105">For current documentation, see [User Accounts for Windows Subsystem for Linux](../user-support.md).</span></span>

### <a name="for-creators-update-version-of-windows-and-earlier"></a><span data-ttu-id="1be59-106">Windows およびそれ以前のバージョンの更新プログラムの場合</span><span class="sxs-lookup"><span data-stu-id="1be59-106">For Creators Update version of Windows and earlier</span></span>

<span data-ttu-id="1be59-107">Windows 10 Creators Update 以前を実行している場合は、次のコマンドを実行して既定の Bash ユーザーを変更できます。</span><span class="sxs-lookup"><span data-stu-id="1be59-107">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="1be59-108">既定のユーザーを `root` に変更します。</span><span class="sxs-lookup"><span data-stu-id="1be59-108">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="1be59-109">`bash.exe` を実行して、今度は `root` としてログインします。</span><span class="sxs-lookup"><span data-stu-id="1be59-109">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="1be59-110">ディストリビューションのパスワード コマンドを使用してパスワードを再設定し、Linux コンソールを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1be59-110">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="1be59-111">Windows CMD で、既定のユーザーを通常の Linux ユーザー アカウントに再設定して戻します。</span><span class="sxs-lookup"><span data-stu-id="1be59-111">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="1be59-112">Fall Creators Update 以降の場合</span><span class="sxs-lookup"><span data-stu-id="1be59-112">For Fall Creators Update and later</span></span>

<span data-ttu-id="1be59-113">特定のディストリビューションで使用できるコマンドを確認するには、`[distro.exe] /?` を実行します。</span><span class="sxs-lookup"><span data-stu-id="1be59-113">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="1be59-114">たとえば、Ubuntu がインストールされているとします。</span><span class="sxs-lookup"><span data-stu-id="1be59-114">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="1be59-115">Ubuntu を使用したステップ バイ ステップの手順:</span><span class="sxs-lookup"><span data-stu-id="1be59-115">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="1be59-116">CMD を開きます。</span><span class="sxs-lookup"><span data-stu-id="1be59-116">Open CMD</span></span>
1. <span data-ttu-id="1be59-117">既定の Linux ユーザーを `root` に設定します。</span><span class="sxs-lookup"><span data-stu-id="1be59-117">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="1be59-118">Linux ディストリビューション (`ubuntu`) を起動します。</span><span class="sxs-lookup"><span data-stu-id="1be59-118">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="1be59-119">`root` として自動的にログインします。</span><span class="sxs-lookup"><span data-stu-id="1be59-119">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="1be59-120">`passwd` コマンドを使用してパスワードを再設定します。</span><span class="sxs-lookup"><span data-stu-id="1be59-120">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="1be59-121">Windows CMD で、既定のユーザーを通常の Linux ユーザー アカウントに再設定して戻します。</span><span class="sxs-lookup"><span data-stu-id="1be59-121">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```
