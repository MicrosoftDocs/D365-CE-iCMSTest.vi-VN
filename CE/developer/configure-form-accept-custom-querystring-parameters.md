---
title: Configure a form to accept custom querystring parameters (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about configuring a form to acept custom querystring parameters. Use these parameters to set default values when you create a new record in the application.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6c05ff14-2d5a-4e90-a3c4-dc7ca1ec4698
caps.latest.revision: 19
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 88d3efddecf7bdc6b4f3a5961e34892a81c7bd93
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387751"
---
# <a name="configure-a-form-to-accept-custom-querystring-parameters"></a><span data-ttu-id="5622a-104">Configure a form to accept custom querystring parameters</span><span class="sxs-lookup"><span data-stu-id="5622a-104">Configure a form to accept custom querystring parameters</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5622a-105">The ability to pass values to a Web page by using query strings represents a concern for security.</span><span class="sxs-lookup"><span data-stu-id="5622a-105">The ability to pass values to a Web page by using query strings represents a concern for security.</span></span> [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="5622a-106">applies the best practice of always comparing any parameter passed as a query string against a list of expected parameter names and data types.</span><span class="sxs-lookup"><span data-stu-id="5622a-106">applies the best practice of always comparing any parameter passed as a query string against a list of expected parameter names and data types.</span></span>  
  
 <span data-ttu-id="5622a-107">By default, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] allows a specified set of query string parameters to be passed to a form.</span><span class="sxs-lookup"><span data-stu-id="5622a-107">By default, [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] allows a specified set of query string parameters to be passed to a form.</span></span> <span data-ttu-id="5622a-108">You use these parameters to set default values when you create a new record in the application.</span><span class="sxs-lookup"><span data-stu-id="5622a-108">You use these parameters to set default values when you create a new record in the application.</span></span> <span data-ttu-id="5622a-109">Each parameter must use a standard naming convention that includes a reference to the attribute logical name.</span><span class="sxs-lookup"><span data-stu-id="5622a-109">Each parameter must use a standard naming convention that includes a reference to the attribute logical name.</span></span> <span data-ttu-id="5622a-110">For more information, see [Set field values using parameters passed to a form](set-field-values-using-parameters-passed-form.md).</span><span class="sxs-lookup"><span data-stu-id="5622a-110">For more information, see [Set field values using parameters passed to a form](set-field-values-using-parameters-passed-form.md).</span></span>  
  
 <span data-ttu-id="5622a-111">In your applications, you may want to pass custom query string parameters to an entity form.</span><span class="sxs-lookup"><span data-stu-id="5622a-111">In your applications, you may want to pass custom query string parameters to an entity form.</span></span> <span data-ttu-id="5622a-112">This topic provides information about how you can define a set of specific parameter names and data types that can be accepted for a specific entity form.</span><span class="sxs-lookup"><span data-stu-id="5622a-112">This topic provides information about how you can define a set of specific parameter names and data types that can be accepted for a specific entity form.</span></span>  
  
## <a name="define-allowed-query-string-parameters"></a><span data-ttu-id="5622a-113">Define allowed query string parameters</span><span class="sxs-lookup"><span data-stu-id="5622a-113">Define allowed query string parameters</span></span>  
 <span data-ttu-id="5622a-114">There are two ways to specify which query string parameters will be accepted by the form:</span><span class="sxs-lookup"><span data-stu-id="5622a-114">There are two ways to specify which query string parameters will be accepted by the form:</span></span>  
  
-   <span data-ttu-id="5622a-115">Chỉnh sửa thuộc tính biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="5622a-115">Edit form properties</span></span>  
  
-   <span data-ttu-id="5622a-116">Edit form XML</span><span class="sxs-lookup"><span data-stu-id="5622a-116">Edit form XML</span></span>  
  
### <a name="edit-form-properties"></a><span data-ttu-id="5622a-117">Edit form properties</span><span class="sxs-lookup"><span data-stu-id="5622a-117">Edit form properties</span></span>  
 <span data-ttu-id="5622a-118">When you edit an entity form, on the **Home** tab in the **Form** group, click **Form Properties**.</span><span class="sxs-lookup"><span data-stu-id="5622a-118">When you edit an entity form, on the **Home** tab in the **Form** group, click **Form Properties**.</span></span> <span data-ttu-id="5622a-119">In the **Form Properties** dialog box, select the **Parameters** tab.</span><span class="sxs-lookup"><span data-stu-id="5622a-119">In the **Form Properties** dialog box, select the **Parameters** tab.</span></span>  
  
 <span data-ttu-id="5622a-120">Use this tab to modify the names and data types that the form allows.</span><span class="sxs-lookup"><span data-stu-id="5622a-120">Use this tab to modify the names and data types that the form allows.</span></span>  
  
