---
title: AsyncOperation (system job) entity (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn about the system job, also known as an asynchronous operation, is used to define and track the execution of an asynchronous operation, for example an asynchronous registered plug-in, workflow, or other background system operation.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2745928e-1601-4bde-b777-cdf518a65b92
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 10a4bc9a29d4f49122d79020d5c9d742f08955e8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386849"
---
# <a name="asyncoperation-system-job-entity"></a><span data-ttu-id="b195a-103">AsyncOperation (system job) entity</span><span class="sxs-lookup"><span data-stu-id="b195a-103">AsyncOperation (system job) entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b195a-104">A *system job*, also known as an asynchronous operation, is used to define and track the execution of an asynchronous operation, for example an asynchronous registered plug-in, workflow, or other background system operation.</span><span class="sxs-lookup"><span data-stu-id="b195a-104">A *system job*, also known as an asynchronous operation, is used to define and track the execution of an asynchronous operation, for example an asynchronous registered plug-in, workflow, or other background system operation.</span></span> <span data-ttu-id="b195a-105">When dealing with asynchronous plug-ins and workflows, you typically don’t create an `asyncoperation` entity record directly.</span><span class="sxs-lookup"><span data-stu-id="b195a-105">When dealing with asynchronous plug-ins and workflows, you typically don’t create an `asyncoperation` entity record directly.</span></span> <span data-ttu-id="b195a-106">Instead, an `asyncoperation` record is automatically created in the database whenever an asynchronous system operation, such as an asynchronous plug-in or a workflow, is going to run.</span><span class="sxs-lookup"><span data-stu-id="b195a-106">Instead, an `asyncoperation` record is automatically created in the database whenever an asynchronous system operation, such as an asynchronous plug-in or a workflow, is going to run.</span></span> <span data-ttu-id="b195a-107">However, you can use the `asyncoperation` entity when you develop custom tools to manage or report on asynchronous operations in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="b195a-107">However, you can use the `asyncoperation` entity when you develop custom tools to manage or report on asynchronous operations in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps.</span></span>  
  
 <span data-ttu-id="b195a-108">Note that **System Job** is the display name of this entity when you view it in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="b195a-108">Note that **System Job** is the display name of this entity when you view it in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="b195a-109">When you write code, you use the `asyncoperation` logical name.</span><span class="sxs-lookup"><span data-stu-id="b195a-109">When you write code, you use the `asyncoperation` logical name.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b195a-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b195a-110">See also</span></span>  
 <span data-ttu-id="b195a-111">[Asynchronous Service in Dynamics 365 for Customer Engagement apps](asynchronous-service.md) </span><span class="sxs-lookup"><span data-stu-id="b195a-111">[Asynchronous Service in Dynamics 365 for Customer Engagement apps](asynchronous-service.md) </span></span>  
 [<span data-ttu-id="b195a-112">AsyncOperation Entity</span><span class="sxs-lookup"><span data-stu-id="b195a-112">AsyncOperation Entity</span></span>](entities/asyncoperation.md) 
