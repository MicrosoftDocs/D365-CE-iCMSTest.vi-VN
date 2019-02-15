---
title: getSrc (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: e003d21f-393a-4681-a6fc-256949167fcc
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a5e2893d5da10fef03122412dfbc3262479aa242
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385843"
---
# <a name="getsrc-client-api-reference"></a><span data-ttu-id="d67ed-102">getSrc (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="d67ed-102">getSrc (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d67ed-103">Returns the current URL being displayed in an IFRAME or web resource.</span><span class="sxs-lookup"><span data-stu-id="d67ed-103">Returns the current URL being displayed in an IFRAME or web resource.</span></span> 

## <a name="control-types-supported"></a><span data-ttu-id="d67ed-104">Control types supported</span><span class="sxs-lookup"><span data-stu-id="d67ed-104">Control types supported</span></span>

<span data-ttu-id="d67ed-105">iframe, webresource</span><span class="sxs-lookup"><span data-stu-id="d67ed-105">iframe, webresource</span></span>

## <a name="syntax"></a><span data-ttu-id="d67ed-106">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="d67ed-106">Syntax</span></span>

`formContext.getControl(arg).getSrc();`

## <a name="return-value"></a><span data-ttu-id="d67ed-107">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="d67ed-107">Return Value</span></span>

<span data-ttu-id="d67ed-108">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="d67ed-108">**Type**: String</span></span>

<span data-ttu-id="d67ed-109">**Description**: A URL representing the **src** property of the IFRAME or web resource.</span><span class="sxs-lookup"><span data-stu-id="d67ed-109">**Description**: A URL representing the **src** property of the IFRAME or web resource.</span></span>

### <a name="related-topics"></a><span data-ttu-id="d67ed-110">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="d67ed-110">Related topics</span></span>

[<span data-ttu-id="d67ed-111">setSrc</span><span class="sxs-lookup"><span data-stu-id="d67ed-111">setSrc</span></span>](setSrc.md)

