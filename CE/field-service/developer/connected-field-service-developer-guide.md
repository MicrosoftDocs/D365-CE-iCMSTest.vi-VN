---
title: Develop customized IoT solutions in Connected Field Service | MicrosoftDocs
description: Connected Field Service integrates Internet of Things (IoT) devices with Dynamics 365 for Customer Engagement (online) to enable their registration, monitoring and management into established business processes.
ms.custom:
- dyn365-developer
- dyn365-fieldservice
ms.date: 01/05/2018
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.technology:
- field-service
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: b210b88e-3447-43a7-845e-23d6e7a94331
caps.latest.revision: 8
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
- D365FS
ms.openlocfilehash: 31b59f250117ad6d0f2206e0d0577d825b37c1f1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387176"
---
# <a name="develop-customized-iot-solutions-in-connected-field-service"></a><span data-ttu-id="13167-103">Develop customized IoT solutions in Connected Field Service</span><span class="sxs-lookup"><span data-stu-id="13167-103">Develop customized IoT solutions in Connected Field Service</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_connected_field_service_msdyn365](../../includes/pn-connected-field-service-msdyn365.md)] <span data-ttu-id="13167-104">integrates Internet of Things (IoT) devices with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] to enable their registration, monitoring and management into established business processes.</span><span class="sxs-lookup"><span data-stu-id="13167-104">integrates Internet of Things (IoT) devices with [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] to enable their registration, monitoring and management into established business processes.</span></span> <span data-ttu-id="13167-105">This guide explains the component architecture, supplied interfaces and customization points, and explains the approach to develop customized IoT solutions.</span><span class="sxs-lookup"><span data-stu-id="13167-105">This guide explains the component architecture, supplied interfaces and customization points, and explains the approach to develop customized IoT solutions.</span></span>  
  
## <a name="supported-developer-scenarios"></a><span data-ttu-id="13167-106">Supported Developer Scenarios</span><span class="sxs-lookup"><span data-stu-id="13167-106">Supported Developer Scenarios</span></span>  
 <span data-ttu-id="13167-107">The initial release of Connected Field Service supports the following two primary development scenarios:</span><span class="sxs-lookup"><span data-stu-id="13167-107">The initial release of Connected Field Service supports the following two primary development scenarios:</span></span>  
  
- <span data-ttu-id="13167-108">Extend [!INCLUDE[pn_connected_field_service_msdyn365](../../includes/pn-connected-field-service-msdyn365.md)] so that manufacturers and hardware service organizations can register, monitor, and manage—including controlling and correcting—IoT devices.</span><span class="sxs-lookup"><span data-stu-id="13167-108">Extend [!INCLUDE[pn_connected_field_service_msdyn365](../../includes/pn-connected-field-service-msdyn365.md)] so that manufacturers and hardware service organizations can register, monitor, and manage—including controlling and correcting—IoT devices.</span></span> <span data-ttu-id="13167-109">Future releases will provide additional support for predicative and prescriptive maintenance capabilities.</span><span class="sxs-lookup"><span data-stu-id="13167-109">Future releases will provide additional support for predicative and prescriptive maintenance capabilities.</span></span>  
  
- <span data-ttu-id="13167-110">Provide an IoT Platform that ISVs and partners can build on to IOT-enable their [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] custom entities and managed solutions.</span><span class="sxs-lookup"><span data-stu-id="13167-110">Provide an IoT Platform that ISVs and partners can build on to IOT-enable their [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] custom entities and managed solutions.</span></span>  
  
  <span data-ttu-id="13167-111">To enable the first scenario, the following capabilities are supported:</span><span class="sxs-lookup"><span data-stu-id="13167-111">To enable the first scenario, the following capabilities are supported:</span></span>  
  
- <span data-ttu-id="13167-112">Abstract device registration in an action, so that devices can be easily registered using the CRM web client or the mobile client</span><span class="sxs-lookup"><span data-stu-id="13167-112">Abstract device registration in an action, so that devices can be easily registered using the CRM web client or the mobile client</span></span>  
  
- <span data-ttu-id="13167-113">Enable any CRM entity to be IOT-enabled, enabling straightforward IoT integration within existing business processes by using [Connection entities](../../developer/connection-entities.md)</span><span class="sxs-lookup"><span data-stu-id="13167-113">Enable any CRM entity to be IOT-enabled, enabling straightforward IoT integration within existing business processes by using [Connection entities](../../developer/connection-entities.md)</span></span>  
  
- <span data-ttu-id="13167-114">Receive service alerts and automating their response with a customized workflow</span><span class="sxs-lookup"><span data-stu-id="13167-114">Receive service alerts and automating their response with a customized workflow</span></span>  
  
- <span data-ttu-id="13167-115">Send remote commands to IoT devices, for example after diagnosing a problem to correct a malfunctioning device</span><span class="sxs-lookup"><span data-stu-id="13167-115">Send remote commands to IoT devices, for example after diagnosing a problem to correct a malfunctioning device</span></span>  
  
- <span data-ttu-id="13167-116">Analyze incoming device data, and displaying aggregate, trend and other metrics in custom dashboards</span><span class="sxs-lookup"><span data-stu-id="13167-116">Analyze incoming device data, and displaying aggregate, trend and other metrics in custom dashboards</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="13167-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="13167-117">See also</span></span>  
 <span data-ttu-id="13167-118">[Connected Field Service architecture](connected-field-service-architecture.md) </span><span class="sxs-lookup"><span data-stu-id="13167-118">[Connected Field Service architecture](connected-field-service-architecture.md) </span></span>  
 [<span data-ttu-id="13167-119">Mở rộng các giải pháp Connected Field Service</span><span class="sxs-lookup"><span data-stu-id="13167-119">Extend Connected Field Service solutions</span></span>](extend-connected-field-service-solutions.md)<br>
 [<span data-ttu-id="13167-120">Hướng dẫn về Dynamics 365 for Customer Engagement dành cho nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="13167-120">Developer Guide for Dynamics 365 for Customer Engagement</span></span>](../../developer/developer-guide.md)   
