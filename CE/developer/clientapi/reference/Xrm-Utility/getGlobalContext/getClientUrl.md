---
title: getClientUrl (Client API reference) in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 89123cde-7c66-4c7d-94e4-e287285019f8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c8601dc7540bf43c4867f4e57a49bc46b92e9e5f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387585"
---
# <a name="getclienturl-client-api-reference"></a><span data-ttu-id="bc3ee-102">getClientUrl (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="bc3ee-102">getClientUrl (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="bc3ee-103">Returns the base URL that was used to access the application.</span><span class="sxs-lookup"><span data-stu-id="bc3ee-103">Returns the base URL that was used to access the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3ee-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="bc3ee-104">Syntax</span></span>

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getClientUrl();
``` 

## <a name="return-value"></a><span data-ttu-id="bc3ee-105">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="bc3ee-105">Return Value</span></span>

<span data-ttu-id="bc3ee-106">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="bc3ee-106">**Type**: String</span></span>

<span data-ttu-id="bc3ee-107">**Description**: The values returned will resemble those listed in the following table.</span><span class="sxs-lookup"><span data-stu-id="bc3ee-107">**Description**: The values returned will resemble those listed in the following table.</span></span>


|             <span data-ttu-id="bc3ee-108">Value</span><span class="sxs-lookup"><span data-stu-id="bc3ee-108">Value</span></span>              |                                    <span data-ttu-id="bc3ee-109">Máy khách</span><span class="sxs-lookup"><span data-stu-id="bc3ee-109">Client</span></span>                                     |
|--------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="bc3ee-110">https://[org].crm.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="bc3ee-110">https://[org].crm.dynamics.com</span></span> |                   <span data-ttu-id="bc3ee-111">Ứng dụng Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="bc3ee-111">Dynamics 365 for Customer Engagement apps</span></span>                   |
|    <span data-ttu-id="bc3ee-112">http(s)://[server]/[org]</span><span class="sxs-lookup"><span data-stu-id="bc3ee-112">http(s)://[server]/[org]</span></span>    |                <span data-ttu-id="bc3ee-113">Dynamics 365 for Customer Engagement (on-premises) apps</span><span class="sxs-lookup"><span data-stu-id="bc3ee-113">Dynamics 365 for Customer Engagement (on-premises) apps</span></span>                |
|     http://localhost:2525      | <span data-ttu-id="bc3ee-114">Dynamics 365 for Outlook with Offline Access when offline</span><span class="sxs-lookup"><span data-stu-id="bc3ee-114">Dynamics 365 for Outlook with Offline Access when offline</span></span> |

### <a name="related-topics"></a><span data-ttu-id="bc3ee-115">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="bc3ee-115">Related topics</span></span>

[<span data-ttu-id="bc3ee-116">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="bc3ee-116">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)