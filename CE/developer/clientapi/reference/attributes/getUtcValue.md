---
title: getUtcValue (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ebd1526e-d014-41a3-973d-75742b9cfbd3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5950a6dcdc180fdcc00330e5e8c79b3604ed0ef9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385859"
---
# <a name="getutcvalue-client-api-reference"></a><span data-ttu-id="91c05-102">getUtcValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="91c05-102">getUtcValue (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="91c05-103">Returns a UTC-equivalent date and time value of the value stored in a **datetime** type of attribute.</span><span class="sxs-lookup"><span data-stu-id="91c05-103">Returns a UTC-equivalent date and time value of the value stored in a **datetime** type of attribute.</span></span> <span data-ttu-id="91c05-104">UTC stands for Coordinated Universal Time.</span><span class="sxs-lookup"><span data-stu-id="91c05-104">UTC stands for Coordinated Universal Time.</span></span>

## <a name="attribute-types-supported"></a><span data-ttu-id="91c05-105">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="91c05-105">Attribute types supported</span></span>

<span data-ttu-id="91c05-106">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="91c05-106">datetime</span></span>

## <a name="syntax"></a><span data-ttu-id="91c05-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="91c05-107">Syntax</span></span>

`formContext.getAttribute(arg).getUtcValue()`

## <a name="return-value"></a><span data-ttu-id="91c05-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="91c05-108">Return Value</span></span>

<span data-ttu-id="91c05-109">**Type**: datetime.</span><span class="sxs-lookup"><span data-stu-id="91c05-109">**Type**: datetime.</span></span> 

<span data-ttu-id="91c05-110">**Description**: The UTC-equivalent date and time value of the value stored in an attribute.</span><span class="sxs-lookup"><span data-stu-id="91c05-110">**Description**: The UTC-equivalent date and time value of the value stored in an attribute.</span></span>


### <a name="related-topic"></a><span data-ttu-id="91c05-111">Related topic</span><span class="sxs-lookup"><span data-stu-id="91c05-111">Related topic</span></span>
[<span data-ttu-id="91c05-112">setUtcValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="91c05-112">setUtcValue (Client API reference)</span></span>](setUtcValue.md)

