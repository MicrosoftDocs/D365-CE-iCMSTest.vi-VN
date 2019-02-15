---
title: getShowTime (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 43341b96-ca2c-4c7e-b6d5-fe7a5fd3c8b2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2765f2391e25a5735a5ccd9b276e9122adfc6146
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385521"
---
# <a name="getshowtime-client-api-reference"></a><span data-ttu-id="19fa3-102">getShowTime (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="19fa3-102">getShowTime (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="19fa3-103">Get whether a date control shows the time portion of the date.</span><span class="sxs-lookup"><span data-stu-id="19fa3-103">Get whether a date control shows the time portion of the date.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="19fa3-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="19fa3-104">Control types supported</span></span>

<span data-ttu-id="19fa3-105">standard control for **datetime** attributes.</span><span class="sxs-lookup"><span data-stu-id="19fa3-105">standard control for **datetime** attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="19fa3-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="19fa3-106">Syntax</span></span>

`formContext.getControl(arg).getShowTime();`

## <a name="return-value"></a><span data-ttu-id="19fa3-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="19fa3-107">Return Value</span></span>

<span data-ttu-id="19fa3-108">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="19fa3-108">**Type**: Boolean</span></span>

<span data-ttu-id="19fa3-109">**Description**: true if shows the time portion of the date; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="19fa3-109">**Description**: true if shows the time portion of the date; false otherwise.</span></span>

### <a name="related-topics"></a><span data-ttu-id="19fa3-110">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="19fa3-110">Related topics</span></span>

[<span data-ttu-id="19fa3-111">setShowTime</span><span class="sxs-lookup"><span data-stu-id="19fa3-111">setShowTime</span></span>](setShowTime.md)

