---
title: save (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a27f8267-9b24-42b7-a075-420a26db6693
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d0988e23755397d90c91624c2b8d7fb1a3c6f5d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388181"
---
# <a name="save-client-api-reference"></a><span data-ttu-id="9d4cf-102">save (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="9d4cf-102">save (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/save-description.md](./includes/save-description.md)]

## <a name="syntax"></a><span data-ttu-id="9d4cf-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="9d4cf-103">Syntax</span></span>

`formContext.data.entity.save(saveOption);`

## <a name="parameters"></a><span data-ttu-id="9d4cf-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="9d4cf-104">Parameters</span></span>

|<span data-ttu-id="9d4cf-105">Tên</span><span class="sxs-lookup"><span data-stu-id="9d4cf-105">Name</span></span>|<span data-ttu-id="9d4cf-106">Loại</span><span class="sxs-lookup"><span data-stu-id="9d4cf-106">Type</span></span>|<span data-ttu-id="9d4cf-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="9d4cf-107">Required</span></span>|<span data-ttu-id="9d4cf-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9d4cf-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="9d4cf-109">saveOption</span><span class="sxs-lookup"><span data-stu-id="9d4cf-109">saveOption</span></span>|<span data-ttu-id="9d4cf-110">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="9d4cf-110">String</span></span>|<span data-ttu-id="9d4cf-111">Không</span><span class="sxs-lookup"><span data-stu-id="9d4cf-111">No</span></span>|<span data-ttu-id="9d4cf-112">Specify options for saving the record.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-112">Specify options for saving the record.</span></span> <span data-ttu-id="9d4cf-113">If no parameter is included in the method, the record will simply be saved.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-113">If no parameter is included in the method, the record will simply be saved.</span></span> <span data-ttu-id="9d4cf-114">This is the equivalent of using the **Save** command.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-114">This is the equivalent of using the **Save** command.</span></span><br/><span data-ttu-id="9d4cf-115">You can specify one of the following values:</span><span class="sxs-lookup"><span data-stu-id="9d4cf-115">You can specify one of the following values:</span></span><br/><br/><span data-ttu-id="9d4cf-116">- **saveandclose**: This is the equivalent of using the **Save and Close** command.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-116">- **saveandclose**: This is the equivalent of using the **Save and Close** command.</span></span><br/><br/><span data-ttu-id="9d4cf-117">- **saveandnew**: This is the equivalent of the using the **Save and New** command.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-117">- **saveandnew**: This is the equivalent of the using the **Save and New** command.</span></span>|

## <a name="example"></a><span data-ttu-id="9d4cf-118">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="9d4cf-118">Example</span></span>

<span data-ttu-id="9d4cf-119">To open a new form after the save is completed:</span><span class="sxs-lookup"><span data-stu-id="9d4cf-119">To open a new form after the save is completed:</span></span>

`formContext.data.entity.save("saveandnew");`

### <a name="related-topics"></a><span data-ttu-id="9d4cf-120">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="9d4cf-120">Related topics</span></span>

[<span data-ttu-id="9d4cf-121">formContext.data.save</span><span class="sxs-lookup"><span data-stu-id="9d4cf-121">formContext.data.save</span></span>](../formContext-data/save.md)

[<span data-ttu-id="9d4cf-122">formContext</span><span class="sxs-lookup"><span data-stu-id="9d4cf-122">formContext</span></span>](../../clientapi-form-context.md)

