---
title: Publish customizations | MicrosoftDocs
description: Publishing customizations makes the Web application aware of changes to the data that affects the user interface.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- publish customizations
ms.assetid: 649ec32a-1ae1-4966-96fa-3543f4a05509
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fee26e9bf1ce8d5736ee4b7445173f95bcb782c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388751"
---
# <a name="publish-customizations"></a>Đăng tùy chỉnh

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

Publishing customizations makes the Web application aware of changes to the data that affects the user interface.  
  
<a name="BKMK_WhenToPublishCustomizations"></a>   
## <a name="when-to-publish-customizations"></a>When to publish customizations  
 Customizations are automatically published when new items are created or existing items are deleted.  
  
 You must publish changes after updating schema metadata or entities that affect the user interface. You can decide to wait and publish a set of related changes together.  
  
 Only published customizations are exported with a solution. You should always publish customizations before exporting a solution.  
  
 Khi bạn thực hiện tuỳ chỉnh mà sẽ xuất hiện trong [!INCLUDE[pn_moca_full](../../includes/pn-moca-full.md)], bạn nên luôn xuất bản tuỳ chỉnh của bạn rõ ràng để đảm bảo rằng mỗi mục được đồng bộ hoá với các ứng dụng [!INCLUDE[pn_moca_short](../../includes/pn-moca-short.md)].  
  
> [!NOTE]
>  Xuất bản tùy chỉnh có thể can thiệp đến hoạt động bình thường hệ thống. In a production environment, we recommend that you schedule publishing customizations when it’s least disruptive to users.  
  
## <a name="publishing-programmatically"></a>Publishing programmatically  
 The following table lists the two messages that you can use to publish customizations.  
  
|Thông báo|Mô tả|  
|-------------|-----------------|  
|<xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest>|Publishes all customizations.|  
|<xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest>|Publishes the specified customizations.|  
  
 When you use the `PublishXmlRequest` message, you specify which items you want to publish by using the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest.ParameterXml> parameter. `ParameterXML` must comply with the [Publish Request Schema](publish-request-schema.md).  
  
<a name="BKMK_RetrieveUnpublishedMetadata"></a>   
## <a name="retrieving-unpublished-metadata"></a>Retrieving unpublished metadata  
 If you want to create an application to edit customizable items in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, you must retrieve any unpublished definitions of those items. If a developer defines some changes but does not publish them, your application must be able to retrieve them to display them in the user interface.  
  
 Use the following two methods to retrieve unpublished metadata:  
  
 **RetrieveAsIfPublished parameter**  
 Retrieves entity, attribute, entity relationship, and option set data by using the following messages:  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllEntitiesRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAllOptionSetsRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveAttributeRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveEntityRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveOptionSetRequest>  
  
- <xref:Microsoft.Xrm.Sdk.Messages.RetrieveRelationshipRequest>  
  
  **RetrieveUnpublished Request**  
  Retrieves user interface items, such as form, template, visualization and Web resource definitions, by using the following messages:  
  
- <xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedRequest>  
  
- <xref:Microsoft.Crm.Sdk.Messages.RetrieveUnpublishedMultipleRequest>  
  
### <a name="see-also"></a>Xem thêm  
 [Customize Dynamics 365 for Customer Engagement](customize-applications.md)   
 [Extend the Metadata Model for Microsoft Dynamics 365 for Customer Engagement](../org-service/use-organization-service-metadata.md)   
 [Publish request schema](publish-request-schema.md)   
 [Customize Entity Forms in Microsoft Dynamics 365 for Customer Engagement](customize-entity-forms.md)   
 [Customize Entity Views in Microsoft Dynamics 365 for Customer Engagement](customize-entity-views.md)   
 [Customize Global Option Sets in Microsoft Dynamics 365 for Customer Engagement](../org-service/customize-global-option-sets.md)   
 [Change Application Navigation using the SiteMap](/developer/customize-dev/change-application-navigation-using-sitemap.md)   
 [Customize the Ribbon for Microsoft Dynamics 365 for Customer Engagement](customize-commands-ribbon.md)   
 [Open Forms, Views, and Dialogs with a URL](../open-forms-views-dialogs-reports-url.md)   
 [Client scripting in Customer Engagement using JavaScript](../clientapi/client-scripting.md)   
 [Web Resources for Microsoft Dynamics 365 for Customer Engagement](../web-resources.md)   
