---
title: 'Sample: Create a reciprocal connection role (early bound) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample code demonstrates how to create the reciprocal connection roles.
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
- creating reciprocal connection roles, sample
- sample for creating reciprocal connection roles
ms.assetid: 768e2422-e725-4de4-85c9-17dff24ee69c
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bd1d524e043b4e038f08bd083665bf0f941a8007
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388145"
---
# <a name="sample-create-a-reciprocal-connection-role-early-bound"></a><span data-ttu-id="a44b0-103">Sample: Create a reciprocal connection role (early bound)</span><span class="sxs-lookup"><span data-stu-id="a44b0-103">Sample: Create a reciprocal connection role (early bound)</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a44b0-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="a44b0-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="a44b0-105">[Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span><span class="sxs-lookup"><span data-stu-id="a44b0-105">[Download the Business Management samples](https://code.msdn.microsoft.com/Business-Management-Samples-6a482e62).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a44b0-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="a44b0-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="a44b0-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="a44b0-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="a44b0-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="a44b0-108">Demonstrates</span></span>  
 <span data-ttu-id="a44b0-109">This sample shows how to create the reciprocal connection roles.</span><span class="sxs-lookup"><span data-stu-id="a44b0-109">This sample shows how to create the reciprocal connection roles.</span></span> <span data-ttu-id="a44b0-110">It creates a connection role for an account and a connection role for a contact, and then makes them reciprocal by associating them with each other.</span><span class="sxs-lookup"><span data-stu-id="a44b0-110">It creates a connection role for an account and a connection role for a contact, and then makes them reciprocal by associating them with each other.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a44b0-111">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="a44b0-111">Example</span></span>  
 [!code-csharp[BusinessManagement#CreateReciprocalConnectionRole](../snippets/csharp/CRMV8/businessmanagement/cs/createreciprocalconnectionrole.cs#createreciprocalconnectionrole)]  
  
### <a name="see-also"></a><span data-ttu-id="a44b0-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="a44b0-112">See also</span></span>  
 <span data-ttu-id="a44b0-113">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span><span class="sxs-lookup"><span data-stu-id="a44b0-113">[Sample Code for Connection Entities](sample-code-connection-entities.md) </span></span>  
 <span data-ttu-id="a44b0-114">[Connection Entities](connection-entities.md) </span><span class="sxs-lookup"><span data-stu-id="a44b0-114">[Connection Entities](connection-entities.md) </span></span>  
 [<span data-ttu-id="a44b0-115">Sample: Update a Connection Role (Early Bound)</span><span class="sxs-lookup"><span data-stu-id="a44b0-115">Sample: Update a Connection Role (Early Bound)</span></span>](sample-update-connection-role-early-bound.md)
