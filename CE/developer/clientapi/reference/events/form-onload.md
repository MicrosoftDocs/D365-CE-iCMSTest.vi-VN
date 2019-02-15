---
title: Form OnLoad Event (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
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
ms.openlocfilehash: b9af909cd4e06bb2776adc033c21f7e4f9771782
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387552"
---
# <a name="form-onload-event-client-api-reference"></a><span data-ttu-id="a6205-102">Form OnLoad Event (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a6205-102">Form OnLoad Event (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a6205-103">The form `OnLoad` event occurs after the form has loaded.</span><span class="sxs-lookup"><span data-stu-id="a6205-103">The form `OnLoad` event occurs after the form has loaded.</span></span> <span data-ttu-id="a6205-104">It cannot prevent the window from loading.</span><span class="sxs-lookup"><span data-stu-id="a6205-104">It cannot prevent the window from loading.</span></span> <span data-ttu-id="a6205-105">Use the `OnLoad` event to apply logic about how the form should be displayed, to set properties on fields, and interact with other page elements.</span><span class="sxs-lookup"><span data-stu-id="a6205-105">Use the `OnLoad` event to apply logic about how the form should be displayed, to set properties on fields, and interact with other page elements.</span></span>

<span data-ttu-id="a6205-106">When the Microsoft Dynamics 365 for tablets client is disconnected, the `OnLoad` event is the only event that will occur.</span><span class="sxs-lookup"><span data-stu-id="a6205-106">When the Microsoft Dynamics 365 for tablets client is disconnected, the `OnLoad` event is the only event that will occur.</span></span> 