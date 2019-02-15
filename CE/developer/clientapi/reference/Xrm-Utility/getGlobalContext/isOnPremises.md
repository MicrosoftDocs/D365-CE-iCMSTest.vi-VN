---
title: isOnPremise (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 855767c5-c48f-47a2-8f99-52423221d974
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c0ec37b0ef8edb01f578e8e11db60be5e9c08b32
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387107"
---
# <a name="isonpremise-client-api-reference"></a><span data-ttu-id="06933-102">isOnPremise (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="06933-102">isOnPremise (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="06933-103">Returns a boolean value indicating if the Customer Engagement instance is hosted on-premises or online.</span><span class="sxs-lookup"><span data-stu-id="06933-103">Returns a boolean value indicating if the Customer Engagement instance is hosted on-premises or online.</span></span> 

## <a name="syntax"></a><span data-ttu-id="06933-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="06933-104">Syntax</span></span>

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.isOnPremises();
```

## <a name="return-value"></a><span data-ttu-id="06933-105">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="06933-105">Return Value</span></span>

<span data-ttu-id="06933-106">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="06933-106">**Type**: Boolean</span></span>

<span data-ttu-id="06933-107">**Description**: **true** if the Customer Engagement instance is on-premises; **false** otherwise.</span><span class="sxs-lookup"><span data-stu-id="06933-107">**Description**: **true** if the Customer Engagement instance is on-premises; **false** otherwise.</span></span>

### <a name="related-topics"></a><span data-ttu-id="06933-108">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="06933-108">Related topics</span></span>

[<span data-ttu-id="06933-109">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="06933-109">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)



