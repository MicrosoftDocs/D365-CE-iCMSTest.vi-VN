---
title: Update a custom workflow activity using assembly versioning (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about updating a custom workflow activity using assembly versioning.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 195362cb-792a-4a02-a2bb-852aa431706f
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 84b081acf55b9dff4bace5c0eafc0aee5db4d114
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386472"
---
# <a name="update-a-custom-workflow-activity-using-assembly-versioning"></a><span data-ttu-id="287a4-103">Update a custom workflow activity using assembly versioning</span><span class="sxs-lookup"><span data-stu-id="287a4-103">Update a custom workflow activity using assembly versioning</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="287a4-104">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, updates to your custom workflow activity assembly are handled more efficiently because of the improved assembly versioning model.</span><span class="sxs-lookup"><span data-stu-id="287a4-104">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, updates to your custom workflow activity assembly are handled more efficiently because of the improved assembly versioning model.</span></span>  
  
<a name="AssemblyVersioning"></a>   
## <a name="understand-the-assembly-version-number"></a><span data-ttu-id="287a4-105">Understand the assembly version number</span><span class="sxs-lookup"><span data-stu-id="287a4-105">Understand the assembly version number</span></span>  
 <span data-ttu-id="287a4-106">Each custom workflow activity assembly has a version number.</span><span class="sxs-lookup"><span data-stu-id="287a4-106">Each custom workflow activity assembly has a version number.</span></span> <span data-ttu-id="287a4-107">This version number is represented as a four-part string in the following format:</span><span class="sxs-lookup"><span data-stu-id="287a4-107">This version number is represented as a four-part string in the following format:</span></span>  
  
 `<major_version>.<minor_version>.<build_number>.<revision>`  
  
 <span data-ttu-id="287a4-108">For example, version `1.5.200.5` indicates `1` as the major version, `5` as the minor version, `200` as the build number, and `5` as the revision number.</span><span class="sxs-lookup"><span data-stu-id="287a4-108">For example, version `1.5.200.5` indicates `1` as the major version, `5` as the minor version, `200` as the build number, and `5` as the revision number.</span></span>  
  
<a name="UpdatingCustomActivity"></a>   
## <a name="update-a-custom-workflow-activity"></a><span data-ttu-id="287a4-109">Update a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="287a4-109">Update a custom workflow activity</span></span>  
 <span data-ttu-id="287a4-110">You might want to update your existing workflow activities to fix some bugs or to make changes in some of the private code implementation.</span><span class="sxs-lookup"><span data-stu-id="287a4-110">You might want to update your existing workflow activities to fix some bugs or to make changes in some of the private code implementation.</span></span> <span data-ttu-id="287a4-111">When updating a custom workflow activity, make sure that you do not make significant changes in the public classes or method signatures in the underlying code, such as changing the input parameters, because this might break existing workflow instances that use the custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="287a4-111">When updating a custom workflow activity, make sure that you do not make significant changes in the public classes or method signatures in the underlying code, such as changing the input parameters, because this might break existing workflow instances that use the custom workflow activity.</span></span>  
  
1. <span data-ttu-id="287a4-112">Make necessary changes in the underlying code of the custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="287a4-112">Make necessary changes in the underlying code of the custom workflow activity.</span></span>  
  
2. <span data-ttu-id="287a4-113">Change the values for `<build_number>` and `<revision>` only in the assembly information of the custom workflow activity, and compile it.</span><span class="sxs-lookup"><span data-stu-id="287a4-113">Change the values for `<build_number>` and `<revision>` only in the assembly information of the custom workflow activity, and compile it.</span></span> <span data-ttu-id="287a4-114">For example, change the value of your assembly from “1.0.0.0” to “1.0.10.5”.</span><span class="sxs-lookup"><span data-stu-id="287a4-114">For example, change the value of your assembly from “1.0.0.0” to “1.0.10.5”.</span></span>  
  
3. <span data-ttu-id="287a4-115">Update your registered custom workflow activity in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] with the new assembly.</span><span class="sxs-lookup"><span data-stu-id="287a4-115">Update your registered custom workflow activity in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] with the new assembly.</span></span>  
  
   <span data-ttu-id="287a4-116">After updating the custom workflow activity in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], all existing running process (workflows and dialogs) instances that are using the custom workflow activity will automatically start using the updated activity without requiring you to update the process definitions.</span><span class="sxs-lookup"><span data-stu-id="287a4-116">After updating the custom workflow activity in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)], all existing running process (workflows and dialogs) instances that are using the custom workflow activity will automatically start using the updated activity without requiring you to update the process definitions.</span></span>  
  
