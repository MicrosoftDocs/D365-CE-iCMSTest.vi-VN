---
title: setPrecision (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 580aebec-c1d1-4e4a-8c20-ced859569fb2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ddb7a8f0b9aad91f402808ae7bf60945083ada0a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387117"
---
# <a name="setprecision-client-api-reference"></a><span data-ttu-id="6d04b-102">setPrecision (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="6d04b-102">setPrecision (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6d04b-103">Sets the number of digits allowed to the right of the decimal point.</span><span class="sxs-lookup"><span data-stu-id="6d04b-103">Sets the number of digits allowed to the right of the decimal point.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="6d04b-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="6d04b-104">Attribute types supported</span></span>

<span data-ttu-id="6d04b-105">Money, decimal, double, and integer</span><span class="sxs-lookup"><span data-stu-id="6d04b-105">Money, decimal, double, and integer</span></span>

## <a name="syntax"></a><span data-ttu-id="6d04b-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6d04b-106">Syntax</span></span>

`formContext.getAttribute(arg).setPrecision(value);`

## <a name="parameter"></a><span data-ttu-id="6d04b-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="6d04b-107">Parameter</span></span>

 <span data-ttu-id="6d04b-108">Parameter Name</span><span class="sxs-lookup"><span data-stu-id="6d04b-108">Parameter Name</span></span>| <span data-ttu-id="6d04b-109">Loại</span><span class="sxs-lookup"><span data-stu-id="6d04b-109">Type</span></span>| <span data-ttu-id="6d04b-110">Mô tả</span><span class="sxs-lookup"><span data-stu-id="6d04b-110">Description</span></span>  |
| --------|-----------| -----|
|<span data-ttu-id="6d04b-111">giá trị</span><span class="sxs-lookup"><span data-stu-id="6d04b-111">value</span></span>| <span data-ttu-id="6d04b-112">Số</span><span class="sxs-lookup"><span data-stu-id="6d04b-112">Number</span></span>| <span data-ttu-id="6d04b-113">Number of digits allowed to the right of the decimal point.</span><span class="sxs-lookup"><span data-stu-id="6d04b-113">Number of digits allowed to the right of the decimal point.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="6d04b-114">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="6d04b-114">Related topics</span></span>

[<span data-ttu-id="6d04b-115">getPrecision</span><span class="sxs-lookup"><span data-stu-id="6d04b-115">getPrecision</span></span>](getPrecision.md)

