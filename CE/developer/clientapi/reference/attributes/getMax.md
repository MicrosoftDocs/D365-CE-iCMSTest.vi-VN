---
title: getMax (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6bcd4b47-b3b6-4a9c-899f-a5dce4cbab51
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1cd7ca2a9c9874b9a15fe0869f4f8f566f3f2542
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388811"
---
# <a name="getmax-client-api-reference"></a><span data-ttu-id="6ec0c-102">getMax (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="6ec0c-102">getMax (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6ec0c-103">Returns a number indicating the maximum allowed value for an attribute.</span><span class="sxs-lookup"><span data-stu-id="6ec0c-103">Returns a number indicating the maximum allowed value for an attribute.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="6ec0c-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="6ec0c-104">Attribute types supported</span></span>

<span data-ttu-id="6ec0c-105">decimal, integer, double, money</span><span class="sxs-lookup"><span data-stu-id="6ec0c-105">decimal, integer, double, money</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec0c-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6ec0c-106">Syntax</span></span>

`formContext.getAttribute(arg).getMax()`

## <a name="return-value"></a><span data-ttu-id="6ec0c-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="6ec0c-107">Return Value</span></span>

<span data-ttu-id="6ec0c-108">**Type**: Number.</span><span class="sxs-lookup"><span data-stu-id="6ec0c-108">**Type**: Number.</span></span> 

<span data-ttu-id="6ec0c-109">**Description**: The maximum allowed value for the attribute.</span><span class="sxs-lookup"><span data-stu-id="6ec0c-109">**Description**: The maximum allowed value for the attribute.</span></span>

