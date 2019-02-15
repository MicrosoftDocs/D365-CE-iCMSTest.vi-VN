---
title: prependOrgName (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3bde3c4599793ca48b34249e949838d1844cccab
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386980"
---
# <a name="prependorgname-client-api-reference"></a><span data-ttu-id="20bd1-102">prependOrgName (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="20bd1-102">prependOrgName (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="20bd1-103">Prefixes the current organization's unique name to a string, typically a URL path.</span><span class="sxs-lookup"><span data-stu-id="20bd1-103">Prefixes the current organization's unique name to a string, typically a URL path.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bd1-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="20bd1-104">Syntax</span></span>

 ```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.prependOrgName(sPath);
```

## <a name="parameters"></a><span data-ttu-id="20bd1-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="20bd1-105">Parameters</span></span>

|<span data-ttu-id="20bd1-106">Tên</span><span class="sxs-lookup"><span data-stu-id="20bd1-106">Name</span></span> |<span data-ttu-id="20bd1-107">Loại</span><span class="sxs-lookup"><span data-stu-id="20bd1-107">Type</span></span> |<span data-ttu-id="20bd1-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="20bd1-108">Required</span></span> |<span data-ttu-id="20bd1-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="20bd1-109">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="20bd1-110">sPath</span><span class="sxs-lookup"><span data-stu-id="20bd1-110">sPath</span></span> |<span data-ttu-id="20bd1-111">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="20bd1-111">String</span></span> |<span data-ttu-id="20bd1-112">Có</span><span class="sxs-lookup"><span data-stu-id="20bd1-112">Yes</span></span> |<span data-ttu-id="20bd1-113">A local path to a resource.</span><span class="sxs-lookup"><span data-stu-id="20bd1-113">A local path to a resource.</span></span> |

## <a name="return-value"></a><span data-ttu-id="20bd1-114">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="20bd1-114">Return Value</span></span>

<span data-ttu-id="20bd1-115">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="20bd1-115">**Type**: String</span></span>

<span data-ttu-id="20bd1-116">**Description**: A path string with the organization name prefixed in the following format:</span><span class="sxs-lookup"><span data-stu-id="20bd1-116">**Description**: A path string with the organization name prefixed in the following format:</span></span>

`"/"+ orgName + sPath`

### <a name="related-topics"></a><span data-ttu-id="20bd1-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="20bd1-117">Related topics</span></span>

[<span data-ttu-id="20bd1-118">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="20bd1-118">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)


