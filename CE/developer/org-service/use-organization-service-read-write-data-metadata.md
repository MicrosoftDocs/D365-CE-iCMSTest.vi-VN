---
title: Use the Organization Service to read and write data or metadata (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: IOrganizationService is the primary web service that accesses data and metadata for your organization. This web service contains the methods that you use to write code that uses all the data and metadata in Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8c212d9c-cfd6-4dcb-9d11-04b7cb472dbc
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b8426038d0fc22a368571f754c6b4b1615fe14e4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386856"
---
# <a name="use-the-organization-service-to-read-and-write-data-or-metadata"></a>Use the Organization Service to read and write data or metadata

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, the primary web service that accesses data and metadata for your organization is <xref:Microsoft.Xrm.Sdk.IOrganizationService>. This web service contains the methods that you use to write code that uses all the data and metadata in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps.  
  
 To use the `IOrganizationService` web service, add a reference to the Microsoft.Xrm.Sdk.dll assembly to your [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] project. To access the non-core xRM messages, add a reference to the Microsoft.Crm.Sdk.Proxy.dll assembly to your project also. Alternatively, add the service reference to your project. [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] [Developer resources page](../developer-resources-page.md)
  
## <a name="in-this-section"></a>In This Section  
 [IOrganizationService Methods](organization-service-methods.md)  
  
 [Use Messages](use-messages-request-response-classes-execute-method.md)  
  
 [Use Execute Multiple to Improve Performance](use-executemultiple-improve-performance-bulk-data-load.md)  
  
 [Microsoft.Xrm.Sdk Messages](xrm-messages-organization-service.md)  
  
 [Microsoft.Crm.Sdk Data Messages](organization-service-messages.md)  
  
 [Perform specialized operations using Update](perform-specialized-operations-using-update.md)  
  
 [IOrganizationService Entities](organization-service-entities.md)  
  
 [Sample: Execute Multiple Requests](sample-execute-multiple-requests.md)  
  
 [Sample: Execute multiple requests in transaction](sample-execute-multiple-requests-transaction.md)  
  
## <a name="related-sections"></a>Các phần liên quan  
 [Use the Early Bound Entity Classes in Code](use-early-bound-entity-classes-code.md)  
  
 [Use the Late Bound Entity Class in Code](use-late-bound-entity-class-code.md)  
  
 [Retrieve Data with Queries](retrieve-data-queries-sdk-assemblies.md)  
  
 [Developing Custom Code](../extend-dynamics-365-server.md)  
  
 [Connecting to the Dynamics 365 for Customer Engagement apps Services - Authentication](../authenticate-users.md)  
  
 [Discover the URL for your organization using the Organization Service](discover-url-organization-organization-service.md)  
  
 [Quick Start: A Simple Program](../simple-program-web-services.md)
