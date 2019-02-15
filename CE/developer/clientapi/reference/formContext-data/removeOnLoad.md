---
title: removeOnLoad (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: bf07fe04-fc4c-43ed-a445-1b61bf0ea2db
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 69945153ddcbc22432b0d20c29c9481d44bc9ade
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388387"
---
# <a name="removeonload-client-api-reference"></a><span data-ttu-id="53012-102">removeOnLoad (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="53012-102">removeOnLoad (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/removeOnLoad-description.md](./includes/removeOnLoad-description.md)]

## <a name="syntax"></a><span data-ttu-id="53012-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="53012-103">Syntax</span></span>

`formContext.data.removeOnLoad(myFunction)`

## <a name="parameter"></a><span data-ttu-id="53012-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="53012-104">Parameter</span></span>

|<span data-ttu-id="53012-105">Tên</span><span class="sxs-lookup"><span data-stu-id="53012-105">Name</span></span>|<span data-ttu-id="53012-106">Loại</span><span class="sxs-lookup"><span data-stu-id="53012-106">Type</span></span>|<span data-ttu-id="53012-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="53012-107">Required</span></span>|<span data-ttu-id="53012-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="53012-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="53012-109">myFunction</span><span class="sxs-lookup"><span data-stu-id="53012-109">myFunction</span></span>|<span data-ttu-id="53012-110">function reference</span><span class="sxs-lookup"><span data-stu-id="53012-110">function reference</span></span>|<span data-ttu-id="53012-111">Có</span><span class="sxs-lookup"><span data-stu-id="53012-111">Yes</span></span>|<span data-ttu-id="53012-112">The function to be removed when the form data loads.</span><span class="sxs-lookup"><span data-stu-id="53012-112">The function to be removed when the form data loads.</span></span>

### <a name="related-topics"></a><span data-ttu-id="53012-113">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="53012-113">Related topics</span></span>

[<span data-ttu-id="53012-114">addOnLoad</span><span class="sxs-lookup"><span data-stu-id="53012-114">addOnLoad</span></span>](addOnLoad.md)

[<span data-ttu-id="53012-115">Form data OnLoad event</span><span class="sxs-lookup"><span data-stu-id="53012-115">Form data OnLoad event</span></span>](../events/form-data-onload.md)

