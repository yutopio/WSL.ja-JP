---
title: Windows Subsystem for for Enterprise Linux
description: リソースや、最善の方法については、Linux 用 Windows サブシステムを使用して、エンタープライズ環境でします。
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu、debian、suse、windows 10、enterprise、展開、オフラインでパッケージ化、ストア、配布、インストール用の windows サブシステムのインストールします。
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063280"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Windows Subsystem for for Enterprise Linux

ビジネス向け Microsoft Store では、自分の会社の WSL のデプロイを希望する企業までのさまざまなソリューションを提供します。 [オンライン ドキュメント](https://docs.microsoft.com/en-us/microsoft-store/)ビジネス向け Microsoft Store は、ストアのエクスペリエンスに関する全般情報を調べるための優れたリソースです。

設定だけを見て、企業の場合を WSL のデプロイを開始することができます次の手順に従って、Microsoft Store のドキュメントの内部で説明されています。

* [ビジネス向け Microsoft Store にサインアップして開始します。](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [製品やサービス (プライベート ストアでアプリにアクセスできるユーザーを含む) を管理](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)します。 ここでは、ストアにインストールできるユーザーを制御して WSL ディストリビューションを追加できます。
* [任意の配布方法を使用して、ソフトウェア会社を展開するには](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* できる限り WSL ディストリビューションへのアクセスを持つユーザーとの通信[次の手順を使用して、](https://docs.microsoft.com/en-us/windows/wsl/install-win10)ディストリビューションまたは自分で選択したディストリビューションをインストールするには 

## <a name="how-to-distribute-a-distro-offline"></a>ディストリビューションをオフラインに配布する方法

社内のコンピューターでは、ビジネス向け Microsoft Store または Microsoft Store へのアクセスを持っていない場合は、次の手順に従って、オフラインのライセンスを持つ Linux ディストリビューションのインストーラーをダウンロードできます。 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Azure Active Directory (AD) アカウントを設定します。 

Azure AD アカウントを持っており、Microsoft Store アプリのインストーラーを取得する、組織のグローバル管理者である必要があります。 アカウントを既にある場合は、この手順をスキップすることができます。

アカウントを登録する手順についてはここにあります。 https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>ビジネス向けストアにサインインし、ホーム ページに移動
ここでサインイン: www.microsoft.com/business-store

![会社のホーム ページの MS ストア](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>管理に移動の設定-> およびオフライン アプリを表示する を有効にします。

![MS ストア for business の設定 ページ](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>'自分のグループを探す' をクリックしてメイン ページに戻る

![会社のホーム ページの MS ストア](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>必要なディストリビューションを検索して選択します

![MS ストアのアクティブな検索とビジネスのホーム ページ](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>ライセンスの種類 ドロップダウン メニューで、オフライン ライセンスを選択し、'アプリを入手する をクリックします。

![MS ストア for business の Ubuntu 製品 ページ](media/offlineinstallscreens/4-screen.png)

注: いくつかのディストリビューションがオフラインのライセンスを取得するには、しないことができます

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>アプリの製品ページに [管理] ボタンをクリックします

![MS ストア for business の Ubuntu 製品 ページ](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>アーキテクチャを選択し、オフラインで使用するパッケージをダウンロード

![MS ストア for business Ubuntu 製品の詳細 ページ](media/offlineinstallscreens/6-screen.png)

このインストーラーは、WSL をインストールするには任意のコンピューターに配布できます。