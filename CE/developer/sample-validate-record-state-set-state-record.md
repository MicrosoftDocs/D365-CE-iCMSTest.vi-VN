---
title: 'Sample: Validate record state and set the state of the record (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample demonstrates how to validate a change of state of an entity and set a state of an entity.
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
- setting record states sample
- validating record states sample
- record states, sample for validating and setting
ms.assetid: 6b2f00ca-dbac-47d8-ab4a-0be52b72f05d
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: eb44c575e996b3e16dc1713509108439b5b7b6bc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387297"
---
# <a name="sample-validate-record-state-and-set-the-state-of-the-record"></a><span data-ttu-id="652cc-103">Sample: Validate record state and set the state of the record</span><span class="sxs-lookup"><span data-stu-id="652cc-103">Sample: Validate record state and set the state of the record</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="652cc-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="652cc-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="652cc-105">Download the complete sample from [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)</span><span class="sxs-lookup"><span data-stu-id="652cc-105">Download the complete sample from [Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62)</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="652cc-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="652cc-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="652cc-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="652cc-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="652cc-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="652cc-108">Demonstrates</span></span>  
 <span data-ttu-id="652cc-109">This sample shows how to validate a change of state of an entity and set a state of an entity.</span><span class="sxs-lookup"><span data-stu-id="652cc-109">This sample shows how to validate a change of state of an entity and set a state of an entity.</span></span>  
  
## <a name="example"></a><span data-ttu-id="652cc-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="652cc-110">Example</span></span>  
 [!code-csharp[BusinessManagement#ValidateAndSetState](../snippets/csharp/CRMV8/businessmanagement/cs/validateandsetstate.cs#validateandsetstate)]  
  
### <a name="see-also"></a><span data-ttu-id="652cc-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="652cc-111">See also</span></span>  
 <span data-ttu-id="652cc-112">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md) </span><span class="sxs-lookup"><span data-stu-id="652cc-112">[Introduction to Entities in Dynamics 365 for Customer Engagement apps](introduction-entities.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>   
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>   
 [<span data-ttu-id="652cc-113">Sample: Rollup records related to a specific record</span><span class="sxs-lookup"><span data-stu-id="652cc-113">Sample: Rollup records related to a specific record</span></span>](sample-rollup-records-related-specific-record.md)
