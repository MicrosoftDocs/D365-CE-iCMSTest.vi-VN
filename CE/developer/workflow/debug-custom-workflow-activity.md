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
# <a name="debug-a-custom-workflow-activity"></a>Debug a custom workflow activity

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

To debug a custom workflow activity, copy the .pdb file for the assembly to the `%installdir%\server\bin\assembly` folder. The assembly can be deployed as on-disk or stored in the database. The recommended deployment is in the database, but for debugging you should select on-disk. Next, attach the debugger to the `CrmAsyncService.exe` process. Make sure that you remove the .pdb file when you’ve finished debugging because it uses memory to have it loaded. For detailed information, see [Debug a plug-In](../debug-plugin.md).  
  
### <a name="see-also"></a>Xem thêm  
 [Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md)   
 [Update a custom workflow activity using assembly versioning](update-custom-workflow-activity-using-assembly-versioning.md)
