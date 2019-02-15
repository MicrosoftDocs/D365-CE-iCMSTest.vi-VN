---
title: getControlType (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 72d6c761-bcc7-4de6-b73f-5f2833297825
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3489f8ec12d193c3a20289fc4966e9189ab6e78b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387345"
---
# <a name="getcontroltype-client-api-reference"></a><span data-ttu-id="93e4a-102">getControlType (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="93e4a-102">getControlType (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getControlType-description.md](./includes/getControlType-description.md)]

## <a name="syntax"></a><span data-ttu-id="93e4a-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="93e4a-103">Syntax</span></span>

`quickViewControl.getControlType();`

## <a name="return-value"></a><span data-ttu-id="93e4a-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="93e4a-104">Return Value</span></span>

<span data-ttu-id="93e4a-105">**Type**: String.</span><span class="sxs-lookup"><span data-stu-id="93e4a-105">**Type**: String.</span></span>

<span data-ttu-id="93e4a-106">**Description**: For a quick view control, the method returns "quickform".</span><span class="sxs-lookup"><span data-stu-id="93e4a-106">**Description**: For a quick view control, the method returns "quickform".</span></span> 

<span data-ttu-id="93e4a-107">For a constituent control in a quick view control, the method returns the actual category of the control.</span><span class="sxs-lookup"><span data-stu-id="93e4a-107">For a constituent control in a quick view control, the method returns the actual category of the control.</span></span> <span data-ttu-id="93e4a-108">For more information about possible return values, see [getControlType](../controls/getControlType.md)..</span><span class="sxs-lookup"><span data-stu-id="93e4a-108">For more information about possible return values, see [getControlType](../controls/getControlType.md)..</span></span>

### <a name="related-topics"></a><span data-ttu-id="93e4a-109">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="93e4a-109">Related topics</span></span>

[<span data-ttu-id="93e4a-110">formContext.ui.quickForms</span><span class="sxs-lookup"><span data-stu-id="93e4a-110">formContext.ui.quickForms</span></span>](../formContext-ui-quickForms.md)
