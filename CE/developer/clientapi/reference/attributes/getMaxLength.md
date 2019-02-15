---
title: getMaxLength (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 67a96fc4-4d65-4858-90da-f41eeba0365a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a671ba64d84891cc8d51eac9b5903105380a9b6a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386114"
---
# <a name="getmaxlength-client-api-reference"></a><span data-ttu-id="05f4d-102">getMaxLength (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="05f4d-102">getMaxLength (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="05f4d-103">Returns a number indicating the maximum length of a string or memo attribute.</span><span class="sxs-lookup"><span data-stu-id="05f4d-103">Returns a number indicating the maximum length of a string or memo attribute.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="05f4d-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="05f4d-104">Attribute types supported</span></span>

<span data-ttu-id="05f4d-105">string, memo</span><span class="sxs-lookup"><span data-stu-id="05f4d-105">string, memo</span></span>

## <a name="syntax"></a><span data-ttu-id="05f4d-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="05f4d-106">Syntax</span></span>

`formContext.getAttribute(arg).getMaxLength()`

## <a name="return-value"></a><span data-ttu-id="05f4d-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="05f4d-107">Return Value</span></span>

<span data-ttu-id="05f4d-108">**Type**: Number.</span><span class="sxs-lookup"><span data-stu-id="05f4d-108">**Type**: Number.</span></span> 

<span data-ttu-id="05f4d-109">**Description**: The maximum allowed length of a string for this attribute.</span><span class="sxs-lookup"><span data-stu-id="05f4d-109">**Description**: The maximum allowed length of a string for this attribute.</span></span>

> [!NOTE]
> <span data-ttu-id="05f4d-110">The email form description attribute is a memo attribute, but it does not have a `getMaxLength` method.</span><span class="sxs-lookup"><span data-stu-id="05f4d-110">The email form description attribute is a memo attribute, but it does not have a `getMaxLength` method.</span></span>
