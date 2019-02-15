---
title: getCurrentAppUrl (Client API reference)| MicrosoftDocs
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
ms.openlocfilehash: 4e45a90c0aad12598388f322a57bd53f3f41b6a0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388403"
---
# <a name="getcurrentappurl-client-api-reference"></a><span data-ttu-id="1ab64-102">getCurrentAppUrl (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="1ab64-102">getCurrentAppUrl (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="1ab64-103">Returns the URL of the current business app in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="1ab64-103">Returns the URL of the current business app in Customer Engagement.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab64-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="1ab64-104">Syntax</span></span>

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getCurrentAppUrl();
``` 

## <a name="return-value"></a><span data-ttu-id="1ab64-105">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="1ab64-105">Return Value</span></span>

<span data-ttu-id="1ab64-106">**Type**: String</span><span class="sxs-lookup"><span data-stu-id="1ab64-106">**Type**: String</span></span>

<span data-ttu-id="1ab64-107">**Description**: URL of the current business app.</span><span class="sxs-lookup"><span data-stu-id="1ab64-107">**Description**: URL of the current business app.</span></span> <span data-ttu-id="1ab64-108">Possible return values:</span><span class="sxs-lookup"><span data-stu-id="1ab64-108">Possible return values:</span></span>

|<span data-ttu-id="1ab64-109">Value</span><span class="sxs-lookup"><span data-stu-id="1ab64-109">Value</span></span> |<span data-ttu-id="1ab64-110">Máy khách</span><span class="sxs-lookup"><span data-stu-id="1ab64-110">Client</span></span> |
|---|---|
|<span data-ttu-id="1ab64-111">https://[org].crm.dynamics.com/main.aspx?appid=[GUID]</span><span class="sxs-lookup"><span data-stu-id="1ab64-111">https://[org].crm.dynamics.com/main.aspx?appid=[GUID]</span></span>|<span data-ttu-id="1ab64-112">Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="1ab64-112">Dynamics 365 for Customer Engagement apps</span></span> |
|<span data-ttu-id="1ab64-113">https://[server]/[org]/main.aspx?appid=[GUID]</span><span class="sxs-lookup"><span data-stu-id="1ab64-113">https://[server]/[org]/main.aspx?appid=[GUID]</span></span>|<span data-ttu-id="1ab64-114">Dynamics 365 for Customer Engagement (on-premises) apps</span><span class="sxs-lookup"><span data-stu-id="1ab64-114">Dynamics 365 for Customer Engagement (on-premises) apps</span></span> |

### <a name="related-topics"></a><span data-ttu-id="1ab64-115">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="1ab64-115">Related topics</span></span>

[<span data-ttu-id="1ab64-116">Create and manage custom business apps using code</span><span class="sxs-lookup"><span data-stu-id="1ab64-116">Create and manage custom business apps using code</span></span>](../../../../create-manage-custom-business-apps-using-code.md)

[<span data-ttu-id="1ab64-117">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="1ab64-117">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md) 