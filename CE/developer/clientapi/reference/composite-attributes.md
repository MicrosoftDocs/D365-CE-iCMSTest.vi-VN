---
title: Composite attributes in Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about the attribute addOnchange method to set a function to be called when the attribute value is changed.
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 9f3b2fed-fde5-46e4-8c59-43aa51aa82df
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 826c0d864b345ff4697fe7e6ad3b38545dbae040
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388073"
---
# <a name="composite-attributes"></a><span data-ttu-id="4c0a7-103">Composite attributes</span><span class="sxs-lookup"><span data-stu-id="4c0a7-103">Composite attributes</span></span> 

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4c0a7-104">Some fields added to a form can represent multiple items of data.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-104">Some fields added to a form can represent multiple items of data.</span></span> <span data-ttu-id="4c0a7-105">These *composite attributes* behave differently from other attributes when displayed in the web application and you must write scripts differently to use them properly.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-105">These *composite attributes* behave differently from other attributes when displayed in the web application and you must write scripts differently to use them properly.</span></span>

<span data-ttu-id="4c0a7-106">The following table lists the composite attributes available in Customer Engagement:</span><span class="sxs-lookup"><span data-stu-id="4c0a7-106">The following table lists the composite attributes available in Customer Engagement:</span></span>

<table>
    <tbody>
        <tr>
            <th scope="col">
                <p>
<span data-ttu-id="4c0a7-107">Thực thể</span><span class="sxs-lookup"><span data-stu-id="4c0a7-107">Entity</span></span> </p>
            </th>
            <th scope="col">
                <p>
<span data-ttu-id="4c0a7-108">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="4c0a7-108">Display Name</span></span> </p>
            </th>
            <th scope="col">
                <p>
<span data-ttu-id="4c0a7-109">Tên lô-gic</span><span class="sxs-lookup"><span data-stu-id="4c0a7-109">Logical name</span></span> </p>
            </th>
        </tr>
        <tr>
            <td rowspan="2">
                <p>
<span data-ttu-id="4c0a7-110">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="4c0a7-110">Account</span></span> </p>
            </td>
            <td>
                <p><span data-ttu-id="4c0a7-111">
                    <strong>Địa chỉ 1</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-111">
                    <strong>Address 1</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-112">address1_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-112">address1_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-113">
                    <strong>Địa chỉ 2</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-113">
                    <strong>Address 2</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-114">address2_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-114">address2_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td rowspan="3">
                <p>
<span data-ttu-id="4c0a7-115">người liên hệ</span><span class="sxs-lookup"><span data-stu-id="4c0a7-115">Contact</span></span> </p>
            </td>
            <td>
                <p><span data-ttu-id="4c0a7-116">
                    <strong>Họ tên</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-116">
                    <strong>Full Name</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-117">họ tên</span><span class="sxs-lookup"><span data-stu-id="4c0a7-117">fullname</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-118">
                    <strong>Địa chỉ 1</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-118">
                    <strong>Address 1</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-119">address1_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-119">address1_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-120">
                    <strong>Địa chỉ 2</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-120">
                    <strong>Address 2</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-121">address2_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-121">address2_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td rowspan="3">
                <p>
<span data-ttu-id="4c0a7-122">Khách hàng tiềm năng</span><span class="sxs-lookup"><span data-stu-id="4c0a7-122">Lead</span></span> </p>
            </td>
            <td>
                <p><span data-ttu-id="4c0a7-123">
                    <strong>Họ tên</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-123">
                    <strong>Full Name</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-124">họ tên</span><span class="sxs-lookup"><span data-stu-id="4c0a7-124">fullname</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-125">
                    <strong>Địa chỉ 1</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-125">
                    <strong>Address 1</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-126">address1_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-126">address1_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-127">
                    <strong>Địa chỉ 2</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-127">
                    <strong>Address 2</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-128">address2_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-128">address2_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td rowspan="3">
                <p>
<span data-ttu-id="4c0a7-129">Người dùng</span><span class="sxs-lookup"><span data-stu-id="4c0a7-129">User</span></span> </p>
            </td>
            <td>
                <p><span data-ttu-id="4c0a7-130">
                    <strong>Họ tên</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-130">
                    <strong>Full Name</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-131">họ tên</span><span class="sxs-lookup"><span data-stu-id="4c0a7-131">fullname</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-132">
                    <strong>Address</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-132">
                    <strong>Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-133">address1_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-133">address1_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-134">
                    <strong>Địa chỉ khác</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-134">
                    <strong>Other Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-135">address2_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-135">address2_composite</span></span> </p>
            </td>
        </tr><br/>        <tr>
            <td rowspan="2">
                <p>
