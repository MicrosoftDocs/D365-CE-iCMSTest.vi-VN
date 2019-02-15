---
title: getOption (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e334d2d9-91c0-4953-956d-444a84dc9da2
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4d26daf4ea2b97841924c6bf4ee2ca9a646e41c6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387878"
---
# <a name="getoption-client-api-reference"></a><span data-ttu-id="70ec6-102">getOption (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="70ec6-102">getOption (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="70ec6-103">Returns an option object with the value matching the argument (label or enumeration value) passed to the method.</span><span class="sxs-lookup"><span data-stu-id="70ec6-103">Returns an option object with the value matching the argument (label or enumeration value) passed to the method.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="70ec6-104">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="70ec6-104">Attribute types supported</span></span>

<span data-ttu-id="70ec6-105">OptionSet, MultiSelectOptionSet</span><span class="sxs-lookup"><span data-stu-id="70ec6-105">OptionSet, MultiSelectOptionSet</span></span>

## <a name="syntax"></a><span data-ttu-id="70ec6-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="70ec6-106">Syntax</span></span>

`formContext.getAttribute(arg).getOption(value)`

## <a name="parameters"></a><span data-ttu-id="70ec6-107">Tham số</span><span class="sxs-lookup"><span data-stu-id="70ec6-107">Parameters</span></span>

<span data-ttu-id="70ec6-108">**String** (label of the option) or **Number** (enumeration value of the option).</span><span class="sxs-lookup"><span data-stu-id="70ec6-108">**String** (label of the option) or **Number** (enumeration value of the option).</span></span>

## <a name="return-value"></a><span data-ttu-id="70ec6-109">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="70ec6-109">Return Value</span></span>

<span data-ttu-id="70ec6-110">**Type**: Option object.</span><span class="sxs-lookup"><span data-stu-id="70ec6-110">**Type**: Option object.</span></span> 

<span data-ttu-id="70ec6-111">**Description**: The logical name of the attribute.</span><span class="sxs-lookup"><span data-stu-id="70ec6-111">**Description**: The logical name of the attribute.</span></span>

