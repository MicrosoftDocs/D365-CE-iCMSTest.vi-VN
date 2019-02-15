---
title: formContext.ui.FormSelector (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about working with processes in Customer Engagement using client API.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 32e8d1d0-4093-4588-a517-2930eec34dce
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7b4f18f18b94d731f4a95440643d002478e1de0f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388532"
---
# <a name="formcontextuiformselector-client-api-reference"></a><span data-ttu-id="84e93-103">formContext.ui.formSelector (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="84e93-103">formContext.ui.formSelector (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="84e93-104">The **formContext.ui.formSelector** property lets you work with form items where a form item represents a form that is available to a user because it is associated with a security role that the user is also associated to.</span><span class="sxs-lookup"><span data-stu-id="84e93-104">The **formContext.ui.formSelector** property lets you work with form items where a form item represents a form that is available to a user because it is associated with a security role that the user is also associated to.</span></span> <span data-ttu-id="84e93-105">Often there will be only one form.</span><span class="sxs-lookup"><span data-stu-id="84e93-105">Often there will be only one form.</span></span> <span data-ttu-id="84e93-106">When more than one form is available, methods for a form item can be used to change the form the user is viewing.</span><span class="sxs-lookup"><span data-stu-id="84e93-106">When more than one form is available, methods for a form item can be used to change the form the user is viewing.</span></span>

<span data-ttu-id="84e93-107">Form Items are available through any of the following:</span><span class="sxs-lookup"><span data-stu-id="84e93-107">Form Items are available through any of the following:</span></span>

- <span data-ttu-id="84e93-108">**formselector.items** collection: A collection of all the form items accessible to the current user.</span><span class="sxs-lookup"><span data-stu-id="84e93-108">**formselector.items** collection: A collection of all the form items accessible to the current user.</span></span> <span data-ttu-id="84e93-109">Only those forms that share an association with one of the user’s security roles are available in this collection.</span><span class="sxs-lookup"><span data-stu-id="84e93-109">Only those forms that share an association with one of the user’s security roles are available in this collection.</span></span> <span data-ttu-id="84e93-110">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="84e93-110">Example:</span></span>
 
    `formItem = formContext.ui.formSelector.items.get(arg);`

    <span data-ttu-id="84e93-111">See [Collections](collections.md)) for information about the collection methods.</span><span class="sxs-lookup"><span data-stu-id="84e93-111">See [Collections](collections.md)) for information about the collection methods.</span></span>
 
    >[!NOTE]
    ><span data-ttu-id="84e93-112">This collection isn't available for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets).</span><span class="sxs-lookup"><span data-stu-id="84e93-112">This collection isn't available for Dynamics 365 for Customer Engagement apps mobile clients (phones and tablets).</span></span>

- <span data-ttu-id="84e93-113">**formselector.getCurrentItem** method: Returns a reference to the form currently being shown.</span><span class="sxs-lookup"><span data-stu-id="84e93-113">**formselector.getCurrentItem** method: Returns a reference to the form currently being shown.</span></span> <span data-ttu-id="84e93-114">When only one form is available this method will return **null**.</span><span class="sxs-lookup"><span data-stu-id="84e93-114">When only one form is available this method will return **null**.</span></span> <span data-ttu-id="84e93-115">Ví dụ: </span><span class="sxs-lookup"><span data-stu-id="84e93-115">Example:</span></span>
 
    `formItem = formContext.ui.formSelector.getCurrentItem();`       

## <a name="form-item-methods"></a><span data-ttu-id="84e93-116">Form Item methods</span><span class="sxs-lookup"><span data-stu-id="84e93-116">Form Item methods</span></span>

<span data-ttu-id="84e93-117">After retrieving a form item using one of the above ways, use the following methods to work with the form item.</span><span class="sxs-lookup"><span data-stu-id="84e93-117">After retrieving a form item using one of the above ways, use the following methods to work with the form item.</span></span> 


|                        <span data-ttu-id="84e93-118">Tên</span><span class="sxs-lookup"><span data-stu-id="84e93-118">Name</span></span>                         |                                                               <span data-ttu-id="84e93-119">Decription</span><span class="sxs-lookup"><span data-stu-id="84e93-119">Decription</span></span>                                                               |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|    [<span data-ttu-id="84e93-120">getId</span><span class="sxs-lookup"><span data-stu-id="84e93-120">getId</span></span>](formcontext-ui-formselector/getId.md)    |    [!INCLUDE[formcontext-ui-formselector/includes/getId-description.md](formcontext-ui-formselector/includes/getId-description.md)]    |
| [<span data-ttu-id="84e93-121">getLabel</span><span class="sxs-lookup"><span data-stu-id="84e93-121">getLabel</span></span>](formcontext-ui-formselector/getLabel.md) | [!INCLUDE[formcontext-ui-formselector/includes/getLabel-description.md](formcontext-ui-formselector/includes/getLabel-description.md)] |
| [<span data-ttu-id="84e93-122">navigate</span><span class="sxs-lookup"><span data-stu-id="84e93-122">navigate</span></span>](formcontext-ui-formselector/navigate.md) | [!INCLUDE[formcontext-ui-formselector/includes/navigate-description.md](formcontext-ui-formselector/includes/navigate-description.md)] |