---
title: Analyze data with dashboards (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The dashboard entities in Dynamics 365 for Customer Engagement enable you to present data from various charts, grids, IFRAMES, or web resources simultaneously. Dashboards allow you to compare and analyze various pieces of customer information, and give you data snapshots.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 16f0dd2f-7dad-43be-86fd-f93c7905c8dd
caps.latest.revision: 29
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bc82417e11b0628199d9f8bbbed46b1adfb8ada3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386907"
---
# <a name="analyze-data-with-dashboards"></a><span data-ttu-id="40236-104">Analyze data with dashboards</span><span class="sxs-lookup"><span data-stu-id="40236-104">Analyze data with dashboards</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="40236-105">The dashboard entities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement enable you to present data from various charts, grids, IFRAMES, or web resources simultaneously.</span><span class="sxs-lookup"><span data-stu-id="40236-105">The dashboard entities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement enable you to present data from various charts, grids, IFRAMES, or web resources simultaneously.</span></span> <span data-ttu-id="40236-106">Dashboards allow you to compare and analyze various pieces of customer information, and give you data snapshots.</span><span class="sxs-lookup"><span data-stu-id="40236-106">Dashboards allow you to compare and analyze various pieces of customer information, and give you data snapshots.</span></span>  
  
## <a name="types-of-dashboards"></a><span data-ttu-id="40236-107">Types of dashboards</span><span class="sxs-lookup"><span data-stu-id="40236-107">Types of dashboards</span></span>  
<span data-ttu-id="40236-108">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], there are two types of dashboards: organization-owned dashboards and user-owned dashboards.</span><span class="sxs-lookup"><span data-stu-id="40236-108">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], there are two types of dashboards: organization-owned dashboards and user-owned dashboards.</span></span>  
  
<span data-ttu-id="40236-109">**Organization-owned dashboard.**</span><span class="sxs-lookup"><span data-stu-id="40236-109">**Organization-owned dashboard.**</span></span>

<span data-ttu-id="40236-110">An organization-owned dashboard is represented by the `SystemForm` entity, and can’t be assigned or shared.</span><span class="sxs-lookup"><span data-stu-id="40236-110">An organization-owned dashboard is represented by the `SystemForm` entity, and can’t be assigned or shared.</span></span> <span data-ttu-id="40236-111">These dashboards are solution-aware entities in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="40236-111">These dashboards are solution-aware entities in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="40236-112">When you perform an update operation on this entity, you must publish the changes for the updates to be available across the organization.</span><span class="sxs-lookup"><span data-stu-id="40236-112">When you perform an update operation on this entity, you must publish the changes for the updates to be available across the organization.</span></span> <span data-ttu-id="40236-113">When you publish customizations using the <xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest> message, the newly-created organization-owned dashboards are also published and become available across the organization.</span><span class="sxs-lookup"><span data-stu-id="40236-113">When you publish customizations using the <xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest> message, the newly-created organization-owned dashboards are also published and become available across the organization.</span></span> <span data-ttu-id="40236-114">Alternatively, you can publish the changes done to a specific dashboard by using the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest> message, and specifying the dashboard ID as the parameter in the request message.</span><span class="sxs-lookup"><span data-stu-id="40236-114">Alternatively, you can publish the changes done to a specific dashboard by using the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest> message, and specifying the dashboard ID as the parameter in the request message.</span></span>  
  
<span data-ttu-id="40236-115">**User-owned dashboard.**</span><span class="sxs-lookup"><span data-stu-id="40236-115">**User-owned dashboard.**</span></span>

<span data-ttu-id="40236-116">A user-owned dashboard is represented by the `UserForm` entity, can be assigned and shared with other users, and can be viewed by other users depending on the dashboard’s access privileges.</span><span class="sxs-lookup"><span data-stu-id="40236-116">A user-owned dashboard is represented by the `UserForm` entity, can be assigned and shared with other users, and can be viewed by other users depending on the dashboard’s access privileges.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="40236-117">You can’t programmatically create or manage the new interactive dashboards introduced in [!INCLUDE[pn-crm-2016-shortest](../../includes/pn-crm-2016-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="40236-117">You can’t programmatically create or manage the new interactive dashboards introduced in [!INCLUDE[pn-crm-2016-shortest](../../includes/pn-crm-2016-shortest.md)].</span></span> <span data-ttu-id="40236-118">For information about working with interactive dashboards using the web client, see [Configure interactive experience dashboards](../../customize/configure-interactive-experience-dashboards.md)</span><span class="sxs-lookup"><span data-stu-id="40236-118">For information about working with interactive dashboards using the web client, see [Configure interactive experience dashboards](../../customize/configure-interactive-experience-dashboards.md)</span></span>
  
### <a name="see-also"></a><span data-ttu-id="40236-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="40236-119">See also</span></span>  
 <span data-ttu-id="40236-120">[Using FormXML for Dashboards](understand-dashboards-dashboard-components-formxml.md) </span><span class="sxs-lookup"><span data-stu-id="40236-120">[Using FormXML for Dashboards](understand-dashboards-dashboard-components-formxml.md) </span></span>  
 <span data-ttu-id="40236-121">[Actions on Dashboards](actions-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="40236-121">[Actions on Dashboards](actions-dashboards.md) </span></span>  
 <span data-ttu-id="40236-122">[Create a Dashboard](create-dashboard.md) </span><span class="sxs-lookup"><span data-stu-id="40236-122">[Create a Dashboard](create-dashboard.md) </span></span>  
 <span data-ttu-id="40236-123">[Sample Dashboards](sample-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="40236-123">[Sample Dashboards](sample-dashboards.md) </span></span>  
 <span data-ttu-id="40236-124">[Dashboard Entities](dashboard-entities.md) </span><span class="sxs-lookup"><span data-stu-id="40236-124">[Dashboard Entities](dashboard-entities.md) </span></span>  
 <span data-ttu-id="40236-125">[Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md) </span><span class="sxs-lookup"><span data-stu-id="40236-125">[Sample: Create, Retrieve, Update and Delete (CRUD) a Dashboard](sample-create-retrieve-update-delete-dashboard.md) </span></span>  
 <span data-ttu-id="40236-126">[Sample: Assign a User-Owned Dashboard to Another User](sample-assign-user-owned-dashboard-another-user.md) </span><span class="sxs-lookup"><span data-stu-id="40236-126">[Sample: Assign a User-Owned Dashboard to Another User](sample-assign-user-owned-dashboard-another-user.md) </span></span>  
 <span data-ttu-id="40236-127">[Visualization data description schema](visualization-data-description-schema.md)   </span><span class="sxs-lookup"><span data-stu-id="40236-127">[Visualization data description schema](visualization-data-description-schema.md)   </span></span>  
 [<span data-ttu-id="40236-128">Customize visualizations and dashboards</span><span class="sxs-lookup"><span data-stu-id="40236-128">Customize visualizations and dashboards</span></span>](customize-visualizations-dashboards.md)
