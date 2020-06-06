---
title: Windows Subsystem for Linux で VS Code の使用を開始する
description: Windows Subsystem for Linux を使用してコードを作成およびデバッグするための VS Code を設定する方法について説明します。
keywords: wsl、windows、windowssubsystem、gnu、linux、bash、vs code、remote extension、debug、path、visual studio
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 416862201094ba28474918dca8e7d9ce316844cc
ms.sourcegitcommit: d95bdbc2fea991ba14a4c9ec53ee0ec19d6bbdb4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2020
ms.locfileid: "84457784"
---
# <a name="get-started-using-visual-studio-code-with-windows-subsystem-for-linux"></a><span data-ttu-id="4cd33-104">Windows Subsystem for Linux で Visual Studio Code の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="4cd33-104">Get started using Visual Studio Code with Windows Subsystem for Linux</span></span>

<span data-ttu-id="4cd33-105">Visual Studio Code をリモート WSL 拡張機能と共に使用すると、WSL を完全な開発環境として VS Code から直接使用できます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-105">Visual Studio Code, along with the Remote - WSL extension, enables you to use WSL as your full-time development environment directly from VS Code.</span></span> <span data-ttu-id="4cd33-106">次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="4cd33-106">You can:</span></span>

* <span data-ttu-id="4cd33-107">Linux ベースの環境での開発</span><span class="sxs-lookup"><span data-stu-id="4cd33-107">develop in a Linux-based environment</span></span>
* <span data-ttu-id="4cd33-108">Linux 固有のツールチェーンとユーティリティを使用する</span><span class="sxs-lookup"><span data-stu-id="4cd33-108">use Linux-specific toolchains and utilities</span></span>
* <span data-ttu-id="4cd33-109">Outlook や Office などの生産性向上ツールへのアクセスを維持しながら、Windows の快適さを利用して Linux ベースのアプリケーションを実行およびデバッグする</span><span class="sxs-lookup"><span data-stu-id="4cd33-109">run and debug your Linux-based applications from the comfort of Windows while maintaining access to productivity tools like Outlook and Office</span></span>
* <span data-ttu-id="4cd33-110">VS Code 組み込みターミナルを使用して、選択した Linux ディストリビューションを実行します。</span><span class="sxs-lookup"><span data-stu-id="4cd33-110">use the VS Code built-in terminal to run your Linux distribution of choice</span></span>
* <span data-ttu-id="4cd33-111">[Intellisense コード補完](https://code.visualstudio.com/docs/editor/intellisense) [、インライン処理、](https://code.visualstudio.com/docs/python/linting)[デバッグサポート](https://code.visualstudio.com/docs/nodejs/nodejs-debugging)、[コードスニペット](https://code.visualstudio.com/docs/editor/userdefinedsnippets)、[単体テスト](https://code.visualstudio.com/docs/python/testing)などの VS Code 機能を活用する</span><span class="sxs-lookup"><span data-stu-id="4cd33-111">take advantage of VS Code features like [Intellisense code completion](https://code.visualstudio.com/docs/editor/intellisense), [linting](https://code.visualstudio.com/docs/python/linting), [debug support](https://code.visualstudio.com/docs/nodejs/nodejs-debugging), [code snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets), and [unit testing](https://code.visualstudio.com/docs/python/testing)</span></span>
* <span data-ttu-id="4cd33-112">VS Code の組み込みの[Git サポート](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support)を使用して、バージョン管理を簡単に管理</span><span class="sxs-lookup"><span data-stu-id="4cd33-112">easily manage your version control with VS Code's built-in [Git support](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support)</span></span>
* <span data-ttu-id="4cd33-113">WSL プロジェクトでコマンドと拡張機能を直接実行する VS Code</span><span class="sxs-lookup"><span data-stu-id="4cd33-113">run commands and VS Code extensions directly on your WSL projects</span></span>
* <span data-ttu-id="4cd33-114">パスの問題、バイナリの互換性、またはその他の OS 間の課題を気にせずに、Linux またはマウントされた Windows ファイルシステム (/mnt/c など) のファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="4cd33-114">edit files in your Linux or mounted Windows filesystem (for example /mnt/c) without worrying about pathing issues, binary compatibility, or other cross-OS challenges</span></span>

## <a name="install-vs-code-and-the-remote-wsl-extension"></a><span data-ttu-id="4cd33-115">VS Code とリモート WSL 拡張機能をインストールする</span><span class="sxs-lookup"><span data-stu-id="4cd33-115">Install VS Code and the Remote WSL extension</span></span>

* <span data-ttu-id="4cd33-116">[VS Code インストールページ](https://code.visualstudio.com/download)にアクセスし、32または64ビットインストーラーを選択します。</span><span class="sxs-lookup"><span data-stu-id="4cd33-116">Visit the [VS Code install page](https://code.visualstudio.com/download) and select the 32 or 64 bit installer.</span></span> <span data-ttu-id="4cd33-117">(WSL ファイルシステムではなく) Windows に Visual Studio Code をインストールします。</span><span class="sxs-lookup"><span data-stu-id="4cd33-117">Install Visual Studio Code on Windows (not in your WSL file system).</span></span>

* <span data-ttu-id="4cd33-118">インストール中に**追加のタスクを選択**するように求めるメッセージが表示されたら、[**パスの追加**] オプションをオンにして、wsl 内のフォルダーをコードコマンドで簡単に開くことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="4cd33-118">When prompted to **Select Additional Tasks** during installation, be sure to check the **Add to PATH** option so you can easily open a folder in WSL using the code command.</span></span>

* <span data-ttu-id="4cd33-119">[リモート開発拡張機能パック](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)をインストールします。</span><span class="sxs-lookup"><span data-stu-id="4cd33-119">Install the [Remote Development extension pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack).</span></span> <span data-ttu-id="4cd33-120">この拡張パックには、リモート SSH およびリモートコンテナーの拡張機能に加えて、リモートの WSL 拡張機能が含まれており、コンテナー、リモートコンピューター、または WSL で任意のフォルダーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-120">This extension pack includes the Remote - WSL extension, in addition to the Remote - SSH, and Remote - Containers extensions, enabling you to open any folder in a container, on a remote machine, or in WSL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cd33-121">リモート WSL 拡張機能をインストールするには、VS Code の[1.35 リリース](https://code.visualstudio.com/updates/v1_35)バージョン以降が必要になります。</span><span class="sxs-lookup"><span data-stu-id="4cd33-121">In order to install the Remote-WSL extension, you will need the [1.35 May release](https://code.visualstudio.com/updates/v1_35) version or later of VS Code.</span></span> <span data-ttu-id="4cd33-122">リモート WSL 拡張機能を使用せずに VS Code で WSL を使用することはお勧めしません。オートコンプリート、デバッグ、インライン処理などのサポートが失われるためです。楽しい事実: この WSL 拡張機能は $HOME/.vscode-server/extensions. にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-122">We do not recommend using WSL in VS Code without the Remote-WSL extension as you will lose support for auto-complete, debugging, linting, etc. Fun fact: this WSL extension is installed in $HOME/.vscode-server/extensions.</span></span>

## <a name="update-your-linux-distribution"></a><span data-ttu-id="4cd33-123">Linux ディストリビューションを更新する</span><span class="sxs-lookup"><span data-stu-id="4cd33-123">Update your Linux distribution</span></span>

<span data-ttu-id="4cd33-124">一部の WSL Linux ディストリビューションでは、VS Code サーバーが起動するために必要なライブラリが不足しています。</span><span class="sxs-lookup"><span data-stu-id="4cd33-124">Some WSL Linux distributions are lacking libraries that are required by the VS Code server to start up.</span></span> <span data-ttu-id="4cd33-125">パッケージマネージャーを使用して、Linux ディストリビューションに追加のライブラリを追加できます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-125">You can add additional libraries into your Linux distribution by using its package manager.</span></span>

<span data-ttu-id="4cd33-126">たとえば、Debian または Ubuntu を更新するには、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4cd33-126">For example, to update Debian or Ubuntu, use:</span></span>

```bash
sudo apt-get update
```

<span data-ttu-id="4cd33-127">Wget (web サーバーからコンテンツを取得するため) および ca 証明書を追加するには (SSL ベースのアプリケーションが SSL 接続の信頼性を確認できるようにするため)、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="4cd33-127">To add wget (to retrieve content from web servers) and ca-certificates (to allow SSL-based applications to check for the authenticity of SSL connections), enter:</span></span>

```bash
sudo apt-get install wget ca-certificates
```

## <a name="open-a-wsl-project-in-visual-studio-code"></a><span data-ttu-id="4cd33-128">Visual Studio Code で WSL プロジェクトを開く</span><span class="sxs-lookup"><span data-stu-id="4cd33-128">Open a WSL project in Visual Studio Code</span></span>

### <a name="from-the-command-line"></a><span data-ttu-id="4cd33-129">コマンドラインから</span><span class="sxs-lookup"><span data-stu-id="4cd33-129">From the command-line</span></span>

<span data-ttu-id="4cd33-130">WSL ディストリビューションからプロジェクトを開くには、ディストリビューションのコマンドラインを開き、次のように入力します。`code .`</span><span class="sxs-lookup"><span data-stu-id="4cd33-130">To open a project from your WSL distribution, open the distribution's command line and enter: `code .`</span></span>

![VS Code リモートサーバーで WSL プロジェクトを開く](../media/wsl-open-vs-code.gif)

### <a name="from-vs-code"></a><span data-ttu-id="4cd33-132">VS Code から</span><span class="sxs-lookup"><span data-stu-id="4cd33-132">From VS Code</span></span>

<span data-ttu-id="4cd33-133">コマンドパレットを表示するには、ショートカット: VS Code を使用して、VS Code リモートオプションにアクセスすることもできます。 `CTRL+SHIFT+P`</span><span class="sxs-lookup"><span data-stu-id="4cd33-133">You can also access more VS Code Remote options by using the shortcut: `CTRL+SHIFT+P` in VS Code to bring up the command palette.</span></span> <span data-ttu-id="4cd33-134">入力すると、[ `VSCODE-REMOTE` VS Code のリモートオプションがすべて表示されます。これにより、リモートセッションでフォルダーを再度開き、開く配布を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-134">If you then type `VSCODE-REMOTE` you will see all of the VS Code Remote options available, allowing you to reopen the folder in a remote session, specify which distribution you want to open in, and more.</span></span>

![VS Code のコマンドパレット](../media/vscode-remote-command-palette.png)

## <a name="extensions-inside-of-vs-code-remote"></a><span data-ttu-id="4cd33-136">VS Code リモート内の拡張機能</span><span class="sxs-lookup"><span data-stu-id="4cd33-136">Extensions inside of VS Code Remote</span></span>

<span data-ttu-id="4cd33-137">リモート WSL 拡張機能は、VS Code を "クライアント/サーバー" アーキテクチャに分割します。このアーキテクチャでは、Windows コンピューター上で実行されているクライアント (ユーザーインターフェイス) と、リモートで実行されているサーバー (コード、Git、プラグインなど) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-137">The Remote-WSL extension splits VS Code into a “client-server” architecture, with the client (the user interface) running on your Windows machine and the server (your code, Git, plugins, etc) running remotely.</span></span>

<span data-ttu-id="4cd33-138">VS Code リモートで実行しているときに、[拡張機能] タブを選択すると、ローカルコンピューターと WSL 分散の間に分割された拡張機能の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-138">When running VS Code Remote, selecting the 'Extensions' tab will display a list of extensions split between your local machine and your WSL distribution.</span></span>

<span data-ttu-id="4cd33-139">[テーマ](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs)などのローカル拡張機能のインストールは、1回だけインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cd33-139">Installing a local extension, like a [theme](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs),  only needs to be installed once.</span></span>

<span data-ttu-id="4cd33-140">[Python 拡張](https://marketplace.visualstudio.com/items?itemName=ms-python.python)機能などの一部の拡張機能や、lint デバッグなどを処理するものは、リモートの wsl ディストリビューションごとに個別にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cd33-140">Some extensions, like the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) or anything that handles things like linting or debugging, must be installed separately on each remote WSL distributions.</span></span> <span data-ttu-id="4cd33-141">WSL リモートにインストールされていない拡張機能がローカルにインストールされている場合は、VS Code によって、警告アイコンと ⚠ 緑色の [wsl にインストール] ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-141">VS Code will display a warning icon ⚠, along with a green "Install in WSL" button, if you have an extension locally installed that is not installed on your WSL Remote.</span></span>

![リモート WSL 拡張機能とローカル拡張機能の VS Code](../media/vscode-remote-wsl-extensions.png)

<span data-ttu-id="4cd33-143">詳細については、VS Code のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cd33-143">For further information, see the VS Code docs:</span></span>

* <span data-ttu-id="4cd33-144">WSL で VS Code リモートが開始されると、シェルスタートアップスクリプトは実行されません。</span><span class="sxs-lookup"><span data-stu-id="4cd33-144">When VS Code Remote is started in WSL, no shell startup scripts are run.</span></span> <span data-ttu-id="4cd33-145">追加のコマンドを実行する方法、または環境を変更する方法の詳細については、この[高度な環境セットアップスクリプト](https://code.visualstudio.com/docs/remote/wsl#_advanced-environment-setup-script)に関する記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cd33-145">See this [advanced environment setup script article](https://code.visualstudio.com/docs/remote/wsl#_advanced-environment-setup-script) for more info on how to run additional commands or modify the environment.</span></span>

* <span data-ttu-id="4cd33-146">WSL コマンドラインから VS Code を起動するときに問題が発生する場合は、</span><span class="sxs-lookup"><span data-stu-id="4cd33-146">Having problems launching VS Code from your WSL command line?</span></span> <span data-ttu-id="4cd33-147">この[トラブルシューティングガイド](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-problems-with-the-code-command-not-working)には、パス変数の変更、依存関係の欠落に関する拡張機能のエラーの解決、Git 行の終了に関する問題の解決、リモートコンピューターへのローカル VSIX のインストール、ブラウザーウィンドウの起動、ブロック localhost ポート、web ソケットの起動、拡張データの格納エラーなどに関するヒントが記載されています。</span><span class="sxs-lookup"><span data-stu-id="4cd33-147">This [troubleshooting guide](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-problems-with-the-code-command-not-working) includes tips on changing path variables, resolving extension errors about missing dependencies, resolving Git line ending issues, installing a local VSIX on a remote machine, launching a browser window, blocker localhost port, web sockets not working, errors storing extension data, and more.</span></span>

## <a name="install-git-optional"></a><span data-ttu-id="4cd33-148">Git のインストール (省略可能)</span><span class="sxs-lookup"><span data-stu-id="4cd33-148">Install Git (optional)</span></span>

<span data-ttu-id="4cd33-149">共同作業で開発する場合や、(GitHub のような) オープンソース サイトでプロジェクトをホストする場合のために、VS Code では [Git によるバージョン管理](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support)がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4cd33-149">If you plan to collaborate with others, or host your project on an open-source site (like GitHub), VS Code supports [version control with Git](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support).</span></span> <span data-ttu-id="4cd33-150">VS Code の [ソース管理] タブでは、すべての変更が追跡され、一般的な Git コマンド (追加、コミット、プッシュ、プル) が UI に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="4cd33-150">The Source Control tab in VS Code tracks all of your changes and has common Git commands (add, commit, push, pull) built right into the UI.</span></span>

<span data-ttu-id="4cd33-151">Git をインストールするには、「 [Windows Subsystem For Linux で動作するように git を設定する](./wsl-git.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cd33-151">To install Git, see [set up Git to work with Windows Subsystem for Linux](./wsl-git.md).</span></span>

## <a name="install-windows-terminal-optional"></a><span data-ttu-id="4cd33-152">Windows ターミナルをインストールする (省略可能)</span><span class="sxs-lookup"><span data-stu-id="4cd33-152">Install Windows Terminal (optional)</span></span>

<span data-ttu-id="4cd33-153">新しい Windows ターミナルでは、複数のタブが有効になり (コマンドプロンプト、PowerShell、または複数の Linux ディストリビューションをすばやく切り替えることができます)、カスタムキーバインド (タブを開いたり閉じたりするための独自のショートカットキーを作成する、コピーと貼り付けなど)、絵文字☺、カスタムテーマ (配色、フォントスタイルとサイズ、背景画像、</span><span class="sxs-lookup"><span data-stu-id="4cd33-153">The new Windows Terminal enables multiple tabs (quickly switch between Command Prompt, PowerShell, or multiple Linux distributions), custom key bindings (create your own shortcut keys for opening or closing tabs, copy+paste, etc.), emojis ☺, and custom themes (color schemes, font styles and sizes, background image/blur/transparency).</span></span> <span data-ttu-id="4cd33-154">詳細については、 [Windows ターミナルのドキュメント](https://docs.microsoft.com/windows/terminal)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4cd33-154">Learn more in the [Windows Terminal docs](https://docs.microsoft.com/windows/terminal).</span></span>

1. <span data-ttu-id="4cd33-155">[Microsoft Store で Windows ターミナル](https://www.microsoft.com/store/apps/9n0dx20hk701)を取得する: ストアを使用してをインストールすることにより、更新プログラムは自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-155">Get [Windows Terminal in the Microsoft Store](https://www.microsoft.com/store/apps/9n0dx20hk701): By installing via the store, updates are handled automatically.</span></span>

2. <span data-ttu-id="4cd33-156">インストールが完了したら、Windows ターミナルを開き、 **[設定]** を選択して、`profile.json` ファイルによってターミナルをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="4cd33-156">Once installed, open Windows Terminal and select **Settings** to customize your terminal using the `profile.json` file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4cd33-157">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="4cd33-157">Additional Resources</span></span>

* [<span data-ttu-id="4cd33-158">リモート開発の VS Code</span><span class="sxs-lookup"><span data-stu-id="4cd33-158">VS Code Remote Development</span></span>](https://code.visualstudio.com/docs/remote/remote-overview)
* [<span data-ttu-id="4cd33-159">リモート開発のヒントとテクニック</span><span class="sxs-lookup"><span data-stu-id="4cd33-159">Remote development tips and tricks</span></span>](https://code.visualstudio.com/docs/remote/troubleshooting)
* [<span data-ttu-id="4cd33-160">WSL を使用したリモート開発のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="4cd33-160">Remote development with WSL tutorial</span></span>](https://code.visualstudio.com/remote-tutorials/wsl/getting-started)
* [<span data-ttu-id="4cd33-161">WSL 2 および VS Code での Docker の使用</span><span class="sxs-lookup"><span data-stu-id="4cd33-161">Using Docker with WSL 2 and VS Code</span></span>](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
* [<span data-ttu-id="4cd33-162">VS Code での C++ と WSL の使用</span><span class="sxs-lookup"><span data-stu-id="4cd33-162">Using C++ and WSL in VS Code</span></span>](https://code.visualstudio.com/docs/cpp/config-wsl)
* [<span data-ttu-id="4cd33-163">Linux 用のリモート R サービス</span><span class="sxs-lookup"><span data-stu-id="4cd33-163">Remote R Service for Linux</span></span>](https://docs.microsoft.com/visualstudio/rtvs/setting-up-remote-r-service-on-linux?view=vs-2017)

<span data-ttu-id="4cd33-164">他にも検討をお勧めする拡張機能として、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="4cd33-164">A few additional extensions you may want to consider include:</span></span>

* <span data-ttu-id="4cd33-165">[他のエディターからのキーマップ](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads): これらの拡張機能は、別のテキスト エディター (Atom、Sublime、Vim、eMacs、Notepad++ など) から移行する場合に、ご利用の環境を快適に保つのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-165">[Keymaps from other editors](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads): These extensions can help your environment feel right at home if you're transitioning from another text editor (like Atom, Sublime, Vim, eMacs, Notepad++, etc).</span></span>
* <span data-ttu-id="4cd33-166">[設定の同期](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync): GitHub を使用して、異なるインストール間で VS Code の設定を同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-166">[Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync): Enables you to synchronize your VS Code settings across different installations using GitHub.</span></span> <span data-ttu-id="4cd33-167">複数のコンピューターで作業する場合、この機能によってコンピューター間で環境の一貫性を保つことができます。</span><span class="sxs-lookup"><span data-stu-id="4cd33-167">If you work on different machines, this helps keep your environment consistent across them.</span></span>
* <span data-ttu-id="4cd33-168">[Chrome のデバッガー](https://code.visualstudio.com/blogs/2016/02/23/introducing-chrome-debugger-for-vs-code): Linux でサーバー側で開発を完了したら、クライアント側を開発してテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cd33-168">[Debugger for Chrome](https://code.visualstudio.com/blogs/2016/02/23/introducing-chrome-debugger-for-vs-code): Once you finish developing on the server side with Linux, you'll need to develop and test the client side.</span></span> <span data-ttu-id="4cd33-169">この拡張機能により、ご利用の VS Code エディターと Chrome ブラウザーのデバッグ サービスが統合され、効率がより向上します。</span><span class="sxs-lookup"><span data-stu-id="4cd33-169">This extension integrates your VS Code editor with your Chrome browser debugging service, making things a bit more efficient.</span></span>
