---
title: エンタープライズ向け Windows Subsystem for Linux
description: エンタープライズ環境で Linux 用 Windows サブシステムを最適に使用する方法に関するリソースと手順。
keywords: BashOnWindows, bash, wsl, windows, linux 用 windows サブシステム, windowssubsystem, ubuntu, debian, suse, windows 10, エンタープライズ, デプロイ, オフライン, パッケージング, ストア, ディストリビューション, インストール, インストール
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 02f4ff41614f78c0e588f329c777a87f8b416233
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235829"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a><span data-ttu-id="9b028-104">エンタープライズ企業向けに Linux 用 Windows サブシステムを設定する</span><span class="sxs-lookup"><span data-stu-id="9b028-104">Set up Windows Subsystem for Linux for your enterprise company</span></span>

<span data-ttu-id="9b028-105">ビジネス向け Microsoft Store では、自社に WSL をデプロイすることを検討している企業に対してさまざまなソリューションを提供しています。</span><span class="sxs-lookup"><span data-stu-id="9b028-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="9b028-106">[ビジネスおよび教育機関向け Microsoft Store のドキュメント](https://docs.microsoft.com/microsoft-store/)は、Store のエクスペリエンスに関する一般的な情報を見つけるための優れたリソースです。</span><span class="sxs-lookup"><span data-stu-id="9b028-106">The [Microsoft Store for Business and Education docs](https://docs.microsoft.com/microsoft-store/) are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="9b028-107">WSL のデプロイを開始する準備の方法を調べている企業のお客様は、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="9b028-107">If you're a company that's just looking to get set up to start deploying WSL, follow these steps:</span></span>

* [<span data-ttu-id="9b028-108">ビジネス向け Microsoft Store にサインアップして開始します</span><span class="sxs-lookup"><span data-stu-id="9b028-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="9b028-109">[対象の製品とサービスを管理します (たとえば、どのユーザーがプライベート ストア内のどのアプリにアクセスできるか)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview)。</span><span class="sxs-lookup"><span data-stu-id="9b028-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="9b028-110">ここでは、WSL ディストリビューションをストアに追加したり、それらをインストールできるユーザーを制御したりできます</span><span class="sxs-lookup"><span data-stu-id="9b028-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="9b028-111">任意の配布方法を使用して、ソフトウェアを会社にデプロイします</span><span class="sxs-lookup"><span data-stu-id="9b028-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="9b028-112">このドキュメント リンクを使用して WSL をインストールできることを会社の従業員に伝えます: [Linux 用 Windows サブシステムのインストール](./install-win10.md)</span><span class="sxs-lookup"><span data-stu-id="9b028-112">Communicate to the employees of your company that they can use this documentation link to install WSL: [Install the Windows Subsystem for Linux](./install-win10.md)</span></span>

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a><span data-ttu-id="9b028-113">Windows 上で Linux ディストリビューションをオフラインで配布する方法</span><span class="sxs-lookup"><span data-stu-id="9b028-113">How to distribute a Linux distribution on Windows offline</span></span>

<span data-ttu-id="9b028-114">社内のコンピューターから Microsoft Store またはビジネス向け Microsoft Store にアクセスできない場合は、次の手順に従って、オフライン ライセンスが与えられた Linux ディストリビューションのインストーラーをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="9b028-114">If the computers in your company don't have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distribution that has an offline license by following these steps.</span></span>

### <a name="set-up-an-azure-active-directory-account"></a><span data-ttu-id="9b028-115">Azure Active Directory アカウントを設定する</span><span class="sxs-lookup"><span data-stu-id="9b028-115">Set up an Azure Active Directory account</span></span>

<span data-ttu-id="9b028-116">Microsoft Store アプリのインストーラーを入手するには、[Azure AD アカウントにサインアップ](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner)する必要があり、組織のグローバル管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b028-116">You need to [sign up for an Azure AD account](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="9b028-117">既にアカウントがある場合は、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="9b028-117">If you already have an account, you can skip this step.</span></span>

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a><span data-ttu-id="9b028-118">ビジネス向け Microsoft Store アカウントを使用して WSL を設定する</span><span class="sxs-lookup"><span data-stu-id="9b028-118">Set up WSL using your Microsoft Store for Business account</span></span>

<span data-ttu-id="9b028-119">アカウントを登録する手順については、以下を参照してください: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="9b028-119">The instructions to register an account are found here: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span></span>

1. <span data-ttu-id="9b028-120">ビジネス向け Store にサインインし、ホームページに移動します: https://www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="9b028-120">Sign into the Store for Business and go to the homepage: https://www.microsoft.com/business-store</span></span>

    ![ビジネス向け MS Store のホーム ページ](media/offlineinstallscreens/1-screen.png)

2. <span data-ttu-id="9b028-122">[管理] > [設定] に移動し、[Show offline apps]\(オフライン アプリを表示\) を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9b028-122">Go to Manage > Settings and enable 'Show offline apps'.</span></span>

    ![ビジネス向け MS Store の [設定] ページ](media/offlineinstallscreens/2-screen.png)

3. <span data-ttu-id="9b028-124">[Shop for my group]\(自分のグループ用に購入\) を選択して、メイン ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="9b028-124">Go back to the main page by selecting 'Shop for my group'.</span></span>

    ![ビジネス向け MS Store のホーム ページ](media/offlineinstallscreens/1-screen.png)

4. <span data-ttu-id="9b028-126">目的のディストリビューションを検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="9b028-126">Search for your desired distribution and select it.</span></span>

    ![ビジネス向け MS Store の検索がアクティブなホーム ページ](media/offlineinstallscreens/3-screen.png)

5. <span data-ttu-id="9b028-128">[ライセンスの種類] ドロップダウン メニューで [オフライン] ライセンスを選択し、[Get the app]\(アプリを入手\) を選択します</span><span class="sxs-lookup"><span data-stu-id="9b028-128">Select an 'Offline' license in the License type dropdown menu and select 'Get the app'.</span></span> <span data-ttu-id="9b028-129">(一部の Linux ディストリビューションでは、オフライン ライセンスが提供されない場合があります)。</span><span class="sxs-lookup"><span data-stu-id="9b028-129">(Some Linux distributions may elect not to provide an offline license).</span></span>

    ![ビジネス向け MS Store の Ubuntu の製品ページ](media/offlineinstallscreens/4-screen.png)

6. <span data-ttu-id="9b028-131">[管理] ボタンを選択して、アプリの製品ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="9b028-131">Select the 'Manage' button to get to the app's product page.</span></span>

    ![ビジネス向け MS Store の Ubuntu の製品ページ](media/offlineinstallscreens/5-screen.png)

7. <span data-ttu-id="9b028-133">対象のアーキテクチャを選択し、オフラインで使用するためにパッケージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="9b028-133">Select your architecture and download the package for offline use.</span></span>

    ![ビジネス向け MS Store の Ubuntu の製品詳細ページ](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="9b028-135">このインストーラーは、WSL をインストールする任意のコンピューターに配布できます。</span><span class="sxs-lookup"><span data-stu-id="9b028-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>
