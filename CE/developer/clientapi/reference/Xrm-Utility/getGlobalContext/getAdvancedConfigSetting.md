---
title: getAdvancedConfigSetting (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
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
ms.openlocfilehash: 6eceb6e623b9bba2d59eb9c6a8a1acd57a019e08
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388796"
---
# <a name="getadvancedconfigsetting-client-api-reference"></a><span data-ttu-id="767a3-102">getAdvancedConfigSetting (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="767a3-102">getAdvancedConfigSetting (Client API reference)</span></span>

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="767a3-103">Returns information about the advanced configuration settings for the organization.</span><span class="sxs-lookup"><span data-stu-id="767a3-103">Returns information about the advanced configuration settings for the organization.</span></span> 

## <a name="syntax"></a><span data-ttu-id="767a3-104">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="767a3-104">Syntax</span></span>

```JavaScript
var globalContext = Xrm.Utility.getGlobalContext();
globalContext.getAdvancedConfigSetting(setting);
```

## <a name="parameters"></a><span data-ttu-id="767a3-105">Tham số</span><span class="sxs-lookup"><span data-stu-id="767a3-105">Parameters</span></span>

|<span data-ttu-id="767a3-106">Tên</span><span class="sxs-lookup"><span data-stu-id="767a3-106">Name</span></span> |<span data-ttu-id="767a3-107">Loại</span><span class="sxs-lookup"><span data-stu-id="767a3-107">Type</span></span> |<span data-ttu-id="767a3-108">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="767a3-108">Required</span></span> |<span data-ttu-id="767a3-109">Mô tả</span><span class="sxs-lookup"><span data-stu-id="767a3-109">Description</span></span> |
|---|---|---|---|
|<span data-ttu-id="767a3-110">setting</span><span class="sxs-lookup"><span data-stu-id="767a3-110">setting</span></span> |<span data-ttu-id="767a3-111">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="767a3-111">String</span></span> |<span data-ttu-id="767a3-112">Có</span><span class="sxs-lookup"><span data-stu-id="767a3-112">Yes</span></span> |<span data-ttu-id="767a3-113">Name of the configuration setting.</span><span class="sxs-lookup"><span data-stu-id="767a3-113">Name of the configuration setting.</span></span> <br/><span data-ttu-id="767a3-114">Only the following two configuration settings are supported: **"MaxChildIncidentNumber"** and **"MaxIncidentMergeNumber"**</span><span class="sxs-lookup"><span data-stu-id="767a3-114">Only the following two configuration settings are supported: **"MaxChildIncidentNumber"** and **"MaxIncidentMergeNumber"**</span></span> |

## <a name="return-value"></a><span data-ttu-id="767a3-115">Giá trị trả lại</span><span class="sxs-lookup"><span data-stu-id="767a3-115">Return Value</span></span>

<span data-ttu-id="767a3-116">Returns the advanced configuration setting value.</span><span class="sxs-lookup"><span data-stu-id="767a3-116">Returns the advanced configuration setting value.</span></span>

### <a name="related-topics"></a><span data-ttu-id="767a3-117">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="767a3-117">Related topics</span></span>

[<span data-ttu-id="767a3-118">Xrm.Utility.getGlobalContext</span><span class="sxs-lookup"><span data-stu-id="767a3-118">Xrm.Utility.getGlobalContext</span></span>](../getGlobalContext.md)



