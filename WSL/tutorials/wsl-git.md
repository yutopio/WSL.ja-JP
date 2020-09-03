---
title: Windows Subsystem for Linux で Git の使用を開始する
description: Windows Subsystem for Linux でバージョン管理用の Git を設定する方法について説明します。
keywords: wsl、windows、windowssubsystem、gnu、linux、bash、git、github、バージョン管理
ms.date: 06/04/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: c48234be5c3867d771363aaa5e630d8ebe378364
ms.sourcegitcommit: 6ff046993e9f196cdfa04f5f91130e0e4ff1e7fa
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "89427219"
---
# <a name="get-started-using-git-on-windows-subsystem-for-linux"></a><span data-ttu-id="f6fbb-104">Windows Subsystem for Linux で Git の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="f6fbb-104">Get started using Git on Windows Subsystem for Linux</span></span>

<span data-ttu-id="f6fbb-105">Git は、最も一般的に使用されるバージョン管理システムです。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-105">Git is the most commonly used version control system.</span></span> <span data-ttu-id="f6fbb-106">Git を使用すると、ファイルに加えた変更を追跡できるため、実行された内容を記録し、必要に応じて、以前のバージョンのファイルに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-106">With Git, you can track changes you make to files, so you have a record of what has been done, and have the ability to revert to earlier versions of the files if needed.</span></span> <span data-ttu-id="f6fbb-107">また、Git を使用するとコラボレーションが容易になり、複数の人が変更を1つのソースにマージできるようになります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-107">Git also makes collaboration easier, allowing changes by multiple people to all be merged into one source.</span></span>

## <a name="git-can-be-installed-on-windows-and-on-wsl"></a><span data-ttu-id="f6fbb-108">Git は、Windows および WSL にインストールできます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-108">Git can be installed on Windows AND on WSL</span></span>

<span data-ttu-id="f6fbb-109">重要な考慮事項: WSL を有効にして Linux ディストリビューションをインストールする場合は、Windows NTFS C:\ から分離した新しいファイルシステムをインストールします。コンピューター上のドライブ。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-109">An important consideration: when you enable WSL and install a Linux distribution, you are installing a new file system, separated from the Windows NTFS C:\ drive on your machine.</span></span> <span data-ttu-id="f6fbb-110">Linux では、ドライブに文字が指定されていません。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-110">In Linux, drives are not given letters.</span></span> <span data-ttu-id="f6fbb-111">これらにはマウントポイントが指定されています。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-111">They are given mount points.</span></span> <span data-ttu-id="f6fbb-112">ファイルシステムのルートは、 `/` ルートパーティションのマウントポイント、または WSL の場合はフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-112">The root of your file system `/` is the mount point of your root partition, or folder, in the case of WSL.</span></span> <span data-ttu-id="f6fbb-113">すべてが同じドライブであるとは限りません `/` 。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-113">Not everything under `/` is the same drive.</span></span> <span data-ttu-id="f6fbb-114">たとえば、ラップトップには、2つのバージョンの Ubuntu (20.04 と 18.04) と Debian がインストールされています。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-114">For example, on my laptop, I've installed two version of Ubuntu (20.04 and 18.04), as well as Debian.</span></span> <span data-ttu-id="f6fbb-115">これらの配布を開いた場合は、コマンドを使用してルートディレクトリを選択 `cd ~` し、コマンドを入力すると、 `explorer.exe .` Windows ファイルエクスプローラーが開き、その配布のディレクトリパスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-115">If I open those distributions, select the root directory with the command `cd ~`, and then enter the command `explorer.exe .`, Windows File Explorer will open and show me the directory path for that distribution.</span></span>

| <span data-ttu-id="f6fbb-116">Linux ディストリビューション</span><span class="sxs-lookup"><span data-stu-id="f6fbb-116">Linux distro</span></span> | <span data-ttu-id="f6fbb-117">ホームフォルダーにアクセスするための Windows パス</span><span class="sxs-lookup"><span data-stu-id="f6fbb-117">Windows Path to access home folder</span></span> |
| ----------- | ----------- |
| <span data-ttu-id="f6fbb-118">Ubuntu 20.04</span><span class="sxs-lookup"><span data-stu-id="f6fbb-118">Ubuntu 20.04</span></span> | `\\wsl$\Ubuntu-20.04\home\username` |
| <span data-ttu-id="f6fbb-119">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="f6fbb-119">Ubuntu 18.04</span></span> | `\\wsl$\Ubuntu-18.04\home\username` |
| <span data-ttu-id="f6fbb-120">Debian</span><span class="sxs-lookup"><span data-stu-id="f6fbb-120">Debian</span></span> | `\\wsl$\Debian\home\username` |
| <span data-ttu-id="f6fbb-121">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f6fbb-121">Windows PowerShell</span></span> | `C:\Users\username` |

