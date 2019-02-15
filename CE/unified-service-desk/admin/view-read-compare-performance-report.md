---
title: View, read, and compare Unified Service Desk performance report | MicrosoftDocs
description: Learn on how to view, read, and compare different Unified Service Desk performance report generated using the Unified Service Desk Performance Analyzer.
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
ms.assetid: 787A5201-588B-4ECC-9E5F-BCCBFC1EE482
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
monikerRange: '>= dynamics-usd-3'
ms.openlocfilehash: 81aff38bb2ecd94309ee9fd4e229bac293b8ce8e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382354"
---
# <a name="public-preview-view-read-and-compare-unified-service-desk-performance-report"></a><span data-ttu-id="d51f6-103">Public Preview: View, read, and compare Unified Service Desk performance report</span><span class="sxs-lookup"><span data-stu-id="d51f6-103">Public Preview: View, read, and compare Unified Service Desk performance report</span></span>

[!INCLUDE[cc-beta-prerelease-disclaimer](../../includes/cc-beta-prerelease-disclaimer.md)]

## <a name="view-the-performance-report-for-a-performance-session"></a><span data-ttu-id="d51f6-104">View the performance report for a performance session</span><span class="sxs-lookup"><span data-stu-id="d51f6-104">View the performance report for a performance session</span></span>

<span data-ttu-id="d51f6-105">You can see a report with the performance session Id in the left pane.</span><span class="sxs-lookup"><span data-stu-id="d51f6-105">You can see a report with the performance session Id in the left pane.</span></span> <span data-ttu-id="d51f6-106">Selecting the report, you can see all the operations from various categories, and time consumed for the different percentiles in milliseconds.</span><span class="sxs-lookup"><span data-stu-id="d51f6-106">Selecting the report, you can see all the operations from various categories, and time consumed for the different percentiles in milliseconds.</span></span>

<span data-ttu-id="d51f6-107">![View the performance report for performance session](../media/individual-perf-report.PNG "View the performance report for performance session")</span><span class="sxs-lookup"><span data-stu-id="d51f6-107">![View the performance report for performance session](../media/individual-perf-report.PNG "View the performance report for performance session")</span></span>

## <a name="compare-operations-from-different-reports-performance-session"></a><span data-ttu-id="d51f6-108">Compare operations from different reports (performance session)</span><span class="sxs-lookup"><span data-stu-id="d51f6-108">Compare operations from different reports (performance session)</span></span>

<span data-ttu-id="d51f6-109">Use the **Reports comparison** tab to review the comparative analysis of different operations based on the individual reports displayed in the performance report.</span><span class="sxs-lookup"><span data-stu-id="d51f6-109">Use the **Reports comparison** tab to review the comparative analysis of different operations based on the individual reports displayed in the performance report.</span></span> <span data-ttu-id="d51f6-110">The Report comparison tab displays sub tabs that has comparative analysis based on the percentiles.</span><span class="sxs-lookup"><span data-stu-id="d51f6-110">The Report comparison tab displays sub tabs that has comparative analysis based on the percentiles.</span></span> <span data-ttu-id="d51f6-111">You can view the comparative analysis for 50th, 75th, 90th, 95th, and 99th percentile.</span><span class="sxs-lookup"><span data-stu-id="d51f6-111">You can view the comparative analysis for 50th, 75th, 90th, 95th, and 99th percentile.</span></span> <span data-ttu-id="d51f6-112">The report shows **Operations ID** with an alphabet suffix and displays the comparison in terms of percentage.</span><span class="sxs-lookup"><span data-stu-id="d51f6-112">The report shows **Operations ID** with an alphabet suffix and displays the comparison in terms of percentage.</span></span> 

<span data-ttu-id="d51f6-113">For example, time taken for the **Browser Navigation** operation under the category, **Load Dashboard** from the two different reports shows with the Operation ID.</span><span class="sxs-lookup"><span data-stu-id="d51f6-113">For example, time taken for the **Browser Navigation** operation under the category, **Load Dashboard** from the two different reports shows with the Operation ID.</span></span> <span data-ttu-id="d51f6-114">You can see the comparison between these operations displayed as **(a) vs (b)** in terms of percentage.</span><span class="sxs-lookup"><span data-stu-id="d51f6-114">You can see the comparison between these operations displayed as **(a) vs (b)** in terms of percentage.</span></span>

<span data-ttu-id="d51f6-115">![Compare the performance report for different performance session](../media/compare-reports.PNG "Compare the performance report for different performance session")</span><span class="sxs-lookup"><span data-stu-id="d51f6-115">![Compare the performance report for different performance session](../media/compare-reports.PNG "Compare the performance report for different performance session")</span></span>

> [!NOTE]
> <span data-ttu-id="d51f6-116">The readability and legibility of the comparison works best when you view three performance sessions in a report.</span><span class="sxs-lookup"><span data-stu-id="d51f6-116">The readability and legibility of the comparison works best when you view three performance sessions in a report.</span></span>

## <a name="view-performance-timeline-graph-and-performance-details-table"></a><span data-ttu-id="d51f6-117">View performance timeline graph and Performance details table</span><span class="sxs-lookup"><span data-stu-id="d51f6-117">View performance timeline graph and Performance details table</span></span>

1. <span data-ttu-id="d51f6-118">Select a performance session ID from the left pane of the report.</span><span class="sxs-lookup"><span data-stu-id="d51f6-118">Select a performance session ID from the left pane of the report.</span></span>

