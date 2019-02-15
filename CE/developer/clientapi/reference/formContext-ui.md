---
title: formContext.ui (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about working with processes in Customer Engagement using client API.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: f93e0e21-f911-4681-81b0-82ccf98ee28b
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ce63e16ac3739aae0ddeab1b14265253dc0f2369
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386474"
---
# <a name="formcontextui-client-api-reference"></a><span data-ttu-id="fd780-103">formContext.ui (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="fd780-103">formContext.ui (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fd780-104">Provides properties and methods to retrieve information about the user interface (UI) as well as collections for several subcomponents of the form.</span><span class="sxs-lookup"><span data-stu-id="fd780-104">Provides properties and methods to retrieve information about the user interface (UI) as well as collections for several subcomponents of the form.</span></span>

![formContext UI object model](../../media/ClientAPI-formContext-ui-Model.png)

## <a name="properties"></a><span data-ttu-id="fd780-106">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="fd780-106">Properties</span></span>

|<span data-ttu-id="fd780-107">Tên</span><span class="sxs-lookup"><span data-stu-id="fd780-107">Name</span></span>|<span data-ttu-id="fd780-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fd780-108">Description</span></span>|
|--|--|
|<span data-ttu-id="fd780-109">Kiểm soát</span><span class="sxs-lookup"><span data-stu-id="fd780-109">Controls</span></span>|<span data-ttu-id="fd780-110">Collection of all the controls on the page.</span><span class="sxs-lookup"><span data-stu-id="fd780-110">Collection of all the controls on the page.</span></span> <span data-ttu-id="fd780-111">See [Collections](collections.md) for information about the collections and [Controls](controls.md) for information about the control objects in the collection.</span><span class="sxs-lookup"><span data-stu-id="fd780-111">See [Collections](collections.md) for information about the collections and [Controls](controls.md) for information about the control objects in the collection.</span></span>|
|<span data-ttu-id="fd780-112">formSelector</span><span class="sxs-lookup"><span data-stu-id="fd780-112">formSelector</span></span>|<span data-ttu-id="fd780-113">Use the formSelector.getCurrentItem method to retrieve information about the form currently in use.</span><span class="sxs-lookup"><span data-stu-id="fd780-113">Use the formSelector.getCurrentItem method to retrieve information about the form currently in use.</span></span> <span data-ttu-id="fd780-114">Use the formSelector.items collection to return information about all the forms available for the user.</span><span class="sxs-lookup"><span data-stu-id="fd780-114">Use the formSelector.items collection to return information about all the forms available for the user.</span></span> <span data-ttu-id="fd780-115">**formSelector** is not available for Microsoft Dynamics 365 for tablets.</span><span class="sxs-lookup"><span data-stu-id="fd780-115">**formSelector** is not available for Microsoft Dynamics 365 for tablets.</span></span>|
|<span data-ttu-id="fd780-116">navigation</span><span class="sxs-lookup"><span data-stu-id="fd780-116">navigation</span></span>|<span data-ttu-id="fd780-117">A collection of all the navigation items on the page.</span><span class="sxs-lookup"><span data-stu-id="fd780-117">A collection of all the navigation items on the page.</span></span> <span data-ttu-id="fd780-118">See [Collections](collections.md) for information about the collection methods and [formContext.ui.navigation item](formContext-ui-navigation.md) for information about the items in the collection.</span><span class="sxs-lookup"><span data-stu-id="fd780-118">See [Collections](collections.md) for information about the collection methods and [formContext.ui.navigation item](formContext-ui-navigation.md) for information about the items in the collection.</span></span> <span data-ttu-id="fd780-119">**navigation** is not available for Microsoft Dynamics 365 for tablets.</span><span class="sxs-lookup"><span data-stu-id="fd780-119">**navigation** is not available for Microsoft Dynamics 365 for tablets.</span></span>|
|<span data-ttu-id="fd780-120">process</span><span class="sxs-lookup"><span data-stu-id="fd780-120">process</span></span>|<span data-ttu-id="fd780-121">Provides objects and methods to interact with the business process flow control on a form.</span><span class="sxs-lookup"><span data-stu-id="fd780-121">Provides objects and methods to interact with the business process flow control on a form.</span></span><br/><span data-ttu-id="fd780-122">More information: [formContext.ui.process](formContext-ui-process.md)</span><span class="sxs-lookup"><span data-stu-id="fd780-122">More information: [formContext.ui.process](formContext-ui-process.md)</span></span>|
|<span data-ttu-id="fd780-123">quickForms</span><span class="sxs-lookup"><span data-stu-id="fd780-123">quickForms</span></span>|<span data-ttu-id="fd780-124">A collection of all the quick view controls on a form using the new form rendering engine (also called "turbo forms").</span><span class="sxs-lookup"><span data-stu-id="fd780-124">A collection of all the quick view controls on a form using the new form rendering engine (also called "turbo forms").</span></span><br/><span data-ttu-id="fd780-125">More information: [formContext.ui quickForms](formContext-ui-quickforms.md)</span><span class="sxs-lookup"><span data-stu-id="fd780-125">More information: [formContext.ui quickForms](formContext-ui-quickforms.md)</span></span>|
|<span data-ttu-id="fd780-126">tabs</span><span class="sxs-lookup"><span data-stu-id="fd780-126">tabs</span></span>|<span data-ttu-id="fd780-127">A collection of all the tabs on the page.</span><span class="sxs-lookup"><span data-stu-id="fd780-127">A collection of all the tabs on the page.</span></span><br/><span data-ttu-id="fd780-128">See [Collections](collections.md) for information about the collection methods and [formContex.ui tab](formContext-ui-tabs.md)  for information about the items in the collection.</span><span class="sxs-lookup"><span data-stu-id="fd780-128">See [Collections](collections.md) for information about the collection methods and [formContex.ui tab](formContext-ui-tabs.md)  for information about the items in the collection.</span></span>|


## <a name="methods"></a><span data-ttu-id="fd780-129">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="fd780-129">Methods</span></span> 

|                               <span data-ttu-id="fd780-130">Tên</span><span class="sxs-lookup"><span data-stu-id="fd780-130">Name</span></span>                               |                                                              <span data-ttu-id="fd780-131">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fd780-131">Description</span></span>                                                               |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|             [<span data-ttu-id="fd780-132">addOnLoad</span><span class="sxs-lookup"><span data-stu-id="fd780-132">addOnLoad</span></span>](formContext-ui/addOnload.md)             |             [!INCLUDE[formContext-ui/includes/addOnLoad-description.md](formContext-ui/includes/addOnLoad-description.md)]             |
| [<span data-ttu-id="fd780-133">clearFormNotification</span><span class="sxs-lookup"><span data-stu-id="fd780-133">clearFormNotification</span></span>](formContext-ui/clearFormNotification.md) | [!INCLUDE[formContext-ui/includes/clearFormNotification-description.md](formContext-ui/includes/clearFormNotification-description.md)] |
|                 [<span data-ttu-id="fd780-134">close</span><span class="sxs-lookup"><span data-stu-id="fd780-134">close</span></span>](formContext-ui/close.md)                 |                 [!INCLUDE[formContext-ui/includes/close-description.md](formContext-ui/includes/close-description.md)]                 |
|           [<span data-ttu-id="fd780-135">getFormType</span><span class="sxs-lookup"><span data-stu-id="fd780-135">getFormType</span></span>](formContext-ui/getFormType.md)           |           [!INCLUDE[formContext-ui/includes/getFormType-description.md](formContext-ui/includes/getFormType-description.md)]           |
|     [<span data-ttu-id="fd780-136">getViewPortHeight</span><span class="sxs-lookup"><span data-stu-id="fd780-136">getViewPortHeight</span></span>](formContext-ui/getViewPortHeight.md)     |     [!INCLUDE[formContext-ui/includes/getViewPortHeight-description.md](formContext-ui/includes/getViewPortHeight-description.md)]     |
|      [<span data-ttu-id="fd780-137">getViewPortWidth</span><span class="sxs-lookup"><span data-stu-id="fd780-137">getViewPortWidth</span></span>](formContext-ui/getViewPortWidth.md)      |      [!INCLUDE[formContext-ui/includes/getViewPortWidth-description.md](formContext-ui/includes/getViewPortWidth-description.md)]      |
|         [<span data-ttu-id="fd780-138">refreshRibbon</span><span class="sxs-lookup"><span data-stu-id="fd780-138">refreshRibbon</span></span>](formContext-ui/refreshRibbon.md)         |         [!INCLUDE[formContext-ui/includes/refreshRibbon-description.md](formContext-ui/includes/refreshRibbon-description.md)]         |
|          [<span data-ttu-id="fd780-139">removeOnLoad</span><span class="sxs-lookup"><span data-stu-id="fd780-139">removeOnLoad</span></span>](formContext-ui/removeOnLoad.md)          |          [!INCLUDE[formContext-ui/includes/removeOnLoad-description.md](formContext-ui/includes/removeOnLoad-description.md)]          |
|     [<span data-ttu-id="fd780-140">setFormEntityName</span><span class="sxs-lookup"><span data-stu-id="fd780-140">setFormEntityName</span></span>](formContext-ui/setFormEntityName.md)     |     [!INCLUDE[formContext-ui/includes/setFormEntityName-description.md](formContext-ui/includes/setFormEntityName-description.md)]     |
|   [<span data-ttu-id="fd780-141">setFormNotification</span><span class="sxs-lookup"><span data-stu-id="fd780-141">setFormNotification</span></span>](formContext-ui/setFormNotification.md)   |   [!INCLUDE[formContext-ui/includes/setFormNotification-description.md](formContext-ui/includes/setFormNotification-description.md)]   |

### <a name="related-topics"></a><span data-ttu-id="fd780-142">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="fd780-142">Related topics</span></span>

[<span data-ttu-id="fd780-143">formContext</span><span class="sxs-lookup"><span data-stu-id="fd780-143">formContext</span></span>](../clientapi-form-context.md)