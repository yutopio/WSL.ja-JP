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
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a>エンタープライズ企業向けに Linux 用 Windows サブシステムを設定する

ビジネス向け Microsoft Store では、自社に WSL をデプロイすることを検討している企業に対してさまざまなソリューションを提供しています。 [ビジネスおよび教育機関向け Microsoft Store のドキュメント](https://docs.microsoft.com/microsoft-store/)は、Store のエクスペリエンスに関する一般的な情報を見つけるための優れたリソースです。

WSL のデプロイを開始する準備の方法を調べている企業のお客様は、次の手順に従ってください。

* [ビジネス向け Microsoft Store にサインアップして開始します](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [対象の製品とサービスを管理します (たとえば、どのユーザーがプライベート ストア内のどのアプリにアクセスできるか)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview)。 ここでは、WSL ディストリビューションをストアに追加したり、それらをインストールできるユーザーを制御したりできます
* [任意の配布方法を使用して、ソフトウェアを会社にデプロイします](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* このドキュメント リンクを使用して WSL をインストールできることを会社の従業員に伝えます: [Linux 用 Windows サブシステムのインストール](./install-win10.md)

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a>Windows 上で Linux ディストリビューションをオフラインで配布する方法

社内のコンピューターから Microsoft Store またはビジネス向け Microsoft Store にアクセスできない場合は、次の手順に従って、オフライン ライセンスが与えられた Linux ディストリビューションのインストーラーをダウンロードできます。

### <a name="set-up-an-azure-active-directory-account"></a>Azure Active Directory アカウントを設定する

Microsoft Store アプリのインストーラーを入手するには、[Azure AD アカウントにサインアップ](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner)する必要があり、組織のグローバル管理者である必要があります。 既にアカウントがある場合は、この手順を省略できます。

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a>ビジネス向け Microsoft Store アカウントを使用して WSL を設定する

アカウントを登録する手順については、以下を参照してください: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business

1. ビジネス向け Store にサインインし、ホームページに移動します: https://www.microsoft.com/business-store

    ![ビジネス向け MS Store のホーム ページ](media/offlineinstallscreens/1-screen.png)

2. [管理] > [設定] に移動し、[Show offline apps]\(オフライン アプリを表示\) を有効にします。

    ![ビジネス向け MS Store の [設定] ページ](media/offlineinstallscreens/2-screen.png)

3. [Shop for my group]\(自分のグループ用に購入\) を選択して、メイン ページに戻ります。

    ![ビジネス向け MS Store のホーム ページ](media/offlineinstallscreens/1-screen.png)

4. 目的のディストリビューションを検索し、選択します。

    ![ビジネス向け MS Store の検索がアクティブなホーム ページ](media/offlineinstallscreens/3-screen.png)

5. [ライセンスの種類] ドロップダウン メニューで [オフライン] ライセンスを選択し、[Get the app]\(アプリを入手\) を選択します (一部の Linux ディストリビューションでは、オフライン ライセンスが提供されない場合があります)。

    ![ビジネス向け MS Store の Ubuntu の製品ページ](media/offlineinstallscreens/4-screen.png)

6. [管理] ボタンを選択して、アプリの製品ページに移動します。

    ![ビジネス向け MS Store の Ubuntu の製品ページ](media/offlineinstallscreens/5-screen.png)

7. 対象のアーキテクチャを選択し、オフラインで使用するためにパッケージをダウンロードします。

    ![ビジネス向け MS Store の Ubuntu の製品詳細ページ](media/offlineinstallscreens/6-screen.png)

このインストーラーは、WSL をインストールする任意のコンピューターに配布できます。
