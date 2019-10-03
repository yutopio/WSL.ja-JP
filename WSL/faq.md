---
title: よく寄せられる質問 (FAQ)
description: Windows Subsystem for Linux に関してよく寄せられる質問。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 78d0dc3db6f0c173cec64c9830df981568320717
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269741"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="36dd3-104">Windows Subsystem for Linux に関してよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="36dd3-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="36dd3-105">Windows Subsystem for Linux (WSL) とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="36dd3-106">Windows Subsystem for Linux (WSL) は、ネイティブ Linux コマンド ライン ツールを Windows で直接実行できる Windows 10 の新機能です。これは、従来の Windows デスクトップや最新のストア アプリと共存します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="36dd3-107">詳しくは、[詳細ページ](./about.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="36dd3-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="36dd3-108">WSL の対象ユーザーは誰ですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-108">Who is WSL for?</span></span>
<span data-ttu-id="36dd3-109">これは、主に開発者向けのツールです。特に Web 開発者と、オープン ソース プロジェクトで作業している開発者が対象です。</span><span class="sxs-lookup"><span data-stu-id="36dd3-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="36dd3-110">これにより、Bash、一般的な Linux ツール (`sed`、 `awk` など)、および多くの Linux ファースト ツール (Ruby、Python など) を使用する必要があるユーザーは、Windows でそれらのツールチェーンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="36dd3-111">WSL で何ができますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-111">What can I do with WSL?</span></span>
<span data-ttu-id="36dd3-112">WSL が提供する Bash.exe というアプリケーションを開始すると、Bash シェルを実行している Windows コンソールが開きます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="36dd3-113">Bash を使用すると、コマンド ライン Linux ツールおよびアプリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="36dd3-114">たとえば、「`lsb_release -a`」と入力して Enter キーを押すと、現在実行中の Linux ディストリビューションの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![ディストリビューションの詳細のスクリーンショット](media/distro.png)

<span data-ttu-id="36dd3-116">Linux Bash シェル内からローカル コンピューターのファイル システムにアクセスすることもできます。ローカル ドライブは `/mnt` フォルダーの下にマウントされます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="36dd3-117">たとえば、 `C:` ドライブは `/mnt/c` の下にマウントされます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![マウントされた C ドライブのスクリーンショット](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="36dd3-119">Bash とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-119">What is Bash?</span></span>
<span data-ttu-id="36dd3-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) は、広く使われているテキスト ベースのシェルおよびコマンド言語です。</span><span class="sxs-lookup"><span data-stu-id="36dd3-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="36dd3-121">これは、Ubuntu およびその他の Linux ディストリビューション内と macOS に含まれる既定のシェルです。</span><span class="sxs-lookup"><span data-stu-id="36dd3-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="36dd3-122">ユーザーは、シェルにコマンドを入力して、スクリプトを実行したり、コマンドやツールを実行したりして多くのタスクを行います。</span><span class="sxs-lookup"><span data-stu-id="36dd3-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="36dd3-123">この処理のしくみ</span><span class="sxs-lookup"><span data-stu-id="36dd3-123">How does this work?</span></span>
<span data-ttu-id="36dd3-124">基礎となるテクノロジの詳細については、[ブログ](https://blogs.msdn.microsoft.com/wsl/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36dd3-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="36dd3-125">VM で Linux ではなく WSL を使用するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="36dd3-126">WSL は、必要なリソース (CPU、メモリ、およびストレージ) が完全な仮想マシンよりも少なくて済みます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="36dd3-127">また、WSL を使用すると、Linux コマンド ライン ツールおよびアプリを Windows コマンド ライン、デスクトップおよびストア アプリと共に実行したり、Linux 内から Windows ファイルにアクセスしたりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="36dd3-128">これにより、必要に応じて、同じファイル セットに対して Windows アプリと Linux コマンド ライン ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="36dd3-129">たとえば、Windows ではなく Linux 上で Ruby を使用するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="36dd3-130">一部のクロスプラットフォーム ツールは、それらが実行される環境が Linux のように動作することを前提として構築されました。</span><span class="sxs-lookup"><span data-stu-id="36dd3-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="36dd3-131">たとえば、一部のツールでは、非常に長いファイル パスにアクセスできることや、特定のファイルまたはフォルダーが存在することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="36dd3-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="36dd3-132">これにより、Linux とは動作が異なる事が多い Windows で問題が発生することがよくあります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="36dd3-133">Ruby や node のような多くの言語は、たいていの場合、Windows に移植され、非常にうまく動作します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="36dd3-134">ただし、すべての Ruby Gem または node/NPM ライブラリ所有者が、Windows をサポートするためにライブラリを移植するわけではなく、多くのものに Linux 固有の依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="36dd3-135">これにより、このようなツールやライブラリを使用して構築されたシステムはビルドから悪影響を受ける場合が多く、Windows で実行時エラーや望ましくない動作が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="36dd3-136">これらは、多くのユーザーが Windows のコマンド ライン ツールの向上を Microsoft に依頼する原因となった問題の一部に過ぎません。また、こうした要因から、Microsoft が Canonical と提携して、ネイティブ Bash と Linux コマンド ライン ツールを Windows で実行できるようにすることになりました。</span><span class="sxs-lookup"><span data-stu-id="36dd3-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="36dd3-137">PowerShell においてこれは何を意味しますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="36dd3-138">OSS プロジェクトでの作業中、PowerShell プロンプトから Bash を実行すると非常に役立つシナリオが多数あります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="36dd3-139">Bash のサポートは補完的なものであり、Windows でのそのコマンド ラインの価値を高め、PowerShell と PowerShell コミュニティでその他の一般的なテクノロジを利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="36dd3-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="36dd3-140">詳細については、PowerShell チームのブログ「[Windows の Bash:それがすばらしい理由と PowerShell における意味](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)」をお読みください</span><span class="sxs-lookup"><span data-stu-id="36dd3-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="36dd3-141">WSL ですべての Linux アプリを実行できますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="36dd3-142">いいえ。</span><span class="sxs-lookup"><span data-stu-id="36dd3-142">No!</span></span> <span data-ttu-id="36dd3-143">WSL は、Bash およびコア Linux コマンド ライン ツールを必要とするユーザーが Windows 上でそれらを実行できるようにすることを目的としたツールです。</span><span class="sxs-lookup"><span data-stu-id="36dd3-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="36dd3-144">WSL は、GUI デスクトップやアプリケーション (例: Gnome、KDE など) をサポートすることを目的として**いません**。</span><span class="sxs-lookup"><span data-stu-id="36dd3-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="36dd3-145">また、多くの一般的なサーバー アプリケーション (Redis など) を実行できる場合でも、実稼働サービスをホストする目的には WSL をお勧めしません。Microsoft は、Azure、Hyper-V、Docker で実稼働 Linux ワークロードを実行するためのさまざまなソリューションを提供しています。</span><span class="sxs-lookup"><span data-stu-id="36dd3-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="36dd3-146">WSL はどの Windows SKU に含まれていますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="36dd3-147">Windows Subsystem for Linux は、Windows 10 Anniversary および Creators Update 以降の Windows デスクトップ バージョンで使用できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="36dd3-148">Fall Creators Update 以降では、WSL は Windows のデスクトップとサーバーの両方の SKU で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="36dd3-149">WSL はどのようなプロセッサをサポートしていますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-149">What processors does WSL support?</span></span>
<span data-ttu-id="36dd3-150">WSL は x64 および ARM の CPU をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="36dd3-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="36dd3-151">C: ドライブにアクセスするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-151">How do I access my C: drive?</span></span>
<span data-ttu-id="36dd3-152">ローカル コンピューター上のハード ドライブのマウント ポイントが自動的に作成され、Windows ファイル システムに簡単にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="36dd3-153">**/mnt/\<ドライブ文字>/**</span><span class="sxs-lookup"><span data-stu-id="36dd3-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="36dd3-154">使用例は、c:\ にアクセスする `cd /mnt/c` です。</span><span class="sxs-lookup"><span data-stu-id="36dd3-154">Example usage would be `cd /mnt/c` to access c:\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="36dd3-155">Linux アプリで Windows ファイルをどのように使用しますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="36dd3-156">WSL の利点の 1 つは、Windows と Linux の両方のアプリまたはツールを経由してファイルにアクセスできることです。</span><span class="sxs-lookup"><span data-stu-id="36dd3-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="36dd3-157">WSL では、コンピューターの固定ドライブを Linux ディストリビューションの `/mnt/<drive>` フォルダーの下にマウントします。</span><span class="sxs-lookup"><span data-stu-id="36dd3-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="36dd3-158">たとえば、 `C:` ドライブは `/mnt/c/` の下にマウントされます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="36dd3-159">マウントされたドライブを使用すると、[Visual Studio](https://visualstudio.microsoft.com/vs/) または[VS Code](https://code.visualstudio.com/)を使用して、たとえば `C:\dev\myproj\` 内のコードを編集したり、`/mnt/c/dev/myproj` を介して同じファイルにアクセスして Linux でそのコードをビルド/テストしたりできます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="36dd3-160">**重要な注意**:WSL を使用する際の主な制限事項の 1 つは、Windows アプリまたはツールを使用して Linux ディストリビューションのファイル システム内のファイルに直接アクセスしたり、変更したりすることがサポートされていないことです。</span><span class="sxs-lookup"><span data-stu-id="36dd3-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="36dd3-161">以下をご覧ください。[Windows アプリやツールを使用して Linux ファイルを変更しない](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="36dd3-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="36dd3-162">Linux ドライブのファイルはマウントされた Windows ドライブのものとは異なりますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="36dd3-163">Linux ルート (つまり `/`) の下にあるファイルは、Linux 固有の性質を模倣する WSL によって制御されます。次のようなものが含まれますが、これらに限定されません。</span><span class="sxs-lookup"><span data-stu-id="36dd3-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="36dd3-164">無効な Windows ファイル名の文字を含むファイル</span><span class="sxs-lookup"><span data-stu-id="36dd3-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="36dd3-165">管理者以外のユーザー用に作成されたシンボリック リンク</span><span class="sxs-lookup"><span data-stu-id="36dd3-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="36dd3-166">chmod および chown を使用したファイル属性の変更</span><span class="sxs-lookup"><span data-stu-id="36dd3-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="36dd3-167">ファイル/フォルダーの大文字と小文字の区別</span><span class="sxs-lookup"><span data-stu-id="36dd3-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="36dd3-168">マウントされたドライブのファイルは Windows によって制御され、次のように動作します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="36dd3-169">大文字と小文字の区別をサポート</span><span class="sxs-lookup"><span data-stu-id="36dd3-169">Support case sensitivity</span></span>
   * <span data-ttu-id="36dd3-170">すべてのアクセス許可は、Windows アクセス許可を最適に反映するように設定</span><span class="sxs-lookup"><span data-stu-id="36dd3-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="36dd3-171">apt-get upgrade を実行すると、多くのエラーが発生するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="36dd3-172">一部のパッケージでは、Microsoft がまだ実装していない機能が使用されています。</span><span class="sxs-lookup"><span data-stu-id="36dd3-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="36dd3-173">たとえば、`udev` はまだサポートされていないため、`apt-get upgrade` エラーがいくつか発生します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="36dd3-174">`udev` に関連する問題を修正するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="36dd3-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="36dd3-175">次の内容を `/usr/sbin/policy-rc.d` に記述して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="36dd3-176">実行のアクセス許可を `/usr/sbin/policy-rc.d` に追加します</span><span class="sxs-lookup"><span data-stu-id="36dd3-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="36dd3-177">次のコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="36dd3-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="36dd3-178">WSL ディストリビューションをアンインストールするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="36dd3-179">1709 (16299) より前のビルドでは、コマンド プロンプトを開き、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="36dd3-180">ストアからインストールされた WSL ディストリビューションは、他の Windows アプリと同様に、アプリ タイルを右クリックして [アンインストール] をクリックするか、[`Remove-AppxPackage` コマンドレット](https://technet.microsoft.com/en-us/library/hh856038.aspx)を使用して PowerShell を介してアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="36dd3-181">ping によってアクセス拒否エラーが発生するのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="36dd3-182">14926 より前の WSL ビルドでは、WSL で管理者特権のコンソールを使用して ping を実行する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="36dd3-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="36dd3-183">この問題は、ビルド14926 以降で修正されました。</span><span class="sxs-lookup"><span data-stu-id="36dd3-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="36dd3-184">OpenSSH サーバーを実行するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="36dd3-185">WSL で OpenSSH を実行するには、Windows の管理者特権が必要です。</span><span class="sxs-lookup"><span data-stu-id="36dd3-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="36dd3-186">OpenSSH サーバーを実行するには、管理者として Bash on Ubuntu on Windows を実行するか、管理者特権を使用して CMD/PowerShell プロンプトから bash.exe を実行します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="36dd3-187">インストールしようとすると、"エラー:0x80040306" が表示されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="36dd3-188">WSL は、従来のコンソールでの実行をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="36dd3-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="36dd3-189">従来のコンソールをオフにするには、以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="36dd3-190">WSL、PowerShell、または Cmd を開きます</span><span class="sxs-lookup"><span data-stu-id="36dd3-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="36dd3-191">タイトル バーを右クリックして、[プロパティ] を選択し、[従来のコンソールを使う] をオフにします</span><span class="sxs-lookup"><span data-stu-id="36dd3-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="36dd3-192">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36dd3-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="36dd3-193">Windows のアップグレード後に bash.exe を実行すると、"エラー:0x80040154" が表示されるのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="36dd3-194">Windows Update 時に "Windows Subsystem for Linux" 機能が無効になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="36dd3-195">その場合は、この Windows 機能を再度有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="36dd3-196">"Windows Subsystem for Linux" 機能を有効にする手順については、[インストール ガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="36dd3-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="36dd3-197">WSL の表示言語を変更するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="36dd3-198">WSL インストールでは、Windows インストールのロケールに合わせて Ubuntu ロケールを自動的に変更しようとします。</span><span class="sxs-lookup"><span data-stu-id="36dd3-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="36dd3-199">この動作が不要な場合は、次のコマンドを実行して、インストールの完了後に Ubuntu ロケールを変更できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="36dd3-200">この変更を有効にするには、bash.exe を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="36dd3-201">次の例は、ロケールを en-US に変更します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="36dd3-202">WSL からインターネットにアクセスできないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="36dd3-203">一部のユーザーにより、WSL でのインターネット アクセスをブロックする特定のファイアウォール アプリケーションに関する問題が報告されています。</span><span class="sxs-lookup"><span data-stu-id="36dd3-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="36dd3-204">報告されているファイアウォールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="36dd3-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="36dd3-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="36dd3-205">Kaspersky</span></span>
1. <span data-ttu-id="36dd3-206">AVG</span><span class="sxs-lookup"><span data-stu-id="36dd3-206">AVG</span></span>
1. <span data-ttu-id="36dd3-207">Avast</span><span class="sxs-lookup"><span data-stu-id="36dd3-207">Avast</span></span>

<span data-ttu-id="36dd3-208">ファイアウォールをオフにすると、アクセスできる場合があります。</span><span class="sxs-lookup"><span data-stu-id="36dd3-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="36dd3-209">場合によっては、ファイアウォールをインストールするだけでアクセスがブロックされるようです。</span><span class="sxs-lookup"><span data-stu-id="36dd3-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="36dd3-210">Windows の WSL からポートにアクセスするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="36dd3-211">WSL は Windows で実行されているため、Windows の IP アドレスを共有します。</span><span class="sxs-lookup"><span data-stu-id="36dd3-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="36dd3-212">そのため、localhost 上の任意のポートにアクセスできます。たとえば、ポート 1234 に Web コンテンツがあるとすると、 https://localhost:1234 を Windows ブラウザーに入力できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="36dd3-213">WSL ディストリビューションをバックアップするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="36dd3-214">ディストリビューションをバックアップする最適な方法は、Windows バージョン1809 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="36dd3-215">`wsl --export` コマンドを使用して、ディストリビューション全体を tarball にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="36dd3-216">その後、`wsl --import` コマンドを使用してこのディストリビューションを WSL にインポートし直すことができます。これにより、WSL ディストリビューションの状態をバックアップして保存できます。</span><span class="sxs-lookup"><span data-stu-id="36dd3-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="36dd3-217">Appdata フォルダーのファイルをバックアップする従来のバックアップ サービス (Windows バックアップなど) によって Linux ファイルが破損することはありません。</span><span class="sxs-lookup"><span data-stu-id="36dd3-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="36dd3-218">フィードバックはどこで提供できますか。</span><span class="sxs-lookup"><span data-stu-id="36dd3-218">Where can I provide feedback?</span></span>

<span data-ttu-id="36dd3-219">複数のチャネルを通じて、フィードバックを共有したり、質問したりできます。フィードバックや質問は以下宛てにお願いいたします。</span><span class="sxs-lookup"><span data-stu-id="36dd3-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="36dd3-220">Microsoft の [GitHub の問題の追跡ツール](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="36dd3-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="36dd3-221">Microsoft の[コマンド ライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="36dd3-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="36dd3-222">[Microsoft のコマンド ライン チームのブログ](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="36dd3-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="36dd3-223">Twitter 経由。</span><span class="sxs-lookup"><span data-stu-id="36dd3-223">Via Twitter.</span></span> <span data-ttu-id="36dd3-224">ニュース、更新などを確認するには、Twitter で [@richturn_ms](https://twitter.com/richturn_MS) をフォローしてください。</span><span class="sxs-lookup"><span data-stu-id="36dd3-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
