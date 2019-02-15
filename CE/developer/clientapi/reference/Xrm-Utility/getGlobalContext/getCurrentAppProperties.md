---
title: getCurrentAppProperties (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 5f8d91ff-ba0d-4e90-a79a-18e32d09baa3
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 35b704bc1065da802f4d4da4223ed316b6d157e4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387526"
---
# <a name="getcurrentappproperties-client-api-reference"></a><span data-ttu-id="55263-102">getCurrentAppProperties (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="55263-102">getCurrentAppProperties (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="55263-103">Returns the properties of the current business app in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="55263-103">Returns the properties of the current business app in Customer Engagement.</span></span>

## <a name="syntax"></a><span data-ttu-id="55263-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="55263-104">Syntax</span></span>

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getCurrentAppProperties().then(successCallback, errorCallback);
``` 

## <a name="parameters"></a><span data-ttu-id="55263-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="55263-105">Parameters</span></span>

|<span data-ttu-id="55263-106">Tên</span><span class="sxs-lookup"><span data-stu-id="55263-106">Name</span></span> |<span data-ttu-id="55263-107">Loại</span><span class="sxs-lookup"><span data-stu-id="55263-107">Type</span></span> |<span data-ttu-id="55263-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="55263-108">Required</span></span> |<span data-ttu-id="55263-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="55263-109">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="55263-110">successCallback</span><span class="sxs-lookup"><span data-stu-id="55263-110">successCallback</span></span> |<span data-ttu-id="55263-111">Hàm</span><span class="sxs-lookup"><span data-stu-id="55263-111">Function</span></span> |<span data-ttu-id="55263-112">Có</span><span class="sxs-lookup"><span data-stu-id="55263-112">Yes</span></span> |<span data-ttu-id="55263-113">A function to call when the business app property information is returned.</span><span class="sxs-lookup"><span data-stu-id="55263-113">A function to call when the business app property information is returned.</span></span> <span data-ttu-id="55263-114">An object with the following attributes (app properties) is passed to the function :</span><span class="sxs-lookup"><span data-stu-id="55263-114">An object with the following attributes (app properties) is passed to the function :</span></span><br/><span data-ttu-id="55263-115">- **appId**</span><span class="sxs-lookup"><span data-stu-id="55263-115">- **appId**</span></span><br/><span data-ttu-id="55263-116">- **displayName**</span><span class="sxs-lookup"><span data-stu-id="55263-116">- **displayName**</span></span><br/><span data-ttu-id="55263-117">- **uniqueName**</span><span class="sxs-lookup"><span data-stu-id="55263-117">- **uniqueName**</span></span><br/><span data-ttu-id="55263-118">- **url**</span><span class="sxs-lookup"><span data-stu-id="55263-118">- **url**</span></span><br/><span data-ttu-id="55263-119">- **webResourceId**</span><span class="sxs-lookup"><span data-stu-id="55263-119">- **webResourceId**</span></span><br/><span data-ttu-id="55263-120">- **webResourceName**</span><span class="sxs-lookup"><span data-stu-id="55263-120">- **webResourceName**</span></span><br/><span data-ttu-id="55263-121">- **welcomePageId**</span><span class="sxs-lookup"><span data-stu-id="55263-121">- **welcomePageId**</span></span><br/><span data-ttu-id="55263-122">- **welcomePageName**</span><span class="sxs-lookup"><span data-stu-id="55263-122">- **welcomePageName**</span></span>|
|<span data-ttu-id="55263-123">errorCallback</span><span class="sxs-lookup"><span data-stu-id="55263-123">errorCallback</span></span> |<span data-ttu-id="55263-124">Hàm</span><span class="sxs-lookup"><span data-stu-id="55263-124">Function</span></span> |<span data-ttu-id="55263-125">Có</span><span class="sxs-lookup"><span data-stu-id="55263-125">Yes</span></span> |<span data-ttu-id="55263-126">A function to call when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="55263-126">A function to call when the operation fails.</span></span>  |

## <a name="return-value"></a><span data-ttu-id="55263-127">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="55263-127">Return Value</span></span>

<span data-ttu-id="55263-128">If this method is called in the context of a business app, returns the properties of the business app.</span><span class="sxs-lookup"><span data-stu-id="55263-128">If this method is called in the context of a business app, returns the properties of the business app.</span></span> <span data-ttu-id="55263-129">Otherwise, it fails with an error.</span><span class="sxs-lookup"><span data-stu-id="55263-129">Otherwise, it fails with an error.</span></span>

### <a name="related-topics"></a><span data-ttu-id="55263-130">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="55263-130">Related topics</span></span>

[<span data-ttu-id="55263-131">Create and manage custom business apps using code</span><span class="sxs-lookup"><span data-stu-id="55263-131">Create and manage custom business apps using code</span></span>](../../../../create-manage-custom-business-apps-using-code.md)

[<span data-ttu-id="55263-132">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="55263-132">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md) 



