---
title: getVisible (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 72c7ec48-1d27-499c-b56c-b7a449a347b8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0320d9fdbc60838a17b43d9603df528f346dde60
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385489"
---
# <a name="getvisible-client-api-reference"></a><span data-ttu-id="087ab-102">getVisible (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="087ab-102">getVisible (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getVisible-description.md](./includes/getVisible-description.md)]

>[!NOTE]
><span data-ttu-id="087ab-103">If the containing **section** or **tab** for this control isn’t visible, this method can still return **true**.</span><span class="sxs-lookup"><span data-stu-id="087ab-103">If the containing **section** or **tab** for this control isn’t visible, this method can still return **true**.</span></span> <span data-ttu-id="087ab-104">To make certain that the control is actually visible; you need to also check the visibility of the containing elements.</span><span class="sxs-lookup"><span data-stu-id="087ab-104">To make certain that the control is actually visible; you need to also check the visibility of the containing elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="087ab-105">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="087ab-105">Syntax</span></span>

`quickViewControl.getVisible();`

## <a name="return-value"></a><span data-ttu-id="087ab-106">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="087ab-106">Return Value</span></span>

<span data-ttu-id="087ab-107">**Type**: Boolean.</span><span class="sxs-lookup"><span data-stu-id="087ab-107">**Type**: Boolean.</span></span>

<span data-ttu-id="087ab-108">**Description**: true if the control is visible; false otherwise.</span><span class="sxs-lookup"><span data-stu-id="087ab-108">**Description**: true if the control is visible; false otherwise.</span></span>

### <a name="related-topics"></a><span data-ttu-id="087ab-109">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="087ab-109">Related topics</span></span>

[<span data-ttu-id="087ab-110">setVisible</span><span class="sxs-lookup"><span data-stu-id="087ab-110">setVisible</span></span>](setVisible.md)

[<span data-ttu-id="087ab-111">formContext.ui.quickForms</span><span class="sxs-lookup"><span data-stu-id="087ab-111">formContext.ui.quickForms</span></span>](../formContext-ui-quickForms.md)



