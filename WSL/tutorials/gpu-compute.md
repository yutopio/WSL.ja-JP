---
title: Windows Subsystem for Linux の GPU アクセラレータ Machine Learning トレーニング
description: 詳細については、NVIDIA CUDA、DirectML、PyTorch の WSL 2 サポートに関するページを参照してください。
keywords: wsl、windows、windows サブシステム、gpu コンピューティング、gpu アクセラレーション、NVIDIA、CUDA、DirectML、、PyTorch、NVIDIA CUDA preview、GPU ドライバー、NVIDIA Container Toolkit、Docker
ms.date: 06/17/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: f101022dec534055905b25619a6c4fcee36f3f7d
ms.sourcegitcommit: 031a74801e03a90aed4b34c4fd5bfe964fc30994
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2020
ms.locfileid: "84947412"
---
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a><span data-ttu-id="e7816-104">Windows Subsystem for Linux での GPU アクセラレータによる機械学習トレーニング</span><span class="sxs-lookup"><span data-stu-id="e7816-104">GPU accelerated machine learning training in the Windows Subsystem for Linux</span></span>

<span data-ttu-id="e7816-105">GPU コンピューティングのサポートは、最も要求の厳しい WSL 機能 #1、Windows Insider プログラムを使用してプレビューできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e7816-105">Support for GPU compute, the #1 most requested WSL feature, is now available for preview via the Windows Insider program.</span></span> <span data-ttu-id="e7816-106">[ブログの投稿をお読みください](https://blogs.windows.com/windowsdeveloper/?p=55781)。</span><span class="sxs-lookup"><span data-stu-id="e7816-106">[Read the blog post](https://blogs.windows.com/windowsdeveloper/?p=55781).</span></span>

## <a name="what-is-gpu-compute"></a><span data-ttu-id="e7816-107">GPU コンピューティングとは</span><span class="sxs-lookup"><span data-stu-id="e7816-107">What is GPU compute?</span></span>

<span data-ttu-id="e7816-108">多くのコンピューティング処理を要するタスクで GPU アクセラレーションを利用することは、"GPU コンピューティング" と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e7816-108">Leveraging GPU acceleration for compute-intensive tasks is generally referred  to as "GPU compute".</span></span> <span data-ttu-id="e7816-109">GPU コンピューティングでは、GPU (グラフィックスプロセッシングユニット) を活用して、計算量の多いワークロードを高速化し、並列処理を使用して、多くの場合、CPU だけを利用するよりも、必要な計算を高速に実行します。</span><span class="sxs-lookup"><span data-stu-id="e7816-109">GPU computing leverages the GPU (graphics processing unit) to accelerate math heavy workloads and uses its parallel processing to complete the required calculations faster, in many cases, than utilizing only a CPU.</span></span> <span data-ttu-id="e7816-110">この並列処理によって、CPU 上で実行されている場合に、これらの計算負荷が高いワークロードで処理速度が大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="e7816-110">This parallelization enables significant processing speed improvements for these math heavy workloads then when running on a CPU.</span></span> <span data-ttu-id="e7816-111">機械学習モデルのトレーニングは、このような負荷の高いタスクを実行するために GPU コンピューティングによって時間が大幅に短縮される優れた例です。</span><span class="sxs-lookup"><span data-stu-id="e7816-111">Training machine learning models is a great example in which GPU compute can significantly accelerate the time to complete this computationally expensive task.</span></span>

## <a name="install-and-set-up"></a><span data-ttu-id="e7816-112">インストールと設定</span><span class="sxs-lookup"><span data-stu-id="e7816-112">Install and set up</span></span>

<span data-ttu-id="e7816-113">WSL 2 のサポートと、DirectML ドキュメント内の[GPU アクセラレーショントレーニングガイド](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training)で機械学習モデルのトレーニングを開始する方法の詳細については、こちらを参照してください。このガイドの内容は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e7816-113">Learn more about WSL 2 support and how to start training machine learning models in the [GPU Accelerated Training guide](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training) inside the DirectML docs. This guide covers:</span></span>

* <span data-ttu-id="e7816-114">DirectML を使用した、初級または学生向けのセットアップに関するガイダンス</span><span class="sxs-lookup"><span data-stu-id="e7816-114">Guidance for beginners or students to set up TensorFlow with DirectML</span></span>
* <span data-ttu-id="e7816-115">既存の CUDA ML ワークフローの実行を開始するためのプロフェッショナル向けガイダンス</span><span class="sxs-lookup"><span data-stu-id="e7816-115">Guidance for professionals to start running their exisiting CUDA ML workflows</span></span>
