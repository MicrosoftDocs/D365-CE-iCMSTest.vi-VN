---
title: addTabStateChange (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 51b0dbf3-28bd-4eea-9ee9-50b322e9af9b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b069e0199f9dccd9a7613d9feada7b2b76b7bb1a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387744"
---
# <a name="addtabstatechange-client-api-reference"></a><span data-ttu-id="30684-102">addTabStateChange (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="30684-102">addTabStateChange (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addTabStateChange-description.md](./includes/addTabStateChange-description.md)]<span data-ttu-id="30684-103">.</span><span class="sxs-lookup"><span data-stu-id="30684-103">.</span></span>

## <a name="syntax"></a><span data-ttu-id="30684-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="30684-104">Syntax</span></span>

`tabObj.addTabStateChange(myFunction);` 

## <a name="parameter"></a><span data-ttu-id="30684-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="30684-105">Parameter</span></span>

|<span data-ttu-id="30684-106">Tên</span><span class="sxs-lookup"><span data-stu-id="30684-106">Name</span></span>|<span data-ttu-id="30684-107">Loại</span><span class="sxs-lookup"><span data-stu-id="30684-107">Type</span></span>|<span data-ttu-id="30684-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="30684-108">Required</span></span>|<span data-ttu-id="30684-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="30684-109">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="30684-110">myFunction</span><span class="sxs-lookup"><span data-stu-id="30684-110">myFunction</span></span>|<span data-ttu-id="30684-111">function reference</span><span class="sxs-lookup"><span data-stu-id="30684-111">function reference</span></span>|<span data-ttu-id="30684-112">Có</span><span class="sxs-lookup"><span data-stu-id="30684-112">Yes</span></span>|<span data-ttu-id="30684-113">The function to be executed on the [TabStateChange](../events/tabstatechange.md) event.</span><span class="sxs-lookup"><span data-stu-id="30684-113">The function to be executed on the [TabStateChange](../events/tabstatechange.md) event.</span></span> <span data-ttu-id="30684-114">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="30684-114">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="30684-115">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="30684-115">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="30684-116">See [Execution context](../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="30684-116">See [Execution context](../../clientapi-execution-context.md) for more information.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="30684-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="30684-117">Related topics</span></span>

[<span data-ttu-id="30684-118">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="30684-118">formContext.ui</span></span>](../formContext-ui.md)

[<span data-ttu-id="30684-119">formContext</span><span class="sxs-lookup"><span data-stu-id="30684-119">formContext</span></span>](../../clientapi-form-context.md)


