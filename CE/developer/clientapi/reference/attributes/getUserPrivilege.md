---
title: getUserPrivilege (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0a3f0349-af9a-418a-b99d-5085999884eb
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c982d8f4386d2188fc5c61b574f3199371666b0e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387755"
---
# <a name="getuserprivilege-client-api-reference"></a><span data-ttu-id="0c6f4-102">getUserPrivilege (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="0c6f4-102">getUserPrivilege (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0c6f4-103">Returns an object with three Boolean properties corresponding to privileges indicating if the user can create, read or update data values for an attribute.</span><span class="sxs-lookup"><span data-stu-id="0c6f4-103">Returns an object with three Boolean properties corresponding to privileges indicating if the user can create, read or update data values for an attribute.</span></span> <span data-ttu-id="0c6f4-104">This function is intended for use when Field Level Security modifies a user’s privileges for a particular attribute</span><span class="sxs-lookup"><span data-stu-id="0c6f4-104">This function is intended for use when Field Level Security modifies a user’s privileges for a particular attribute</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="0c6f4-105">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="0c6f4-105">Attribute types supported</span></span>

<span data-ttu-id="0c6f4-106">Tất cả</span><span class="sxs-lookup"><span data-stu-id="0c6f4-106">All</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6f4-107">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="0c6f4-107">Syntax</span></span>

`formContext.getAttribute(arg).getUserPrivilege()`

## <a name="return-value"></a><span data-ttu-id="0c6f4-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="0c6f4-108">Return Value</span></span>

<span data-ttu-id="0c6f4-109">**Type**: Object.</span><span class="sxs-lookup"><span data-stu-id="0c6f4-109">**Type**: Object.</span></span> 

<span data-ttu-id="0c6f4-110">**Description**: The object has three Boolean properties:</span><span class="sxs-lookup"><span data-stu-id="0c6f4-110">**Description**: The object has three Boolean properties:</span></span>
- <span data-ttu-id="0c6f4-111">canRead</span><span class="sxs-lookup"><span data-stu-id="0c6f4-111">canRead</span></span>
- <span data-ttu-id="0c6f4-112">canUpdate</span><span class="sxs-lookup"><span data-stu-id="0c6f4-112">canUpdate</span></span>
- <span data-ttu-id="0c6f4-113">canCreate</span><span class="sxs-lookup"><span data-stu-id="0c6f4-113">canCreate</span></span>