> [!TIP]
> <span data-ttu-id="f6fbb-122">ではなく、WSL ディストリビューションコマンドラインから Windows ファイルディレクトリにアクセスしようとすると、を `C:\Users\username` 使用してディレクトリにアクセスし `/mnt/c/Users/username` ます。 Linux ディストリビューションでは、windows ファイルシステムがマウントされたドライブとして表示されるためです。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-122">If you are seeking to access the Windows file directory from your WSL distribution command line, instead of `C:\Users\username`, the directory would be accessed using `/mnt/c/Users/username`, because the Linux distribution views your Windows file system as a mounted drive.</span></span>

<span data-ttu-id="f6fbb-123">使用する予定の各ファイルシステムに Git をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-123">You will need to install Git on each file system that you intend to use it with.</span></span>

![ディストリビューションによる Git バージョンの表示](../media/git-versions.gif)

## <a name="installing-git"></a><span data-ttu-id="f6fbb-125">Installing Git (Git のインストール) (Git のインストール)</span><span class="sxs-lookup"><span data-stu-id="f6fbb-125">Installing Git</span></span>

<span data-ttu-id="f6fbb-126">Git は、ほとんどの Windows Subsystem for Linux ディストリビューションで既にインストールされていますが、最新バージョンに更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-126">Git comes already installed with most of the Windows Subsystem for Linux distributions, however, you may want to update to the latest version.</span></span> <span data-ttu-id="f6fbb-127">また、git 構成ファイルを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-127">You also will need to set up your git config file.</span></span>

