---
title: showProgressIndicator (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 36e17a06-e381-4efd-b3a6-62391377b613
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 13a0367cf963552731f3ac0924328acab9bfe73f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385782"
---
# <a name="showprogressindicator-client-api-reference"></a><span data-ttu-id="22512-102">showProgressIndicator (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="22512-102">showProgressIndicator (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/showProgressIndicator-description.md](./includes/showProgressIndicator-description.md)]

<span data-ttu-id="22512-103">Any subsequent call to this method will update the displayed message in the existing progress dialog with the message specified in the latest method call.</span><span class="sxs-lookup"><span data-stu-id="22512-103">Any subsequent call to this method will update the displayed message in the existing progress dialog with the message specified in the latest method call.</span></span>

>[!WARNING]
><span data-ttu-id="22512-104">The progress dialog blocks the UI until it is closed using the [closeProgressIndicator](closeProgressIndicator.md) method.</span><span class="sxs-lookup"><span data-stu-id="22512-104">The progress dialog blocks the UI until it is closed using the [closeProgressIndicator](closeProgressIndicator.md) method.</span></span> <span data-ttu-id="22512-105">So, you must use this method with caution.</span><span class="sxs-lookup"><span data-stu-id="22512-105">So, you must use this method with caution.</span></span>

## <a name="syntax"></a><span data-ttu-id="22512-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="22512-106">Syntax</span></span>

`Xrm.Utility.showProgressIndicator(message)`

## <a name="parameters"></a><span data-ttu-id="22512-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="22512-107">Parameters</span></span> 

|<span data-ttu-id="22512-108">Tên</span><span class="sxs-lookup"><span data-stu-id="22512-108">Name</span></span> |<span data-ttu-id="22512-109">Loại</span><span class="sxs-lookup"><span data-stu-id="22512-109">Type</span></span> |<span data-ttu-id="22512-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="22512-110">Required</span></span> |<span data-ttu-id="22512-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="22512-111">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="22512-112">message</span><span class="sxs-lookup"><span data-stu-id="22512-112">message</span></span>|<span data-ttu-id="22512-113">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="22512-113">String</span></span>|<span data-ttu-id="22512-114">Có</span><span class="sxs-lookup"><span data-stu-id="22512-114">Yes</span></span>|<span data-ttu-id="22512-115">The message to be displayed in the progress dialog.</span><span class="sxs-lookup"><span data-stu-id="22512-115">The message to be displayed in the progress dialog.</span></span>|



### <a name="related-topics"></a><span data-ttu-id="22512-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="22512-116">Related topics</span></span>

[<span data-ttu-id="22512-117">closeProgressIndicator</span><span class="sxs-lookup"><span data-stu-id="22512-117">closeProgressIndicator</span></span>](closeProgressIndicator.md)

[<span data-ttu-id="22512-118">Xrm.Utility</span><span class="sxs-lookup"><span data-stu-id="22512-118">Xrm.Utility</span></span>](../xrm-utility.md)  