2. <span data-ttu-id="d51f6-119">Select an operation from the list.</span><span class="sxs-lookup"><span data-stu-id="d51f6-119">Select an operation from the list.</span></span><br>
<span data-ttu-id="d51f6-120">![Select a operation from the list of operations](../media/operation-navigation.PNG "Select a operation from the list of operations")</span><span class="sxs-lookup"><span data-stu-id="d51f6-120">![Select a operation from the list of operations](../media/operation-navigation.PNG "Select a operation from the list of operations")</span></span>

3. <span data-ttu-id="d51f6-121">Select the correlation ID from the list.</span><span class="sxs-lookup"><span data-stu-id="d51f6-121">Select the correlation ID from the list.</span></span><br>
<span data-ttu-id="d51f6-122">![Select a correlation ID from the list](../media/operation-navigation-correlationid.PNG "Select a correlation ID from the list")</span><span class="sxs-lookup"><span data-stu-id="d51f6-122">![Select a correlation ID from the list](../media/operation-navigation-correlationid.PNG "Select a correlation ID from the list")</span></span>

<span data-ttu-id="d51f6-123">The report displays the Performance timeline graph and Performance details table.</span><span class="sxs-lookup"><span data-stu-id="d51f6-123">The report displays the Performance timeline graph and Performance details table.</span></span>

<span data-ttu-id="d51f6-124">![Performance timeline graph](../media/performance-timeline-graph.PNG "Performance timeline graph")</span><span class="sxs-lookup"><span data-stu-id="d51f6-124">![Performance timeline graph](../media/performance-timeline-graph.PNG "Performance timeline graph")</span></span>

<span data-ttu-id="d51f6-125">![Performance details table](../media/performance-details-table.PNG "Performance details table")</span><span class="sxs-lookup"><span data-stu-id="d51f6-125">![Performance details table](../media/performance-details-table.PNG "Performance details table")</span></span>

## <a name="read-the-performance-timeline-graph-and-the-details-table"></a><span data-ttu-id="d51f6-126">Read the performance timeline graph and the details table</span><span class="sxs-lookup"><span data-stu-id="d51f6-126">Read the performance timeline graph and the details table</span></span>

<span data-ttu-id="d51f6-127">The timeline graph displays the time taken for an operation in terms of time consumed by each method under every class.</span><span class="sxs-lookup"><span data-stu-id="d51f6-127">The timeline graph displays the time taken for an operation in terms of time consumed by each method under every class.</span></span> <span data-ttu-id="d51f6-128">The Y-axis displays the operation name and the X-axis displays the timeline.</span><span class="sxs-lookup"><span data-stu-id="d51f6-128">The Y-axis displays the operation name and the X-axis displays the timeline.</span></span>

<span data-ttu-id="d51f6-129">![Read the Performance report](../media/read-perf-timline.PNG "Read the Performance report")</span><span class="sxs-lookup"><span data-stu-id="d51f6-129">![Read the Performance report](../media/read-perf-timline.PNG "Read the Performance report")</span></span>

<span data-ttu-id="d51f6-130">Hover the cursor on any method name to see the time consumed.</span><span class="sxs-lookup"><span data-stu-id="d51f6-130">Hover the cursor on any method name to see the time consumed.</span></span>

<span data-ttu-id="d51f6-131">![Hover the cursor on any method to see the duration and name of the method](../media/hover-graph-details.PNG "Hover the cursor on any method to see the duration and name of the method")</span><span class="sxs-lookup"><span data-stu-id="d51f6-131">![Hover the cursor on any method to see the duration and name of the method](../media/hover-graph-details.PNG "Hover the cursor on any method to see the duration and name of the method")</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d51f6-132">Categories and operations</span><span class="sxs-lookup"><span data-stu-id="d51f6-132">Categories and operations</span></span>](operations-categories.md)

## <a name="see-also"></a><span data-ttu-id="d51f6-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d51f6-133">See also</span></span>

[<span data-ttu-id="d51f6-134">Overview of Unified Service Desk Performance Analyzer</span><span class="sxs-lookup"><span data-stu-id="d51f6-134">Overview of Unified Service Desk Performance Analyzer</span></span>](overview-performance-analyzer.md)

[<span data-ttu-id="d51f6-135">Download Unified Service Desk Performance Analyzer</span><span class="sxs-lookup"><span data-stu-id="d51f6-135">Download Unified Service Desk Performance Analyzer</span></span>](download-performance-analyzer.md)

[<span data-ttu-id="d51f6-136">Generate (collect) performance data log</span><span class="sxs-lookup"><span data-stu-id="d51f6-136">Generate (collect) performance data log</span></span>](performance-data-collection-using-keyboard-shortcut.md)

[<span data-ttu-id="d51f6-137">Generate performance report</span><span class="sxs-lookup"><span data-stu-id="d51f6-137">Generate performance report</span></span>](generate-performance-report.md)

[<span data-ttu-id="d51f6-138">Overview of performance report user interface</span><span class="sxs-lookup"><span data-stu-id="d51f6-138">Overview of performance report user interface</span></span>](overview-performance-report-user-interface.md)

[<span data-ttu-id="d51f6-139">Terminologies in the performance report</span><span class="sxs-lookup"><span data-stu-id="d51f6-139">Terminologies in the performance report</span></span>](terminologies-performance-report.md)