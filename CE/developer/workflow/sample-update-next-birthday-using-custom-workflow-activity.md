---
title: 'Sample: Update next birthday using a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample demonstrates workflow activity returns the next birthday. Use this in a workflow that sends a birthday greeting to a customer. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1cff83b0-1f7b-4ddb-a2af-b85f9f785529
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b42b552712de4accac5a2e6a606e821f1e0d15bb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385852"
---
# <a name="sample-update-next-birthday-using-a-custom-workflow-activity"></a><span data-ttu-id="99277-104">Sample: Update next birthday using a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="99277-104">Sample: Update next birthday using a custom workflow activity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="99277-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="99277-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="99277-106">Download the complete sample here [Custom workflow activities sample](https://code.msdn.microsoft.com/Custom-Workflow-Activities-eee57285).</span><span class="sxs-lookup"><span data-stu-id="99277-106">Download the complete sample here [Custom workflow activities sample](https://code.msdn.microsoft.com/Custom-Workflow-Activities-eee57285).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="99277-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="99277-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="99277-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="99277-108">Requirements</span></span>  
 <span data-ttu-id="99277-109">The following custom field must exist for this custom workflow activity to work:</span><span class="sxs-lookup"><span data-stu-id="99277-109">The following custom field must exist for this custom workflow activity to work:</span></span>  
  
-   <span data-ttu-id="99277-110">Contact.new_nextbirthday</span><span class="sxs-lookup"><span data-stu-id="99277-110">Contact.new_nextbirthday</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="99277-111">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="99277-111">Demonstrates</span></span>  
 <span data-ttu-id="99277-112">The following sample workflow activity returns the next birthday.</span><span class="sxs-lookup"><span data-stu-id="99277-112">The following sample workflow activity returns the next birthday.</span></span> <span data-ttu-id="99277-113">Use this in a workflow that sends a birthday greeting to a customer.</span><span class="sxs-lookup"><span data-stu-id="99277-113">Use this in a workflow that sends a birthday greeting to a customer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="99277-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="99277-114">Example</span></span>  
 [!code-csharp[customworkflowactivities#ReleaseISVActivities](../../snippets/csharp/CRMV8/customworkflowactivities/cs/releaseisvactivities.cs#releaseisvactivities)]  
  
### <a name="see-also"></a><span data-ttu-id="99277-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="99277-115">See also</span></span>  
 <span data-ttu-id="99277-116">[Custom Workflow Activities (Workflow Assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="99277-116">[Custom Workflow Activities (Workflow Assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 <span data-ttu-id="99277-117">[Sample: Calculate a Credit Score with a Custom Workflow Activity](sample-calculate-credit-score-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="99277-117">[Sample: Calculate a Credit Score with a Custom Workflow Activity](sample-calculate-credit-score-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="99277-118">[Add Metadata to a Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="99277-118">[Add Metadata to a Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Workflow.IWorkflowContext>
