---
title: Form data OnLoad Event (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: fb13c0a1-0e00-4592-8e58-3c2412141fbd
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0c94297d691caf6d65c1bb09aeffddb32d16a813
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385632"
---
# <a name="form-data-onload-event-client-api-reference"></a><span data-ttu-id="5ff31-102">Form data OnLoad Event (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="5ff31-102">Form data OnLoad Event (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5ff31-103">This event occurs whenever form data is loaded, specifically:</span><span class="sxs-lookup"><span data-stu-id="5ff31-103">This event occurs whenever form data is loaded, specifically:</span></span>

- <span data-ttu-id="5ff31-104">On initial page load</span><span class="sxs-lookup"><span data-stu-id="5ff31-104">On initial page load</span></span>
- <span data-ttu-id="5ff31-105">When the page data is explicitly refreshed using formContext.data.[refresh](../formContext-data/refresh.md) method.</span><span class="sxs-lookup"><span data-stu-id="5ff31-105">When the page data is explicitly refreshed using formContext.data.[refresh](../formContext-data/refresh.md) method.</span></span>
- <span data-ttu-id="5ff31-106">When the data is refreshed on a page on saving a record, if there are any changes.</span><span class="sxs-lookup"><span data-stu-id="5ff31-106">When the data is refreshed on a page on saving a record, if there are any changes.</span></span>
 
<span data-ttu-id="5ff31-107">Use the formContext.data.[addOnLoad](../formContext-data/addOnLoad.md) and formContext.data.[removeOnLoad](../formContext-data/removeOnLoad.md) methods to manage event handlers for this event.</span><span class="sxs-lookup"><span data-stu-id="5ff31-107">Use the formContext.data.[addOnLoad](../formContext-data/addOnLoad.md) and formContext.data.[removeOnLoad](../formContext-data/removeOnLoad.md) methods to manage event handlers for this event.</span></span> 



