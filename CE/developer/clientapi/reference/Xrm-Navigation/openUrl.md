---
title: openUrl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 29cb3685-21aa-42fc-8e84-0074dcc69197
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 6b9436e9148bd815c77dafaafce6817e2310c8f0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387030"
---
# <a name="openurl-client-api-reference"></a><span data-ttu-id="a8b04-102">openUrl (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a8b04-102">openUrl (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openUrl-description.md](./includes/openUrl-description.md)]

## <a name="syntax"></a><span data-ttu-id="a8b04-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a8b04-103">Syntax</span></span>

`Xrm.Navigation.openUrl(url,openUrlOptions)`

## <a name="parameters"></a><span data-ttu-id="a8b04-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="a8b04-104">Parameters</span></span>

|<span data-ttu-id="a8b04-105">Tên</span><span class="sxs-lookup"><span data-stu-id="a8b04-105">Name</span></span> |<span data-ttu-id="a8b04-106">Loại</span><span class="sxs-lookup"><span data-stu-id="a8b04-106">Type</span></span> |<span data-ttu-id="a8b04-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="a8b04-107">Required</span></span> |<span data-ttu-id="a8b04-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="a8b04-108">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="a8b04-109">url</span><span class="sxs-lookup"><span data-stu-id="a8b04-109">url</span></span>|<span data-ttu-id="a8b04-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="a8b04-110">String</span></span>|<span data-ttu-id="a8b04-111">Có</span><span class="sxs-lookup"><span data-stu-id="a8b04-111">Yes</span></span>|<span data-ttu-id="a8b04-112">URL to open.</span><span class="sxs-lookup"><span data-stu-id="a8b04-112">URL to open.</span></span>|
|<span data-ttu-id="a8b04-113">openUrlOptions</span><span class="sxs-lookup"><span data-stu-id="a8b04-113">openUrlOptions</span></span>|<span data-ttu-id="a8b04-114">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="a8b04-114">Object</span></span>|<span data-ttu-id="a8b04-115">Không</span><span class="sxs-lookup"><span data-stu-id="a8b04-115">No</span></span>|<span data-ttu-id="a8b04-116">Options to open the URL.The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="a8b04-116">Options to open the URL.The object contains the following attributes:</span></span><br/><span data-ttu-id="a8b04-117">- **height**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="a8b04-117">- **height**: (Optional) Number.</span></span> <span data-ttu-id="a8b04-118">Height of the window to display the resultant page in pixels.</span><span class="sxs-lookup"><span data-stu-id="a8b04-118">Height of the window to display the resultant page in pixels.</span></span><br/><span data-ttu-id="a8b04-119">- **width**: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="a8b04-119">- **width**: (Optional) Number.</span></span> <span data-ttu-id="a8b04-120">Width of the window to display the resultant page in pixels.</span><span class="sxs-lookup"><span data-stu-id="a8b04-120">Width of the window to display the resultant page in pixels.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a8b04-121">Chú thích</span><span class="sxs-lookup"><span data-stu-id="a8b04-121">Remarks</span></span>

<span data-ttu-id="a8b04-122">This method is especially helpful for mobile clients to open a URL in a browser outside of shim.</span><span class="sxs-lookup"><span data-stu-id="a8b04-122">This method is especially helpful for mobile clients to open a URL in a browser outside of shim.</span></span>

 ### <a name="related-topics"></a><span data-ttu-id="a8b04-123">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a8b04-123">Related topics</span></span>

[<span data-ttu-id="a8b04-124">Xrm.Navigation</span><span class="sxs-lookup"><span data-stu-id="a8b04-124">Xrm.Navigation</span></span>](../xrm-navigation.md)

