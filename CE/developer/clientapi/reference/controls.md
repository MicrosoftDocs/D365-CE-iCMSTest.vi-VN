---
title: Controls in Customer Engagement for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
ms.date: 10/31/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 753ca75a4f15ca1c05f1253216df825304a6fe45
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386763"
---
# <a name="controls-client-api-reference"></a><span data-ttu-id="dd7ca-102">Controls (Client API reference)</span><span class="sxs-lookup"><span data-stu-id="dd7ca-102">Controls (Client API reference)</span></span>

[!INCLUDE[](../../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="dd7ca-103">A control represents an HTML element present on the form.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-103">A control represents an HTML element present on the form.</span></span> <span data-ttu-id="dd7ca-104">Some controls are bound to a specific attribute, whereas others may represent unbound controls such as an IFRAME, Web resource, or a sub grid that has been added to the form.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-104">Some controls are bound to a specific attribute, whereas others may represent unbound controls such as an IFRAME, Web resource, or a sub grid that has been added to the form.</span></span> 

<span data-ttu-id="dd7ca-105">The **control** object provides methods to change the presentation or behavior of a control and identify the corresponding attribute.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-105">The **control** object provides methods to change the presentation or behavior of a control and identify the corresponding attribute.</span></span> <span data-ttu-id="dd7ca-106">You access controls using one of the following collections:</span><span class="sxs-lookup"><span data-stu-id="dd7ca-106">You access controls using one of the following collections:</span></span> 
- <span data-ttu-id="dd7ca-107">**formContext.ui.controls**</span><span class="sxs-lookup"><span data-stu-id="dd7ca-107">**formContext.ui.controls**</span></span>
- <span data-ttu-id="dd7ca-108">**formContext.ui Section.controls**</span><span class="sxs-lookup"><span data-stu-id="dd7ca-108">**formContext.ui Section.controls**</span></span>
- <span data-ttu-id="dd7ca-109">**formContext.data.entity** **Attribute.controls**</span><span class="sxs-lookup"><span data-stu-id="dd7ca-109">**formContext.data.entity** **Attribute.controls**</span></span>

<span data-ttu-id="dd7ca-110">The **formContext**.[getControl](controls/getControl.md) method is a shortcut method to access **formContext.ui.controls.get**.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-110">The **formContext**.[getControl](controls/getControl.md) method is a shortcut method to access **formContext.ui.controls.get**.</span></span> 

<span data-ttu-id="dd7ca-111">Controls are categorized by type.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-111">Controls are categorized by type.</span></span> <span data-ttu-id="dd7ca-112">You can determine the type of a control by using the [getControlType](controls/getControlType.md) method.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-112">You can determine the type of a control by using the [getControlType](controls/getControlType.md) method.</span></span> <span data-ttu-id="dd7ca-113">Certain control methods are only available for specific types of controls.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-113">Certain control methods are only available for specific types of controls.</span></span>

<span data-ttu-id="dd7ca-114">This topic provides information about the methods available per control type.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-114">This topic provides information about the methods available per control type.</span></span> 

## <a name="standard-control-type"></a><span data-ttu-id="dd7ca-115">standard control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-115">standard control type</span></span>

<span data-ttu-id="dd7ca-116">These are the methods available for a Standard control.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-116">These are the methods available for a Standard control.</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="dd7ca-117"><a href="controls/addNotification.md" data-raw-source="[addNotification](controls/addNotification.md)">addNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-117"><a href="controls/addNotification.md" data-raw-source="[addNotification](controls/addNotification.md)">addNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-118"><a href="controls/clearNotification.md" data-raw-source="[clearNotification](controls/clearNotification.md)">clearNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-118"><a href="controls/clearNotification.md" data-raw-source="[clearNotification](controls/clearNotification.md)">clearNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-119"><a href="controls/getAttribute.md" data-raw-source="[getAttribute](controls/getAttribute.md)">getAttribute</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-119"><a href="controls/getAttribute.md" data-raw-source="[getAttribute](controls/getAttribute.md)">getAttribute</a></span></span></a></li>
<li><span data-ttu-id="dd7ca-120"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-120"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span></span></li>
<li><span data-ttu-id="dd7ca-121"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-121"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-122"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-122"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-123"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-123"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span></span></li>
<li><span data-ttu-id="dd7ca-124"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-124"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="dd7ca-125"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-125"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span></span></li>
<li><span data-ttu-id="dd7ca-126"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-126"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-127"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-127"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span></span></li>
<li><span data-ttu-id="dd7ca-128"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-128"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-129"><a href="controls/setNotification.md" data-raw-source="[setNotification](controls/setNotification.md)">setNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-129"><a href="controls/setNotification.md" data-raw-source="[setNotification](controls/setNotification.md)">setNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-130"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-130"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span></span></li>
</ul>
</td>
</tr>
</table>

<span data-ttu-id="dd7ca-131">The following methods for the Standard control are [deprecated](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated) in this release: addOnKeyPress, fireOnKeyPress, and removeOnKeyPress.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-131">The following methods for the Standard control are [deprecated](/dynamics365/get-started/whats-new/customer-engagement/important-changes-coming#some-client-apis-are-deprecated) in this release: addOnKeyPress, fireOnKeyPress, and removeOnKeyPress.</span></span>

## <a name="iframe-control-type"></a><span data-ttu-id="dd7ca-132">iframe control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-132">iframe control type</span></span>

<span data-ttu-id="dd7ca-133">These are the methods available for an IFRAME control.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-133">These are the methods available for an IFRAME control.</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="dd7ca-134"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-134"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span></span></li>
<li><span data-ttu-id="dd7ca-135"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-135"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-136"><a href="controls/getInitialUrl.md" data-raw-source="[getInitialUrl](controls/getInitialUrl.md)">getInitialUrl</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-136"><a href="controls/getInitialUrl.md" data-raw-source="[getInitialUrl](controls/getInitialUrl.md)">getInitialUrl</a></span></span></li>
<li><span data-ttu-id="dd7ca-137"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-137"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-138"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-138"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-139"><a href="controls/getObject.md" data-raw-source="[getObject](controls/getObject.md)">getObject</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-139"><a href="controls/getObject.md" data-raw-source="[getObject](controls/getObject.md)">getObject</a></span></span></li>
<li><span data-ttu-id="dd7ca-140"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-140"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="dd7ca-141"><a href="controls/getSrc.md" data-raw-source="[getSrc](controls/getSrc.md)">getSrc</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-141"><a href="controls/getSrc.md" data-raw-source="[getSrc](controls/getSrc.md)">getSrc</a></span></span></li>
<li><span data-ttu-id="dd7ca-142"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-142"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span></span></li>
<li><span data-ttu-id="dd7ca-143"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-143"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-144"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-144"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span></span></li>
<li><span data-ttu-id="dd7ca-145"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-145"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-146"><a href="controls/setSrc.md" data-raw-source="[setSrc](controls/setSrc.md)">setSrc</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-146"><a href="controls/setSrc.md" data-raw-source="[setSrc](controls/setSrc.md)">setSrc</a></span></span></li>
<li><span data-ttu-id="dd7ca-147"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-147"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span></span></li>
</ul>
</td>
</tr>
</table>

## <a name="kbsearch-knowledge-base-search-control-type"></a><span data-ttu-id="dd7ca-148">kbsearch (Knowledge base search) control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-148">kbsearch (Knowledge base search) control type</span></span>

<span data-ttu-id="dd7ca-149">These are the methods available for knowledge base search control.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-149">These are the methods available for knowledge base search control.</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="dd7ca-150"><a href="controls/addOnPostSearch.md" data-raw-source="[addOnPostSearch](controls/addOnPostSearch.md)">addOnPostSearch</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-150"><a href="controls/addOnPostSearch.md" data-raw-source="[addOnPostSearch](controls/addOnPostSearch.md)">addOnPostSearch</a></span></span></li>
<li><span data-ttu-id="dd7ca-151"><a href="controls/addOnResultOpened.md" data-raw-source="[addOnResultOpened](controls/addOnResultOpened.md)">addOnResultOpened</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-151"><a href="controls/addOnResultOpened.md" data-raw-source="[addOnResultOpened](controls/addOnResultOpened.md)">addOnResultOpened</a></span></span></li>
<li><span data-ttu-id="dd7ca-152"><a href="controls/addOnSelection.md" data-raw-source="[addOnSelection](controls/addOnSelection.md)">addOnSelection</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-152"><a href="controls/addOnSelection.md" data-raw-source="[addOnSelection](controls/addOnSelection.md)">addOnSelection</a></span></span></li>
<li><span data-ttu-id="dd7ca-153"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-153"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span></span></li>
<li><span data-ttu-id="dd7ca-154"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-154"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-155"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-155"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-156"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-156"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-157"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-157"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="dd7ca-158"><a href="controls/getSearchQuery.md" data-raw-source="[getSearchQuery](controls/getSearchQuery.md)">getSearchQuery</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-158"><a href="controls/getSearchQuery.md" data-raw-source="[getSearchQuery](controls/getSearchQuery.md)">getSearchQuery</a></span></span></li>
<li><span data-ttu-id="dd7ca-159"><a href="controls/getSelectedResults.md" data-raw-source="[getSelectedResults](controls/getSelectedResults.md)">getSelectedResults</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-159"><a href="controls/getSelectedResults.md" data-raw-source="[getSelectedResults](controls/getSelectedResults.md)">getSelectedResults</a></span></span></li>
<li><span data-ttu-id="dd7ca-160"><a href="controls/getTotalResultCount.md" data-raw-source="[getTotalResultCount](controls/getTotalResultCount.md)">getTotalResultCount</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-160"><a href="controls/getTotalResultCount.md" data-raw-source="[getTotalResultCount](controls/getTotalResultCount.md)">getTotalResultCount</a></span></span></li>
<li><span data-ttu-id="dd7ca-161"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-161"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span></span></li>
<li><span data-ttu-id="dd7ca-162"><a href="controls/openSearchResult.md" data-raw-source="[openSearchResult](controls/openSearchResult.md)">openSearchResult</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-162"><a href="controls/openSearchResult.md" data-raw-source="[openSearchResult](controls/openSearchResult.md)">openSearchResult</a></span></span></li>
<li><span data-ttu-id="dd7ca-163"><a href="controls/removeOnPostSearch.md" data-raw-source="[removeOnPostSearch](controls/removeOnPostSearch.md)">removeOnPostSearch</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-163"><a href="controls/removeOnPostSearch.md" data-raw-source="[removeOnPostSearch](controls/removeOnPostSearch.md)">removeOnPostSearch</a></span></span></li>

</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-164"><a href="controls/removeOnResultOpened.md" data-raw-source="[removeOnResultOpened](controls/removeOnResultOpened.md)">removeOnResultOpened</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-164"><a href="controls/removeOnResultOpened.md" data-raw-source="[removeOnResultOpened](controls/removeOnResultOpened.md)">removeOnResultOpened</a></span></span></li>
<li><span data-ttu-id="dd7ca-165"><a href="controls/removeOnSelection.md" data-raw-source="[removeOnSelection](controls/removeOnSelection.md)">removeOnSelection</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-165"><a href="controls/removeOnSelection.md" data-raw-source="[removeOnSelection](controls/removeOnSelection.md)">removeOnSelection</a></span></span></li>
<li><span data-ttu-id="dd7ca-166"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-166"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span></span></li>
<li><span data-ttu-id="dd7ca-167"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-167"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-168"><a href="controls/setSearchQuery.md" data-raw-source="[setSearchQuery](controls/setSearchQuery.md)">setSearchQuery</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-168"><a href="controls/setSearchQuery.md" data-raw-source="[setSearchQuery](controls/setSearchQuery.md)">setSearchQuery</a></span></span></li>
<li><span data-ttu-id="dd7ca-169"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-169"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span></span></li>
</ul>
</td>
</tr>
</table>

>[!NOTE]
><span data-ttu-id="dd7ca-170">When the knowledge base search control is added to the social pane, the name of the control will be "searchwidgetcontrol_notescontrol".</span><span class="sxs-lookup"><span data-stu-id="dd7ca-170">When the knowledge base search control is added to the social pane, the name of the control will be "searchwidgetcontrol_notescontrol".</span></span> <span data-ttu-id="dd7ca-171">This name can’t be changed.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-171">This name can’t be changed.</span></span> 

## <a name="lookup-control-type"></a><span data-ttu-id="dd7ca-172">lookup control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-172">lookup control type</span></span>

<span data-ttu-id="dd7ca-173">These are the methods available for a lookup control.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-173">These are the methods available for a lookup control.</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="dd7ca-174"><a href="controls/addCustomFilter.md" data-raw-source="[addCustomFilter](controls/addCustomFilter.md)">addCustomFilter</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-174"><a href="controls/addCustomFilter.md" data-raw-source="[addCustomFilter](controls/addCustomFilter.md)">addCustomFilter</a></span></span></li>
<li><span data-ttu-id="dd7ca-175"><a href="controls/addCustomView.md" data-raw-source="[addCustomView](controls/addCustomView.md)">addCustomView</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-175"><a href="controls/addCustomView.md" data-raw-source="[addCustomView](controls/addCustomView.md)">addCustomView</a></span></span></li>
<li><span data-ttu-id="dd7ca-176"><a href="controls/addNotification.md" data-raw-source="[addNotification](controls/addNotification.md)">addNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-176"><a href="controls/addNotification.md" data-raw-source="[addNotification](controls/addNotification.md)">addNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-177"><a href="controls/addPreSearch.md" data-raw-source="[addPreSearch](controls/addPreSearch.md)">addPreSearch</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-177"><a href="controls/addPreSearch.md" data-raw-source="[addPreSearch](controls/addPreSearch.md)">addPreSearch</a></span></span></li>
<li><span data-ttu-id="dd7ca-178"><a href="controls/clearNotification.md" data-raw-source="[clearNotification](controls/clearNotification.md)">clearNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-178"><a href="controls/clearNotification.md" data-raw-source="[clearNotification](controls/clearNotification.md)">clearNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-179"><a href="controls/getAttribute.md" data-raw-source="[getAttribute](controls/getAttribute.md)">getAttribute</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-179"><a href="controls/getAttribute.md" data-raw-source="[getAttribute](controls/getAttribute.md)">getAttribute</a></span></span></a></li>
<li><span data-ttu-id="dd7ca-180"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-180"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span></span></li>
<li><span data-ttu-id="dd7ca-181"><a href="controls/getDefaultView.md" data-raw-source="[getDefaultView](controls/getDefaultView.md)">getDefaultView</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-181"><a href="controls/getDefaultView.md" data-raw-source="[getDefaultView](controls/getDefaultView.md)">getDefaultView</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-182"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-182"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-183"><a href="controls/getEntityTypes.md" data-raw-source="[getEntityTypes](controls/getEntityTypes.md)">getEntityTypes</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-183"><a href="controls/getEntityTypes.md" data-raw-source="[getEntityTypes](controls/getEntityTypes.md)">getEntityTypes</a></span></span></li>
<li><span data-ttu-id="dd7ca-184"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-184"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-185"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-185"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span></span></li>
<li><span data-ttu-id="dd7ca-186"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-186"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="dd7ca-187"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-187"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span></span></li>
<li><span data-ttu-id="dd7ca-188"><a href="controls/removePreSearch.md" data-raw-source="[removePreSearch](controls/removePreSearch.md)">removePreSearch</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-188"><a href="controls/removePreSearch.md" data-raw-source="[removePreSearch](controls/removePreSearch.md)">removePreSearch</a></span></span></li>
<li><span data-ttu-id="dd7ca-189"><a href="controls/setDefaultView.md" data-raw-source="[setDefaultView](controls/setDefaultView.md)">setDefaultView</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-189"><a href="controls/setDefaultView.md" data-raw-source="[setDefaultView](controls/setDefaultView.md)">setDefaultView</a></span></span></li>

</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-190"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-190"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-191"><a href="controls/setEntityTypes.md" data-raw-source="[setEntityTypes](controls/setEntityTypes.md)">setEntityTypes</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-191"><a href="controls/setEntityTypes.md" data-raw-source="[setEntityTypes](controls/setEntityTypes.md)">setEntityTypes</a></span></span></li>
<li><span data-ttu-id="dd7ca-192"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-192"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span></span></li>
<li><span data-ttu-id="dd7ca-193"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-193"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-194"><a href="controls/setNotification.md" data-raw-source="[setNotification](controls/setNotification.md)">setNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-194"><a href="controls/setNotification.md" data-raw-source="[setNotification](controls/setNotification.md)">setNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-195"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-195"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span></span></li>
</ul>
</td>
</tr>
</table>

## <a name="multiselectoptionset-and-optionset-control-types"></a><span data-ttu-id="dd7ca-196">multiselectoptionset and optionset control types</span><span class="sxs-lookup"><span data-stu-id="dd7ca-196">multiselectoptionset and optionset control types</span></span>

<span data-ttu-id="dd7ca-197">Both multi-select option set and option set controls have the same set of methods available.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-197">Both multi-select option set and option set controls have the same set of methods available.</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="dd7ca-198"><a href="controls/addNotification.md" data-raw-source="[addNotification](controls/addNotification.md)">addNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-198"><a href="controls/addNotification.md" data-raw-source="[addNotification](controls/addNotification.md)">addNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-199"><a href="controls/addOption.md" data-raw-source="[addOption](controls/addOption.md)">addOption</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-199"><a href="controls/addOption.md" data-raw-source="[addOption](controls/addOption.md)">addOption</a></span></span></li>
<li><span data-ttu-id="dd7ca-200"><a href="controls/clearNotification.md" data-raw-source="[clearNotification](controls/clearNotification.md)">clearNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-200"><a href="controls/clearNotification.md" data-raw-source="[clearNotification](controls/clearNotification.md)">clearNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-201"><a href="controls/clearOptions.md" data-raw-source="[clearOptions](controls/clearOptions.md)">clearOptions</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-201"><a href="controls/clearOptions.md" data-raw-source="[clearOptions](controls/clearOptions.md)">clearOptions</a></span></span></li>
<li><span data-ttu-id="dd7ca-202"><a href="controls/getAttribute.md" data-raw-source="[getAttribute](controls/getAttribute.md)">getAttribute</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-202"><a href="controls/getAttribute.md" data-raw-source="[getAttribute](controls/getAttribute.md)">getAttribute</a></span></span></a></li>
<li><span data-ttu-id="dd7ca-203"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-203"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-204"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-204"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-205"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-205"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-206"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-206"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span></span></li>
<li><span data-ttu-id="dd7ca-207"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-207"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="dd7ca-208"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-208"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span></span></li>
<li><span data-ttu-id="dd7ca-209"><a href="controls/removeoption.md" data-raw-source="[removeOption](controls/removeoption.md)">removeOption</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-209"><a href="controls/removeoption.md" data-raw-source="[removeOption](controls/removeoption.md)">removeOption</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-210"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-210"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-211"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-211"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span></span></li>
<li><span data-ttu-id="dd7ca-212"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-212"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-213"><a href="controls/setNotification.md" data-raw-source="[setNotification](controls/setNotification.md)">setNotification</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-213"><a href="controls/setNotification.md" data-raw-source="[setNotification](controls/setNotification.md)">setNotification</a></span></span></li>
<li><span data-ttu-id="dd7ca-214"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-214"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span></span></li>
</ul>
</td>
</tr>
</table>

## <a name="quickform-control-type"></a><span data-ttu-id="dd7ca-215">quickform control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-215">quickform control type</span></span>

<span data-ttu-id="dd7ca-216">See [formContext.ui.quickForms](formcontext-ui-quickforms.md) for information about methods supported for this control type.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-216">See [formContext.ui.quickForms](formcontext-ui-quickforms.md) for information about methods supported for this control type.</span></span>

## <a name="subgrid-control-type"></a><span data-ttu-id="dd7ca-217">subgrid control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-217">subgrid control type</span></span>

<span data-ttu-id="dd7ca-218">See [Grids and subgrids](grids.md) for information methods supported for this control type.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-218">See [Grids and subgrids](grids.md) for information methods supported for this control type.</span></span>

## <a name="timelinewall-control-type"></a><span data-ttu-id="dd7ca-219">timelinewall control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-219">timelinewall control type</span></span>

<span data-ttu-id="dd7ca-220">The timeline control is a new control type introduced in Dynamics 365 for Customer Engagement apps version 9.0 that presents the Posts, Activities, and Notes in a unified view.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-220">The timeline control is a new control type introduced in Dynamics 365 for Customer Engagement apps version 9.0 that presents the Posts, Activities, and Notes in a unified view.</span></span> <span data-ttu-id="dd7ca-221">These are the methods available for this control type.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-221">These are the methods available for this control type.</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="dd7ca-222"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-222"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span></span></li>
<li><span data-ttu-id="dd7ca-223"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-223"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-224"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-224"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-225"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-225"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span></span></li>
</ul>
</td>
<td>
<ul>

<li><span data-ttu-id="dd7ca-226"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-226"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="dd7ca-227"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-227"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span></span></li>
<li><span data-ttu-id="dd7ca-228"><a href="controls/refresh.md" data-raw-source="[refresh](controls/refresh.md)">refresh</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-228"><a href="controls/refresh.md" data-raw-source="[refresh](controls/refresh.md)">refresh</a></span></span></li>
<li><span data-ttu-id="dd7ca-229"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-229"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-230"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-230"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span></span></li>
<li><span data-ttu-id="dd7ca-231"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-231"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-232"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-232"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span></span></li>
</ul>
</td>
</tr>
</table>

## <a name="timer-control-type"></a><span data-ttu-id="dd7ca-233">timer control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-233">timer control type</span></span>

<span data-ttu-id="dd7ca-234">These are the methods available for the timer control.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-234">These are the methods available for the timer control.</span></span>

<table>
<tr>
<td>
<ul>
<li><span data-ttu-id="dd7ca-235"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-235"><a href="controls/getControlType.md" data-raw-source="[getControlType](controls/getControlType.md)">getControlType</a></span></span></li>
<li><span data-ttu-id="dd7ca-236"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-236"><a href="controls/getDisabled.md" data-raw-source="[getDisabled](controls/getDisabled.md)">getDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-237"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-237"><a href="controls/getLabel.md" data-raw-source="[getLabel](controls/getLabel.md)">getLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-238"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-238"><a href="controls/getName.md" data-raw-source="[getName](controls/getName.md)">getName</a></span></span></li>
</ul>
</td>
<td>
<ul>

<li><span data-ttu-id="dd7ca-239"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-239"><a href="controls/getParent.md" data-raw-source="[getParent](controls/getParent.md)">getParent</a></span></span></li>
<li><span data-ttu-id="dd7ca-240"><a href="controls/getState.md" data-raw-source="[getState](controls/getState.md)">getState</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-240"><a href="controls/getState.md" data-raw-source="[getState](controls/getState.md)">getState</a></span></span></li>
<li><span data-ttu-id="dd7ca-241"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-241"><a href="controls/getVisible.md" data-raw-source="[getVisible](controls/getVisible.md)">getVisible</a></span></span></li>
<li><span data-ttu-id="dd7ca-242"><a href="controls/refresh.md" data-raw-source="[refresh](controls/refresh.md)">refresh</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-242"><a href="controls/refresh.md" data-raw-source="[refresh](controls/refresh.md)">refresh</a></span></span></li>

</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="dd7ca-243"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-243"><a href="controls/setDisabled.md" data-raw-source="[setDisabled](controls/setDisabled.md)">setDisabled</a></span></span></li>
<li><span data-ttu-id="dd7ca-244"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-244"><a href="controls/setFocus.md" data-raw-source="[setFocus](controls/setFocus.md)">setFocus</a></span></span></li>
<li><span data-ttu-id="dd7ca-245"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-245"><a href="controls/setLabel.md" data-raw-source="[setLabel](controls/setLabel.md)">setLabel</a></span></span></li>
<li><span data-ttu-id="dd7ca-246"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span><span class="sxs-lookup"><span data-stu-id="dd7ca-246"><a href="controls/setVisible.md" data-raw-source="[setVisible](controls/setVisible.md)">setVisible</a></span></span></li>
</ul>
</td>
</tr>
</table>

## <a name="webresource-control-type"></a><span data-ttu-id="dd7ca-247">webresource control type</span><span class="sxs-lookup"><span data-stu-id="dd7ca-247">webresource control type</span></span>

<span data-ttu-id="dd7ca-248">A web resource control has the same set of methods available as the iframe control.</span><span class="sxs-lookup"><span data-stu-id="dd7ca-248">A web resource control has the same set of methods available as the iframe control.</span></span> <span data-ttu-id="dd7ca-249">See [iframe control type](#iframe-control-type)</span><span class="sxs-lookup"><span data-stu-id="dd7ca-249">See [iframe control type](#iframe-control-type)</span></span>

### <a name="related-topics"></a><span data-ttu-id="dd7ca-250">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="dd7ca-250">Related topics</span></span>

[<span data-ttu-id="dd7ca-251">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="dd7ca-251">Attributes</span></span>](attributes.md)
