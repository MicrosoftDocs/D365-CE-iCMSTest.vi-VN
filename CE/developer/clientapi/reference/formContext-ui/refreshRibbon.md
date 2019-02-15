---
title: refreshRibbon (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: dbd43d7b-c9b0-4ca5-943d-dd813d3bb049
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5794e54c34b8f69b1b656f4d27122efe3a6d2db0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387448"
---
# <a name="refreshribbon-client-api-reference"></a><span data-ttu-id="7e5cf-102">refreshRibbon (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="7e5cf-102">refreshRibbon (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/refreshRibbon-description.md](./includes/refreshRibbon-description.md)]

## <a name="syntax"></a><span data-ttu-id="7e5cf-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="7e5cf-103">Syntax</span></span>

`formContext.ui.refreshRibbon(refreshAll);`

## <a name="parameter"></a><span data-ttu-id="7e5cf-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="7e5cf-104">Parameter</span></span>

|<span data-ttu-id="7e5cf-105">Tên</span><span class="sxs-lookup"><span data-stu-id="7e5cf-105">Name</span></span>|<span data-ttu-id="7e5cf-106">Loại</span><span class="sxs-lookup"><span data-stu-id="7e5cf-106">Type</span></span>|<span data-ttu-id="7e5cf-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="7e5cf-107">Required</span></span>|<span data-ttu-id="7e5cf-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="7e5cf-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="7e5cf-109">refreshAll</span><span class="sxs-lookup"><span data-stu-id="7e5cf-109">refreshAll</span></span>|<span data-ttu-id="7e5cf-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="7e5cf-110">Boolean</span></span>|<span data-ttu-id="7e5cf-111">Không</span><span class="sxs-lookup"><span data-stu-id="7e5cf-111">No</span></span>|<span data-ttu-id="7e5cf-112">Indicates whether all the ribbon command bars on the current page are refreshed.</span><span class="sxs-lookup"><span data-stu-id="7e5cf-112">Indicates whether all the ribbon command bars on the current page are refreshed.</span></span> <span data-ttu-id="7e5cf-113">If you specify **false**, only the page-level ribbon command bar is refreshed.</span><span class="sxs-lookup"><span data-stu-id="7e5cf-113">If you specify **false**, only the page-level ribbon command bar is refreshed.</span></span> <span data-ttu-id="7e5cf-114">If you do not specify this parameter, by default **false** is passed.</span><span class="sxs-lookup"><span data-stu-id="7e5cf-114">If you do not specify this parameter, by default **false** is passed.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7e5cf-115">Chú thích</span><span class="sxs-lookup"><span data-stu-id="7e5cf-115">Remarks</span></span>

 <span data-ttu-id="7e5cf-116">This function is typically used when a ribbon <EnableRule> (RibbonDiffXml) depends on a value in the form.</span><span class="sxs-lookup"><span data-stu-id="7e5cf-116">This function is typically used when a ribbon <EnableRule> (RibbonDiffXml) depends on a value in the form.</span></span> <span data-ttu-id="7e5cf-117">After your code changes a value that is used by a rule, use this method to force the ribbon to re-evaluate the data in the form so that the rule can be applied.</span><span class="sxs-lookup"><span data-stu-id="7e5cf-117">After your code changes a value that is used by a rule, use this method to force the ribbon to re-evaluate the data in the form so that the rule can be applied.</span></span>

### <a name="related-topics"></a><span data-ttu-id="7e5cf-118">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="7e5cf-118">Related topics</span></span>

[<span data-ttu-id="7e5cf-119">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="7e5cf-119">formContext.ui</span></span>](../formContext-ui.md)

[<span data-ttu-id="7e5cf-120">formContext</span><span class="sxs-lookup"><span data-stu-id="7e5cf-120">formContext</span></span>](../../clientapi-form-context.md)

