---
title: Data import entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Lists the data import entities used to create data maps, configure and run data imports, and log failure information.
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
- data import entities, for configuring and running data imports
- data import entities, for creating data maps
- creating data maps; and configuring and running data imports, entities for
- entities for data importing
- data import entities
- data import entities, for obtaining logs for information about data import failures
ms.assetid: e18c1e40-0c9a-417b-a7de-3c13b68128ca
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 941afd2d90d377d25f5621922fbba9cb3e50b996
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387359"
---
# <a name="data-import-entities"></a><span data-ttu-id="93636-103">Data import entities</span><span class="sxs-lookup"><span data-stu-id="93636-103">Data import entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="93636-104">The [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] data import entities are used to create data maps, configure and run data imports, and log failure information.</span><span class="sxs-lookup"><span data-stu-id="93636-104">The [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] data import entities are used to create data maps, configure and run data imports, and log failure information.</span></span>  

 <span data-ttu-id="93636-105">The following table lists the entities that are used to configure, run, and log failures for import operations.</span><span class="sxs-lookup"><span data-stu-id="93636-105">The following table lists the entities that are used to configure, run, and log failures for import operations.</span></span>  

|<span data-ttu-id="93636-106">Entity name (display name)</span><span class="sxs-lookup"><span data-stu-id="93636-106">Entity name (display name)</span></span>|<span data-ttu-id="93636-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="93636-107">Description</span></span>|  
|----------------------------------|-----------------|  
|<span data-ttu-id="93636-108">import (data import)</span><span class="sxs-lookup"><span data-stu-id="93636-108">import (data import)</span></span>|<span data-ttu-id="93636-109">Status and ownership information for the import job.</span><span class="sxs-lookup"><span data-stu-id="93636-109">Status and ownership information for the import job.</span></span>|  
|<span data-ttu-id="93636-110">importfile (import source file)</span><span class="sxs-lookup"><span data-stu-id="93636-110">importfile (import source file)</span></span>|<span data-ttu-id="93636-111">Logical source file.</span><span class="sxs-lookup"><span data-stu-id="93636-111">Logical source file.</span></span>|  
|<span data-ttu-id="93636-112">importlog (import log)</span><span class="sxs-lookup"><span data-stu-id="93636-112">importlog (import log)</span></span>|<span data-ttu-id="93636-113">Failure reason and other detailed information for a record that failed to import.</span><span class="sxs-lookup"><span data-stu-id="93636-113">Failure reason and other detailed information for a record that failed to import.</span></span>|  

 <span data-ttu-id="93636-114">The following table lists the entities that are used for creating data maps.</span><span class="sxs-lookup"><span data-stu-id="93636-114">The following table lists the entities that are used for creating data maps.</span></span>  


|                    <span data-ttu-id="93636-115">Entity name (display name)</span><span class="sxs-lookup"><span data-stu-id="93636-115">Entity name (display name)</span></span>                     |                                                                                                                      <span data-ttu-id="93636-116">Mô tả</span><span class="sxs-lookup"><span data-stu-id="93636-116">Description</span></span>                                                                                                                       |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                       <span data-ttu-id="93636-117">importmap (data map)</span><span class="sxs-lookup"><span data-stu-id="93636-117">importmap (data map)</span></span>                        |                                                                                                           <span data-ttu-id="93636-118">Data map that is used for import.</span><span class="sxs-lookup"><span data-stu-id="93636-118">Data map that is used for import.</span></span>                                                                                                            |
|                  <span data-ttu-id="93636-119">columnmapping (column mapping)</span><span class="sxs-lookup"><span data-stu-id="93636-119">columnmapping (column mapping)</span></span>                   |                                                           <span data-ttu-id="93636-120">Mapping between a column in the source file and a target attribute in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="93636-120">Mapping between a column in the source file and a target attribute in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span>                                                           |
|                  <span data-ttu-id="93636-121">lookupmapping (lookup mapping)</span><span class="sxs-lookup"><span data-stu-id="93636-121">lookupmapping (lookup mapping)</span></span>                   |       <span data-ttu-id="93636-122">Mapping between a column in the source file, or an output of a complex transformation and a target attribute of type <xref:Microsoft.Xrm.Sdk.EntityReference>.</span><span class="sxs-lookup"><span data-stu-id="93636-122">Mapping between a column in the source file, or an output of a complex transformation and a target attribute of type <xref:Microsoft.Xrm.Sdk.EntityReference>.</span></span> <span data-ttu-id="93636-123">Used in conjunction with column mapping or complex transformation mapping.</span><span class="sxs-lookup"><span data-stu-id="93636-123">Used in conjunction with column mapping or complex transformation mapping.</span></span>        |
|                   <span data-ttu-id="93636-124">ownermapping (owner mapping)</span><span class="sxs-lookup"><span data-stu-id="93636-124">ownermapping (owner mapping)</span></span>                    |                                                             <span data-ttu-id="93636-125">Mapping between a user specified in the source file and a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="93636-125">Mapping between a user specified in the source file and a user in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span>                                                             |
|                <span data-ttu-id="93636-126">picklistmapping (picklist mapping)</span><span class="sxs-lookup"><span data-stu-id="93636-126">picklistmapping (picklist mapping)</span></span>                 | <span data-ttu-id="93636-127">Mapping between a column in the source file and a target attribute of <xref:Microsoft.Xrm.Sdk.OptionSetValue>, Boolean, state, or status type in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="93636-127">Mapping between a column in the source file and a target attribute of <xref:Microsoft.Xrm.Sdk.OptionSetValue>, Boolean, state, or status type in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span> <span data-ttu-id="93636-128">Used in conjunction with column mapping.</span><span class="sxs-lookup"><span data-stu-id="93636-128">Used in conjunction with column mapping.</span></span> |
|          <span data-ttu-id="93636-129">transformationmapping (transformation mapping)</span><span class="sxs-lookup"><span data-stu-id="93636-129">transformationmapping (transformation mapping)</span></span>           |                                                                                                            <span data-ttu-id="93636-130">Complex transformation mapping.</span><span class="sxs-lookup"><span data-stu-id="93636-130">Complex transformation mapping.</span></span>                                                                                                             |
| <span data-ttu-id="93636-131">transformationparametermapping (transformation parameter mapping)</span><span class="sxs-lookup"><span data-stu-id="93636-131">transformationparametermapping (transformation parameter mapping)</span></span> |                                                                                           <span data-ttu-id="93636-132">Parameter mapping that is used in complex transformation mapping.</span><span class="sxs-lookup"><span data-stu-id="93636-132">Parameter mapping that is used in complex transformation mapping.</span></span>                                                                                            |

