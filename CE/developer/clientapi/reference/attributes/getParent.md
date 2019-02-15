---
title: getParent (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6d77db1b-18b4-410f-b91b-d2b65b369946
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: dbbd7df380c002fdf2ab637401b8ea16ca54b575
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387011"
---
# <a name="getparent-client-api-reference"></a><span data-ttu-id="ac58d-102">getParent (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="ac58d-102">getParent (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ac58d-103">Returns the `formContext.data.entity` object that is the parent to all attributes.</span><span class="sxs-lookup"><span data-stu-id="ac58d-103">Returns the `formContext.data.entity` object that is the parent to all attributes.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="ac58d-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="ac58d-104">Attribute types supported</span></span>

<span data-ttu-id="ac58d-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="ac58d-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="ac58d-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="ac58d-106">Syntax</span></span>

`formContext.getAttribute(arg).getParent()`

## <a name="return-value"></a><span data-ttu-id="ac58d-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="ac58d-107">Return Value</span></span>

<span data-ttu-id="ac58d-108">**Type**: `formContext.data.entity` object.</span><span class="sxs-lookup"><span data-stu-id="ac58d-108">**Type**: `formContext.data.entity` object.</span></span> 

<span data-ttu-id="ac58d-109">**Description**: The parent object.</span><span class="sxs-lookup"><span data-stu-id="ac58d-109">**Description**: The parent object.</span></span>

