---
title: Create or delete custom sources in Social Engagement | Microsoft Docs
description: Learn how you can add RSS and Atom feeds to a group of custom sources and how you can manage custom sources.
keywords: custom source, custom sources
ms.date: 10/17/2017
ms.service: dynamics-365-marketing
ms.topic: article
applies_to:
- Social Engagement
ms.assetid: eeda21ac-40b8-45ec-a90a-3c22e07c872a
author: m-hartmann
ms.author: mhart
manager: sakudes
topic-status: Drafting
ms.custom:
- dyn365-socialengagement
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365SE
ms.openlocfilehash: 725eda4b55cfdeaf2a8dc1cd4cb0b2bae39fc7dd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375343"
---
# <a name="create-or-delete-custom-sources"></a><span data-ttu-id="2ed83-104">Create or delete custom sources</span><span class="sxs-lookup"><span data-stu-id="2ed83-104">Create or delete custom sources</span></span>

<span data-ttu-id="2ed83-105">Extend the coverage of your data sources by adding public RSS feeds in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span><span class="sxs-lookup"><span data-stu-id="2ed83-105">Extend the coverage of your data sources by adding public RSS feeds in [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)].</span></span> <span data-ttu-id="2ed83-106">Custom sources offer a way to receive additional data from your favorite RSS and Atom feeds.</span><span class="sxs-lookup"><span data-stu-id="2ed83-106">Custom sources offer a way to receive additional data from your favorite RSS and Atom feeds.</span></span> <span data-ttu-id="2ed83-107">Broaden your sources while efficiently keeping track of all of your feeds.</span><span class="sxs-lookup"><span data-stu-id="2ed83-107">Broaden your sources while efficiently keeping track of all of your feeds.</span></span> <span data-ttu-id="2ed83-108">Administrators can also define Search Setup defaults.</span><span class="sxs-lookup"><span data-stu-id="2ed83-108">Administrators can also define Search Setup defaults.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2ed83-109">[Manage global settings](manage-global-settings.md)</span><span class="sxs-lookup"><span data-stu-id="2ed83-109">[Manage global settings](manage-global-settings.md)</span></span>

