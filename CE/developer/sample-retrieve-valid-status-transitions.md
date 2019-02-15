---
title: 'Sample: Retrieve valid status transitions (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to retrieve valid state transitions regardless of whether custom state transitions have been defined for the entity.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d367aa6d-36dc-4084-8625-50f515602504
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 875f36e947237fe6de8aa7f10c153cf1fb39829d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385855"
---
# <a name="sample-retrieve-valid-status-transitions"></a><span data-ttu-id="ea64c-103">Sample: Retrieve valid status transitions</span><span class="sxs-lookup"><span data-stu-id="ea64c-103">Sample: Retrieve valid status transitions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ea64c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="ea64c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="ea64c-105">Download the complete sample of [work with attribute metadata](https://code.msdn.microsoft.com/Samples-of-attributes-1c0f93e7).</span><span class="sxs-lookup"><span data-stu-id="ea64c-105">Download the complete sample of [work with attribute metadata](https://code.msdn.microsoft.com/Samples-of-attributes-1c0f93e7).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ea64c-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="ea64c-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="ea64c-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="ea64c-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="ea64c-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="ea64c-108">Demonstrates</span></span>  
 <span data-ttu-id="ea64c-109">This sample shows how to retrieve valid state transitions regardless of whether custom state transitions have been defined for the entity.</span><span class="sxs-lookup"><span data-stu-id="ea64c-109">This sample shows how to retrieve valid state transitions regardless of whether custom state transitions have been defined for the entity.</span></span>  
  
 <span data-ttu-id="ea64c-110">The sample does the following tasks:</span><span class="sxs-lookup"><span data-stu-id="ea64c-110">The sample does the following tasks:</span></span>  
  
1. <span data-ttu-id="ea64c-111">Retrieves status options for the Incident entity</span><span class="sxs-lookup"><span data-stu-id="ea64c-111">Retrieves status options for the Incident entity</span></span>  
  
2. <span data-ttu-id="ea64c-112">Uses a `GetValidStatusOptions` method in the sample to get valid status transitions for each status option</span><span class="sxs-lookup"><span data-stu-id="ea64c-112">Uses a `GetValidStatusOptions` method in the sample to get valid status transitions for each status option</span></span>  
  
3. <span data-ttu-id="ea64c-113">Displays the valid transition options in the console</span><span class="sxs-lookup"><span data-stu-id="ea64c-113">Displays the valid transition options in the console</span></span>  
  
   <span data-ttu-id="ea64c-114">When status reason transitions for the incident entity are configured in the following way:</span><span class="sxs-lookup"><span data-stu-id="ea64c-114">When status reason transitions for the incident entity are configured in the following way:</span></span>  
  
   <span data-ttu-id="ea64c-115">![Ví dụ về chuyển đổi lý do dẫn đến trạng thái với trường hợp](media/status-reason-transitions-example.PNG "Ví dụ về chuyển đổi lý do dẫn đến trạng thái với trường hợp")</span><span class="sxs-lookup"><span data-stu-id="ea64c-115">![Example of status reason transitions for case](media/status-reason-transitions-example.PNG "Example of status reason transitions for case")</span></span>  
  
   <span data-ttu-id="ea64c-116">The valid state transitions are filtered and you will see the following representing all the valid transitions for each status option.</span><span class="sxs-lookup"><span data-stu-id="ea64c-116">The valid state transitions are filtered and you will see the following representing all the valid transitions for each status option.</span></span>  
  
```ms-dos
[In Progress] incident records can transition to:  
2  Canceled  1    Canceled  
2  Canceled  1    Merged  
0  Active    1    On Hold  
  
[On Hold] incident records can transition to:  
2  Canceled  2    Canceled  
2  Canceled  2    Merged  
0  Active    2    Waiting for Details  
  
[Waiting for Details] incident records can transition to:  
2  Canceled  3    Canceled  
2  Canceled  3    Merged  
0  Active    3    Researching  
  
[Researching] incident records can transition to:  
2  Canceled  4    Canceled  
1  Resolved  4    Information Provided  
1  Resolved  4    Problem Solved  
2  Canceled  4    Merged  
  
[Problem Solved] incident records can transition to:  
2  Canceled  5    Merged  
  
[Information Provided] incident records can transition to:  
2  Canceled  1000 Merged  
  
[Canceled] incident records can transition to:  
2  Canceled  6    Merged  
  
[Merged] incident records can transition to:  
```  
  
 <span data-ttu-id="ea64c-117">When this sample is run without status reason transitions applied on the incident entity you will see the following representing all the possible transitions for each status.</span><span class="sxs-lookup"><span data-stu-id="ea64c-117">When this sample is run without status reason transitions applied on the incident entity you will see the following representing all the possible transitions for each status.</span></span>  
  
