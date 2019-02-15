---
title: 'Sample: Retrieve absolute URL and site collection URL of a location record | MicrosoftDocs'
description: ''
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f40b22d9-89fc-4b9f-a158-c7944c768d1b
author: KumarVivek
ms.author: kvivek
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 19
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 60cc12c6975cc064f24ba466b6c8644b092fad80
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388461"
---
# <a name="sample-retrieve-absolute-url-and-site-collection-url-of-a-location-record"></a>Sample: Retrieve absolute URL and site collection URL of a location record

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps. Download the sample: [Work with SharePoint Integration](https://code.msdn.microsoft.com/Samples-of-Sharepoint-b4fb016f).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
   
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to retrieve the absolute URL and the site collection URL of a [!INCLUDE[pn_SharePoint_Server_short](../../includes/pn-sharepoint-server-short.md)] location record in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps using the <xref:Microsoft.Crm.Sdk.Messages.RetrieveAbsoluteAndSiteCollectionUrlRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[SharePointIntegration#RetrieveAbsoluteAndSiteCollectionURLs](../../snippets/csharp/CRMV8/sharepointintegration/cs/retrieveabsoluteandsitecollectionurls.cs#retrieveabsoluteandsitecollectionurls)]  
  
### <a name="see-also"></a>Xem thêm  
 [Integrate SharePoint with Microsoft Dynamics 365 for Customer Engagement apps](integrate-sharepoint.md)   
 [Retrieve Absolute and Site Collection URLs for a Location Record](actions-on-sharepoint-location-records.md#RetrieveUrls)   
 [Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md)   
 [Sample: Create, Retrieve, Update, and Delete (CRUD) a SharePoint Location Record](sample-create-retrieve-update-delete-sharepoint-location-record.md)   
 <xref:Microsoft.Crm.Sdk.Messages.RetrieveAbsoluteAndSiteCollectionUrlRequest>
