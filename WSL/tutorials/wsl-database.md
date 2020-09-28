---
title: MySQL MongoDB、PostgreSQL、SQLite、Microsoft SQL Server、または Redis を使用して、Windows Subsystem for Linux でデータベースをセットアップする
description: Windows Subsystem for Linux で MySQL MongoDB、PostgreSQL、SQLite、Microsoft SQL Server、または Redis を設定する方法について説明します。
keywords: wsl、windows、windowssubsystem、MySQL MongoDB、PostgreSQL、SQLite、Microsoft SQL Server、Redis、windows 10
ms.date: 07/07/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: b7e4f7477741a931c4ee71e07736bac115443ac9
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413303"
---
# <a name="get-started-with-databases-on-windows-subsystem-for-linux"></a><span data-ttu-id="930aa-104">Windows Subsystem for Linux でデータベースを使ってみる</span><span class="sxs-lookup"><span data-stu-id="930aa-104">Get started with databases on Windows Subsystem for Linux</span></span>

<span data-ttu-id="930aa-105">このステップバイステップガイドでは、WSL 内のプロジェクトをデータベースに接続する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="930aa-105">This step-by-step guide will help you get started connecting your project in WSL to a database.</span></span> <span data-ttu-id="930aa-106">MySQL、PostgreSQL、MongoDB、Redis、Microsoft SQL Server、または SQLite の使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="930aa-106">Get started with MySQL, PostgreSQL, MongoDB, Redis, Microsoft SQL Server, or SQLite.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="930aa-107">[前提条件]</span><span class="sxs-lookup"><span data-stu-id="930aa-107">Prerequisites</span></span>

