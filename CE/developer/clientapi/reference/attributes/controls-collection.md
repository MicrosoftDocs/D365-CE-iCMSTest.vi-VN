---
title: Controls collection (Client API reference)| MicrosoftDocs
description: Learn about how to access controls associated with attributes.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: d5f3c0c5-b267-42a8-82e8-8c4a1cda3752
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 714ded318ae74af84689354ada326ae933014bfe
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388543"
---
# <a name="controls-collection-client-api-reference"></a><span data-ttu-id="e0cb2-103">Controls collection (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e0cb2-103">Controls collection (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e0cb2-104">Use the Controls collection to access controls associated with attributes.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-104">Use the Controls collection to access controls associated with attributes.</span></span> 

<span data-ttu-id="e0cb2-105">Because each attribute may be represented more than one time on the page, the controls collection provides access to all controls representing that attribute.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-105">Because each attribute may be represented more than one time on the page, the controls collection provides access to all controls representing that attribute.</span></span> <span data-ttu-id="e0cb2-106">If the attribute is represented by only one field in the page, the length of this collection will be 1.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-106">If the attribute is represented by only one field in the page, the length of this collection will be 1.</span></span> <span data-ttu-id="e0cb2-107">When you use the control getName method the name of the first control will be the same as the name of the attribute.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-107">When you use the control getName method the name of the first control will be the same as the name of the attribute.</span></span> <span data-ttu-id="e0cb2-108">The second instance of a control for that attribute will be **<attributeName>1**.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-108">The second instance of a control for that attribute will be **<attributeName>1**.</span></span> <span data-ttu-id="e0cb2-109">The pattern **<attributeName>+N** will continue for each additional control added to the form for a specific attribute.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-109">The pattern **<attributeName>+N** will continue for each additional control added to the form for a specific attribute.</span></span>

<span data-ttu-id="e0cb2-110">When a form displays a business process flow control in the header, additional controls will be added for each attribute that is displayed in the business process flow.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-110">When a form displays a business process flow control in the header, additional controls will be added for each attribute that is displayed in the business process flow.</span></span> <span data-ttu-id="e0cb2-111">These controls have a unique name like the following: **header_process_<attribute name>**.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-111">These controls have a unique name like the following: **header_process_<attribute name>**.</span></span>

<span data-ttu-id="e0cb2-112">When performing actions on controls that are tied to an attribute you should always consider that the control may be included on the page more than once and you should generally perform the same actions for each control for the attribute.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-112">When performing actions on controls that are tied to an attribute you should always consider that the control may be included on the page more than once and you should generally perform the same actions for each control for the attribute.</span></span> <span data-ttu-id="e0cb2-113">You can do this by looping through the attribute controls collection and perform the actions on each control.</span><span class="sxs-lookup"><span data-stu-id="e0cb2-113">You can do this by looping through the attribute controls collection and perform the actions on each control.</span></span>

### <a name="related-topics"></a><span data-ttu-id="e0cb2-114">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e0cb2-114">Related topics</span></span>

[<span data-ttu-id="e0cb2-115">attributes (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e0cb2-115">attributes (Client API reference)</span></span>](../attributes.md)


