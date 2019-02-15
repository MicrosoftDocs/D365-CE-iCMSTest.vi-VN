---
title: Customize visualizations and dashboards (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'Learn about configuring dashboards in such a way that enables you to view data from multiple areas of Dynamics 365 for Customer Engagement such as sales, marketing, and service. You can even adjust the data displayed in visualizations and dashboards per your business requirements by applying filters. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- visualizations
- charts
- dashboards
ms.assetid: 275d803b-68ea-41d0-9a31-e0adbb9c1815
caps.latest.revision: 37
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5d0d075d602b135e75539025d0ad4dbf7a1d5f97
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387370"
---
# <a name="customize-visualizations-and-dashboards"></a><span data-ttu-id="531b3-104">Customize visualizations and dashboards</span><span class="sxs-lookup"><span data-stu-id="531b3-104">Customize visualizations and dashboards</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="531b3-105">Data visualization and analytics in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement enable you to graphically view and analyze the data for your business, and help you to derive quick insights to make important business decisions.</span><span class="sxs-lookup"><span data-stu-id="531b3-105">Data visualization and analytics in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement enable you to graphically view and analyze the data for your business, and help you to derive quick insights to make important business decisions.</span></span> <span data-ttu-id="531b3-106">You can configure dashboards in such a way that enables you to view data from multiple areas of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] such as sales, marketing, and service.</span><span class="sxs-lookup"><span data-stu-id="531b3-106">You can configure dashboards in such a way that enables you to view data from multiple areas of [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] such as sales, marketing, and service.</span></span> <span data-ttu-id="531b3-107">You can even adjust the data displayed in visualizations and dashboards per your business requirements by applying filters.</span><span class="sxs-lookup"><span data-stu-id="531b3-107">You can even adjust the data displayed in visualizations and dashboards per your business requirements by applying filters.</span></span>  
  
 <span data-ttu-id="531b3-108">The following elements constitute the visualization and analytics abilities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)]:</span><span class="sxs-lookup"><span data-stu-id="531b3-108">The following elements constitute the visualization and analytics abilities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)]:</span></span>  
  
- <span data-ttu-id="531b3-109">**Visualization**.</span><span class="sxs-lookup"><span data-stu-id="531b3-109">**Visualization**.</span></span> <span data-ttu-id="531b3-110">Visualizations enable you to present your data in the form of charts.</span><span class="sxs-lookup"><span data-stu-id="531b3-110">Visualizations enable you to present your data in the form of charts.</span></span> <span data-ttu-id="531b3-111">Charts enable you to view the aggregate or non-aggregate summary of grid data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="531b3-111">Charts enable you to view the aggregate or non-aggregate summary of grid data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)].</span></span> <span data-ttu-id="531b3-112">The charts are integrated with the grid, and display data in context with the grids.</span><span class="sxs-lookup"><span data-stu-id="531b3-112">The charts are integrated with the grid, and display data in context with the grids.</span></span> <span data-ttu-id="531b3-113">The charts update automatically to reflect the filtering done on the data in the grids.</span><span class="sxs-lookup"><span data-stu-id="531b3-113">The charts update automatically to reflect the filtering done on the data in the grids.</span></span> <span data-ttu-id="531b3-114">Similarly, when you perform a drill-down operation on the chart, the data in the corresponding grid updates accordingly.</span><span class="sxs-lookup"><span data-stu-id="531b3-114">Similarly, when you perform a drill-down operation on the chart, the data in the corresponding grid updates accordingly.</span></span> <span data-ttu-id="531b3-115">You can also use a web resource instead of charts in visualization.</span><span class="sxs-lookup"><span data-stu-id="531b3-115">You can also use a web resource instead of charts in visualization.</span></span>  
  
