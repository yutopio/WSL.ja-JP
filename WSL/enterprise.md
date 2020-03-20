---
title: エンタープライズ向け Windows Subsystem for Linux
description: エンタープライズ環境で Windows Subsystem for Linux を最適に使用する方法に関するリソースと手順です。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10、enterprise、deployment、offline、パッケージング、ストア、ディストリビューション、インストール、インストール
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c32d62267c77d87fb200cfe43b8e6f43b4e3a56d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269859"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="8a06c-104">エンタープライズ向け Windows Subsystem for Linux</span><span class="sxs-lookup"><span data-stu-id="8a06c-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="8a06c-105">ビジネス向け Microsoft Store は、WSL を会社に展開する企業に対してさまざまなソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="8a06c-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="8a06c-106">ビジネス向け Microsoft Store の[オンラインドキュメント](https://docs.microsoft.com/en-us/microsoft-store/)は、ストアエクスペリエンスに関する一般的な情報を確認するための優れたリソースです。</span><span class="sxs-lookup"><span data-stu-id="8a06c-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="8a06c-107">WSL のデプロイを開始するように設定しようとしている企業の場合は、次の手順に従ってください。 Microsoft Store のドキュメントで説明されています。</span><span class="sxs-lookup"><span data-stu-id="8a06c-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="8a06c-108">ビジネス向け Microsoft Store にサインアップして開始する</span><span class="sxs-lookup"><span data-stu-id="8a06c-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="8a06c-109">[(プライベートストア内のどのアプリにアクセスできるかを含む) 製品とサービスを管理](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)します。</span><span class="sxs-lookup"><span data-stu-id="8a06c-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="8a06c-110">ここでは、WSL ディストリビューションをストアに追加し、それらをインストールできるユーザーを制御できます。</span><span class="sxs-lookup"><span data-stu-id="8a06c-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="8a06c-111">任意の配布方法を使用してソフトウェアを会社に展開する</span><span class="sxs-lookup"><span data-stu-id="8a06c-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="8a06c-112">WSL ディストリビューションにアクセスできるユーザーと通信します。[これらの手順を使用](https://docs.microsoft.com/en-us/windows/wsl/install-win10)して、選択したディストリビューションまたはディストリビューションをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="8a06c-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="8a06c-113">ディストリビューションをオフラインで配布する方法</span><span class="sxs-lookup"><span data-stu-id="8a06c-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="8a06c-114">社内のコンピューターが Microsoft Store または Microsoft Store for Business にアクセスできない場合は、次の手順に従って、オフラインライセンスを持つ Linux ディストリビューションのインストーラーをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="8a06c-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="8a06c-115">Azure Active Directory (AD) アカウントを設定する</span><span class="sxs-lookup"><span data-stu-id="8a06c-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="8a06c-116">Microsoft Store アプリのインストーラーを取得するには、Azure AD アカウントが必要であり、組織のグローバル管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a06c-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="8a06c-117">アカウントを既に持っている場合は、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="8a06c-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="8a06c-118">アカウントを登録する手順については、「」を参照してください https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="8a06c-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="8a06c-119">ビジネス向けストアにサインインし、ホームページにアクセスします</span><span class="sxs-lookup"><span data-stu-id="8a06c-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="8a06c-120">ここでサインイン: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="8a06c-120">Sign in here: www.microsoft.com/business-store</span></span>

![ビジネス向け MS ストアのホームページ](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="8a06c-122">管理-> 設定にアクセスして、[オフラインアプリの表示] を有効にします</span><span class="sxs-lookup"><span data-stu-id="8a06c-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![[ビジネス向け MS ストアの設定] ページ](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="8a06c-124">メインページに戻るには、[グループの購入] をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="8a06c-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![ビジネス向け MS ストアのホームページ](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="8a06c-126">目的のディストリビューションを検索して選択します</span><span class="sxs-lookup"><span data-stu-id="8a06c-126">Search for your desired distro and select it</span></span>

![アクティブな検索を使用したビジネス向け MS ストアのホームページ](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="8a06c-128">[ライセンスの種類] ドロップダウンメニューで [オフライン] ライセンスを選択し、[アプリの取得] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a06c-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![ビジネス向け MS ストアの Ubuntu 製品ページ](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="8a06c-130">注意: 一部のディストリビューションではオフラインライセンスを使用しないことを選択できます</span><span class="sxs-lookup"><span data-stu-id="8a06c-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="8a06c-131">[管理] ボタンをクリックして、アプリの製品ページにアクセスします</span><span class="sxs-lookup"><span data-stu-id="8a06c-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![ビジネス向け MS ストアの Ubuntu 製品ページ](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="8a06c-133">アーキテクチャを選択し、オフラインで使用するパッケージをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="8a06c-133">Select your architecture and download the package for offline use</span></span>

![ビジネス向け MS ストアの Ubuntu 製品の詳細ページ](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="8a06c-135">このインストーラーは、WSL をインストールする任意のコンピューターに配布できます。</span><span class="sxs-lookup"><span data-stu-id="8a06c-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>