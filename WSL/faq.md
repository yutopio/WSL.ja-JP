---
title: よく寄せられる質問 (FAQ)
description: に関してよく寄せられる質問 Windows サブシステム for Linux。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、よく寄せられる質問
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 07461f7db4a351f5b79ab0c5179d3d917ef1bdf7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035061"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="88664-104">Linux 用 Windows サブシステムに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="88664-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="88664-105">Windows Subsystem for Linux (WSL) とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="88664-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="88664-106">Windows Subsystem for Linux (WSL) は、Windows 10 の新機能を使用すると、Windows 上で直接ネイティブの Linux コマンド ライン ツールを実行、と共に、従来の Windows デスクトップおよび最新のストア アプリです。</span><span class="sxs-lookup"><span data-stu-id="88664-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="88664-107">参照してください、[ページに関する](./about.md)の詳細。</span><span class="sxs-lookup"><span data-stu-id="88664-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="88664-108">用の WSL は誰ですか。</span><span class="sxs-lookup"><span data-stu-id="88664-108">Who is WSL for?</span></span>
<span data-ttu-id="88664-109">これは、主に開発者--特に web 開発者と人とでまたはオープン ソース プロジェクトの作業のツールです。</span><span class="sxs-lookup"><span data-stu-id="88664-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="88664-110">これによりする/、Bash、Linux の一般的なツールを使用する必要がある人 (`sed`、`awk`など) と多くの Linux 最初ツール (Ruby、Python など) で Windows のツール チェーンを使用します。</span><span class="sxs-lookup"><span data-stu-id="88664-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="88664-111">WSL では、どうすればでしょうか。</span><span class="sxs-lookup"><span data-stu-id="88664-111">What can I do with WSL?</span></span>
<span data-ttu-id="88664-112">WSL では、アプリケーションと呼ばれる Bash.exe、起動するが開き、Bash シェルを実行する Windows コンソールを提供します。</span><span class="sxs-lookup"><span data-stu-id="88664-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="88664-113">Bash を使用して、Linux のコマンド ライン ツールとアプリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="88664-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="88664-114">たとえば、「`lsb_release -a`し、enter キーを押します。 現在実行されている Linux ディストリビューション詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88664-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![ディストリビューションの詳細のスクリーン ショット](media/distro.png)

