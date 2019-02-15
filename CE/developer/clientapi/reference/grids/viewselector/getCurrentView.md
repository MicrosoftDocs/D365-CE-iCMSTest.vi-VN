---
title: getCurrentView (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7a5e469eb586a39898afa6d1e6169682eeb0d877
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386398"
---
# <a name="getcurrentview-client-api-reference"></a><span data-ttu-id="6e2f9-102">getCurrentView (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="6e2f9-102">getCurrentView (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getCurrentView-description.md](./includes/getCurrentView-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="6e2f9-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="6e2f9-103">Grid types supported</span></span>

<span data-ttu-id="6e2f9-104">Read-only grid</span><span class="sxs-lookup"><span data-stu-id="6e2f9-104">Read-only grid</span></span>

## <a name="syntax"></a><span data-ttu-id="6e2f9-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6e2f9-105">Syntax</span></span>

`viewSelector.getCurrentView();`

## <a name="return-value"></a><span data-ttu-id="6e2f9-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="6e2f9-106">Return Value</span></span>

<span data-ttu-id="6e2f9-107">**Type**: Lookup object</span><span class="sxs-lookup"><span data-stu-id="6e2f9-107">**Type**: Lookup object</span></span>

<span data-ttu-id="6e2f9-108">**Description**: The Lookup object has the following attributes:</span><span class="sxs-lookup"><span data-stu-id="6e2f9-108">**Description**: The Lookup object has the following attributes:</span></span>

- <span data-ttu-id="6e2f9-109">**entityType**: Number.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-109">**entityType**: Number.</span></span> <span data-ttu-id="6e2f9-110">The object type code for the SavedQuery (1039) or UserQuery (4230) that represents the view the user can select.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-110">The object type code for the SavedQuery (1039) or UserQuery (4230) that represents the view the user can select.</span></span>
- <span data-ttu-id="6e2f9-111">**id**: String.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-111">**id**: String.</span></span> <span data-ttu-id="6e2f9-112">The Id for the view the user can select.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-112">The Id for the view the user can select.</span></span>
- <span data-ttu-id="6e2f9-113">**name**: String.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-113">**name**: String.</span></span> <span data-ttu-id="6e2f9-114">The name of the view the user can select.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-114">The name of the view the user can select.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e2f9-115">Chú thích</span><span class="sxs-lookup"><span data-stu-id="6e2f9-115">Remarks</span></span>

<span data-ttu-id="6e2f9-116">If the subgrid control is not configured to display the view selector, calling this method on the `viewSelector` object will throw an error.</span><span class="sxs-lookup"><span data-stu-id="6e2f9-116">If the subgrid control is not configured to display the view selector, calling this method on the `viewSelector` object will throw an error.</span></span>

<span data-ttu-id="6e2f9-117">To get the `viewSelector` object, see [ViewSelector](../viewselector.md).</span><span class="sxs-lookup"><span data-stu-id="6e2f9-117">To get the `viewSelector` object, see [ViewSelector](../viewselector.md).</span></span>



