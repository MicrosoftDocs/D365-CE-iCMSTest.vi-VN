---
title: Enable document management for entities (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Document management can be enabled for customizable entities in Dynamics 365 for Customer Engagement. To enable document management for an entity, set the EntityMetadata.IsDocumentManagementEnabled attribute value to true
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ecda2ce2-e4b6-4c8d-838c-f3d70ad9e63f
caps.latest.revision: 25
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 79f4e0afb0109f3a989ef626a0e755a00eb171ef
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387208"
---
# <a name="enable-document-management-for-entities"></a><span data-ttu-id="45ce3-104">Enable document management for entities</span><span class="sxs-lookup"><span data-stu-id="45ce3-104">Enable document management for entities</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="45ce3-105">Document management can be enabled for those entities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps that can be customized.</span><span class="sxs-lookup"><span data-stu-id="45ce3-105">Document management can be enabled for those entities in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps that can be customized.</span></span> <span data-ttu-id="45ce3-106">By default, document management is enabled only for the following entities in a new installation of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]:</span><span class="sxs-lookup"><span data-stu-id="45ce3-106">By default, document management is enabled only for the following entities in a new installation of [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)]:</span></span>  
  
- `Account`  
  
- `KbArticle`  
  
- `Lead`  
  
- `Opportunity`  
  
- `Product`  
  
- `Quote`  
  
- `SalesLiterature`  
  
  <span data-ttu-id="45ce3-107">To enable document management for an entity, set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsDocumentManagementEnabled></span><span class="sxs-lookup"><span data-stu-id="45ce3-107">To enable document management for an entity, set the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsDocumentManagementEnabled></span></span> <span data-ttu-id="45ce3-108">attribute value to **true**.</span><span class="sxs-lookup"><span data-stu-id="45ce3-108">attribute value to **true**.</span></span> <span data-ttu-id="45ce3-109">To disable document management for an entity, set the value to **false**.</span><span class="sxs-lookup"><span data-stu-id="45ce3-109">To disable document management for an entity, set the value to **false**.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="45ce3-110">You must have the System Administrator or System Customizer role to enable or disable document management for an entity.</span><span class="sxs-lookup"><span data-stu-id="45ce3-110">You must have the System Administrator or System Customizer role to enable or disable document management for an entity.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="45ce3-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="45ce3-111">See also</span></span>  
 <span data-ttu-id="45ce3-112">[SharePoint Extensions for Dynamics 365 for Customer Engagement apps](integrate-sharepoint.md) </span><span class="sxs-lookup"><span data-stu-id="45ce3-112">[SharePoint Extensions for Dynamics 365 for Customer Engagement apps](integrate-sharepoint.md) </span></span>  
 <span data-ttu-id="45ce3-113">[Actions on SharePoint Location Records](actions-on-sharepoint-location-records.md) </span><span class="sxs-lookup"><span data-stu-id="45ce3-113">[Actions on SharePoint Location Records](actions-on-sharepoint-location-records.md) </span></span>  
 [<span data-ttu-id="45ce3-114">Sample: Enable SharePoint Integration</span><span class="sxs-lookup"><span data-stu-id="45ce3-114">Sample: Enable SharePoint Integration</span></span>](sample-enable-document-management-entities.md)
