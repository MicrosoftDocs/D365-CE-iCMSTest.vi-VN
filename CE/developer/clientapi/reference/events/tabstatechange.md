---
title: TabStateChange Event (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: f2927df67867952300e91c9eb2f98670c4d5f9dc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388295"
---
# <a name="tabstatechange-event-client-api-reference"></a><span data-ttu-id="b662b-102">TabStateChange Event (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b662b-102">TabStateChange Event (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b662b-103">This event occurs when the **DisplayState** of the tab changes due to user interaction or when the [setDisplayState](../formContext-ui-tabs/setDisplayState.md) method is applied in code.</span><span class="sxs-lookup"><span data-stu-id="b662b-103">This event occurs when the **DisplayState** of the tab changes due to user interaction or when the [setDisplayState](../formContext-ui-tabs/setDisplayState.md) method is applied in code.</span></span> 

<span data-ttu-id="b662b-104">Use this event when you want to change the **src** property of an IFRAME within the tab. If you set the IFrame.**src** property in the OnLoad event for an IFRAME within a collapsed tab, the value will be overwritten when the tab is expanded.</span><span class="sxs-lookup"><span data-stu-id="b662b-104">Use this event when you want to change the **src** property of an IFRAME within the tab. If you set the IFrame.**src** property in the OnLoad event for an IFRAME within a collapsed tab, the value will be overwritten when the tab is expanded.</span></span>

<span data-ttu-id="b662b-105">Use the [addTabStateChange](../formContext-ui-tabs/addTabStateChange.md) method to add event handlers for this event and the [removeTabStateChange](../formContext-ui-tabs/removeTabStateChange.md) method to remove them.</span><span class="sxs-lookup"><span data-stu-id="b662b-105">Use the [addTabStateChange](../formContext-ui-tabs/addTabStateChange.md) method to add event handlers for this event and the [removeTabStateChange](../formContext-ui-tabs/removeTabStateChange.md) method to remove them.</span></span>