- <span data-ttu-id="930aa-108">[バージョン 2004](ms-settings:windowsupdate)、**ビルド 19041** 以上に更新された Windows 10 を実行している。</span><span class="sxs-lookup"><span data-stu-id="930aa-108">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>
- <span data-ttu-id="930aa-109">[Wsl が有効になり、インストールされ、wsl 2 に更新されました](../install-win10.md)。</span><span class="sxs-lookup"><span data-stu-id="930aa-109">[WSL enabled and installed, and updated to WSL 2](../install-win10.md).</span></span>
- <span data-ttu-id="930aa-110">[Linux ディストリビューションがインストールされている](../install-win10.md#step-6---install-your-linux-distribution-of-choice) (例については Ubuntu 18.04)。</span><span class="sxs-lookup"><span data-stu-id="930aa-110">[Linux distribution installed](../install-win10.md#step-6---install-your-linux-distribution-of-choice) (Ubuntu 18.04 for our examples).</span></span>
- <span data-ttu-id="930aa-111">Ubuntu 18.04 のディストリビューションが [WSL 2 モードで実行](../install-win10.md#set-your-distribution-version-to-wsl-1-or-wsl-2)されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="930aa-111">Ensure your Ubuntu 18.04 distribution is [running in WSL 2 mode](../install-win10.md#set-your-distribution-version-to-wsl-1-or-wsl-2).</span></span> <span data-ttu-id="930aa-112">(WSL では、v1 モードと v2 モードの両方でディストリビューションを実行できます)。これを確認するには、PowerShell を開き、次のように入力します。 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="930aa-112">(WSL can run distributions in both v1 or v2 mode.) You can check this by opening PowerShell and entering: `wsl -l -v`</span></span>

## <a name="differences-between-database-systems"></a><span data-ttu-id="930aa-113">データベースシステム間の相違点</span><span class="sxs-lookup"><span data-stu-id="930aa-113">Differences between database systems</span></span>

<span data-ttu-id="930aa-114">データベースシステムの最も [一般的な選択肢](https://insights.stackoverflow.com/survey/2019#technology-_-databases) は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="930aa-114">The most [popular choices](https://insights.stackoverflow.com/survey/2019#technology-_-databases) for a database system include:</span></span>

- <span data-ttu-id="930aa-115">[MySQL](https://www.mysql.com/why-mysql/) (SQL)</span><span class="sxs-lookup"><span data-stu-id="930aa-115">[MySQL](https://www.mysql.com/why-mysql/) (SQL)</span></span>
- <span data-ttu-id="930aa-116">[PostgreSQL](https://www.postgresql.org/about/) (SQL)</span><span class="sxs-lookup"><span data-stu-id="930aa-116">[PostgreSQL](https://www.postgresql.org/about/) (SQL)</span></span>
- <span data-ttu-id="930aa-117">[Microsoft SQL Server](/sql) (SQL)</span><span class="sxs-lookup"><span data-stu-id="930aa-117">[Microsoft SQL Server](/sql) (SQL)</span></span>
- <span data-ttu-id="930aa-118">[SQLite](https://www.sqlite.org/about.html) (SQL)</span><span class="sxs-lookup"><span data-stu-id="930aa-118">[SQLite](https://www.sqlite.org/about.html) (SQL)</span></span>
- <span data-ttu-id="930aa-119">[MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)</span><span class="sxs-lookup"><span data-stu-id="930aa-119">[MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)</span></span>
- <span data-ttu-id="930aa-120">[Redis](https://redis.io/topics/introduction) (NoSQL)</span><span class="sxs-lookup"><span data-stu-id="930aa-120">[Redis](https://redis.io/topics/introduction) (NoSQL)</span></span>

<span data-ttu-id="930aa-121">**MySQL** は、オープンソースの SQL リレーショナルデータベースで、データ型が相互に関連している可能性のある1つ以上のテーブルにデータを整理します。</span><span class="sxs-lookup"><span data-stu-id="930aa-121">**MySQL** is an open-source SQL relational database, organizing data into one or more tables in which data types may be related to each other.</span></span> <span data-ttu-id="930aa-122">この機能は垂直方向にスケーラブルであるため、1つの究極のコンピューターで作業が行われます。</span><span class="sxs-lookup"><span data-stu-id="930aa-122">It is vertically scalable, which means one ultimate machine will do the work for you.</span></span> <span data-ttu-id="930aa-123">現在、4つのデータベースシステムで最も広く使用されています。</span><span class="sxs-lookup"><span data-stu-id="930aa-123">It is currently the most widely used of the four database systems.</span></span>

<span data-ttu-id="930aa-124">**PostgreSQL** (Postgres とも呼ばれます) もオープンソースの SQL リレーショナルデータベースであり、拡張性と標準への準拠を重視しています。</span><span class="sxs-lookup"><span data-stu-id="930aa-124">**PostgreSQL** (sometimes referred to as Postgres) is also an open-source SQL relational database with an emphasis on extensibility and standards compliance.</span></span> <span data-ttu-id="930aa-125">現在は JSON も処理できますが、一般的には、構造化データ、垂直方向の規模拡張、および、e コマースや金融取引などの ACID 準拠のニーズに適しています。</span><span class="sxs-lookup"><span data-stu-id="930aa-125">It can handle JSON now too, but it is generally better for structured data, vertical scaling, and ACID-compliant needs like eCommerce and financial transactions.</span></span>

<span data-ttu-id="930aa-126">**Microsoft SQL Server** には、Azure 上の Windows、SQL SERVER ON LINUX、SQL の SQL Server が含まれています。</span><span class="sxs-lookup"><span data-stu-id="930aa-126">**Microsoft SQL Server** includes SQL Server on Windows, SQL Server on Linux, and SQL on Azure.</span></span> <span data-ttu-id="930aa-127">これらは、ソフトウェアアプリケーションによって要求されたデータの格納と取得の主な機能を備えたサーバーに設定されたリレーショナルデータベース管理システムでもあります。</span><span class="sxs-lookup"><span data-stu-id="930aa-127">These are also relational database management systems set up on servers with primary function of storing and retrieving data as requested by software applications.</span></span>

<span data-ttu-id="930aa-128">**SQLite** は、オープンソースの自己完結型の "サーバーレス" データベースです。低メモリ環境でも、移植性、信頼性、優れたパフォーマンスが確保されています。</span><span class="sxs-lookup"><span data-stu-id="930aa-128">**SQLite** is an open-source self-contained, file-based, “serverless” database, known for its portability, reliability, and good performance even in low-memory environments.</span></span>

<span data-ttu-id="930aa-129">**MongoDB** は、JSON を使用してスキーマフリーデータを格納するように設計されたオープンソースの NoSQL ドキュメントデータベースです。</span><span class="sxs-lookup"><span data-stu-id="930aa-129">**MongoDB** is an open-source NoSQL document database designed to work with JSON and store schema-free data.</span></span> <span data-ttu-id="930aa-130">水平方向にスケーラブルなので、複数の小さなマシンで作業が行われます。</span><span class="sxs-lookup"><span data-stu-id="930aa-130">It is horizontally scalable, which means multiple smaller machines will do the work for you.</span></span> <span data-ttu-id="930aa-131">柔軟性と非構造化データに適しており、リアルタイム分析をキャッシュしています。</span><span class="sxs-lookup"><span data-stu-id="930aa-131">It's good for flexibility and unstructured data, and caching real-time analytics.</span></span>

<span data-ttu-id="930aa-132">**Redis** は、オープンソースのメモリ内の NoSQL データ構造ストアです。</span><span class="sxs-lookup"><span data-stu-id="930aa-132">**Redis** is is an open-source NoSQL in-memory data structure store.</span></span> <span data-ttu-id="930aa-133">ドキュメントではなく、ストレージにキーと値のペアを使用します。</span><span class="sxs-lookup"><span data-stu-id="930aa-133">It uses key-value pairs for storage instead of documents.</span></span> <span data-ttu-id="930aa-134">Redis は、柔軟性、パフォーマンス、および幅広い言語のサポートのために認識されています。</span><span class="sxs-lookup"><span data-stu-id="930aa-134">Redis is known for its flexibility, performance, and wide language support.</span></span> <span data-ttu-id="930aa-135">キャッシュまたはメッセージブローカーとして使用するのに十分な柔軟性があり、リスト、セット、ハッシュなどのデータ構造を使用できます。</span><span class="sxs-lookup"><span data-stu-id="930aa-135">It’s flexible enough to be used as a cache or message broker and can use data structures like lists, sets, and hashes.</span></span>

<span data-ttu-id="930aa-136">選択するデータベースの種類は、データベースを使用するアプリケーションの種類に応じて決める必要があります。</span><span class="sxs-lookup"><span data-stu-id="930aa-136">The sort of database you choose should depend on the type of application you will be using the database with.</span></span> <span data-ttu-id="930aa-137">構造化データベースと非構造化データベースの長所と短所を検討し、ユースケースに基づいて選択することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="930aa-137">We recommend that you look up the advantages and disadvantages of structured and unstructured databases and choose based on your use case.</span></span>

## <a name="install-mysql"></a><span data-ttu-id="930aa-138">MySQL をインストールする</span><span class="sxs-lookup"><span data-stu-id="930aa-138">Install MySQL</span></span>

<span data-ttu-id="930aa-139">WSL に MySQL をインストールするには (Ubuntu 18.04):</span><span class="sxs-lookup"><span data-stu-id="930aa-139">To install MySQL on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="930aa-140">WSL ターミナルを開きます (Ubuntu 18.04)。</span><span class="sxs-lookup"><span data-stu-id="930aa-140">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="930aa-141">`sudo apt update` を実行して Ubuntu パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="930aa-141">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="930aa-142">パッケージが更新されたら、次のものを使用して MySQL をインストールします。 `sudo apt install mysql-server`</span><span class="sxs-lookup"><span data-stu-id="930aa-142">Once the packages have updated, install MySQL with: `sudo apt install mysql-server`</span></span>
4. <span data-ttu-id="930aa-143">`mysql --version` を実行してインストールを確認し、バージョン番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="930aa-143">Confirm installation and get the version number: `mysql --version`</span></span>

<span data-ttu-id="930aa-144">また、含まれているセキュリティスクリプトを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="930aa-144">You may also want to run the included security script.</span></span> <span data-ttu-id="930aa-145">これにより、リモートルートログインやサンプルユーザーなどの、安全性の低い既定のオプションの一部が変更されます。</span><span class="sxs-lookup"><span data-stu-id="930aa-145">This changes some of the less secure default options for things like remote root logins and sample users.</span></span> <span data-ttu-id="930aa-146">セキュリティスクリプトを実行するには:</span><span class="sxs-lookup"><span data-stu-id="930aa-146">To run the security script:</span></span>

1. <span data-ttu-id="930aa-147">MySQL サーバーを起動します。 `sudo /etc/init.d/mysql start`</span><span class="sxs-lookup"><span data-stu-id="930aa-147">Start a MySQL server: `sudo /etc/init.d/mysql start`</span></span>
2. <span data-ttu-id="930aa-148">セキュリティスクリプトのプロンプトを開始します。 `sudo mysql_secure_installation`</span><span class="sxs-lookup"><span data-stu-id="930aa-148">Start the security script prompts: `sudo mysql_secure_installation`</span></span>
3. <span data-ttu-id="930aa-149">最初のプロンプトで、パスワードの検証プラグインを設定するかどうかを確認するメッセージが表示されます。これを使用すると、MySQL パスワードの強度をテストできます。</span><span class="sxs-lookup"><span data-stu-id="930aa-149">The first prompt will ask whether you’d like to set up the Validate Password Plugin, which can be used to test the strength of your MySQL password.</span></span> <span data-ttu-id="930aa-150">次に、MySQL ルートユーザーのパスワードを設定し、匿名ユーザーを削除するかどうかを決定し、ルートユーザーがローカルとリモートの両方でログインできるようにするかどうかを決定し、テストデータベースを削除するかどうかを決定し、最後に特権テーブルを直ちに再読み込みするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="930aa-150">You will then set a password for the MySQL root user, decide whether or not to remove anonymous users, decide whether to allow the root user to login both locally and remotely, decide whether to remove the test database, and, lastly, decide whether to reload the privilege tables immediately.</span></span>

<span data-ttu-id="930aa-151">MySQL プロンプトを開くには、次のように入力します。 `sudo mysql`</span><span class="sxs-lookup"><span data-stu-id="930aa-151">To open the MySQL prompt, enter: `sudo mysql`</span></span>

<span data-ttu-id="930aa-152">使用できるデータベースを確認するには、MySQL プロンプトで次のように入力します。 `SHOW DATABASES;`</span><span class="sxs-lookup"><span data-stu-id="930aa-152">To see what databases you have available, in the MySQL prompt, enter: `SHOW DATABASES;`</span></span>

<span data-ttu-id="930aa-153">新しいデータベースを作成するには、次のように入力します。 `CREATE DATABASE database_name;`</span><span class="sxs-lookup"><span data-stu-id="930aa-153">To create a new database, enter: `CREATE DATABASE database_name;`</span></span>

<span data-ttu-id="930aa-154">データベースを削除するには、次のように入力します。 ` DROP DATABASE database_name;`</span><span class="sxs-lookup"><span data-stu-id="930aa-154">To delete a database, enter: ` DROP DATABASE database_name;`</span></span>

<span data-ttu-id="930aa-155">MySQL データベースの操作の詳細については、 [mysql のドキュメント](https://dev.mysql.com/doc/mysql-getting-started/en/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-155">For more about working with MySQL databases, see the [MySQL docs](https://dev.mysql.com/doc/mysql-getting-started/en/).</span></span>

<span data-ttu-id="930aa-156">VS Code で MySQL データベースを操作するには、 [mysql 拡張機能](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2)を試してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-156">To work with with MySQL databases in VS Code, try the [MySQL extension](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).</span></span>

## <a name="install-postgresql"></a><span data-ttu-id="930aa-157">PostgreSQL のインストール</span><span class="sxs-lookup"><span data-stu-id="930aa-157">Install PostgreSQL</span></span>

<span data-ttu-id="930aa-158">WSL に PostgreSQL をインストールするには (Ubuntu 18.04):</span><span class="sxs-lookup"><span data-stu-id="930aa-158">To install PostgreSQL on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="930aa-159">WSL ターミナルを開きます (Ubuntu 18.04)。</span><span class="sxs-lookup"><span data-stu-id="930aa-159">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="930aa-160">`sudo apt update` を実行して Ubuntu パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="930aa-160">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="930aa-161">パッケージが更新されたら、`sudo apt install postgresql postgresql-contrib` を実行して PostgreSQL (およびいくつかの便利なユーティリティが含まれている -contrib パッケージ) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="930aa-161">Once the packages have updated, install PostgreSQL (and the -contrib package which has some helpful utilities) with: `sudo apt install postgresql postgresql-contrib`</span></span>
4. <span data-ttu-id="930aa-162">`psql --version` を実行してインストールを確認し、バージョン番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="930aa-162">Confirm installation and get the version number: `psql --version`</span></span>

<span data-ttu-id="930aa-163">PostgreSQL をインストールした後は、次の 3 つのコマンドについて覚えておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="930aa-163">There are 3 commands you need to know once PostgreSQL is installed:</span></span>

- <span data-ttu-id="930aa-164">データベースの状態を確認する `sudo service postgresql status`</span><span class="sxs-lookup"><span data-stu-id="930aa-164">`sudo service postgresql status` for checking the status of your database.</span></span>
- <span data-ttu-id="930aa-165">データベースの実行を開始する `sudo service postgresql start`</span><span class="sxs-lookup"><span data-stu-id="930aa-165">`sudo service postgresql start`  to start running your database.</span></span>
- <span data-ttu-id="930aa-166">データベースの実行を停止する `sudo service postgresql stop`</span><span class="sxs-lookup"><span data-stu-id="930aa-166">`sudo service postgresql stop` to stop running your database.</span></span>

<span data-ttu-id="930aa-167">既定の管理者ユーザー `postgres` には、データベースに接続するパスワードを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="930aa-167">The default admin user, `postgres`, needs a password assigned in order to connect to a database.</span></span> <span data-ttu-id="930aa-168">パスワードを設定するには:</span><span class="sxs-lookup"><span data-stu-id="930aa-168">To set a password:</span></span>

1. <span data-ttu-id="930aa-169">コマンド `sudo passwd postgres` を入力します。</span><span class="sxs-lookup"><span data-stu-id="930aa-169">Enter the command: `sudo passwd postgres`</span></span>
2. <span data-ttu-id="930aa-170">新しいパスワードを入力するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="930aa-170">You will get a prompt to enter your new password.</span></span>
3. <span data-ttu-id="930aa-171">ターミナルを閉じ、開き直します。</span><span class="sxs-lookup"><span data-stu-id="930aa-171">Close and reopen your terminal.</span></span>

<span data-ttu-id="930aa-172">[Psql](https://www.postgresql.org/docs/10/app-psql.html)シェルで PostgreSQL を実行するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="930aa-172">To run PostgreSQL with [psql](https://www.postgresql.org/docs/10/app-psql.html) shell:</span></span>

1. <span data-ttu-id="930aa-173">`sudo service postgresql start` を実行して postgres サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="930aa-173">Start your postgres service: `sudo service postgresql start`</span></span>
2. <span data-ttu-id="930aa-174">`sudo -u postgres psql` を実行して postgres サービスに接続し、psql シェルを開きます。</span><span class="sxs-lookup"><span data-stu-id="930aa-174">Connect to the postgres service and open the psql shell: `sudo -u postgres psql`</span></span>

<span data-ttu-id="930aa-175">正常に psql シェルに入ると、コマンドラインが `postgres=#` のように変わります。</span><span class="sxs-lookup"><span data-stu-id="930aa-175">Once you have successfully entered the psql shell, you will see your command line change to look like this: `postgres=#`</span></span>

> [!NOTE]
> <span data-ttu-id="930aa-176">または、`su - postgres` を使用して postgres ユーザーに切り替え、コマンド `psql` を入力することで psql シェルを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="930aa-176">Alternatively, you can open the psql shell by switching to the postgres user with: `su - postgres` and then entering the command: `psql`.</span></span>

<span data-ttu-id="930aa-177">Postgres = # enter を終了するに `\q` は、またはショートカットキーを使用します: Ctrl + D</span><span class="sxs-lookup"><span data-stu-id="930aa-177">To exit postgres=# enter: `\q` or use the shortcut key: Ctrl+D</span></span>

<span data-ttu-id="930aa-178">PostgreSQL のインストールで作成されたユーザー アカウントを確認するには、WSL ターミナルから `psql -c "\du"` を使用します。または、psql シェルが開いている場合は、`\du` を実行します。</span><span class="sxs-lookup"><span data-stu-id="930aa-178">To see what user accounts have been created on your PostgreSQL installation, use from your WSL terminal: `psql -c "\du"` ...or just `\du` if you have the psql shell open.</span></span> <span data-ttu-id="930aa-179">このコマンドでは、アカウントのユーザー名、ロール属性の一覧、およびロールグループのメンバーの列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="930aa-179">This command will display columns: Account User Name, List of Roles Attributes, and Member of role group(s).</span></span> <span data-ttu-id="930aa-180">`q` を入力すると、終了してコマンド ラインに戻ります。</span><span class="sxs-lookup"><span data-stu-id="930aa-180">To exit back to the command line, enter: `q`.</span></span>

<span data-ttu-id="930aa-181">PostgreSQL データベースの操作の詳細については、 [postgresql のドキュメント](https://www.postgresql.org/docs/13/tutorial-createdb.html)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-181">For more about working with PostgreSQL databases, see the [PostgreSQL docs](https://www.postgresql.org/docs/13/tutorial-createdb.html).</span></span>

<span data-ttu-id="930aa-182">VS Code で PostgreSQL データベースを使用するには、 [postgresql の拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql)を試してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-182">To work with with PostgreSQL databases in VS Code, try the [PostgreSQL extension](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).</span></span>

## <a name="install-mongodb"></a><span data-ttu-id="930aa-183">MongoDB をインストールする</span><span class="sxs-lookup"><span data-stu-id="930aa-183">Install MongoDB</span></span>

<span data-ttu-id="930aa-184">WSL に MongoDB をインストールするには (Ubuntu 18.04):</span><span class="sxs-lookup"><span data-stu-id="930aa-184">To install MongoDB on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="930aa-185">WSL ターミナルを開きます (Ubuntu 18.04)。</span><span class="sxs-lookup"><span data-stu-id="930aa-185">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="930aa-186">`sudo apt update` を実行して Ubuntu パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="930aa-186">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="930aa-187">パッケージが更新されたら、`sudo apt-get install mongodb` を実行して MongoDB をインストールします。</span><span class="sxs-lookup"><span data-stu-id="930aa-187">Once the packages have updated, install MongoDB with: `sudo apt-get install mongodb`</span></span>
4. <span data-ttu-id="930aa-188">`mongod --version` を実行してインストールを確認し、バージョン番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="930aa-188">Confirm installation and get the version number: `mongod --version`</span></span>

<span data-ttu-id="930aa-189">MongoDB をインストールした後は、次の 3 つのコマンドについて覚えておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="930aa-189">There are 3 commands you need to know once MongoDB is installed:</span></span>

- <span data-ttu-id="930aa-190">データベースの状態を確認する `sudo service mongodb status`</span><span class="sxs-lookup"><span data-stu-id="930aa-190">`sudo service mongodb status` for checking the status of your database.</span></span>
- <span data-ttu-id="930aa-191">データベースの実行を開始する `sudo service mongodb start`</span><span class="sxs-lookup"><span data-stu-id="930aa-191">`sudo service mongodb start`  to start running your database.</span></span>
- <span data-ttu-id="930aa-192">データベースの実行を停止する `sudo service mongodb stop`</span><span class="sxs-lookup"><span data-stu-id="930aa-192">`sudo service mongodb stop` to stop running your database.</span></span>

> [!NOTE]
> <span data-ttu-id="930aa-193">チュートリアルや記事で、`sudo systemctl status mongodb` コマンドが使用されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="930aa-193">You might see the command `sudo systemctl status mongodb` used in tutorials or articles.</span></span> <span data-ttu-id="930aa-194">軽量状態を維持するために、WSL には `systemd` (Linux のサービス管理システム) は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="930aa-194">In order to remain lightweight, WSL does not include `systemd` (a service management system in Linux).</span></span> <span data-ttu-id="930aa-195">代わりに、SysVinit を使用してマシン上のサービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="930aa-195">Instead, it uses SysVinit to start services on your machine.</span></span> <span data-ttu-id="930aa-196">違いはほとんどありませんが、チュートリアルで `sudo systemctl` が使用されている場合は、代わりに `sudo /etc/init.d/` を使用します。</span><span class="sxs-lookup"><span data-stu-id="930aa-196">You shouldn't notice a difference, but if a tutorial recommends using `sudo systemctl`, instead use: `sudo /etc/init.d/`.</span></span> <span data-ttu-id="930aa-197">たとえば、`sudo /etc/inid.d/mongodb status` は WSL では `sudo systemctl status mongodb` になります。または、`sudo service mongodb status` を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="930aa-197">For example, `sudo systemctl status mongodb`, for WSL would be `sudo /etc/inid.d/mongodb status` ...or you can also use `sudo service mongodb status`.</span></span>

<span data-ttu-id="930aa-198">ローカルサーバーで Mongo データベースを実行するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="930aa-198">To run your Mongo database in a local server:</span></span>

1. <span data-ttu-id="930aa-199">データベースの状態を確認します。データベースを既に起動している場合を `sudo service mongodb status` 除き、[Fail] (失敗) の応答が表示されます。</span><span class="sxs-lookup"><span data-stu-id="930aa-199">Check the status of your database: `sudo service mongodb status` You should see a [Fail] response, unless you've already started your database.</span></span>

2. <span data-ttu-id="930aa-200">データベースを起動します。 `sudo service mongodb start` [OK] の応答が表示されます。</span><span class="sxs-lookup"><span data-stu-id="930aa-200">Start your database: `sudo service mongodb start` You should now see an [OK] response.</span></span>

3. <span data-ttu-id="930aa-201">データベースサーバーに接続し、診断コマンドを実行して確認します。これにより、 `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` 現在のデータベースのバージョン、サーバーのアドレスとポート、および status コマンドの出力が出力されます。</span><span class="sxs-lookup"><span data-stu-id="930aa-201">Verify by connecting to the database server and running a diagnostic command: `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` This will output the current database version, the server address and port, and the output of the status command.</span></span> <span data-ttu-id="930aa-202">応答の "ok" フィールドに `1` の値は、サーバーが動作していることを示しています。</span><span class="sxs-lookup"><span data-stu-id="930aa-202">A value of `1` for the "ok" field in the response indicates that the server is working.</span></span>

4. <span data-ttu-id="930aa-203">MongoDB のサービスの実行を停止するには、`sudo service mongodb stop` と入力します。</span><span class="sxs-lookup"><span data-stu-id="930aa-203">To stop your MongoDB service from running, enter: `sudo service mongodb stop`</span></span>

> [!NOTE]
> <span data-ttu-id="930aa-204">MongoDB には、データを /data/db に格納する、ポート 27017 で実行するなど、いくつかの既定のパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="930aa-204">MongoDB has several default parameters, including storing data in /data/db and running on port 27017.</span></span> <span data-ttu-id="930aa-205">また、`mongod` はデーモン (データベースのホスト プロセス) であり、`mongo` は `mongod` の特定のインスタンスに接続するコマンドライン シェルです。</span><span class="sxs-lookup"><span data-stu-id="930aa-205">Also, `mongod` is the daemon (host process for the database) and `mongo` is the command-line shell that connects to a specific instance of `mongod`.</span></span>

<span data-ttu-id="930aa-206">VS Code は、 [Azure CosmosDB 拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb)を使用した mongodb データベースの操作をサポートしており、VS Code 内から mongodb データベースを作成、管理、クエリできます。</span><span class="sxs-lookup"><span data-stu-id="930aa-206">VS Code supports working with MongoDB databases via the [Azure CosmosDB extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb), you can create, manage and query MongoDB databases from within VS Code.</span></span> <span data-ttu-id="930aa-207">詳細については、「VS Code ドキュメント: [MongoDB の](https://code.visualstudio.com/docs/azure/mongodb)使用」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-207">To learn more, visit the VS Code docs: [Working with MongoDB](https://code.visualstudio.com/docs/azure/mongodb).</span></span>

<span data-ttu-id="930aa-208">詳細については、MongoDB のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-208">Learn more in the MongoDB docs:</span></span>

- [<span data-ttu-id="930aa-209">MongoDB の使用の概要</span><span class="sxs-lookup"><span data-stu-id="930aa-209">Introduction to using MongoDB</span></span>](https://docs.mongodb.com/manual/introduction/)
- [<span data-ttu-id="930aa-210">ユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="930aa-210">Create users</span></span>](https://docs.mongodb.com/manual/tutorial/create-users/)
- [<span data-ttu-id="930aa-211">リモートホスト上の MongoDB インスタンスに接続する</span><span class="sxs-lookup"><span data-stu-id="930aa-211">Connect to a MongoDB instance on a remote host</span></span>](https://docs.mongodb.com/manual/mongo/#mongodb-instance-on-a-remote-host)
- [<span data-ttu-id="930aa-212">CRUD: 作成、読み取り、更新、削除</span><span class="sxs-lookup"><span data-stu-id="930aa-212">CRUD: Create, Read, Update, Delete</span></span>](https://docs.mongodb.com/manual/crud/)
- [<span data-ttu-id="930aa-213">リファレンスドキュメント</span><span class="sxs-lookup"><span data-stu-id="930aa-213">Reference Docs</span></span>](https://docs.mongodb.com/manual/reference/)

## <a name="install-microsoft-sql-server"></a><span data-ttu-id="930aa-214">Microsoft SQL Server のインストール:</span><span class="sxs-lookup"><span data-stu-id="930aa-214">Install Microsoft SQL Server</span></span>

<span data-ttu-id="930aa-215">WSL (Ubuntu 18.04) に SQL Server をインストールするには、次のクイックスタートに従ってください。 [ubuntu で SQL Server をインストールし、データベースを作成](/sql/linux/quickstart-install-connect-ubuntu)します。</span><span class="sxs-lookup"><span data-stu-id="930aa-215">To install SQL Server on WSL (Ubuntu 18.04), follow this quickstart: [Install SQL Server and create a database on Ubuntu](/sql/linux/quickstart-install-connect-ubuntu).</span></span>

<span data-ttu-id="930aa-216">VS Code で Microsoft SQL Server データベースを操作するには、 [MSSQL 拡張子](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql)を試してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-216">To work with Microsoft SQL Server databases in VS Code, try the [MSSQL extension](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).</span></span>

## <a name="install-sqlite"></a><span data-ttu-id="930aa-217">SQLite をインストールする</span><span class="sxs-lookup"><span data-stu-id="930aa-217">Install SQLite</span></span>

<span data-ttu-id="930aa-218">WSL に SQLite をインストールするには (Ubuntu 18.04):</span><span class="sxs-lookup"><span data-stu-id="930aa-218">To install SQLite on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="930aa-219">WSL ターミナルを開きます (Ubuntu 18.04)。</span><span class="sxs-lookup"><span data-stu-id="930aa-219">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="930aa-220">`sudo apt update` を実行して Ubuntu パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="930aa-220">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="930aa-221">パッケージが更新されたら、次のように SQLite3 をインストールします。 `sudo apt install sqlite3`</span><span class="sxs-lookup"><span data-stu-id="930aa-221">Once the packages have updated, install SQLite3 with: `sudo apt install sqlite3`</span></span>
4. <span data-ttu-id="930aa-222">`sqlite3 --version` を実行してインストールを確認し、バージョン番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="930aa-222">Confirm installation and get the version number: `sqlite3 --version`</span></span>

<span data-ttu-id="930aa-223">"Example. db" という名前のテストデータベースを作成するには、次のように入力します。 `sqlite3 example.db`</span><span class="sxs-lookup"><span data-stu-id="930aa-223">To create a test database, called "example.db", enter: `sqlite3 example.db`</span></span>

<span data-ttu-id="930aa-224">SQLite データベースの一覧を表示するには、次のように入力します。 `.databases`</span><span class="sxs-lookup"><span data-stu-id="930aa-224">To see a list of your SQLite databases, enter: `.databases`</span></span>

<span data-ttu-id="930aa-225">データベースの状態を確認するには、次のように入力します。 `.dbinfo ?DB?`</span><span class="sxs-lookup"><span data-stu-id="930aa-225">To see the status of your database, enter: `.dbinfo ?DB?`</span></span>

<span data-ttu-id="930aa-226">SQLite プロンプトを終了するには、次のように入力します。 `.exit`</span><span class="sxs-lookup"><span data-stu-id="930aa-226">To exit the SQLite prompt, enter: `.exit`</span></span>

<span data-ttu-id="930aa-227">SQLite データベースの操作の詳細については、 [sqlite のドキュメント](https://www.sqlite.org/quickstart.html)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-227">For more information about working with a SQLite database, see the [SQLite docs](https://www.sqlite.org/quickstart.html).</span></span>

<span data-ttu-id="930aa-228">VS Code で SQLite データベースを使用するには、 [sqlite 拡張機能](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools)を試してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-228">To work with SQLite databases in VS Code, try the [SQLite extension](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).</span></span>

## <a name="install-redis"></a><span data-ttu-id="930aa-229">Redis のインストール</span><span class="sxs-lookup"><span data-stu-id="930aa-229">Install Redis</span></span>

<span data-ttu-id="930aa-230">WSL に Redis をインストールするには (Ubuntu 18.04):</span><span class="sxs-lookup"><span data-stu-id="930aa-230">To install Redis on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="930aa-231">WSL ターミナルを開きます (Ubuntu 18.04)。</span><span class="sxs-lookup"><span data-stu-id="930aa-231">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="930aa-232">`sudo apt update` を実行して Ubuntu パッケージを更新します。</span><span class="sxs-lookup"><span data-stu-id="930aa-232">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="930aa-233">パッケージが更新されたら、次のものを使用して Redis をインストールします。 `sudo apt install redis-server`</span><span class="sxs-lookup"><span data-stu-id="930aa-233">Once the packages have updated, install Redis with: `sudo apt install redis-server`</span></span>
4. <span data-ttu-id="930aa-234">`redis-server --version` を実行してインストールを確認し、バージョン番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="930aa-234">Confirm installation and get the version number: `redis-server --version`</span></span>

<span data-ttu-id="930aa-235">Redis サーバーの実行を開始するには、次のようにします。 `sudo service redis-server start`</span><span class="sxs-lookup"><span data-stu-id="930aa-235">To start running your Redis server: `sudo service redis-server start`</span></span>

<span data-ttu-id="930aa-236">Redis が動作しているかどうかを確認します (redis は、Redis と対話するためのコマンドラインインターフェイスユーティリティです)。これにより、 `redis-cli ping` "、" という応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="930aa-236">Check to see if redis is working (redis-cli is the command line interface utility to talk with Redis): `redis-cli ping` this should return a reply of "PONG".</span></span>

<span data-ttu-id="930aa-237">Redis サーバーの実行を停止するには、次のようにします。 `sudo service redis-server stop`</span><span class="sxs-lookup"><span data-stu-id="930aa-237">To stop running your Redis server: `sudo service redis-server stop`</span></span>

<span data-ttu-id="930aa-238">Redis データベースの使用方法の詳細については、 [redis のドキュメント](https://redis.io/topics/quickstart)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-238">For more information about working with a Redis database, see the [Redis docs](https://redis.io/topics/quickstart).</span></span>

<span data-ttu-id="930aa-239">VS Code で Redis データベースを使用するには、 [redis 拡張機能](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client)を試してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-239">To work with Redis databases in VS Code, try the [Redis extension](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).</span></span>

## <a name="see-services-running-and-set-up-profile-aliases"></a><span data-ttu-id="930aa-240">「実行中のサービス」と「プロファイルの別名の設定」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-240">See services running and set up profile aliases</span></span>

<span data-ttu-id="930aa-241">現在 WSL ディストリビューションで実行されているサービスを表示するには、次のように入力します。 `service --status-all`</span><span class="sxs-lookup"><span data-stu-id="930aa-241">To see the services that you currently have running on your WSL distribution, enter: `service --status-all`</span></span>

<span data-ttu-id="930aa-242">`sudo service mongodb start`、`sudo service postgres start`、`sudo -u postgrest psql` などの入力は面倒な場合があります。</span><span class="sxs-lookup"><span data-stu-id="930aa-242">Typing out `sudo service mongodb start` or `sudo service postgres start` and `sudo -u postgrest psql` can get tedious.</span></span>  <span data-ttu-id="930aa-243">これらのコマンドをすばやく使えるように、また覚えやすくするために、WSL 上の `.profile` ファイルでエイリアスを設定することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-243">However, you could consider setting up aliases in your `.profile` file on WSL to make these commands quicker to use and easier to remember.</span></span>

<span data-ttu-id="930aa-244">これらのコマンドを実行するためのカスタム エイリアス (ショートカット) を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="930aa-244">To set up your own custom alias, or shortcut, for executing these commands:</span></span>

1. <span data-ttu-id="930aa-245">WSL ターミナルを開き、`cd ~` と入力してルート ディレクトリに移動します。</span><span class="sxs-lookup"><span data-stu-id="930aa-245">Open your WSL terminal and enter `cd ~` to be sure you're in the root directory.</span></span>
2. <span data-ttu-id="930aa-246">`sudo nano .profile` と入力して、ターミナルの設定を制御する `.profile` ファイルを、ターミナルのテキスト エディター Nano で開きます。</span><span class="sxs-lookup"><span data-stu-id="930aa-246">Open the `.profile` file, which controls the settings for your terminal, with the terminal text editor, Nano: `sudo nano .profile`</span></span>
3. <span data-ttu-id="930aa-247">ファイルの最後に次の内容を追加します (`# set PATH` 設定は変更しないでください)。</span><span class="sxs-lookup"><span data-stu-id="930aa-247">At the bottom of the file (don't change the `# set PATH` settings), add the following:</span></span>

    ```bash
    # My Aliases
    alias start-pg='sudo service postgresql start'
    alias run-pg='sudo -u postgres psql'
    ```

    <span data-ttu-id="930aa-248">以後、`start-pg` と入力して postgresql サービスの実行を開始し、`run-pg` と入力して psql シェルを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="930aa-248">This will allow you to enter `start-pg` to start running the postgresql service and `run-pg` to open the psql shell.</span></span> <span data-ttu-id="930aa-249">`start-pg` および `run-pg` は任意の名前に変更できますが、postgres が既に使用しているコマンドを上書きしないよう注意してください。</span><span class="sxs-lookup"><span data-stu-id="930aa-249">You can change `start-pg` and `run-pg` to whatever names you want, just be careful not to overwrite a command that postgres already uses!</span></span>

4. <span data-ttu-id="930aa-250">新しいエイリアスを追加したら、**Ctrl + X** キーを使用して Nano テキスト エディターを終了し、保存の確認に対して `Y` (はい) を選択して Enter キーを押します (ファイル名は `.profile` のままにします)。</span><span class="sxs-lookup"><span data-stu-id="930aa-250">Once you've added your new aliases, exit the Nano text editor using **Ctrl+X** -- select `Y` (Yes) when prompted to save and Enter (leaving the file name as `.profile`).</span></span>
5. <span data-ttu-id="930aa-251">WSL ターミナルを閉じて開き直してから、新しいエイリアス コマンドを試してみてください。</span><span class="sxs-lookup"><span data-stu-id="930aa-251">Close and re-open your WSL terminal, then try your new alias commands.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="930aa-252">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="930aa-252">Additional resources</span></span>

- [<span data-ttu-id="930aa-253">Windows 10 での開発環境のセットアップ</span><span class="sxs-lookup"><span data-stu-id="930aa-253">Setting up your development environment on Windows 10</span></span>](/windows/dev-environment/)