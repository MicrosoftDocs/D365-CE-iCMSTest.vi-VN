---
title: removeOnSave (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 14a92f7c-f4c0-475d-8797-dcbb283db37a
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 31fd555f410d24a5b4faf6e1d08bddb2d69e0749
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386636"
---
# <a name="removeonsave-client-api-reference"></a><span data-ttu-id="9b132-102">removeOnSave (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="9b132-102">removeOnSave (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/removeOnSave-description.md](./includes/removeOnSave-description.md)]

## <a name="syntax"></a><span data-ttu-id="9b132-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="9b132-103">Syntax</span></span>

`formContext.data.entity.removeOnSave(myFunction)`

## <a name="parameter"></a><span data-ttu-id="9b132-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="9b132-104">Parameter</span></span>

|<span data-ttu-id="9b132-105">Tên</span><span class="sxs-lookup"><span data-stu-id="9b132-105">Name</span></span>|<span data-ttu-id="9b132-106">Loại</span><span class="sxs-lookup"><span data-stu-id="9b132-106">Type</span></span>|<span data-ttu-id="9b132-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="9b132-107">Required</span></span>|<span data-ttu-id="9b132-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="9b132-108">Description</span></span>|
|--|--|--|--|
|<span data-ttu-id="9b132-109">myFunction</span><span class="sxs-lookup"><span data-stu-id="9b132-109">myFunction</span></span>|<span data-ttu-id="9b132-110">function reference</span><span class="sxs-lookup"><span data-stu-id="9b132-110">function reference</span></span>|<span data-ttu-id="9b132-111">Có</span><span class="sxs-lookup"><span data-stu-id="9b132-111">Yes</span></span>|<span data-ttu-id="9b132-112">The function to be removed for the **OnSave** event.</span><span class="sxs-lookup"><span data-stu-id="9b132-112">The function to be removed for the **OnSave** event.</span></span>

### <a name="related-topics"></a><span data-ttu-id="9b132-113">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="9b132-113">Related topics</span></span>

[<span data-ttu-id="9b132-114">addOnSave</span><span class="sxs-lookup"><span data-stu-id="9b132-114">addOnSave</span></span>](addOnSave.md)

[<span data-ttu-id="9b132-115">Form OnSave event</span><span class="sxs-lookup"><span data-stu-id="9b132-115">Form OnSave event</span></span>](../events/form-onsave.md)

