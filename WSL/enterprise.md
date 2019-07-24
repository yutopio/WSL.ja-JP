---
title: エンタープライズ向け Windows Subsystem for Linux
description: エンタープライズ環境で Windows Subsystem for Linux を最適に使用する方法に関するリソースと手順です。
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu、debian、suse、windows 10、enterprise、deployment、offline、パッケージング、ストア、ディストリビューション、インストール、インストール
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "59063280"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>エンタープライズ向け Windows Subsystem for Linux

ビジネス向け Microsoft Store は、WSL を会社に展開する企業に対してさまざまなソリューションを提供します。 ビジネス向け Microsoft Store の[オンラインドキュメント](https://docs.microsoft.com/en-us/microsoft-store/)は、ストアエクスペリエンスに関する一般的な情報を確認するための優れたリソースです。

WSL のデプロイを開始するように設定しようとしている企業の場合は、次の手順に従ってください。 Microsoft Store のドキュメントで説明されています。

* [ビジネス向け Microsoft Store にサインアップして開始する](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [(プライベートストア内のどのアプリにアクセスできるかを含む) 製品とサービスを管理](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)します。 ここでは、WSL ディストリビューションをストアに追加し、それらをインストールできるユーザーを制御できます。
* [任意の配布方法を使用してソフトウェアを会社に展開する](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* WSL ディストリビューションにアクセスできるユーザーと通信します。[これらの手順を使用](https://docs.microsoft.com/en-us/windows/wsl/install-win10)して、選択したディストリビューションまたはディストリビューションをインストールすることができます。 

## <a name="how-to-distribute-a-distro-offline"></a>ディストリビューションをオフラインで配布する方法

社内のコンピューターが Microsoft Store または Microsoft Store for Business にアクセスできない場合は、次の手順に従って、オフラインライセンスを持つ Linux ディストリビューションのインストーラーをダウンロードできます。 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Azure Active Directory (AD) アカウントを設定する 

Microsoft Store アプリのインストーラーを取得するには、Azure AD アカウントが必要であり、組織のグローバル管理者である必要があります。 アカウントを既に持っている場合は、この手順を省略できます。

アカウントを登録する手順については、次を参照してください。 https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>ビジネス向けストアにサインインし、ホームページにアクセスします
ここでサインイン: www.microsoft.com/business-store

![ビジネス向け MS ストアのホームページ](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>管理-> 設定にアクセスして、[オフラインアプリの表示] を有効にします

![[ビジネス向け MS ストアの設定] ページ](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>メインページに戻るには、[グループの購入] をクリックしてください。

![ビジネス向け MS ストアのホームページ](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>目的のディストリビューションを検索して選択します

![アクティブな検索を使用したビジネス向け MS ストアのホームページ](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>[ライセンスの種類] ドロップダウンメニューで [オフライン] ライセンスを選択し、[アプリの取得] をクリックします。

![ビジネス向け MS ストアの Ubuntu 製品ページ](media/offlineinstallscreens/4-screen.png)

注意: 一部のディストリビューションではオフラインライセンスを使用しないことを選択できます

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>[管理] ボタンをクリックして、アプリの製品ページにアクセスします

![ビジネス向け MS ストアの Ubuntu 製品ページ](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>アーキテクチャを選択し、オフラインで使用するパッケージをダウンロードする

![ビジネス向け MS ストアの Ubuntu 製品の詳細ページ](media/offlineinstallscreens/6-screen.png)

このインストーラーは、WSL をインストールする任意のコンピューターに配布できます。