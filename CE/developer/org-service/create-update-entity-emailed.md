---
title: Create and update an entity to send email activities to records | MicrosoftDocs
description: Learn about creating an entity that contains an email address you can use to send email activities to records for that entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bc1ae819-61c1-4a44-8f38-a6240975b111
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5ec0bfdc96d47177c2b51d90f708d4c556e70004
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386043"
---
# <a name="create-and-update-an-entity-to-send-email-activities-to-records"></a><span data-ttu-id="0ec49-103">Create and update an entity to send email activities to records</span><span class="sxs-lookup"><span data-stu-id="0ec49-103">Create and update an entity to send email activities to records</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0ec49-104">You can create an entity that contains an email address you can use to send email activities to records for that entity.</span><span class="sxs-lookup"><span data-stu-id="0ec49-104">You can create an entity that contains an email address you can use to send email activities to records for that entity.</span></span>  
  
 <span data-ttu-id="0ec49-105">The following sample creates a custom entity and sets the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsActivityParty> property to `true`.</span><span class="sxs-lookup"><span data-stu-id="0ec49-105">The following sample creates a custom entity and sets the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsActivityParty> property to `true`.</span></span> <span data-ttu-id="0ec49-106">It also creates a <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attribute using <xref:Microsoft.Xrm.Sdk.Metadata.StringFormatName>.`Email`</span><span class="sxs-lookup"><span data-stu-id="0ec49-106">It also creates a <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attribute using <xref:Microsoft.Xrm.Sdk.Metadata.StringFormatName>.`Email`</span></span> <span data-ttu-id="0ec49-107">to provide an email address to use.</span><span class="sxs-lookup"><span data-stu-id="0ec49-107">to provide an email address to use.</span></span>  
  
 <span data-ttu-id="0ec49-108">Even if you add other <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attributes formatted as an email address, only the first one specified is used.</span><span class="sxs-lookup"><span data-stu-id="0ec49-108">Even if you add other <xref:Microsoft.Xrm.Sdk.Metadata.StringAttributeMetadata> attributes formatted as an email address, only the first one specified is used.</span></span>  
  
 [!code-csharp[Entities#CreateUpdateEmailableEntity1](../../snippets/csharp/CRMV8/entities/cs/createupdateemailableentity1.cs#createupdateemailableentity1)]  
  
### <a name="see-also"></a><span data-ttu-id="0ec49-109">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0ec49-109">See Also</span></span>

 <span data-ttu-id="0ec49-110">[Use the IOrganizationService Sample and Helper Code](use-sample-helper-code.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-110">[Use the IOrganizationService Sample and Helper Code](use-sample-helper-code.md) </span></span>  
 <span data-ttu-id="0ec49-111">[Customize entity metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-111">[Customize entity metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="0ec49-112">[Which Entities are Customizable?](../which-entities-are-customizable.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-112">[Which Entities are Customizable?](../which-entities-are-customizable.md) </span></span>  
 <span data-ttu-id="0ec49-113">[Tạo thực thể tùy chỉnh](create-custom-entity.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-113">[Create a custom entity](create-custom-entity.md) </span></span>  
 <span data-ttu-id="0ec49-114">[Retrieve, update, and delete entities](retrieve-update-delete-entities.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-114">[Retrieve, update, and delete entities](retrieve-update-delete-entities.md) </span></span>  
 <span data-ttu-id="0ec49-115">[Create a custom activity entity](create-custom-activity-entity.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-115">[Create a custom activity entity](create-custom-activity-entity.md) </span></span>  
 <span data-ttu-id="0ec49-116">[Change Entity Icons](../modify-icons-entity.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-116">[Change Entity Icons](../modify-icons-entity.md) </span></span>  
 <span data-ttu-id="0ec49-117">[Change Entity Messages](../modify-messages-entity.md) </span><span class="sxs-lookup"><span data-stu-id="0ec49-117">[Change Entity Messages](../modify-messages-entity.md) </span></span>  
 [<span data-ttu-id="0ec49-118">Sample: Create and update an emailable entity</span><span class="sxs-lookup"><span data-stu-id="0ec49-118">Sample: Create and update an emailable entity</span></span>](sample-create-update-emailable-entity.md)
