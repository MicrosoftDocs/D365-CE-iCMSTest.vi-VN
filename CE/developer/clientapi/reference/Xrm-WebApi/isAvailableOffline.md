---
title: isAvailableOffline (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 12/18/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ea9eacc0-2e31-49f4-a329-dcdf430a5a7e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 776a21a77781ae016ea1f8a8f39c2d3ac79fded2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387506"
---
# <a name="isavailableoffline-client-api-reference"></a><span data-ttu-id="e95f4-102">isAvailableOffline (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e95f4-102">isAvailableOffline (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/isAvailableOffline-description.md](./includes/isAvailableOffline-description.md)] 

## <a name="syntax"></a><span data-ttu-id="e95f4-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e95f4-103">Syntax</span></span>

`Xrm.WebApi.offline.isAvailableOffline(entityLogicalName);`

## <a name="parameters"></a><span data-ttu-id="e95f4-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="e95f4-104">Parameters</span></span>

<table style="width:100%">
<tr>
<th><span data-ttu-id="e95f4-105">Tên</span><span class="sxs-lookup"><span data-stu-id="e95f4-105">Name</span></span></th>
<th><span data-ttu-id="e95f4-106">Loại</span><span class="sxs-lookup"><span data-stu-id="e95f4-106">Type</span></span></th>
<th><span data-ttu-id="e95f4-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="e95f4-107">Required</span></span></th>
<th><span data-ttu-id="e95f4-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="e95f4-108">Description</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="e95f4-109">entityLogicalName</span><span class="sxs-lookup"><span data-stu-id="e95f4-109">entityLogicalName</span></span></td>
<td><span data-ttu-id="e95f4-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="e95f4-110">String</span></span></td>
<td><span data-ttu-id="e95f4-111">Có</span><span class="sxs-lookup"><span data-stu-id="e95f4-111">Yes</span></span></td>
<td><span data-ttu-id="e95f4-112">Logical name of the entity.</span><span class="sxs-lookup"><span data-stu-id="e95f4-112">Logical name of the entity.</span></span> <span data-ttu-id="e95f4-113">For example: &quot;account&quot;.</span><span class="sxs-lookup"><span data-stu-id="e95f4-113">For example: &quot;account&quot;.</span></span></td>
</tr>

</table>

## <a name="return-value"></a><span data-ttu-id="e95f4-114">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="e95f4-114">Return Value</span></span>

<span data-ttu-id="e95f4-115">**Type**: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e95f4-115">**Type**: Boolean.</span></span>

<span data-ttu-id="e95f4-116">**Description**: true if the entity is present in user’s profile and is currently available for use in offline mode; otherwise false.</span><span class="sxs-lookup"><span data-stu-id="e95f4-116">**Description**: true if the entity is present in user’s profile and is currently available for use in offline mode; otherwise false.</span></span>

[<span data-ttu-id="e95f4-117">Xrm.WebApi.offline</span><span class="sxs-lookup"><span data-stu-id="e95f4-117">Xrm.WebApi.offline</span></span>](offline.md)

[<span data-ttu-id="e95f4-118">Xrm.WebApi</span><span class="sxs-lookup"><span data-stu-id="e95f4-118">Xrm.WebApi</span></span>](../xrm-webapi.md)




