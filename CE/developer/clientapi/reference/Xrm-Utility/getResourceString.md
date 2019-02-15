---
title: getResourceString (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 01/02/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d5e51eac-ce0a-4f4a-b7b6-495433e3f8c1
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2909a7e6dae2eebec17075e3aa51176d15a77246
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386052"
---
# <a name="getresourcestring-client-api-reference"></a><span data-ttu-id="8d91d-102">getResourceString (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="8d91d-102">getResourceString (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getResourceString-description.md](./includes/getResourceString-description.md)] 

## <a name="syntax"></a><span data-ttu-id="8d91d-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="8d91d-103">Syntax</span></span>

`Xrm.Utility.getResourceString(webResourceName,key)` 

## <a name="parameters"></a><span data-ttu-id="8d91d-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="8d91d-104">Parameters</span></span>

|<span data-ttu-id="8d91d-105">Tên</span><span class="sxs-lookup"><span data-stu-id="8d91d-105">Name</span></span> |<span data-ttu-id="8d91d-106">Loại</span><span class="sxs-lookup"><span data-stu-id="8d91d-106">Type</span></span> |<span data-ttu-id="8d91d-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="8d91d-107">Required</span></span> |<span data-ttu-id="8d91d-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8d91d-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="8d91d-109">webResourceName</span><span class="sxs-lookup"><span data-stu-id="8d91d-109">webResourceName</span></span>|<span data-ttu-id="8d91d-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="8d91d-110">String</span></span>|<span data-ttu-id="8d91d-111">Có</span><span class="sxs-lookup"><span data-stu-id="8d91d-111">Yes</span></span>|<span data-ttu-id="8d91d-112">The name of the web resource.</span><span class="sxs-lookup"><span data-stu-id="8d91d-112">The name of the web resource.</span></span>|
|<span data-ttu-id="8d91d-113">khóa</span><span class="sxs-lookup"><span data-stu-id="8d91d-113">key</span></span>|<span data-ttu-id="8d91d-114">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="8d91d-114">String</span></span>|<span data-ttu-id="8d91d-115">Có</span><span class="sxs-lookup"><span data-stu-id="8d91d-115">Yes</span></span>|<span data-ttu-id="8d91d-116">The key for the localized string.</span><span class="sxs-lookup"><span data-stu-id="8d91d-116">The key for the localized string.</span></span>|

## <a name="return-value"></a><span data-ttu-id="8d91d-117">Return value</span><span class="sxs-lookup"><span data-stu-id="8d91d-117">Return value</span></span>

<span data-ttu-id="8d91d-118">A localized string.</span><span class="sxs-lookup"><span data-stu-id="8d91d-118">A localized string.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d91d-119">Chú thích</span><span class="sxs-lookup"><span data-stu-id="8d91d-119">Remarks</span></span>

<!-- 
Content adapted from /developer/resx-web-resources 
If you change this, make sure that topic is in sync.
-->

<span data-ttu-id="8d91d-120">When you create RESX web resources you must explicitly set the language value and include the locale identifier (LCID) for the appropriate language in the name of the web resource.</span><span class="sxs-lookup"><span data-stu-id="8d91d-120">When you create RESX web resources you must explicitly set the language value and include the locale identifier (LCID) for the appropriate language in the name of the web resource.</span></span> <span data-ttu-id="8d91d-121">For example, `new_/strings/MyAppResources.1033.resx` would contain resources for English language.</span><span class="sxs-lookup"><span data-stu-id="8d91d-121">For example, `new_/strings/MyAppResources.1033.resx` would contain resources for English language.</span></span> <span data-ttu-id="8d91d-122">See [Microsoft Locale ID Values](https://msdn.microsoft.com/library/ms912047(WinEmbedded.10).aspx) for a list of LCID values.</span><span class="sxs-lookup"><span data-stu-id="8d91d-122">See [Microsoft Locale ID Values](https://msdn.microsoft.com/library/ms912047(WinEmbedded.10).aspx) for a list of LCID values.</span></span>

<span data-ttu-id="8d91d-123">For example `Xrm.Utility.getResourceString("new_/strings/MyAppResources","hello")` will return the localized string value for the resource key `hello` within the `new_/strings/MyAppResources.1033.resx` web resource if the user’s preferred language is English.</span><span class="sxs-lookup"><span data-stu-id="8d91d-123">For example `Xrm.Utility.getResourceString("new_/strings/MyAppResources","hello")` will return the localized string value for the resource key `hello` within the `new_/strings/MyAppResources.1033.resx` web resource if the user’s preferred language is English.</span></span> <span data-ttu-id="8d91d-124">Notice that the function doesn’t refer to any specific language or full name of any RESX web resource.</span><span class="sxs-lookup"><span data-stu-id="8d91d-124">Notice that the function doesn’t refer to any specific language or full name of any RESX web resource.</span></span> <span data-ttu-id="8d91d-125">This functionality depends on the RESX web resource being associated to the calling JavaScript web resource as a dependency.</span><span class="sxs-lookup"><span data-stu-id="8d91d-125">This functionality depends on the RESX web resource being associated to the calling JavaScript web resource as a dependency.</span></span> <span data-ttu-id="8d91d-126">More information: [Web resource dependencies](../../../web-resource-dependencies.md).</span><span class="sxs-lookup"><span data-stu-id="8d91d-126">More information: [Web resource dependencies](../../../web-resource-dependencies.md).</span></span>

<span data-ttu-id="8d91d-127">The appropriate string value will be determined by the individual user’s language preference and the languages available in the organization.</span><span class="sxs-lookup"><span data-stu-id="8d91d-127">The appropriate string value will be determined by the individual user’s language preference and the languages available in the organization.</span></span> <span data-ttu-id="8d91d-128">If a localized string is not found that matches the user’s language preference, the localized string will automatically fallback to the base language for the organization.</span><span class="sxs-lookup"><span data-stu-id="8d91d-128">If a localized string is not found that matches the user’s language preference, the localized string will automatically fallback to the base language for the organization.</span></span> <span data-ttu-id="8d91d-129">If no matching localized string is found for the organizations base language, a null value will be returned.</span><span class="sxs-lookup"><span data-stu-id="8d91d-129">If no matching localized string is found for the organizations base language, a null value will be returned.</span></span>

### <a name="related-topics"></a><span data-ttu-id="8d91d-130">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="8d91d-130">Related topics</span></span>

[<span data-ttu-id="8d91d-131">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="8d91d-131">Xrm.Utility</span></span>](../xrm-utility.md)<br />
[<span data-ttu-id="8d91d-132">String (RESX) web resources</span><span class="sxs-lookup"><span data-stu-id="8d91d-132">String (RESX) web resources</span></span>](../../../resx-web-resources.md)<br />
[<span data-ttu-id="8d91d-133">Quan hệ phụ thuộc tài nguyên web</span><span class="sxs-lookup"><span data-stu-id="8d91d-133">Web resource dependencies</span></span>](../../../web-resource-dependencies.md)



