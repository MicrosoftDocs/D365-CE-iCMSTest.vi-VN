---
title: 'Sample: Work with solutions (Dynamics 365 for Customer Engagement apps SDK)| MicrosoftDocs'
description: ''
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a3008ed8-a934-4790-9979-43be7b5e7aaf
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
helpviewer_keywords:
- solution entities samples
- samples for working with solutions, deleting solutions
- samples for working with solutions, exporting or packaging solutions
- samples for working with solutions, retrieving default publishers
- samples for working with solutions, adding existing solution components
- samples for working with solutions, creating publishers
- sample for working with solutions
- samples for working with solutions, creating solutions
- samples for working with solutions, retrieving solutions
- sample for solutions, see samples for working with solutions
- samples for working with solutions, removing solution components
- samples for working with solutions, installing or upgrading solutions
- working with solutions samples
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e38b9d5a133ddf06297dab02a1f9c062d6a4ea52
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388582"
---
# <a name="sample-work-with-solutions"></a><span data-ttu-id="78d07-102">Sample: Work with solutions</span><span class="sxs-lookup"><span data-stu-id="78d07-102">Sample: Work with solutions</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="78d07-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="78d07-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="78d07-104">Download the sample: [Work with solutions](https://code.msdn.microsoft.com/Sample-Work-with-solutions-a496ee8f).</span><span class="sxs-lookup"><span data-stu-id="78d07-104">Download the sample: [Work with solutions](https://code.msdn.microsoft.com/Sample-Work-with-solutions-a496ee8f).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="78d07-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="78d07-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="78d07-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="78d07-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="78d07-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="78d07-107">Demonstrates</span></span>  
 <span data-ttu-id="78d07-108">This sample shows how to how to perform the following actions with solutions:</span><span class="sxs-lookup"><span data-stu-id="78d07-108">This sample shows how to how to perform the following actions with solutions:</span></span>  
  
-   <span data-ttu-id="78d07-109">Create a publisher.</span><span class="sxs-lookup"><span data-stu-id="78d07-109">Create a publisher.</span></span>  
-   <span data-ttu-id="78d07-110">Retrieve the default publisher.</span><span class="sxs-lookup"><span data-stu-id="78d07-110">Retrieve the default publisher.</span></span>  
-   <span data-ttu-id="78d07-111">Tạo một giải pháp.</span><span class="sxs-lookup"><span data-stu-id="78d07-111">Create a solution.</span></span>  
-   <span data-ttu-id="78d07-112">Retrieve a solution.</span><span class="sxs-lookup"><span data-stu-id="78d07-112">Retrieve a solution.</span></span>  
-   <span data-ttu-id="78d07-113">Add an existing solution component.</span><span class="sxs-lookup"><span data-stu-id="78d07-113">Add an existing solution component.</span></span>  
-   <span data-ttu-id="78d07-114">Remove a solution component.</span><span class="sxs-lookup"><span data-stu-id="78d07-114">Remove a solution component.</span></span>  
-   <span data-ttu-id="78d07-115">Export or package a solution.</span><span class="sxs-lookup"><span data-stu-id="78d07-115">Export or package a solution.</span></span>  
-   <span data-ttu-id="78d07-116">Install or upgrade a solution.</span><span class="sxs-lookup"><span data-stu-id="78d07-116">Install or upgrade a solution.</span></span>  
-   <span data-ttu-id="78d07-117">Delete a solution.</span><span class="sxs-lookup"><span data-stu-id="78d07-117">Delete a solution.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78d07-118">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="78d07-118">Example</span></span>  
 [!code-csharp[Solutions#WorkWithSolutions](../snippets/csharp/CRMV8/solutions/cs/workwithsolutions.cs#workwithsolutions)]  
  
### <a name="see-also"></a><span data-ttu-id="78d07-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="78d07-119">See also</span></span>  
 <span data-ttu-id="78d07-120">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-120">[Package and Distribute Extensions with Dynamics 365 for Customer Engagement Solutions](package-distribute-extensions-use-solutions.md) </span></span>  
 <span data-ttu-id="78d07-121">[Sample: Detect Solution Dependencies](sample-detect-solution-dependencies.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-121">[Sample: Detect Solution Dependencies](sample-detect-solution-dependencies.md) </span></span>  
 <span data-ttu-id="78d07-122">[Introduction to Solutions](introduction-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-122">[Introduction to Solutions](introduction-solutions.md) </span></span>  
 <span data-ttu-id="78d07-123">[Plan For Solution Development](plan-solution-development.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-123">[Plan For Solution Development](plan-solution-development.md) </span></span>  
 <span data-ttu-id="78d07-124">[Dependency Tracking for Solution Components](dependency-tracking-solution-components.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-124">[Dependency Tracking for Solution Components](dependency-tracking-solution-components.md) </span></span>  
 <span data-ttu-id="78d07-125">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-125">[Create, Export, or Import an Unmanaged Solution](create-export-import-unmanaged-solution.md) </span></span>  
 <span data-ttu-id="78d07-126">[Create, Install, and Update a Managed Solution](create-install-update-managed-solution.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-126">[Create, Install, and Update a Managed Solution](create-install-update-managed-solution.md) </span></span>  
 <span data-ttu-id="78d07-127">[Uninstall or Delete a Solution](uninstall-delete-solution.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-127">[Uninstall or Delete a Solution](uninstall-delete-solution.md) </span></span>  
 <span data-ttu-id="78d07-128">[Solution Entities](solution-entities.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-128">[Solution Entities](solution-entities.md) </span></span>  
 <span data-ttu-id="78d07-129">[Work with Solutions](work-solutions.md) </span><span class="sxs-lookup"><span data-stu-id="78d07-129">[Work with Solutions](work-solutions.md) </span></span>  
 [<span data-ttu-id="78d07-130">Sample: Detect Solution Dependencies</span><span class="sxs-lookup"><span data-stu-id="78d07-130">Sample: Detect Solution Dependencies</span></span>](sample-detect-solution-dependencies.md)
