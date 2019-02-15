---
title: getControl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 57eb6b4b-90c1-4d56-b4b0-a7160af17f8f
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7ebd48530ec457d1450d586131d44a526829a0bc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388134"
---
# <a name="getcontrol-client-api-reference"></a><span data-ttu-id="e9f5f-102">getControl (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e9f5f-102">getControl (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getControl-description.md](./includes/getControl-description.md)]

## <a name="syntax"></a><span data-ttu-id="e9f5f-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="e9f5f-103">Syntax</span></span>

`quickViewControl.getControl(arg);`

## <a name="parameter"></a><span data-ttu-id="e9f5f-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="e9f5f-104">Parameter</span></span>

<span data-ttu-id="e9f5f-105">**arg**: Optional.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-105">**arg**: Optional.</span></span> <span data-ttu-id="e9f5f-106">You can access a single control in the constituent controls collection by passing an argument as either the name or the index value of the constituent control in a quick view control.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-106">You can access a single control in the constituent controls collection by passing an argument as either the name or the index value of the constituent control in a quick view control.</span></span> <span data-ttu-id="e9f5f-107">For example: `quickViewControl.getControl("firstname")` or `quickViewControl.getControl(0)`</span><span class="sxs-lookup"><span data-stu-id="e9f5f-107">For example: `quickViewControl.getControl("firstname")` or `quickViewControl.getControl(0)`</span></span>


## <a name="return-value"></a><span data-ttu-id="e9f5f-108">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="e9f5f-108">Return Value</span></span>

<span data-ttu-id="e9f5f-109">**Type**: Object or Object collection.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-109">**Type**: Object or Object collection.</span></span>

<span data-ttu-id="e9f5f-110">**Description**: Object if you use the method with parameter; object collection if you use the method without any parameters.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-110">**Description**: Object if you use the method with parameter; object collection if you use the method without any parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f5f-111">Chú thích</span><span class="sxs-lookup"><span data-stu-id="e9f5f-111">Remarks</span></span>

<span data-ttu-id="e9f5f-112">After you have retrieved a constituent control in a quick view control, you can use any of the methods supported for a control in Customer Engagement on the constituent control that does not alter the constituent control data.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-112">After you have retrieved a constituent control in a quick view control, you can use any of the methods supported for a control in Customer Engagement on the constituent control that does not alter the constituent control data.</span></span> <span data-ttu-id="e9f5f-113">This is because constituent controls in a quick view control are read only.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-113">This is because constituent controls in a quick view control are read only.</span></span> <span data-ttu-id="e9f5f-114">For example, you can use:</span><span class="sxs-lookup"><span data-stu-id="e9f5f-114">For example, you can use:</span></span> 

`quickViewControl.getControl(0).getAttribute()` 

<span data-ttu-id="e9f5f-115">For more information about methods supported for a control, see [Controls](../controls.md).</span><span class="sxs-lookup"><span data-stu-id="e9f5f-115">For more information about methods supported for a control, see [Controls](../controls.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9f5f-116">The [getAttribute](../controls/getAttribute.md) or any data related methods on a constituent control might not work on the main form [OnLoad](../events/form-onload.md) event because the quick view form that its bound to might not have loaded completely when the main form has loaded.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-116">The [getAttribute](../controls/getAttribute.md) or any data related methods on a constituent control might not work on the main form [OnLoad](../events/form-onload.md) event because the quick view form that its bound to might not have loaded completely when the main form has loaded.</span></span> <span data-ttu-id="e9f5f-117">You must use the [isLoaded](isLoaded.md) method for the quick view control instance to help you determine if the bounded quick view form has loaded completely.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-117">You must use the [isLoaded](isLoaded.md) method for the quick view control instance to help you determine if the bounded quick view form has loaded completely.</span></span> 
> 
> <span data-ttu-id="e9f5f-118">Also, the way you retrieve constituent controls in a quick view control on forms using the new form rendering engine is different from the legacy forms.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-118">Also, the way you retrieve constituent controls in a quick view control on forms using the new form rendering engine is different from the legacy forms.</span></span> <span data-ttu-id="e9f5f-119">So, if you are using legacy forms and have code targeting constituent controls in a quick view control, you must update your code when you decide to use the new form rendering engine.</span><span class="sxs-lookup"><span data-stu-id="e9f5f-119">So, if you are using legacy forms and have code targeting constituent controls in a quick view control, you must update your code when you decide to use the new form rendering engine.</span></span>

### <a name="related-topics"></a><span data-ttu-id="e9f5f-120">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e9f5f-120">Related topics</span></span>

[<span data-ttu-id="e9f5f-121">formContext.ui.quickForms</span><span class="sxs-lookup"><span data-stu-id="e9f5f-121">formContext.ui.quickForms</span></span>](../formContext-ui-quickForms.md)



