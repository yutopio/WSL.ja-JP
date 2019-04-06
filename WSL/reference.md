---
title: Linux コマンド リファレンス用 Windows サブシステム
description: Linux 用 Windows サブシステムを管理するコマンドの一覧
keywords: BashOnWindows、bash、wsl、windows、linux、windowssubsystem、ubuntu 用 windows サブシステム
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063580"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Windows Subsystem for Linux のコマンド リファレンス

> `lxrun.exe` Windows 10 1803 の時点で非推奨以降。

コマンドは、`lxrun.exe`と対話するために使用できる、 [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)直接します。  これらのコマンドにインストールされている、`\Windows\System32`ディレクトリ内での Windows コマンド プロンプトまたは PowerShell で実行する可能性があります。

* `lxrun.exe` WSL の管理に使用されます。  このコマンドは、インストールまたはアンインストールの Ubuntu イメージを使用できます。


| コマンド                     | 説明                     |
|:----------------------------|:---------------------------|
| `bash`                      | 現在のディレクトリに Bash シェルを起動します。  Bash シェルが自動的にインストールされていない場合の実行します。 `lxrun /install` |
| `bash ~`                    | Ubuntu のユーザーのホーム ディレクトリには、bash シェルを起動します。  Cd の実行に似て ~            |
| `bash -c "<command>"`       | コマンドを実行して、出力を印刷し、Windows コマンド プロンプトに終了します。 <br/> <br/> 例: **-c"%.*ls"の bash** |

<p>

| コマンド                     | 説明                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun コマンドは、WSL インスタンスの管理に使用されます。 |
| `lxrun /install`            | ダウンロードを開始し、プロセスをインストールします。 <br/> **/y**はすべてのプロンプトのバイパスに追加できます。  確認プロンプトが自動的に受け入れられるし、既定のユーザーがルートに設定されています。          |
| `lxrun /uninstall`          | アンインストールし、Ubuntu イメージを削除します。  既定ではこれは、ユーザーの Ubuntu のホーム ディレクトリを削除されません。 <br/> **/y**自動的に確認のプロンプトを受け入れるように追加することがあります <br/>**完全/** をアンインストールし、ユーザーの Ubuntu のホーム ディレクトリを削除します。         |
| `lxrun /setdefaultuser <userName>`     | Ubuntu のユーザーには、既定の Bash を設定します。 指定したユーザーが存在しない場合、パスワードを求められます。  詳細については、次を参照してください。:https://aka.ms/wslusersします。 <br/> **/y**パスワードのバイパス promping します。  パスワードを指定せず、ユーザーが作成されます。|
| `lxrun /update`            | サブシステムのパッケージのインデックスを更新します。          |
