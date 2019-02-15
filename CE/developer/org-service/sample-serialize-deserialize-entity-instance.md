---
title: 'Sample: Serialize and deserialize an entity Instance (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to serialize early-bound and late-bound entity instances into an XML format, and how to de-serialize from an XML format to an early-bound entity instance
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- samples for early-bound classes, serializing and deserializing entities sample
- sample for serializing and deserializing entities
- serializing and deserializing entities sample, early-bound class samples
- early-bound class samples, serializing and deserializing entities sample
ms.assetid: 705f78dc-c392-4ca7-bc48-0ed3fc687a6f
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 99130a2dc9649873779ec7e0488b69761cdb4542
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388225"
---
# <a name="sample-serialize-and-deserialize-an-entity-instance"></a><span data-ttu-id="73ee9-103">Sample: Serialize and deserialize an entity Instance</span><span class="sxs-lookup"><span data-stu-id="73ee9-103">Sample: Serialize and deserialize an entity Instance</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="73ee9-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="73ee9-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> <span data-ttu-id="73ee9-105">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="73ee9-105">Download the complete sample here [Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="73ee9-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="73ee9-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="73ee9-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="73ee9-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="73ee9-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="73ee9-108">Demonstrates</span></span>  
 <span data-ttu-id="73ee9-109">This sample shows how to serialize early-bound and late-bound entity instances into an XML format, and how to de-serialize from an XML format to an early-bound entity instance.</span><span class="sxs-lookup"><span data-stu-id="73ee9-109">This sample shows how to serialize early-bound and late-bound entity instances into an XML format, and how to de-serialize from an XML format to an early-bound entity instance.</span></span>  
  
## <a name="example"></a><span data-ttu-id="73ee9-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="73ee9-110">Example</span></span>  
 [!code-csharp[BusinessManagement#SerializeAndDeserialize](../../snippets/csharp/CRMV8/businessmanagement/cs/serializeanddeserialize.cs#serializeanddeserialize)]  
  
### <a name="see-also"></a><span data-ttu-id="73ee9-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="73ee9-111">See also</span></span>  
 <span data-ttu-id="73ee9-112">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span><span class="sxs-lookup"><span data-stu-id="73ee9-112">[Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md) </span></span>  
 <span data-ttu-id="73ee9-113">[Sample: Initialize a Record From an Existing Record](sample-initialize-record-existing-record.md) </span><span class="sxs-lookup"><span data-stu-id="73ee9-113">[Sample: Initialize a Record From an Existing Record](sample-initialize-record-existing-record.md) </span></span>  
 <span data-ttu-id="73ee9-114">[Mix Early and Late Bound Entities](mix-early-late-bound-entities.md) </span><span class="sxs-lookup"><span data-stu-id="73ee9-114">[Mix Early and Late Bound Entities](mix-early-late-bound-entities.md) </span></span>  
 [<span data-ttu-id="73ee9-115">DataContractSerializer Class</span><span class="sxs-lookup"><span data-stu-id="73ee9-115">DataContractSerializer Class</span></span>](https://msdn.microsoft.com/library/system.runtime.serialization.datacontractserializer.aspx)
