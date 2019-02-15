---
title: getEventSource (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about the getEventSource method that returns a reference to the object that the event occurred on.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9f3b2fed-fde5-46e4-8c59-43aa51aa82df
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 112019dc2f4b0686cbd621b0166c213f65e209cc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388618"
---
# <a name="geteventsource-client-api-reference"></a><span data-ttu-id="449e5-103">getEventSource (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="449e5-103">getEventSource (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="449e5-104">Returns a reference to the object that the event occurred on.</span><span class="sxs-lookup"><span data-stu-id="449e5-104">Returns a reference to the object that the event occurred on.</span></span>

## <a name="syntax"></a><span data-ttu-id="449e5-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="449e5-105">Syntax</span></span>

`ExecutionContextObj.getEventSource()`

## <a name="return-value"></a><span data-ttu-id="449e5-106">Return value</span><span class="sxs-lookup"><span data-stu-id="449e5-106">Return value</span></span>

<span data-ttu-id="449e5-107">**Type**: Object</span><span class="sxs-lookup"><span data-stu-id="449e5-107">**Type**: Object</span></span>

<span data-ttu-id="449e5-108">**Description**: Returns the object from the **Xrm** object model that is the source of the event, not an HTML DOM object.</span><span class="sxs-lookup"><span data-stu-id="449e5-108">**Description**: Returns the object from the **Xrm** object model that is the source of the event, not an HTML DOM object.</span></span> <span data-ttu-id="449e5-109">For example, in an [OnChange](../events/attribute-onchange.md) event, this method returns the **formContext.data.entity** attribute object that represents the changed attribute.</span><span class="sxs-lookup"><span data-stu-id="449e5-109">For example, in an [OnChange](../events/attribute-onchange.md) event, this method returns the **formContext.data.entity** attribute object that represents the changed attribute.</span></span>


### <a name="related-topics"></a><span data-ttu-id="449e5-110">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="449e5-110">Related topics</span></span>
[<span data-ttu-id="449e5-111">Execution context</span><span class="sxs-lookup"><span data-stu-id="449e5-111">Execution context</span></span>](../execution-context.md)





