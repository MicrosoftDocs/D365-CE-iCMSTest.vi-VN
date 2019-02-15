---
title: addOnSave (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1a66f93d-a47c-4316-91f1-dcf5d09f9d19
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: daa7d6e24fe29a50c2e9041ca9c4c35f3018be3e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386341"
---
# <a name="addonsave-client-api-reference"></a><span data-ttu-id="4a31a-102">addOnSave (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="4a31a-102">addOnSave (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/addOnSave-description.md](./includes/addOnSave-description.md)]

## <a name="syntax"></a><span data-ttu-id="4a31a-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="4a31a-103">Syntax</span></span>

`formContext.data.entity.addOnSave(myFunction)`

## <a name="parameter"></a><span data-ttu-id="4a31a-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="4a31a-104">Parameter</span></span>

|<span data-ttu-id="4a31a-105">Tên</span><span class="sxs-lookup"><span data-stu-id="4a31a-105">Name</span></span>|<span data-ttu-id="4a31a-106">Loại</span><span class="sxs-lookup"><span data-stu-id="4a31a-106">Type</span></span>|<span data-ttu-id="4a31a-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="4a31a-107">Required</span></span>|<span data-ttu-id="4a31a-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="4a31a-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="4a31a-109">myFunction</span><span class="sxs-lookup"><span data-stu-id="4a31a-109">myFunction</span></span>|<span data-ttu-id="4a31a-110">function reference</span><span class="sxs-lookup"><span data-stu-id="4a31a-110">function reference</span></span>|<span data-ttu-id="4a31a-111">Có</span><span class="sxs-lookup"><span data-stu-id="4a31a-111">Yes</span></span>|<span data-ttu-id="4a31a-112">The function to be executed when the record is saved.</span><span class="sxs-lookup"><span data-stu-id="4a31a-112">The function to be executed when the record is saved.</span></span> <span data-ttu-id="4a31a-113">The function will be added to the bottom of the event handler pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a31a-113">The function will be added to the bottom of the event handler pipeline.</span></span> <span data-ttu-id="4a31a-114">The execution context is automatically passed as the first parameter to the function.</span><span class="sxs-lookup"><span data-stu-id="4a31a-114">The execution context is automatically passed as the first parameter to the function.</span></span> <span data-ttu-id="4a31a-115">See [Execution context](../../clientapi-execution-context.md) for more information.</span><span class="sxs-lookup"><span data-stu-id="4a31a-115">See [Execution context](../../clientapi-execution-context.md) for more information.</span></span>

### <a name="related-topics"></a><span data-ttu-id="4a31a-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="4a31a-116">Related topics</span></span>

[<span data-ttu-id="4a31a-117">removeOnSave</span><span class="sxs-lookup"><span data-stu-id="4a31a-117">removeOnSave</span></span>](removeOnSave.md)

[<span data-ttu-id="4a31a-118">Form OnSave event</span><span class="sxs-lookup"><span data-stu-id="4a31a-118">Form OnSave event</span></span>](../events/form-onsave.md)

