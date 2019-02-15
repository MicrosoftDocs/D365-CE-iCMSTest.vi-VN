---
title: GridCell (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: d82ebf3bf0a705bcb684bea1ad07d2ee454f0d0f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386772"
---
# <a name="gridcell-client-api-reference"></a><span data-ttu-id="a5316-102">GridCell (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a5316-102">GridCell (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="a5316-103">GridCell is only supported for editable grids.</span><span class="sxs-lookup"><span data-stu-id="a5316-103">GridCell is only supported for editable grids.</span></span>

<span data-ttu-id="a5316-104">GridCell of a selected grid row is analogous to a control on a form that is tied to an attribute in an editable grid.</span><span class="sxs-lookup"><span data-stu-id="a5316-104">GridCell of a selected grid row is analogous to a control on a form that is tied to an attribute in an editable grid.</span></span> <span data-ttu-id="a5316-105">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span><span class="sxs-lookup"><span data-stu-id="a5316-105">See [Collections (Client API reference)](../collections.md) for information on the methods available to access data in a collection.</span></span>

## <a name="methods"></a><span data-ttu-id="a5316-106">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="a5316-106">Methods</span></span>

<span data-ttu-id="a5316-107">GridCell supports the following methods.</span><span class="sxs-lookup"><span data-stu-id="a5316-107">GridCell supports the following methods.</span></span>

|<span data-ttu-id="a5316-108">Tên</span><span class="sxs-lookup"><span data-stu-id="a5316-108">Name</span></span> |<span data-ttu-id="a5316-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a5316-109">Description</span></span> |
|--|--|
|[<span data-ttu-id="a5316-110">clearNotification</span><span class="sxs-lookup"><span data-stu-id="a5316-110">clearNotification</span></span>](../controls/clearNotification.md)| <span data-ttu-id="a5316-111">Clears notification for a cell.</span><span class="sxs-lookup"><span data-stu-id="a5316-111">Clears notification for a cell.</span></span>|
|[<span data-ttu-id="a5316-112">getDisabled</span><span class="sxs-lookup"><span data-stu-id="a5316-112">getDisabled</span></span>](../controls/getDisabled.md)| <span data-ttu-id="a5316-113">Returns whether the cell is disabled (read-only).</span><span class="sxs-lookup"><span data-stu-id="a5316-113">Returns whether the cell is disabled (read-only).</span></span>|
|[<span data-ttu-id="a5316-114">setDisabled</span><span class="sxs-lookup"><span data-stu-id="a5316-114">setDisabled</span></span>](../controls/setDisabled.md)| <span data-ttu-id="a5316-115">Sets whether the cell is disabled.</span><span class="sxs-lookup"><span data-stu-id="a5316-115">Sets whether the cell is disabled.</span></span><br/><br/><span data-ttu-id="a5316-116">**NOTE**: Enabling a read-only cell for editing can cause an error when the record is saved.</span><span class="sxs-lookup"><span data-stu-id="a5316-116">**NOTE**: Enabling a read-only cell for editing can cause an error when the record is saved.</span></span> <span data-ttu-id="a5316-117">If the field is considered read-only by the server, an error may occur if the value is modified.</span><span class="sxs-lookup"><span data-stu-id="a5316-117">If the field is considered read-only by the server, an error may occur if the value is modified.</span></span> <span data-ttu-id="a5316-118">This may happen in scenarios where the user doesn't have write privileges to the record, the record is disabled, or the user doesn't have the necessary field-level security privileges.</span><span class="sxs-lookup"><span data-stu-id="a5316-118">This may happen in scenarios where the user doesn't have write privileges to the record, the record is disabled, or the user doesn't have the necessary field-level security privileges.</span></span>| 
|[<span data-ttu-id="a5316-119">setNotification</span><span class="sxs-lookup"><span data-stu-id="a5316-119">setNotification</span></span>](../controls/setNotification.md)|<span data-ttu-id="a5316-120">Displays an error message for a cell to indicate that data isn’t valid.</span><span class="sxs-lookup"><span data-stu-id="a5316-120">Displays an error message for a cell to indicate that data isn’t valid.</span></span>|
|[<span data-ttu-id="a5316-121">getLabel</span><span class="sxs-lookup"><span data-stu-id="a5316-121">getLabel</span></span>](../controls/getLabel.md)|<span data-ttu-id="a5316-122">Returns the label of the column that contains the cell.</span><span class="sxs-lookup"><span data-stu-id="a5316-122">Returns the label of the column that contains the cell.</span></span>|


### <a name="related-topics"></a><span data-ttu-id="a5316-123">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a5316-123">Related topics</span></span>

[<span data-ttu-id="a5316-124">Grids and subgrids in Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a5316-124">Grids and subgrids in Customer Engagement</span></span>](../grids.md)

[<span data-ttu-id="a5316-125">Kiểm soát</span><span class="sxs-lookup"><span data-stu-id="a5316-125">Controls</span></span>](../controls.md)


