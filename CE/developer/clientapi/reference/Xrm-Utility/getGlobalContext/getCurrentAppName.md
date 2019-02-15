---
title: getCurrentAppName (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a8f83718-41a4-4958-a5ac-9b28cc2f8dba
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 003d4fd5fafd37e2ccca51851e4e041cf1fae2d7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387728"
---
# <a name="getcurrentappname-client-api-reference"></a><span data-ttu-id="8a7fe-102">getCurrentAppName (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="8a7fe-102">getCurrentAppName (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8a7fe-103">Returns the name of the current business app in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="8a7fe-103">Returns the name of the current business app in Customer Engagement.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7fe-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="8a7fe-104">Syntax</span></span>

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getCurrentAppName().then(successCallback, errorCallback);
``` 

## <a name="parameters"></a><span data-ttu-id="8a7fe-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="8a7fe-105">Parameters</span></span>

|<span data-ttu-id="8a7fe-106">Tên</span><span class="sxs-lookup"><span data-stu-id="8a7fe-106">Name</span></span> |<span data-ttu-id="8a7fe-107">Loại</span><span class="sxs-lookup"><span data-stu-id="8a7fe-107">Type</span></span> |<span data-ttu-id="8a7fe-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="8a7fe-108">Required</span></span> |<span data-ttu-id="8a7fe-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8a7fe-109">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="8a7fe-110">successCallback</span><span class="sxs-lookup"><span data-stu-id="8a7fe-110">successCallback</span></span> |<span data-ttu-id="8a7fe-111">Hàm</span><span class="sxs-lookup"><span data-stu-id="8a7fe-111">Function</span></span> |<span data-ttu-id="8a7fe-112">Có</span><span class="sxs-lookup"><span data-stu-id="8a7fe-112">Yes</span></span> |<span data-ttu-id="8a7fe-113">A function to call when the business app name is returned.</span><span class="sxs-lookup"><span data-stu-id="8a7fe-113">A function to call when the business app name is returned.</span></span>  |
|<span data-ttu-id="8a7fe-114">errorCallback</span><span class="sxs-lookup"><span data-stu-id="8a7fe-114">errorCallback</span></span> |<span data-ttu-id="8a7fe-115">Hàm</span><span class="sxs-lookup"><span data-stu-id="8a7fe-115">Function</span></span> |<span data-ttu-id="8a7fe-116">Có</span><span class="sxs-lookup"><span data-stu-id="8a7fe-116">Yes</span></span> |<span data-ttu-id="8a7fe-117">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="8a7fe-117">A function to call when the operation fails.</span></span>  |

## <a name="return-value"></a><span data-ttu-id="8a7fe-118">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="8a7fe-118">Return Value</span></span>

<span data-ttu-id="8a7fe-119">If this method is called in the context of a business app, returns the name of the business app.</span><span class="sxs-lookup"><span data-stu-id="8a7fe-119">If this method is called in the context of a business app, returns the name of the business app.</span></span> <span data-ttu-id="8a7fe-120">Otherwise, it fails with an error.</span><span class="sxs-lookup"><span data-stu-id="8a7fe-120">Otherwise, it fails with an error.</span></span>

### <a name="related-topics"></a><span data-ttu-id="8a7fe-121">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="8a7fe-121">Related topics</span></span>

[<span data-ttu-id="8a7fe-122">Create and manage custom business apps using code</span><span class="sxs-lookup"><span data-stu-id="8a7fe-122">Create and manage custom business apps using code</span></span>](../../../../create-manage-custom-business-apps-using-code.md)

[<span data-ttu-id="8a7fe-123">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="8a7fe-123">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)


