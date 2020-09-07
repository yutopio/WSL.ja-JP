---
title: Windows Subsystem for Linux (WSL) を Windows 10 にインストールする
description: Windows 10 に Linux 用 Windows サブシステムをインストールする方法について説明します。 Windows 10 は、バージョン 2004、ビルド 19041 以上に更新する必要があります。
keywords: BashOnWindows, bash, wsl, windows, linux 用 windows サブシステム, windowssubsystem, ubuntu, debian, suse, windows 10, インストール, 有効にする, WSL2, バージョン 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 14e1697d1f2ac7a1efa17368be830a5c22973bc6
ms.sourcegitcommit: 910845e9b3f980b2c5b9b4968331a706720603c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2020
ms.locfileid: "89058497"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows 10 用 Windows Subsystem for Linux のインストール ガイド

## <a name="install-the-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のインストール

Windows 上に Linux ディストリビューションをインストールする前に、"Linux 用 Windows サブシステム" オプション機能を有効にする必要があります。

管理者として PowerShell を開き、以下を実行します。

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

WSL 1 のみをインストールするには、お使いのマシンを再起動し、「[選択した Linux ディストリビューションをインストールする](./install-win10.md#install-your-linux-distribution-of-choice)」に進んでください。それ以外の場合は、再起動を待ってから WSL 2 への更新操作に進んでください。 詳細については、「[WSL 2 と WSL 1 の比較](./compare-versions.md)」を参照してください。

## <a name="update-to-wsl-2"></a>WSL 2 に更新する

WSL 2 に更新するには、次の条件を満たす必要があります。

- [バージョン 1903 以降](ms-settings:windowsupdate)、**ビルド 18362** 以上に更新された x64 システム用の Windows 10 を実行している。
- バージョン 2004 以降、**ビルド 19041** に更新された ARM64 システム用の Windows 10 を実行している。
- Windows 10 バージョン 1903 または 1909 を使用している場合は、適切なバックポートがあることを確認する必要があります。手順については、[こちらを参照してください](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it)。 

- Windows のバージョンを確認するには **Windows ロゴ キー + R** キーを押します。次に「**winver**」と入力し、 **[OK]** を選択します (または、Windows コマンド プロンプトで `ver` コマンドを入力します)。 お使いのビルドが 18361 より前の場合は、[最新の Windows バージョンに更新](ms-settings:windowsupdate)してください。 [Windows 更新アシスタントを入手する](https://www.microsoft.com/software-download/windows10)。

### <a name="enable-the-virtual-machine-platform-optional-component"></a>"仮想マシン プラットフォーム" のオプション コンポーネントを有効にする

WSL 2 をインストールする前に、"仮想マシン プラットフォーム" オプション機能を有効にする必要があります。

管理者として PowerShell を開き、以下を実行します。

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

お使いのマシンを**再起動**して WSL のインストールを完了し、WSL 2 に更新します。

### <a name="set-wsl-2-as-your-default-version"></a>WSL 2 を既定のバージョンとして設定する

管理者として PowerShell を開いて次のコマンドを実行し、新しい Linux ディストリビューションをインストールする際の既定のバージョンとして WSL 2 を設定します。

```powershell
wsl --set-default-version 2
```

このメッセージは、コマンド `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel` を実行した後に表示されることがあります。 リンク ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) に従って、WSL 2 で使用する Linux カーネルをコンピューターにインストールするためのドキュメントのこのページから MSI をインストールしてください。 カーネルをインストールしたら、コマンドを再度実行すると、メッセージが表示されることなく正常に完了します。 

> [!NOTE]
> 対象のディストリビューションのサイズによっては、WSL 1 から WSL 2 への更新が完了するまでに数分かかる場合があります。 Windows 10 Anniversary Update または Creators Update から WSL 1 の古い (レガシ) インストールを実行している場合は、更新エラーが発生することがあります。 次の手順に従って、[レガシ ディストリビューションをアンインストールして削除](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro)します。 
>
> `wsl --set-default-version` の結果が無効なコマンドである場合は、「`wsl --help`」と入力してください。 `--set-default-version` が表示されない場合は、お使いの OS によってサポートされていないことを意味しているため、バージョン 1903、ビルド 18362 以上に更新する必要があります。

## <a name="install-your-linux-distribution-of-choice"></a>選択した Linux ディストリビューションをインストールする

1. [Microsoft Store](https://aka.ms/wslstore) を開き、希望する Linux ディストリビューションを選択します。

    ![Microsoft Store での Linux ディストリビューションの表示](media/store.png)

    次のリンクを使用すると、各ディストリビューションの Microsoft Store ページが開きます。

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [Ubuntu 20.04 LTS](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [openSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [WSL のための Fedora リミックス](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

2. ディストリビューションのページで、[入手] を選択します。

    ![Microsoft Store での Linux ディストリビューション](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a>新しいディストリビューションを設定する

新しくインストールした Linux ディストリビューションを初めて起動すると、コンソール ウィンドウが開き、ファイルが圧縮解除されて PC に格納されるまで 1、2 分待つように求められます。 今後のすべての起動には、1 秒もかかりません。

次に、[新しい Linux ディストリビューションのユーザー アカウントとパスワードを作成する](./user-support.md)必要があります。

![Windows コンソールでの Ubuntu の展開](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>ディストリビューションのバージョンを WSL 1 または WSL 2 に設定する

インストールされている各 Linux ディストリビューションに割り当てられている WSL バージョンを確認するには、PowerShell コマンド ラインを開き、次のコマンドを入力します ([Windows ビルド 18362 以上](ms-settings:windowsupdate)でのみ使用可能): `wsl -l -v`

```powershell
wsl --list --verbose
```

ディストリビューションで使用される WSL のバージョンを設定するには、以下を実行します。

```powershell
wsl --set-version <distribution name> <versionNumber>
```

`<distribution name>` は、お使いのディストリビューションの実際の名前に必ず置き換えてください。`<versionNumber>` は、数字の "1" または "2" に置き換えてください。 上記と同じコマンドで "2" を "1" に置き換えて実行することにより、いつでも WSL 1 に戻すことができます。

また、WSL 2 を既定のアーキテクチャにする場合は、次のコマンドを使用して実行できます。

```powershell
wsl --set-default-version 2
```

これにより、インストールされるすべての新しいディストリビューションのバージョンが WSL 2 に設定されます。

## <a name="troubleshooting-installation"></a>インストールのトラブルシューティング

関連エラーと推奨される修正を次に示します。 その他の一般的なエラーとその解決策については、[WSL のトラブルシューティングのページ](troubleshooting.md)を参照してください。

- **エラー 0x80070003 が発生してインストールに失敗しました**
  - Windows Subsystem for Linux はシステム ドライブ (通常、これは `C:` ドライブ) でのみ実行されます。 ディストリビューションがシステム ドライブに格納されていることを確認します。  
  - **[設定]** -> **[ストレージ]** -> **[その他のストレージ設定: 新しいコンテンツの保存先を変更する]** 
    を開きます。![C: ドライブにアプリをインストールするためのシステム設定の画像](media/AppStorage.png)

- **WslRegisterDistribution failed with error 0x8007019e (エラー0x8007019e で WslRegisterDistribution が失敗しました)**
  - Windows Subsystem for Linux オプション コンポーネントが有効になっていません。
  - **[コントロール パネル]**  ->  **[プログラムと機能]**  ->  **[Windows の機能の有効化または無効化]** を開いて、 **[Linux 用 Windows サブシステム]** をチェックするか、またはこの記事の冒頭に記載した PowerShell コマンドレットを使用してください。

- **インストールがエラー 0x80070003 またはエラー 0x80370102 で失敗した**
  - コンピューターの BIOS 内部で仮想化が有効になっていることを確認してください。 これを行う方法の手順は、コンピューターによって異なりますが、最も可能性が高いのは CPU 関連のオプションの下です。

- **アップグレードしようとしたときに次のエラーが発生する: `Invalid command line option: wsl --set-version Ubuntu 2`**
  - Linux 用 Windows サブシステムが有効になっていること、および Windows ビルド バージョン 18362 以上を使用していることをご確認ください。 WSL を有効にするには、PowerShell プロンプトで管理者特権を使用してこのコマンドを実行します: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。

- **仮想ディスク システムの制限があるため、要求された操作を完了できませんでした。仮想ハード ディスク ファイルは、圧縮と暗号化が解除されている必要があります。また、スパースにすることはできません。**
  - [内容を圧縮] ([内容を暗号化] のチェックボックスがオンになっている場合はこれも) を選択解除するため、Linux ディストリビューションのプロファイル フォルダーを開きます。 これは、Windows ファイル システムのフォルダーにあります (例: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`)。
  - この Linux ディストリビューション プロファイル内に、LocalState フォルダーが存在します。 このフォルダーを右クリックして、オプションのメニューを表示します。 [プロパティ] > [詳細設定] の順に選択し、[内容を圧縮してディスク領域を節約する] および [内容を暗号化してデータをセキュリティで保護する] チェックボックスを確実にオフにします。 これを現在のフォルダーのみに適用するか、すべてのサブフォルダーとファイルに適用するかを確認するメッセージが表示された場合は、圧縮フラグをオフにしようとしているだけなので、[このフォルダーのみ] を選択します。 この操作を実行すると、`wsl –set-version` コマンドが機能するようになります。

![WSL ディストリビューションのプロパティ設定のスクリーンショット](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> この例では、Ubuntu 18.04 ディストリビューションの LocalState フォルダーの場所は次のとおりです。C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc
>
> この問題の最新情報が追跡されている [WSL ドキュメント GitHub スレッド #4103](https://github.com/microsoft/WSL/issues/4103) をご確認ください。

- **"wsl" という用語が、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。**
  - [Linux 用 Windows サブシステムのオプション コンポーネントがインストールされている](./install-win10.md#enable-the-virtual-machine-platform-optional-component)ことを確認してください。 また、ARM64 デバイスを使用し、PowerShell からこのコマンドを実行している場合も、このエラーを受け取ります。 代わりに、`wsl.exe`PowerShell Core[ またはコマンド プロンプトから ](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) を実行します。
