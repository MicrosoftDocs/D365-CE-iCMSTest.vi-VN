---
title: Link custom attributes of the recurring appointment master and appointment entities (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Link the custom attributes of the RecurringAppointmentMaster entity with custom attributes of the Appointment entity to automatically copy data.
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
- custom attributes, 1:1 mapping between
- schedule and appointment entities, linking custom attributes of a recurring appointment master (series)
- linking custom attributes of a recurring appointment master (series)
- schedule and appointment entities, custom attributes of a recurring appointment master
- custom attributes, affect of field-level security on
ms.assetid: 0480c355-6954-472c-8c9e-2129a3684364
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 15bfcec106728a0cda1373ab89069932eb96a8aa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387913"
---
# <a name="link-custom-attributes-of-the-recurring-appointment-master-and-appointment-entities"></a><span data-ttu-id="6b898-103">Link custom attributes of the recurring appointment master and appointment entities</span><span class="sxs-lookup"><span data-stu-id="6b898-103">Link custom attributes of the recurring appointment master and appointment entities</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6b898-104">You can link the custom attributes created for the `RecurringAppointmentMaster` entity with the custom attributes created for the `Appointment` entity to automatically copy the data from the recurring appointment master custom attribute to the linked recurring appointment instances custom attribute, every time it is expanded.</span><span class="sxs-lookup"><span data-stu-id="6b898-104">You can link the custom attributes created for the `RecurringAppointmentMaster` entity with the custom attributes created for the `Appointment` entity to automatically copy the data from the recurring appointment master custom attribute to the linked recurring appointment instances custom attribute, every time it is expanded.</span></span>  
  
 <span data-ttu-id="6b898-105">There is a 1:1 mapping between the custom attributes, which implies that a custom attribute of the recurring appointment master entity can be linked to only one custom attribute of the appointment entity.</span><span class="sxs-lookup"><span data-stu-id="6b898-105">There is a 1:1 mapping between the custom attributes, which implies that a custom attribute of the recurring appointment master entity can be linked to only one custom attribute of the appointment entity.</span></span> <span data-ttu-id="6b898-106">Moreover, the custom attributes that are to be linked together must be of the same type.</span><span class="sxs-lookup"><span data-stu-id="6b898-106">Moreover, the custom attributes that are to be linked together must be of the same type.</span></span> <span data-ttu-id="6b898-107">For example, you cannot link a custom attribute of type `string` with a `decimal` custom attribute.</span><span class="sxs-lookup"><span data-stu-id="6b898-107">For example, you cannot link a custom attribute of type `string` with a `decimal` custom attribute.</span></span> <span data-ttu-id="6b898-108">For information about different types of attributes, see [Customize Entity Attribute Metadata](customize-entity-attribute-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="6b898-108">For information about different types of attributes, see [Customize Entity Attribute Metadata](customize-entity-attribute-metadata.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6b898-109">You cannot link the custom attributes that have *field-level security* enabled.</span><span class="sxs-lookup"><span data-stu-id="6b898-109">You cannot link the custom attributes that have *field-level security* enabled.</span></span> <span data-ttu-id="6b898-110">Similarly, you cannot enable field-level security for linked custom attributes.</span><span class="sxs-lookup"><span data-stu-id="6b898-110">Similarly, you cannot enable field-level security for linked custom attributes.</span></span>  
  
### <a name="link-custom-attributes"></a><span data-ttu-id="6b898-111">Link custom attributes</span><span class="sxs-lookup"><span data-stu-id="6b898-111">Link custom attributes</span></span>  
  
1. <span data-ttu-id="6b898-112">Create a custom attribute for the appointment entity using the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> class.</span><span class="sxs-lookup"><span data-stu-id="6b898-112">Create a custom attribute for the appointment entity using the <xref:Microsoft.Xrm.Sdk.Messages.CreateAttributeRequest> class.</span></span>  
  
2. <span data-ttu-id="6b898-113">Create a custom attribute for the recurring appointment series (recurring appointment master) entity.</span><span class="sxs-lookup"><span data-stu-id="6b898-113">Create a custom attribute for the recurring appointment series (recurring appointment master) entity.</span></span> <span data-ttu-id="6b898-114">While specifying the attribute metadata for the custom attribute, use the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.LinkedAttributeId></span><span class="sxs-lookup"><span data-stu-id="6b898-114">While specifying the attribute metadata for the custom attribute, use the <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata>.<xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.LinkedAttributeId></span></span> <span data-ttu-id="6b898-115">property to link to the custom attribute that you created in step 1.</span><span class="sxs-lookup"><span data-stu-id="6b898-115">property to link to the custom attribute that you created in step 1.</span></span>  
  
3. <span data-ttu-id="6b898-116">Publish the changes to the solution.</span><span class="sxs-lookup"><span data-stu-id="6b898-116">Publish the changes to the solution.</span></span>  
  
   <span data-ttu-id="6b898-117">For sample code, see [Sample: Link Custom Attributes between Series and Instances](sample-link-custom-attributes-between-series-instances.md).</span><span class="sxs-lookup"><span data-stu-id="6b898-117">For sample code, see [Sample: Link Custom Attributes between Series and Instances](sample-link-custom-attributes-between-series-instances.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6b898-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6b898-118">See also</span></span>

 <span data-ttu-id="6b898-119">[Recurring Appointment Entities](recurring-appointment-entities.md) </span><span class="sxs-lookup"><span data-stu-id="6b898-119">[Recurring Appointment Entities](recurring-appointment-entities.md) </span></span>  
 <span data-ttu-id="6b898-120">[RecurringAppointmentMaster Entity](entities/recurringappointmentmaster.md) </span><span class="sxs-lookup"><span data-stu-id="6b898-120">[RecurringAppointmentMaster Entity](entities/recurringappointmentmaster.md) </span></span>  
 <span data-ttu-id="6b898-121">[Sample: Link Custom Attributes between Series and Instances](sample-link-custom-attributes-between-series-instances.md) </span><span class="sxs-lookup"><span data-stu-id="6b898-121">[Sample: Link Custom Attributes between Series and Instances](sample-link-custom-attributes-between-series-instances.md) </span></span>  
 [<span data-ttu-id="6b898-122">Customize Entity Attribute Metadata</span><span class="sxs-lookup"><span data-stu-id="6b898-122">Customize Entity Attribute Metadata</span></span>](customize-entity-attribute-metadata.md)
