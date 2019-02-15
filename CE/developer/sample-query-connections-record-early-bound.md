---
title: 'Sample: Query connections by a record (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to query connections for a particular record after creating connections between a contact and two accounts.
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
- sample for querying connections for a particular record
- querying connections for a particular record, sample
ms.assetid: b1155815-cab2-459f-b363-2b337dcfb453
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3d21535dcf879eb130fb2a4ca40816dbeba791ac
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388244"
---
# <a name="sample-query-connections-by-a-record-early-bound"></a><span data-ttu-id="521d4-103">Sample: Query connections by a record (early bound)</span><span class="sxs-lookup"><span data-stu-id="521d4-103">Sample: Query connections by a record (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="521d4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="521d4-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="521d4-105">[Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="521d4-105">[Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="521d4-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="521d4-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="521d4-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="521d4-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="521d4-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="521d4-108">Demonstrates</span></span>  
 <span data-ttu-id="521d4-109">This sample shows how to query connections for a particular record.</span><span class="sxs-lookup"><span data-stu-id="521d4-109">This sample shows how to query connections for a particular record.</span></span> <span data-ttu-id="521d4-110">It creates connections between a contact and two accounts, and then searches for the contact’s connections.</span><span class="sxs-lookup"><span data-stu-id="521d4-110">It creates connections between a contact and two accounts, and then searches for the contact’s connections.</span></span>  
  
## <a name="example"></a><span data-ttu-id="521d4-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="521d4-111">Example</span></span>  
 [!code-csharp[BusinessManagement#QueryConnections](../snippets/csharp/CRMV8/businessmanagement/cs/queryconnections.cs#queryconnections)]  
  
### <a name="see-also"></a><span data-ttu-id="521d4-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="521d4-112">See also</span></span>  
 <span data-ttu-id="521d4-113">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span><span class="sxs-lookup"><span data-stu-id="521d4-113">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span></span>  
 [<span data-ttu-id="521d4-114">Connection Entities</span><span class="sxs-lookup"><span data-stu-id="521d4-114">Connection Entities</span></span>](connection-entities.md)
