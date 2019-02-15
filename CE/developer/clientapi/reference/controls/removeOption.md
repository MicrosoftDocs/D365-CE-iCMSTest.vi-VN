---
title: removeOption (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 09fd288c-d687-4976-b708-29a466fc35b1
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: d571691e848b7aaffc2fc2f8463d3b3eec9f386e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388061"
---
# <a name="removeoption-client-api-reference"></a><span data-ttu-id="71b65-102">removeOption (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="71b65-102">removeOption (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="71b65-103">Removes an option from a control.</span><span class="sxs-lookup"><span data-stu-id="71b65-103">Removes an option from a control.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="71b65-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="71b65-104">Control types supported</span></span>

<span data-ttu-id="71b65-105">optionset, multiselectoptionset</span><span class="sxs-lookup"><span data-stu-id="71b65-105">optionset, multiselectoptionset</span></span>

## <a name="syntax"></a><span data-ttu-id="71b65-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="71b65-106">Syntax</span></span>

`formContext.getControl(arg).removeOption(value);`

## <a name="parameters"></a><span data-ttu-id="71b65-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="71b65-107">Parameters</span></span>

|<span data-ttu-id="71b65-108">Tên</span><span class="sxs-lookup"><span data-stu-id="71b65-108">Name</span></span> | <span data-ttu-id="71b65-109">Loại</span><span class="sxs-lookup"><span data-stu-id="71b65-109">Type</span></span> | <span data-ttu-id="71b65-110">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="71b65-110">Required</span></span> | <span data-ttu-id="71b65-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="71b65-111">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="71b65-112">giá trị</span><span class="sxs-lookup"><span data-stu-id="71b65-112">value</span></span> |<span data-ttu-id="71b65-113">Số</span><span class="sxs-lookup"><span data-stu-id="71b65-113">Number</span></span> |<span data-ttu-id="71b65-114">Có</span><span class="sxs-lookup"><span data-stu-id="71b65-114">Yes</span></span>|<span data-ttu-id="71b65-115">The value of the option you want to remove.</span><span class="sxs-lookup"><span data-stu-id="71b65-115">The value of the option you want to remove.</span></span>|

### <a name="related-topics"></a><span data-ttu-id="71b65-116">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="71b65-116">Related topics</span></span>

[<span data-ttu-id="71b65-117">addOption</span><span class="sxs-lookup"><span data-stu-id="71b65-117">addOption</span></span>](addOption.md)

[<span data-ttu-id="71b65-118">clearOptions</span><span class="sxs-lookup"><span data-stu-id="71b65-118">clearOptions</span></span>](clearOptions.md)

 


