---
title: getRelationship (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: be233583a9e932b37e1dd769895093ecf928b8e4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388136"
---
# <a name="getrelationship-client-api-reference"></a><span data-ttu-id="5dcac-102">getRelationship (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="5dcac-102">getRelationship (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getRelationship-description.md](./includes/getRelationship-description.md)]

## <a name="grid-types-supported"></a><span data-ttu-id="5dcac-103">Grid types supported</span><span class="sxs-lookup"><span data-stu-id="5dcac-103">Grid types supported</span></span>

<span data-ttu-id="5dcac-104">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="5dcac-104">Read-only and editable grids</span></span>

## <a name="syntax"></a><span data-ttu-id="5dcac-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="5dcac-105">Syntax</span></span>

`gridContext.getRelationship();`

## <a name="return-value"></a><span data-ttu-id="5dcac-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="5dcac-106">Return Value</span></span>

<span data-ttu-id="5dcac-107">**Type**: Object.</span><span class="sxs-lookup"><span data-stu-id="5dcac-107">**Type**: Object.</span></span>

<span data-ttu-id="5dcac-108">**Description**: A relationship object with the following attributes:</span><span class="sxs-lookup"><span data-stu-id="5dcac-108">**Description**: A relationship object with the following attributes:</span></span>
- <span data-ttu-id="5dcac-109">**attributeName**: String.</span><span class="sxs-lookup"><span data-stu-id="5dcac-109">**attributeName**: String.</span></span> <span data-ttu-id="5dcac-110">Name of the attribute.</span><span class="sxs-lookup"><span data-stu-id="5dcac-110">Name of the attribute.</span></span>
- <span data-ttu-id="5dcac-111">**name**: String.</span><span class="sxs-lookup"><span data-stu-id="5dcac-111">**name**: String.</span></span> <span data-ttu-id="5dcac-112">Name of the relationship.</span><span class="sxs-lookup"><span data-stu-id="5dcac-112">Name of the relationship.</span></span> 
- <span data-ttu-id="5dcac-113">**navigationPropertyName**: String.</span><span class="sxs-lookup"><span data-stu-id="5dcac-113">**navigationPropertyName**: String.</span></span> <span data-ttu-id="5dcac-114">Name of the navigation property for this relationship.</span><span class="sxs-lookup"><span data-stu-id="5dcac-114">Name of the navigation property for this relationship.</span></span>
- <span data-ttu-id="5dcac-115">**relationshipType**: Number.</span><span class="sxs-lookup"><span data-stu-id="5dcac-115">**relationshipType**: Number.</span></span> <span data-ttu-id="5dcac-116">Returns one of the following values to indicate the relationship type:</span><span class="sxs-lookup"><span data-stu-id="5dcac-116">Returns one of the following values to indicate the relationship type:</span></span>
    - <span data-ttu-id="5dcac-117">0: OneToMany</span><span class="sxs-lookup"><span data-stu-id="5dcac-117">0: OneToMany</span></span>
    - <span data-ttu-id="5dcac-118">1: ManyToMany</span><span class="sxs-lookup"><span data-stu-id="5dcac-118">1: ManyToMany</span></span>
- <span data-ttu-id="5dcac-119">**roleType**: Number.</span><span class="sxs-lookup"><span data-stu-id="5dcac-119">**roleType**: Number.</span></span> <span data-ttu-id="5dcac-120">Returns one of the following values to indicate the role type of relationship:</span><span class="sxs-lookup"><span data-stu-id="5dcac-120">Returns one of the following values to indicate the role type of relationship:</span></span>
    - <span data-ttu-id="5dcac-121">1: Referencing</span><span class="sxs-lookup"><span data-stu-id="5dcac-121">1: Referencing</span></span>
    - <span data-ttu-id="5dcac-122">2: AssociationEntity</span><span class="sxs-lookup"><span data-stu-id="5dcac-122">2: AssociationEntity</span></span>

## <a name="remarks"></a><span data-ttu-id="5dcac-123">Chú thích</span><span class="sxs-lookup"><span data-stu-id="5dcac-123">Remarks</span></span>

<span data-ttu-id="5dcac-124">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span><span class="sxs-lookup"><span data-stu-id="5dcac-124">To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).</span></span>

### <a name="related-topics"></a><span data-ttu-id="5dcac-125">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="5dcac-125">Related topics</span></span>

[<span data-ttu-id="5dcac-126">openRelatedGrid</span><span class="sxs-lookup"><span data-stu-id="5dcac-126">openRelatedGrid</span></span>](openRelatedGrid.md)

[<span data-ttu-id="5dcac-127">Customize entity relationship metadata</span><span class="sxs-lookup"><span data-stu-id="5dcac-127">Customize entity relationship metadata</span></span>](../../../../customize-entity-relationship-metadata.md)


