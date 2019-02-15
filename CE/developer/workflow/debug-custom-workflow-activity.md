---
title: Debug a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn more about how to debug a custom workflow activity
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0922585a-006b-4229-8f6d-b7849062a156
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 93576596a4c34415bd3906d7cbcc18617c07d503
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388818"
---
# <a name="debug-a-custom-workflow-activity"></a><span data-ttu-id="6aad0-103">Debug a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="6aad0-103">Debug a custom workflow activity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6aad0-104">To debug a custom workflow activity, copy the .pdb file for the assembly to the `%installdir%\server\bin\assembly` folder.</span><span class="sxs-lookup"><span data-stu-id="6aad0-104">To debug a custom workflow activity, copy the .pdb file for the assembly to the `%installdir%\server\bin\assembly` folder.</span></span> <span data-ttu-id="6aad0-105">The assembly can be deployed as on-disk or stored in the database.</span><span class="sxs-lookup"><span data-stu-id="6aad0-105">The assembly can be deployed as on-disk or stored in the database.</span></span> <span data-ttu-id="6aad0-106">The recommended deployment is in the database, but for debugging you should select on-disk.</span><span class="sxs-lookup"><span data-stu-id="6aad0-106">The recommended deployment is in the database, but for debugging you should select on-disk.</span></span> <span data-ttu-id="6aad0-107">Next, attach the debugger to the `CrmAsyncService.exe` process.</span><span class="sxs-lookup"><span data-stu-id="6aad0-107">Next, attach the debugger to the `CrmAsyncService.exe` process.</span></span> <span data-ttu-id="6aad0-108">Make sure that you remove the .pdb file when you’ve finished debugging because it uses memory to have it loaded.</span><span class="sxs-lookup"><span data-stu-id="6aad0-108">Make sure that you remove the .pdb file when you’ve finished debugging because it uses memory to have it loaded.</span></span> <span data-ttu-id="6aad0-109">For detailed information, see [Debug a plug-In](../debug-plugin.md).</span><span class="sxs-lookup"><span data-stu-id="6aad0-109">For detailed information, see [Debug a plug-In](../debug-plugin.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6aad0-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6aad0-110">See also</span></span>  
 <span data-ttu-id="6aad0-111">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="6aad0-111">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 [<span data-ttu-id="6aad0-112">Update a custom workflow activity using assembly versioning</span><span class="sxs-lookup"><span data-stu-id="6aad0-112">Update a custom workflow activity using assembly versioning</span></span>](update-custom-workflow-activity-using-assembly-versioning.md)
