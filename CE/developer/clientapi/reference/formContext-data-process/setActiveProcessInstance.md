---
title: setActiveProcessInstance (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c01a9445-00b6-4152-a482-df830f91a3ea
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 26492510b322dae7ad8edca1639c7ac19615d78f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387336"
---
# <a name="setactiveprocessinstance-client-api-reference"></a><span data-ttu-id="8f79b-102">setActiveProcessInstance (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="8f79b-102">setActiveProcessInstance (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setActiveProcessInstance-description.md](./includes/setActiveProcessInstance-description.md)]

## <a name="syntax"></a><span data-ttu-id="8f79b-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="8f79b-103">Syntax</span></span>

`formContext.data.process.setActiveProcessInstance(processInstanceId, callbackFunction);`

## <a name="parameter"></a><span data-ttu-id="8f79b-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="8f79b-104">Parameter</span></span>

|<span data-ttu-id="8f79b-105">Tên</span><span class="sxs-lookup"><span data-stu-id="8f79b-105">Name</span></span>|<span data-ttu-id="8f79b-106">Loại</span><span class="sxs-lookup"><span data-stu-id="8f79b-106">Type</span></span>|<span data-ttu-id="8f79b-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="8f79b-107">Required</span></span>|<span data-ttu-id="8f79b-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="8f79b-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="8f79b-109">processInstanceId</span><span class="sxs-lookup"><span data-stu-id="8f79b-109">processInstanceId</span></span>|<span data-ttu-id="8f79b-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="8f79b-110">String</span></span>|<span data-ttu-id="8f79b-111">Có</span><span class="sxs-lookup"><span data-stu-id="8f79b-111">Yes</span></span>|<span data-ttu-id="8f79b-112">The Id of the process instance to set as the active instance.</span><span class="sxs-lookup"><span data-stu-id="8f79b-112">The Id of the process instance to set as the active instance.</span></span>|
|<span data-ttu-id="8f79b-113">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="8f79b-113">callbackFunction</span></span>|<span data-ttu-id="8f79b-114">Hàm</span><span class="sxs-lookup"><span data-stu-id="8f79b-114">Function</span></span>|<span data-ttu-id="8f79b-115">Không</span><span class="sxs-lookup"><span data-stu-id="8f79b-115">No</span></span>|<span data-ttu-id="8f79b-116">A function to call when the operation is complete.</span><span class="sxs-lookup"><span data-stu-id="8f79b-116">A function to call when the operation is complete.</span></span> <span data-ttu-id="8f79b-117">This callback function is passed one of the following string values to indicate whether the operation succeeded:</span><span class="sxs-lookup"><span data-stu-id="8f79b-117">This callback function is passed one of the following string values to indicate whether the operation succeeded:</span></span><br/><span data-ttu-id="8f79b-118">- **success**: The operation succeeded.</span><span class="sxs-lookup"><span data-stu-id="8f79b-118">- **success**: The operation succeeded.</span></span><br/><span data-ttu-id="8f79b-119">- **invalid**: The processInstanceId isn’t valid or the process isn’t enabled.</span><span class="sxs-lookup"><span data-stu-id="8f79b-119">- **invalid**: The processInstanceId isn’t valid or the process isn’t enabled.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="8f79b-120">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="8f79b-120">Related topics</span></span>

[<span data-ttu-id="8f79b-121">getProcessInstances</span><span class="sxs-lookup"><span data-stu-id="8f79b-121">getProcessInstances</span></span>](getProcessInstances.md)

[<span data-ttu-id="8f79b-122">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="8f79b-122">formContext.data.process</span></span>](../formContext-data-process.md)
 


