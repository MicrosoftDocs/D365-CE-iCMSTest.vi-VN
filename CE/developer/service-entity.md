---
title: Service entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The Service entity represents a service made available to a customer, with attributes that include the standard duration of the service, when the service is offered, and its required resources.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- service entity, resource requirements; availability; and specifications
- schedule and appointment entities, service entity
- service entity, introduction
- service entity
- service entity, service booking
- service entity, service engine
- service booking, service entity
- service entity, definition
- resource requirements; availability; and specifications, service entity
ms.assetid: ed077e11-8af6-4f9b-a1f3-4feefeae1f4e
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 43cc54d2a7dce6f2a9c3a50eb44862414e09d110
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386745"
---
# <a name="service-entity"></a><span data-ttu-id="9acce-103">Service entity</span><span class="sxs-lookup"><span data-stu-id="9acce-103">Service entity</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="9acce-104">A service is work that is performed for a customer.</span><span class="sxs-lookup"><span data-stu-id="9acce-104">A service is work that is performed for a customer.</span></span> <span data-ttu-id="9acce-105">The definition typically includes service attributes such as name, duration, granularity, calendar restrictions, and resource requirements.</span><span class="sxs-lookup"><span data-stu-id="9acce-105">The definition typically includes service attributes such as name, duration, granularity, calendar restrictions, and resource requirements.</span></span> <span data-ttu-id="9acce-106">A `Service` entity represents a service made available to a customer, with attributes that include the standard duration of the service, when the service can be offered, and required resources, which is described by the `ResourceSpec` class.</span><span class="sxs-lookup"><span data-stu-id="9acce-106">A `Service` entity represents a service made available to a customer, with attributes that include the standard duration of the service, when the service can be offered, and required resources, which is described by the `ResourceSpec` class.</span></span>  
  
 <span data-ttu-id="9acce-107">For example, a dental cleaning service definition may include resource requirements for a hygienist, a dental cleaning chair, a patient, and a duration limit of 90 minutes.</span><span class="sxs-lookup"><span data-stu-id="9acce-107">For example, a dental cleaning service definition may include resource requirements for a hygienist, a dental cleaning chair, a patient, and a duration limit of 90 minutes.</span></span> <span data-ttu-id="9acce-108">The definition may also include additional parameterized constraints that are evaluated during availability search.</span><span class="sxs-lookup"><span data-stu-id="9acce-108">The definition may also include additional parameterized constraints that are evaluated during availability search.</span></span> <span data-ttu-id="9acce-109">In this service definition, a constraint may be defined that the "patient" resource must have a valid insurance provider identification number.</span><span class="sxs-lookup"><span data-stu-id="9acce-109">In this service definition, a constraint may be defined that the "patient" resource must have a valid insurance provider identification number.</span></span> <span data-ttu-id="9acce-110">This constraint example uses a custom attribute added to the resource for the insurance provider identification number.</span><span class="sxs-lookup"><span data-stu-id="9acce-110">This constraint example uses a custom attribute added to the resource for the insurance provider identification number.</span></span>  
  
 <span data-ttu-id="9acce-111">For each resource specification, there is an objective that ranks available resources from most suitable to least.</span><span class="sxs-lookup"><span data-stu-id="9acce-111">For each resource specification, there is an objective that ranks available resources from most suitable to least.</span></span> <span data-ttu-id="9acce-112">For example, the busiest nurse, least busy doctor, or the cheapest resource.</span><span class="sxs-lookup"><span data-stu-id="9acce-112">For example, the busiest nurse, least busy doctor, or the cheapest resource.</span></span>  
  
 <span data-ttu-id="9acce-113">To start using [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] service scheduling to manage your service delivery process, you must first create a model of your service business.</span><span class="sxs-lookup"><span data-stu-id="9acce-113">To start using [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] service scheduling to manage your service delivery process, you must first create a model of your service business.</span></span> <span data-ttu-id="9acce-114">To do this, you create a `Resource` record or an `Equipment` record for the people and equipment that you want to schedule and you create `Service` records for the services you offer.</span><span class="sxs-lookup"><span data-stu-id="9acce-114">To do this, you create a `Resource` record or an `Equipment` record for the people and equipment that you want to schedule and you create `Service` records for the services you offer.</span></span> <span data-ttu-id="9acce-115">When you define the service, you can describe which resources are required for each service by using a series of resource specifications (`ResourceSpec`).</span><span class="sxs-lookup"><span data-stu-id="9acce-115">When you define the service, you can describe which resources are required for each service by using a series of resource specifications (`ResourceSpec`).</span></span> <span data-ttu-id="9acce-116">Then, you can model the business rules that govern service availability into the system.</span><span class="sxs-lookup"><span data-stu-id="9acce-116">Then, you can model the business rules that govern service availability into the system.</span></span> <span data-ttu-id="9acce-117">These rules include things such as the working hours of the service delivery personnel, and any special restrictions on services.</span><span class="sxs-lookup"><span data-stu-id="9acce-117">These rules include things such as the working hours of the service delivery personnel, and any special restrictions on services.</span></span> <span data-ttu-id="9acce-118">After this information is defined, the scheduling engine has what it must have to manage the service delivery schedule.</span><span class="sxs-lookup"><span data-stu-id="9acce-118">After this information is defined, the scheduling engine has what it must have to manage the service delivery schedule.</span></span>  
  
 <span data-ttu-id="9acce-119">Service booking granularity determines the time interval on which availability is displayed to users.</span><span class="sxs-lookup"><span data-stu-id="9acce-119">Service booking granularity determines the time interval on which availability is displayed to users.</span></span> <span data-ttu-id="9acce-120">Typically, this is something like "every 15 minutes" or "every hour on the hour."</span><span class="sxs-lookup"><span data-stu-id="9acce-120">Typically, this is something like "every 15 minutes" or "every hour on the hour."</span></span> <span data-ttu-id="9acce-121">Duration is the time that is required to perform the service.</span><span class="sxs-lookup"><span data-stu-id="9acce-121">Duration is the time that is required to perform the service.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9acce-122">In This Section</span><span class="sxs-lookup"><span data-stu-id="9acce-122">In This Section</span></span>  
 [<span data-ttu-id="9acce-123">Service Entity</span><span class="sxs-lookup"><span data-stu-id="9acce-123">Service Entity</span></span>](entities/service.md)
