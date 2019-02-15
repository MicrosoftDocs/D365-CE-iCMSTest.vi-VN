---
title: reflow (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 6833e4ea-70fc-4ee0-8aab-68cc55e21444
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 82b50e5d5fe2803c4115bb4658863caa72020779
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388592"
---
# <a name="reflow-client-api-reference"></a><span data-ttu-id="68c1d-102">reflow (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="68c1d-102">reflow (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/reflow-description.md](./includes/reflow-description.md)]

## <a name="syntax"></a><span data-ttu-id="68c1d-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="68c1d-103">Syntax</span></span>

`formContext.ui.process.reflow(updateUI, parentStage, nextStage);`

## <a name="parameter"></a><span data-ttu-id="68c1d-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="68c1d-104">Parameter</span></span>

|<span data-ttu-id="68c1d-105">Tên</span><span class="sxs-lookup"><span data-stu-id="68c1d-105">Name</span></span>|<span data-ttu-id="68c1d-106">Loại</span><span class="sxs-lookup"><span data-stu-id="68c1d-106">Type</span></span>|<span data-ttu-id="68c1d-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="68c1d-107">Required</span></span>|<span data-ttu-id="68c1d-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="68c1d-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="68c1d-109">updateUI</span><span class="sxs-lookup"><span data-stu-id="68c1d-109">updateUI</span></span>|<span data-ttu-id="68c1d-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="68c1d-110">Boolean</span></span>|<span data-ttu-id="68c1d-111">Có</span><span class="sxs-lookup"><span data-stu-id="68c1d-111">Yes</span></span>|<span data-ttu-id="68c1d-112">Specify **true** to update the UI of the process control; **false** otherwise.</span><span class="sxs-lookup"><span data-stu-id="68c1d-112">Specify **true** to update the UI of the process control; **false** otherwise.</span></span>|
|<span data-ttu-id="68c1d-113">parentStage</span><span class="sxs-lookup"><span data-stu-id="68c1d-113">parentStage</span></span>|<span data-ttu-id="68c1d-114">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="68c1d-114">String</span></span>|<span data-ttu-id="68c1d-115">Có</span><span class="sxs-lookup"><span data-stu-id="68c1d-115">Yes</span></span>|<span data-ttu-id="68c1d-116">Specify the ID of the parent stage in the GUID format.</span><span class="sxs-lookup"><span data-stu-id="68c1d-116">Specify the ID of the parent stage in the GUID format.</span></span>|
|<span data-ttu-id="68c1d-117">nextStage</span><span class="sxs-lookup"><span data-stu-id="68c1d-117">nextStage</span></span>|<span data-ttu-id="68c1d-118">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="68c1d-118">String</span></span>|<span data-ttu-id="68c1d-119">Có</span><span class="sxs-lookup"><span data-stu-id="68c1d-119">Yes</span></span>|<span data-ttu-id="68c1d-120">Specify the ID of the next stage in the GUID format.</span><span class="sxs-lookup"><span data-stu-id="68c1d-120">Specify the ID of the next stage in the GUID format.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="68c1d-121">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="68c1d-121">Related topics</span></span>

[<span data-ttu-id="68c1d-122">formContext.ui.process</span><span class="sxs-lookup"><span data-stu-id="68c1d-122">formContext.ui.process</span></span>](../formContext-ui-process.md)



