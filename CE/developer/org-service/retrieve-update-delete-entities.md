---
title: Retrieve, update, and delete entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn how to retrieve, update, and delete an entity by using the custom entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 67571a52-57bf-4872-add5-11f76d3b5adc
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6729bb0b6c9024868f514b313b1560667d9c2919
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386310"
---
# <a name="retrieve-update-and-delete-entities"></a><span data-ttu-id="620c6-103">Retrieve, update, and delete entities</span><span class="sxs-lookup"><span data-stu-id="620c6-103">Retrieve, update, and delete entities</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="620c6-104">This topic shows how to retrieve, update, and delete an entity by using the custom `Bank Account` entity created in [Create a Custom Entity](create-custom-entity.md).</span><span class="sxs-lookup"><span data-stu-id="620c6-104">This topic shows how to retrieve, update, and delete an entity by using the custom `Bank Account` entity created in [Create a Custom Entity](create-custom-entity.md).</span></span>  
  
<a name="BKMK_RetrieveAndUpdateEntity"></a>   
## <a name="retrieve-and-update-an-entity"></a><span data-ttu-id="620c6-105">Retrieve and update an entity</span><span class="sxs-lookup"><span data-stu-id="620c6-105">Retrieve and update an entity</span></span>  
 <span data-ttu-id="620c6-106">The following sample retrieves an entity by using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityRequest> message.</span><span class="sxs-lookup"><span data-stu-id="620c6-106">The following sample retrieves an entity by using the <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityRequest> message.</span></span> <span data-ttu-id="620c6-107">It then updates the entity to disable mail merge by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsMailMergeEnabled> property to `false`, and sets <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasNotes> to `true` in the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> to specify that the entity should include a relationship to the `Annotation` entity so that the entity can display notes.</span><span class="sxs-lookup"><span data-stu-id="620c6-107">It then updates the entity to disable mail merge by setting the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsMailMergeEnabled> property to `false`, and sets <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest.HasNotes> to `true` in the <xref:Microsoft.Xrm.Sdk.Messages.UpdateEntityRequest> to specify that the entity should include a relationship to the `Annotation` entity so that the entity can display notes.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata9](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata9.cs#createupdateentitymetadata9)]  
  
<a name="BKMK_DeleteCustomEntity"></a>   
## <a name="delete-a-custom-entity"></a><span data-ttu-id="620c6-108">Xóa thực thể tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="620c6-108">Delete a custom entity</span></span>  
 <span data-ttu-id="620c6-109">The following sample uses the <xref:Microsoft.Xrm.Sdk.Messages.DeleteEntityRequest> message to delete the entity with the logical name specified by the `_customEntityName` variable.</span><span class="sxs-lookup"><span data-stu-id="620c6-109">The following sample uses the <xref:Microsoft.Xrm.Sdk.Messages.DeleteEntityRequest> message to delete the entity with the logical name specified by the `_customEntityName` variable.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEntityMetadata10](../../snippets/csharp/CRMV8/entities/cs/createupdateentitymetadata10.cs#createupdateentitymetadata10)]  
  
### <a name="see-also"></a><span data-ttu-id="620c6-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="620c6-110">See also</span></span>  
 <span data-ttu-id="620c6-111">[Use the IOrganizationService Sample and Helper Code](use-sample-helper-code.md) </span><span class="sxs-lookup"><span data-stu-id="620c6-111">[Use the IOrganizationService Sample and Helper Code](use-sample-helper-code.md) </span></span>  
 <span data-ttu-id="620c6-112">[Customize entity metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="620c6-112">[Customize entity metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="620c6-113">[Create and update an entity than can be emailed](create-update-entity-emailed.md) </span><span class="sxs-lookup"><span data-stu-id="620c6-113">[Create and update an entity than can be emailed](create-update-entity-emailed.md) </span></span>  
 [<span data-ttu-id="620c6-114">Create a Custom Entity</span><span class="sxs-lookup"><span data-stu-id="620c6-114">Create a Custom Entity</span></span>](create-custom-entity.md)
