---
title: formContext.ui.quickForms (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with processes in Customer Engagement using client API.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a04043de-3497-433a-ae73-4101806dd931
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 262b400319072170aea2d3bd7876152d1ffa9c49
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386246"
---
# <a name="formcontextuiquickforms-client-api-reference"></a><span data-ttu-id="2d6cc-103">formContext.ui.quickForms (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="2d6cc-103">formContext.ui.quickForms (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2d6cc-104">Provides methods to access all the quick view controls and its constituent controls on the Customer Engagement forms when using the new form rendering engine (also called "turbo forms").</span><span class="sxs-lookup"><span data-stu-id="2d6cc-104">Provides methods to access all the quick view controls and its constituent controls on the Customer Engagement forms when using the new form rendering engine (also called "turbo forms").</span></span> <span data-ttu-id="2d6cc-105">A quick view control is a quick view form added to a main form in Customer Engagement that enables you to view information about a related entity record within the main form.</span><span class="sxs-lookup"><span data-stu-id="2d6cc-105">A quick view control is a quick view form added to a main form in Customer Engagement that enables you to view information about a related entity record within the main form.</span></span> <span data-ttu-id="2d6cc-106">Data in constituent controls in a quick view control cannot be edited.</span><span class="sxs-lookup"><span data-stu-id="2d6cc-106">Data in constituent controls in a quick view control cannot be edited.</span></span>

<span data-ttu-id="2d6cc-107">The **quickForms** collection provides access to all the quick view controls on a form, and supports all the standard methods of the collections.</span><span class="sxs-lookup"><span data-stu-id="2d6cc-107">The **quickForms** collection provides access to all the quick view controls on a form, and supports all the standard methods of the collections.</span></span> <span data-ttu-id="2d6cc-108">See [Collections](collections.md)) for information about the collection methods.</span><span class="sxs-lookup"><span data-stu-id="2d6cc-108">See [Collections](collections.md)) for information about the collection methods.</span></span> 

<span data-ttu-id="2d6cc-109">You can retrieve a quick view control in the **quickForms** collection by using the [get](collections/get.md) method by specifying either the index value (integer) or name (string) of the quick view control as the argument:</span><span class="sxs-lookup"><span data-stu-id="2d6cc-109">You can retrieve a quick view control in the **quickForms** collection by using the [get](collections/get.md) method by specifying either the index value (integer) or name (string) of the quick view control as the argument:</span></span>

`quickViewControl = formContext.ui.quickForms.get(arg)`


## <a name="quick-form-control-methods"></a><span data-ttu-id="2d6cc-110">Quick form control Methods</span><span class="sxs-lookup"><span data-stu-id="2d6cc-110">Quick form control Methods</span></span>

