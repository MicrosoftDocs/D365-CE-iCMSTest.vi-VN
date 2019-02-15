---
title: getEntityTypes (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c20ba958-821f-4168-a518-e39431603b28
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 98e1a172f5bb21f9b24c58bbe0a158ed22e940be
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387444"
---
# <a name="getentitytypes-client-api-reference"></a><span data-ttu-id="aa523-102">getEntityTypes (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="aa523-102">getEntityTypes (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="aa523-103">Gets the types of entities allowed in the lookup control.</span><span class="sxs-lookup"><span data-stu-id="aa523-103">Gets the types of entities allowed in the lookup control.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="aa523-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="aa523-104">Control types supported</span></span>

<span data-ttu-id="aa523-105">Lookup control</span><span class="sxs-lookup"><span data-stu-id="aa523-105">Lookup control</span></span>

## <a name="syntax"></a><span data-ttu-id="aa523-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="aa523-106">Syntax</span></span>

`formContext.getControl(arg).getEntityTypes();`

## <a name="return-value"></a><span data-ttu-id="aa523-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="aa523-107">Return Value</span></span>

<span data-ttu-id="aa523-108">**Type**: Array of String</span><span class="sxs-lookup"><span data-stu-id="aa523-108">**Type**: Array of String</span></span>

<span data-ttu-id="aa523-109">**Description**: The logical names of the entities allowed in this control.</span><span class="sxs-lookup"><span data-stu-id="aa523-109">**Description**: The logical names of the entities allowed in this control.</span></span>

### <a name="related-topics"></a><span data-ttu-id="aa523-110">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="aa523-110">Related topics</span></span>

[<span data-ttu-id="aa523-111">setEntityTypes</span><span class="sxs-lookup"><span data-stu-id="aa523-111">setEntityTypes</span></span>](setEntityTypes.md)
