---
title: 什么是 ML.NET？应该如何理解机器学习基础知识？
description: ML.NET 是一个免费的开源跨平台机器学习框架，可用于生成自定义 AI 解决方案并将其集成到 .NET 应用程序。
author: cjgronlund
ms.custom: seodec18
ms.topic: overview
ms.date: 11/06/2018
ms.openlocfilehash: fb0ece94d77c76fddc667070a8aaef154fd2053a
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2019
ms.locfileid: "55252416"
---
# <a name="what-is-mlnet-and-how-do-i-understand-machine-learning-basics"></a><span data-ttu-id="f372a-103">什么是 ML.NET？应该如何理解机器学习基础知识？</span><span class="sxs-lookup"><span data-stu-id="f372a-103">What is ML.NET and how do I understand Machine Learning basics?</span></span>

<span data-ttu-id="f372a-104">ML.NET 是一个免费的开源跨平台机器学习框架，可用于生成自定义机器学习解决方案并将其集成到 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="f372a-104">ML.NET is a free, open-source, and cross-platform machine learning framework that enables you to build custom machine learning solutions and integrate them into your .NET applications.</span></span> <span data-ttu-id="f372a-105">借助 ML.NET API，可以使用你已有的 .NET 技能将 AI 结合到应用中，无需离开 .NET。</span><span class="sxs-lookup"><span data-stu-id="f372a-105">With the ML.NET APIs you can incorporate AI into your apps using the .NET skills you already have and without leaving .NET.</span></span>

## <a name="what-is-machine-learning"></a><span data-ttu-id="f372a-106">什么是机器学习？</span><span class="sxs-lookup"><span data-stu-id="f372a-106">What is machine learning?</span></span>

<span data-ttu-id="f372a-107">机器学习是一种允许计算机使用现有数据预测未来行为、结果和趋势的数据科学方法。</span><span class="sxs-lookup"><span data-stu-id="f372a-107">Machine learning is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes, and trends.</span></span> <span data-ttu-id="f372a-108">使用机器学习，计算机可以在未显式编程的情况下进行学习。</span><span class="sxs-lookup"><span data-stu-id="f372a-108">Using machine learning, computers learn without being explicitly programmed.</span></span>

<span data-ttu-id="f372a-109">机器学习的预测可以使得应用和设备更智能。</span><span class="sxs-lookup"><span data-stu-id="f372a-109">Forecasts or predictions from machine learning can make apps and devices smarter.</span></span> <span data-ttu-id="f372a-110">在线购物时，机器学习基于历史购买推荐你可能喜欢的其他产品。</span><span class="sxs-lookup"><span data-stu-id="f372a-110">When you shop online, machine learning helps recommend other products you might like based on what you've purchased.</span></span> <span data-ttu-id="f372a-111">刷信用卡时，机器学习将事务与事务数据库进行比较，帮助检测欺诈行为。</span><span class="sxs-lookup"><span data-stu-id="f372a-111">When your credit card is swiped, machine learning compares the transaction to a database of transactions and helps detect fraud.</span></span> <span data-ttu-id="f372a-112">当机器人吸尘器清理房间时，机器学习帮助其决定工作是否完成。</span><span class="sxs-lookup"><span data-stu-id="f372a-112">When your robot vacuum cleaner vacuums a room, machine learning helps it decide whether the job is done.</span></span>


## <a name="short-videos-on-data-science"></a><span data-ttu-id="f372a-113">数据科学的简短视频</span><span class="sxs-lookup"><span data-stu-id="f372a-113">Short videos on data science</span></span> 

<span data-ttu-id="f372a-114">从一位顶级数据科学家的五个有关“适合初学者的数据科学”的短片了解机器学习和数据科学基础知识的简介。</span><span class="sxs-lookup"><span data-stu-id="f372a-114">Get a quick introduction to the basics of machine learning and data science from *Data Science for Beginners* in five short videos from a top data scientist.</span></span> <span data-ttu-id="f372a-115">这些视频很基础但也很有用，适用于对数据科学感兴趣的人和与数据科学家合作的人。</span><span class="sxs-lookup"><span data-stu-id="f372a-115">These videos are basic but useful, whether you're interested in doing data science or you work with data scientists.</span></span>

* <span data-ttu-id="f372a-116">视频 1：[5 个数据科学问题的解答](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-the-5-questions-data-science-answers)（5 分 14 秒）。</span><span class="sxs-lookup"><span data-stu-id="f372a-116">Video 1: [The 5 questions data science answers](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-the-5-questions-data-science-answers) *(5 min 14 sec)*.</span></span>

* <span data-ttu-id="f372a-117">视频 2：[数据是否可用于数据科学？](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-is-your-data-ready-for-data-science)</span><span class="sxs-lookup"><span data-stu-id="f372a-117">Video 2: [Is your data ready for data science?](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-is-your-data-ready-for-data-science)</span></span> <span data-ttu-id="f372a-118">（4 分 56 秒）</span><span class="sxs-lookup"><span data-stu-id="f372a-118">*(4 min 56 sec)*</span></span>

* <span data-ttu-id="f372a-119">视频 3：[提出数据方面的可解答问题](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-ask-a-question-you-can-answer-with-data)（4 分 17 秒）</span><span class="sxs-lookup"><span data-stu-id="f372a-119">Video 3: [Ask a question you can answer with data](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-ask-a-question-you-can-answer-with-data) *(4 min 17 sec)*</span></span>

* <span data-ttu-id="f372a-120">视频 4：[使用简单的模型预测答案](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-predict-an-answer-with-a-simple-model)（7 分 42 秒）</span><span class="sxs-lookup"><span data-stu-id="f372a-120">Video 4: [Predict an answer with a simple model](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-predict-an-answer-with-a-simple-model) *(7 min 42 sec)*</span></span>

* <span data-ttu-id="f372a-121">视频 5：[复制他人的工作以研究数据科学](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-copy-other-peoples-work-to-do-data-science)（3 分 18 秒）</span><span class="sxs-lookup"><span data-stu-id="f372a-121">Video 5: [Copy other people's work to do data science](https://docs.microsoft.com/azure/machine-learning/studio/data-science-for-beginners-copy-other-peoples-work-to-do-data-science) *(3 min 18 sec)*</span></span>