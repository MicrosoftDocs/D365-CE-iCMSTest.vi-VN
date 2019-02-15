---
title: getIsDirty (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5f75ecae-a946-47a0-b748-96525b556f31
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7152fd5cd6f0e792d5df1f30ed1d6ff5c7535979
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386739"
---
# <a name="getisdirty-client-api-reference"></a><span data-ttu-id="7494e-102">getIsDirty (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="7494e-102">getIsDirty (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7494e-103">Returns a Boolean value indicating if there are unsaved changes to the attribute value.</span><span class="sxs-lookup"><span data-stu-id="7494e-103">Returns a Boolean value indicating if there are unsaved changes to the attribute value.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="7494e-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="7494e-104">Attribute types supported</span></span>

<span data-ttu-id="7494e-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="7494e-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="7494e-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="7494e-106">Syntax</span></span>

`formContext.getAttribute(arg).getIsDirty()`

## <a name="return-value"></a><span data-ttu-id="7494e-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="7494e-107">Return Value</span></span>

<span data-ttu-id="7494e-108">**Type**: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7494e-108">**Type**: Boolean.</span></span> 

<span data-ttu-id="7494e-109">**Description**: True if there are unsaved changes, otherwise false.</span><span class="sxs-lookup"><span data-stu-id="7494e-109">**Description**: True if there are unsaved changes, otherwise false.</span></span>