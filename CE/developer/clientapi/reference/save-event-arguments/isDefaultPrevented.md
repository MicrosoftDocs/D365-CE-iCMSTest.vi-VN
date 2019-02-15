---
title: isDefaultPrevented (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9a8802ad-80aa-4386-a192-573280587546
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 06c0f34f4971ad95c31ff9c2377f499d6198003f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386728"
---
# <a name="isdefaultprevented-client-api-reference"></a><span data-ttu-id="b12c5-102">isDefaultPrevented (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="b12c5-102">isDefaultPrevented (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/isDefaultPrevented-description.md](./includes/isDefaultPrevented-description.md)]

## <a name="syntax"></a><span data-ttu-id="b12c5-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="b12c5-103">Syntax</span></span>

`executionContext.getEventArgs().isDefaultPrevented();`

## <a name="return-value"></a><span data-ttu-id="b12c5-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="b12c5-104">Return Value</span></span>

<span data-ttu-id="b12c5-105">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="b12c5-105">**Type**: Boolean</span></span>

<span data-ttu-id="b12c5-106">**Description**: **true** if the save event has been canceled because the preventDefault method was used; **false** otherwise.</span><span class="sxs-lookup"><span data-stu-id="b12c5-106">**Description**: **true** if the save event has been canceled because the preventDefault method was used; **false** otherwise.</span></span>


### <a name="related-topics"></a><span data-ttu-id="b12c5-107">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="b12c5-107">Related topics</span></span>

[<span data-ttu-id="b12c5-108">getSaveMode</span><span class="sxs-lookup"><span data-stu-id="b12c5-108">getSaveMode</span></span>](getSaveMode.md)

[<span data-ttu-id="b12c5-109">preventDefault</span><span class="sxs-lookup"><span data-stu-id="b12c5-109">preventDefault</span></span>](preventDefault.md)

