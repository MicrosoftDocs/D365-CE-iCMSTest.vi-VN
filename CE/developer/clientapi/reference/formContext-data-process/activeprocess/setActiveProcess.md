---
title: setActiveProcess (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0d4c2d8a-a2fb-4cdd-9153-041646068992
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9f6cfd47887dae13464a0563680aa78c16d82275
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386243"
---
# <a name="setactiveprocess-client-api-reference"></a><span data-ttu-id="04391-102">setActiveProcess (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="04391-102">setActiveProcess (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setActiveProcess-description.md](./includes/setActiveProcess-description.md)]

<span data-ttu-id="04391-103">If there is an active instance of the process, the entity record is loaded with the process instance ID.</span><span class="sxs-lookup"><span data-stu-id="04391-103">If there is an active instance of the process, the entity record is loaded with the process instance ID.</span></span> <span data-ttu-id="04391-104">If there is no active instance of the process, a new process instance is created and the entity record is loaded with the process instance ID.</span><span class="sxs-lookup"><span data-stu-id="04391-104">If there is no active instance of the process, a new process instance is created and the entity record is loaded with the process instance ID.</span></span> <span data-ttu-id="04391-105">If there are multiple instances of the current process, the record is loaded with the first instance of the active process as per the defaulting logic, that is the most recently used process instance per user.</span><span class="sxs-lookup"><span data-stu-id="04391-105">If there are multiple instances of the current process, the record is loaded with the first instance of the active process as per the defaulting logic, that is the most recently used process instance per user.</span></span>

## <a name="syntax"></a><span data-ttu-id="04391-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="04391-106">Syntax</span></span>

`formContext.data.process.setActiveProcess(processId, callbackFunction);`

## <a name="parameter"></a><span data-ttu-id="04391-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="04391-107">Parameter</span></span>

|<span data-ttu-id="04391-108">Tên</span><span class="sxs-lookup"><span data-stu-id="04391-108">Name</span></span>|<span data-ttu-id="04391-109">Loại</span><span class="sxs-lookup"><span data-stu-id="04391-109">Type</span></span>|<span data-ttu-id="04391-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="04391-110">Required</span></span>|<span data-ttu-id="04391-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="04391-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="04391-112">processInstanceId</span><span class="sxs-lookup"><span data-stu-id="04391-112">processInstanceId</span></span>|<span data-ttu-id="04391-113">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="04391-113">String</span></span>|<span data-ttu-id="04391-114">Có</span><span class="sxs-lookup"><span data-stu-id="04391-114">Yes</span></span>|<span data-ttu-id="04391-115">The Id of the process to set as the active process.</span><span class="sxs-lookup"><span data-stu-id="04391-115">The Id of the process to set as the active process.</span></span>|
|<span data-ttu-id="04391-116">callbackFunction</span><span class="sxs-lookup"><span data-stu-id="04391-116">callbackFunction</span></span>|<span data-ttu-id="04391-117">Hàm</span><span class="sxs-lookup"><span data-stu-id="04391-117">Function</span></span>|<span data-ttu-id="04391-118">Không</span><span class="sxs-lookup"><span data-stu-id="04391-118">No</span></span>|<span data-ttu-id="04391-119">A function to call when the operation is complete.</span><span class="sxs-lookup"><span data-stu-id="04391-119">A function to call when the operation is complete.</span></span> <span data-ttu-id="04391-120">This callback function is passed one of the following string values to indicate whether the operation succeeded:</span><span class="sxs-lookup"><span data-stu-id="04391-120">This callback function is passed one of the following string values to indicate whether the operation succeeded:</span></span><br/><span data-ttu-id="04391-121">- **success**: The operation succeeded.</span><span class="sxs-lookup"><span data-stu-id="04391-121">- **success**: The operation succeeded.</span></span><br/><span data-ttu-id="04391-122">- **invalid**: The processId isn’t valid or the process isn’t enabled.</span><span class="sxs-lookup"><span data-stu-id="04391-122">- **invalid**: The processId isn’t valid or the process isn’t enabled.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="04391-123">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="04391-123">Related topics</span></span>

[<span data-ttu-id="04391-124">getActiveProcess</span><span class="sxs-lookup"><span data-stu-id="04391-124">getActiveProcess</span></span>](getActiveProcess.md)

[<span data-ttu-id="04391-125">setActiveProcessInstance</span><span class="sxs-lookup"><span data-stu-id="04391-125">setActiveProcessInstance</span></span>](../setActiveProcessInstance.md)

[<span data-ttu-id="04391-126">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="04391-126">formContext.data.process</span></span>](../../formContext-data-process.md)
 


