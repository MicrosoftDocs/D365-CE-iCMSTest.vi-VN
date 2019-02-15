---
title: getEntityReference (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: b8e23eee-f20f-4db9-9cc6-7fa5dd7ce2bb
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: aa247d5e7eadaa7a6a627e260f916611e077f045
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387456"
---
# <a name="getentityreference-client-api-reference"></a><span data-ttu-id="99a38-102">getEntityReference (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="99a38-102">getEntityReference (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getEntityReference-description.md](./includes/getEntityReference-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="99a38-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="99a38-103">Grid types supported</span></span>

<span data-ttu-id="99a38-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="99a38-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="99a38-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="99a38-105">Syntax</span></span>

`gridEntity.getEntityReference();`

## <a name="return-value"></a><span data-ttu-id="99a38-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="99a38-106">Return Value</span></span>

<span data-ttu-id="99a38-107">**Type**: Lookup</span><span class="sxs-lookup"><span data-stu-id="99a38-107">**Type**: Lookup</span></span>

<span data-ttu-id="99a38-108">**Description**: Lookup object that references the record in the row.</span><span class="sxs-lookup"><span data-stu-id="99a38-108">**Description**: Lookup object that references the record in the row.</span></span> <span data-ttu-id="99a38-109">The object has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="99a38-109">The object has the following attributes:</span></span>
- <span data-ttu-id="99a38-110">**entityType**: String.</span><span class="sxs-lookup"><span data-stu-id="99a38-110">**entityType**: String.</span></span> <span data-ttu-id="99a38-111">The logical name for the record in the row.</span><span class="sxs-lookup"><span data-stu-id="99a38-111">The logical name for the record in the row.</span></span> <span data-ttu-id="99a38-112">The same data returned by the **GridEntity**.[getEntityName](getEntityName.md) method.</span><span class="sxs-lookup"><span data-stu-id="99a38-112">The same data returned by the **GridEntity**.[getEntityName](getEntityName.md) method.</span></span>
- <span data-ttu-id="99a38-113">**id**: String.</span><span class="sxs-lookup"><span data-stu-id="99a38-113">**id**: String.</span></span> <span data-ttu-id="99a38-114">The Id for the record in the row.</span><span class="sxs-lookup"><span data-stu-id="99a38-114">The Id for the record in the row.</span></span> <span data-ttu-id="99a38-115">The same data returned by the **GridEntity**.[getId](getId.md) method.</span><span class="sxs-lookup"><span data-stu-id="99a38-115">The same data returned by the **GridEntity**.[getId](getId.md) method.</span></span>
- <span data-ttu-id="99a38-116">**name**: String.</span><span class="sxs-lookup"><span data-stu-id="99a38-116">**name**: String.</span></span> <span data-ttu-id="99a38-117">The primary attribute value for the record in the row.</span><span class="sxs-lookup"><span data-stu-id="99a38-117">The primary attribute value for the record in the row.</span></span> <span data-ttu-id="99a38-118">The same data returned by the **GridEntity**.[getPrimaryAttributeValue](getPrimaryAttributeValue.md) method.</span><span class="sxs-lookup"><span data-stu-id="99a38-118">The same data returned by the **GridEntity**.[getPrimaryAttributeValue](getPrimaryAttributeValue.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="99a38-119">Chú thích</span><span class="sxs-lookup"><span data-stu-id="99a38-119">Remarks</span></span>

<span data-ttu-id="99a38-120">To get the `gridEntity` object, see [GridEntity](../gridentity.md).</span><span class="sxs-lookup"><span data-stu-id="99a38-120">To get the `gridEntity` object, see [GridEntity](../gridentity.md).</span></span> 

