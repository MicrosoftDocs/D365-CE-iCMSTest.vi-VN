---
title: getControl (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 34715e1f-35c0-4b7f-971e-e0a6518f0722
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4f0188a2475e08873bc4c01d58121e1ea219cc2a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387004"
---
# <a name="getcontrol-client-api-reference"></a><span data-ttu-id="11a24-102">getControl (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="11a24-102">getControl (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="11a24-103">Gets a control on the form.</span><span class="sxs-lookup"><span data-stu-id="11a24-103">Gets a control on the form.</span></span> 

## <a name="syntax"></a><span data-ttu-id="11a24-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="11a24-104">Syntax</span></span>

`formContext.getControl(arg);`

<span data-ttu-id="11a24-105">The **formContext.getControl(arg)** method is a shortcut method to access **formContext.ui.controls.get**.</span><span class="sxs-lookup"><span data-stu-id="11a24-105">The **formContext.getControl(arg)** method is a shortcut method to access **formContext.ui.controls.get**.</span></span>

## <a name="parameter"></a><span data-ttu-id="11a24-106">Tham số</span><span class="sxs-lookup"><span data-stu-id="11a24-106">Parameter</span></span>

<span data-ttu-id="11a24-107">**arg**: Optional.</span><span class="sxs-lookup"><span data-stu-id="11a24-107">**arg**: Optional.</span></span> <span data-ttu-id="11a24-108">You can access a control on a form by passing an argument as either the **name** or the **index valu**e of the control on a form.</span><span class="sxs-lookup"><span data-stu-id="11a24-108">You can access a control on a form by passing an argument as either the **name** or the **index valu**e of the control on a form.</span></span> <span data-ttu-id="11a24-109">For example: `formContext.getControl("firstname")` or `formContext.getControl(0)`</span><span class="sxs-lookup"><span data-stu-id="11a24-109">For example: `formContext.getControl("firstname")` or `formContext.getControl(0)`</span></span>


## <a name="return-value"></a><span data-ttu-id="11a24-110">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="11a24-110">Return Value</span></span>

<span data-ttu-id="11a24-111">**Type**: Object or Object collection.</span><span class="sxs-lookup"><span data-stu-id="11a24-111">**Type**: Object or Object collection.</span></span>

<span data-ttu-id="11a24-112">**Description**: Object if you use the method with parameter; object collection if you use the method without any parameters.</span><span class="sxs-lookup"><span data-stu-id="11a24-112">**Description**: Object if you use the method with parameter; object collection if you use the method without any parameters.</span></span>



### <a name="related-topics"></a><span data-ttu-id="11a24-113">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="11a24-113">Related topics</span></span>

[<span data-ttu-id="11a24-114">formContext</span><span class="sxs-lookup"><span data-stu-id="11a24-114">formContext</span></span>](../../clientapi-form-Context.md)



