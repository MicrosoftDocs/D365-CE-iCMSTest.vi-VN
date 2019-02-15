---
title: 'Walkthrough: Update a service endpoint imported from a solution (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The walkthrough demonstrates updating a service endpoint imported from a solution.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8c860992-d3c6-4bfa-86c4-98018af6f22c
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 89d75425cd8d129ba1845270ff368f3290921845
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385553"
---
# <a name="walkthrough-update-a-service-endpoint-imported-from-a-solution"></a>Walkthrough: Update a service endpoint imported from a solution

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

An extra step is required after importing into an organization a solution containing one or more service endpoints configured for SAS authorization. When the solution containing the service endpoints is exported, the exported solution does not contain the SAS Key for each service endpoint. After importing the solution into an organization, you must perform an additional step to provide the SAS Key for each service endpoint.  
  
 Follow these steps to set the SAS Key for each service endpoint after solution import.  
  
### <a name="update-the-sas-key"></a>Update the SAS Key  
  
1. Run the Plug-in Registration Tool, which can be found in the Tools folder of the [!INCLUDE[pn_crm_8_1_0_op](../includes/pn-crm-8-1-0-op.md)] (or later) SDK download. Previous releases of the tool do not support SAS authorization.  
  
2. Using the tool, sign in to the organization that contains the imported solution.  
  
3. Select the target service endpoint in the tab view of the organization.  
  
4. Chọn **Cập nhật**. You should see the following form with the fields already filled in.  
  
   ![Update service endpoint SAS key value](media/sas-key.PNG "Update service endpoint SAS key value")  
  
5. The **SAS Key** field is displayed with a value of "*******".  Replace that value with the correct SAS key value. You can obtain the SAS Key for your [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] messaging entity (queue, topic, etc.) from the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)][classic portal](http://manage.windowsazure.com).  
  
6. Chọn **Lưu**.  
  
### <a name="see-also"></a>Xem thêm  
 [Azure extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md)   
 [Service Bus authentication and authorization](https://azure.microsoft.com/en-us/documentation/articles/service-bus-authentication-and-authorization/)
