---
title: Attributes in Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Learn about working with attributes in Customer Engagement using client API.
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 32e8d1d0-4093-4588-a517-2930eec34dce
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 61af3b6e536dc5496d8d546d57eb5e7b187bd51a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388636"
---
# <a name="attributes-client-api-reference"></a><span data-ttu-id="e0a07-103">Attributes (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e0a07-103">Attributes (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="e0a07-104">Attributes contain data in the Customer Engagement form or grids.</span><span class="sxs-lookup"><span data-stu-id="e0a07-104">Attributes contain data in the Customer Engagement form or grids.</span></span> <span data-ttu-id="e0a07-105">Use the `formContext.data.entity.attributes` collection or the `formContext.getAttribute` shortcut method to access a collection of attributes.</span><span class="sxs-lookup"><span data-stu-id="e0a07-105">Use the `formContext.data.entity.attributes` collection or the `formContext.getAttribute` shortcut method to access a collection of attributes.</span></span> <span data-ttu-id="e0a07-106">For more information about collections, see [Collections (Client API reference)](collections.md).</span><span class="sxs-lookup"><span data-stu-id="e0a07-106">For more information about collections, see [Collections (Client API reference)](collections.md).</span></span> 

<span data-ttu-id="e0a07-107">To access an attribute within the collection, you pass either the name (string) or the index value (number) of the attribute as an argument to the method.</span><span class="sxs-lookup"><span data-stu-id="e0a07-107">To access an attribute within the collection, you pass either the name (string) or the index value (number) of the attribute as an argument to the method.</span></span> <span data-ttu-id="e0a07-108">Ví dụ: `formContext.getAttribute(arg)`</span><span class="sxs-lookup"><span data-stu-id="e0a07-108">For example: `formContext.getAttribute(arg)`</span></span>

<span data-ttu-id="e0a07-109">Attributes are categorized by type.</span><span class="sxs-lookup"><span data-stu-id="e0a07-109">Attributes are categorized by type.</span></span> <span data-ttu-id="e0a07-110">You can determine the type of an attribute by using the [getAttributeType](attributes/getAttributeType.md) method.</span><span class="sxs-lookup"><span data-stu-id="e0a07-110">You can determine the type of an attribute by using the [getAttributeType](attributes/getAttributeType.md) method.</span></span> <span data-ttu-id="e0a07-111">Certain attribute methods are only available for specific types of attributes.</span><span class="sxs-lookup"><span data-stu-id="e0a07-111">Certain attribute methods are only available for specific types of attributes.</span></span>

<span data-ttu-id="e0a07-112">This topic provides information about the methods available per attribute type.</span><span class="sxs-lookup"><span data-stu-id="e0a07-112">This topic provides information about the methods available per attribute type.</span></span> 