<span data-ttu-id="4c0a7-136">Báo giá</span><span class="sxs-lookup"><span data-stu-id="4c0a7-136">Quote</span></span> </p>
            </td>
            <td>
                <p><span data-ttu-id="4c0a7-137">
                    <strong>Bill To Address</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-137">
                    <strong>Bill To Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-138">billto_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-138">billto_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-139">
                    <strong>Ship To Address</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-139">
                    <strong>Ship To Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-140">shipto_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-140">shipto_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td rowspan="2">
                <p>
<span data-ttu-id="4c0a7-141">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="4c0a7-141">Order</span></span> </p>
            </td>
            <td>
                <p><span data-ttu-id="4c0a7-142">
                    <strong>Bill To Address</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-142">
                    <strong>Bill To Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-143">billto_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-143">billto_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-144">
                    <strong>Ship To Address</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-144">
                    <strong>Ship To Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-145">shipto_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-145">shipto_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td rowspan="2">
                <p>
<span data-ttu-id="4c0a7-146">Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="4c0a7-146">Invoice</span></span> </p>
            </td>
            <td>
                <p><span data-ttu-id="4c0a7-147">
                    <strong>Bill To Address</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-147">
                    <strong>Bill To Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-148">billto_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-148">billto_composite</span></span> </p>
            </td>
        </tr>
        <tr>
            <td>
                <p><span data-ttu-id="4c0a7-149">
                    <strong>Ship To Address</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4c0a7-149">
                    <strong>Ship To Address</strong>
                </span></span></p>
            </td>
            <td>
                <p>
<span data-ttu-id="4c0a7-150">shipto_composite</span><span class="sxs-lookup"><span data-stu-id="4c0a7-150">shipto_composite</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

## <a name="composite-attributes-in-the-web-application"></a><span data-ttu-id="4c0a7-151">Composite attributes in the web application</span><span class="sxs-lookup"><span data-stu-id="4c0a7-151">Composite attributes in the web application</span></span>

<span data-ttu-id="4c0a7-152">When fields for composite attributes are added to a main form, the web application will show just the composite attribute.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-152">When fields for composite attributes are added to a main form, the web application will show just the composite attribute.</span></span> <span data-ttu-id="4c0a7-153">When someone edits the field, a flyout appears showing the individual attributes that comprise the composite attribute.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-153">When someone edits the field, a flyout appears showing the individual attributes that comprise the composite attribute.</span></span> 

<span data-ttu-id="4c0a7-154">For example, the **Address** field on a Contact form is a composite attribute.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-154">For example, the **Address** field on a Contact form is a composite attribute.</span></span> <span data-ttu-id="4c0a7-155">Clicking the **Address** field dispays a flyout with individual attributes that comprise the composite attribute.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-155">Clicking the **Address** field dispays a flyout with individual attributes that comprise the composite attribute.</span></span> 

![An example of a composite attribute](../../media/clientapi_compositeattribute.png)

<span data-ttu-id="4c0a7-157">Although not explicitly added to the form in the form editor, each of the attributes that are part of the attribute are available to the form.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-157">Although not explicitly added to the form in the form editor, each of the attributes that are part of the attribute are available to the form.</span></span> <span data-ttu-id="4c0a7-158">Although you can read the value of the composite value using [getValue](attributes/getValue.md), you can’t use [setValue](attributes/setValue.md) to change the value of the composite attribute directly; you must set one or more of the attributes referenced by the composite attribute.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-158">Although you can read the value of the composite value using [getValue](attributes/getValue.md), you can’t use [setValue](attributes/setValue.md) to change the value of the composite attribute directly; you must set one or more of the attributes referenced by the composite attribute.</span></span>

<span data-ttu-id="4c0a7-159">You can access the individual constituent controls displayed in the flyout by name.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-159">You can access the individual constituent controls displayed in the flyout by name.</span></span> <span data-ttu-id="4c0a7-160">These controls use the following naming convention: \<**composite control name**>\_compositionLinkControl_\<**constituent attribute name**>.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-160">These controls use the following naming convention: \<**composite control name**>\_compositionLinkControl_\<**constituent attribute name**>.</span></span> 

<span data-ttu-id="4c0a7-161">To access just the **address_line1** control in the **address1_composite** control, you would use:</span><span class="sxs-lookup"><span data-stu-id="4c0a7-161">To access just the **address_line1** control in the **address1_composite** control, you would use:</span></span> 

`formContext.getControl("address1_composite_compositionLinkControl_address1_line1")`

