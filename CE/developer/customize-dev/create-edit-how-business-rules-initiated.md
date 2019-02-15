---
title: Create or edit how business rules are initiated | MicrosoftDocs
description: Business rules allow for defining logic that takes place in a form. Business rules provide an alternative to form scripts because they can be defined within a user interface without writing code.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 250c9a3b-7ae1-480d-8bac-0ac72a32bc4f
caps.latest.revision: 12
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 041c91884258a19ac7ab34b9d96a91067f4e5d34
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386425"
---
# <a name="create-or-edit-how-business-rules-are-initiated"></a><span data-ttu-id="555a0-104">Create or edit how business rules are initiated</span><span class="sxs-lookup"><span data-stu-id="555a0-104">Create or edit how business rules are initiated</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="555a0-105">Business rules allow for defining logic that takes place in a form.</span><span class="sxs-lookup"><span data-stu-id="555a0-105">Business rules allow for defining logic that takes place in a form.</span></span> <span data-ttu-id="555a0-106">Business rules provide an alternative to form scripts because they can be defined within a user interface without writing code.</span><span class="sxs-lookup"><span data-stu-id="555a0-106">Business rules provide an alternative to form scripts because they can be defined within a user interface without writing code.</span></span> <span data-ttu-id="555a0-107">Business rules do not offer any opportunities for the actions they perform to be extended in this release, but by using the Process Trigger entity, you can modify how existing business rules are initiated or register an existing business rule to different events that will initiate it.</span><span class="sxs-lookup"><span data-stu-id="555a0-107">Business rules do not offer any opportunities for the actions they perform to be extended in this release, but by using the Process Trigger entity, you can modify how existing business rules are initiated or register an existing business rule to different events that will initiate it.</span></span>

 [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="555a0-108">[Tạo quy các tắc công việc và đề xuất](../../customize/create-business-rules-recommendations-apply-logic-form.md)</span><span class="sxs-lookup"><span data-stu-id="555a0-108">[Create business rules and recommendations](../../customize/create-business-rules-recommendations-apply-logic-form.md)</span></span>

## <a name="registering-business-rules"></a><span data-ttu-id="555a0-109">Registering business rules</span><span class="sxs-lookup"><span data-stu-id="555a0-109">Registering business rules</span></span>

 <span data-ttu-id="555a0-110">When you create a business rule, you must set the scope and configure conditions that will initiate the business rule.</span><span class="sxs-lookup"><span data-stu-id="555a0-110">When you create a business rule, you must set the scope and configure conditions that will initiate the business rule.</span></span> <span data-ttu-id="555a0-111">The business rule editor stores this information in the Process Trigger entity.</span><span class="sxs-lookup"><span data-stu-id="555a0-111">The business rule editor stores this information in the Process Trigger entity.</span></span> <span data-ttu-id="555a0-112">You can read, create, update, and delete process trigger records to modify how business rules are initiated.</span><span class="sxs-lookup"><span data-stu-id="555a0-112">You can read, create, update, and delete process trigger records to modify how business rules are initiated.</span></span>

 <span data-ttu-id="555a0-113">The primary scenarios for working with the process trigger entity are:</span><span class="sxs-lookup"><span data-stu-id="555a0-113">The primary scenarios for working with the process trigger entity are:</span></span>
- <span data-ttu-id="555a0-114">Clone a business rule that is applied to one or more forms to another form.</span><span class="sxs-lookup"><span data-stu-id="555a0-114">Clone a business rule that is applied to one or more forms to another form.</span></span>
- <span data-ttu-id="555a0-115">Modify a business rule that is applied to one or more forms so that it applies to all forms.</span><span class="sxs-lookup"><span data-stu-id="555a0-115">Modify a business rule that is applied to one or more forms so that it applies to all forms.</span></span>
- <span data-ttu-id="555a0-116">Modify a business rule that is applied to all forms so that it applies only to one or more specific forms.</span><span class="sxs-lookup"><span data-stu-id="555a0-116">Modify a business rule that is applied to all forms so that it applies only to one or more specific forms.</span></span>
- <span data-ttu-id="555a0-117">Register a business rule to be applied on the Save event.</span><span class="sxs-lookup"><span data-stu-id="555a0-117">Register a business rule to be applied on the Save event.</span></span>

> [!NOTE]
> <span data-ttu-id="555a0-118">If you use the business rule editor to modify a business rule that has been programmatically set to be applied on the Save event, it will revert to either load or change.</span><span class="sxs-lookup"><span data-stu-id="555a0-118">If you use the business rule editor to modify a business rule that has been programmatically set to be applied on the Save event, it will revert to either load or change.</span></span> <span data-ttu-id="555a0-119">You must re-apply the change programmatically to have the rule applied on the Save event.</span><span class="sxs-lookup"><span data-stu-id="555a0-119">You must re-apply the change programmatically to have the rule applied on the Save event.</span></span>

 <span data-ttu-id="555a0-120">The following table describes relevant process trigger entity attributes.</span><span class="sxs-lookup"><span data-stu-id="555a0-120">The following table describes relevant process trigger entity attributes.</span></span>

|<span data-ttu-id="555a0-121">SchemaName</span><span class="sxs-lookup"><span data-stu-id="555a0-121">SchemaName</span></span>|<span data-ttu-id="555a0-122">Loại</span><span class="sxs-lookup"><span data-stu-id="555a0-122">Type</span></span>|<span data-ttu-id="555a0-123">Mô tả</span><span class="sxs-lookup"><span data-stu-id="555a0-123">Description</span></span>|
|----------------|----------|-----------------|
|`ControlName`|<span data-ttu-id="555a0-124">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="555a0-124">String</span></span>|<span data-ttu-id="555a0-125">Name of the attribute that a change event is registered for.</span><span class="sxs-lookup"><span data-stu-id="555a0-125">Name of the attribute that a change event is registered for.</span></span> <span data-ttu-id="555a0-126">For other events this value is null.</span><span class="sxs-lookup"><span data-stu-id="555a0-126">For other events this value is null.</span></span>|
|`ControlType`|<span data-ttu-id="555a0-127">Danh sách chọn</span><span class="sxs-lookup"><span data-stu-id="555a0-127">Picklist</span></span>|<span data-ttu-id="555a0-128">Type of the control to which this trigger is bound.</span><span class="sxs-lookup"><span data-stu-id="555a0-128">Type of the control to which this trigger is bound.</span></span><br /> <span data-ttu-id="555a0-129">The only valid value for this release is 1.</span><span class="sxs-lookup"><span data-stu-id="555a0-129">The only valid value for this release is 1.</span></span> <span data-ttu-id="555a0-130">This indicates that the control is an attribute.</span><span class="sxs-lookup"><span data-stu-id="555a0-130">This indicates that the control is an attribute.</span></span> <span data-ttu-id="555a0-131">This value only applies when the `ControlName` is not null.</span><span class="sxs-lookup"><span data-stu-id="555a0-131">This value only applies when the `ControlName` is not null.</span></span>|
|`Event`|<span data-ttu-id="555a0-132">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="555a0-132">String</span></span>|<span data-ttu-id="555a0-133">There are three valid values to indicate the event:</span><span class="sxs-lookup"><span data-stu-id="555a0-133">There are three valid values to indicate the event:</span></span><br /> -   `load`<br />-   `change`<br />-   `save`|
|`FormId`|<span data-ttu-id="555a0-134">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="555a0-134">Lookup</span></span>|<span data-ttu-id="555a0-135">ID of the form associated with the business rule.</span><span class="sxs-lookup"><span data-stu-id="555a0-135">ID of the form associated with the business rule.</span></span><br /> <span data-ttu-id="555a0-136">This value is null when the rule applies to all forms for the entity that supports business rules.</span><span class="sxs-lookup"><span data-stu-id="555a0-136">This value is null when the rule applies to all forms for the entity that supports business rules.</span></span>|
|`IsCustomizable`|<span data-ttu-id="555a0-137">ManagedProperty</span><span class="sxs-lookup"><span data-stu-id="555a0-137">ManagedProperty</span></span>|<span data-ttu-id="555a0-138">Information that specifies whether this component can be customized.</span><span class="sxs-lookup"><span data-stu-id="555a0-138">Information that specifies whether this component can be customized.</span></span><br /> <span data-ttu-id="555a0-139">You cannot change process trigger records included in a managed solution when the `IsCustomizable.Value` is false.</span><span class="sxs-lookup"><span data-stu-id="555a0-139">You cannot change process trigger records included in a managed solution when the `IsCustomizable.Value` is false.</span></span>|
|`PrimaryEntityTypeCode`|<span data-ttu-id="555a0-140">EntityName</span><span class="sxs-lookup"><span data-stu-id="555a0-140">EntityName</span></span>|<span data-ttu-id="555a0-141">Logical name for the entity that the business rule is applied on.</span><span class="sxs-lookup"><span data-stu-id="555a0-141">Logical name for the entity that the business rule is applied on.</span></span>|
|`ProcessId`|<span data-ttu-id="555a0-142">Tra cứu</span><span class="sxs-lookup"><span data-stu-id="555a0-142">Lookup</span></span>|<span data-ttu-id="555a0-143">ID of the process.</span><span class="sxs-lookup"><span data-stu-id="555a0-143">ID of the process.</span></span>|
|`ProcessTriggerId`|<span data-ttu-id="555a0-144">Uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="555a0-144">Uniqueidentifier</span></span>|<span data-ttu-id="555a0-145">ID of the process trigger record.</span><span class="sxs-lookup"><span data-stu-id="555a0-145">ID of the process trigger record.</span></span>|

### <a name="see-also"></a><span data-ttu-id="555a0-146">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="555a0-146">See also</span></span>

 [<span data-ttu-id="555a0-147">Tạo các quy tắc và đề xuất công việc</span><span class="sxs-lookup"><span data-stu-id="555a0-147">Create business rules and recommendations</span></span>](../../customize/create-business-rules-recommendations-apply-logic-form.md)
 <!--
 Add back after Web API reference regen
 [ProcessTrigger Entity]/entities/processtrigger.md)
 -->
