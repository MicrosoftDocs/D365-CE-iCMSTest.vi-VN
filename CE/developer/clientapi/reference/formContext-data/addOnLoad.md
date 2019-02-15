---
title: addOnLoad (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 03e970ee-7ed3-4df2-9670-222d76a479fd
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9c2a808237f8bb826e012911bcbbbbbe136b7941
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387681"
---
# <a name="addonload-client-api-reference"></a><span data-ttu-id="c7ef8-102">addOnLoad (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="c7ef8-102">addOnLoad (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnLoad-description.md](./includes/addOnLoad-description.md)]

## <a name="syntax"></a><span data-ttu-id="c7ef8-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="c7ef8-103">Syntax</span></span>

`formContext.data.addOnLoad(myFunction)`

## <a name="parameter"></a><span data-ttu-id="c7ef8-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="c7ef8-104">Parameter</span></span>

|    <span data-ttu-id="c7ef8-105">Tên</span><span class="sxs-lookup"><span data-stu-id="c7ef8-105">Name</span></span>    |        <span data-ttu-id="c7ef8-106">Loại</span><span class="sxs-lookup"><span data-stu-id="c7ef8-106">Type</span></span>        | <span data-ttu-id="c7ef8-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="c7ef8-107">Required</span></span> |                                                                                                                                               <span data-ttu-id="c7ef8-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="c7ef8-108">Description</span></span>                                                                                                                                               |
|------------|--------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ef8-109">myFunction</span><span class="sxs-lookup"><span data-stu-id="c7ef8-109">myFunction</span></span> | <span data-ttu-id="c7ef8-110">function reference</span><span class="sxs-lookup"><span data-stu-id="c7ef8-110">function reference</span></span> |   <span data-ttu-id="c7ef8-111">Có</span><span class="sxs-lookup"><span data-stu-id="c7ef8-111">Yes</span></span>    | <span data-ttu-id="c7ef8-112">The function to be executed when the form data loads.</span><span class="sxs-lookup"><span data-stu-id="c7ef8-112">The function to be executed when the form data loads.</span></span> <span data-ttu-id="c7ef8-113">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="c7ef8-113">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="c7ef8-114">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="c7ef8-114">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="c7ef8-115">See [Execution context](../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="c7ef8-115">See [Execution context](../../clientapi-execution-context.md) for more information.</span></span> |

### <a name="related-topics"></a><span data-ttu-id="c7ef8-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="c7ef8-116">Related topics</span></span>

[<span data-ttu-id="c7ef8-117">removeOnLoad</span><span class="sxs-lookup"><span data-stu-id="c7ef8-117">removeOnLoad</span></span>](removeOnLoad.md)

[<span data-ttu-id="c7ef8-118">Form data OnLoad event</span><span class="sxs-lookup"><span data-stu-id="c7ef8-118">Form data OnLoad event</span></span>](../events/form-data-onload.md)

