---
title: getInitialValue (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 56fb62e6-d357-4096-bf4c-f4c1b543d633
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7e471f87e59d5bb1d6f7974db62a278eb7086e1b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386397"
---
# <a name="getinitialvalue-client-api-reference"></a><span data-ttu-id="208c0-102">getInitialValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="208c0-102">getInitialValue (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="208c0-103">Returns a value that represents the value set for a **Boolean**, **OptionSet** or **MultiSelectOptionSet** attribute when the form is opened.</span><span class="sxs-lookup"><span data-stu-id="208c0-103">Returns a value that represents the value set for a **Boolean**, **OptionSet** or **MultiSelectOptionSet** attribute when the form is opened.</span></span>

## <a name="attribute-types-supported"></a><span data-ttu-id="208c0-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="208c0-104">Attribute types supported</span></span>

<span data-ttu-id="208c0-105">Boolean, OptionSet, MultiSelectOptionSet</span><span class="sxs-lookup"><span data-stu-id="208c0-105">Boolean, OptionSet, MultiSelectOptionSet</span></span> 

## <a name="syntax"></a><span data-ttu-id="208c0-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="208c0-106">Syntax</span></span>

`formContext.getAttribute(arg).getInitialValue()`

## <a name="return-value"></a><span data-ttu-id="208c0-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="208c0-107">Return Value</span></span>

<span data-ttu-id="208c0-108">**Type**: Number</span><span class="sxs-lookup"><span data-stu-id="208c0-108">**Type**: Number</span></span>

<span data-ttu-id="208c0-109">**Description**: The initial value for the attribute.</span><span class="sxs-lookup"><span data-stu-id="208c0-109">**Description**: The initial value for the attribute.</span></span>