<span data-ttu-id="88664-116">Linux の Bash シェル内からローカル コンピューターのファイル システムにもアクセスできます: ローカル ドライブでマウントされていることがわかります、`/mnt`フォルダー。</span><span class="sxs-lookup"><span data-stu-id="88664-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="88664-117">たとえば、`C:`下ドライブがマウントされて`/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="88664-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![マウントの C ドライブのスクリーン ショット](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="88664-119">Bash とは何ですか。</span><span class="sxs-lookup"><span data-stu-id="88664-119">What is Bash?</span></span>
<span data-ttu-id="88664-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)は、一般的なテキスト ベースのシェルおよびコマンド言語。</span><span class="sxs-lookup"><span data-stu-id="88664-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="88664-121">Ubuntu およびその他の Linux ディストリビューション内および macOS に含まれる既定のシェルになります。</span><span class="sxs-lookup"><span data-stu-id="88664-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="88664-122">ユーザーは、スクリプトを実行したり、多くのタスクを実行するには、コマンドとツールを実行するシェルにコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="88664-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="88664-123">この処理のしくみ</span><span class="sxs-lookup"><span data-stu-id="88664-123">How does this work?</span></span>
<span data-ttu-id="88664-124">チェック アウト、[ブログ](https://blogs.msdn.microsoft.com/wsl/)基になるテクノロジについての詳細を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88664-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="88664-125">使用する理由を Linux ではなく、WSL vm ですか。</span><span class="sxs-lookup"><span data-stu-id="88664-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="88664-126">WSL では、完全な仮想マシンよりも少ないリソース (CPU、メモリ、および記憶域) が必要です。</span><span class="sxs-lookup"><span data-stu-id="88664-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="88664-127">また、WSL では、アプリと共に、Windows コマンドライン、デスクトップ アプリとストア アプリ、および Linux コマンド ライン ツールを実行して、Linux 内から Windows ファイルにアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="88664-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="88664-128">これにより、希望する場合、同じファイルのセットでアプリを Windows および Linux コマンド ライン ツールを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="88664-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="88664-129">使用する理由をたとえば、Windows 上の代わりに Linux で Ruby でしょうか。</span><span class="sxs-lookup"><span data-stu-id="88664-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="88664-130">Linux のように実行される環境が動作すると仮定すると、いくつかのクロス プラットフォーム ツールを構築しました。</span><span class="sxs-lookup"><span data-stu-id="88664-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="88664-131">たとえば、いくつかのツールは、非常に長いファイル パスにアクセスできるか、特定のファイル/フォルダーが存在するとします。</span><span class="sxs-lookup"><span data-stu-id="88664-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="88664-132">多くの場合、問題が生じます動作では多くの場合、Windows の異なる方法で Linux から。</span><span class="sxs-lookup"><span data-stu-id="88664-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="88664-133">Ruby とノードのような多くの言語は多くの場合、移植し、優れた、Windows 上で実行します。</span><span class="sxs-lookup"><span data-stu-id="88664-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="88664-134">ただし、ポート、Windows をサポートするために、ライブラリのすべての Ruby Gem またはノード/NPM ライブラリの所有者と、Linux 固有の依存関係を持つ多くします。</span><span class="sxs-lookup"><span data-stu-id="88664-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="88664-135">このようなツールとライブラリのビルドと場合によっては実行時エラーまたは Windows 上の望ましくない動作の影響を受けてを使用して構築されたシステムでその多くの場合、結果します。</span><span class="sxs-lookup"><span data-stu-id="88664-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="88664-136">これらは、Windows のコマンド ライン ツールとどのようなネイティブ Bash および Linux コマンド ライン ツールを Windows 上で実行を有効にする Canonical によるパートナーを推進したほかを向上させるために Microsoft に依頼する多くの人々 を原因となった問題の一部です。</span><span class="sxs-lookup"><span data-stu-id="88664-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="88664-137">これはどういう PowerShell のでしょうか。</span><span class="sxs-lookup"><span data-stu-id="88664-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="88664-138">OSS プロジェクトで作業中には、PowerShell から Bash にドロップすると非常に便利なさまざまなシナリオがプロンプトです。</span><span class="sxs-lookup"><span data-stu-id="88664-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="88664-139">Bash のサポートは、補完的な人気のあるその他のテクノロジを活用するには、PowerShell と PowerShell コミュニティを許可する Windows 上のコマンドラインの値を強化します。</span><span class="sxs-lookup"><span data-stu-id="88664-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="88664-140">詳細については、PowerShell チームのブログ - [Bash for Windows:すばらしいことが理由と、PowerShell の意味](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="88664-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="88664-141">WSL では、すべての Linux アプリを実行できますか。</span><span class="sxs-lookup"><span data-stu-id="88664-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="88664-142">違います！</span><span class="sxs-lookup"><span data-stu-id="88664-142">No!</span></span> <span data-ttu-id="88664-143">WSL は、Bash を実行し、Windows 上の Linux コマンド ライン ツールのコアする必要があるユーザーの有効化を目的としたツールです。</span><span class="sxs-lookup"><span data-stu-id="88664-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="88664-144">WSL は**いない**GUI デスクトップまたはアプリケーション (例: Gnome、KDE など) をサポートする目的</span><span class="sxs-lookup"><span data-stu-id="88664-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="88664-145">また、たとえできなく多くの人気のあるサーバー アプリケーションを実行する (例: Redis)、運用環境のサービスをホストするため WSL お勧めしません – Microsoft はさまざまな Azure では、実稼働 Linux ワークロードを実行するためのソリューションを提供、HYPER-V、および Docker。</span><span class="sxs-lookup"><span data-stu-id="88664-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="88664-146">どのような Windows Sku が WSL には含まれますか。</span><span class="sxs-lookup"><span data-stu-id="88664-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="88664-147">Windows Subsystem for Linux は、Windows 10 Anniversary の Windows と Creators update 以降のデスクトップ バージョンで利用できます。</span><span class="sxs-lookup"><span data-stu-id="88664-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="88664-148">以降で Fall Creators update WSL は Sku の Windows デスクトップおよびサーバーの両方で提供されます。</span><span class="sxs-lookup"><span data-stu-id="88664-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="88664-149">WSL はどのようなプロセッサをサポートしますか。</span><span class="sxs-lookup"><span data-stu-id="88664-149">What processors does WSL support?</span></span>
<span data-ttu-id="88664-150">WSL では、x64 と ARM Cpu をサポートします。</span><span class="sxs-lookup"><span data-stu-id="88664-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="88664-151">C: ドライブをアクセスする方法はありますか</span><span class="sxs-lookup"><span data-stu-id="88664-151">How do I access my C: drive?</span></span>
<span data-ttu-id="88664-152">ローカル コンピューターのハード ドライブのマウント ポイントが自動的に作成し、Windows ファイル システムに簡単にアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="88664-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="88664-153">**/mnt/\<ドライブ文字 >/**</span><span class="sxs-lookup"><span data-stu-id="88664-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="88664-154">使用例`cd /mnt/c`c:\ にアクセスするには</span><span class="sxs-lookup"><span data-stu-id="88664-154">Example usage would be `cd /mnt/c` to access c:\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="88664-155">Linux アプリと Windows ファイルを使用する方法</span><span class="sxs-lookup"><span data-stu-id="88664-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="88664-156">WSL の利点の 1 つは、Windows と Linux の両方のアプリまたはツールを使用して、ファイルにアクセスできることです。</span><span class="sxs-lookup"><span data-stu-id="88664-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="88664-157">WSL が コンピューターの固定ドライブをマウント、 `/mnt/<drive>` Linux ディストリビューションでのフォルダー。</span><span class="sxs-lookup"><span data-stu-id="88664-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="88664-158">たとえば、`C:`下ドライブがマウントされて `/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="88664-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="88664-159">マウントされたドライブを使用して、コードを編集できます、たとえば、`C:\dev\myproj\`を使用して[Visual Studio](https://visualstudio.microsoft.com/vs/) /または[VS Code](https://code.visualstudio.com/)とを使用して同じファイルにアクセスして Linux では、そのコードのビルドおよびテスト`/mnt/c/dev/myproj`します。</span><span class="sxs-lookup"><span data-stu-id="88664-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="88664-160">**重要な注意事項**:WSL を使用する主な制限事項の 1 つは、直接へのアクセスまたは変更する、Windows アプリケーションやツールを使用して Linux ディストリビューションのファイル システム内のファイルがサポートされていないことです。</span><span class="sxs-lookup"><span data-stu-id="88664-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="88664-161">参照トピック[Windows アプリケーションおよびツールを使用して Linux ファイルを変更しないでください。](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="88664-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="88664-162">Windows のマウントされたドライブからさまざまな Linux ドライブにファイルがでしょうか。</span><span class="sxs-lookup"><span data-stu-id="88664-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="88664-163">Linux ルートの下のファイル (つまり`/`) を含むこれらに限定されませんが、Linux 特定の動作を模倣 WSL によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="88664-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="88664-164">無効な Windows ファイル名の文字が含まれるファイル</span><span class="sxs-lookup"><span data-stu-id="88664-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="88664-165">管理者以外のユーザー用に作成されたシンボリック リンク</span><span class="sxs-lookup"><span data-stu-id="88664-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="88664-166">Chmod、chown によるファイルの属性を変更します。</span><span class="sxs-lookup"><span data-stu-id="88664-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="88664-167">ファイル/フォルダー大文字小文字の区別</span><span class="sxs-lookup"><span data-stu-id="88664-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="88664-168">マウントされたドライブ内のファイルは、Windows によって制御され、次の動作します。</span><span class="sxs-lookup"><span data-stu-id="88664-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="88664-169">大文字小文字の区別をサポートします。</span><span class="sxs-lookup"><span data-stu-id="88664-169">Support case sensitivity</span></span>
   * <span data-ttu-id="88664-170">すべてのアクセス許可が最適な Windows のアクセス許可を反映するように設定されます。</span><span class="sxs-lookup"><span data-stu-id="88664-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="88664-171">なぜエラーがある非常に多く apt-get とアップグレードを実行するとしますか。</span><span class="sxs-lookup"><span data-stu-id="88664-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="88664-172">一部のパッケージはまだ実装されていない機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="88664-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="88664-173">`udev`、たとえば、はまだサポートされていません、いくつかの原因`apt-get upgrade`エラー。</span><span class="sxs-lookup"><span data-stu-id="88664-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="88664-174">関連する問題を修正する`udev`、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88664-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="88664-175">次のコードを記述`/usr/sbin/policy-rc.d`して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="88664-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="88664-176">追加するアクセス許可を実行 `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="88664-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="88664-177">次のコマンドを実行します</span><span class="sxs-lookup"><span data-stu-id="88664-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="88664-178">WSL 配布のアンインストール方法</span><span class="sxs-lookup"><span data-stu-id="88664-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="88664-179">ビルド 1709 (16299) オープンする前に、コマンド プロンプトし実行します。</span><span class="sxs-lookup"><span data-stu-id="88664-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="88664-180">アプリのタイルを右クリックし、[アンインストール] をクリックすると、または PowerShell を使用して他の Windows アプリのようなストアからインストール WSL ディストリビューションをアンインストールする、 [ `Remove-AppxPackage`コマンドレット](https://technet.microsoft.com/en-us/library/hh856038.aspx)します。</span><span class="sxs-lookup"><span data-stu-id="88664-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="88664-181">Ping が権限拒否エラーを生成する理由</span><span class="sxs-lookup"><span data-stu-id="88664-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="88664-182">WSL で構築されます < 14926、ping WSL を管理者特権でのコンソールを使用して実行するために必要な。</span><span class="sxs-lookup"><span data-stu-id="88664-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="88664-183">14926 のビルド以降、この問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="88664-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="88664-184">OpenSSH server を実行する方法はありますか</span><span class="sxs-lookup"><span data-stu-id="88664-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="88664-185">WSL で OpenSSH を実行するには、Windows で管理者特権が必要です。</span><span class="sxs-lookup"><span data-stu-id="88664-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="88664-186">OpenSSH server を実行するには、Ubuntu 上で管理者は、Windows で Bash を実行または bash.exe を管理者特権での CMD または PowerShell プロンプトから実行します。</span><span class="sxs-lookup"><span data-stu-id="88664-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="88664-187">なぜ"エラー。0x80040306"をインストールしようとするとしますか?</span><span class="sxs-lookup"><span data-stu-id="88664-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="88664-188">WSL では、従来のコンソールで実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="88664-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="88664-189">従来のコンソールをオフにするには。</span><span class="sxs-lookup"><span data-stu-id="88664-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="88664-190">WSL、PowerShell、または Cmd を開きます</span><span class="sxs-lookup"><span data-stu-id="88664-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="88664-191">タイトルを右クリックしてバー]-> [プロパティ]、[「従来のコンソールを使用して」をオフにします</span><span class="sxs-lookup"><span data-stu-id="88664-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="88664-192">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88664-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="88664-193">なぜ"エラー。0x80040154"Windows をアップグレードした後 bash.exe を実行するとしますか?</span><span class="sxs-lookup"><span data-stu-id="88664-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="88664-194">"Linux 用 Windows サブシステム"機能が無効になっている Windows の更新中にします。</span><span class="sxs-lookup"><span data-stu-id="88664-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="88664-195">このような場合、Windows の機能が再度有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88664-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="88664-196">"Linux 用 Windows サブシステム"機能を有効にする手順が記載されて、[インストール ガイド](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)します。</span><span class="sxs-lookup"><span data-stu-id="88664-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="88664-197">WSL の表示言語を変更する方法はありますか</span><span class="sxs-lookup"><span data-stu-id="88664-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="88664-198">WSL インストールは自動的に Windows インストールのロケールに一致するように Ubuntu ロケールを変更しようとします。</span><span class="sxs-lookup"><span data-stu-id="88664-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="88664-199">この動作したくない場合は、インストールが完了した後は、Ubuntu ロケールを変更するには、このコマンドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="88664-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="88664-200">この変更を有効にする bash.exe を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88664-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="88664-201">次の例のロケールを EN-US に変更します。</span><span class="sxs-lookup"><span data-stu-id="88664-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="88664-202">理由はアクセスできないインターネット WSL からでしょうか。</span><span class="sxs-lookup"><span data-stu-id="88664-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="88664-203">一部のユーザーには、WSL でインターネット アクセスをブロックする特定のファイアウォール アプリケーションで問題が報告します。</span><span class="sxs-lookup"><span data-stu-id="88664-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="88664-204">報告されるファイアウォールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="88664-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="88664-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="88664-205">Kaspersky</span></span>
1. <span data-ttu-id="88664-206">AVG</span><span class="sxs-lookup"><span data-stu-id="88664-206">AVG</span></span>
1. <span data-ttu-id="88664-207">Avast</span><span class="sxs-lookup"><span data-stu-id="88664-207">Avast</span></span>

<span data-ttu-id="88664-208">場合によっては、ファイアウォールを無効にすることに対するアクセス許可します。</span><span class="sxs-lookup"><span data-stu-id="88664-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="88664-209">アクセスをブロックするには、場合によっては、ファイアウォールをインストールしているだけで検索します。</span><span class="sxs-lookup"><span data-stu-id="88664-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="88664-210">ポートを Windows で WSL からアクセスする方法</span><span class="sxs-lookup"><span data-stu-id="88664-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="88664-211">WSL は、Windows で実行されているように、Windows の IP アドレスを共有します。</span><span class="sxs-lookup"><span data-stu-id="88664-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="88664-212">例: localhost 上の任意のポートをアクセスするようポート 1234 できますで web コンテンツをした https://localhost:1234Windows ブラウザーにします。</span><span class="sxs-lookup"><span data-stu-id="88664-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="88664-213">フィードバックを提供する場所は?</span><span class="sxs-lookup"><span data-stu-id="88664-213">Where can I provide feedback?</span></span>

<span data-ttu-id="88664-214">フィードバックを共有し、複数のチャネルを通じてに関する質問をしたりできます。フィードバックや質問が表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88664-214">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="88664-215">この[GitHub の issue トラッカー](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="88664-215">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="88664-216">この[コマンド ライン UserVoice ポータル](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="88664-216">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="88664-217">この[コマンド ライン チームのブログ](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="88664-217">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="88664-218">Twitter。</span><span class="sxs-lookup"><span data-stu-id="88664-218">Via Twitter.</span></span> <span data-ttu-id="88664-219">従ってください[ @richturn_ms ](https://twitter.com/richturn_MS)についてのニュース、更新プログラム、twitter など。</span><span class="sxs-lookup"><span data-stu-id="88664-219">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