<span data-ttu-id="f6fbb-128">Git をインストールするには、 [Linux サイト用の Git ダウンロードに関する](https://git-scm.com/download/linux) ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-128">To install Git, see the [Git Download for Linux](https://git-scm.com/download/linux) site.</span></span> <span data-ttu-id="f6fbb-129">各 Linux ディストリビューションには、独自のパッケージマネージャーとインストールコマンドがあります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-129">Each Linux distribution has their own package manager and install command.</span></span>

<span data-ttu-id="f6fbb-130">Ubuntu/Debian の最新の安定した GIt バージョンについては、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-130">For the latest stable GIt version in Ubuntu/Debian, enter the command:</span></span>

```bash
sudo apt-get install git
```

> [!NOTE]
> <span data-ttu-id="f6fbb-131">また、 [Git For Windows](https://git-scm.com/download/win) をまだインストールしていない場合にもインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-131">You also may want to [install Git for Windows](https://git-scm.com/download/win) if you haven't already.</span></span>

## <a name="git-config-file-setup"></a><span data-ttu-id="f6fbb-132">Git 構成ファイルのセットアップ</span><span class="sxs-lookup"><span data-stu-id="f6fbb-132">Git config file setup</span></span>

<span data-ttu-id="f6fbb-133">Git 構成ファイルを設定するには、作業中のディストリビューションのコマンドラインを開き、次のコマンドで名前を設定します ("your Name" を Git ユーザー名に置き換えます)。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-133">To set up your Git config file, open a command line for the distribution you're working in and set your name with this command (replacing "Your Name" with your Git username):</span></span>

```bash
git config --global user.name "Your Name"
```

<span data-ttu-id="f6fbb-134">次のコマンドを使用して電子メールを設定します (" youremail@domain.com " は、Git アカウントで使用する電子メールに置き換えてください)。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-134">Set your email with this command (replacing "youremail@domain.com" with the email you use on your Git account):</span></span>

```bash
git config --global user.email "youremail@domain.com"
```

> [!TIP]
> <span data-ttu-id="f6fbb-135">まだ Git アカウントを持っていない場合は、[GitHub でそれにサインアップ](https://github.com/join)することができます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-135">If you don't yet have a Git account, you can [sign-up for one on GitHub](https://github.com/join).</span></span> <span data-ttu-id="f6fbb-136">以前に Git を使用したことがない場合、入門用の [GitHub ガイド](https://guides.github.com/)が役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-136">If you've never worked with Git before, [GitHub Guides](https://guides.github.com/) can help you get started.</span></span> <span data-ttu-id="f6fbb-137">git 構成を編集する必要がある場合は、nano のような組み込みのテキスト エディターを使用してそれを行うことができます: `nano ~/.gitconfig`</span><span class="sxs-lookup"><span data-stu-id="f6fbb-137">If you need to edit your git config, you can do so with a built-in text editor like nano: `nano ~/.gitconfig`.</span></span>

<span data-ttu-id="f6fbb-138">[2 要素認証 (2FA) を使用](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa)してアカウントをセキュリティで保護することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-138">We recommend that you [secure your account with two-factor authentication (2FA)](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa).</span></span>

## <a name="git-credential-manager-setup"></a><span data-ttu-id="f6fbb-139">Git Credential Manager のセットアップ</span><span class="sxs-lookup"><span data-stu-id="f6fbb-139">Git Credential Manager setup</span></span>

<span data-ttu-id="f6fbb-140">Git Credential Manager を使用すると、リモート Git サーバーを認証することができます。これには、2要素認証のような複雑な認証パターン、Azure Active Directory、またはすべての git プッシュに SSH キーパスワードを必要とする SSH リモート Url の使用などがあります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-140">Git Credential Manager enables you to authenticate a remote Git server, even if you have a complex authentication pattern like two-factor authentication, Azure Active Directory, or using SSH remote URLs that require an SSH key password for every git push.</span></span> <span data-ttu-id="f6fbb-141">Git Credential Manager は、GitHub などのサービスの認証フローに統合されています。ユーザーがホスティング プロバイダーに対して認証されると、新しい認証トークンが要求されます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-141">Git Credential Manager integrates into the authentication flow for services like GitHub and, once you're authenticated to your hosting provider, requests a new authentication token.</span></span> <span data-ttu-id="f6fbb-142">その後、トークンを [Windows 資格情報マネージャー](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager)に安全に格納します。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-142">It then stores the token securely in the [Windows Credential Manager](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager).</span></span> <span data-ttu-id="f6fbb-143">2 回目以降は、Git を使用してホスティング プロバイダーと通信することができ、再認証は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-143">After the first time, you can use git to talk to your hosting provider without needing to re-authenticate.</span></span> <span data-ttu-id="f6fbb-144">Windows 資格情報マネージャーにあるトークンへのアクセスだけが行われることになります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-144">It will just access the token in the Windows Credential Manager.</span></span>

<span data-ttu-id="f6fbb-145">WSL ディストリビューションで使用するように Git Credential Manager をセットアップするには、ディストリビューションを開き、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-145">To set up Git Credential Manager for use with a WSL distribution, open your distribution and enter this command:</span></span>

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

<span data-ttu-id="f6fbb-146">これで、WSL ディストリビューション内で実行するすべての Git 操作で、資格情報マネージャーが使用されるようになります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-146">Now any git operation you perform within your WSL distribution will use the credential manager.</span></span> <span data-ttu-id="f6fbb-147">ホスト用に既にキャッシュされている資格情報がある場合は、それらへのアクセスが資格情報マネージャーから行われます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-147">If you already have credentials cached for a host, it will access them from the credential manager.</span></span> <span data-ttu-id="f6fbb-148">そうでない場合は、Linux コンソールを使用しているとしても、資格情報を要求するダイアログ応答が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-148">If not, you'll receive a dialog response requesting your credentials, even if you're in a Linux console.</span></span>

> [!NOTE]
> <span data-ttu-id="f6fbb-149">コード署名セキュリティに GPG キーを使用している場合は、 [GPG キーを GitHub の電子メールに関連付ける](https://help.github.com/en/github/authenticating-to-github/associating-an-email-with-your-gpg-key)必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-149">If you are using a GPG key for code signing security, you may need to [associate your GPG key with your GitHub email](https://help.github.com/en/github/authenticating-to-github/associating-an-email-with-your-gpg-key).</span></span>

## <a name="adding-a-git-ignore-file"></a><span data-ttu-id="f6fbb-150">Git Ignore ファイルの追加</span><span class="sxs-lookup"><span data-stu-id="f6fbb-150">Adding a Git Ignore file</span></span>

<span data-ttu-id="f6fbb-151">プロジェクトには、ファイルを追加することをお勧め [します](https://help.github.com/en/articles/ignoring-files) 。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-151">We recommend adding a [.gitignore file](https://help.github.com/en/articles/ignoring-files) to your projects.</span></span> <span data-ttu-id="f6fbb-152">GitHub では、使用事例に従って整理されたファイル設定を使用して [、便利なテンプレートのコレクションを](https://github.com/github/gitignore) 提供しています。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-152">GitHub offers [a collection of useful .gitignore templates](https://github.com/github/gitignore) with recommended .gitignore file setups organized according to your use-case.</span></span> <span data-ttu-id="f6fbb-153">たとえば、 [Node.js プロジェクトの GitHub の既定の gitemplate テンプレート](https://github.com/github/gitignore/blob/master/Node.gitignore)は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-153">For example, here is [GitHub's default gitignore template for a Node.js project](https://github.com/github/gitignore/blob/master/Node.gitignore).</span></span>

<span data-ttu-id="f6fbb-154">[Github web サイトを使用して新しいリポジトリを作成](https://help.github.com/articles/create-a-repo)することを選択した場合は、README ファイルを使用してリポジトリを初期化するためのチェックボックスがあります。特定のプロジェクトの種類に対してファイルがセットアップされ、必要に応じてライセンスを追加するためのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-154">If you choose to [create a new repo using the GitHub website](https://help.github.com/articles/create-a-repo), there are check boxes available to initialize your repo with a README file, .gitignore file set up for your specific project type, and options to add a license if you need one.</span></span>

## <a name="git-and-vs-code"></a><span data-ttu-id="f6fbb-155">Git と VS Code</span><span class="sxs-lookup"><span data-stu-id="f6fbb-155">Git and VS Code</span></span>

<span data-ttu-id="f6fbb-156">Visual Studio Code には、Git のサポートが組み込まれています。これには、変更内容を表示し、さまざまな git コマンドを処理するソース管理タブが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-156">Visual Studio Code comes with built-in support for Git, including a source control tab that will show your changes and handle a variety of git commands for you.</span></span> <span data-ttu-id="f6fbb-157">[VS Code の Git サポートの](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support)詳細については、こちらをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-157">Learn more about [VS Code's Git support](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support).</span></span>

## <a name="git-line-endings"></a><span data-ttu-id="f6fbb-158">Git の行の終わり</span><span class="sxs-lookup"><span data-stu-id="f6fbb-158">Git line endings</span></span>

<span data-ttu-id="f6fbb-159">Windows、WSL、またはコンテナー間で同じリポジトリフォルダーを使用している場合は、一貫性のある行の終わりを設定してください。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-159">If you are working with the same repository folder between Windows, WSL, or a container, be sure to set up consistent line endings.</span></span>

<span data-ttu-id="f6fbb-160">Windows と Linux では異なる既定の行の終わりが使用されるため、Git では、変更されたファイルのうち、行の終わりとは異なるものが多数報告される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-160">Since Windows and Linux use different default line endings, Git may report a large number of modified files that have no differences aside from their line endings.</span></span> <span data-ttu-id="f6fbb-161">これが行われないようにするには、ファイルを使用する `.gitattributes` か、Windows 側でグローバルに行の終了変換を無効にします。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-161">To prevent this from happening, you can disable line ending conversion using a `.gitattributes` file or globally on the Windows side.</span></span> <span data-ttu-id="f6fbb-162">Git の [行の終了問題の解決について](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files)は、この VS Code のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6fbb-162">See this [VS Code doc about resolving Git line ending issues](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6fbb-163">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f6fbb-163">Additional resources</span></span>

* [<span data-ttu-id="f6fbb-164">WSL & VS Code</span><span class="sxs-lookup"><span data-stu-id="f6fbb-164">WSL & VS Code</span></span>](./wsl-vscode.md)
* [<span data-ttu-id="f6fbb-165">GitHub の学習ラボ: オンラインコース</span><span class="sxs-lookup"><span data-stu-id="f6fbb-165">GitHub Learning Lab: Online courses</span></span>](https://lab.github.com/)
* [<span data-ttu-id="f6fbb-166">Git 視覚化ツール</span><span class="sxs-lookup"><span data-stu-id="f6fbb-166">Git Visualization Tool</span></span>](http://git-school.github.io/visualizing-git/)
* [<span data-ttu-id="f6fbb-167">Git ツール-資格情報の保存</span><span class="sxs-lookup"><span data-stu-id="f6fbb-167">Git Tools - Credential Storage</span></span>](https://git-scm.com/book/it/v2/Git-Tools-Credential-Storage)
