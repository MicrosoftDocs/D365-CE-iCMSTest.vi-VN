---
title: GridRowData (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 8139c622-e4d9-478f-9510-414d140e5556
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c038f8199f4ec6aac3da12f49ac9b5790d315668
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386659"
---
# <a name="gridrowdata-client-api-reference"></a><span data-ttu-id="ea904-102">GridRowData (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="ea904-102">GridRowData (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ea904-103">GridRowData is returned by the [GridRow](gridrow.md).[getData](gridrow/getData.md) method.</span><span class="sxs-lookup"><span data-stu-id="ea904-103">GridRowData is returned by the [GridRow](gridrow.md).[getData](gridrow/getData.md) method.</span></span>

<span data-ttu-id="ea904-104">GridRowData also provides methods for retrieving information specific to a record displayed in an editable grid row, including a collection of all the attributes included in the row.</span><span class="sxs-lookup"><span data-stu-id="ea904-104">GridRowData also provides methods for retrieving information specific to a record displayed in an editable grid row, including a collection of all the attributes included in the row.</span></span> <span data-ttu-id="ea904-105">Attribute data is limited to the columns presented by the editable grid.</span><span class="sxs-lookup"><span data-stu-id="ea904-105">Attribute data is limited to the columns presented by the editable grid.</span></span> <span data-ttu-id="ea904-106">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="ea904-106">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span></span>

```JavaScript
var myRows = gridContext.getGrid().getRows();
var myRow = myRows.get(arg);
var gridRowData = myRow.getData();
```

## <a name="properties"></a><span data-ttu-id="ea904-107">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="ea904-107">Properties</span></span>

|<span data-ttu-id="ea904-108">Tên</span><span class="sxs-lookup"><span data-stu-id="ea904-108">Name</span></span>|<span data-ttu-id="ea904-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ea904-109">Description</span></span>|<span data-ttu-id="ea904-110">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="ea904-110">Available for</span></span>|
|--|--|--|
|<span data-ttu-id="ea904-111">thực thể</span><span class="sxs-lookup"><span data-stu-id="ea904-111">entity</span></span>|<span data-ttu-id="ea904-112">Returns the [GridEntity](gridentity.md) for the GridRowData.</span><span class="sxs-lookup"><span data-stu-id="ea904-112">Returns the [GridEntity](gridentity.md) for the GridRowData.</span></span>|<span data-ttu-id="ea904-113">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="ea904-113">Read-only and editable grids</span></span>|


## <a name="methods"></a><span data-ttu-id="ea904-114">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="ea904-114">Methods</span></span>

|                 <span data-ttu-id="ea904-115">Tên</span><span class="sxs-lookup"><span data-stu-id="ea904-115">Name</span></span>                  |                                               <span data-ttu-id="ea904-116">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ea904-116">Description</span></span>                                                |        <span data-ttu-id="ea904-117">Có sẵn cho</span><span class="sxs-lookup"><span data-stu-id="ea904-117">Available for</span></span>         |
|---------------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------|
| [<span data-ttu-id="ea904-118">getEntity</span><span class="sxs-lookup"><span data-stu-id="ea904-118">getEntity</span></span>](gridrowdata/getEntity.md) | [!INCLUDE[gridrowdata/includes/getEntity-description.md](gridrowdata/includes/getEntity-description.md)] | <span data-ttu-id="ea904-119">Read-only and editable grids</span><span class="sxs-lookup"><span data-stu-id="ea904-119">Read-only and editable grids</span></span> |

