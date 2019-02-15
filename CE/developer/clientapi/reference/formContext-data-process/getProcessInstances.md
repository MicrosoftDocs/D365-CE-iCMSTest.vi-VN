---
title: getProcessInstances (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 12/04/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4ed6c991-59c9-4a69-90d4-635f3f1d397b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4e876e591eb117ebbb5beb937328456e5d29bfb2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387689"
---
# <a name="getprocessinstances-client-api-reference"></a><span data-ttu-id="812b7-102">getProcessInstances (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="812b7-102">getProcessInstances (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getProcessInstances-description.md](./includes/getProcessInstances-description.md)]

## <a name="syntax"></a><span data-ttu-id="812b7-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="812b7-103">Syntax</span></span>

`formContext.data.process.getProcessInstances(callbackFunction(object));`

## <a name="parameter"></a><span data-ttu-id="812b7-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="812b7-104">Parameter</span></span>

|<span data-ttu-id="812b7-105">Tên</span><span class="sxs-lookup"><span data-stu-id="812b7-105">Name</span></span>|<span data-ttu-id="812b7-106">Loại</span><span class="sxs-lookup"><span data-stu-id="812b7-106">Type</span></span>|<span data-ttu-id="812b7-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="812b7-107">Required</span></span>|<span data-ttu-id="812b7-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="812b7-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="812b7-109">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="812b7-109">callbackFunction</span></span>|<span data-ttu-id="812b7-110">Hàm</span><span class="sxs-lookup"><span data-stu-id="812b7-110">Function</span></span>|<span data-ttu-id="812b7-111">Có</span><span class="sxs-lookup"><span data-stu-id="812b7-111">Yes</span></span>|<span data-ttu-id="812b7-112">The callback function is passed an object with the following attributes and their corresponding values as the key: value pair.</span><span class="sxs-lookup"><span data-stu-id="812b7-112">The callback function is passed an object with the following attributes and their corresponding values as the key: value pair.</span></span> <span data-ttu-id="812b7-113">All returned values are of String type except for **CreatedOnDate**, which is of [Date](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date) type.</span><span class="sxs-lookup"><span data-stu-id="812b7-113">All returned values are of String type except for **CreatedOnDate**, which is of [Date](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date) type.</span></span> <br/><span data-ttu-id="812b7-114">- CreatedOn (deprecated)</span><span class="sxs-lookup"><span data-stu-id="812b7-114">- CreatedOn (deprecated)</span></span><br/><span data-ttu-id="812b7-115">- CreatedOnDate</span><span class="sxs-lookup"><span data-stu-id="812b7-115">- CreatedOnDate</span></span><br/><span data-ttu-id="812b7-116">- ProcessDefinitionID</span><span class="sxs-lookup"><span data-stu-id="812b7-116">- ProcessDefinitionID</span></span><br/><span data-ttu-id="812b7-117">- ProcessDefinitionName</span><span class="sxs-lookup"><span data-stu-id="812b7-117">- ProcessDefinitionName</span></span><br/><span data-ttu-id="812b7-118">- ProcessInstanceID</span><span class="sxs-lookup"><span data-stu-id="812b7-118">- ProcessInstanceID</span></span><br/><span data-ttu-id="812b7-119">- ProcessInstanceName</span><span class="sxs-lookup"><span data-stu-id="812b7-119">- ProcessInstanceName</span></span><br/><span data-ttu-id="812b7-120">- StatusCodeName</span><span class="sxs-lookup"><span data-stu-id="812b7-120">- StatusCodeName</span></span><br/><br/><span data-ttu-id="812b7-121">The process instances are filtered according to the user’s privileges.</span><span class="sxs-lookup"><span data-stu-id="812b7-121">The process instances are filtered according to the user’s privileges.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="812b7-122">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="812b7-122">Related topics</span></span>

[<span data-ttu-id="812b7-123">setActiveProcessInstance</span><span class="sxs-lookup"><span data-stu-id="812b7-123">setActiveProcessInstance</span></span>](setActiveProcessInstance.md)

[<span data-ttu-id="812b7-124">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="812b7-124">formContext.data.process</span></span>](../formContext-data-process.md)
 


