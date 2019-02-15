---
title: Terminologies in the performance report | MicrosoftDocs
description: Learn about the terminologies used in the Unified Service Desk Performance Report generated using Unified Service Desk Performance Analyzer
ms.date: 10/31/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD, dyn365-admin
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 9512192E-A562-4EDE-BAF3-5AFB859BE80B
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
monikerRange: '>= dynamics-usd-3'
ms.openlocfilehash: 0be8f256de9d601111473c09bc50d8813c993887
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382585"
---
# <a name="public-preview-terminologies-in-the-performance-report"></a><span data-ttu-id="884c4-103">Public Preview: Terminologies in the performance report</span><span class="sxs-lookup"><span data-stu-id="884c4-103">Public Preview: Terminologies in the performance report</span></span>

[!INCLUDE[cc-beta-prerelease-disclaimer](../../includes/cc-beta-prerelease-disclaimer.md)]

<span data-ttu-id="884c4-104">When you view the performance report, you may come across certain terminologies.</span><span class="sxs-lookup"><span data-stu-id="884c4-104">When you view the performance report, you may come across certain terminologies.</span></span> <span data-ttu-id="884c4-105">Understanding the terminologies help you to read and analyze the performance report effectively and take a better course of action.</span><span class="sxs-lookup"><span data-stu-id="884c4-105">Understanding the terminologies help you to read and analyze the performance report effectively and take a better course of action.</span></span>

| <span data-ttu-id="884c4-106">Terms</span><span class="sxs-lookup"><span data-stu-id="884c4-106">Terms</span></span> | <span data-ttu-id="884c4-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="884c4-107">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="884c4-108">Thao tác</span><span class="sxs-lookup"><span data-stu-id="884c4-108">Operation</span></span> | <span data-ttu-id="884c4-109">The name of the operation executed during a performance session.</span><span class="sxs-lookup"><span data-stu-id="884c4-109">The name of the operation executed during a performance session.</span></span> <span data-ttu-id="884c4-110">It consists of multiple methods executed in various classes.</span><span class="sxs-lookup"><span data-stu-id="884c4-110">It consists of multiple methods executed in various classes.</span></span> |
| <span data-ttu-id="884c4-111">Count</span><span class="sxs-lookup"><span data-stu-id="884c4-111">Count</span></span> | <span data-ttu-id="884c4-112">The number of times an operation is executed in one performance session.</span><span class="sxs-lookup"><span data-stu-id="884c4-112">The number of times an operation is executed in one performance session.</span></span> <span data-ttu-id="884c4-113">In the consolidated report, it represents the total number of times a operation is executed across multiple performance sessions.</span><span class="sxs-lookup"><span data-stu-id="884c4-113">In the consolidated report, it represents the total number of times a operation is executed across multiple performance sessions.</span></span> |
| <span data-ttu-id="884c4-114">Percentile</span><span class="sxs-lookup"><span data-stu-id="884c4-114">Percentile</span></span> | <span data-ttu-id="884c4-115">The number of times the particular operation is executed within the time mentioned.</span><span class="sxs-lookup"><span data-stu-id="884c4-115">The number of times the particular operation is executed within the time mentioned.</span></span> <span data-ttu-id="884c4-116">50 percentile means 50% of the time the operation executed in t milliseconds.</span><span class="sxs-lookup"><span data-stu-id="884c4-116">50 percentile means 50% of the time the operation executed in t milliseconds.</span></span> |
| <span data-ttu-id="884c4-117">Performance Session ID</span><span class="sxs-lookup"><span data-stu-id="884c4-117">Performance Session ID</span></span> | <span data-ttu-id="884c4-118">A unique identifier assigned to an end-to-end session in which perfomance logging is enabled.</span><span class="sxs-lookup"><span data-stu-id="884c4-118">A unique identifier assigned to an end-to-end session in which perfomance logging is enabled.</span></span> <span data-ttu-id="884c4-119">This includes session creations, form loading, actions and so on.</span><span class="sxs-lookup"><span data-stu-id="884c4-119">This includes session creations, form loading, actions and so on.</span></span> |
| <span data-ttu-id="884c4-120">Danh mục</span><span class="sxs-lookup"><span data-stu-id="884c4-120">Category</span></span> | <span data-ttu-id="884c4-121">The operation category – we divide USD into chunks for example KB search, Form Loading, Boot etc. We split the operations into these buckets for better understanding.</span><span class="sxs-lookup"><span data-stu-id="884c4-121">The operation category – we divide USD into chunks for example KB search, Form Loading, Boot etc. We split the operations into these buckets for better understanding.</span></span> |
| <span data-ttu-id="884c4-122">ID Tương quan</span><span class="sxs-lookup"><span data-stu-id="884c4-122">Correlation ID</span></span> | <span data-ttu-id="884c4-123">A unique Identifier assigned to correlate the start and end of a particular operation.</span><span class="sxs-lookup"><span data-stu-id="884c4-123">A unique Identifier assigned to correlate the start and end of a particular operation.</span></span> |
| <span data-ttu-id="884c4-124">Hành động</span><span class="sxs-lookup"><span data-stu-id="884c4-124">Action</span></span> | <span data-ttu-id="884c4-125">The name of the operation.</span><span class="sxs-lookup"><span data-stu-id="884c4-125">The name of the operation.</span></span> |
| <span data-ttu-id="884c4-126">Start time</span><span class="sxs-lookup"><span data-stu-id="884c4-126">Start time</span></span> | <span data-ttu-id="884c4-127">The start time of the operation with respect to the start of the performance session.</span><span class="sxs-lookup"><span data-stu-id="884c4-127">The start time of the operation with respect to the start of the performance session.</span></span> |
| <span data-ttu-id="884c4-128">End time</span><span class="sxs-lookup"><span data-stu-id="884c4-128">End time</span></span> | <span data-ttu-id="884c4-129">The end time of the operation with respect to the end of the performance session.</span><span class="sxs-lookup"><span data-stu-id="884c4-129">The end time of the operation with respect to the end of the performance session.</span></span> |
| <span data-ttu-id="884c4-130">Total duration</span><span class="sxs-lookup"><span data-stu-id="884c4-130">Total duration</span></span> | <span data-ttu-id="884c4-131">The difference between the end time and start time of the operation in milliseconds.</span><span class="sxs-lookup"><span data-stu-id="884c4-131">The difference between the end time and start time of the operation in milliseconds.</span></span> |
| <span data-ttu-id="884c4-132">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="884c4-132">Method</span></span> | <span data-ttu-id="884c4-133">The method executed in a particular class for an operation.</span><span class="sxs-lookup"><span data-stu-id="884c4-133">The method executed in a particular class for an operation.</span></span> |
| <span data-ttu-id="884c4-134">Lớp</span><span class="sxs-lookup"><span data-stu-id="884c4-134">Class</span></span> | <span data-ttu-id="884c4-135">The classes for a particular operation.</span><span class="sxs-lookup"><span data-stu-id="884c4-135">The classes for a particular operation.</span></span> |

