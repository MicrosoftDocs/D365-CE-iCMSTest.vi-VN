---
title: 'Sample: Create a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to write a custom workflow activity that can create an account and a task for the account. This sample uses early binding.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6d498e86-8702-43ed-bf76-96d1b4246dfd
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 447b9b12c72981d347437977ea669e9abce7b9dc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386239"
---
# <a name="sample-create-a-custom-workflow-activity"></a><span data-ttu-id="37142-104">Sample: Create a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="37142-104">Sample: Create a custom workflow activity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="37142-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="37142-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="37142-106">Download the complete sample here [Custom workflow activities sample](https://code.msdn.microsoft.com/Custom-Workflow-Activities-eee57285).</span><span class="sxs-lookup"><span data-stu-id="37142-106">Download the complete sample here [Custom workflow activities sample](https://code.msdn.microsoft.com/Custom-Workflow-Activities-eee57285).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="37142-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="37142-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="37142-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="37142-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="37142-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="37142-109">Demonstrates</span></span>  
 <span data-ttu-id="37142-110">This sample shows how to write a custom workflow activity that can create an account and a task for the account.</span><span class="sxs-lookup"><span data-stu-id="37142-110">This sample shows how to write a custom workflow activity that can create an account and a task for the account.</span></span> <span data-ttu-id="37142-111">This sample uses early binding.</span><span class="sxs-lookup"><span data-stu-id="37142-111">This sample uses early binding.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37142-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="37142-112">Example</span></span>  
 [!code-csharp[customworkflowactivities#simplesdkactivity](../../snippets/csharp/CRMV8/customworkflowactivities/cs/simplesdkactivity.cs#simplesdkactivity)]  
  
### <a name="see-also"></a><span data-ttu-id="37142-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="37142-113">See also</span></span>  
 <span data-ttu-id="37142-114">[Custom Workflow Activities (Workflow Assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="37142-114">[Custom Workflow Activities (Workflow Assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 <span data-ttu-id="37142-115">[Sample: Update Next Birthday Using a Custom Workflow Activity](sample-update-next-birthday-using-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="37142-115">[Sample: Update Next Birthday Using a Custom Workflow Activity](sample-update-next-birthday-using-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="37142-116">[Sample Code for Processes](../sample-code-processes.md) </span><span class="sxs-lookup"><span data-stu-id="37142-116">[Sample Code for Processes](../sample-code-processes.md) </span></span>  
 <span data-ttu-id="37142-117">[Creating a Custom Workflow Activity](create-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="37142-117">[Creating a Custom Workflow Activity](create-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="37142-118">[Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="37142-118">[Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span></span>  
 [<span data-ttu-id="37142-119">Using the IOrganization Web Service within a Custom Workflow Activity</span><span class="sxs-lookup"><span data-stu-id="37142-119">Using the IOrganization Web Service within a Custom Workflow Activity</span></span>](use-iorganization-web-service-custom-workflow-activity.md)
