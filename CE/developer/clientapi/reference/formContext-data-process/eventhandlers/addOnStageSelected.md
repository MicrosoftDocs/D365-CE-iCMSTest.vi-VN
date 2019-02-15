---
title: addOnStageSelected (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5982770c-d5a4-415a-a32d-3734b6210bb9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6a4089ec83ef62f72f4abcdca313ee855daa8a83
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388384"
---
# <a name="addonstageselected-client-api-reference"></a><span data-ttu-id="20e4c-102">addOnStageSelected (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="20e4c-102">addOnStageSelected (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnStageSelected-description.md](./includes/addOnStageSelected-description.md)]

## <a name="syntax"></a><span data-ttu-id="20e4c-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="20e4c-103">Syntax</span></span>

`formContext.data.process.addOnStageSelected(myFunction);`

## <a name="parameter"></a><span data-ttu-id="20e4c-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="20e4c-104">Parameter</span></span>

|<span data-ttu-id="20e4c-105">Tên</span><span class="sxs-lookup"><span data-stu-id="20e4c-105">Name</span></span>|<span data-ttu-id="20e4c-106">Loại</span><span class="sxs-lookup"><span data-stu-id="20e4c-106">Type</span></span>|<span data-ttu-id="20e4c-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="20e4c-107">Required</span></span>|<span data-ttu-id="20e4c-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="20e4c-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="20e4c-109">myFunction</span><span class="sxs-lookup"><span data-stu-id="20e4c-109">myFunction</span></span>|<span data-ttu-id="20e4c-110">Function reference</span><span class="sxs-lookup"><span data-stu-id="20e4c-110">Function reference</span></span>|<span data-ttu-id="20e4c-111">Có</span><span class="sxs-lookup"><span data-stu-id="20e4c-111">Yes</span></span>|<span data-ttu-id="20e4c-112">The function to be executed when the business process flow stage is selected.</span><span class="sxs-lookup"><span data-stu-id="20e4c-112">The function to be executed when the business process flow stage is selected.</span></span> <span data-ttu-id="20e4c-113">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="20e4c-113">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="20e4c-114">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="20e4c-114">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="20e4c-115">See [Execution context](../../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="20e4c-115">See [Execution context](../../../clientapi-execution-context.md) for more information.</span></span><br/><br/><span data-ttu-id="20e4c-116">You should use a reference to a named function rather than an anonymous function if you may later want to remove the event handler.</span><span class="sxs-lookup"><span data-stu-id="20e4c-116">You should use a reference to a named function rather than an anonymous function if you may later want to remove the event handler.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="20e4c-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="20e4c-117">Related topics</span></span>

[<span data-ttu-id="20e4c-118">removeOnStageSelected</span><span class="sxs-lookup"><span data-stu-id="20e4c-118">removeOnStageSelected</span></span>](removeOnStageSelected.md)
 
[<span data-ttu-id="20e4c-119">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="20e4c-119">formContext.data.process</span></span>](../../formContext-data-process.md)
 


