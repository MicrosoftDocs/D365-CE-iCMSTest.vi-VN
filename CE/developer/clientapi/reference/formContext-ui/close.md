---
title: close (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 12/04/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 1261a94d-4f5c-446d-8c29-a326e819696b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bd5b03469ca5513c4052effffbbb5f3155b99c34
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386542"
---
# <a name="close-client-api-reference"></a><span data-ttu-id="fd0b1-102">close (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="fd0b1-102">close (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/close-description.md](./includes/close-description.md)]

## <a name="syntax"></a><span data-ttu-id="fd0b1-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="fd0b1-103">Syntax</span></span>

`formContext.ui.close();`

## <a name="remarks"></a><span data-ttu-id="fd0b1-104">Chú thích</span><span class="sxs-lookup"><span data-stu-id="fd0b1-104">Remarks</span></span>

<span data-ttu-id="fd0b1-105">The HTML **Window.close** method is suppressed.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-105">The HTML **Window.close** method is suppressed.</span></span> <span data-ttu-id="fd0b1-106">To close a form window, you must use this method.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-106">To close a form window, you must use this method.</span></span> <span data-ttu-id="fd0b1-107">If there are any unsaved changes in the form, the user will be prompted whether they want to save their changes before the window closes.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-107">If there are any unsaved changes in the form, the user will be prompted whether they want to save their changes before the window closes.</span></span>

<span data-ttu-id="fd0b1-108">For Microsoft Dynamics 365 for tablets, this method mimics the behavior of the back navigation button.</span><span class="sxs-lookup"><span data-stu-id="fd0b1-108">For Microsoft Dynamics 365 for tablets, this method mimics the behavior of the back navigation button.</span></span>

### <a name="related-topics"></a><span data-ttu-id="fd0b1-109">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="fd0b1-109">Related topics</span></span>

[<span data-ttu-id="fd0b1-110">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="fd0b1-110">formContext.ui</span></span>](../formContext-ui.md)

[<span data-ttu-id="fd0b1-111">formContext</span><span class="sxs-lookup"><span data-stu-id="fd0b1-111">formContext</span></span>](../../clientapi-form-context.md)