|                             <span data-ttu-id="2d6cc-111">Tên</span><span class="sxs-lookup"><span data-stu-id="2d6cc-111">Name</span></span>                              |                                                                  <span data-ttu-id="2d6cc-112">Mô tả</span><span class="sxs-lookup"><span data-stu-id="2d6cc-112">Description</span></span>                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
|   [<span data-ttu-id="2d6cc-113">getControl</span><span class="sxs-lookup"><span data-stu-id="2d6cc-113">getControl</span></span>](formcontext-ui-quickForms/getControlType.md)   |     [!INCLUDE[formcontext-ui-quickForms/includes/getControl-description.md](formcontext-ui-quickForms/includes/getControl-description.md)]     |
| [<span data-ttu-id="2d6cc-114">getControlType</span><span class="sxs-lookup"><span data-stu-id="2d6cc-114">getControlType</span></span>](formcontext-ui-quickForms/getControlType.md) | [!INCLUDE[formcontext-ui-quickForms/includes/getControlType-description.md](formcontext-ui-quickForms/includes/getControlType-description.md)] |
|    [<span data-ttu-id="2d6cc-115">getDisabled</span><span class="sxs-lookup"><span data-stu-id="2d6cc-115">getDisabled</span></span>](formcontext-ui-quickForms/getDisabled.md)    |    [!INCLUDE[formcontext-ui-quickForms/includes/getDisabled-description.md](formcontext-ui-quickForms/includes/getDisabled-description.md)]    |
|       [<span data-ttu-id="2d6cc-116">getLabel</span><span class="sxs-lookup"><span data-stu-id="2d6cc-116">getLabel</span></span>](formcontext-ui-quickForms/getLabel.md)       |       [!INCLUDE[formcontext-ui-quickForms/includes/getLabel-description.md](formcontext-ui-quickForms/includes/getLabel-description.md)]       |
|        [<span data-ttu-id="2d6cc-117">getName</span><span class="sxs-lookup"><span data-stu-id="2d6cc-117">getName</span></span>](formcontext-ui-quickForms/getName.md)        |        [!INCLUDE[formcontext-ui-quickForms/includes/getName-description.md](formcontext-ui-quickForms/includes/getName-description.md)]        |
|      [<span data-ttu-id="2d6cc-118">getParent</span><span class="sxs-lookup"><span data-stu-id="2d6cc-118">getParent</span></span>](formcontext-ui-quickForms/getParent.md)      |      [!INCLUDE[formcontext-ui-quickForms/includes/getParent-description.md](formcontext-ui-quickForms/includes/getParent-description.md)]      |
|     [<span data-ttu-id="2d6cc-119">getVisible</span><span class="sxs-lookup"><span data-stu-id="2d6cc-119">getVisible</span></span>](formcontext-ui-quickForms/getVisible.md)     |     [!INCLUDE[formcontext-ui-quickForms/includes/getVisible-description.md](formcontext-ui-quickForms/includes/getVisible-description.md)]     |
|       [<span data-ttu-id="2d6cc-120">isLoaded</span><span class="sxs-lookup"><span data-stu-id="2d6cc-120">isLoaded</span></span>](formcontext-ui-quickForms/isLoaded.md)       |       [!INCLUDE[formcontext-ui-quickForms/includes/isLoaded-description.md](formcontext-ui-quickForms/includes/isLoaded-description.md)]       |
|        [<span data-ttu-id="2d6cc-121">refresh</span><span class="sxs-lookup"><span data-stu-id="2d6cc-121">refresh</span></span>](formcontext-ui-quickForms/refresh.md)        |        [!INCLUDE[formcontext-ui-quickForms/includes/refresh-description.md](formcontext-ui-quickForms/includes/refresh-description.md)]        |
|    [<span data-ttu-id="2d6cc-122">setDisabled</span><span class="sxs-lookup"><span data-stu-id="2d6cc-122">setDisabled</span></span>](formcontext-ui-quickForms/setDisabled.md)    |    [!INCLUDE[formcontext-ui-quickForms/includes/setDisabled-description.md](formcontext-ui-quickForms/includes/setDisabled-description.md)]    |
|       [<span data-ttu-id="2d6cc-123">setFocus</span><span class="sxs-lookup"><span data-stu-id="2d6cc-123">setFocus</span></span>](formcontext-ui-quickForms/setFocus.md)       |       [!INCLUDE[formcontext-ui-quickForms/includes/setFocus-description.md](formcontext-ui-quickForms/includes/setFocus-description.md)]       |
|       [<span data-ttu-id="2d6cc-124">setLabel</span><span class="sxs-lookup"><span data-stu-id="2d6cc-124">setLabel</span></span>](formcontext-ui-quickForms/setLabel.md)       |       [!INCLUDE[formcontext-ui-quickForms/includes/setLabel-description.md](formcontext-ui-quickForms/includes/setLabel-description.md)]       |
|     [<span data-ttu-id="2d6cc-125">setVisible</span><span class="sxs-lookup"><span data-stu-id="2d6cc-125">setVisible</span></span>](formcontext-ui-quickForms/setVisible.md)     |     [!INCLUDE[formcontext-ui-quickForms/includes/setVisible-description.md](formcontext-ui-quickForms/includes/setVisible-description.md)]     |

### <a name="related-topics"></a><span data-ttu-id="2d6cc-126">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="2d6cc-126">Related topics</span></span>

[<span data-ttu-id="2d6cc-127">formContext.ui</span><span class="sxs-lookup"><span data-stu-id="2d6cc-127">formContext.ui</span></span>](formContext-ui.md)
