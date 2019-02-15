---
title: Modify the icons for an entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about modifying the icons for an entity.
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
- modifying icons for entities, types of
- modifying icons for entities, properties for
- customizing entity metadata, modifying icons for entities
- icons, customizing for entities
- entities, modifying icons for
- custom icons, modifying for entities
- modifying icons for entities, default specifications for icons
ms.assetid: 32fbb402-3808-4d9a-b2e3-6acecb4bb62a
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 435090efda629bfd6d343bdbf0dbff2bd7f9f7b0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387523"
---
# <a name="modify-the-icons-for-an-entity"></a><span data-ttu-id="5d3d7-103">Modify the icons for an entity</span><span class="sxs-lookup"><span data-stu-id="5d3d7-103">Modify the icons for an entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5d3d7-104">When you create a new entity, default icons are provided.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-104">When you create a new entity, default icons are provided.</span></span> <span data-ttu-id="5d3d7-105">You can change the icons of custom entities by creating image Web resources and updating `EntityMetadata` (<xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" /> or <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata> class) properties.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-105">You can change the icons of custom entities by creating image Web resources and updating `EntityMetadata` (<xref href="Microsoft.Dynamics.CRM.EntityMetadata?text=EntityMetadata EntityType" /> or <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata> class) properties.</span></span> <span data-ttu-id="5d3d7-106">Use the specifications in this topic when creating or ordering icons.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-106">Use the specifications in this topic when creating or ordering icons.</span></span> <span data-ttu-id="5d3d7-107">You will need the icon files before you begin.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-107">You will need the icon files before you begin.</span></span>  

> [!NOTE]
>  <span data-ttu-id="5d3d7-108">When you first associate Web Resources with icons in the application the size of the icons will be checked.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-108">When you first associate Web Resources with icons in the application the size of the icons will be checked.</span></span> <span data-ttu-id="5d3d7-109">If you associate Web Resources programmatically, no size validation occurs.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-109">If you associate Web Resources programmatically, no size validation occurs.</span></span> <span data-ttu-id="5d3d7-110">If the Web Resource is later updated with a large size image, no validation occurs.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-110">If the Web Resource is later updated with a large size image, no validation occurs.</span></span>  

 <span data-ttu-id="5d3d7-111">For more information about how to manually update icons, see [Change entity icons](http://go.microsoft.com/fwlink/p/?LinkId=316860).</span><span class="sxs-lookup"><span data-stu-id="5d3d7-111">For more information about how to manually update icons, see [Change entity icons](http://go.microsoft.com/fwlink/p/?LinkId=316860).</span></span>  

## <a name="types-of-icons"></a><span data-ttu-id="5d3d7-112">Types of icons</span><span class="sxs-lookup"><span data-stu-id="5d3d7-112">Types of icons</span></span>  
 <span data-ttu-id="5d3d7-113">The following table liststhe types of entity icons you can update.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-113">The following table liststhe types of entity icons you can update.</span></span>  


|                                                             <span data-ttu-id="5d3d7-114">Loại</span><span class="sxs-lookup"><span data-stu-id="5d3d7-114">Type</span></span>                                                             |           <span data-ttu-id="5d3d7-115">Specifications</span><span class="sxs-lookup"><span data-stu-id="5d3d7-115">Specifications</span></span>           |                            <span data-ttu-id="5d3d7-116">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="5d3d7-116">Property</span></span>                             |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------|-----------------------------------------------------------------|
|            <span data-ttu-id="5d3d7-117">**Biểu tượng trong Ứng dụng web**</span><span class="sxs-lookup"><span data-stu-id="5d3d7-117">**Icon in Web application**</span></span><br /><br /> <span data-ttu-id="5d3d7-118">Displays when records for this entity are displayed in a grid.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-118">Displays when records for this entity are displayed in a grid.</span></span>            | <span data-ttu-id="5d3d7-119">-   16x16px</span><span class="sxs-lookup"><span data-stu-id="5d3d7-119">-   16x16px</span></span><br /><span data-ttu-id="5d3d7-120">-   Less than 10k</span><span class="sxs-lookup"><span data-stu-id="5d3d7-120">-   Less than 10k</span></span> | <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IconSmallName>  |
|                                                  <span data-ttu-id="5d3d7-121">**Icon for Entity Forms**</span><span class="sxs-lookup"><span data-stu-id="5d3d7-121">**Icon for Entity Forms**</span></span>                                                   | <span data-ttu-id="5d3d7-122">-   32x32px</span><span class="sxs-lookup"><span data-stu-id="5d3d7-122">-   32x32px</span></span><br /><span data-ttu-id="5d3d7-123">-   Less than 10k</span><span class="sxs-lookup"><span data-stu-id="5d3d7-123">-   Less than 10k</span></span> | <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IconMediumName> |
| <span data-ttu-id="5d3d7-124">This size icon is not used in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-124">This size icon is not used in [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> | <span data-ttu-id="5d3d7-125">-   66x48px</span><span class="sxs-lookup"><span data-stu-id="5d3d7-125">-   66x48px</span></span><br /><span data-ttu-id="5d3d7-126">-   Less than 10k</span><span class="sxs-lookup"><span data-stu-id="5d3d7-126">-   Less than 10k</span></span> | <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.IconLargeName>  |

 <span data-ttu-id="5d3d7-127">PNG Web resources are recommended because they support transparency and good compression with a better color fidelity than GIF.</span><span class="sxs-lookup"><span data-stu-id="5d3d7-127">PNG Web resources are recommended because they support transparency and good compression with a better color fidelity than GIF.</span></span> <span data-ttu-id="5d3d7-128">GIF, JPG, and ICO formats are supported for backwards compatibility when organizations are upgraded from [!INCLUDE[pn_Microsoft_Dynamics_CRM_4.0](../includes/pn-microsoft-dynamics-crm-4-0.md)].</span><span class="sxs-lookup"><span data-stu-id="5d3d7-128">GIF, JPG, and ICO formats are supported for backwards compatibility when organizations are upgraded from [!INCLUDE[pn_Microsoft_Dynamics_CRM_4.0](../includes/pn-microsoft-dynamics-crm-4-0.md)].</span></span>  

### <a name="see-also"></a><span data-ttu-id="5d3d7-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5d3d7-129">See also</span></span>  
 <span data-ttu-id="5d3d7-130">[Customize Entity Metadata](customize-entity-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="5d3d7-130">[Customize Entity Metadata](customize-entity-metadata.md) </span></span>  
 [<span data-ttu-id="5d3d7-131">Modify Entity Messages</span><span class="sxs-lookup"><span data-stu-id="5d3d7-131">Modify Entity Messages</span></span>](modify-messages-entity.md)
