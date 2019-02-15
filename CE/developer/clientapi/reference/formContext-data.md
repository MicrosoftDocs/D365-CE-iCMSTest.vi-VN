---
title: formContext.data (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with data on the form using client API.
ms.date: 08/08/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 32e8d1d0-4093-4588-a517-2930eec34dce
author: KumarVivek
ms.author: kvivek
manager: annbe
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a0b714bfce91a643940fc2abb85b411ebb7700ce
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387325"
---
# <a name="formcontextdata-client-api-reference"></a><span data-ttu-id="53466-103">formContext.data (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="53466-103">formContext.data (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="53466-104">Provides properties and methods to work with the data on a form.</span><span class="sxs-lookup"><span data-stu-id="53466-104">Provides properties and methods to work with the data on a form.</span></span>

![formContext Data object model](../../media/ClientAPI-formContext-data-Model.png)

## <a name="properties"></a><span data-ttu-id="53466-106">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="53466-106">Properties</span></span>

|<span data-ttu-id="53466-107">Tên</span><span class="sxs-lookup"><span data-stu-id="53466-107">Name</span></span>|<span data-ttu-id="53466-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="53466-108">Description</span></span>|
|--|--|
|<span data-ttu-id="53466-109">attributes</span><span class="sxs-lookup"><span data-stu-id="53466-109">attributes</span></span>|<span data-ttu-id="53466-110">Collection of non-entity data on the form.</span><span class="sxs-lookup"><span data-stu-id="53466-110">Collection of non-entity data on the form.</span></span> <span data-ttu-id="53466-111">Items in this collection are of the same type as the attributes collection, but they are not attributes of the form entity.</span><span class="sxs-lookup"><span data-stu-id="53466-111">Items in this collection are of the same type as the attributes collection, but they are not attributes of the form entity.</span></span> <br/><span data-ttu-id="53466-112">More information: [Collections](collections.md)</span><span class="sxs-lookup"><span data-stu-id="53466-112">More information: [Collections](collections.md)</span></span><br/><span data-ttu-id="53466-113">**NOTE:** This is supported only for [Unified Interface](../../../admin/about-unified-interface.md) clients.</span><span class="sxs-lookup"><span data-stu-id="53466-113">**NOTE:** This is supported only for [Unified Interface](../../../admin/about-unified-interface.md) clients.</span></span>|
|<span data-ttu-id="53466-114">thực thể</span><span class="sxs-lookup"><span data-stu-id="53466-114">entity</span></span>|<span data-ttu-id="53466-115">Provides methods to retrieve information specific to the record displayed on the page, the save method, and a collection of all the attributes included on the form.</span><span class="sxs-lookup"><span data-stu-id="53466-115">Provides methods to retrieve information specific to the record displayed on the page, the save method, and a collection of all the attributes included on the form.</span></span> <span data-ttu-id="53466-116">Attribute data is limited to attributes represented by fields on the form.</span><span class="sxs-lookup"><span data-stu-id="53466-116">Attribute data is limited to attributes represented by fields on the form.</span></span> <br/><span data-ttu-id="53466-117">More information: [formContext.data.entity](formContext-data-entity.md)</span><span class="sxs-lookup"><span data-stu-id="53466-117">More information: [formContext.data.entity](formContext-data-entity.md)</span></span>|
|<span data-ttu-id="53466-118">process</span><span class="sxs-lookup"><span data-stu-id="53466-118">process</span></span>|<span data-ttu-id="53466-119">Provides objects and methods to interact with the business process flow data on a form.</span><span class="sxs-lookup"><span data-stu-id="53466-119">Provides objects and methods to interact with the business process flow data on a form.</span></span><br/><span data-ttu-id="53466-120">More information: [formContext.data.process](formContext-data-process.md)</span><span class="sxs-lookup"><span data-stu-id="53466-120">More information: [formContext.data.process](formContext-data-process.md)</span></span>|


## <a name="methods"></a><span data-ttu-id="53466-121">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="53466-121">Methods</span></span> 

|                       <span data-ttu-id="53466-122">Tên</span><span class="sxs-lookup"><span data-stu-id="53466-122">Name</span></span>                       |                                                       <span data-ttu-id="53466-123">Mô tả</span><span class="sxs-lookup"><span data-stu-id="53466-123">Description</span></span>                                                        |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
|    [<span data-ttu-id="53466-124">addOnLoad</span><span class="sxs-lookup"><span data-stu-id="53466-124">addOnLoad</span></span>](formContext-data/addOnload.md)    |    [!INCLUDE[formContext-data/includes/addOnLoad-description.md](formContext-data/includes/addOnLoad-description.md)]    |
|   [<span data-ttu-id="53466-125">getIsDirty</span><span class="sxs-lookup"><span data-stu-id="53466-125">getIsDirty</span></span>](formContext-data/getIsDirty.md)   |   [!INCLUDE[formContext-data/includes/getIsDirty-description.md](formContext-data/includes/getIsDirty-description.md)]   |
|      [<span data-ttu-id="53466-126">isValid</span><span class="sxs-lookup"><span data-stu-id="53466-126">isValid</span></span>](formContext-data/isValid.md)      |      [!INCLUDE[formContext-data/includes/isValid-description.md](formContext-data/includes/isValid-description.md)]      |
|      [<span data-ttu-id="53466-127">refresh</span><span class="sxs-lookup"><span data-stu-id="53466-127">refresh</span></span>](formContext-data/refresh.md)      |      [!INCLUDE[formContext-data/includes/refresh-description.md](formContext-data/includes/refresh-description.md)]      |
| [<span data-ttu-id="53466-128">removeOnLoad</span><span class="sxs-lookup"><span data-stu-id="53466-128">removeOnLoad</span></span>](formContext-data/removeOnLoad.md) | [!INCLUDE[formContext-data/includes/removeOnLoad-description.md](formContext-data/includes/removeOnLoad-description.md)] |
|         [<span data-ttu-id="53466-129">save</span><span class="sxs-lookup"><span data-stu-id="53466-129">save</span></span>](formContext-data/save.md)         |         [!INCLUDE[formContext-data/includes/save-description.md](formContext-data/includes/save-description.md)]         |

### <a name="related-topics"></a><span data-ttu-id="53466-130">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="53466-130">Related topics</span></span>

[<span data-ttu-id="53466-131">formContext.data.entity</span><span class="sxs-lookup"><span data-stu-id="53466-131">formContext.data.entity</span></span>](formContext-data-entity.md)

[<span data-ttu-id="53466-132">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="53466-132">formContext.data.process</span></span>](formContext-data-process.md)




