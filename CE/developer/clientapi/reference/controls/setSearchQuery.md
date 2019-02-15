---
title: setSearchQuery (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 99e82b80-b6c3-4ee8-83cc-637b13ed8498
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 222324e1963f5b3eaf147b27c47ea126277439a1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387033"
---
# <a name="setsearchquery-client-api-reference"></a><span data-ttu-id="0a886-102">setSearchQuery (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="0a886-102">setSearchQuery (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="0a886-103">Sets the text used as the search criteria for the knowledge base search control.</span><span class="sxs-lookup"><span data-stu-id="0a886-103">Sets the text used as the search criteria for the knowledge base search control.</span></span>

## <a name="control-types-supported"></a><span data-ttu-id="0a886-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="0a886-104">Control types supported</span></span>

<span data-ttu-id="0a886-105">knowledge base search control</span><span class="sxs-lookup"><span data-stu-id="0a886-105">knowledge base search control</span></span>

## <a name="syntax"></a><span data-ttu-id="0a886-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="0a886-106">Syntax</span></span>

```
var kbSearchControl = formContext.getControl("<name>");
kbSearchControl.setSearchQuery(searchString);
```

## <a name="parameters"></a><span data-ttu-id="0a886-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="0a886-107">Parameters</span></span>

|<span data-ttu-id="0a886-108">Tên</span><span class="sxs-lookup"><span data-stu-id="0a886-108">Name</span></span> | <span data-ttu-id="0a886-109">Loại</span><span class="sxs-lookup"><span data-stu-id="0a886-109">Type</span></span> | <span data-ttu-id="0a886-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="0a886-110">Required</span></span> | <span data-ttu-id="0a886-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="0a886-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="0a886-112">searchString</span><span class="sxs-lookup"><span data-stu-id="0a886-112">searchString</span></span> |<span data-ttu-id="0a886-113">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="0a886-113">String</span></span> |<span data-ttu-id="0a886-114">Có</span><span class="sxs-lookup"><span data-stu-id="0a886-114">Yes</span></span>|<span data-ttu-id="0a886-115">The text for the search query.</span><span class="sxs-lookup"><span data-stu-id="0a886-115">The text for the search query.</span></span>| 

### <a name="related-topics"></a><span data-ttu-id="0a886-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="0a886-116">Related topics</span></span>

[<span data-ttu-id="0a886-117">getSearchQuery</span><span class="sxs-lookup"><span data-stu-id="0a886-117">getSearchQuery</span></span>](getSearchQuery.md)