<a name="UpgradingCustomActivity"></a>   
## <a name="upgrade-a-custom-workflow-activity"></a><span data-ttu-id="287a4-117">Upgrade a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="287a4-117">Upgrade a custom workflow activity</span></span>  
 <span data-ttu-id="287a4-118">You might want to make significant changes to your custom workflow activity such as adding or removing some actions or changing the input/output parameters.</span><span class="sxs-lookup"><span data-stu-id="287a4-118">You might want to make significant changes to your custom workflow activity such as adding or removing some actions or changing the input/output parameters.</span></span> <span data-ttu-id="287a4-119">In that case, you should upgrade your custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="287a4-119">In that case, you should upgrade your custom workflow activity.</span></span>  
  
1. <span data-ttu-id="287a4-120">Make necessary changes in the underlying code of the custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="287a4-120">Make necessary changes in the underlying code of the custom workflow activity.</span></span>  
  
2. <span data-ttu-id="287a4-121">Change the values for `<major_version>` and/or `<minor_version>` in the assembly information of the custom workflow activity, and compile it.</span><span class="sxs-lookup"><span data-stu-id="287a4-121">Change the values for `<major_version>` and/or `<minor_version>` in the assembly information of the custom workflow activity, and compile it.</span></span> <span data-ttu-id="287a4-122">For example, change the value of your assembly from “1.0.0.0” to “2.0.0.0”.</span><span class="sxs-lookup"><span data-stu-id="287a4-122">For example, change the value of your assembly from “1.0.0.0” to “2.0.0.0”.</span></span>  
  
3. <span data-ttu-id="287a4-123">Register the upgraded custom workflow activity as a new assembly.</span><span class="sxs-lookup"><span data-stu-id="287a4-123">Register the upgraded custom workflow activity as a new assembly.</span></span> <span data-ttu-id="287a4-124">Make sure that the new assembly has the same `Name`,  `PublicKeyToken`, and `Culture` as the existing assembly to be considered as a different version of the same assembly.</span><span class="sxs-lookup"><span data-stu-id="287a4-124">Make sure that the new assembly has the same `Name`,  `PublicKeyToken`, and `Culture` as the existing assembly to be considered as a different version of the same assembly.</span></span>  
  
   <span data-ttu-id="287a4-125">After you upgrade the custom workflow activity, existing running process instances that are using the custom workflow activity will continue to use the older version of the custom workflow activity assembly.</span><span class="sxs-lookup"><span data-stu-id="287a4-125">After you upgrade the custom workflow activity, existing running process instances that are using the custom workflow activity will continue to use the older version of the custom workflow activity assembly.</span></span> <span data-ttu-id="287a4-126">This ensures that your existing running process instances do not break.</span><span class="sxs-lookup"><span data-stu-id="287a4-126">This ensures that your existing running process instances do not break.</span></span> <span data-ttu-id="287a4-127">If you want the process to use the new version of the custom workflow activity, you must modify the process definition to use the new version.</span><span class="sxs-lookup"><span data-stu-id="287a4-127">If you want the process to use the new version of the custom workflow activity, you must modify the process definition to use the new version.</span></span> [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="287a4-128">displays all the `<major_version>` and `<minor_version>` combinations for an assembly in a drop-down list for you to select from.</span><span class="sxs-lookup"><span data-stu-id="287a4-128">displays all the `<major_version>` and `<minor_version>` combinations for an assembly in a drop-down list for you to select from.</span></span>  
  
   <span data-ttu-id="287a4-129">![Choose a custom workflow activity version](../media/process-custom-activity-versions.png "Choose a custom workflow activity version")</span><span class="sxs-lookup"><span data-stu-id="287a4-129">![Choose a custom workflow activity version](../media/process-custom-activity-versions.png "Choose a custom workflow activity version")</span></span>  
  
   <span data-ttu-id="287a4-130">Optionally, after you have updated all your process definitions to use the newer version, you could also unregister the older versions of the custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="287a4-130">Optionally, after you have updated all your process definitions to use the newer version, you could also unregister the older versions of the custom workflow activity.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="287a4-131">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="287a4-131">See also</span></span>  
 <span data-ttu-id="287a4-132">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="287a4-132">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 [<span data-ttu-id="287a4-133">Process classes, attributes, and types</span><span class="sxs-lookup"><span data-stu-id="287a4-133">Process classes, attributes, and types</span></span>](process-classes-attributes-and-types.md)
