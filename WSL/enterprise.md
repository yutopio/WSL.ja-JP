---
title: エンタープライズ向け Windows Subsystem for Linux
description: リソースや、最善の方法については、Linux 用 Windows サブシステムを使用して、エンタープライズ環境でします。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10、enterprise、展開、オフラインでパッケージ化、ストア、配布、インストール用の windows サブシステムのインストールします。
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063280"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="1c8d2-104">エンタープライズ向け Windows Subsystem for Linux</span><span class="sxs-lookup"><span data-stu-id="1c8d2-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="1c8d2-105">ビジネス向け Microsoft Store では、自分の会社の WSL のデプロイを希望する企業までのさまざまなソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="1c8d2-106">[オンライン ドキュメント](https://docs.microsoft.com/en-us/microsoft-store/)ビジネス向け Microsoft Store は、ストアのエクスペリエンスに関する全般情報を調べるための優れたリソースです。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="1c8d2-107">設定だけを見て、企業の場合を WSL のデプロイを開始することができます次の手順に従って、Microsoft Store のドキュメントの内部で説明されています。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="1c8d2-108">ビジネス向け Microsoft Store にサインアップして開始します。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="1c8d2-109">[製品やサービス (プライベート ストアでアプリにアクセスできるユーザーを含む) を管理](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)します。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="1c8d2-110">ここでは、ストアにインストールできるユーザーを制御して WSL ディストリビューションを追加できます。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="1c8d2-111">任意の配布方法を使用して、ソフトウェア会社を展開するには</span><span class="sxs-lookup"><span data-stu-id="1c8d2-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="1c8d2-112">できる限り WSL ディストリビューションへのアクセスを持つユーザーとの通信[次の手順を使用して、](https://docs.microsoft.com/en-us/windows/wsl/install-win10)ディストリビューションまたは自分で選択したディストリビューションをインストールするには</span><span class="sxs-lookup"><span data-stu-id="1c8d2-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="1c8d2-113">ディストリビューションをオフラインに配布する方法</span><span class="sxs-lookup"><span data-stu-id="1c8d2-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="1c8d2-114">社内のコンピューターでは、ビジネス向け Microsoft Store または Microsoft Store へのアクセスを持っていない場合は、次の手順に従って、オフラインのライセンスを持つ Linux ディストリビューションのインストーラーをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="1c8d2-115">Azure Active Directory (AD) アカウントを設定します。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="1c8d2-116">Azure AD アカウントを持っており、Microsoft Store アプリのインストーラーを取得する、組織のグローバル管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="1c8d2-117">アカウントを既にある場合は、この手順をスキップすることができます。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="1c8d2-118">アカウントを登録する手順についてはここにあります。 https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="1c8d2-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="1c8d2-119">ビジネス向けストアにサインインし、ホーム ページに移動</span><span class="sxs-lookup"><span data-stu-id="1c8d2-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="1c8d2-120">ここでサインイン: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="1c8d2-120">Sign in here: www.microsoft.com/business-store</span></span>

![会社のホーム ページの MS ストア](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="1c8d2-122">管理に移動の設定-> およびオフライン アプリを表示する を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![MS ストア for business の設定 ページ](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="1c8d2-124">'自分のグループを探す' をクリックしてメイン ページに戻る</span><span class="sxs-lookup"><span data-stu-id="1c8d2-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![会社のホーム ページの MS ストア](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="1c8d2-126">必要なディストリビューションを検索して選択します</span><span class="sxs-lookup"><span data-stu-id="1c8d2-126">Search for your desired distro and select it</span></span>

![MS ストアのアクティブな検索とビジネスのホーム ページ](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="1c8d2-128">ライセンスの種類 ドロップダウン メニューで、オフライン ライセンスを選択し、'アプリを入手する をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![MS ストア for business の Ubuntu 製品 ページ](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="1c8d2-130">注: いくつかのディストリビューションがオフラインのライセンスを取得するには、しないことができます</span><span class="sxs-lookup"><span data-stu-id="1c8d2-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="1c8d2-131">アプリの製品ページに [管理] ボタンをクリックします</span><span class="sxs-lookup"><span data-stu-id="1c8d2-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![MS ストア for business の Ubuntu 製品 ページ](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="1c8d2-133">アーキテクチャを選択し、オフラインで使用するパッケージをダウンロード</span><span class="sxs-lookup"><span data-stu-id="1c8d2-133">Select your architecture and download the package for offline use</span></span>

![MS ストア for business Ubuntu 製品の詳細 ページ](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="1c8d2-135">このインストーラーは、WSL をインストールするには任意のコンピューターに配布できます。</span><span class="sxs-lookup"><span data-stu-id="1c8d2-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>