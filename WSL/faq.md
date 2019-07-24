---
title: よく寄せられる質問 (FAQ)
description: Windows Subsystem for Linux に関してよく寄せられる質問。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 2bbcec661146fcb570209fd895e6543657e98996
ms.sourcegitcommit: 939fe561d178454219adbee96c0ad3f768db2208
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2019
ms.locfileid: "67237391"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="60c46-104">Windows Subsystem for Linux に関してよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="60c46-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="60c46-105">Windows Subsystem for Linux (WSL) とは</span><span class="sxs-lookup"><span data-stu-id="60c46-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="60c46-106">Windows Subsystem for Linux (WSL) は、windows 10 の新しい機能であり、従来の Windows デスクトップや最新のストアアプリと並行して、ネイティブの Linux コマンドラインツールを Windows で直接実行できます。</span><span class="sxs-lookup"><span data-stu-id="60c46-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="60c46-107">詳細については、[[バージョン情報] ページ](./about.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60c46-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="60c46-108">WSL の対象ユーザー</span><span class="sxs-lookup"><span data-stu-id="60c46-108">Who is WSL for?</span></span>
<span data-ttu-id="60c46-109">これは、主に開発者向けのツールであり、特に web 開発者と、オープンソースプロジェクトで作業している開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="60c46-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="60c46-110">これにより、Bash、一般的な linux ツール (`sed`、 `awk`など) と多くの linux ファーストツール (Ruby、Python など) を使用する必要があるユーザーは、Windows でそのツールチェーンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="60c46-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="60c46-111">WSL でできること</span><span class="sxs-lookup"><span data-stu-id="60c46-111">What can I do with WSL?</span></span>
<span data-ttu-id="60c46-112">WSL は、Bash という名前のアプリケーションを提供します。このアプリケーションを開始すると、Bash シェルを実行している Windows コンソールが開きます。</span><span class="sxs-lookup"><span data-stu-id="60c46-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="60c46-113">Bash を使用すると、コマンドラインの Linux ツールとアプリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="60c46-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="60c46-114">たとえば、「」 `lsb_release -a`と入力して enter キーを押すと、現在実行中の Linux ディストリビューションの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="60c46-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![ディストリビューションの詳細のスクリーンショット](media/distro.png)

