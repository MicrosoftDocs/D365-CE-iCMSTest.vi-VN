---
title: getActiveProcess (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: a977a250-b79f-4c88-a6af-776350b110f7
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7f8266d7beb146fe0c452b135b44bd2174e0fbbb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386392"
---
# <a name="getactiveprocess-client-api-reference"></a><span data-ttu-id="c7fb5-102">getActiveProcess (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="c7fb5-102">getActiveProcess (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getActiveProcess-description.md](./includes/getActiveProcess-description.md)]

## <a name="syntax"></a><span data-ttu-id="c7fb5-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="c7fb5-103">Syntax</span></span>

`var activeProcess = formContext.data.process.getActiveProcess();`

## <a name="return-value"></a><span data-ttu-id="c7fb5-104">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="c7fb5-104">Return Value</span></span>

<span data-ttu-id="c7fb5-105">**Type**: Process.</span><span class="sxs-lookup"><span data-stu-id="c7fb5-105">**Type**: Process.</span></span> 

<span data-ttu-id="c7fb5-106">**Description**: The currently active process.</span><span class="sxs-lookup"><span data-stu-id="c7fb5-106">**Description**: The currently active process.</span></span> <span data-ttu-id="c7fb5-107">See [Process methods](../../formContext-data-process.md#process-methods) for the methods to access the properties of the process returned.</span><span class="sxs-lookup"><span data-stu-id="c7fb5-107">See [Process methods](../../formContext-data-process.md#process-methods) for the methods to access the properties of the process returned.</span></span>

### <a name="related-topics"></a><span data-ttu-id="c7fb5-108">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="c7fb5-108">Related topics</span></span>

[<span data-ttu-id="c7fb5-109">setActiveProcess)</span><span class="sxs-lookup"><span data-stu-id="c7fb5-109">setActiveProcess)</span></span>](setActiveProcess.md)

[<span data-ttu-id="c7fb5-110">formContext.data.process</span><span class="sxs-lookup"><span data-stu-id="c7fb5-110">formContext.data.process</span></span>](../../formContext-data-process.md)
 


