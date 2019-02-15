---
title: getIsPartyList (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 487d0923-9675-4308-b88e-fdbf91853a98
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f899aee0c52999dd99c70a7e7fbd6db28e71f57f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387668"
---
# <a name="getispartylist-client-api-reference"></a><span data-ttu-id="0f027-102">getIsPartyList (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="0f027-102">getIsPartyList (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0f027-103">Returns a Boolean value indicating whether the lookup represents a partylist lookup.</span><span class="sxs-lookup"><span data-stu-id="0f027-103">Returns a Boolean value indicating whether the lookup represents a partylist lookup.</span></span> <span data-ttu-id="0f027-104">Partylist lookups allow for multiple records to be set, such as the **To:** field for an email entity record.</span><span class="sxs-lookup"><span data-stu-id="0f027-104">Partylist lookups allow for multiple records to be set, such as the **To:** field for an email entity record.</span></span>

## <a name="attribute-types-supported"></a><span data-ttu-id="0f027-105">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="0f027-105">Attribute types supported</span></span>

<span data-ttu-id="0f027-106">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="0f027-106">Lookup</span></span>

## <a name="syntax"></a><span data-ttu-id="0f027-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="0f027-107">Syntax</span></span>

`formContext.getAttribute(arg).getIsPartyList()`

## <a name="return-value"></a><span data-ttu-id="0f027-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="0f027-108">Return Value</span></span>

<span data-ttu-id="0f027-109">**Type**: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0f027-109">**Type**: Boolean.</span></span> 

<span data-ttu-id="0f027-110">**Description**: True if the lookup attribute is a partylist, otherwise false.</span><span class="sxs-lookup"><span data-stu-id="0f027-110">**Description**: True if the lookup attribute is a partylist, otherwise false.</span></span>

