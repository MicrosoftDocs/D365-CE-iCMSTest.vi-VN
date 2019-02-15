---
title: WebResource entity messages and methods (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about web resource that stores the data equivalent to files used in web development. Web resources are client-side components that provide custom user interface elements. The schema name for this entity is WebResource.
ms.custom: ''
ms.date: 12/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6472bf88-4948-49f3-9f53-a4ef13abb702
caps.latest.revision: 21
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c286aeef3a939de6c715a24d83638c54699317a6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388720"
---
# <a name="webresource-entity-messages-and-methods"></a>WebResource entity messages and methods

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

A *web resource* stores the data equivalent to files used in web development. Web resources are client-side components that provide custom user interface elements. These resources are stored in the [WebResource Entity](entities/webresource.md).  
  
 The following table describes the messages for this entity, which you use with the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Execute*> method.  
  
|Thông báo|Mô tả|  
|-------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest>|Creates a web resource. You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*> method.|  
|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest>|Deletes a web resource. You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*> method.|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest>|Retrieves a web resource. You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*> method.|  
|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>|Retrieves a collection of web resources. You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.|  
|<xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedRequest>|Retrieves the current saved definition of a web resource regardless whether it has been published.|  
|<xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedMultipleRequest>|Retrieves the current saved definition of web resources regardless whether they have been published.|  
|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest>|Updates a web resource. You can also call the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*> method.|  
  
### <a name="see-also"></a>Xem thêm

 [Web Resources for Dynamics 365 for Customer Engagement apps](web-resources.md)<br />
 [Sample: Pass Multiple Values to a  Web Resource Through the Data Parameter](sample-pass-multiple-values-web-resource-through-data-parameter.md)<br />
