---
title: setSubmitMode (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d0728377-4365-4571-97af-9b99b2a39b65
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 92580ba667377f78f632a6902aff113f51722566
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388702"
---
# <a name="setsubmitmode-client-api-reference"></a><span data-ttu-id="e3b3d-102">setSubmitMode (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e3b3d-102">setSubmitMode (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e3b3d-103">Sets whether data from the attribute will be submitted when the record is saved.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-103">Sets whether data from the attribute will be submitted when the record is saved.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="e3b3d-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="e3b3d-104">Attribute types supported</span></span>

<span data-ttu-id="e3b3d-105">Tất cả</span><span class="sxs-lookup"><span data-stu-id="e3b3d-105">All</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b3d-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e3b3d-106">Syntax</span></span>

`formContext.getAttribute(arg).setSubmitMode(mode)`

## <a name="parameters"></a><span data-ttu-id="e3b3d-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="e3b3d-107">Parameters</span></span>

<span data-ttu-id="e3b3d-108">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-108">**Type**: String.</span></span> 

<span data-ttu-id="e3b3d-109">**Description**: Set one of the following mode values:</span><span class="sxs-lookup"><span data-stu-id="e3b3d-109">**Description**: Set one of the following mode values:</span></span>
- <span data-ttu-id="e3b3d-110">**always**: The data is always sent with a save.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-110">**always**: The data is always sent with a save.</span></span>
- <span data-ttu-id="e3b3d-111">**never**: The data is never sent with a save.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-111">**never**: The data is never sent with a save.</span></span> <span data-ttu-id="e3b3d-112">When this is used, the field(s) in the form for this attribute cannot be edited.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-112">When this is used, the field(s) in the form for this attribute cannot be edited.</span></span>
- <span data-ttu-id="e3b3d-113">**dirty**: Default behavior.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-113">**dirty**: Default behavior.</span></span> <span data-ttu-id="e3b3d-114">The data is sent with the save when it has changed.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-114">The data is sent with the save when it has changed.</span></span>
 
## <a name="remarks"></a><span data-ttu-id="e3b3d-115">Chú thích</span><span class="sxs-lookup"><span data-stu-id="e3b3d-115">Remarks</span></span>
<span data-ttu-id="e3b3d-116">Use this method to control when data for an attribute is submitted when a record is created or saved.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-116">Use this method to control when data for an attribute is submitted when a record is created or saved.</span></span> <span data-ttu-id="e3b3d-117">For example, you may have a field on the form which is only intended to control logic in the form.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-117">For example, you may have a field on the form which is only intended to control logic in the form.</span></span> <span data-ttu-id="e3b3d-118">You are not interested in capturing the data in it.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-118">You are not interested in capturing the data in it.</span></span> <span data-ttu-id="e3b3d-119">You might set it so that the data is not saved.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-119">You might set it so that the data is not saved.</span></span> <span data-ttu-id="e3b3d-120">Or you may have a Plugin that depends on the value always being included.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-120">Or you may have a Plugin that depends on the value always being included.</span></span> <span data-ttu-id="e3b3d-121">You may want to set the attribute so that it will always be included.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-121">You may want to set the attribute so that it will always be included.</span></span> 

<span data-ttu-id="e3b3d-122">Attributes that do not get updated after the initial save of the record, such as **createdby**, are set so that they will not be submitted on save.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-122">Attributes that do not get updated after the initial save of the record, such as **createdby**, are set so that they will not be submitted on save.</span></span> <span data-ttu-id="e3b3d-123">To force an attribute value to be submitted whether it has changed or not, use this method with the *mode* parameter set to “always”.</span><span class="sxs-lookup"><span data-stu-id="e3b3d-123">To force an attribute value to be submitted whether it has changed or not, use this method with the *mode* parameter set to “always”.</span></span>

### <a name="related-topic"></a><span data-ttu-id="e3b3d-124">Related topic</span><span class="sxs-lookup"><span data-stu-id="e3b3d-124">Related topic</span></span>
[<span data-ttu-id="e3b3d-125">getSubmitMode (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e3b3d-125">getSubmitMode (Client API reference)</span></span>](getSubmitMode.md)

