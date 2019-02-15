---
title: setUtcValue (Client API reference)| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e7f770ac-ee19-46dd-babb-44127c299411
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 475a48599ce1913e20db61ff244daef658e6d0ff
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386712"
---
# <a name="setutcvalue-client-api-reference"></a><span data-ttu-id="6dc08-102">setUtcValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="6dc08-102">setUtcValue (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6dc08-103">Sets a UTC date and time value for a **datetime** type of attribute.</span><span class="sxs-lookup"><span data-stu-id="6dc08-103">Sets a UTC date and time value for a **datetime** type of attribute.</span></span> <span data-ttu-id="6dc08-104">UTC stands for Coordinated Universal Time.</span><span class="sxs-lookup"><span data-stu-id="6dc08-104">UTC stands for Coordinated Universal Time.</span></span>

> [!NOTE]
> <span data-ttu-id="6dc08-105">Attributes on quick create forms won't save values set using this method.</span><span class="sxs-lookup"><span data-stu-id="6dc08-105">Attributes on quick create forms won't save values set using this method.</span></span> 

## <a name="attribute-types-supported"></a><span data-ttu-id="6dc08-106">Attribute types supported</span><span class="sxs-lookup"><span data-stu-id="6dc08-106">Attribute types supported</span></span>

<span data-ttu-id="6dc08-107">ngày giờ</span><span class="sxs-lookup"><span data-stu-id="6dc08-107">datetime</span></span>

## <a name="syntax"></a><span data-ttu-id="6dc08-108">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="6dc08-108">Syntax</span></span>

`formContext.getAttribute(arg).setUtcValue(value)`

## <a name="parameters"></a><span data-ttu-id="6dc08-109">Tham số</span><span class="sxs-lookup"><span data-stu-id="6dc08-109">Parameters</span></span>

<span data-ttu-id="6dc08-110">**Type**: datetime.</span><span class="sxs-lookup"><span data-stu-id="6dc08-110">**Type**: datetime.</span></span> 

<span data-ttu-id="6dc08-111">**Description**: The UTC date and time value.</span><span class="sxs-lookup"><span data-stu-id="6dc08-111">**Description**: The UTC date and time value.</span></span>

### <a name="related-topic"></a><span data-ttu-id="6dc08-112">Related topic</span><span class="sxs-lookup"><span data-stu-id="6dc08-112">Related topic</span></span>
[<span data-ttu-id="6dc08-113">getUtcValue (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="6dc08-113">getUtcValue (Client API reference)</span></span>](getUtcValue.md)

