---
title: getValue (Client API reference)| MicrosoftDocs
ms.date: 10/16/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: acc78a1e-212a-4eef-88c5-8272f9ba3009
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9f25e7cc1b72c58dd02985652e533cc2c9c7bd5d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387229"
---
# <a name="getvalue-client-api-reference"></a><span data-ttu-id="59f36-102">getValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="59f36-102">getValue (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="59f36-103">Retrieves the data value for an attribute.</span><span class="sxs-lookup"><span data-stu-id="59f36-103">Retrieves the data value for an attribute.</span></span>

## <a name="attribute-types-supported"></a><span data-ttu-id="59f36-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="59f36-104">Attribute types supported</span></span>

<span data-ttu-id="59f36-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="59f36-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="59f36-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="59f36-106">Syntax</span></span>

`formContext.getAttribute(arg).getValue()`

## <a name="return-value"></a><span data-ttu-id="59f36-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="59f36-107">Return Value</span></span>

<span data-ttu-id="59f36-108">**Type**: Depends on the type of attaribute.</span><span class="sxs-lookup"><span data-stu-id="59f36-108">**Type**: Depends on the type of attaribute.</span></span> 

| <span data-ttu-id="59f36-109">Attribute Type</span><span class="sxs-lookup"><span data-stu-id="59f36-109">Attribute Type</span></span> | <span data-ttu-id="59f36-110">Return Type</span><span class="sxs-lookup"><span data-stu-id="59f36-110">Return Type</span></span>| 
|----|-----|
| <span data-ttu-id="59f36-111">boolean</span><span class="sxs-lookup"><span data-stu-id="59f36-111">boolean</span></span> | [<span data-ttu-id="59f36-112">Boolean</span><span class="sxs-lookup"><span data-stu-id="59f36-112">Boolean</span></span>](https://msdn.microsoft.com/library/t7bkhaz6.aspx) |
| <span data-ttu-id="59f36-113">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="59f36-113">datetime</span></span>| [<span data-ttu-id="59f36-114">Date</span><span class="sxs-lookup"><span data-stu-id="59f36-114">Date</span></span>](https://msdn.microsoft.com/library/cd9w2te4.aspx)<br/> <span data-ttu-id="59f36-115">To get the string version of a date using the Microsoft Dynamics 365 for Customer Engagement app user’s locale preferences, use the [format](https://msdn.microsoft.com/library/bb384009.aspx) and [localeFormat](https://msdn.microsoft.com/library/bb383816.aspx) methods.</span><span class="sxs-lookup"><span data-stu-id="59f36-115">To get the string version of a date using the Microsoft Dynamics 365 for Customer Engagement app user’s locale preferences, use the [format](https://msdn.microsoft.com/library/bb384009.aspx) and [localeFormat](https://msdn.microsoft.com/library/bb383816.aspx) methods.</span></span> <span data-ttu-id="59f36-116">Other methods will format dates using the operating system locale rather than the user’s Microsoft Dynamics 365 for Customer Engagement apps locale preferences.</span><span class="sxs-lookup"><span data-stu-id="59f36-116">Other methods will format dates using the operating system locale rather than the user’s Microsoft Dynamics 365 for Customer Engagement apps locale preferences.</span></span> | 
| <span data-ttu-id="59f36-117">thập phân</span><span class="sxs-lookup"><span data-stu-id="59f36-117">decimal</span></span>| [<span data-ttu-id="59f36-118">Number</span><span class="sxs-lookup"><span data-stu-id="59f36-118">Number</span></span>](https://msdn.microsoft.com/library/dwab3ed2.aspx)| 
| <span data-ttu-id="59f36-119">Gấp đôi</span><span class="sxs-lookup"><span data-stu-id="59f36-119">Double</span></span> | [<span data-ttu-id="59f36-120">Number</span><span class="sxs-lookup"><span data-stu-id="59f36-120">Number</span></span>](https://msdn.microsoft.com/library/dwab3ed2.aspx)| 
| <span data-ttu-id="59f36-121">số nguyên</span><span class="sxs-lookup"><span data-stu-id="59f36-121">integer</span></span> | [<span data-ttu-id="59f36-122">Number</span><span class="sxs-lookup"><span data-stu-id="59f36-122">Number</span></span>](https://msdn.microsoft.com/library/dwab3ed2.aspx)|
| <span data-ttu-id="59f36-123">lookup</span><span class="sxs-lookup"><span data-stu-id="59f36-123">lookup</span></span> | [<span data-ttu-id="59f36-124">Mảng</span><span class="sxs-lookup"><span data-stu-id="59f36-124">Array</span></span>](https://msdn.microsoft.com/library/k4h76zbx.aspx) <br/><span data-ttu-id="59f36-125">An array of lookup objects.</span><span class="sxs-lookup"><span data-stu-id="59f36-125">An array of lookup objects.</span></span><br/><br/><span data-ttu-id="59f36-126">NOTE: Certain lookups allow for multiple records to be associated in a lookup, such as the To: field for an email entity record.</span><span class="sxs-lookup"><span data-stu-id="59f36-126">NOTE: Certain lookups allow for multiple records to be associated in a lookup, such as the To: field for an email entity record.</span></span> <span data-ttu-id="59f36-127">Therefore, all lookup data values use an array of lookup objects – even when the lookup attribute does not support more than one record reference to be added.</span><span class="sxs-lookup"><span data-stu-id="59f36-127">Therefore, all lookup data values use an array of lookup objects – even when the lookup attribute does not support more than one record reference to be added.</span></span> <br/><br/><span data-ttu-id="59f36-128">Each lookup has the following properties:</span><span class="sxs-lookup"><span data-stu-id="59f36-128">Each lookup has the following properties:</span></span><br/><span data-ttu-id="59f36-129">- *entityType*: String.</span><span class="sxs-lookup"><span data-stu-id="59f36-129">- *entityType*: String.</span></span> <span data-ttu-id="59f36-130">The name of the entity displayed in the lookup.</span><span class="sxs-lookup"><span data-stu-id="59f36-130">The name of the entity displayed in the lookup.</span></span><br/><span data-ttu-id="59f36-131">- *id*: String: The string representation of the GUID value for the record displayed in the lookup.</span><span class="sxs-lookup"><span data-stu-id="59f36-131">- *id*: String: The string representation of the GUID value for the record displayed in the lookup.</span></span><br/><span data-ttu-id="59f36-132">- *name*: String: The text representing the record to be displayed in the lookup.</span><span class="sxs-lookup"><span data-stu-id="59f36-132">- *name*: String: The text representing the record to be displayed in the lookup.</span></span>|
| <span data-ttu-id="59f36-133">memo</span><span class="sxs-lookup"><span data-stu-id="59f36-133">memo</span></span>  | [<span data-ttu-id="59f36-134">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="59f36-134">String</span></span>](https://msdn.microsoft.com/library/ecczf11c.aspx)  |
| <span data-ttu-id="59f36-135">money</span><span class="sxs-lookup"><span data-stu-id="59f36-135">money</span></span>| [<span data-ttu-id="59f36-136">Number</span><span class="sxs-lookup"><span data-stu-id="59f36-136">Number</span></span>](https://msdn.microsoft.com/library/dwab3ed2.aspx)  |
| <span data-ttu-id="59f36-137">optionset</span><span class="sxs-lookup"><span data-stu-id="59f36-137">optionset</span></span> | [<span data-ttu-id="59f36-138">Number</span><span class="sxs-lookup"><span data-stu-id="59f36-138">Number</span></span>](https://msdn.microsoft.com/library/dwab3ed2.aspx)  |
| <span data-ttu-id="59f36-139">multiselectoptionset</span><span class="sxs-lookup"><span data-stu-id="59f36-139">multiselectoptionset</span></span> | <span data-ttu-id="59f36-140">Array of [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)</span><span class="sxs-lookup"><span data-stu-id="59f36-140">Array of [Number](https://msdn.microsoft.com/library/dwab3ed2.aspx)</span></span>  |
| <span data-ttu-id="59f36-141">chuỗi</span><span class="sxs-lookup"><span data-stu-id="59f36-141">string</span></span> | [<span data-ttu-id="59f36-142">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="59f36-142">String</span></span>](https://msdn.microsoft.com/library/ecczf11c.aspx) |


### <a name="related-topic"></a><span data-ttu-id="59f36-143">Related topic</span><span class="sxs-lookup"><span data-stu-id="59f36-143">Related topic</span></span>
[<span data-ttu-id="59f36-144">setValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="59f36-144">setValue (Client API reference)</span></span>](setValue.md)
