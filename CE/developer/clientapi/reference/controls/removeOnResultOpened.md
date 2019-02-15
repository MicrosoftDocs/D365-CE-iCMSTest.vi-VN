---
title: removeOnResultOpened (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a9a37c95f900373e528e90024595311745a43a37
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386545"
---
# <a name="removeonresultopened-client-api-reference"></a><span data-ttu-id="8d467-102">removeOnResultOpened (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="8d467-102">removeOnResultOpened (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8d467-103">Removes an event handler from the [OnResultOpened](../events/onresultopened.md) event.</span><span class="sxs-lookup"><span data-stu-id="8d467-103">Removes an event handler from the [OnResultOpened](../events/onresultopened.md) event.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="8d467-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="8d467-104">Control types supported</span></span>

<span data-ttu-id="8d467-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="8d467-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="8d467-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="8d467-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.removeOnResultOpened(myFunction);
```

## <a name="parameters"></a><span data-ttu-id="8d467-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="8d467-107">Parameters</span></span>

|<span data-ttu-id="8d467-108">Tên</span><span class="sxs-lookup"><span data-stu-id="8d467-108">Name</span></span> | <span data-ttu-id="8d467-109">Loại</span><span class="sxs-lookup"><span data-stu-id="8d467-109">Type</span></span> | <span data-ttu-id="8d467-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="8d467-110">Required</span></span> | <span data-ttu-id="8d467-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8d467-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="8d467-112">myFunction</span><span class="sxs-lookup"><span data-stu-id="8d467-112">myFunction</span></span> |<span data-ttu-id="8d467-113">Hàm</span><span class="sxs-lookup"><span data-stu-id="8d467-113">Function</span></span> |<span data-ttu-id="8d467-114">Có</span><span class="sxs-lookup"><span data-stu-id="8d467-114">Yes</span></span>|<span data-ttu-id="8d467-115">The function to remove from the **OnResultOpened** event.</span><span class="sxs-lookup"><span data-stu-id="8d467-115">The function to remove from the **OnResultOpened** event.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="8d467-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="8d467-116">Related topics</span></span>

[<span data-ttu-id="8d467-117">OnResultOpened event</span><span class="sxs-lookup"><span data-stu-id="8d467-117">OnResultOpened event</span></span>](../events/onresultopened.md)

[<span data-ttu-id="8d467-118">addOnResultOpened</span><span class="sxs-lookup"><span data-stu-id="8d467-118">addOnResultOpened</span></span>](addOnResultOpened.md) 


