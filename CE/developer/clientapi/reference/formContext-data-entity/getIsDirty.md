---
title: getIsDirty (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 93908c95-c813-4f55-9d19-8fd27a0126d7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 978dd3c54fa74fb23a4aaa59274d061331e8cefc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386119"
---
# <a name="getisdirty-client-api-reference"></a><span data-ttu-id="a1942-102">getIsDirty (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="a1942-102">getIsDirty (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getIsDirty-description.md](./includes/getIsDirty-description.md)]

## <a name="syntax"></a><span data-ttu-id="a1942-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="a1942-103">Syntax</span></span>

`formContext.data.entity.getIsDirty();`

## <a name="return-type"></a><span data-ttu-id="a1942-104">Return Type</span><span class="sxs-lookup"><span data-stu-id="a1942-104">Return Type</span></span>

<span data-ttu-id="a1942-105">**Type**: Boolean</span><span class="sxs-lookup"><span data-stu-id="a1942-105">**Type**: Boolean</span></span>

<span data-ttu-id="a1942-106">**Description**: true if any fields in the form have been changed; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="a1942-106">**Description**: true if any fields in the form have been changed; false otherwise.</span></span>

### <a name="related-topics"></a><span data-ttu-id="a1942-107">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="a1942-107">Related topics</span></span>

[<span data-ttu-id="a1942-108">formContext.data.getIsDirty</span><span class="sxs-lookup"><span data-stu-id="a1942-108">formContext.data.getIsDirty</span></span>](../formContext-data/getIsDirty.md)

[<span data-ttu-id="a1942-109">formContext</span><span class="sxs-lookup"><span data-stu-id="a1942-109">formContext</span></span>](../../clientapi-form-context.md)

