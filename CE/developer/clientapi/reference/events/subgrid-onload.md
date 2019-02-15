---
title: Subgrid OnLoad Event (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0424c44e54d506ec46589305ad0a67ed73bc043b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386338"
---
# <a name="subgrid-onload-event-client-api-reference"></a><span data-ttu-id="a701a-102">Subgrid OnLoad Event (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a701a-102">Subgrid OnLoad Event (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a701a-103">This event occurs every time the subgrid refreshes.</span><span class="sxs-lookup"><span data-stu-id="a701a-103">This event occurs every time the subgrid refreshes.</span></span> <span data-ttu-id="a701a-104">This includes when users sort values in subgrid by clicking the column headings.</span><span class="sxs-lookup"><span data-stu-id="a701a-104">This includes when users sort values in subgrid by clicking the column headings.</span></span> 

<span data-ttu-id="a701a-105">Use the GridControl.addOnLoad and GridControl.removeOnLoad methods to manage event handlers, usually in the form Onload event.</span><span class="sxs-lookup"><span data-stu-id="a701a-105">Use the GridControl.addOnLoad and GridControl.removeOnLoad methods to manage event handlers, usually in the form Onload event.</span></span> 



