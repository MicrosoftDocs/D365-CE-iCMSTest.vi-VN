---
title: openForm (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/09/2018
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 0206c43b-b1fc-490d-a867-1d75331885a8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 5591923dda5fc2e8fc02a10db1094fa3400cb03b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386224"
---
# <a name="openform-client-api-reference"></a><span data-ttu-id="01c7e-102">openForm (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="01c7e-102">openForm (Client API reference)</span></span>

[!INCLUDE[](../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/openForm-description.md](./includes/openForm-description.md)]

## <a name="syntax"></a><span data-ttu-id="01c7e-103">Cú pháp</span><span class="sxs-lookup"><span data-stu-id="01c7e-103">Syntax</span></span>

`Xrm.Navigation.openForm(entityFormOptions,formParameters).then(successCallback,errorCallback);`

## <a name="parameters"></a><span data-ttu-id="01c7e-104">Tham số</span><span class="sxs-lookup"><span data-stu-id="01c7e-104">Parameters</span></span>


<table style="width:100%">
  <tr>
    <th><span data-ttu-id="01c7e-105">Tên</span><span class="sxs-lookup"><span data-stu-id="01c7e-105">Name</span></span></th>
    <th><span data-ttu-id="01c7e-106">Loại</span><span class="sxs-lookup"><span data-stu-id="01c7e-106">Type</span></span></th> 
    <th><span data-ttu-id="01c7e-107">Bắt buộc</span><span class="sxs-lookup"><span data-stu-id="01c7e-107">Required</span></span></th>
    <th><span data-ttu-id="01c7e-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="01c7e-108">Description</span></span></th>
  </tr>
  <tr>
    <td><span data-ttu-id="01c7e-109">entityFormOptions</span><span class="sxs-lookup"><span data-stu-id="01c7e-109">entityFormOptions</span></span></td>
    <td><span data-ttu-id="01c7e-110">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="01c7e-110">Object</span></span></td> 
    <td><span data-ttu-id="01c7e-111">Có</span><span class="sxs-lookup"><span data-stu-id="01c7e-111">Yes</span></span></td>
    <td><span data-ttu-id="01c7e-112">Entity form options for opening the form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-112">Entity form options for opening the form.</span></span> <span data-ttu-id="01c7e-113">The object contains the following attributes:</span><span class="sxs-lookup"><span data-stu-id="01c7e-113">The object contains the following attributes:</span></span><ul>
<li><span data-ttu-id="01c7e-114"><b>cmdbar</b>: (Optional) Boolean.</span><span class="sxs-lookup"><span data-stu-id="01c7e-114"><b>cmdbar</b>: (Optional) Boolean.</span></span> <span data-ttu-id="01c7e-115">Indicates whether to display the command bar.</span><span class="sxs-lookup"><span data-stu-id="01c7e-115">Indicates whether to display the command bar.</span></span> <span data-ttu-id="01c7e-116">If you do not specify this parameter, the command bar is displayed by default.</span><span class="sxs-lookup"><span data-stu-id="01c7e-116">If you do not specify this parameter, the command bar is displayed by default.</span></span></li>
<li><span data-ttu-id="01c7e-117"><b>createFromEntity</b>: (Optional) Lookup.</span><span class="sxs-lookup"><span data-stu-id="01c7e-117"><b>createFromEntity</b>: (Optional) Lookup.</span></span> <span data-ttu-id="01c7e-118">Designates a record that will provide default values based on mapped attribute values.</span><span class="sxs-lookup"><span data-stu-id="01c7e-118">Designates a record that will provide default values based on mapped attribute values.</span></span> <span data-ttu-id="01c7e-119">The lookup object has the following String properties: <code>entityType</code>, <code>id</code>, and <code>name</code> (optional).</span><span class="sxs-lookup"><span data-stu-id="01c7e-119">The lookup object has the following String properties: <code>entityType</code>, <code>id</code>, and <code>name</code> (optional).</span></span></li>
<li><span data-ttu-id="01c7e-120"><b>entityId</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="01c7e-120"><b>entityId</b>: (Optional) String.</span></span> <span data-ttu-id="01c7e-121">ID of the entity record to display the form for.</span><span class="sxs-lookup"><span data-stu-id="01c7e-121">ID of the entity record to display the form for.</span></span></li>
<li><span data-ttu-id="01c7e-122"><b>entityName</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="01c7e-122"><b>entityName</b>: (Optional) String.</span></span> <span data-ttu-id="01c7e-123">Logical name of the entity to display the form for.</span><span class="sxs-lookup"><span data-stu-id="01c7e-123">Logical name of the entity to display the form for.</span></span></li>
<li><span data-ttu-id="01c7e-124"><b>formId</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="01c7e-124"><b>formId</b>: (Optional) String.</span></span> <span data-ttu-id="01c7e-125">ID of the form instance to be displayed.</span><span class="sxs-lookup"><span data-stu-id="01c7e-125">ID of the form instance to be displayed.</span></span></li>
<li><span data-ttu-id="01c7e-126"><b>height</b>: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="01c7e-126"><b>height</b>: (Optional) Number.</span></span> <span data-ttu-id="01c7e-127">Height of the form window to be displayed in pixels.</span><span class="sxs-lookup"><span data-stu-id="01c7e-127">Height of the form window to be displayed in pixels.</span></span></li>
<li><span data-ttu-id="01c7e-128"><b>navbar</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="01c7e-128"><b>navbar</b>: (Optional) String.</span></span> <span data-ttu-id="01c7e-129">Controls whether the navigation bar is displayed and whether application navigation is available using the areas and subareas defined in the sitemap.</span><span class="sxs-lookup"><span data-stu-id="01c7e-129">Controls whether the navigation bar is displayed and whether application navigation is available using the areas and subareas defined in the sitemap.</span></span> <span data-ttu-id="01c7e-130">Valid values are: &quot;on&quot;, &quot;off&quot;, or &quot;entity&quot;.</span><span class="sxs-lookup"><span data-stu-id="01c7e-130">Valid values are: &quot;on&quot;, &quot;off&quot;, or &quot;entity&quot;.</span></span><ul><li><span data-ttu-id="01c7e-131"><code>on</code>: The navigation bar is displayed.</span><span class="sxs-lookup"><span data-stu-id="01c7e-131"><code>on</code>: The navigation bar is displayed.</span></span> <span data-ttu-id="01c7e-132">This is the default behavior if the <b>navbar</b> parameter is not used.</span><span class="sxs-lookup"><span data-stu-id="01c7e-132">This is the default behavior if the <b>navbar</b> parameter is not used.</span></span></li>
<li><span data-ttu-id="01c7e-133"><code>off</code>: The navigation bar is not displayed.</span><span class="sxs-lookup"><span data-stu-id="01c7e-133"><code>off</code>: The navigation bar is not displayed.</span></span> <span data-ttu-id="01c7e-134">People can navigate using other user interface elements or the back and forward buttons.</span><span class="sxs-lookup"><span data-stu-id="01c7e-134">People can navigate using other user interface elements or the back and forward buttons.</span></span></li><li><span data-ttu-id="01c7e-135"><code>entity</code>: On an entity form, only the navigation options for related entities are available.</span><span class="sxs-lookup"><span data-stu-id="01c7e-135"><code>entity</code>: On an entity form, only the navigation options for related entities are available.</span></span> <span data-ttu-id="01c7e-136">After navigating to a related entity, a back button is displayed in the navigation bar to allow returning to the original record.</span><span class="sxs-lookup"><span data-stu-id="01c7e-136">After navigating to a related entity, a back button is displayed in the navigation bar to allow returning to the original record.</span></span></li></ul></li>
<li><span data-ttu-id="01c7e-137"><b>openInNewWindow</b>: (Optional) Boolean.</span><span class="sxs-lookup"><span data-stu-id="01c7e-137"><b>openInNewWindow</b>: (Optional) Boolean.</span></span> <span data-ttu-id="01c7e-138">Indicates whether to display form in a new window.</span><span class="sxs-lookup"><span data-stu-id="01c7e-138">Indicates whether to display form in a new window.</span></span></li>
<li><span data-ttu-id="01c7e-139"><b>windowPosition</b>: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="01c7e-139"><b>windowPosition</b>: (Optional) Number.</span></span> <span data-ttu-id="01c7e-140">Specify one of the following values for the window position of the form on the screen:</span><span class="sxs-lookup"><span data-stu-id="01c7e-140">Specify one of the following values for the window position of the form on the screen:</span></span><ul><li><code>1:center</code></li><li><code>2:side</code></li></ul>
<li><span data-ttu-id="01c7e-141"><b>processId</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="01c7e-141"><b>processId</b>: (Optional) String.</span></span> <span data-ttu-id="01c7e-142">ID of the business process to be displayed on the form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-142">ID of the business process to be displayed on the form.</span></span></li>
<li><span data-ttu-id="01c7e-143"><b>processInstanceId</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="01c7e-143"><b>processInstanceId</b>: (Optional) String.</span></span> <span data-ttu-id="01c7e-144">ID of the business process instance to be displayed on the form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-144">ID of the business process instance to be displayed on the form.</span></span></li>
<li><span data-ttu-id="01c7e-145"><b>relationship</b>: (Optional) Object.</span><span class="sxs-lookup"><span data-stu-id="01c7e-145"><b>relationship</b>: (Optional) Object.</span></span> <span data-ttu-id="01c7e-146">Define a relationship object to display the related records on the form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-146">Define a relationship object to display the related records on the form.</span></span> <span data-ttu-id="01c7e-147">The object has the following attributes.</span><span class="sxs-lookup"><span data-stu-id="01c7e-147">The object has the following attributes.</span></span>
<table style="width:100%">
  <tr>
    <th><span data-ttu-id="01c7e-148">Tên</span><span class="sxs-lookup"><span data-stu-id="01c7e-148">Name</span></span></th>
    <th><span data-ttu-id="01c7e-149">Loại</span><span class="sxs-lookup"><span data-stu-id="01c7e-149">Type</span></span></th> 
    <th><span data-ttu-id="01c7e-150">Mô tả</span><span class="sxs-lookup"><span data-stu-id="01c7e-150">Description</span></span></th>
<tr>
<td><span data-ttu-id="01c7e-151">attributeName</span><span class="sxs-lookup"><span data-stu-id="01c7e-151">attributeName</span></span></td>
<td><span data-ttu-id="01c7e-152">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="01c7e-152">String</span></span></td>
<td><span data-ttu-id="01c7e-153">Name of the attribute used for relationship.</span><span class="sxs-lookup"><span data-stu-id="01c7e-153">Name of the attribute used for relationship.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01c7e-154">tên</span><span class="sxs-lookup"><span data-stu-id="01c7e-154">name</span></span></td>
<td><span data-ttu-id="01c7e-155">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="01c7e-155">String</span></span></td>
<td><span data-ttu-id="01c7e-156">Name of the relationship.</span><span class="sxs-lookup"><span data-stu-id="01c7e-156">Name of the relationship.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01c7e-157">navigationPropertyName</span><span class="sxs-lookup"><span data-stu-id="01c7e-157">navigationPropertyName</span></span></td>
<td><span data-ttu-id="01c7e-158">Chuỗi</span><span class="sxs-lookup"><span data-stu-id="01c7e-158">String</span></span></td>
<td><span data-ttu-id="01c7e-159">Name of the navigation property for this relationship.</span><span class="sxs-lookup"><span data-stu-id="01c7e-159">Name of the navigation property for this relationship.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01c7e-160">relationshipType</span><span class="sxs-lookup"><span data-stu-id="01c7e-160">relationshipType</span></span></td>
<td><span data-ttu-id="01c7e-161">Số</span><span class="sxs-lookup"><span data-stu-id="01c7e-161">Number</span></span></td>
<td><span data-ttu-id="01c7e-162">Relationship type.</span><span class="sxs-lookup"><span data-stu-id="01c7e-162">Relationship type.</span></span> <span data-ttu-id="01c7e-163">Specify one of the following values:</span><span class="sxs-lookup"><span data-stu-id="01c7e-163">Specify one of the following values:</span></span>
<ul><li><code>0:OneToMany</code></li><li><code>1:ManyToMany</code></li></ul></td>
</tr>
<tr>
<td><span data-ttu-id="01c7e-164">roleType</span><span class="sxs-lookup"><span data-stu-id="01c7e-164">roleType</span></span></td>
<td><span data-ttu-id="01c7e-165">Số</span><span class="sxs-lookup"><span data-stu-id="01c7e-165">Number</span></span></td>
<td><span data-ttu-id="01c7e-166">Role type in relationship.</span><span class="sxs-lookup"><span data-stu-id="01c7e-166">Role type in relationship.</span></span> <span data-ttu-id="01c7e-167">Specify one of the following values:</span><span class="sxs-lookup"><span data-stu-id="01c7e-167">Specify one of the following values:</span></span>
<ul><li><code>1:Referencing</code></li><li><code>2:AssociationEntity</code></li></ul></td>
</tr>
</table>
</li>
<li><span data-ttu-id="01c7e-168"><b>selectedStageId</b>: (Optional) String.</span><span class="sxs-lookup"><span data-stu-id="01c7e-168"><b>selectedStageId</b>: (Optional) String.</span></span> <span data-ttu-id="01c7e-169">ID of the selected stage in business process instance.</span><span class="sxs-lookup"><span data-stu-id="01c7e-169">ID of the selected stage in business process instance.</span></span></li>
<li><span data-ttu-id="01c7e-170"><b>useQuickCreateForm</b>: (Optional) Boolean.</span><span class="sxs-lookup"><span data-stu-id="01c7e-170"><b>useQuickCreateForm</b>: (Optional) Boolean.</span></span> <span data-ttu-id="01c7e-171">Indicates whether to open a quick create form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-171">Indicates whether to open a quick create form.</span></span> <span data-ttu-id="01c7e-172">If you do not specify this, by default <b>false</b> is passed.</span><span class="sxs-lookup"><span data-stu-id="01c7e-172">If you do not specify this, by default <b>false</b> is passed.</span></span></li>
<li><span data-ttu-id="01c7e-173"><b>width</b>: (Optional) Number.</span><span class="sxs-lookup"><span data-stu-id="01c7e-173"><b>width</b>: (Optional) Number.</span></span> <span data-ttu-id="01c7e-174">Width of the form window to be displayed in pixels.</span><span class="sxs-lookup"><span data-stu-id="01c7e-174">Width of the form window to be displayed in pixels.</span></span></li>
</ul>
</tr>
<tr>
<td><span data-ttu-id="01c7e-175">formParameters</span><span class="sxs-lookup"><span data-stu-id="01c7e-175">formParameters</span></span></td>
<td><span data-ttu-id="01c7e-176">Đối tượng</span><span class="sxs-lookup"><span data-stu-id="01c7e-176">Object</span></span></td>
<td><span data-ttu-id="01c7e-177">Không</span><span class="sxs-lookup"><span data-stu-id="01c7e-177">No</span></span></td>
<td><span data-ttu-id="01c7e-178">A dictionary object that passes extra parameters to the form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-178">A dictionary object that passes extra parameters to the form.</span></span> <span data-ttu-id="01c7e-179">Invalid parameters will cause an error.</span><span class="sxs-lookup"><span data-stu-id="01c7e-179">Invalid parameters will cause an error.</span></span><br/><br/><span data-ttu-id="01c7e-180">For information about passing parameters to a form, see <a href="../../../set-field-values-using-parameters-passed-form.md" data-raw-source="[Set field values using parameters passed to a form](../../../set-field-values-using-parameters-passed-form.md)">Set field values using parameters passed to a form</a> and <a href="../../../configure-form-accept-custom-querystring-parameters.md" data-raw-source="[Configure a form to accept custom querystring parameters](../../../configure-form-accept-custom-querystring-parameters.md)">Configure a form to accept custom querystring parameters</a> </span><span class="sxs-lookup"><span data-stu-id="01c7e-180">For information about passing parameters to a form, see <a href="../../../set-field-values-using-parameters-passed-form.md" data-raw-source="[Set field values using parameters passed to a form](../../../set-field-values-using-parameters-passed-form.md)">Set field values using parameters passed to a form</a> and <a href="../../../configure-form-accept-custom-querystring-parameters.md" data-raw-source="[Configure a form to accept custom querystring parameters](../../../configure-form-accept-custom-querystring-parameters.md)">Configure a form to accept custom querystring parameters</a> </span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01c7e-181">successCallback</span><span class="sxs-lookup"><span data-stu-id="01c7e-181">successCallback</span></span></td>
<td><span data-ttu-id="01c7e-182">Hàm</span><span class="sxs-lookup"><span data-stu-id="01c7e-182">Function</span></span></td>
<td><span data-ttu-id="01c7e-183">Không</span><span class="sxs-lookup"><span data-stu-id="01c7e-183">No</span></span></td>
<td><span data-ttu-id="01c7e-184">A function to execute when:</span><span class="sxs-lookup"><span data-stu-id="01c7e-184">A function to execute when:</span></span>
<ul>
<li><span data-ttu-id="01c7e-185">The record is saved in the quick create form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-185">The record is saved in the quick create form.</span></span></li>
<li><span data-ttu-id="01c7e-186">The record is saved in the quick create form for a new record created using <b>Save & New</b>.</span><span class="sxs-lookup"><span data-stu-id="01c7e-186">The record is saved in the quick create form for a new record created using <b>Save & New</b>.</span></span> <span data-ttu-id="01c7e-187">This only applies to <a href="/dynamics365/customer-engagement/admin/about-unified-interface" data-raw-source="[Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface)">Unified Interface</a>.</span><span class="sxs-lookup"><span data-stu-id="01c7e-187">This only applies to <a href="/dynamics365/customer-engagement/admin/about-unified-interface" data-raw-source="[Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface)">Unified Interface</a>.</span></span></li>
</ul>

<span data-ttu-id="01c7e-188">This function is passed an object as a parameter.</span><span class="sxs-lookup"><span data-stu-id="01c7e-188">This function is passed an object as a parameter.</span></span> <span data-ttu-id="01c7e-189">The object has a <b>savedEntityReference</b> array with the following properties to identify the record(s) displayed or created:</span><span class="sxs-lookup"><span data-stu-id="01c7e-189">The object has a <b>savedEntityReference</b> array with the following properties to identify the record(s) displayed or created:</span></span>
<ul>
<li><span data-ttu-id="01c7e-190"><b>entityType</b>: The logical name of the entity.</span><span class="sxs-lookup"><span data-stu-id="01c7e-190"><b>entityType</b>: The logical name of the entity.</span></span></li>
<li><span data-ttu-id="01c7e-191"><b>id</b>: A string representation of a GUID value for the record.</span><span class="sxs-lookup"><span data-stu-id="01c7e-191"><b>id</b>: A string representation of a GUID value for the record.</span></span></li>
<li><span data-ttu-id="01c7e-192"><b>name</b>: The primary attribute value of the record displayed or created.</span><span class="sxs-lookup"><span data-stu-id="01c7e-192"><b>name</b>: The primary attribute value of the record displayed or created.</span></span></li></ul>

<span data-ttu-id="01c7e-193"><b>NOTE</b>:</span><span class="sxs-lookup"><span data-stu-id="01c7e-193"><b>NOTE</b>:</span></span>
<ul>
<li><span data-ttu-id="01c7e-194">On web client:</span><span class="sxs-lookup"><span data-stu-id="01c7e-194">On web client:</span></span> <ul>
    <li><span data-ttu-id="01c7e-195">The <b>successCallback</b> function is not executed when you open a form for an existing or new record.</span><span class="sxs-lookup"><span data-stu-id="01c7e-195">The <b>successCallback</b> function is not executed when you open a form for an existing or new record.</span></span></li>
    <li><span data-ttu-id="01c7e-196">The <b>successCallback</b> function is executed only when you save a record in a quick create form that was opened using the <strong>openForm</strong> method.</span><span class="sxs-lookup"><span data-stu-id="01c7e-196">The <b>successCallback</b> function is executed only when you save a record in a quick create form that was opened using the <strong>openForm</strong> method.</span></span></li>
    <li><span data-ttu-id="01c7e-197">When you open a quick create form and create a record, the <b>savedEntityReference</b> array will contain a single item.</span><span class="sxs-lookup"><span data-stu-id="01c7e-197">When you open a quick create form and create a record, the <b>savedEntityReference</b> array will contain a single item.</span></span></li>
  </ul>
</li>
<li><span data-ttu-id="01c7e-198">On <a href="/dynamics365/customer-engagement/admin/about-unified-interface" data-raw-source="[Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface)">Unified Interface</a>:</span><span class="sxs-lookup"><span data-stu-id="01c7e-198">On <a href="/dynamics365/customer-engagement/admin/about-unified-interface" data-raw-source="[Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface)">Unified Interface</a>:</span></span>
<ul>
    <li><span data-ttu-id="01c7e-199">The <b>successCallback</b> function is not executed when you open a form for an existing or new record.</span><span class="sxs-lookup"><span data-stu-id="01c7e-199">The <b>successCallback</b> function is not executed when you open a form for an existing or new record.</span></span></li>
<li><span data-ttu-id="01c7e-200">The <b>successCallback</b> function is executed only when you save a record in a quick create form that was opened using the <strong>openForm</strong> method.</span><span class="sxs-lookup"><span data-stu-id="01c7e-200">The <b>successCallback</b> function is executed only when you save a record in a quick create form that was opened using the <strong>openForm</strong> method.</span></span></li>
    <li><span data-ttu-id="01c7e-201">When you open a quick create form and create a record, the <b>savedEntityReference</b> array will contain a single item.</span><span class="sxs-lookup"><span data-stu-id="01c7e-201">When you open a quick create form and create a record, the <b>savedEntityReference</b> array will contain a single item.</span></span></li>
<li><span data-ttu-id="01c7e-202">When you open a quick create form, and create multiple records by clicking <b>Save & New</b>, the <b>savedEntityReference</b> array will contain multiple items, each item representing the record created using the quick create form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-202">When you open a quick create form, and create multiple records by clicking <b>Save & New</b>, the <b>savedEntityReference</b> array will contain multiple items, each item representing the record created using the quick create form.</span></span></li>
</td>
</tr>
<tr>
<td><span data-ttu-id="01c7e-203">errorCallback</span><span class="sxs-lookup"><span data-stu-id="01c7e-203">errorCallback</span></span></td>
<td><span data-ttu-id="01c7e-204">Hàm</span><span class="sxs-lookup"><span data-stu-id="01c7e-204">Function</span></span></td>
<td><span data-ttu-id="01c7e-205">Không</span><span class="sxs-lookup"><span data-stu-id="01c7e-205">No</span></span></td>
<td><span data-ttu-id="01c7e-206">A function to execute when the operation fails.</span><span class="sxs-lookup"><span data-stu-id="01c7e-206">A function to execute when the operation fails.</span></span><br><span data-ttu-id="01c7e-207">

<b>NOTE</b>: On [Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface), the <b>errorCallback</b> function will be executed only if you are opening a quick create form.</span><span class="sxs-lookup"><span data-stu-id="01c7e-207">

<b>NOTE</b>: On [Unified Interface](/dynamics365/customer-engagement/admin/about-unified-interface), the <b>errorCallback</b> function will be executed only if you are opening a quick create form.</span></span></td>
</tr>
</table>

## <a name="remarks"></a><span data-ttu-id="01c7e-208">Chú thích</span><span class="sxs-lookup"><span data-stu-id="01c7e-208">Remarks</span></span>

<span data-ttu-id="01c7e-209">You must use this method to open entity or quick create forms instead of the deprecated  [Xrm.Utility.openEntityForm](https://msdn.microsoft.com/library/jj602956.aspx#openEntityForm) and  [Xrm.Utility.openQuickCreate](https://msdn.microsoft.com/library/jj602956.aspx#openQuickCreate) methods.</span><span class="sxs-lookup"><span data-stu-id="01c7e-209">You must use this method to open entity or quick create forms instead of the deprecated  [Xrm.Utility.openEntityForm](https://msdn.microsoft.com/library/jj602956.aspx#openEntityForm) and  [Xrm.Utility.openQuickCreate](https://msdn.microsoft.com/library/jj602956.aspx#openQuickCreate) methods.</span></span>
 

## <a name="examples"></a><span data-ttu-id="01c7e-210">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="01c7e-210">Examples</span></span>

### <a name="example-1-open-an-entity-form-for-existing-record"></a><span data-ttu-id="01c7e-211">Example 1: Open an entity form for existing record</span><span class="sxs-lookup"><span data-stu-id="01c7e-211">Example 1: Open an entity form for existing record</span></span>

<span data-ttu-id="01c7e-212">The following sample code opens a contact form to display an existing contact record:</span><span class="sxs-lookup"><span data-stu-id="01c7e-212">The following sample code opens a contact form to display an existing contact record:</span></span>

```JavaScript
var entityFormOptions = {};
entityFormOptions["entityName"] = "contact";
entityFormOptions["entityId"] = "8DA6E5B9-88DF-E311-B8E5-6C3BE5A8B200"

// Open the form.
Xrm.Navigation.openForm(entityFormOptions).then(
    function (success) {
        console.log(success);
    },
    function (error) {
        console.log(error);
    });
```

### <a name="example-2-open-an-entity-form-for-new-record"></a><span data-ttu-id="01c7e-213">Example 2: Open an entity form for new record</span><span class="sxs-lookup"><span data-stu-id="01c7e-213">Example 2: Open an entity form for new record</span></span>

<span data-ttu-id="01c7e-214">The following sample code opens a contact form with some pre-populated values to create a new record:</span><span class="sxs-lookup"><span data-stu-id="01c7e-214">The following sample code opens a contact form with some pre-populated values to create a new record:</span></span>

```JavaScript
var entityFormOptions = {};
entityFormOptions["entityName"] = "contact";

// Set default values for the Contact form
var formParameters = {};
formParameters["firstname"] = "Sample";
formParameters["lastname"] = "Contact";
formParameters["fullname"] = "Sample Contact";
formParameters["emailaddress1"] = "contact@adventure-works.com";
formParameters["jobtitle"] = "Sr. Marketing Manager";
formParameters["donotemail"] = "1";
formParameters["description"] = "Default values for this record were set programmatically.";

// Open the form.
Xrm.Navigation.openForm(entityFormOptions, formParameters).then(
    function (success) {
        console.log(success);
    },
    function (error) {
        console.log(error);
    });
```

### <a name="example-3-open-a-quick-create-form"></a><span data-ttu-id="01c7e-215">Example 3: Open a quick create form</span><span class="sxs-lookup"><span data-stu-id="01c7e-215">Example 3: Open a quick create form</span></span>

<span data-ttu-id="01c7e-216">The following sample code opens a quick create contact form with some pre-populated values:</span><span class="sxs-lookup"><span data-stu-id="01c7e-216">The following sample code opens a quick create contact form with some pre-populated values:</span></span>

```JavaScript
var entityFormOptions = {};
entityFormOptions["entityName"] = "contact";
entityFormOptions["useQuickCreateForm"] = true;

// Set default values for the Contact form
var formParameters = {};
formParameters["firstname"] = "Sample";
formParameters["lastname"] = "Contact";
formParameters["fullname"] = "Sample Contact";
formParameters["emailaddress1"] = "contact@adventure-works.com";
formParameters["jobtitle"] = "Sr. Marketing Manager";
formParameters["donotemail"] = "1";
formParameters["description"] = "Default values for this record were set programmatically.";

// Open the form.
Xrm.Navigation.openForm(entityFormOptions, formParameters).then(
    function (success) {
        console.log(success);
    },
    function (error) {
        console.log(error);
    });
```

### <a name="related-topics"></a><span data-ttu-id="01c7e-217">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="01c7e-217">Related topics</span></span>

[<span data-ttu-id="01c7e-218">Xrm.Navigation</span><span class="sxs-lookup"><span data-stu-id="01c7e-218">Xrm.Navigation</span></span>](../xrm-navigation.md)