### <a name="edit-formxml"></a><span data-ttu-id="5622a-121">Edit FormXml</span><span class="sxs-lookup"><span data-stu-id="5622a-121">Edit FormXml</span></span>  
 <span data-ttu-id="5622a-122">Within the exported solution customizations.xml file, immediately following the footer element, you can add a `<formparameters>` element.</span><span class="sxs-lookup"><span data-stu-id="5622a-122">Within the exported solution customizations.xml file, immediately following the footer element, you can add a `<formparameters>` element.</span></span> <span data-ttu-id="5622a-123">In the `<formparameters>` element, add `<querystringparameter>` elements to specify which parameters will be allowed.</span><span class="sxs-lookup"><span data-stu-id="5622a-123">In the `<formparameters>` element, add `<querystringparameter>` elements to specify which parameters will be allowed.</span></span>  
  
 <span data-ttu-id="5622a-124">The following describes the `querystringparameter` element attributes, `name` and `type`:</span><span class="sxs-lookup"><span data-stu-id="5622a-124">The following describes the `querystringparameter` element attributes, `name` and `type`:</span></span>  
  
- <span data-ttu-id="5622a-125">**name**.</span><span class="sxs-lookup"><span data-stu-id="5622a-125">**name**.</span></span> <span data-ttu-id="5622a-126">Each name attribute must contain at least one underscore ('\_') character, but the name of the query string parameter cannot begin with an underscore.</span><span class="sxs-lookup"><span data-stu-id="5622a-126">Each name attribute must contain at least one underscore ('\_') character, but the name of the query string parameter cannot begin with an underscore.</span></span> <span data-ttu-id="5622a-127">The name also can’t start with “crm\_”.</span><span class="sxs-lookup"><span data-stu-id="5622a-127">The name also can’t start with “crm\_”.</span></span> <span data-ttu-id="5622a-128">We strongly recommend that you use the customization prefix of the solution publisher as the naming convention.</span><span class="sxs-lookup"><span data-stu-id="5622a-128">We strongly recommend that you use the customization prefix of the solution publisher as the naming convention.</span></span> <span data-ttu-id="5622a-129">A valid `querystringparameter` name attribute value is “myISV_contact_specialvalue”.</span><span class="sxs-lookup"><span data-stu-id="5622a-129">A valid `querystringparameter` name attribute value is “myISV_contact_specialvalue”.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="5622a-130">If a `querystringparameter` element name is not unique, it may be overwritten by another parameter definition using a different data type.</span><span class="sxs-lookup"><span data-stu-id="5622a-130">If a `querystringparameter` element name is not unique, it may be overwritten by another parameter definition using a different data type.</span></span>  
  
- <span data-ttu-id="5622a-131">**Loại**.</span><span class="sxs-lookup"><span data-stu-id="5622a-131">**Type**.</span></span> <span data-ttu-id="5622a-132">Match the data type values with the parameter values so that invalid data is not passed with the parameter.</span><span class="sxs-lookup"><span data-stu-id="5622a-132">Match the data type values with the parameter values so that invalid data is not passed with the parameter.</span></span> <span data-ttu-id="5622a-133">The following are valid data types:</span><span class="sxs-lookup"><span data-stu-id="5622a-133">The following are valid data types:</span></span>  
  
    -   <span data-ttu-id="5622a-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="5622a-134">Boolean</span></span>  
  
    -   <span data-ttu-id="5622a-135">Ngày Giờ</span><span class="sxs-lookup"><span data-stu-id="5622a-135">DateTime</span></span>  
  
    -   <span data-ttu-id="5622a-136">Gấp đôi</span><span class="sxs-lookup"><span data-stu-id="5622a-136">Double</span></span>  
  
    -   <span data-ttu-id="5622a-137">EntityType</span><span class="sxs-lookup"><span data-stu-id="5622a-137">EntityType</span></span>  
  
    -   <span data-ttu-id="5622a-138">Số nguyên</span><span class="sxs-lookup"><span data-stu-id="5622a-138">Integer</span></span>  
  
    -   <span data-ttu-id="5622a-139">Long</span><span class="sxs-lookup"><span data-stu-id="5622a-139">Long</span></span>  
  
    -   <span data-ttu-id="5622a-140">PositiveInteger</span><span class="sxs-lookup"><span data-stu-id="5622a-140">PositiveInteger</span></span>  
  
        > [!NOTE]
        >  <span data-ttu-id="5622a-141">PositiveInteger includes “0” in the range of valid values.</span><span class="sxs-lookup"><span data-stu-id="5622a-141">PositiveInteger includes “0” in the range of valid values.</span></span>  
  
    -   <span data-ttu-id="5622a-142">SafeString</span><span class="sxs-lookup"><span data-stu-id="5622a-142">SafeString</span></span>  
  
    -   <span data-ttu-id="5622a-143">UniqueId</span><span class="sxs-lookup"><span data-stu-id="5622a-143">UniqueId</span></span>  
  
    -   <span data-ttu-id="5622a-144">UnsignedInt</span><span class="sxs-lookup"><span data-stu-id="5622a-144">UnsignedInt</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5622a-145">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5622a-145">See also</span></span>  
 <span data-ttu-id="5622a-146">[Set field values using parameters passed to a form](set-field-values-using-parameters-passed-form.md) </span><span class="sxs-lookup"><span data-stu-id="5622a-146">[Set field values using parameters passed to a form](set-field-values-using-parameters-passed-form.md) </span></span>  
 [<span data-ttu-id="5622a-147">Open Forms And Views with a URL</span><span class="sxs-lookup"><span data-stu-id="5622a-147">Open Forms And Views with a URL</span></span>](open-forms-views-dialogs-reports-url.md)
