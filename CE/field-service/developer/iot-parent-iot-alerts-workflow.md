---
title: IoT - Parent IoT Alerts workflow (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Links potential redundant IoT alerts to an existing parent alert.
ms.custom:
- dyn365-developer
- dyn365-fieldservice
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.technology:
- field-service
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 66ed4cef-33f3-4a15-b865-f8b9e8934b68
caps.latest.revision: 7
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
- D365FS
ms.openlocfilehash: 51d3473a3760a7460115233ba89fce5171d3da01
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388444"
---
# <a name="iot---parent-iot-alerts-workflow"></a><span data-ttu-id="f3cc3-103">IoT - Quy trình làm việc Cảnh báo IoT Chính</span><span class="sxs-lookup"><span data-stu-id="f3cc3-103">IoT - Parent IoT Alerts workflow</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f3cc3-104">The **IoT - Parent IoT Alerts** workflow links potential redundant alerts to an existing parent alert.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-104">The **IoT - Parent IoT Alerts** workflow links potential redundant alerts to an existing parent alert.</span></span>  
  
 <span data-ttu-id="f3cc3-105">Calls the <xref href="Microsoft.Dynamics.CRM.msdyn_ParentIoTAlerts?text=msdyn_ParentIoTAlerts Action" /> and passes 60 for the `TimespanSeconds` parameter.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-105">Calls the <xref href="Microsoft.Dynamics.CRM.msdyn_ParentIoTAlerts?text=msdyn_ParentIoTAlerts Action" /> and passes 60 for the `TimespanSeconds` parameter.</span></span> <span data-ttu-id="f3cc3-106">The primary entity for this workflow is [msdyn_iotalert Entity Reference](../../developer/entities/msdyn_iotalert.md).</span><span class="sxs-lookup"><span data-stu-id="f3cc3-106">The primary entity for this workflow is [msdyn_iotalert Entity Reference](../../developer/entities/msdyn_iotalert.md).</span></span>  
  
 <span data-ttu-id="f3cc3-107">This workflow is an example that ships with the thermostat sample solution.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-107">This workflow is an example that ships with the thermostat sample solution.</span></span> <span data-ttu-id="f3cc3-108">It demonstrates how to handle duplicate/redundant alerts to [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)], which typically occurs when a device malfunctions.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-108">It demonstrates how to handle duplicate/redundant alerts to [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)], which typically occurs when a device malfunctions.</span></span>  <span data-ttu-id="f3cc3-109">This is a recommended best practices approach, because unfiltered alerts can result in unwanted duplicated remedial processing, for example, multiple, redundant reset commands being sent or field service repair orders being generated.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-109">This is a recommended best practices approach, because unfiltered alerts can result in unwanted duplicated remedial processing, for example, multiple, redundant reset commands being sent or field service repair orders being generated.</span></span> <span data-ttu-id="f3cc3-110">These can also negatively affect the performance of your [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-110">These can also negatively affect the performance of your [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] instance.</span></span> <span data-ttu-id="f3cc3-111">(The thermostat sample is coded to filter duplicate alerts so that they are not passed to [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)], which is also a recommended practice.)</span><span class="sxs-lookup"><span data-stu-id="f3cc3-111">(The thermostat sample is coded to filter duplicate alerts so that they are not passed to [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)], which is also a recommended practice.)</span></span>  
  
 <span data-ttu-id="f3cc3-112">This workflow is enabled by default, but can be deactivated or edited by users; for example, the time span can be modified.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-112">This workflow is enabled by default, but can be deactivated or edited by users; for example, the time span can be modified.</span></span>  
  
<a name="bkmk_Parameters"></a>   
## <a name="parameters"></a><span data-ttu-id="f3cc3-113">Tham số</span><span class="sxs-lookup"><span data-stu-id="f3cc3-113">Parameters</span></span>  
 <span data-ttu-id="f3cc3-114">Parameter(s) allow for data to be passed to the workflow.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-114">Parameter(s) allow for data to be passed to the workflow.</span></span>  
  
|<span data-ttu-id="f3cc3-115">Tên</span><span class="sxs-lookup"><span data-stu-id="f3cc3-115">Name</span></span>|<span data-ttu-id="f3cc3-116">Loại</span><span class="sxs-lookup"><span data-stu-id="f3cc3-116">Type</span></span>|<span data-ttu-id="f3cc3-117">Không có</span><span class="sxs-lookup"><span data-stu-id="f3cc3-117">Nullable</span></span>|<span data-ttu-id="f3cc3-118">Unicode</span><span class="sxs-lookup"><span data-stu-id="f3cc3-118">Unicode</span></span>|<span data-ttu-id="f3cc3-119">Mô tả</span><span class="sxs-lookup"><span data-stu-id="f3cc3-119">Description</span></span>|  
|----------|----------|--------------|-------------|-----------------|  
|<span data-ttu-id="f3cc3-120">TimespanSeconds</span><span class="sxs-lookup"><span data-stu-id="f3cc3-120">TimespanSeconds</span></span>|<span data-ttu-id="f3cc3-121">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="f3cc3-121">Edm.Int32</span></span>|<span data-ttu-id="f3cc3-122">false</span><span class="sxs-lookup"><span data-stu-id="f3cc3-122">false</span></span>||<span data-ttu-id="f3cc3-123">Determines the time window to consider when parenting (or suppressing) an alert, from 60 to 180 seconds.</span><span class="sxs-lookup"><span data-stu-id="f3cc3-123">Determines the time window to consider when parenting (or suppressing) an alert, from 60 to 180 seconds.</span></span>|
| | | | | |