## <a name="composite-attributes-in-mobile-clients"></a><span data-ttu-id="4c0a7-162">Composite attributes in mobile clients</span><span class="sxs-lookup"><span data-stu-id="4c0a7-162">Composite attributes in mobile clients</span></span>
<span data-ttu-id="4c0a7-163">The mobile client for Dynamics 365 for Customer Engagement apps use the same form definitions used for the entities that have composite attributes but it interprets them differently.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-163">The mobile client for Dynamics 365 for Customer Engagement apps use the same form definitions used for the entities that have composite attributes but it interprets them differently.</span></span> <span data-ttu-id="4c0a7-164">If a composite attribute is found in the form definition, it will show all the attributes that are part of the composite attribute in that section of the form.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-164">If a composite attribute is found in the form definition, it will show all the attributes that are part of the composite attribute in that section of the form.</span></span> <span data-ttu-id="4c0a7-165">There is no need for a flyout because all the fields are visible.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-165">There is no need for a flyout because all the fields are visible.</span></span> <span data-ttu-id="4c0a7-166">You can write scripts for the form accessing each of the individual attributes just as if they had been individually added to the form.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-166">You can write scripts for the form accessing each of the individual attributes just as if they had been individually added to the form.</span></span>
<span data-ttu-id="4c0a7-167">However, the actual composite control will not be present in the Dynamics 365 for Customer Engagement apps mobile clients page.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-167">However, the actual composite control will not be present in the Dynamics 365 for Customer Engagement apps mobile clients page.</span></span>

## <a name="mitigate-the-differences"></a><span data-ttu-id="4c0a7-168">Mitigate the differences</span><span class="sxs-lookup"><span data-stu-id="4c0a7-168">Mitigate the differences</span></span>

<span data-ttu-id="4c0a7-169">If you want to access the fullname field for the Contact, Lead, or User entities, using the **formContext.data.entity**.[getPrimaryAttributeValue](formContext-data-entity/getPrimaryAttributeValue.md) method is an easy way to get the value for this attribute without referencing it directly.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-169">If you want to access the fullname field for the Contact, Lead, or User entities, using the **formContext.data.entity**.[getPrimaryAttributeValue](formContext-data-entity/getPrimaryAttributeValue.md) method is an easy way to get the value for this attribute without referencing it directly.</span></span> <span data-ttu-id="4c0a7-170">This method works for both the web application and Dynamics 365 for Customer Engagement apps mobile clients.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-170">This method works for both the web application and Dynamics 365 for Customer Engagement apps mobile clients.</span></span>

<span data-ttu-id="4c0a7-171">If you have code that needs to read the value of one of the address composite attributes, to work with both clients, you need to separate the code using the [getClient](Xrm-Utility/getGlobalContext/client.md#getclient) method as shown in the following function that will display the formatted address using the **Xrm.Navigation**.[openAlertDialog](Xrm-Navigation/openAlertDialog.md) method in either the main web application or the mobile apps version of the same form.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-171">If you have code that needs to read the value of one of the address composite attributes, to work with both clients, you need to separate the code using the [getClient](Xrm-Utility/getGlobalContext/client.md#getclient) method as shown in the following function that will display the formatted address using the **Xrm.Navigation**.[openAlertDialog](Xrm-Navigation/openAlertDialog.md) method in either the main web application or the mobile apps version of the same form.</span></span>

```JavaScript
function showAddressDialog(executionContext) {
    var address1_compositeValue;
    var formContext = executionContext.getFormContext();
    if (Xrm.Utility.getGlobalContext().client.getClient() != "Mobile") {
        address1_compositeValue = formContext.getAttribute("address1_composite").getValue();
    }
    else {
        var address1_line1 = formContext.getAttribute("address1_line1").getValue();
        var address1_line2 = formContext.getAttribute("address1_line2").getValue();
        var address1_line3 = formContext.getAttribute("address1_line3").getValue();
        var address1_city = formContext.getAttribute("address1_city").getValue();
        var address1_stateorprovince = formContext.getAttribute("address1_stateorprovince").getValue();
        var address1_postalcode = formContext.getAttribute("address1_postalcode").getValue();
        var address1_country = formContext.getAttribute("address1_country").getValue();

        // Achieve equivalent formatting
        //address1_line1
        //address1_line2
        //address1_line3
        //address1_city, address1_stateorprovince address1_postalcode
        //address1_country

        var addressText = "";
        if (address1_line1 != null) {
            addressText += address1_line1 + "\n";
        }
        if (address1_line2 != null) {
            addressText += address1_line2 + "\n";
        }
        if (address1_line3 != null) {
            addressText += address1_line3 + "\n";
        }
        if (address1_city != null) {
            addressText += address1_city + ", ";
        }
        if (address1_stateorprovince != null) {
            addressText += address1_stateorprovince + " ";
        }
        if (address1_postalcode != null) {
            addressText += address1_postalcode + "\n";
        }
        addressText += address1_country;

        address1_compositeValue = addressText;
    }
    Xrm.Navigation.openAlertDialog({ text: address1_compositeValue });
    console.log(address1_compositeValue);
}
```

### <a name="related-topics"></a><span data-ttu-id="4c0a7-172">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="4c0a7-172">Related topics</span></span>
[<span data-ttu-id="4c0a7-173">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="4c0a7-173">Attributes</span></span>](attributes.md)
