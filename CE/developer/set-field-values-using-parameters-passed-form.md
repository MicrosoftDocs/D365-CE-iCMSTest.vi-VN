---
title: Set field values using parameters passed to a form (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: The content in this topic can be used for Dynamics 365 for Customer Engagement (online). You can set default values for new records created by users by specifying attribute values in the URL that is used to open the form.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 62984977-83a2-464a-b8d9-f7f3fa4b7d33
caps.latest.revision: 43
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1085990ddb0bd3fdac990499d2d308cdfa958a35
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387167"
---
# <a name="set-field-values-using-parameters-passed-to-a-form"></a><span data-ttu-id="fd739-104">Set field values using parameters passed to a form</span><span class="sxs-lookup"><span data-stu-id="fd739-104">Set field values using parameters passed to a form</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fd739-105">The content in this topic can be used for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="fd739-105">The content in this topic can be used for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="fd739-106">You can set default values for new records created by users by specifying attribute values in the URL that is used to open the form.</span><span class="sxs-lookup"><span data-stu-id="fd739-106">You can set default values for new records created by users by specifying attribute values in the URL that is used to open the form.</span></span> <span data-ttu-id="fd739-107">By default, these values are set in the form, but can be changed by users before they save the record.</span><span class="sxs-lookup"><span data-stu-id="fd739-107">By default, these values are set in the form, but can be changed by users before they save the record.</span></span>  
  
<a name="BKMK_PassingParameters"></a>   
## <a name="pass-parameters-to-set-field-record-values"></a><span data-ttu-id="fd739-108">Pass parameters to set field record values</span><span class="sxs-lookup"><span data-stu-id="fd739-108">Pass parameters to set field record values</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fd739-109">You can pass parameter values to the form to set field values using the `Xrm.Navigation.`[openForm](clientapi/reference/Xrm-Navigation/openForm.md) function.</span><span class="sxs-lookup"><span data-stu-id="fd739-109">You can pass parameter values to the form to set field values using the `Xrm.Navigation.`[openForm](clientapi/reference/Xrm-Navigation/openForm.md) function.</span></span> <span data-ttu-id="fd739-110">For an example, see [Example: Use Xrm.Navigation.openForm to Open a New Window](set-field-values-using-parameters-passed-form.md#BKMK_ExampleXrmNavigationOpentForm).</span><span class="sxs-lookup"><span data-stu-id="fd739-110">For an example, see [Example: Use Xrm.Navigation.openForm to Open a New Window](set-field-values-using-parameters-passed-form.md#BKMK_ExampleXrmNavigationOpentForm).</span></span>  
  
 <span data-ttu-id="fd739-111">When you open a new form by using the URL address, you can include arguments in the `extraqs` parameter to set field values.</span><span class="sxs-lookup"><span data-stu-id="fd739-111">When you open a new form by using the URL address, you can include arguments in the `extraqs` parameter to set field values.</span></span> <span data-ttu-id="fd739-112">The following requirements must be met:</span><span class="sxs-lookup"><span data-stu-id="fd739-112">The following requirements must be met:</span></span>  
  
- <span data-ttu-id="fd739-113">You must encode the parameters passed in the `extraqs` parameter.</span><span class="sxs-lookup"><span data-stu-id="fd739-113">You must encode the parameters passed in the `extraqs` parameter.</span></span> <span data-ttu-id="fd739-114">To encode the parameters, use [encodeURIComponent](https://msdn.microsoft.com/library/aeh9cef7\(VS.85\).aspx).</span><span class="sxs-lookup"><span data-stu-id="fd739-114">To encode the parameters, use [encodeURIComponent](https://msdn.microsoft.com/library/aeh9cef7\(VS.85\).aspx).</span></span>  
  
- <span data-ttu-id="fd739-115">The names of the query string arguments must match or include the names of attributes for the entity.</span><span class="sxs-lookup"><span data-stu-id="fd739-115">The names of the query string arguments must match or include the names of attributes for the entity.</span></span>  
  
- <span data-ttu-id="fd739-116">The values passed must be valid.</span><span class="sxs-lookup"><span data-stu-id="fd739-116">The values passed must be valid.</span></span>  
  
- <span data-ttu-id="fd739-117">The value can’t be a script.</span><span class="sxs-lookup"><span data-stu-id="fd739-117">The value can’t be a script.</span></span>  
  
  <span data-ttu-id="fd739-118">Any attempt to pass an invalid parameter or value will result in an error.</span><span class="sxs-lookup"><span data-stu-id="fd739-118">Any attempt to pass an invalid parameter or value will result in an error.</span></span>  
  
- <span data-ttu-id="fd739-119">For Boolean fields, use either an integer value of `0` or `1`, or a text value of `true` or `false` to set the value.</span><span class="sxs-lookup"><span data-stu-id="fd739-119">For Boolean fields, use either an integer value of `0` or `1`, or a text value of `true` or `false` to set the value.</span></span>  
  
- <span data-ttu-id="fd739-120">For DateTime fields, use the text value of the date.</span><span class="sxs-lookup"><span data-stu-id="fd739-120">For DateTime fields, use the text value of the date.</span></span>  
  
<a name="BKMK_ExampleSetValueStringFields"></a>   
## <a name="example-set-the-value-for-string-fields"></a><span data-ttu-id="fd739-121">Example: Set the value for string fields</span><span class="sxs-lookup"><span data-stu-id="fd739-121">Example: Set the value for string fields</span></span>  
 <span data-ttu-id="fd739-122">The following sample sets the value for the **Name** field of a new account record to "New Account".</span><span class="sxs-lookup"><span data-stu-id="fd739-122">The following sample sets the value for the **Name** field of a new account record to "New Account".</span></span>  
  
 <span data-ttu-id="fd739-123">The unencoded value for the `extraqs` parameter is “name=New Account”.</span><span class="sxs-lookup"><span data-stu-id="fd739-123">The unencoded value for the `extraqs` parameter is “name=New Account”.</span></span>  
  
```  
/main.aspx?etn=account&extraqs=name%3DNew%20Account&pagetype=entityrecord  
```  
  
<a name="BKMK_SetLookupFieldValues"></a>   
## <a name="set-values-for-lookup-fields"></a><span data-ttu-id="fd739-124">Set values for lookup fields</span><span class="sxs-lookup"><span data-stu-id="fd739-124">Set values for lookup fields</span></span>  
 <span data-ttu-id="fd739-125">The following table describes five types of lookup fields.</span><span class="sxs-lookup"><span data-stu-id="fd739-125">The following table describes five types of lookup fields.</span></span> <span data-ttu-id="fd739-126">For examples using lookup fields, see [Example: Set the Value for Lookup Fields](set-field-values-using-parameters-passed-form.md#BKMK_setValueLookupfields) and [Example: Use Xrm.Navigation.openForm to Open a New Window](set-field-values-using-parameters-passed-form.md#BKMK_ExampleXrmNavigationOpentForm).</span><span class="sxs-lookup"><span data-stu-id="fd739-126">For examples using lookup fields, see [Example: Set the Value for Lookup Fields](set-field-values-using-parameters-passed-form.md#BKMK_setValueLookupfields) and [Example: Use Xrm.Navigation.openForm to Open a New Window](set-field-values-using-parameters-passed-form.md#BKMK_ExampleXrmNavigationOpentForm).</span></span>  
  
|<span data-ttu-id="fd739-127">Lookup Type</span><span class="sxs-lookup"><span data-stu-id="fd739-127">Lookup Type</span></span>|<span data-ttu-id="fd739-128">Mô tả</span><span class="sxs-lookup"><span data-stu-id="fd739-128">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="fd739-129">simple lookup</span><span class="sxs-lookup"><span data-stu-id="fd739-129">simple lookup</span></span>|<span data-ttu-id="fd739-130">Allows for a single reference to one type of entity.</span><span class="sxs-lookup"><span data-stu-id="fd739-130">Allows for a single reference to one type of entity.</span></span>|  
|<span data-ttu-id="fd739-131">customer lookup</span><span class="sxs-lookup"><span data-stu-id="fd739-131">customer lookup</span></span>|<span data-ttu-id="fd739-132">Cho phép một tham chiếu duy nhất vào một tài khoản hoặc hồ sơ địa chỉ liên lạc.</span><span class="sxs-lookup"><span data-stu-id="fd739-132">Allows for a single reference to either an account or a contact record.</span></span>|  
|<span data-ttu-id="fd739-133">owner lookup</span><span class="sxs-lookup"><span data-stu-id="fd739-133">owner lookup</span></span>|<span data-ttu-id="fd739-134">Allows for a single reference to either a team or a system user record.</span><span class="sxs-lookup"><span data-stu-id="fd739-134">Allows for a single reference to either a team or a system user record.</span></span>|  
|<span data-ttu-id="fd739-135">partylist lookup</span><span class="sxs-lookup"><span data-stu-id="fd739-135">partylist lookup</span></span>|<span data-ttu-id="fd739-136">Cho phép nhiều tham chiếu đến nhiều thực thể.</span><span class="sxs-lookup"><span data-stu-id="fd739-136">Allows for multiple references to multiple entities.</span></span>|  
|<span data-ttu-id="fd739-137">regarding lookup</span><span class="sxs-lookup"><span data-stu-id="fd739-137">regarding lookup</span></span>|<span data-ttu-id="fd739-138">Cho phép một tham chiếu đến nhiều thực thể.</span><span class="sxs-lookup"><span data-stu-id="fd739-138">Allows for a single reference to multiple entities.</span></span>|  
  
 <span data-ttu-id="fd739-139">The following guidelines apply when setting the value of a lookup on a form using a query string argument:</span><span class="sxs-lookup"><span data-stu-id="fd739-139">The following guidelines apply when setting the value of a lookup on a form using a query string argument:</span></span>  
  
-   <span data-ttu-id="fd739-140">For simple lookups you must set the value and the text to display in the lookup.</span><span class="sxs-lookup"><span data-stu-id="fd739-140">For simple lookups you must set the value and the text to display in the lookup.</span></span> <span data-ttu-id="fd739-141">Use the suffix “name” with the name of the attribute to set the value for the text.</span><span class="sxs-lookup"><span data-stu-id="fd739-141">Use the suffix “name” with the name of the attribute to set the value for the text.</span></span>  
  
     <span data-ttu-id="fd739-142">Don’t use any other arguments.</span><span class="sxs-lookup"><span data-stu-id="fd739-142">Don’t use any other arguments.</span></span>  
  
-   <span data-ttu-id="fd739-143">For customer and owner lookups you must set the value and the name in the same way you set them for simple lookups.</span><span class="sxs-lookup"><span data-stu-id="fd739-143">For customer and owner lookups you must set the value and the name in the same way you set them for simple lookups.</span></span> <span data-ttu-id="fd739-144">In addition you must use the suffix “type” to specify the type of entity.</span><span class="sxs-lookup"><span data-stu-id="fd739-144">In addition you must use the suffix “type” to specify the type of entity.</span></span> <span data-ttu-id="fd739-145">Allowable values are account, contact, systemuser, and team.</span><span class="sxs-lookup"><span data-stu-id="fd739-145">Allowable values are account, contact, systemuser, and team.</span></span>  
  
-   <span data-ttu-id="fd739-146">You can’t set the values for partylist or regarding lookups.</span><span class="sxs-lookup"><span data-stu-id="fd739-146">You can’t set the values for partylist or regarding lookups.</span></span>  
  
<a name="BKMK_setValueLookupfields"></a>   
## <a name="example-set-the-value-for-lookup-fields"></a><span data-ttu-id="fd739-147">Example: Set the value for lookup fields</span><span class="sxs-lookup"><span data-stu-id="fd739-147">Example: Set the value for lookup fields</span></span>  
 <span data-ttu-id="fd739-148">To set values for lookup fields, use the data value, the name value, and for customer or owner lookups only, specify the type value for the respective field.</span><span class="sxs-lookup"><span data-stu-id="fd739-148">To set values for lookup fields, use the data value, the name value, and for customer or owner lookups only, specify the type value for the respective field.</span></span> <span data-ttu-id="fd739-149">The following sample sets the owner field to a user named “Mark Folkerts”.</span><span class="sxs-lookup"><span data-stu-id="fd739-149">The following sample sets the owner field to a user named “Mark Folkerts”.</span></span>  
  
 <span data-ttu-id="fd739-150">The unencoded value for the `extraqs` parameter is “**ownerid**={B8C6E040-656E-DF11-B414-00155DB1891A}&**owneridname**=Mark Folkerts&**owneridtype**=systemuser”.</span><span class="sxs-lookup"><span data-stu-id="fd739-150">The unencoded value for the `extraqs` parameter is “**ownerid**={B8C6E040-656E-DF11-B414-00155DB1891A}&**owneridname**=Mark Folkerts&**owneridtype**=systemuser”.</span></span>  
  
```  
/main.aspx?etn=lead&pagetype=entityrecord&extraqs=ownerid%3D%7bB8C6E040-656E-DF11-B414-00155DB1891A%7d%26owneridname%3DMark%20Folkerts%26owneridtype%3Dsystemuser  
```  
  
 <span data-ttu-id="fd739-151">The following sample sets the primary contact field to a user named “Yvonne McKay (sample)”.The unencoded value for the `extraqs` parameter is “**primarycontactid**={43b58571-eefa-e311-80c1-00155d2a68c4}&**primarycontactidname**=Yvonne McKay (sample)”.</span><span class="sxs-lookup"><span data-stu-id="fd739-151">The following sample sets the primary contact field to a user named “Yvonne McKay (sample)”.The unencoded value for the `extraqs` parameter is “**primarycontactid**={43b58571-eefa-e311-80c1-00155d2a68c4}&**primarycontactidname**=Yvonne McKay (sample)”.</span></span>  
  
```  
/main.aspx?etn=account&pagetype=entityrecord&extraqs=primarycontactid%3D%7B43b58571-eefa-e311-80c1-00155d2a68c4%7D%26primarycontactidname%3DYvonne%20McKay%20(sample)  
```  
  
> [!NOTE]
>  <span data-ttu-id="fd739-152">For a simple lookup like this, you don’t have to set a type value.</span><span class="sxs-lookup"><span data-stu-id="fd739-152">For a simple lookup like this, you don’t have to set a type value.</span></span>  
  
<a name="BKMK_SetValueDateFields"></a>   
## <a name="example-set-the-value-for-date-fields"></a><span data-ttu-id="fd739-153">Example: Set the value for date fields</span><span class="sxs-lookup"><span data-stu-id="fd739-153">Example: Set the value for date fields</span></span>  
 <span data-ttu-id="fd739-154">The following sample sets the **Est. Close Date** field for a new opportunity to January 31, 2011.</span><span class="sxs-lookup"><span data-stu-id="fd739-154">The following sample sets the **Est. Close Date** field for a new opportunity to January 31, 2011.</span></span> <span data-ttu-id="fd739-155">The unencoded value for the `extraqs` parameter is “estimatedclosedate=01/31/11”.</span><span class="sxs-lookup"><span data-stu-id="fd739-155">The unencoded value for the `extraqs` parameter is “estimatedclosedate=01/31/11”.</span></span>  
  
```  
/main.aspx?etn=opportunity&extraqs=estimatedclosedate%3D01%2F31%2F11&pagetype=entityrecord  
```  
  
<a name="BKMK_SampleSEtValueOptionSetFields"></a>   
## <a name="example-set-the-value-for-option-set-fields"></a><span data-ttu-id="fd739-156">Example: Set the value for option set fields</span><span class="sxs-lookup"><span data-stu-id="fd739-156">Example: Set the value for option set fields</span></span>  
 <span data-ttu-id="fd739-157">To set the value for an **Option set** field, set the integer value for the option.</span><span class="sxs-lookup"><span data-stu-id="fd739-157">To set the value for an **Option set** field, set the integer value for the option.</span></span> <span data-ttu-id="fd739-158">The following sample sets the **Role** field value to “Decision Maker” in a new contact record.</span><span class="sxs-lookup"><span data-stu-id="fd739-158">The following sample sets the **Role** field value to “Decision Maker” in a new contact record.</span></span>  
  
 <span data-ttu-id="fd739-159">The unencoded value for the `extraqs` parameter is “accountrolecode=1”.</span><span class="sxs-lookup"><span data-stu-id="fd739-159">The unencoded value for the `extraqs` parameter is “accountrolecode=1”.</span></span>  
  
```  
/main.aspx?etn=contact&extraqs=accountrolecode%3D1&pagetype=entityrecord  
``` 

<a name="BKMK_SampleSEtValueMultiSelectOptionSetFields"></a>   
## <a name="example-set-the-value-for-multi-select-option-set-fields"></a><span data-ttu-id="fd739-160">Example: Set the value for multi-select option set fields</span><span class="sxs-lookup"><span data-stu-id="fd739-160">Example: Set the value for multi-select option set fields</span></span>

<span data-ttu-id="fd739-161">To set the value for **multi-select option set** field, Specify integer values for the options in the URL that is used to open the form.</span><span class="sxs-lookup"><span data-stu-id="fd739-161">To set the value for **multi-select option set** field, Specify integer values for the options in the URL that is used to open the form.</span></span> <span data-ttu-id="fd739-162">For example, to set the options for the **Hobbies** field, the unencoded value for the extraqs parameter will be “hobbies=[1,3,4]”.</span><span class="sxs-lookup"><span data-stu-id="fd739-162">For example, to set the options for the **Hobbies** field, the unencoded value for the extraqs parameter will be “hobbies=[1,3,4]”.</span></span>   

```  
/main.aspx?etn=contact&extraqs=hobbies%3D%5B1%2C3%2C4%5D&pagetype=entityrecord   
``` 
  
<a name="BKMK_ExampleXrmNavigationOpentForm"></a>   
## <a name="example-use-xrmnavigationopenform-to-open-a-new-window"></a><span data-ttu-id="fd739-163">Example: Use Xrm.Navigation.openForm to open a new window</span><span class="sxs-lookup"><span data-stu-id="fd739-163">Example: Use Xrm.Navigation.openForm to open a new window</span></span>  
 <span data-ttu-id="fd739-164">The following sample sets default values on several different fields and shows how to use the `Xrm.Navigation`.[openForm](clientapi/reference/Xrm-Navigation/openForm.md) function.</span><span class="sxs-lookup"><span data-stu-id="fd739-164">The following sample sets default values on several different fields and shows how to use the `Xrm.Navigation`.[openForm](clientapi/reference/Xrm-Navigation/openForm.md) function.</span></span> <span data-ttu-id="fd739-165">It is equivalent to the previous example that used the `window.open` method.</span><span class="sxs-lookup"><span data-stu-id="fd739-165">It is equivalent to the previous example that used the `window.open` method.</span></span>  
  
```javascript  
function OpenNewContact() {  
 var parameters = {};  
 //Set the Parent Customer field value to “Contoso”.  
 parameters["parentcustomerid"] = "2878282E-94D6-E111-9B1D-00155D9D700B";  
 parameters["parentcustomeridname"] = "Contoso";  
 parameters["parentcustomeridtype"] = "account";  
 //Set the Address Type to “Primary”.  
 parameters["address1_addresstypecode"] = "3";  
 //Set text in the Description field.  
 parameters["description"] = "Default values for this record were set programmatically.";  
 //Set Do not allow E-mails to "Do Not Allow".  
 parameters["donotemail"] = "1";  
  
 // Define the entity name to open the form  
 var entityFormOptions = {};
 entityFormOptions["entityName"] = "contact";

// Open the form
 Xrm.Navigation.openForm(entityFormOptions, parameters).then(
    function (success) {
        console.log(success);
    },
    function (error) {
        console.log(error);
    });  
}  
```  
  
<a name="BKMK_ExampleWindowOpen"></a>   
## <a name="example-use-windowopen-to-open-a-new-window"></a><span data-ttu-id="fd739-166">Example: Use window.open to open a new window</span><span class="sxs-lookup"><span data-stu-id="fd739-166">Example: Use window.open to open a new window</span></span>  
 <span data-ttu-id="fd739-167">The following sample sets default values on several different fields and shows how to use [encodeURIComponent](https://msdn.microsoft.com/library/aeh9cef7\(VS.85\).aspx) to encode the value of the `extraqs` parameter.</span><span class="sxs-lookup"><span data-stu-id="fd739-167">The following sample sets default values on several different fields and shows how to use [encodeURIComponent](https://msdn.microsoft.com/library/aeh9cef7\(VS.85\).aspx) to encode the value of the `extraqs` parameter.</span></span> <span data-ttu-id="fd739-168">If you use the [window.open](https://msdn.microsoft.com/library/ms536651\(VS.85\).aspx) method, you can control the features of the window that is opened.</span><span class="sxs-lookup"><span data-stu-id="fd739-168">If you use the [window.open](https://msdn.microsoft.com/library/ms536651\(VS.85\).aspx) method, you can control the features of the window that is opened.</span></span>  
  
```jscript  
function OpenNewContact() {  
    //Set the Parent Customer field value to “Contoso”.  
    var extraqs = "parentcustomerid={F01F3F6D-896E-DF11-B414-00155DB1891A}";  
    extraqs += "&parentcustomeridname=Contoso";  
    extraqs += "&parentcustomeridtype=account";  
    //Set the Address Type to “Primary”.  
    extraqs += "&address1_addresstypecode=3";  
    //Set text in the Description field.  
    extraqs += "&description=Default values for this record were set programatically.";  
    //Set Do not allow E-mails to "Do Not Allow".  
    extraqs += "&donotemail=1";  
    //Set features for how the window will appear.  
    var features = "location=no,menubar=no,status=no,toolbar=no";  
    // Open the window.  
    window.open("/main.aspx?etn=contact&pagetype=entityrecord&extraqs=" +  
     encodeURIComponent(extraqs), "_blank", features, false);  
}  
```  
  
### <a name="see-also"></a><span data-ttu-id="fd739-169">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="fd739-169">See also</span></span>  
 <span data-ttu-id="fd739-170">[Open Forms And Views with a URL](open-forms-views-dialogs-reports-url.md) </span><span class="sxs-lookup"><span data-stu-id="fd739-170">[Open Forms And Views with a URL](open-forms-views-dialogs-reports-url.md) </span></span>  
 [<span data-ttu-id="fd739-171">openForm</span><span class="sxs-lookup"><span data-stu-id="fd739-171">openForm</span></span>](clientapi/reference/Xrm-Navigation/openForm.md)  
 [<span data-ttu-id="fd739-172">Configure a form to accept custom querystring parameters</span><span class="sxs-lookup"><span data-stu-id="fd739-172">Configure a form to accept custom querystring parameters</span></span>](configure-form-accept-custom-querystring-parameters.md)
