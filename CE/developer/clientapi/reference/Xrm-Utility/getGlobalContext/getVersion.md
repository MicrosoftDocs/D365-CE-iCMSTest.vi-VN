---
title: getVersion (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 2fd5c43e-5a01-431d-ac2c-abefdb8d06ac
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b7be6e9f4ab3680849063197daa8aeb6d715b8f2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388446"
---
# <a name="getversion-client-api-reference"></a><span data-ttu-id="5a68d-102">getVersion (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="5a68d-102">getVersion (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5a68d-103">Returns the version number of the Dynamics 365 for Customer Engagement apps instance.</span><span class="sxs-lookup"><span data-stu-id="5a68d-103">Returns the version number of the Dynamics 365 for Customer Engagement apps instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a68d-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="5a68d-104">Syntax</span></span>

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getVersion();
``` 
## <a name="return-value"></a><span data-ttu-id="5a68d-105">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="5a68d-105">Return Value</span></span>

<span data-ttu-id="5a68d-106">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="5a68d-106">**Type**: String</span></span>

<span data-ttu-id="5a68d-107">**Description**: Version of the Customer Engagement instance.</span><span class="sxs-lookup"><span data-stu-id="5a68d-107">**Description**: Version of the Customer Engagement instance.</span></span> <span data-ttu-id="5a68d-108">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="5a68d-108">For example:</span></span>

`"9.0.0.1103"`

### <a name="related-topics"></a><span data-ttu-id="5a68d-109">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="5a68d-109">Related topics</span></span>

[<span data-ttu-id="5a68d-110">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="5a68d-110">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)
