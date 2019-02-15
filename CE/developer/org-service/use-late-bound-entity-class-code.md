---
title: Use the late bound entity class in code (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Entity class lets you use late binding so that you can work with types such as custom entities and custom attributes that weren’t available when your application was compiled
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 75c9f21a-9bb7-4324-8a50-c655fc4b589d
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a8449bd55d08746f8bf76a2369ee239f5ace5adb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387450"
---
# <a name="use-the-late-bound-entity-class-in-code"></a><span data-ttu-id="af6a3-103">Use the late bound entity class in code</span><span class="sxs-lookup"><span data-stu-id="af6a3-103">Use the late bound entity class in code</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="af6a3-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can use the <xref:Microsoft.Xrm.Sdk.Entity> class when you work with entities.</span><span class="sxs-lookup"><span data-stu-id="af6a3-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you can use the <xref:Microsoft.Xrm.Sdk.Entity> class when you work with entities.</span></span> <span data-ttu-id="af6a3-105">When initialized, the <xref:Microsoft.Xrm.Sdk.Entity> class contains the logical name of an entity and a property-bag array of the entity’s attributes.</span><span class="sxs-lookup"><span data-stu-id="af6a3-105">When initialized, the <xref:Microsoft.Xrm.Sdk.Entity> class contains the logical name of an entity and a property-bag array of the entity’s attributes.</span></span> <span data-ttu-id="af6a3-106">This lets you use late binding so that you can work with types such as custom entities and custom attributes that weren’t available when your application was compiled.</span><span class="sxs-lookup"><span data-stu-id="af6a3-106">This lets you use late binding so that you can work with types such as custom entities and custom attributes that weren’t available when your application was compiled.</span></span>  
  
 <span data-ttu-id="af6a3-107">The key difference between early and late binding involves type conversion.</span><span class="sxs-lookup"><span data-stu-id="af6a3-107">The key difference between early and late binding involves type conversion.</span></span> <span data-ttu-id="af6a3-108">While early binding provides compile-time checking of all types so that no implicit casts occur, late binding checks types only when the object is created or an action is performed on the type.</span><span class="sxs-lookup"><span data-stu-id="af6a3-108">While early binding provides compile-time checking of all types so that no implicit casts occur, late binding checks types only when the object is created or an action is performed on the type.</span></span> <span data-ttu-id="af6a3-109">The <xref:Microsoft.Xrm.Sdk.Entity> class requires types to be explicitly specified to prevent implicit casts.</span><span class="sxs-lookup"><span data-stu-id="af6a3-109">The <xref:Microsoft.Xrm.Sdk.Entity> class requires types to be explicitly specified to prevent implicit casts.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="af6a3-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="af6a3-110">See also</span></span>  
 <span data-ttu-id="af6a3-111">[Extend Dynamics 365 for Customer Engagement apps on the server](../extend-dynamics-365-server.md) </span><span class="sxs-lookup"><span data-stu-id="af6a3-111">[Extend Dynamics 365 for Customer Engagement apps on the server](../extend-dynamics-365-server.md) </span></span>  
 <span data-ttu-id="af6a3-112">[Retrieve Data with Queries](retrieve-data-queries-sdk-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="af6a3-112">[Retrieve Data with Queries](retrieve-data-queries-sdk-assemblies.md) </span></span>  
 <span data-ttu-id="af6a3-113">[Use the Entity Class for Create, Update and Delete](use-entity-class-create-update-delete.md) </span><span class="sxs-lookup"><span data-stu-id="af6a3-113">[Use the Entity Class for Create, Update and Delete](use-entity-class-create-update-delete.md) </span></span>  
 <span data-ttu-id="af6a3-114">[Use the Entity Class to Add or Update Associations Between Related Records](use-entity-class-add-update-associations-records.md) </span><span class="sxs-lookup"><span data-stu-id="af6a3-114">[Use the Entity Class to Add or Update Associations Between Related Records](use-entity-class-add-update-associations-records.md) </span></span>  
 <span data-ttu-id="af6a3-115">[Sample: Create, Retrieve, Update and Delete (Late Bound)](sample-create-retrieve-update-delete-late-bound.md) </span><span class="sxs-lookup"><span data-stu-id="af6a3-115">[Sample: Create, Retrieve, Update and Delete (Late Bound)](sample-create-retrieve-update-delete-late-bound.md) </span></span>  
 [<span data-ttu-id="af6a3-116">Sample: Serialize and Deserialize an Entity</span><span class="sxs-lookup"><span data-stu-id="af6a3-116">Sample: Serialize and Deserialize an Entity</span></span>](sample-serialize-deserialize-entity-instance.md)
