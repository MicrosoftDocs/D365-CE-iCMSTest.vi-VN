---
title: formContext.data.entity (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 32e8d1d0-4093-4588-a517-2930eec34dce
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 652dcc4f0c4b6c19c026f3d045299660f82e603e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388617"
---
# <a name="formcontextdataentity-client-api-reference"></a><span data-ttu-id="759cb-102">formContext.data.entity (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="759cb-102">formContext.data.entity (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="759cb-103">Provides properties and methods to retrieve information specific to the record displayed on the page, the save method, and a collection of all the attributes included in the form.</span><span class="sxs-lookup"><span data-stu-id="759cb-103">Provides properties and methods to retrieve information specific to the record displayed on the page, the save method, and a collection of all the attributes included in the form.</span></span> <span data-ttu-id="759cb-104">Attribute data is limited to attributes represented by fields on the form.</span><span class="sxs-lookup"><span data-stu-id="759cb-104">Attribute data is limited to attributes represented by fields on the form.</span></span>

## <a name="properties"></a><span data-ttu-id="759cb-105">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="759cb-105">Properties</span></span>

|<span data-ttu-id="759cb-106">Tên</span><span class="sxs-lookup"><span data-stu-id="759cb-106">Name</span></span>|<span data-ttu-id="759cb-107">Mô tả</span><span class="sxs-lookup"><span data-stu-id="759cb-107">Description</span></span>|
|--|--|
|<span data-ttu-id="759cb-108">attributes</span><span class="sxs-lookup"><span data-stu-id="759cb-108">attributes</span></span>|<span data-ttu-id="759cb-109">Collection of attributes for a record displayed on the form.</span><span class="sxs-lookup"><span data-stu-id="759cb-109">Collection of attributes for a record displayed on the form.</span></span> <br/><span data-ttu-id="759cb-110">More information: [Collections](collections.md) and [Attributes](attributes.md).</span><span class="sxs-lookup"><span data-stu-id="759cb-110">More information: [Collections](collections.md) and [Attributes](attributes.md).</span></span>

## <a name="methods"></a><span data-ttu-id="759cb-111">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="759cb-111">Methods</span></span>

|                                      <span data-ttu-id="759cb-112">Tên</span><span class="sxs-lookup"><span data-stu-id="759cb-112">Name</span></span>                                       |                                                                          <span data-ttu-id="759cb-113">Mô tả</span><span class="sxs-lookup"><span data-stu-id="759cb-113">Description</span></span>                                                                           |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                [<span data-ttu-id="759cb-114">addOnSave</span><span class="sxs-lookup"><span data-stu-id="759cb-114">addOnSave</span></span>](formContext-data-entity/addOnSave.md)                |                [!INCLUDE[formContext-data-entity/includes/addOnSave-description.md](formContext-data-entity/includes/addOnSave-description.md)]                |
|               [<span data-ttu-id="759cb-115">getDataXml</span><span class="sxs-lookup"><span data-stu-id="759cb-115">getDataXml</span></span>](formContext-data-entity/getDataXml.md)               |               [!INCLUDE[formContext-data-entity/includes/getDataXml-description.md](formContext-data-entity/includes/getDataXml-description.md)]               |
|            [<span data-ttu-id="759cb-116">getEntityName</span><span class="sxs-lookup"><span data-stu-id="759cb-116">getEntityName</span></span>](formContext-data-entity/getEntityName.md)            |            [!INCLUDE[formContext-data-entity/includes/getEntityName-description.md](formContext-data-entity/includes/getEntityName-description.md)]            |
|       [<span data-ttu-id="759cb-117">getEntityReference</span><span class="sxs-lookup"><span data-stu-id="759cb-117">getEntityReference</span></span>](formContext-data-entity/getEntityReference.md)       |       [!INCLUDE[formContext-data-entity/includes/getEntityReference-description.md](formContext-data-entity/includes/getEntityReference-description.md)]       |
|                    [<span data-ttu-id="759cb-118">getId</span><span class="sxs-lookup"><span data-stu-id="759cb-118">getId</span></span>](formContext-data-entity/getId.md)                    |                    [!INCLUDE[formContext-data-entity/includes/getId-description.md](formContext-data-entity/includes/getId-description.md)]                    |
|               [<span data-ttu-id="759cb-119">getIsDirty</span><span class="sxs-lookup"><span data-stu-id="759cb-119">getIsDirty</span></span>](formContext-data-entity/getIsDirty.md)               |               [!INCLUDE[formContext-data-entity/includes/getIsDirty-description.md](formContext-data-entity/includes/getIsDirty-description.md)]               |
| [<span data-ttu-id="759cb-120">getPrimaryAttributeValue</span><span class="sxs-lookup"><span data-stu-id="759cb-120">getPrimaryAttributeValue</span></span>](formContext-data-entity/getPrimaryAttributeValue.md) | [!INCLUDE[formContext-data-entity/includes/getPrimaryAttributeValue-description.md](formContext-data-entity/includes/getPrimaryAttributeValue-description.md)] |
|                  [<span data-ttu-id="759cb-121">isValid</span><span class="sxs-lookup"><span data-stu-id="759cb-121">isValid</span></span>](formContext-data-entity/isValid.md)                  |                  [!INCLUDE[formContext-data-entity/includes/isValid-description.md](formContext-data-entity/includes/isValid-description.md)]                  |
|             [<span data-ttu-id="759cb-122">removeOnSave</span><span class="sxs-lookup"><span data-stu-id="759cb-122">removeOnSave</span></span>](formContext-data-entity/removeOnSave.md)             |             [!INCLUDE[formContext-data-entity/includes/removeOnSave-description.md](formContext-data-entity/includes/removeOnSave-description.md)]             |
|                     [<span data-ttu-id="759cb-123">save</span><span class="sxs-lookup"><span data-stu-id="759cb-123">save</span></span>](formContext-data-entity/save.md)                     |                     [!INCLUDE[formContext-data-entity/includes/save-description.md](formContext-data-entity/includes/save-description.md)]                     |

### <a name="related-topics"></a><span data-ttu-id="759cb-124">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="759cb-124">Related topics</span></span>

[<span data-ttu-id="759cb-125">Understand Xrm object model</span><span class="sxs-lookup"><span data-stu-id="759cb-125">Understand Xrm object model</span></span>](../understand-clientapi-object-model.md)

[<span data-ttu-id="759cb-126">Controls (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="759cb-126">Controls (Client API reference)</span></span>](controls.md)




