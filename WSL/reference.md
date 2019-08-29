---
title: Linux 用 Windows サブシステムのコマンドリファレンス
description: Windows Subsystem for Linux を管理するコマンドの一覧
keywords: BashOnWindows、bash、wsl、windows、windows subsystem for linux、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: edd4b8216a25f519e36b8b99b626b0a4315f6039
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122742"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のコマンドリファレンス

Windows Subsystem for Linux を操作する最良の方法は、 `wsl.exe`コマンドを使用することです。 


## `wsl.exe`

Windows バージョン1903以降を使用して`wsl.exe`いる場合のすべてのオプションを含む一覧を次に示します。

従っ`wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-binaries"></a>Linux バイナリを実行するための引数

* **引数なし**

  コマンドラインが指定されていない場合、既定のシェルが起動されます。

* **--exec、-e \<コマンドライン >**
  
  既定の Linux シェルを使用せずに、指定したコマンドを実行します。

* **--**
  
  残りのコマンドラインをそのまま渡します。

上記のコマンドでは、次のオプションも使用できます。

* **--distribution、-d \<ディストリビューション >**

  指定された分布を実行します。

* **--user、-u \<UserName >**

  指定されたユーザーとして実行します。

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a>Linux 用 Windows サブシステムを管理するための引数

* **--ディストリビューション\<> \<ファイル名 > をエクスポートします**
  
  配布を tar ファイルにエクスポートします。 ファイル名には、標準出力の場合はを指定できます。

* **--ディストリビューション\<> \<InstallLocation > \<FileName > をインポートします**
  
  指定した tar ファイルを新しいディストリビューションとしてインポートします。 ファイル名には、標準入力の場合はを指定できます。

* **--list、-l [Options]**
  
  ディストリビューションを一覧表示します。

  オプション:
  * **--すべて**
      
    現在インストール中またはアンインストール中のディストリビューションを含む、すべてのディストリビューションを一覧表示します。

  * **--実行中**
      
    現在実行中のディストリビューションのみを一覧表示します。

* **--set-既定値、- \<s ディストリビューション >**
  
  ディストリビューションを既定値として設定します。

* **--terminate、-t \<ディストリビューション >**
  
  指定された分布を終了します。

* **--ディストリビューション\<の登録を解除 >**
  
  ディストリビューションの登録を解除します。
   
* **--help**使用状況に関する情報を表示します。

## <a name="additional-commands"></a>その他のコマンド

Windows Subsystem for Linux と対話するための履歴コマンドもあります。 これらの機能はに`wsl.exe`含まれていますが、引き続き使用できます。 

### `wslconfig.exe`

このコマンドでは、WSL 分布を構成できます。 そのオプションの一覧を次に示します。

従っ`wslconfig [Argument] [Options...]`

#### <a name="arguments"></a>引数
* **/l、/list [オプション]**
  
  登録済みのディストリビューションを一覧表示します。
  
  オプション:
    * **/all**
    
      必要に応じて、現在インストール中またはアンインストール中のディストリビューションも含め、すべてのディストリビューションを一覧表示します。

    * **/実行中**
      
      現在実行中のディストリビューションのみを一覧表示します。

* **/s、/setdefault \<のディストリビューション >**
  
  ディストリビューションを既定値として設定します。

* **/t、または\<ディストリビューションを終了し >**
  
  分布を終了します。

* **/u、/unregister \<のディストリビューション >**
  
  ディストリビューションの登録を解除します。
   
* **/upgrade \<のディストリビューション >**
  
  分散を WslFs ファイルシステム形式にアップグレードします。

### `bash.exe`

このコマンドは、bash シェルを開始するために使用されます。 このコマンドで使用できるオプションを以下に示します。

従っ`bash [Options...]`

* **オプションが指定されていません**
  
  現在のディレクトリで Bash シェルを起動します。 Bash シェルがインストールされていない場合は、自動的に実行されます。`lxrun /install`

* **~**
  
  `bash ~`ユーザーのホームディレクトリに bash シェルを起動します。  の実行`cd ~`と同様です。

* **-c "\<command >"**
  
  コマンドを実行し、出力を出力して、Windows のコマンドプロンプトに戻ります。
    
  例: `bash -c "ls"`。

## <a name="deprecated-commands"></a>非推奨のコマンド

は`lxrun.exe` 、Windows Subsystem for Linux をインストールして管理するために使用される最初のコマンドでした。 Windows 10 1803 以降では非推奨とされます。

コマンド`lxrun.exe`を使用して、 [Windows Subsystem for Linux (wsl)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)と直接やり取りできます。  これらのコマンドは`\Windows\System32`ディレクトリにインストールされ、Windows コマンドプロンプトまたは PowerShell 内で実行できます。

| Command                     | 説明                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun コマンドは、WSL インスタンスを管理するために使用されます。 |
| `lxrun /install`            | ダウンロードとインストールのプロセスを開始します。 <br/> すべてのプロンプトをバイパスするには、 **/y**を追加します。  確認プロンプトが自動的に受け入れられ、既定のユーザーは root に設定されます。          |
| `lxrun /uninstall`          | Ubuntu イメージをアンインストールおよび削除します。  既定では、ユーザーの Ubuntu ホームディレクトリは削除されません。 <br/> **/y**を追加して確認プロンプトを自動的に受け入れることができます <br/>のユーザーの Ubuntu ホームディレクトリをアンインストールおよび削除します。         |
| `lxrun /setdefaultuser <userName>`     | Ubuntu ユーザーの既定の Bash を設定します。 指定されたユーザーが存在しない場合は、パスワードの入力を求められます。  詳細については https://aka.ms/wslusers 、「」を参照してください。 <br/> **/y**パスワードの promping をバイパスします。  ユーザーはパスワードなしで作成されます。|
| `lxrun /update`            | サブシステムのパッケージインデックスを更新します          |