```ms-dos
[Problem Solved] incident records can transition to:  
1  Resolved  1000 Information Provided  
2  Canceled  6    Canceled  
2  Canceled  2000 Merged  
0  Active    1    In Progress  
0  Active    2    On Hold  
0  Active    3    Waiting for Details  
0  Active    4    Researching  
  
[Information Provided] incident records can transition to:  
1  Resolved  5    Problem Solved  
2  Canceled  6    Canceled  
2  Canceled  2000 Merged  
0  Active    1    In Progress  
0  Active    2    On Hold  
0  Active    3    Waiting for Details  
0  Active    4    Researching  
  
[Canceled] incident records can transition to:  
1  Resolved  5    Problem Solved  
1  Resolved  1000 Information Provided  
2  Canceled  2000 Merged  
0  Active    1    In Progress  
0  Active    2    On Hold  
0  Active    3    Waiting for Details  
0  Active    4    Researching  
  
[Merged] incident records can transition to:  
1  Resolved  5    Problem Solved  
1  Resolved  1000 Information Provided  
2  Canceled  6    Canceled  
0  Active    1    In Progress  
0  Active    2    On Hold  
0  Active    3    Waiting for Details  
0  Active    4    Researching  
  
[In Progress] incident records can transition to:  
1  Resolved  5    Problem Solved  
1  Resolved  1000 Information Provided  
2  Canceled  6    Canceled  
2  Canceled  2000 Merged  
0  Active    2    On Hold  
0  Active    3    Waiting for Details  
0  Active    4    Researching  
  
[On Hold] incident records can transition to:  
1  Resolved  5    Problem Solved  
1  Resolved  1000 Information Provided  
2  Canceled  6    Canceled  
2  Canceled  2000 Merged  
0  Active    1    In Progress  
0  Active    3    Waiting for Details  
0  Active    4    Researching  
  
[Waiting for Details] incident records can transition to:  
1  Resolved  5    Problem Solved  
1  Resolved  1000 Information Provided  
2  Canceled  6    Canceled  
2  Canceled  2000 Merged  
0  Active    1    In Progress  
0  Active    2    On Hold  
0  Active    4    Researching  
  
[Researching] incident records can transition to:  
1  Resolved  5    Problem Solved  
1  Resolved  1000 Information Provided  
2  Canceled  6    Canceled  
2  Canceled  2000 Merged  
0  Active    1    In Progress  
0  Active    2    On Hold  
0  Active    3    Waiting for Details  
```  
  
## <a name="example"></a><span data-ttu-id="ea64c-118">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="ea64c-118">Example</span></span>  
 <span data-ttu-id="ea64c-119">The following is the `GetValidStatusOptions` method used in the sample:</span><span class="sxs-lookup"><span data-stu-id="ea64c-119">The following is the `GetValidStatusOptions` method used in the sample:</span></span>  
  
 [!code-csharp[Attributes#StateModelTransitions.GetValidStatusOptions](../snippets/csharp/CRMV8/attributes/cs/statemodeltransitions.getvalidstatusoptions.cs#statemodeltransitions.getvalidstatusoptions)]  
  
## <a name="example"></a><span data-ttu-id="ea64c-120">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="ea64c-120">Example</span></span>  
 <span data-ttu-id="ea64c-121">The following is the full code for the sample.</span><span class="sxs-lookup"><span data-stu-id="ea64c-121">The following is the full code for the sample.</span></span>  
  
 [!code-csharp[Attributes#StateModelTransitions](../snippets/csharp/CRMV8/attributes/cs/statemodeltransitions.cs#statemodeltransitions)]  
  
### <a name="see-also"></a><span data-ttu-id="ea64c-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ea64c-122">See also</span></span>  
 [<span data-ttu-id="ea64c-123">Xác định chuyển tiếp mô hình trạng thái tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="ea64c-123">Define custom state model transitions</span></span>](define-custom-state-model-transitions.md)
