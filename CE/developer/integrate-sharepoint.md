---
title: Integrate Dynamics 365 for Customer Engagement with SharePoint (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: The SharePoint integration feature enables you to store and manage documents on SharePoint in the context of a Dynamics 365 for Customer Engagement apps record, and use the SharePoint document management abilities in Dynamics 365 for Customer Engagement apps, such as checking the document in and out, viewing version history, and changing document properties.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: fc7f8994-a531-48d1-8495-3f8663f6c3e3
caps.latest.revision: 52
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f5a0faf2aa24d260310350b1fec5287d51e62935
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386422"
---
# <a name="integrate-dynamics-365-for-customer-engagement-apps-with-sharepoint"></a>Integrate Dynamics 365 for Customer Engagement apps with SharePoint

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_ms_sharepoint_server](../includes/pn-ms-sharepoint-server.md)] is a collaboration and content management application that simplifies how people store, find, and share information. It helps people to collaborate effectively by having secure access to documents and information that they require to make business decisions.  
  
 The [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] integration feature enables you to store and manage documents on [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] in the context of a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps record, and use the [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] apps document management abilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps, such as checking the document in and out, viewing version history, and changing document properties.  
  
 [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps support two types of integration with [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)] apps: client-to-server and server-to-server (server-based). [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Enable SharePoint integration](integration-dev/get-started-sharepoint-integration.md#SPIntegration)  
  
 Use the `SharePointSite` and `SharePointDocumentLocation` entities to store and manage the [!INCLUDE[pn_SharePoint_Server_short](../includes/pn-sharepoint-server-short.md)] location records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and the `UserMapping` entity to define custom claim mappings to use a value other than the default value used by [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] apps to authenticate and authorize [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps user in [!INCLUDE[pn_SharePoint_short](../includes/pn-sharepoint-short.md)].  
  
## <a name="in-this-section"></a>In This Section  
 [Understanding Dynamics 365 for Customer Engagement apps and SharePoint Integration](integration-dev/get-started-sharepoint-integration.md)  
  
 [Enable SharePoint Integration](integration-dev/enable-document-management-entities.md)  
  
 [Actions on SharePoint Location Records](integration-dev/actions-on-sharepoint-location-records.md)  
  
 [Define custom claim mapping for SharePoint server-based integration](integration-dev/define-custom-claim-mapping-sharepoint-server-based-integration.md)  
  
 [Sample: Enable Document Management for Entities](integration-dev/sample-enable-document-management-entities.md)  
  
 [Sample: Create, Retrieve, Update, and Delete a SharePoint Location Record](integration-dev/sample-create-retrieve-update-delete-sharepoint-location-record.md)  
  
 [Sample: Retrieve Absolute URL and Site Collection URL of a Location Record](integration-dev/sample-retrieve-absolute-url-and-site-collection-url-of-a-location-record.md)  
  
## <a name="reference"></a>Tham chiếu  
 [Manage your documents using SharePoint](../admin/manage-documents-using-sharepoint.md)  
  
 [Office and SharePoint development](https://docs.microsoft.com/visualstudio/vsto/office-and-sharepoint-development-in-visual-studio)  
   
## <a name="related-sections"></a>Các phần liên quan  
 [Extend Dynamics 365 for Customer Engagement apps](extend-dynamics-365-server.md)  
  
 [Supported Extensions for Dynamics 365 for Customer Engagement apps](supported-extensions.md)  
  
 [The Metadata and Data Models in Dynamics 365 for Customer Engagement apps](metadata-data-models.md)  
  
 [Extend Dynamics 365 for Customer Engagement on the server apps](extend-dynamics-365-server.md)  
  
 [Extend Dynamics 365 for Customer Engagement on the client apps](extend-client.md)  
  
 [Customize Dynamics 365 for Customer Engagement applications](customize-dev/customize-applications.md)  
  
 [Package and distribute extensions using solutions](package-distribute-extensions-use-solutions.md)  
  
 [Extend Dynamics 365 for Outlook](extend-customer-engagement-outlook.md)  
  
 [Integrate Dynamics 365 for Customer Engagement apps with OneNote](integration-dev/integrate-onenote.md) 
  
 
