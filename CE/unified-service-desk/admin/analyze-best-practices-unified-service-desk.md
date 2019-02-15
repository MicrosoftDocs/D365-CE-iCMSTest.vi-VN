---
title: Analyze best practices in Unified Service Desk (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about the best practices analyzer, which performs analysis on the Internet Explorer settings, Unified Service Desk configurations in Dynamics 365 for Customer Engagement apps, and system configurations on which you install Unified Service Desk, and displays a report to review and mitigate the issues.
ms.custom: ''
ms.date: 04/24/2018
ms.service: usd
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 8ED5D0F6-4A3E-49FA-A399-0AEDFF2236AA
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 975589c8cbc9b8e41d646a5db72432e7424e3bf8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382479"
---
# <a name="analyze-best-practices-in-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a><span data-ttu-id="c37db-103">Analyze best practices in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="c37db-103">Analyze best practices in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span></span>

<span data-ttu-id="c37db-104">Best practices are the guidelines about System Configurations, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], Internet Explorer settings, and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="c37db-104">Best practices are the guidelines about System Configurations, [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], Internet Explorer settings, and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] configurations in Dynamics 365 for Customer Engagement apps.</span></span> <span data-ttu-id="c37db-105">Consider these guidelines as our recommended way to use [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and serve your customers.</span><span class="sxs-lookup"><span data-stu-id="c37db-105">Consider these guidelines as our recommended way to use [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and serve your customers.</span></span>

<span data-ttu-id="c37db-106">Although deviating from best practices may not necessarily lead to a breakdown, they indicate crucial parameters that can result in poor performance, poor reliability, unexpected conflicts, increased security risks, or other potential problems.</span><span class="sxs-lookup"><span data-stu-id="c37db-106">Although deviating from best practices may not necessarily lead to a breakdown, they indicate crucial parameters that can result in poor performance, poor reliability, unexpected conflicts, increased security risks, or other potential problems.</span></span> 

## <a name="what-is-includepn-best-practices-analyzerincludespn-best-practices-analyzermd-for-includepnunifiedservicedeskincludespn-unified-service-deskmd"></a><span data-ttu-id="c37db-107">What is [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="c37db-107">What is [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]</span></span>

[!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] <span data-ttu-id="c37db-108">analyzes the compliance of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] with best practice rules in certain categories.</span><span class="sxs-lookup"><span data-stu-id="c37db-108">analyzes the compliance of [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] with best practice rules in certain categories.</span></span> <span data-ttu-id="c37db-109">The [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays the results of analysis in the form of a report with severity levels, description of the parameter, and mitigation for the non-compliant / problematic areas.</span><span class="sxs-lookup"><span data-stu-id="c37db-109">The [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] displays the results of analysis in the form of a report with severity levels, description of the parameter, and mitigation for the non-compliant / problematic areas.</span></span>

<span data-ttu-id="c37db-110">The following table lists the categories against which [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] analyzes the compliance of best practice rules.</span><span class="sxs-lookup"><span data-stu-id="c37db-110">The following table lists the categories against which [!INCLUDE[pn-best-practices-analyzer](../../includes/pn-best-practices-analyzer.md)] analyzes the compliance of best practice rules.</span></span>


|                                         <span data-ttu-id="c37db-111">Category name</span><span class="sxs-lookup"><span data-stu-id="c37db-111">Category name</span></span>                                         |                                                                                                                                        <span data-ttu-id="c37db-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c37db-112">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="c37db-113">Configurations</span><span class="sxs-lookup"><span data-stu-id="c37db-113">Configurations</span></span> | [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="c37db-114">Configurations are the configurations (hosted controls, actions, events, and so on) that you configure for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="c37db-114">Configurations are the configurations (hosted controls, actions, events, and so on) that you configure for [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] in Dynamics 365 for Customer Engagement apps.</span></span> |
|                                     <span data-ttu-id="c37db-115">System configurations</span><span class="sxs-lookup"><span data-stu-id="c37db-115">System configurations</span></span>                                     |                                          <span data-ttu-id="c37db-116">System configurations are the information about local computer hardware (RAM, operating system, and so on), and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] version.</span><span class="sxs-lookup"><span data-stu-id="c37db-116">System configurations are the information about local computer hardware (RAM, operating system, and so on), and [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] version.</span></span>                                          |
|                                  <span data-ttu-id="c37db-117">Internet Explorer settings</span><span class="sxs-lookup"><span data-stu-id="c37db-117">Internet Explorer settings</span></span>                                   |                                                                              <span data-ttu-id="c37db-118">Internet Explorer settings are the settings (General, Security, Advanced, and so on) that you configure for Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c37db-118">Internet Explorer settings are the settings (General, Security, Advanced, and so on) that you configure for Internet Explorer.</span></span>                                                                               |

<span data-ttu-id="c37db-119">The following table lists the results of Severity level analysis.</span><span class="sxs-lookup"><span data-stu-id="c37db-119">The following table lists the results of Severity level analysis.</span></span>


| <span data-ttu-id="c37db-120">Severity category</span><span class="sxs-lookup"><span data-stu-id="c37db-120">Severity category</span></span> |                                                                                                                                                                                      <span data-ttu-id="c37db-121">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c37db-121">Description</span></span>                                                                                                                                                                                       |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       <span data-ttu-id="c37db-122">Pass</span><span class="sxs-lookup"><span data-stu-id="c37db-122">Pass</span></span>        |                                                                                                                                                 <span data-ttu-id="c37db-123">The report displays a pass result when a parameter satisfies the recommended criteria.</span><span class="sxs-lookup"><span data-stu-id="c37db-123">The report displays a pass result when a parameter satisfies the recommended criteria.</span></span>                                                                                                                                                 |
|      <span data-ttu-id="c37db-124">Cảnh báo</span><span class="sxs-lookup"><span data-stu-id="c37db-124">Warning</span></span>      | <span data-ttu-id="c37db-125">The report displays a warning result when a parameter doesn't satisfy the recommended criteria and due to which [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can encounter potential issues.</span><span class="sxs-lookup"><span data-stu-id="c37db-125">The report displays a warning result when a parameter doesn't satisfy the recommended criteria and due to which [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] can encounter potential issues.</span></span> <span data-ttu-id="c37db-126">Using recommended value settings for parameters helps [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to perform better.</span><span class="sxs-lookup"><span data-stu-id="c37db-126">Using recommended value settings for parameters helps [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to perform better.</span></span> |
|       <span data-ttu-id="c37db-127">Lỗi</span><span class="sxs-lookup"><span data-stu-id="c37db-127">Error</span></span>       |                                                                                                                                             <span data-ttu-id="c37db-128">The report displays an error result when a parameter doesn't satisfy the recommended criteria.</span><span class="sxs-lookup"><span data-stu-id="c37db-128">The report displays an error result when a parameter doesn't satisfy the recommended criteria.</span></span>                                                                                                                                             |

## <a name="see-also"></a><span data-ttu-id="c37db-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c37db-129">See also</span></span>

[<span data-ttu-id="c37db-130">Download and install Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="c37db-130">Download and install Best Practices Analyzer</span></span>](../admin/download-install-best-practices-analyzer.md)

[<span data-ttu-id="c37db-131">Walkthrough: Configure Best Practices Analyzer</span><span class="sxs-lookup"><span data-stu-id="c37db-131">Walkthrough: Configure Best Practices Analyzer</span></span>](../admin/walkthrough-configure-best-practices-analyzer.md)

[<span data-ttu-id="c37db-132">Read Best Practices Analyzer report</span><span class="sxs-lookup"><span data-stu-id="c37db-132">Read Best Practices Analyzer report</span></span>](../admin/read-best-practices-analyzer-report.md)

[<span data-ttu-id="c37db-133">Best practice rule categories and parameters</span><span class="sxs-lookup"><span data-stu-id="c37db-133">Best practice rule categories and parameters</span></span>](../admin/compliance-categories-parameters-bpa.md)

[<span data-ttu-id="c37db-134">System configurations</span><span class="sxs-lookup"><span data-stu-id="c37db-134">System configurations</span></span>](../admin/system-configurations-bpa.md)

[<span data-ttu-id="c37db-135">Internet Explorer settings</span><span class="sxs-lookup"><span data-stu-id="c37db-135">Internet Explorer settings</span></span>](../admin/internet-explorer-settings-bpa.md)

[<span data-ttu-id="c37db-136">Unified Service Desk configurations</span><span class="sxs-lookup"><span data-stu-id="c37db-136">Unified Service Desk configurations</span></span>](../admin/unified-service-desk-configurations-bpa.md)