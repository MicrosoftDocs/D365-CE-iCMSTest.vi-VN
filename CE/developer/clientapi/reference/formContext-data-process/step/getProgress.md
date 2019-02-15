---
title: getProgress (Client API reference) in Dynamics 365 for Customer Engagement apps| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 56502c8b-af23-40d1-ad97-e780bb757d6d
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 680b559cee804c3be60b5677897f85908a8572f1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386161"
---
# <a name="getprogress-client-api-reference"></a><span data-ttu-id="0e4d0-102">getProgress (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="0e4d0-102">getProgress (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getProgress-description.md](./includes/getProgress-description.md)]

## <a name="syntax"></a><span data-ttu-id="0e4d0-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="0e4d0-103">Syntax</span></span>

`var stepProgress = stepObj.getProgress();`

## <a name="return-value"></a><span data-ttu-id="0e4d0-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="0e4d0-104">Return Value</span></span>

<span data-ttu-id="0e4d0-105">**Type**: Number.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-105">**Type**: Number.</span></span> 

<span data-ttu-id="0e4d0-106">**Description**: Returns one of the following values:</span><span class="sxs-lookup"><span data-stu-id="0e4d0-106">**Description**: Returns one of the following values:</span></span>

|<span data-ttu-id="0e4d0-107">Value</span><span class="sxs-lookup"><span data-stu-id="0e4d0-107">Value</span></span> |<span data-ttu-id="0e4d0-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="0e4d0-108">Description</span></span>|
|--|--|
|<span data-ttu-id="0e4d0-109">0</span><span class="sxs-lookup"><span data-stu-id="0e4d0-109">0</span></span>|<span data-ttu-id="0e4d0-110">Không có</span><span class="sxs-lookup"><span data-stu-id="0e4d0-110">None</span></span>|
|<span data-ttu-id="0e4d0-111">1</span><span class="sxs-lookup"><span data-stu-id="0e4d0-111">1</span></span>|<span data-ttu-id="0e4d0-112">Processing</span><span class="sxs-lookup"><span data-stu-id="0e4d0-112">Processing</span></span>|
|<span data-ttu-id="0e4d0-113">2</span><span class="sxs-lookup"><span data-stu-id="0e4d0-113">2</span></span>|<span data-ttu-id="0e4d0-114">Đã hoàn thành</span><span class="sxs-lookup"><span data-stu-id="0e4d0-114">Completed</span></span>|
|<span data-ttu-id="0e4d0-115">3</span><span class="sxs-lookup"><span data-stu-id="0e4d0-115">3</span></span>|<span data-ttu-id="0e4d0-116">Failure</span><span class="sxs-lookup"><span data-stu-id="0e4d0-116">Failure</span></span>|
|<span data-ttu-id="0e4d0-117">4</span><span class="sxs-lookup"><span data-stu-id="0e4d0-117">4</span></span>|<span data-ttu-id="0e4d0-118">Invalid</span><span class="sxs-lookup"><span data-stu-id="0e4d0-118">Invalid</span></span>|

## <a name="remarks"></a><span data-ttu-id="0e4d0-119">Chú thích</span><span class="sxs-lookup"><span data-stu-id="0e4d0-119">Remarks</span></span>

<span data-ttu-id="0e4d0-120">This method is supported only for the action steps; not for the data steps.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-120">This method is supported only for the action steps; not for the data steps.</span></span> <span data-ttu-id="0e4d0-121">Action steps are buttons on the business process stages that users can click to trigger an on-demand workflow or action.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-121">Action steps are buttons on the business process stages that users can click to trigger an on-demand workflow or action.</span></span> <span data-ttu-id="0e4d0-122">Action step is a preview feature introduced in the [!INCLUDE[pn_crm_9_0_0_online](../../../../../includes/pn-crm-9-0-0-online.md)] release.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-122">Action step is a preview feature introduced in the [!INCLUDE[pn_crm_9_0_0_online](../../../../../includes/pn-crm-9-0-0-online.md)] release.</span></span> <span data-ttu-id="0e4d0-123">More information: See the **Business Process Flow automation with Action Steps** section in [Blog: New automation and visualization features for Business Process Flows (public preview)](https://blogs.msdn.microsoft.com/crm/2017/10/25/new-automation-and-visualization-features-for-business-process-flows-public-preview/)</span><span class="sxs-lookup"><span data-stu-id="0e4d0-123">More information: See the **Business Process Flow automation with Action Steps** section in [Blog: New automation and visualization features for Business Process Flows (public preview)](https://blogs.msdn.microsoft.com/crm/2017/10/25/new-automation-and-visualization-features-for-business-process-flows-public-preview/)</span></span>

### <a name="related-topics"></a><span data-ttu-id="0e4d0-124">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="0e4d0-124">Related topics</span></span>

[<span data-ttu-id="0e4d0-125">setProgress</span><span class="sxs-lookup"><span data-stu-id="0e4d0-125">setProgress</span></span>](setprogress.md)

[<span data-ttu-id="0e4d0-126">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="0e4d0-126">formContext.data.process</span></span>](../../formContext-data-process.md)