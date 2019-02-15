---
title: addOnProcessStatusChange (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 2bf30298-f52b-4ab7-8833-4838f0d87e12
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3edafa67793ecb62ce0318a3b89b63822c2d702d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385471"
---
# <a name="addonprocessstatuschange-client-api-reference"></a><span data-ttu-id="9195b-102">addOnProcessStatusChange (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="9195b-102">addOnProcessStatusChange (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnProcessStatusChange-description.md](./includes/addOnProcessStatusChange-description.md)]

## <a name="syntax"></a><span data-ttu-id="9195b-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="9195b-103">Syntax</span></span>

`formContext.data.process.addOnProcessStatusChange(myFunction);`

## <a name="parameter"></a><span data-ttu-id="9195b-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="9195b-104">Parameter</span></span>

|<span data-ttu-id="9195b-105">Tên</span><span class="sxs-lookup"><span data-stu-id="9195b-105">Name</span></span>|<span data-ttu-id="9195b-106">Loại</span><span class="sxs-lookup"><span data-stu-id="9195b-106">Type</span></span>|<span data-ttu-id="9195b-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="9195b-107">Required</span></span>|<span data-ttu-id="9195b-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9195b-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="9195b-109">myFunction</span><span class="sxs-lookup"><span data-stu-id="9195b-109">myFunction</span></span>|<span data-ttu-id="9195b-110">Function reference</span><span class="sxs-lookup"><span data-stu-id="9195b-110">Function reference</span></span>|<span data-ttu-id="9195b-111">Có</span><span class="sxs-lookup"><span data-stu-id="9195b-111">Yes</span></span>|<span data-ttu-id="9195b-112">The function to be executed when the business process flow status changes.</span><span class="sxs-lookup"><span data-stu-id="9195b-112">The function to be executed when the business process flow status changes.</span></span> <span data-ttu-id="9195b-113">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="9195b-113">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="9195b-114">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="9195b-114">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="9195b-115">See [Execution context](../../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="9195b-115">See [Execution context](../../../clientapi-execution-context.md) for more information.</span></span><br/><br/><span data-ttu-id="9195b-116">You should use a reference to a named function rather than an anonymous function if you may later want to remove the event handler.</span><span class="sxs-lookup"><span data-stu-id="9195b-116">You should use a reference to a named function rather than an anonymous function if you may later want to remove the event handler.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="9195b-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="9195b-117">Related topics</span></span>

[<span data-ttu-id="9195b-118">removeOnProcessStatusChange</span><span class="sxs-lookup"><span data-stu-id="9195b-118">removeOnProcessStatusChange</span></span>](removeOnProcessStatusChange.md)
 
[<span data-ttu-id="9195b-119">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="9195b-119">formContext.data.process</span></span>](../../formContext-data-process.md)

