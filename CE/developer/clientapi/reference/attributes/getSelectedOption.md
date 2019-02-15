---
title: Xrm.Device| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: ce572df6-aae6-431a-aa95-73eee544c7e9
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 22974db8a8f8a051e863cc5478583e5f98136acf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386307"
---
# <a name="getselectedoption-client-api-reference"></a><span data-ttu-id="37052-102">getSelectedOption (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="37052-102">getSelectedOption (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="37052-103">Returns the option object or an array of option objects selected in an **optionset** or **multiselectoptionset** attribute respectively.</span><span class="sxs-lookup"><span data-stu-id="37052-103">Returns the option object or an array of option objects selected in an **optionset** or **multiselectoptionset** attribute respectively.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="37052-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="37052-104">Attribute types supported</span></span>

<span data-ttu-id="37052-105">optionset, multiselectoptionset</span><span class="sxs-lookup"><span data-stu-id="37052-105">optionset, multiselectoptionset</span></span>

## <a name="syntax"></a><span data-ttu-id="37052-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="37052-106">Syntax</span></span>

`formContext.getAttribute(arg).getSelectedOption()`

## <a name="return-value"></a><span data-ttu-id="37052-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="37052-107">Return Value</span></span>

<span data-ttu-id="37052-108">**Type**: Option object for optionset; array of option objects for multiselectoptionset.</span><span class="sxs-lookup"><span data-stu-id="37052-108">**Type**: Option object for optionset; array of option objects for multiselectoptionset.</span></span> 

<span data-ttu-id="37052-109">**Description**: Returns the object with text and value properties.</span><span class="sxs-lookup"><span data-stu-id="37052-109">**Description**: Returns the object with text and value properties.</span></span>

### <a name="related-topics"></a><span data-ttu-id="37052-110">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="37052-110">Related topics</span></span>
[<span data-ttu-id="37052-111">getInitialValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="37052-111">getInitialValue (Client API reference)</span></span>](getInitialValue.md)

[<span data-ttu-id="37052-112">getOption (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="37052-112">getOption (Client API reference)</span></span>](getOption.md)

[<span data-ttu-id="37052-113">getOptions (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="37052-113">getOptions (Client API reference)</span></span>](getOptions.md)

[<span data-ttu-id="37052-114">getText (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="37052-114">getText (Client API reference)</span></span>](getText.md)