> [!div class="nextstepaction"]
> [<span data-ttu-id="884c4-136">View, read, and compare performance report</span><span class="sxs-lookup"><span data-stu-id="884c4-136">View, read, and compare performance report</span></span>](view-read-compare-performance-report.md)

## <a name="see-also"></a><span data-ttu-id="884c4-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="884c4-137">See also</span></span>

[<span data-ttu-id="884c4-138">Overview of Unified Service Desk Performance Analyzer</span><span class="sxs-lookup"><span data-stu-id="884c4-138">Overview of Unified Service Desk Performance Analyzer</span></span>](overview-performance-analyzer.md)

[<span data-ttu-id="884c4-139">Download Unified Service Desk Performance Analyzer</span><span class="sxs-lookup"><span data-stu-id="884c4-139">Download Unified Service Desk Performance Analyzer</span></span>](download-performance-analyzer.md)

[<span data-ttu-id="884c4-140">Generate (collect) performance data log</span><span class="sxs-lookup"><span data-stu-id="884c4-140">Generate (collect) performance data log</span></span>](performance-data-collection-using-keyboard-shortcut.md)

[<span data-ttu-id="884c4-141">Generate performance report</span><span class="sxs-lookup"><span data-stu-id="884c4-141">Generate performance report</span></span>](generate-performance-report.md)

[<span data-ttu-id="884c4-142">Overview of performance report user interface</span><span class="sxs-lookup"><span data-stu-id="884c4-142">Overview of performance report user interface</span></span>](overview-performance-report-user-interface.md)

[<span data-ttu-id="884c4-143">Categories and operations</span><span class="sxs-lookup"><span data-stu-id="884c4-143">Categories and operations</span></span>](operations-categories.md)