> [!NOTE]
> [!INCLUDE[proc_permissions_social_listening_admin](../includes/proc-permissions-social-listening-admin.md)] <span data-ttu-id="2ed83-110">[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Understand user roles](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="2ed83-110">[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Understand user roles](user-roles.md)</span></span>

## <a name="create-custom-sources"></a><span data-ttu-id="2ed83-111">Create custom sources</span><span class="sxs-lookup"><span data-stu-id="2ed83-111">Create custom sources</span></span>

> [!TIP]
> <span data-ttu-id="2ed83-112">You need to create a group and add feeds before adding custom sources in Search Setup but you can have one custom source per group.</span><span class="sxs-lookup"><span data-stu-id="2ed83-112">You need to create a group and add feeds before adding custom sources in Search Setup but you can have one custom source per group.</span></span>

1. <span data-ttu-id="2ed83-113">Go to **Search Setup** > **Custom Sources**.</span><span class="sxs-lookup"><span data-stu-id="2ed83-113">Go to **Search Setup** > **Custom Sources**.</span></span>

2. <span data-ttu-id="2ed83-114">In the **Custom Sources** pane, click **Add a custom source** ![Add button](media/add-icon.png "Add button").</span><span class="sxs-lookup"><span data-stu-id="2ed83-114">In the **Custom Sources** pane, click **Add a custom source** ![Add button](media/add-icon.png "Add button").</span></span>

3. <span data-ttu-id="2ed83-115">Enter the name of the group and initials to uniquely identify your sources.</span><span class="sxs-lookup"><span data-stu-id="2ed83-115">Enter the name of the group and initials to uniquely identify your sources.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2ed83-116">It is important to create distinct initials so you can differentiate your custom sources when analyzing your data.</span><span class="sxs-lookup"><span data-stu-id="2ed83-116">It is important to create distinct initials so you can differentiate your custom sources when analyzing your data.</span></span> <span data-ttu-id="2ed83-117">The initials will appear anywhere your custom sources are displayed.</span><span class="sxs-lookup"><span data-stu-id="2ed83-117">The initials will appear anywhere your custom sources are displayed.</span></span>

4. <span data-ttu-id="2ed83-118">Enter your RSS or Atom feed and click the **Add** ![New or Add button](media/plus-icon.png "New or Add button") button to validate and add a source.</span><span class="sxs-lookup"><span data-stu-id="2ed83-118">Enter your RSS or Atom feed and click the **Add** ![New or Add button](media/plus-icon.png "New or Add button") button to validate and add a source.</span></span>

   <span data-ttu-id="2ed83-119">**Example of feed URL**: `http://contoso.com/rss`</span><span class="sxs-lookup"><span data-stu-id="2ed83-119">**Example of feed URL**: `http://contoso.com/rss`</span></span>

5. <span data-ttu-id="2ed83-120">Click **Save** ![Save button](media/save-icon.png "Save button").</span><span class="sxs-lookup"><span data-stu-id="2ed83-120">Click **Save** ![Save button](media/save-icon.png "Save button").</span></span>

## <a name="edit-custom-sources"></a><span data-ttu-id="2ed83-121">Edit custom sources</span><span class="sxs-lookup"><span data-stu-id="2ed83-121">Edit custom sources</span></span>

1.  <span data-ttu-id="2ed83-122">Go to **Search Setup** > **Custom Sources**.</span><span class="sxs-lookup"><span data-stu-id="2ed83-122">Go to **Search Setup** > **Custom Sources**.</span></span>

2.  <span data-ttu-id="2ed83-123">In the custom sources pane, click the custom source group you want to edit.</span><span class="sxs-lookup"><span data-stu-id="2ed83-123">In the custom sources pane, click the custom source group you want to edit.</span></span>

3.  <span data-ttu-id="2ed83-124">Remove sources from the group by clicking the **Remove** ![Delete button](media/delete-icon.png "Delete button") button.</span><span class="sxs-lookup"><span data-stu-id="2ed83-124">Remove sources from the group by clicking the **Remove** ![Delete button](media/delete-icon.png "Delete button") button.</span></span> <span data-ttu-id="2ed83-125">You can also change the name of the group or the initials.</span><span class="sxs-lookup"><span data-stu-id="2ed83-125">You can also change the name of the group or the initials.</span></span>

4.  <span data-ttu-id="2ed83-126">Click **Save** ![Save button](media/save-icon.png "Save button").</span><span class="sxs-lookup"><span data-stu-id="2ed83-126">Click **Save** ![Save button](media/save-icon.png "Save button").</span></span>

## <a name="delete-groups-of-custom-sources"></a><span data-ttu-id="2ed83-127">Delete groups of custom sources</span><span class="sxs-lookup"><span data-stu-id="2ed83-127">Delete groups of custom sources</span></span>

1.  <span data-ttu-id="2ed83-128">Go to **Search Setup** > **Custom Sources**.</span><span class="sxs-lookup"><span data-stu-id="2ed83-128">Go to **Search Setup** > **Custom Sources**.</span></span>

2.  <span data-ttu-id="2ed83-129">In the list of custom sources, click the **Delete** ![Delete button](media/trashbin-icon.png "Delete button") button by the custom sources group you want to delete, and confirm the deletion.</span><span class="sxs-lookup"><span data-stu-id="2ed83-129">In the list of custom sources, click the **Delete** ![Delete button](media/trashbin-icon.png "Delete button") button by the custom sources group you want to delete, and confirm the deletion.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ed83-130">Deleting a custom source has the following effects:</span><span class="sxs-lookup"><span data-stu-id="2ed83-130">Deleting a custom source has the following effects:</span></span>
> - <span data-ttu-id="2ed83-131">Data acquisition for the deleted custom source stops immediately.</span><span class="sxs-lookup"><span data-stu-id="2ed83-131">Data acquisition for the deleted custom source stops immediately.</span></span>
> - <span data-ttu-id="2ed83-132">The custom source is no longer visible in the user interface.</span><span class="sxs-lookup"><span data-stu-id="2ed83-132">The custom source is no longer visible in the user interface.</span></span>
> - <span data-ttu-id="2ed83-133">Search topics, rules, alerts and streams based exclusively on this custom source are deactivated.</span><span class="sxs-lookup"><span data-stu-id="2ed83-133">Search topics, rules, alerts and streams based exclusively on this custom source are deactivated.</span></span>

### <a name="see-also"></a><span data-ttu-id="2ed83-134">See Also</span><span class="sxs-lookup"><span data-stu-id="2ed83-134">See Also</span></span>

<span data-ttu-id="2ed83-135">[Set up searches to listen to social media conversations](set-up-searches.md)  </span><span class="sxs-lookup"><span data-stu-id="2ed83-135">[Set up searches to listen to social media conversations](set-up-searches.md)  </span></span>  
<span data-ttu-id="2ed83-136">[Create or delete a search topic](create-delete-search-topic.md)  </span><span class="sxs-lookup"><span data-stu-id="2ed83-136">[Create or delete a search topic](create-delete-search-topic.md)  </span></span>  
[<span data-ttu-id="2ed83-137">Add rules to a search topic</span><span class="sxs-lookup"><span data-stu-id="2ed83-137">Add rules to a search topic</span></span>](add-rules-search-topic.md)
