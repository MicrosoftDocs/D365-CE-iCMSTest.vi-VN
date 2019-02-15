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
# <a name="duplicate-detection-messages"></a><span data-ttu-id="631f0-103">Duplicate detection messages</span><span class="sxs-lookup"><span data-stu-id="631f0-103">Duplicate detection messages</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="631f0-104">Use the messages listed in the following table to detect duplicates in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="631f0-104">Use the messages listed in the following table to detect duplicates in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span></span>  


|                                                                                                                                                                                                                   <span data-ttu-id="631f0-105">Thông báo</span><span class="sxs-lookup"><span data-stu-id="631f0-105">Message</span></span>                                                                                                                                                                                                                   |                                      <span data-ttu-id="631f0-106">Web API Operation</span><span class="sxs-lookup"><span data-stu-id="631f0-106">Web API Operation</span></span>                                       |                         <span data-ttu-id="631f0-107">SDK Assembly</span><span class="sxs-lookup"><span data-stu-id="631f0-107">SDK Assembly</span></span>                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="631f0-108">Detects duplicates for a specified entity type based on query criteria and store them as instances of a duplicate record entity type in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database.</span><span class="sxs-lookup"><span data-stu-id="631f0-108">Detects duplicates for a specified entity type based on query criteria and store them as instances of a duplicate record entity type in the [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] database.</span></span><br /><br /> <span data-ttu-id="631f0-109">The query expression that describes the records on which to run the duplicate detection job is specified in the <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest.Query> property of this request.</span><span class="sxs-lookup"><span data-stu-id="631f0-109">The query expression that describes the records on which to run the duplicate detection job is specified in the <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest.Query> property of this request.</span></span> | <xref href="Microsoft.Dynamics.CRM.BulkDetectDuplicates?text=BulkDetectDuplicates Action" /> | <xref:Microsoft.Crm.Sdk.Messages.BulkDetectDuplicatesRequest> |
|                                                                                                         <span data-ttu-id="631f0-110">Detects and retrieves duplicates for a specified record.</span><span class="sxs-lookup"><span data-stu-id="631f0-110">Detects and retrieves duplicates for a specified record.</span></span><br /><br /> <span data-ttu-id="631f0-111">The matching entity type is specified in the <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest.MatchingEntityName> property of this request.</span><span class="sxs-lookup"><span data-stu-id="631f0-111">The matching entity type is specified in the <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest.MatchingEntityName> property of this request.</span></span>                                                                                                          |  <xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates Function" />  |  <xref:Microsoft.Crm.Sdk.Messages.RetrieveDuplicatesRequest>  |

### <a name="see-also"></a><span data-ttu-id="631f0-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="631f0-112">See also</span></span>  
 [<span data-ttu-id="631f0-113">Enable and disable duplicate detection</span><span class="sxs-lookup"><span data-stu-id="631f0-113">Enable and disable duplicate detection</span></span>](enable-disable-duplicate-detection.md)  
 <span data-ttu-id="631f0-114">[Running Duplicate Detection](run-duplicate-detection.md) </span><span class="sxs-lookup"><span data-stu-id="631f0-114">[Running Duplicate Detection](run-duplicate-detection.md) </span></span>  
 [<span data-ttu-id="631f0-115">Duplicate Rule entities</span><span class="sxs-lookup"><span data-stu-id="631f0-115">Duplicate Rule entities</span></span>](duplicaterule-entities.md)<br />
