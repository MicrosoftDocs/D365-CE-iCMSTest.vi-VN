---
title: Duplicate detection messages (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Use the BulkDetectDuplicatesRequest or RetrieveDuplicatesRequest messages to detect duplicates.
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
- duplicate detection messages
ms.assetid: f041dfd5-cfc4-44e2-b274-1107bdf75293
caps.latest.revision: 13
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fe358e4de054048152928fe007ea28a2cf86aa9f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386771"
---
# <a name="duplicate-detection-messages"></a>Duplicate detection messages

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

Use the messages listed in the following table to detect duplicates in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].  


|                                                                                                                                                                                                                   Thông báo                                                                                                                                                                                                                   |                                      Web API Operation                                       |                         SDK Assembly                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Detects duplicates for a specified entity type based on query criteria and store them as instances of a duplicate record entity type in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database.<br /><br /> The query expression that describes the records on which to run the duplicate detection job is specified in the <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest.Query> property of this request. | <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates Action" /> | <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest> |
|                                                                                                         Detects and retrieves duplicates for a specified record.<br /><br /> The matching entity type is specified in the <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest.MatchingEntityName> property of this request.                                                                                                          |  <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates Function" />  |  <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest>  |

### <a name="see-also"></a>Xem thêm  
 [Enable and disable duplicate detection](enable-disable-duplicate-detection.md)  
 [Running Duplicate Detection](run-duplicate-detection.md)   
 [Duplicate Rule entities](duplicaterule-entities.md)<br />