### <a name="see-also"></a><span data-ttu-id="93636-133">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="93636-133">See also</span></span>  
 <span data-ttu-id="93636-134">[Import Data in Dynamics 365 for Customer Engagement](import-data.md) </span><span class="sxs-lookup"><span data-stu-id="93636-134">[Import Data in Dynamics 365 for Customer Engagement](import-data.md) </span></span>  
 <span data-ttu-id="93636-135">[Import Entity](entities/import.md) </span><span class="sxs-lookup"><span data-stu-id="93636-135">[Import Entity](entities/import.md) </span></span>  
 <span data-ttu-id="93636-136">[ImportFile Entity](entities/importfile.md) </span><span class="sxs-lookup"><span data-stu-id="93636-136">[ImportFile Entity](entities/importfile.md) </span></span>  
 <span data-ttu-id="93636-137">[ImportLog Entity](entities/importlog.md) </span><span class="sxs-lookup"><span data-stu-id="93636-137">[ImportLog Entity](entities/importlog.md) </span></span>  
 <span data-ttu-id="93636-138">[ImportMap Entity](entities/importmap.md) </span><span class="sxs-lookup"><span data-stu-id="93636-138">[ImportMap Entity](entities/importmap.md) </span></span>  
 <span data-ttu-id="93636-139"><!-- jdaly These links will have content when we re-gen docs after bug 689487 is checked in. START --> [ColumnMapping Entity](entities/columnmapping.md) </span><span class="sxs-lookup"><span data-stu-id="93636-139"><!-- jdaly These links will have content when we re-gen docs after bug 689487 is checked in. START --> [ColumnMapping Entity](entities/columnmapping.md) </span></span>  
 <span data-ttu-id="93636-140">[LookupMapping Entity](entities/lookupmapping.md) </span><span class="sxs-lookup"><span data-stu-id="93636-140">[LookupMapping Entity](entities/lookupmapping.md) </span></span>  
 <span data-ttu-id="93636-141">[OwnerMapping Entity](entities/ownermapping.md) </span><span class="sxs-lookup"><span data-stu-id="93636-141">[OwnerMapping Entity](entities/ownermapping.md) </span></span>  
 <span data-ttu-id="93636-142">[PicklistMapping Entity](entities/picklistmapping.md) </span><span class="sxs-lookup"><span data-stu-id="93636-142">[PicklistMapping Entity](entities/picklistmapping.md) </span></span>  
 <span data-ttu-id="93636-143">[TransformationMapping Entity](entities/transformationmapping.md)  </span><span class="sxs-lookup"><span data-stu-id="93636-143">[TransformationMapping Entity](entities/transformationmapping.md)  </span></span>  
 <span data-ttu-id="93636-144">[TransformationParameterMapping Entity](entities/transformationparametermapping.md) </span><span class="sxs-lookup"><span data-stu-id="93636-144">[TransformationParameterMapping Entity](entities/transformationparametermapping.md) </span></span>  
 <span data-ttu-id="93636-145"><!-- jdaly These links will have content  when we re-gen docs after bug 689487 is checked in. END --> [Sample: Export and Import a Data Map](sample-export-import-data-map.md)</span><span class="sxs-lookup"><span data-stu-id="93636-145"><!-- jdaly These links will have content  when we re-gen docs after bug 689487 is checked in. END --> [Sample: Export and Import a Data Map](sample-export-import-data-map.md)</span></span>   
