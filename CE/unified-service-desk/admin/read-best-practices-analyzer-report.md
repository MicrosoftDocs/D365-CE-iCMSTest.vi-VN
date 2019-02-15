---
title: Read Best Practices Analyzer Report (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about how to read Best Practices Analyzer report.
ms.custom: ''
ms.date: 05/15/2018
ms.service: usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 4BACD2D6-A17D-468D-A2CB-F4BEEF06AE5E
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 01fe9350d09e145c3a8e7511f107a0ab70797159
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382364"
---
# <a name="read-best-practices-analyzer-report"></a><span data-ttu-id="8c2ac-103">Read Best Practices Analyzer report</span><span class="sxs-lookup"><span data-stu-id="8c2ac-103">Read Best Practices Analyzer report</span></span>

<span data-ttu-id="8c2ac-104">This section describes the layout of the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] report and provides information to help you understand the results of the analysis.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-104">This section describes the layout of the [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] report and provides information to help you understand the results of the analysis.</span></span>

<span data-ttu-id="8c2ac-105">![Read Best Practices Analyzer report](../media/bpa-read-report.gif "Read Best Practices Analyzer report")</span><span class="sxs-lookup"><span data-stu-id="8c2ac-105">![Read Best Practices Analyzer report](../media/bpa-read-report.gif "Read Best Practices Analyzer report")</span></span>

<span data-ttu-id="8c2ac-106">![Best Practices Analyzer report](../media/bpa-report.PNG "Best Practices Analyzer report")</span><span class="sxs-lookup"><span data-stu-id="8c2ac-106">![Best Practices Analyzer report](../media/bpa-report.PNG "Best Practices Analyzer report")</span></span>

<span data-ttu-id="8c2ac-107">The report displays the following elements:</span><span class="sxs-lookup"><span data-stu-id="8c2ac-107">The report displays the following elements:</span></span>


|       <span data-ttu-id="8c2ac-108">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="8c2ac-108">Element</span></span>       |                                                                                                                        <span data-ttu-id="8c2ac-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8c2ac-109">Description</span></span>                                                                                                                         |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|      <span data-ttu-id="8c2ac-110">Tải xuống</span><span class="sxs-lookup"><span data-stu-id="8c2ac-110">Downloads</span></span>      |                                 <span data-ttu-id="8c2ac-111">This is the location where the generated report is maintained.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-111">This is the location where the generated report is maintained.</span></span><br><br>`C:\Users\\\<User>\AppData\Roaming\Microsoft\Microsoft Dynamics® 365 Unified Service Desk\\\<Version>\BPA\BPALogs\`                                  |
|    <span data-ttu-id="8c2ac-112">Computer name</span><span class="sxs-lookup"><span data-stu-id="8c2ac-112">Computer name</span></span>    |                                                         <span data-ttu-id="8c2ac-113">Local computer name on which [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] performed the analysis.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-113">Local computer name on which [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] performed the analysis.</span></span>                                                          |
| <span data-ttu-id="8c2ac-114">Analysis Start Time</span><span class="sxs-lookup"><span data-stu-id="8c2ac-114">Analysis Start Time</span></span> |                                                       <span data-ttu-id="8c2ac-115">The time at which the you start analysis.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-115">The time at which the you start analysis.</span></span> <span data-ttu-id="8c2ac-116">The format of the Analysis Start Time appears as a timestamp in the format <MM-DD-YYYY> <HH:MM:SS>.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-116">The format of the Analysis Start Time appears as a timestamp in the format <MM-DD-YYYY> <HH:MM:SS>.</span></span>                                                        |
|    <span data-ttu-id="8c2ac-117">Analysis Time</span><span class="sxs-lookup"><span data-stu-id="8c2ac-117">Analysis Time</span></span>    |                                                                                                    <span data-ttu-id="8c2ac-118">The time taken in seconds to complete the analysis.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-118">The time taken in seconds to complete the analysis.</span></span>                                                                                                     |
|        <span data-ttu-id="8c2ac-119">Score</span><span class="sxs-lookup"><span data-stu-id="8c2ac-119">Score</span></span>        |                                                                                                 <span data-ttu-id="8c2ac-120">Number of parameters passed / Total number of parameters.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-120">Number of parameters passed / Total number of parameters.</span></span>                                                                                                  |
|      <span data-ttu-id="8c2ac-121">Tham số</span><span class="sxs-lookup"><span data-stu-id="8c2ac-121">Parameter</span></span>      |                                                          <span data-ttu-id="8c2ac-122">The parameter name against which [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] performs analysis.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-122">The parameter name against which [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] performs analysis.</span></span>                                                          |
|      <span data-ttu-id="8c2ac-123">Danh mục</span><span class="sxs-lookup"><span data-stu-id="8c2ac-123">Category</span></span>       | <span data-ttu-id="8c2ac-124">The category name under which the parameter is classified.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-124">The category name under which the parameter is classified.</span></span> <br> <span data-ttu-id="8c2ac-125">Clicking on the **Category** list, you can filter the categories to see information under those categories.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-125">Clicking on the **Category** list, you can filter the categories to see information under those categories.</span></span><br><br> <span data-ttu-id="8c2ac-126">![Category Filter](../media/bpa-category-filter.PNG "Category Filter")</span><span class="sxs-lookup"><span data-stu-id="8c2ac-126">![Category Filter](../media/bpa-category-filter.PNG "Category Filter")</span></span> |
|       <span data-ttu-id="8c2ac-127">Kết quả</span><span class="sxs-lookup"><span data-stu-id="8c2ac-127">Result</span></span>        |                                                                                                           <span data-ttu-id="8c2ac-128">The analysis result of the parameter.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-128">The analysis result of the parameter.</span></span>                                                                                                            |

