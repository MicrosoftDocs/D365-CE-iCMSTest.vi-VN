---
title: 'Sample: Add a security principal (user or team) to a queue (early bound) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
decription: The sample code demonstrates how to give a user or team access to a queue. The AddPrincipalToQueueRequest adds the specified principal to the list of queue members.
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
- sample for sharing queues (early bound)
- giving teams limited access to queues (early bound), sample
- sharing queues (early bound), sample
- sample for limiting team access to queues (early bound)
ms.assetid: cd7c39d3-14cb-484a-a1e1-795d9d3d81ff
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0733d65d321a789e368414266c8b18c25e77cb19
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387676"
---
# <a name="sample-add-a-security-principal-user-or-team-to-a-queue-early-bound"></a><span data-ttu-id="ddc08-102">Sample: Add a security principal (user or team) to a queue (early bound)</span><span class="sxs-lookup"><span data-stu-id="ddc08-102">Sample: Add a security principal (user or team) to a queue (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ddc08-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="ddc08-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="ddc08-104">[Download the Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="ddc08-104">[Download the Business management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ddc08-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="ddc08-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a><span data-ttu-id="ddc08-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="ddc08-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="ddc08-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="ddc08-107">Demonstrates</span></span>  
 <span data-ttu-id="ddc08-108">This sample shows how to give a user or team access to a queue.</span><span class="sxs-lookup"><span data-stu-id="ddc08-108">This sample shows how to give a user or team access to a queue.</span></span> <span data-ttu-id="ddc08-109">The <xref:Microsoft.Crm.Sdk.Messages.AddPrincipalToQueueRequest> adds the specified principal to the list of queue members.</span><span class="sxs-lookup"><span data-stu-id="ddc08-109">The <xref:Microsoft.Crm.Sdk.Messages.AddPrincipalToQueueRequest> adds the specified principal to the list of queue members.</span></span> <span data-ttu-id="ddc08-110">If the passed-in security principal is a team each member of the team is added to the queue.</span><span class="sxs-lookup"><span data-stu-id="ddc08-110">If the passed-in security principal is a team each member of the team is added to the queue.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ddc08-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="ddc08-111">Example</span></span>  
 [!code-csharp[BusinessManagement#AddPrincipalToQueue](../snippets/csharp/CRMV8/businessmanagement/cs/addprincipaltoqueue.cs#addprincipaltoqueue)]  
  
### <a name="see-also"></a><span data-ttu-id="ddc08-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ddc08-112">See also</span></span>  
 <span data-ttu-id="ddc08-113">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="ddc08-113">[Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="ddc08-114">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span><span class="sxs-lookup"><span data-stu-id="ddc08-114">[Sample Code for Queue Entities](sample-code-queue-entities.md) </span></span>  
 [<span data-ttu-id="ddc08-115">Queue Entities</span><span class="sxs-lookup"><span data-stu-id="ddc08-115">Queue Entities</span></span>](queue-entities.md)
