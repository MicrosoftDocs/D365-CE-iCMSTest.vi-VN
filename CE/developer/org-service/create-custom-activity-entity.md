---
title: Create a custom activity entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The sample demonstrates how to create a custom activity entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2016
- Dynamics CRM Online
ms.assetid: 56e37fe0-182e-4021-a0b1-b32cba93d49e
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 17c7fc4c09ce0e6dad745ffab246df563a8367e0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386442"
---
# <a name="create-a-custom-activity-entity"></a><span data-ttu-id="df707-103">Create a custom activity entity</span><span class="sxs-lookup"><span data-stu-id="df707-103">Create a custom activity entity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="df707-104">This topic contains a sample that shows how to create a custom activity entity.</span><span class="sxs-lookup"><span data-stu-id="df707-104">This topic contains a sample that shows how to create a custom activity entity.</span></span>  
  
 <span data-ttu-id="df707-105">The following sample creates a custom entity and sets the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsActivity> property to `true`.</span><span class="sxs-lookup"><span data-stu-id="df707-105">The following sample creates a custom entity and sets the <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IsActivity> property to `true`.</span></span> <span data-ttu-id="df707-106">All activities must have a <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.PrimaryAttribute><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.SchemaName> set to `Subject` so that it corresponds to the common `ActivityPointer`.`Subject`</span><span class="sxs-lookup"><span data-stu-id="df707-106">All activities must have a <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest.PrimaryAttribute><xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.SchemaName> set to `Subject` so that it corresponds to the common `ActivityPointer`.`Subject`</span></span> <span data-ttu-id="df707-107">attribute used by all activities.</span><span class="sxs-lookup"><span data-stu-id="df707-107">attribute used by all activities.</span></span>  
  
 [!code-csharp[Entities#CreateCustomActivityEntity1](../../snippets/csharp/CRMV8/entities/cs/createcustomactivityentity1.cs#createcustomactivityentity1)]  
  
### <a name="see-also"></a><span data-ttu-id="df707-108">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="df707-108">See Also</span></span>  

 <xref:Microsoft.Xrm.Sdk.Messages.CreateEntityRequest>  
 <span data-ttu-id="df707-109">[Use the sample and helper code](use-sample-helper-code.md) </span><span class="sxs-lookup"><span data-stu-id="df707-109">[Use the sample and helper code](use-sample-helper-code.md) </span></span>  
 <span data-ttu-id="df707-110">[Custom activities](../custom-activities.md) </span><span class="sxs-lookup"><span data-stu-id="df707-110">[Custom activities](../custom-activities.md) </span></span>  
 <span data-ttu-id="df707-111">[Customize entity metadata](../customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="df707-111">[Customize entity metadata](../customize-entity-metadata.md) </span></span>  
 <span data-ttu-id="df707-112">[Modify Entity Icons](../modify-icons-entity.md) </span><span class="sxs-lookup"><span data-stu-id="df707-112">[Modify Entity Icons](../modify-icons-entity.md) </span></span>  
 <span data-ttu-id="df707-113">[Modify Entity Messages](../modify-messages-entity.md) </span><span class="sxs-lookup"><span data-stu-id="df707-113">[Modify Entity Messages](../modify-messages-entity.md) </span></span>  
 [<span data-ttu-id="df707-114">Sample: Create a custom activity</span><span class="sxs-lookup"><span data-stu-id="df707-114">Sample: Create a custom activity</span></span>](../sample-create-custom-activity.md)
