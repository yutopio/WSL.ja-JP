---
title: Windows Subsystem for Linux (WSL) ディストリビューションを手動でダウンロードする
description: Windows Subsystem for Linux ディストリビューションを手動でダウンロードする方法について説明します。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、WSL、windows subsystem、ディストリビューション、ubuntu、openSUSE、SLES、debian、kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 99215a3bccc3d0b07e8ed4b7629913af3765aec0
ms.sourcegitcommit: d35870009477813aa4c8fe4e401af4bddef4a47c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "72778823"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="3b838-104">Windows Subsystem for Linux ディストリビューションパッケージを手動でダウンロードする</span><span class="sxs-lookup"><span data-stu-id="3b838-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="3b838-105">Microsoft Store 経由で WSL Linux ディストリビューションをインストールすることはできない (または必要ない) シナリオがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="3b838-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="3b838-106">具体的には、Microsoft Store をサポートしていない Windows Server または長期的なサービス (LTSC) デスクトップ OS SKU を実行している可能性があります。また、環境内で Microsoft Store の使用を許可しないように企業ネットワークポリシーや管理者を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3b838-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="3b838-107">このような場合は、WSL 自体を利用できますが、ストアにアクセスできない場合は、WSL で Linux ディストリビューションをダウンロードしてインストールするにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="3b838-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="3b838-108">注:**コマンドラインシェル環境 (Cmd、PowerShell、Linux/WSL ディストリビューションを含む) は、Windows 10 S モードでの実行は許可されていません**。</span><span class="sxs-lookup"><span data-stu-id="3b838-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="3b838-109">この制限は、S モードで提供される整合性と安全性の目標を確保するために存在します。詳細については、[この投稿](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b838-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="3b838-110">ディストリビューションのダウンロード</span><span class="sxs-lookup"><span data-stu-id="3b838-110">Downloading distros</span></span>

<span data-ttu-id="3b838-111">Microsoft Store アプリが使用できない場合は、次のリンクをクリックして Linux ディストリビューションをダウンロードし、手動でインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b838-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="3b838-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="3b838-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="3b838-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="3b838-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="3b838-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="3b838-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="3b838-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="3b838-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="3b838-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="3b838-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="3b838-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="3b838-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="3b838-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="3b838-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="3b838-119">WSL のための Fedora リミックス</span><span class="sxs-lookup"><span data-stu-id="3b838-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="3b838-120">これにより、`<distro>.appx` パッケージが、選択したフォルダーにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="3b838-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="3b838-121">[インストール手順](#installing-your-distro)に従って、ダウンロードしたディストリビューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="3b838-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="3b838-122">コマンドラインを使用したディストリビューションのダウンロード</span><span class="sxs-lookup"><span data-stu-id="3b838-122">Downloading distros via the command line</span></span>
<span data-ttu-id="3b838-123">必要に応じて、コマンドラインを使用して、優先するディストリビューションをダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3b838-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="3b838-124">PowerShell を使用してダウンロードする</span><span class="sxs-lookup"><span data-stu-id="3b838-124">Download using PowerShell</span></span>
 <span data-ttu-id="3b838-125">PowerShell を使用してディストリビューションをダウンロードするには、 [-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest)コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b838-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="3b838-126">Ubuntu 16.04 をダウンロードするためのサンプル命令を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3b838-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="3b838-127">ダウンロードに時間がかかる場合は、を設定して進行状況バーをオフにし `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="3b838-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="3b838-128">Curl を使用してダウンロードする</span><span class="sxs-lookup"><span data-stu-id="3b838-128">Download using curl</span></span>
<span data-ttu-id="3b838-129">Windows 10 Spring 2018 Update (またはそれ以降) には、コマンドラインから web 要求 (HTTP GET、POST、PUT などのコマンド) を呼び出すことができる、一般的な[curl コマンドラインユーティリティ](https://curl.haxx.se/)が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3b838-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="3b838-130">@No__t_0 を使用すると、上記のディストリビューションをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="3b838-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="3b838-131">上の例では、(`curl` だけでなく) `curl.exe` が実行され、PowerShell によって実際の curl 実行可能ファイルが呼び出されます。これは、[呼び出し](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)の powershell curl エイリアスではありません。</span><span class="sxs-lookup"><span data-stu-id="3b838-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="3b838-132">注: `curl` を使用すると、Cmd シェルや `.bat`  /  `.cmd` スクリプトを使用してダウンロード手順を呼び出したりスクリプトを作成したりする必要がある場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="3b838-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="3b838-133">ディストリビューションのインストール</span><span class="sxs-lookup"><span data-stu-id="3b838-133">Installing your distro</span></span>
<span data-ttu-id="3b838-134">Windows 10 を使用している場合は、PowerShell を使用してディストリビューションをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="3b838-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="3b838-135">上記の手順でダウンロードしたディストリビューションが格納されているフォルダーに移動し、そのディレクトリで次のコマンドを実行します。 `app_name` は、ディストリビューションの .appx ファイル名です。</span><span class="sxs-lookup"><span data-stu-id="3b838-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="3b838-136">Windows server を使用している場合は、 [Windows server](install-on-server.md)のドキュメントページでインストール手順を確認できます。</span><span class="sxs-lookup"><span data-stu-id="3b838-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="3b838-137">ディストリビューションがインストールされたら、初期化の[手順](initialize-distro.md)ページを参照して、新しいディストリビューションを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3b838-137">Once your distro is installed please refer to the [Initialization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
