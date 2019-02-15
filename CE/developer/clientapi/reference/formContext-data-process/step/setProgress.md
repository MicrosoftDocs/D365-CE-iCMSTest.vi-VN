---
title: setProgress (Client API reference) in Dynamics 365 for Customer Engagement apps| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ac2881feaf964219e17243887c3dea9520898caa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387541"
---
# <a name="setprogress-client-api-reference"></a><span data-ttu-id="ba8af-102">setProgress (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="ba8af-102">setProgress (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setProgress-description.md](./includes/setProgress-description.md)]

## <a name="syntax"></a><span data-ttu-id="ba8af-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="ba8af-103">Syntax</span></span>

`stepObj.setProgress(stepProgress,message);`

## <a name="parameters"></a><span data-ttu-id="ba8af-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="ba8af-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="ba8af-105">Tên</span><span class="sxs-lookup"><span data-stu-id="ba8af-105">Name</span></span></th>
<th><span data-ttu-id="ba8af-106">Loại</span><span class="sxs-lookup"><span data-stu-id="ba8af-106">Type</span></span></th>
<th><span data-ttu-id="ba8af-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="ba8af-107">Required</span></span></th>
<th><span data-ttu-id="ba8af-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ba8af-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="ba8af-109">stepProgress</span><span class="sxs-lookup"><span data-stu-id="ba8af-109">stepProgress</span></span></td>
<td><span data-ttu-id="ba8af-110">Số</span><span class="sxs-lookup"><span data-stu-id="ba8af-110">Number</span></span></td>
<td><span data-ttu-id="ba8af-111">Có</span><span class="sxs-lookup"><span data-stu-id="ba8af-111">Yes</span></span></td>
<td><span data-ttu-id="ba8af-112">Specify one of the following values to specify the step progress:</span><span class="sxs-lookup"><span data-stu-id="ba8af-112">Specify one of the following values to specify the step progress:</span></span>
<ul>
<li><span data-ttu-id="ba8af-113">0: None</span><span class="sxs-lookup"><span data-stu-id="ba8af-113">0: None</span></span></li>
<li><span data-ttu-id="ba8af-114">1: Processing</span><span class="sxs-lookup"><span data-stu-id="ba8af-114">1: Processing</span></span></li>
<li><span data-ttu-id="ba8af-115">2: Đã hoàn thành</span><span class="sxs-lookup"><span data-stu-id="ba8af-115">2: Completed</span></span></li>
<li><span data-ttu-id="ba8af-116">3: Failure</span><span class="sxs-lookup"><span data-stu-id="ba8af-116">3: Failure</span></span></li>
<li><span data-ttu-id="ba8af-117">4: Invalid</span><span class="sxs-lookup"><span data-stu-id="ba8af-117">4: Invalid</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ba8af-118">message</span><span class="sxs-lookup"><span data-stu-id="ba8af-118">message</span></span></td>
<td><span data-ttu-id="ba8af-119">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="ba8af-119">String</span></span></td>
<td><span data-ttu-id="ba8af-120">Không</span><span class="sxs-lookup"><span data-stu-id="ba8af-120">No</span></span></td>
<td><p><span data-ttu-id="ba8af-121">An optional message that is set as the Alt text on the icon for the step.</span><span class="sxs-lookup"><span data-stu-id="ba8af-121">An optional message that is set as the Alt text on the icon for the step.</span></span></td>
</tr>
</table>


## <a name="return-value"></a><span data-ttu-id="ba8af-122">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="ba8af-122">Return Value</span></span>

<span data-ttu-id="ba8af-123">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="ba8af-123">**Type**: String.</span></span> 

<span data-ttu-id="ba8af-124">**Description**: Returns "invalid" or "success" depending on whether the step progress was updated.</span><span class="sxs-lookup"><span data-stu-id="ba8af-124">**Description**: Returns "invalid" or "success" depending on whether the step progress was updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8af-125">Chú thích</span><span class="sxs-lookup"><span data-stu-id="ba8af-125">Remarks</span></span>

<span data-ttu-id="ba8af-126">This method is supported only for the action steps.</span><span class="sxs-lookup"><span data-stu-id="ba8af-126">This method is supported only for the action steps.</span></span> <span data-ttu-id="ba8af-127">Action steps are buttons on the business process stages that users can click to trigger an on-demand workflow or action.</span><span class="sxs-lookup"><span data-stu-id="ba8af-127">Action steps are buttons on the business process stages that users can click to trigger an on-demand workflow or action.</span></span> <span data-ttu-id="ba8af-128">Action step is a preview feature introduced in the [!INCLUDE[pn_crm_9_0_0_online](../../../../../includes/pn-crm-9-0-0-online.md)] release.</span><span class="sxs-lookup"><span data-stu-id="ba8af-128">Action step is a preview feature introduced in the [!INCLUDE[pn_crm_9_0_0_online](../../../../../includes/pn-crm-9-0-0-online.md)] release.</span></span> <span data-ttu-id="ba8af-129">Thông tin khác: Xem phần **Tự động hóa Dòng quy trình Công việc qua Các bước Hành động** trong [Blog: Các tính năng trực quan hóa và tự động hóa dành cho Dòng Quy trình Công việc (bản xem trước công khai)](https://blogs.msdn.microsoft.com/crm/2017/10/25/new-automation-and-visualization-features-for-business-process-flows-public-preview/).</span><span class="sxs-lookup"><span data-stu-id="ba8af-129">More information: See the **Business Process Flow automation with Action Steps** section in [Blog: New automation and visualization features for Business Process Flows (public preview)](https://blogs.msdn.microsoft.com/crm/2017/10/25/new-automation-and-visualization-features-for-business-process-flows-public-preview/).</span></span>

### <a name="related-topics"></a><span data-ttu-id="ba8af-130">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="ba8af-130">Related topics</span></span>

[<span data-ttu-id="ba8af-131">getProgress</span><span class="sxs-lookup"><span data-stu-id="ba8af-131">getProgress</span></span>](getprogress.md)
 
[<span data-ttu-id="ba8af-132">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="ba8af-132">formContext.data.process</span></span>](../../formContext-data-process.md)

