---
title: addOnLoad (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/03/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 31a146de-9e25-43be-ae3e-83a2a5c86543
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0d083f2f5b94e8b8a1d59c3568b93ce3b19849d5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386463"
---
# <a name="addonload-client-api-reference"></a><span data-ttu-id="e502e-102">addOnLoad (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e502e-102">addOnLoad (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnLoad-description.md](./includes/addOnLoad-description.md)]

> [!NOTE]
> <span data-ttu-id="e502e-103">This method is supported only on Unified Interface.</span><span class="sxs-lookup"><span data-stu-id="e502e-103">This method is supported only on Unified Interface.</span></span>


## <a name="syntax"></a><span data-ttu-id="e502e-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e502e-104">Syntax</span></span>

`formContext.ui.addOnLoad(myFunction)`

## <a name="parameter"></a><span data-ttu-id="e502e-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="e502e-105">Parameter</span></span>

|<span data-ttu-id="e502e-106">Tên</span><span class="sxs-lookup"><span data-stu-id="e502e-106">Name</span></span>|<span data-ttu-id="e502e-107">Loại</span><span class="sxs-lookup"><span data-stu-id="e502e-107">Type</span></span>|<span data-ttu-id="e502e-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="e502e-108">Required</span></span>|<span data-ttu-id="e502e-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e502e-109">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="e502e-110">myFunction</span><span class="sxs-lookup"><span data-stu-id="e502e-110">myFunction</span></span>|<span data-ttu-id="e502e-111">function reference</span><span class="sxs-lookup"><span data-stu-id="e502e-111">function reference</span></span>|<span data-ttu-id="e502e-112">Có</span><span class="sxs-lookup"><span data-stu-id="e502e-112">Yes</span></span>|<span data-ttu-id="e502e-113">The function to be executed on the form [OnLoad](../events/form-onload.md) event.</span><span class="sxs-lookup"><span data-stu-id="e502e-113">The function to be executed on the form [OnLoad](../events/form-onload.md) event.</span></span> <span data-ttu-id="e502e-114">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="e502e-114">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="e502e-115">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="e502e-115">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="e502e-116">See [Execution context](../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="e502e-116">See [Execution context](../../clientapi-execution-context.md) for more information.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="e502e-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e502e-117">Related topics</span></span>

[<span data-ttu-id="e502e-118">removeOnLoad</span><span class="sxs-lookup"><span data-stu-id="e502e-118">removeOnLoad</span></span>](removeOnLoad.md)

[<span data-ttu-id="e502e-119">Form OnLoad event</span><span class="sxs-lookup"><span data-stu-id="e502e-119">Form OnLoad event</span></span>](../events/form-onload.md)

[<span data-ttu-id="e502e-120">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="e502e-120">formContext.ui</span></span>](../formContext-ui.md)

[<span data-ttu-id="e502e-121">formContext</span><span class="sxs-lookup"><span data-stu-id="e502e-121">formContext</span></span>](../../clientapi-form-context.md)