## <a name="all-attribute-types"></a><span data-ttu-id="e0a07-113">All attribute types</span><span class="sxs-lookup"><span data-stu-id="e0a07-113">All attribute types</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="e0a07-114"><a href="attributes/controls-collection.md" data-raw-source="[controls](attributes/controls-collection.md)">controls</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-114"><a href="attributes/controls-collection.md" data-raw-source="[controls](attributes/controls-collection.md)">controls</a></span></span></li>
<li><span data-ttu-id="e0a07-115"><a href="attributes/addOnChange.md" data-raw-source="[addOnChange](attributes/addOnChange.md)">addOnChange</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-115"><a href="attributes/addOnChange.md" data-raw-source="[addOnChange](attributes/addOnChange.md)">addOnChange</a></span></span></li>
<li><span data-ttu-id="e0a07-116"><a href="attributes/fireOnChange.md" data-raw-source="[fireOnChange](attributes/fireOnChange.md)">fireOnChange</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-116"><a href="attributes/fireOnChange.md" data-raw-source="[fireOnChange](attributes/fireOnChange.md)">fireOnChange</a></span></span></a></li>
<li><span data-ttu-id="e0a07-117"><a href="attributes/getAttributeType.md" data-raw-source="[getAttributeType](attributes/getAttributeType.md)">getAttributeType</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-117"><a href="attributes/getAttributeType.md" data-raw-source="[getAttributeType](attributes/getAttributeType.md)">getAttributeType</a></span></span></li>
<li><span data-ttu-id="e0a07-118"><a href="attributes/getFormat.md" data-raw-source="[getFormat](attributes/getFormat.md)">getFormat</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-118"><a href="attributes/getFormat.md" data-raw-source="[getFormat](attributes/getFormat.md)">getFormat</a></span></span></li>
<li><span data-ttu-id="e0a07-119"><a href="attributes/getIsDirty.md" data-raw-source="[getIsDirty](attributes/getIsDirty.md)">getIsDirty</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-119"><a href="attributes/getIsDirty.md" data-raw-source="[getIsDirty](attributes/getIsDirty.md)">getIsDirty</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="e0a07-120"><a href="attributes/getName.md" data-raw-source="[getName](attributes/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-120"><a href="attributes/getName.md" data-raw-source="[getName](attributes/getName.md)">getName</a></span></span></li>
<li><span data-ttu-id="e0a07-121"><a href="attributes/getParent.md" data-raw-source="[getParent](attributes/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-121"><a href="attributes/getParent.md" data-raw-source="[getParent](attributes/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="e0a07-122"><a href="attributes/getRequiredLevel.md" data-raw-source="[getRequiredLevel](attributes/getRequiredLevel.md)">getRequiredLevel</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-122"><a href="attributes/getRequiredLevel.md" data-raw-source="[getRequiredLevel](attributes/getRequiredLevel.md)">getRequiredLevel</a></span></span></li>
<li><span data-ttu-id="e0a07-123"><a href="attributes/getSubmitMode.md" data-raw-source="[getSubmitMode](attributes/getSubmitMode.md)">getSubmitMode</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-123"><a href="attributes/getSubmitMode.md" data-raw-source="[getSubmitMode](attributes/getSubmitMode.md)">getSubmitMode</a></span></span></li>
<li><span data-ttu-id="e0a07-124"><a href="attributes/getUserPrivilege.md" data-raw-source="[getUserPrivilege](attributes/getUserPrivilege.md)">getUserPrivilege</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-124"><a href="attributes/getUserPrivilege.md" data-raw-source="[getUserPrivilege](attributes/getUserPrivilege.md)">getUserPrivilege</a></span></span></li>
<li><span data-ttu-id="e0a07-125"><a href="attributes/getValue.md" data-raw-source="[getValue](attributes/getValue.md)">getValue</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-125"><a href="attributes/getValue.md" data-raw-source="[getValue](attributes/getValue.md)">getValue</a></span></span></li>
</ul>
</td>
<td>
<ul>

<li><span data-ttu-id="e0a07-126"><a href="attributes/isValid.md" data-raw-source="[isValid](attributes/isValid.md)">isValid</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-126"><a href="attributes/isValid.md" data-raw-source="[isValid](attributes/isValid.md)">isValid</a></span></span></li>
<li><span data-ttu-id="e0a07-127"><a href="attributes/removeOnChange.md" data-raw-source="[removeOnChange](attributes/removeOnChange.md)">removeOnChange</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-127"><a href="attributes/removeOnChange.md" data-raw-source="[removeOnChange](attributes/removeOnChange.md)">removeOnChange</a></span></span></li>
<li><span data-ttu-id="e0a07-128"><a href="attributes/setRequiredLevel.md" data-raw-source="[setRequiredLevel](attributes/setRequiredLevel.md)">setRequiredLevel</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-128"><a href="attributes/setRequiredLevel.md" data-raw-source="[setRequiredLevel](attributes/setRequiredLevel.md)">setRequiredLevel</a></span></span></li>
<li><span data-ttu-id="e0a07-129"><a href="attributes/setSubmitMode.md" data-raw-source="[setSubmitMode](attributes/setSubmitMode.md)">setSubmitMode</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-129"><a href="attributes/setSubmitMode.md" data-raw-source="[setSubmitMode](attributes/setSubmitMode.md)">setSubmitMode</a></span></span></li>
<li><span data-ttu-id="e0a07-130"><a href="attributes/setValue.md" data-raw-source="[setValue](attributes/setValue.md)">setValue</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-130"><a href="attributes/setValue.md" data-raw-source="[setValue](attributes/setValue.md)">setValue</a></span></span></li>
</ul>
</td>
</tr>
</table>


## <a name="boolean-attribute-type"></a><span data-ttu-id="e0a07-131">Boolean attribute type</span><span class="sxs-lookup"><span data-stu-id="e0a07-131">Boolean attribute type</span></span>
<span data-ttu-id="e0a07-132">In addition to the methods available for all attribute types as explained ealier, the following method is available only for the **boolean** attribute:</span><span class="sxs-lookup"><span data-stu-id="e0a07-132">In addition to the methods available for all attribute types as explained ealier, the following method is available only for the **boolean** attribute:</span></span>

- [<span data-ttu-id="e0a07-133">getInitialValue</span><span class="sxs-lookup"><span data-stu-id="e0a07-133">getInitialValue</span></span>](attributes/getInitialValue.md)

## <a name="lookup-attribute-type"></a><span data-ttu-id="e0a07-134">Lookup attribute type</span><span class="sxs-lookup"><span data-stu-id="e0a07-134">Lookup attribute type</span></span>
<span data-ttu-id="e0a07-135">In addition to the methods available for all attribute types as explained ealier, the following method is available only for the **lookup** attribute:</span><span class="sxs-lookup"><span data-stu-id="e0a07-135">In addition to the methods available for all attribute types as explained ealier, the following method is available only for the **lookup** attribute:</span></span>

- [<span data-ttu-id="e0a07-136">getIsPartyList</span><span class="sxs-lookup"><span data-stu-id="e0a07-136">getIsPartyList</span></span>](attributes/getIsPartyList.md)

## <a name="multiselectoptionset-and-optionset-attribute-types"></a><span data-ttu-id="e0a07-137">MultiSelectOptionSet and OptionSet attribute types</span><span class="sxs-lookup"><span data-stu-id="e0a07-137">MultiSelectOptionSet and OptionSet attribute types</span></span>

<span data-ttu-id="e0a07-138">In addition to the methods available for all attribute types as explained ealier, the following methods are available only for the **multiselectoption** and **optionset** attributes:</span><span class="sxs-lookup"><span data-stu-id="e0a07-138">In addition to the methods available for all attribute types as explained ealier, the following methods are available only for the **multiselectoption** and **optionset** attributes:</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="e0a07-139"><a href="attributes/getInitialValue.md" data-raw-source="[getInitialValue](attributes/getInitialValue.md)">getInitialValue</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-139"><a href="attributes/getInitialValue.md" data-raw-source="[getInitialValue](attributes/getInitialValue.md)">getInitialValue</a></span></span></li>
<li><span data-ttu-id="e0a07-140"><a href="attributes/getOption.md" data-raw-source="[getOption](attributes/getOption.md)">getOption</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-140"><a href="attributes/getOption.md" data-raw-source="[getOption](attributes/getOption.md)">getOption</a></span></span></li>
<li><span data-ttu-id="e0a07-141"><a href="attributes/getOptions.md" data-raw-source="[getOptions](attributes/getOptions.md)">getOptions</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-141"><a href="attributes/getOptions.md" data-raw-source="[getOptions](attributes/getOptions.md)">getOptions</a></span></span></a></li>
<li><span data-ttu-id="e0a07-142"><a href="attributes/getSelectedOption.md" data-raw-source="[getSelectedOption](attributes/getSelectedOption.md)">getSelectedOption</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-142"><a href="attributes/getSelectedOption.md" data-raw-source="[getSelectedOption](attributes/getSelectedOption.md)">getSelectedOption</a></span></span></li>
<li><span data-ttu-id="e0a07-143"><a href="attributes/getText.md" data-raw-source="[getText](attributes/getText.md)">getText</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-143"><a href="attributes/getText.md" data-raw-source="[getText](attributes/getText.md)">getText</a></span></span></li>
</ul>
</td>
</tr>
</table>

## <a name="number-attribute-type-decimal-double-integer-money"></a><span data-ttu-id="e0a07-144">Number attribute type (decimal, double, integer, money)</span><span class="sxs-lookup"><span data-stu-id="e0a07-144">Number attribute type (decimal, double, integer, money)</span></span>
<span data-ttu-id="e0a07-145">The following methods are available only for the **decimal**,  **double**, and **integer** attributes:</span><span class="sxs-lookup"><span data-stu-id="e0a07-145">The following methods are available only for the **decimal**,  **double**, and **integer** attributes:</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="e0a07-146"><a href="attributes/getMax.md" data-raw-source="[getMax](attributes/getMax.md)">getMax</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-146"><a href="attributes/getMax.md" data-raw-source="[getMax](attributes/getMax.md)">getMax</a></span></span></li>
<li><span data-ttu-id="e0a07-147"><a href="attributes/getMin.md" data-raw-source="[getMin](attributes/getMin.md)">getMin</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-147"><a href="attributes/getMin.md" data-raw-source="[getMin](attributes/getMin.md)">getMin</a></span></span></li>
<li><span data-ttu-id="e0a07-148"><a href="attributes/getPrecision.md" data-raw-source="[getPrecision](attributes/getPrecision.md)">getPrecision</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-148"><a href="attributes/getPrecision.md" data-raw-source="[getPrecision](attributes/getPrecision.md)">getPrecision</a></span></span></a></li>
<li><span data-ttu-id="e0a07-149"><a href="attributes/setPrecision.md" data-raw-source="[setPrecision](attributes/setPrecision.md)">setPrecision</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-149"><a href="attributes/setPrecision.md" data-raw-source="[setPrecision](attributes/setPrecision.md)">setPrecision</a></span></span></li>
<li><span data-ttu-id="e0a07-150"><a href="attributes/getText.md" data-raw-source="[getText](attributes/getText.md)">getText</a></span><span class="sxs-lookup"><span data-stu-id="e0a07-150"><a href="attributes/getText.md" data-raw-source="[getText](attributes/getText.md)">getText</a></span></span></li>
</ul>
</td>
</tr>
</table>

## <a name="string-attribute-type"></a><span data-ttu-id="e0a07-151">String attribute type</span><span class="sxs-lookup"><span data-stu-id="e0a07-151">String attribute type</span></span>
<span data-ttu-id="e0a07-152">In addition to the methods available for all attribute types as explained ealier, the following method is available only for the **string** attribute:</span><span class="sxs-lookup"><span data-stu-id="e0a07-152">In addition to the methods available for all attribute types as explained ealier, the following method is available only for the **string** attribute:</span></span>

- [<span data-ttu-id="e0a07-153">getMaxLength</span><span class="sxs-lookup"><span data-stu-id="e0a07-153">getMaxLength</span></span>](attributes/getMaxLength.md)

### <a name="related-topics"></a><span data-ttu-id="e0a07-154">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="e0a07-154">Related topics</span></span>

[<span data-ttu-id="e0a07-155">Composite attributes</span><span class="sxs-lookup"><span data-stu-id="e0a07-155">Composite attributes</span></span>](composite-attributes.md)

[<span data-ttu-id="e0a07-156">Understand Xrm object model</span><span class="sxs-lookup"><span data-stu-id="e0a07-156">Understand Xrm object model</span></span>](../understand-clientapi-object-model.md)

[<span data-ttu-id="e0a07-157">Controls (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="e0a07-157">Controls (Client API reference)</span></span>](controls.md)




