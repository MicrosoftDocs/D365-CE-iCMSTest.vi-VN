---
title: 'Sample: Create, retrieve, update, and delete (late bound) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample demonstrates the create, retrieve, update, and delete operations on an account using the late bound Entity class
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- sample for late-bound Entity classes, creating; retrieving; updating; and deleting (late-bound Entity classes) sample
- creating; retrieving; updating; and deleting (late-bound Entity classes) sample
- sample for creating; retrieving; updating; and deleting (late-bound Entity classes)
- late-bound Entity classes, samples
ms.assetid: 9f4f05c6-0d19-4a32-8ef3-776757c0ea86
caps.latest.revision: 27
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f481d38b9809cbe3c2e5472260aec53f12d6ff98
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385988"
---
# <a name="sample-create-retrieve-update-and-delete-late-bound"></a><span data-ttu-id="67c28-103">Sample: Create, retrieve, update, and delete (late bound)</span><span class="sxs-lookup"><span data-stu-id="67c28-103">Sample: Create, retrieve, update, and delete (late bound)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="67c28-104">This sample is for [!INCLUDE[pn_crm_2015_and_online_full](../../includes/pn-crm-2015-and-online-full.md)].</span><span class="sxs-lookup"><span data-stu-id="67c28-104">This sample is for [!INCLUDE[pn_crm_2015_and_online_full](../../includes/pn-crm-2015-and-online-full.md)].</span></span> <span data-ttu-id="67c28-105">Download the sample: [Sample: Create, retrieve, update and delete (late bound)](https://code.msdn.microsoft.com/Sample-Create-retrieve-e183a7fb).</span><span class="sxs-lookup"><span data-stu-id="67c28-105">Download the sample: [Sample: Create, retrieve, update and delete (late bound)](https://code.msdn.microsoft.com/Sample-Create-retrieve-e183a7fb).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="67c28-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="67c28-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]

## <a name="requirements"></a><span data-ttu-id="67c28-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="67c28-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="example"></a><span data-ttu-id="67c28-108">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="67c28-108">Example</span></span>  
 <span data-ttu-id="67c28-109">This sample demonstrates the create, retrieve, update, and delete operations on an account using the late bound <xref:Microsoft.Xrm.Sdk.Entity> class.</span><span class="sxs-lookup"><span data-stu-id="67c28-109">This sample demonstrates the create, retrieve, update, and delete operations on an account using the late bound <xref:Microsoft.Xrm.Sdk.Entity> class.</span></span>  
  
 [!code-csharp[DynamicEntity#CRUDOperationsDE](../../snippets/csharp/CRMV8/dynamicentity/cs/crudoperationsde.cs#crudoperationsde)]  
  
### <a name="see-also"></a><span data-ttu-id="67c28-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="67c28-110">See also</span></span>  
 <span data-ttu-id="67c28-111">[Use the Late Bound Entity Class in Code](use-late-bound-entity-class-code.md) </span><span class="sxs-lookup"><span data-stu-id="67c28-111">[Use the Late Bound Entity Class in Code](use-late-bound-entity-class-code.md) </span></span>  
 <span data-ttu-id="67c28-112">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="67c28-112">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>   
 [<span data-ttu-id="67c28-113">Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types</span><span class="sxs-lookup"><span data-stu-id="67c28-113">Sample: Create, Retrieve, Update and Delete (CRUD) Using Strong Types</span></span>](sample-create-retrieve-update-delete-records-early-bound.md)
