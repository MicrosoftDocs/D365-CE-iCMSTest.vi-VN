---
title: getAttribute (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9ef1c886-a0b8-4ba9-bb9f-e6ecfa9d6dff
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fe690beea6321eabb7cd4ee07ed701022abd4435
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388705"
---
# <a name="getattribute-client-api-reference"></a><span data-ttu-id="c0a23-102">getAttribute (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="c0a23-102">getAttribute (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c0a23-103">Returns a string value that represents the type of attribute.</span><span class="sxs-lookup"><span data-stu-id="c0a23-103">Returns a string value that represents the type of attribute.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="c0a23-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="c0a23-104">Attribute types supported</span></span>

<span data-ttu-id="c0a23-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="c0a23-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a23-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="c0a23-106">Syntax</span></span>

`formContext.getAttribute(arg).getAttributeType()`

## <a name="return-value"></a><span data-ttu-id="c0a23-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="c0a23-107">Return Value</span></span>

<span data-ttu-id="c0a23-108">This method will return one of the following **string** values:</span><span class="sxs-lookup"><span data-stu-id="c0a23-108">This method will return one of the following **string** values:</span></span>

- <span data-ttu-id="c0a23-109">boolean</span><span class="sxs-lookup"><span data-stu-id="c0a23-109">boolean</span></span>
- <span data-ttu-id="c0a23-110">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="c0a23-110">datetime</span></span>
- <span data-ttu-id="c0a23-111">thập phân</span><span class="sxs-lookup"><span data-stu-id="c0a23-111">decimal</span></span>
- <span data-ttu-id="c0a23-112">double</span><span class="sxs-lookup"><span data-stu-id="c0a23-112">double</span></span>
- <span data-ttu-id="c0a23-113">số nguyên</span><span class="sxs-lookup"><span data-stu-id="c0a23-113">integer</span></span>
- <span data-ttu-id="c0a23-114">lookup</span><span class="sxs-lookup"><span data-stu-id="c0a23-114">lookup</span></span>
- <span data-ttu-id="c0a23-115">memo</span><span class="sxs-lookup"><span data-stu-id="c0a23-115">memo</span></span>
- <span data-ttu-id="c0a23-116">money</span><span class="sxs-lookup"><span data-stu-id="c0a23-116">money</span></span>
- <span data-ttu-id="c0a23-117">multioptionset</span><span class="sxs-lookup"><span data-stu-id="c0a23-117">multioptionset</span></span>
- <span data-ttu-id="c0a23-118">optionset</span><span class="sxs-lookup"><span data-stu-id="c0a23-118">optionset</span></span>
- <span data-ttu-id="c0a23-119">chuỗi</span><span class="sxs-lookup"><span data-stu-id="c0a23-119">string</span></span>
