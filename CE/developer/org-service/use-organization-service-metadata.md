---
title: Use the Organization service with metadata (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about how to programmactically access and modify the metadata model using the organization service with metadata.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b7d37dd8-4a1d-4a7f-ac77-436f00c003f1
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3599379545e9c6327d582be263b4551993f22ed3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386062"
---
# <a name="use-the-organization-service-with-dynamics-365-for-customer-engagement-metadata"></a><span data-ttu-id="99fe3-103">Use the Organization service with Dynamics 365 for Customer Engagement metadata</span><span class="sxs-lookup"><span data-stu-id="99fe3-103">Use the Organization service with Dynamics 365 for Customer Engagement metadata</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="99fe3-104">Metadata refers to the structure of entities used to manage data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="99fe3-104">Metadata refers to the structure of entities used to manage data in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.</span></span> <span data-ttu-id="99fe3-105">Virtually all tasks to manage metadata can be performed by using the customization tools in the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps application.</span><span class="sxs-lookup"><span data-stu-id="99fe3-105">Virtually all tasks to manage metadata can be performed by using the customization tools in the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] apps application.</span></span> <span data-ttu-id="99fe3-106">This section describes how to programmatically access and modify the metadata model.</span><span class="sxs-lookup"><span data-stu-id="99fe3-106">This section describes how to programmatically access and modify the metadata model.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="99fe3-107">Adding, removing or changing entities, alternate keys, attributes, or relationships can interfere with normal system operation.</span><span class="sxs-lookup"><span data-stu-id="99fe3-107">Adding, removing or changing entities, alternate keys, attributes, or relationships can interfere with normal system operation.</span></span> <span data-ttu-id="99fe3-108">If you’re applying changes to a production system we recommend that you schedule these operations when it’s least disruptive to users.</span><span class="sxs-lookup"><span data-stu-id="99fe3-108">If you’re applying changes to a production system we recommend that you schedule these operations when it’s least disruptive to users.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="99fe3-109">In This Section</span><span class="sxs-lookup"><span data-stu-id="99fe3-109">In This Section</span></span>  
 [<span data-ttu-id="99fe3-110">Customize Entity Metadata</span><span class="sxs-lookup"><span data-stu-id="99fe3-110">Customize Entity Metadata</span></span>](../customize-entity-metadata.md)  
  
 [<span data-ttu-id="99fe3-111">Customize entity attribute metadata</span><span class="sxs-lookup"><span data-stu-id="99fe3-111">Customize entity attribute metadata</span></span>](../customize-entity-attribute-metadata.md)  
  
 [<span data-ttu-id="99fe3-112">Xác định khóa thay thế cho thực thể</span><span class="sxs-lookup"><span data-stu-id="99fe3-112">Define alternate keys for an entity</span></span>](../define-alternate-keys-entity.md)  
  
 [<span data-ttu-id="99fe3-113">Entity Relationship Metadata</span><span class="sxs-lookup"><span data-stu-id="99fe3-113">Entity Relationship Metadata</span></span>](../customize-entity-relationship-metadata.md)  
  
 [<span data-ttu-id="99fe3-114">Customize global option sets</span><span class="sxs-lookup"><span data-stu-id="99fe3-114">Customize global option sets</span></span>](customize-global-option-sets.md)  
  
 [<span data-ttu-id="99fe3-115">Customize entity and attribute mappings</span><span class="sxs-lookup"><span data-stu-id="99fe3-115">Customize entity and attribute mappings</span></span>](../customize-entity-attribute-mappings.md)  
  
 [<span data-ttu-id="99fe3-116">Support Multiple Languages with Labels</span><span class="sxs-lookup"><span data-stu-id="99fe3-116">Support Multiple Languages with Labels</span></span>](../customize-labels-support-multiple-languages.md)  
  
## <a name="reference"></a><span data-ttu-id="99fe3-117">Tham chiếu</span><span class="sxs-lookup"><span data-stu-id="99fe3-117">Reference</span></span>  
 <xref:Microsoft.Xrm.Sdk.Metadata>  
  
## <a name="related-sections"></a><span data-ttu-id="99fe3-118">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="99fe3-118">Related Sections</span></span>  
 [<span data-ttu-id="99fe3-119">Extend Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="99fe3-119">Extend Dynamics 365 for Customer Engagement apps</span></span>](../extend-dynamics-365-server.md)  
  
 [<span data-ttu-id="99fe3-120">The Metadata and Data Models in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="99fe3-120">The Metadata and Data Models in Dynamics 365 for Customer Engagement apps</span></span>](../metadata-data-models.md)  
  
 [<span data-ttu-id="99fe3-121">Browse the Metadata for Your Organization</span><span class="sxs-lookup"><span data-stu-id="99fe3-121">Browse the Metadata for Your Organization</span></span>](../browse-your-metadata.md)  
  
 [<span data-ttu-id="99fe3-122">Use the Web API with metadata</span><span class="sxs-lookup"><span data-stu-id="99fe3-122">Use the Web API with metadata</span></span>](../webapi/use-web-api-metadata.md)