## <a name="expand-parameter-to-see-details"></a><span data-ttu-id="8c2ac-129">Expand parameter to see details</span><span class="sxs-lookup"><span data-stu-id="8c2ac-129">Expand parameter to see details</span></span>

<span data-ttu-id="8c2ac-130">You must expand a parameter to see the details, which illustrate the following:</span><span class="sxs-lookup"><span data-stu-id="8c2ac-130">You must expand a parameter to see the details, which illustrate the following:</span></span>


|      <span data-ttu-id="8c2ac-131">Yếu tố</span><span class="sxs-lookup"><span data-stu-id="8c2ac-131">Element</span></span>      |                                                                        <span data-ttu-id="8c2ac-132">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8c2ac-132">Description</span></span>                                                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="8c2ac-133">Current Value</span><span class="sxs-lookup"><span data-stu-id="8c2ac-133">Current Value</span></span>   |                                                             <span data-ttu-id="8c2ac-134">This is the value you configure.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-134">This is the value you configure.</span></span>                                                              |
| <span data-ttu-id="8c2ac-135">Recommended Value</span><span class="sxs-lookup"><span data-stu-id="8c2ac-135">Recommended Value</span></span> |            <span data-ttu-id="8c2ac-136">This is the value that [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] recommends configuring.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-136">This is the value that [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] recommends configuring.</span></span>            |
|    <span data-ttu-id="8c2ac-137">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8c2ac-137">Description</span></span>    |                                                       <span data-ttu-id="8c2ac-138">This is the description about the parameter.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-138">This is the description about the parameter.</span></span>                                                        |
| <span data-ttu-id="8c2ac-139">Mitigation Steps</span><span class="sxs-lookup"><span data-stu-id="8c2ac-139">Mitigation Steps</span></span>  | <span data-ttu-id="8c2ac-140">These are the steps that you must perform to mitigate the issue.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-140">These are the steps that you must perform to mitigate the issue.</span></span></br> <span data-ttu-id="8c2ac-141">**Note:** The mitigation steps appear when the report displays an error or warning.</span><span class="sxs-lookup"><span data-stu-id="8c2ac-141">**Note:** The mitigation steps appear when the report displays an error or warning.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8c2ac-142">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8c2ac-142">See also</span></span>

[<span data-ttu-id="8c2ac-143">Analyze best practices in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="8c2ac-143">Analyze best practices in Unified Service Desk</span></span>](../admin/analyze-best-practices-unified-service-desk.md)

[<span data-ttu-id="8c2ac-144">Download and install Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="8c2ac-144">Download and install Best Practices Analyzer</span></span>](../admin/download-install-best-practices-analyzer.md)

[<span data-ttu-id="8c2ac-145">Walkthrough: Configure Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="8c2ac-145">Walkthrough: Configure Best Practices Analyzer</span></span>](../admin/walkthrough-configure-best-practices-analyzer.md)

[<span data-ttu-id="8c2ac-146">Best practice rule categories and parameters</span><span class="sxs-lookup"><span data-stu-id="8c2ac-146">Best practice rule categories and parameters</span></span>](../admin/compliance-categories-parameters-bpa.md)

[<span data-ttu-id="8c2ac-147">System configurations</span><span class="sxs-lookup"><span data-stu-id="8c2ac-147">System configurations</span></span>](../admin/system-configurations-bpa.md)

[<span data-ttu-id="8c2ac-148">Internet Explorer settings</span><span class="sxs-lookup"><span data-stu-id="8c2ac-148">Internet Explorer settings</span></span>](../admin/internet-explorer-settings-bpa.md)

[<span data-ttu-id="8c2ac-149">Unified Service Desk configurations</span><span class="sxs-lookup"><span data-stu-id="8c2ac-149">Unified Service Desk configurations</span></span>](../admin/unified-service-desk-configurations-bpa.md)