- <span data-ttu-id="531b3-116">**Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="531b3-116">**Dashboard**.</span></span> <span data-ttu-id="531b3-117">Dashboards act as a business intelligence tool in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] by providing a snapshot of your data in various forms.</span><span class="sxs-lookup"><span data-stu-id="531b3-117">Dashboards act as a business intelligence tool in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] by providing a snapshot of your data in various forms.</span></span> <span data-ttu-id="531b3-118">You can use a dashboard to simultaneously present data from up to six charts, grids, IFrames, or web resources.</span><span class="sxs-lookup"><span data-stu-id="531b3-118">You can use a dashboard to simultaneously present data from up to six charts, grids, IFrames, or web resources.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="531b3-119">In This Section</span><span class="sxs-lookup"><span data-stu-id="531b3-119">In This Section</span></span>  
 [<span data-ttu-id="531b3-120">View Data with Visualizations (Charts)</span><span class="sxs-lookup"><span data-stu-id="531b3-120">View Data with Visualizations (Charts)</span></span>](view-data-with-visualizations-charts.md)  
  
 [<span data-ttu-id="531b3-121">Analyze Data with Dashboards</span><span class="sxs-lookup"><span data-stu-id="531b3-121">Analyze Data with Dashboards</span></span>](analyze-data-with-dashboards.md)  
  
 [<span data-ttu-id="531b3-122">Visualization Data Description Schema</span><span class="sxs-lookup"><span data-stu-id="531b3-122">Visualization Data Description Schema</span></span>](visualization-data-description-schema.md)  
  
## <a name="related-sections"></a><span data-ttu-id="531b3-123">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="531b3-123">Related Sections</span></span>  
 [<span data-ttu-id="531b3-124">Extend the metadata model</span><span class="sxs-lookup"><span data-stu-id="531b3-124">Extend the metadata model</span></span>](../org-service/use-organization-service-metadata.md)  
  
 [<span data-ttu-id="531b3-125">Customize entity forms</span><span class="sxs-lookup"><span data-stu-id="531b3-125">Customize entity forms</span></span>](customize-entity-forms.md)  
  
 [<span data-ttu-id="531b3-126">Customize Entity Views in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="531b3-126">Customize Entity Views in Dynamics 365 for Customer Engagement</span></span>](customize-entity-views.md)  
  
 [<span data-ttu-id="531b3-127">Customize global option sets</span><span class="sxs-lookup"><span data-stu-id="531b3-127">Customize global option sets</span></span>](../org-service/customize-global-option-sets.md)  
  
 [<span data-ttu-id="531b3-128">Change application navigation using the SiteMap</span><span class="sxs-lookup"><span data-stu-id="531b3-128">Change application navigation using the SiteMap</span></span>](/developer/customize-dev/change-application-navigation-using-sitemap.md)  
  
 [<span data-ttu-id="531b3-129">Tùy chỉnh lệnh và ru băng</span><span class="sxs-lookup"><span data-stu-id="531b3-129">Customize commands and the ribbon</span></span>](customize-commands-ribbon.md)  
  
 [<span data-ttu-id="531b3-130">Service calendar appearance configuration</span><span class="sxs-lookup"><span data-stu-id="531b3-130">Service calendar appearance configuration</span></span>](service-calendar-appearance-configuration.md)  
  
 [<span data-ttu-id="531b3-131">Phát hành tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="531b3-131">Publish customizations</span></span>](publish-customizations.md)  
  
 [<span data-ttu-id="531b3-132">When to edit the customizations file</span><span class="sxs-lookup"><span data-stu-id="531b3-132">When to edit the customizations file</span></span>](when-edit-customization-file.md)  
  
 [<span data-ttu-id="531b3-133">Customize Entity Views in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="531b3-133">Customize Entity Views in Dynamics 365 for Customer Engagement</span></span>](customize-entity-views.md)  
  
 [<span data-ttu-id="531b3-134">Change Application Navigation using the SiteMap</span><span class="sxs-lookup"><span data-stu-id="531b3-134">Change Application Navigation using the SiteMap</span></span>](/developer/customize-dev/change-application-navigation-using-sitemap.md)  
  
 [<span data-ttu-id="531b3-135">Extend Microsoft Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="531b3-135">Extend Microsoft Dynamics 365 for Customer Engagement</span></span>](../extend-client.md)  
  
 [<span data-ttu-id="531b3-136">Web Resources for Microsoft Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="531b3-136">Web Resources for Microsoft Dynamics 365 for Customer Engagement</span></span>](../web-resources.md)
