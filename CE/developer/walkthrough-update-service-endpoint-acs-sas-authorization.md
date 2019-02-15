---
title: 'Walkthrough: Update a service endpoint from ACS to SAS authorization (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The walkthrough demonstrates updating a service endpoint from Access Control Service (ACS) to Shared Access Signature (SAS) authorization.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a1a4fe6f-be17-4a75-af6c-cd1ee901b868
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4c8905d673d5cac646cc34c75693be673edb1fbd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385621"
---
# <a name="walkthrough-update-a-service-endpoint-from-acs-to-sas-authorization"></a>Walkthrough: Update a service endpoint from ACS to SAS authorization

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Shared Access Signature (SAS) is the recommended authorization method for the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement and [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] integration as its use results in improved authorization performance compared to Access Control Service (ACS), and SAS is supported on all [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] deployments without any special server configuration. You can update existing service endpoint entity records in a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization from ACS to SAS authorization by using the Plug-in Registration Tool and following these steps.  
  
> [!NOTE]
> [!INCLUDE[cc_feature_included_with_update_8_1_0_admins](../includes/cc-feature-included-with-update-8-1-0-admins.md)] The Plug-in Registration Tool from the v8.1 or later [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] SDK includes SAS support.  
  
## <a name="step-1-update-the-messaging-entity"></a>Step 1: Update the messaging entity  
 You'll need to update your [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] messaging entity that was configured for ACS authorization, for example a queue or topic, to be properly configured for SAS. This is simple to do as you just need to add a SAS shared access policy.  
  
### <a name="perform-the-update"></a>Perform the update  
  
1. Sign in to the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)][Classic portal](https://manage.windowsazure.com).  
  
2. Navigate to the messaging entity that you plan to update.  
  
3. Select the entity and then select **CONFIGURE**.  
  
4. Create a shared access policy and specify **Send** permission at a minimum. **Listen** permission is required for a two-way endpoint contract.  
  
5. Verify the messaging entity's SAS connection information. It should have a connection string.  
  
## <a name="step-2-update-the-service-endpoint"></a>Step 2: Update the service endpoint  
 Now go ahead an update the service endpoint entity record in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization with the SAS information of your messaging entity.  
  
### <a name="perform-the-update"></a>Perform the update  
  
1. Run the Plug-in Registration Tool and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] organization containing the service endpoint.  
  
2. Select the service endpoint and then select **Update**.  
  
3. Enter a value for the **SAS Key Name** and the **SAS Key**. These are obtained from the messaging entity's connection string that is available in the [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] management portal. Look for SharedAccessKeyName and `SharedAccessKey` values in the connection string.  
  
4. Chọn **Lưu**.  
  
### <a name="see-also"></a>Xem thêm  
 [Azure extensions for Dynamics 365 for Customer Engagement](azure-extensions.md)   
 [Azure integration with Dynamics 365 for Customer Engagement](azure-integration.md)