<span data-ttu-id="60c46-116">Linux Bash シェル内からローカルコンピューターのファイルシステムにアクセスすることもできます。ローカルドライブはフォルダーの`/mnt`下にマウントされています。</span><span class="sxs-lookup"><span data-stu-id="60c46-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="60c46-117">たとえば、 `C:`ドライブは`/mnt/c`次のようにマウントされます。</span><span class="sxs-lookup"><span data-stu-id="60c46-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![マウントされた C ドライブのスクリーンショット](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="60c46-119">Bash とは</span><span class="sxs-lookup"><span data-stu-id="60c46-119">What is Bash?</span></span>
<span data-ttu-id="60c46-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)は、広く使われているテキストベースのシェルとコマンド言語です。</span><span class="sxs-lookup"><span data-stu-id="60c46-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="60c46-121">これは、Ubuntu とその他の Linux ディストリビューション、および macOS に含まれる既定のシェルです。</span><span class="sxs-lookup"><span data-stu-id="60c46-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="60c46-122">ユーザーは、シェルにコマンドを入力してスクリプトを実行したり、コマンドやツールを実行したりして、多くのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="60c46-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="60c46-123">この処理のしくみ</span><span class="sxs-lookup"><span data-stu-id="60c46-123">How does this work?</span></span>
<span data-ttu-id="60c46-124">基になるテクノロジの詳細については、こちらの[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60c46-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="60c46-125">VM で Linux ではなく WSL を使用するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="60c46-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="60c46-126">WSL が必要とするリソース (CPU、メモリ、およびストレージ) は、完全な仮想マシンよりも少なくなります。</span><span class="sxs-lookup"><span data-stu-id="60c46-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="60c46-127">また、WSL を使用すると、Linux のコマンドラインツールとアプリを Windows コマンドライン、デスクトップアプリ、ストアアプリと共に実行し、Linux 内から Windows ファイルにアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="60c46-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="60c46-128">これにより、必要に応じて、同じファイルセットで Windows アプリと Linux コマンドラインツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="60c46-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="60c46-129">たとえば、Windows ではなく Linux で Ruby を使用するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="60c46-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="60c46-130">一部のクロスプラットフォームツールは、それらが実行される環境が Linux のように動作することを前提として構築されました。</span><span class="sxs-lookup"><span data-stu-id="60c46-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="60c46-131">たとえば、一部のツールでは、非常に長いファイルパスにアクセスできること、または特定のファイルやフォルダーが存在することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="60c46-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="60c46-132">多くの場合、Linux とは動作が異なる Windows で問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="60c46-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="60c46-133">多くの場合、Ruby や node のような多くの言語は、Windows 上ではに移植され、優れた動作をします。</span><span class="sxs-lookup"><span data-stu-id="60c46-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="60c46-134">ただし、すべての Ruby Gem または node/NPM ライブラリ所有者が、Windows をサポートするためにライブラリを移植するわけではありません。また、多くの場合、Linux 固有の依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="60c46-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="60c46-135">多くの場合、このようなツールやライブラリを使用して構築されたシステムは、ビルドから悪影響を受ける可能性があります。また、Windows で実行時エラーや望ましくない動作が発生することも</span><span class="sxs-lookup"><span data-stu-id="60c46-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="60c46-136">これらの問題の一部は、Windows のコマンドラインツールを改善するために Microsoft に依頼することがあります。また、ネイティブの Bash と Linux のコマンドラインツールを Windows で実行できるようにするために、パートナーに正規のパートナーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="60c46-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="60c46-137">PowerShell の意味</span><span class="sxs-lookup"><span data-stu-id="60c46-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="60c46-138">OSS プロジェクトの作業中に、PowerShell プロンプトから Bash に非常ことができるシナリオは多数あります。</span><span class="sxs-lookup"><span data-stu-id="60c46-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="60c46-139">Bash のサポートは補完的で、Windows のコマンドラインの価値を強化し、PowerShell と PowerShell コミュニティで他の一般的なテクノロジを利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="60c46-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="60c46-140">詳細については、PowerShell チームブログ[の「Bash for Windows:それがすばらしい理由と PowerShell の意味](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="60c46-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="60c46-141">WSL ですべての Linux アプリを実行できますか。</span><span class="sxs-lookup"><span data-stu-id="60c46-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="60c46-142">違います！</span><span class="sxs-lookup"><span data-stu-id="60c46-142">No!</span></span> <span data-ttu-id="60c46-143">WSL は、Windows 上で Bash およびコア Linux コマンドラインツールを実行する必要があるユーザーを有効にすることを目的としたツールです。</span><span class="sxs-lookup"><span data-stu-id="60c46-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="60c46-144">WSL は、GUI デスクトップやアプリケーション (例: Gnome、KDE など) をサポートすることを目的とし**ていません**。</span><span class="sxs-lookup"><span data-stu-id="60c46-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="60c46-145">また、多くの一般的なサーバーアプリケーション (Redis など) を実行できる場合でも、運用サービスをホストするための WSL はお勧めしません。 Microsoft は、Azure、Hyper-v、Docker で運用環境の Linux ワークロードを実行するためのさまざまなソリューションを提供しています。</span><span class="sxs-lookup"><span data-stu-id="60c46-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="60c46-146">WSL はどのような Windows Sku に含まれていますか。</span><span class="sxs-lookup"><span data-stu-id="60c46-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="60c46-147">Windows Subsystem for Linux は、windows 10 記念日および作成者更新以降の windows のデスクトップバージョンで使用できます。</span><span class="sxs-lookup"><span data-stu-id="60c46-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="60c46-148">Windows のデスクトップとサーバーの両方の Sku で、秋の更新プログラム WSL が使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="60c46-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="60c46-149">WSL はどのようなプロセッサをサポートしていますか。</span><span class="sxs-lookup"><span data-stu-id="60c46-149">What processors does WSL support?</span></span>
<span data-ttu-id="60c46-150">WSL は、x64 および ARM の Cpu をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="60c46-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="60c46-151">C: ドライブにアクセス操作方法</span><span class="sxs-lookup"><span data-stu-id="60c46-151">How do I access my C: drive?</span></span>
<span data-ttu-id="60c46-152">ローカルコンピューター上のハードドライブのマウントポイントが自動的に作成され、Windows ファイルシステムに簡単にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="60c46-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="60c46-153">**/mnt/\<ドライブ文字 >/**</span><span class="sxs-lookup"><span data-stu-id="60c46-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="60c46-154">使用例は c:\ `cd /mnt/c`にアクセスすることになります。</span><span class="sxs-lookup"><span data-stu-id="60c46-154">Example usage would be `cd /mnt/c` to access c:\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="60c46-155">Linux アプリで Windows ファイルを使用操作方法には</span><span class="sxs-lookup"><span data-stu-id="60c46-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="60c46-156">WSL の利点の1つは、Windows と Linux の両方のアプリまたはツールでファイルにアクセスできることです。</span><span class="sxs-lookup"><span data-stu-id="60c46-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="60c46-157">Wsl は、コンピューターの固定ドライブを Linux `/mnt/<drive>`ディストリビューションのフォルダーの下にマウントします。</span><span class="sxs-lookup"><span data-stu-id="60c46-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="60c46-158">たとえば、 `C:`ドライブは次のようにマウントされます。`/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="60c46-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="60c46-159">マウントされたドライブを使用する`C:\dev\myproj\`と、たとえば、 [Visual Studio](https://visualstudio.microsoft.com/vs/) /または[VS Code](https://code.visualstudio.com/)を使用してコードを編集したり、を介し`/mnt/c/dev/myproj`て同じファイルにアクセスして Linux でコードをビルド/テストしたりできます。</span><span class="sxs-lookup"><span data-stu-id="60c46-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="60c46-160">**重要な注意**:WSL を使用する際の主な制限事項の1つは、Windows アプリまたはツールを使用して Linux ディストリビューション ' ファイルシステム内のファイルに直接アクセスしたり変更したりすることがサポートされていないことです。</span><span class="sxs-lookup"><span data-stu-id="60c46-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="60c46-161">参照トピック[Windows アプリとツールを使用して Linux ファイルを変更しない](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="60c46-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="60c46-162">Linux ドライブのファイルはマウントされた Windows ドライブとは別のものですか。</span><span class="sxs-lookup"><span data-stu-id="60c46-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="60c46-163">Linux ルートの下にあるファイル ( `/`つまり) は、linux 固有の動作を模倣する wsl によって制御されます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="60c46-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="60c46-164">無効な Windows ファイル名文字を含むファイル</span><span class="sxs-lookup"><span data-stu-id="60c46-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="60c46-165">管理者以外のユーザーに対して作成されたシンボリックリンク</span><span class="sxs-lookup"><span data-stu-id="60c46-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="60c46-166">Chmod および chown を使用したファイル属性の変更</span><span class="sxs-lookup"><span data-stu-id="60c46-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="60c46-167">ファイル/フォルダーの大文字と小文字の区別</span><span class="sxs-lookup"><span data-stu-id="60c46-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="60c46-168">マウントされたドライブのファイルは Windows によって制御され、次の動作があります。</span><span class="sxs-lookup"><span data-stu-id="60c46-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="60c46-169">大文字と小文字の区別のサポート</span><span class="sxs-lookup"><span data-stu-id="60c46-169">Support case sensitivity</span></span>
   * <span data-ttu-id="60c46-170">すべてのアクセス許可は、Windows のアクセス許可を最適に反映するように設定されます。</span><span class="sxs-lookup"><span data-stu-id="60c46-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="60c46-171">Apt-upgrade upgrade を実行すると、多くのエラーが発生するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="60c46-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="60c46-172">一部のパッケージでは、まだ実装していない機能が使用されています。</span><span class="sxs-lookup"><span data-stu-id="60c46-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="60c46-173">`udev`たとえば、はまだサポートされていない`apt-get upgrade`ため、いくつかのエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="60c46-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="60c46-174">に`udev`関連する問題を修正するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="60c46-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="60c46-175">に次のもの`/usr/sbin/policy-rc.d`を書き込んで、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="60c46-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="60c46-176">実行アクセス許可の追加先`/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="60c46-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="60c46-177">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="60c46-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="60c46-178">WSL 配布操作方法アンインストールしますか?</span><span class="sxs-lookup"><span data-stu-id="60c46-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="60c46-179">1709 (16299) より前のビルドでは、コマンドプロンプトを開き、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="60c46-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="60c46-180">ストアからインストールされた wsl ディストリビューションは、他の Windows アプリと同様にアンインストールできます。そのためには、アプリタイルを右クリックして [アンインストール] をクリックするか、 [ `Remove-AppxPackage`コマンドレット](https://technet.microsoft.com/en-us/library/hh856038.aspx)を使用して PowerShell を使用します。</span><span class="sxs-lookup"><span data-stu-id="60c46-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="60c46-181">Ping によってアクセス拒否エラーが生成されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="60c46-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="60c46-182">WSL ビルド < 14926 では、管理者特権のコンソールを使用して実行するために必要な WSL を ping します。</span><span class="sxs-lookup"><span data-stu-id="60c46-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="60c46-183">この問題は、ビルド14926以降で修正されました。</span><span class="sxs-lookup"><span data-stu-id="60c46-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="60c46-184">OpenSSH サーバーを実行操作方法ますか?</span><span class="sxs-lookup"><span data-stu-id="60c46-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="60c46-185">Windows の管理者特権は、WSL で OpenSSH を実行するために必要です。</span><span class="sxs-lookup"><span data-stu-id="60c46-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="60c46-186">OpenSSH サーバーを実行するには、管理者として Windows 上で Bash on Ubuntu を実行するか、管理者特権を使用して CMD/PowerShell プロンプトから bash を実行します。</span><span class="sxs-lookup"><span data-stu-id="60c46-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="60c46-187">"エラー:0x80040306 "をインストールしようとすると、</span><span class="sxs-lookup"><span data-stu-id="60c46-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="60c46-188">WSL は、従来のコンソールでの実行をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="60c46-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="60c46-189">レガシコンソールをオフにするには:</span><span class="sxs-lookup"><span data-stu-id="60c46-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="60c46-190">WSL、PowerShell、または Cmd を開く</span><span class="sxs-lookup"><span data-stu-id="60c46-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="60c46-191">タイトルバーを右クリックし > プロパティ-> レガシコンソールを使用する をオフにします。</span><span class="sxs-lookup"><span data-stu-id="60c46-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="60c46-192">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60c46-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="60c46-193">"エラー:Windows をアップグレードした後に bash を実行する場合の0x80040154 が</span><span class="sxs-lookup"><span data-stu-id="60c46-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="60c46-194">Windows update で windows Subsystem for Linux 機能が無効になっている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="60c46-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="60c46-195">この問題が発生した場合は、Windows の機能を再度有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60c46-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="60c46-196">"Windows Subsystem for Linux" 機能を有効にする手順については、[インストールガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60c46-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="60c46-197">WSL の表示言語を変更操作方法には</span><span class="sxs-lookup"><span data-stu-id="60c46-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="60c46-198">WSL install は、Windows インストールのロケールに合わせて Ubuntu のロケールを自動的に変更しようとします。</span><span class="sxs-lookup"><span data-stu-id="60c46-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="60c46-199">この動作が不要な場合は、このコマンドを実行して、インストールの完了後に Ubuntu のロケールを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="60c46-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="60c46-200">この変更を有効にするには、bash を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60c46-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="60c46-201">次の例では、ロケールを en-us に変更します。</span><span class="sxs-lookup"><span data-stu-id="60c46-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="60c46-202">WSL からインターネットにアクセスできないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="60c46-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="60c46-203">一部のユーザーが、WSL でのインターネットアクセスをブロックする特定のファイアウォールアプリケーションに関する問題を報告しています。</span><span class="sxs-lookup"><span data-stu-id="60c46-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="60c46-204">報告されるファイアウォールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="60c46-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="60c46-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="60c46-205">Kaspersky</span></span>
1. <span data-ttu-id="60c46-206">AVG</span><span class="sxs-lookup"><span data-stu-id="60c46-206">AVG</span></span>
1. <span data-ttu-id="60c46-207">Avast</span><span class="sxs-lookup"><span data-stu-id="60c46-207">Avast</span></span>

<span data-ttu-id="60c46-208">場合によっては、ファイアウォールをオフにすることでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="60c46-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="60c46-209">場合によっては、ファイアウォールをインストールするだけでアクセスがブロックされます。</span><span class="sxs-lookup"><span data-stu-id="60c46-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="60c46-210">Windows の WSL からポートにアクセス操作方法には、</span><span class="sxs-lookup"><span data-stu-id="60c46-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="60c46-211">WSL は windows で実行されているため、Windows の IP アドレスを共有します。</span><span class="sxs-lookup"><span data-stu-id="60c46-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="60c46-212">このように、localhost 上の任意のポートにアクセスできます。たとえば、ポート 1234 https://localhost:1234 に web コンテンツがあった場合は、Windows ブラウザーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="60c46-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="60c46-213">WSL ディストリビューションをバックアップするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="60c46-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="60c46-214">ディストリビューションをバックアップする最適な方法は、Windows バージョン1809以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="60c46-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="60c46-215">`wsl --export`コマンドを使用して、配布全体を tar にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="60c46-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="60c46-216">その後、 `wsl --import`コマンドを使用してこのディストリビューションを wsl にインポートし直すことができます。これにより、wsl ディストリビューションの状態をバックアップして保存することができます。</span><span class="sxs-lookup"><span data-stu-id="60c46-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="60c46-217">Appdata フォルダー (Windows バックアップなど) のファイルをバックアップする従来のバックアップサービスでは、Linux ファイルが破損しないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="60c46-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="60c46-218">フィードバックはどこで提供できますか。</span><span class="sxs-lookup"><span data-stu-id="60c46-218">Where can I provide feedback?</span></span>

<span data-ttu-id="60c46-219">複数のチャネルを通じて、フィードバックを共有したり質問したりすることができます。フィードバックと質問は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="60c46-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="60c46-220">[GitHub の問題の追跡ツール](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="60c46-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="60c46-221">Microsoft[のコマンドライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="60c46-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="60c46-222">Microsoft[のコマンドラインチームのブログ](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="60c46-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="60c46-223">Twitter 経由。</span><span class="sxs-lookup"><span data-stu-id="60c46-223">Via Twitter.</span></span> <span data-ttu-id="60c46-224">ニュース、 [@richturn_ms](https://twitter.com/richturn_MS)更新プログラムなどの詳細については、Twitter でフォローしてください。</span><span class="sxs-lookup"><span data-stu-id="60c46-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
