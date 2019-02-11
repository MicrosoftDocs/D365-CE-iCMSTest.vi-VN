---
title: Data retention in Social Engagement | Microsoft Docs
description: Find out how long data is stored when working with Social Engagement.
ms.custom:
- dyn365-socialengagement
ms.date: 06/13/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to: Social Engagement
ms.assetid: d3617d7f-29df-42e9-baff-4625ab4ee85a
author: m-hartmann
ms.author: mhart
manager: sakudes
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365SE
ms.openlocfilehash: f84a4846a5a1a388f757720df9156016250d1391
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375701"
---
# <a name="data-retention-in-includepnnetbreezeshortincludespn-social-engagement-shortmd"></a><span data-ttu-id="a2fca-103">Data retention in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]</span><span class="sxs-lookup"><span data-stu-id="a2fca-103">Data retention in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)]</span></span>

<span data-ttu-id="a2fca-104">Get to know which user data gets stored when you work with [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and how long this data persists.</span><span class="sxs-lookup"><span data-stu-id="a2fca-104">Get to know which user data gets stored when you work with [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] and how long this data persists.</span></span> <span data-ttu-id="a2fca-105">Whenever data is stored in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], either as acquired posts or user settings, it’s stored in a database.</span><span class="sxs-lookup"><span data-stu-id="a2fca-105">Whenever data is stored in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)], either as acquired posts or user settings, it’s stored in a database.</span></span> <span data-ttu-id="a2fca-106">While posts end up in a central data store, all other data is stored in a solution-specific database.</span><span class="sxs-lookup"><span data-stu-id="a2fca-106">While posts end up in a central data store, all other data is stored in a solution-specific database.</span></span> <span data-ttu-id="a2fca-107">Posts acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] are available for analysis for 15 months before they are automatically removed from the database.</span><span class="sxs-lookup"><span data-stu-id="a2fca-107">Posts acquired in [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] are available for analysis for 15 months before they are automatically removed from the database.</span></span> <span data-ttu-id="a2fca-108">If you need to keep track of older data for reporting purposes, you can [export the data](analyze-social-data-using-widgets.md#export-data-from-widgets) before it reaches the retention time.</span><span class="sxs-lookup"><span data-stu-id="a2fca-108">If you need to keep track of older data for reporting purposes, you can [export the data](analyze-social-data-using-widgets.md#export-data-from-widgets) before it reaches the retention time.</span></span>     
  
## <a name="storage-of-private-messages-and-direct-messages-as-regular-posts"></a><span data-ttu-id="a2fca-109">Storage of private messages and direct messages as regular posts</span><span class="sxs-lookup"><span data-stu-id="a2fca-109">Storage of private messages and direct messages as regular posts</span></span> 

<span data-ttu-id="a2fca-110">If at least one user has added a social profile to an organization’s [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution and the acquisition is allowed for private messages of this social profile, private messages of this profile can be acquired.</span><span class="sxs-lookup"><span data-stu-id="a2fca-110">If at least one user has added a social profile to an organization’s [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution and the acquisition is allowed for private messages of this social profile, private messages of this profile can be acquired.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a2fca-111">A user with permissions to work with search topics can create rules that acquire the private messages and similar posts that are found through public searches.</span><span class="sxs-lookup"><span data-stu-id="a2fca-111">A user with permissions to work with search topics can create rules that acquire the private messages and similar posts that are found through public searches.</span></span> <span data-ttu-id="a2fca-112">When a private message is stored in the database, it’s visible to every user who can access [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] in the same organization.</span><span class="sxs-lookup"><span data-stu-id="a2fca-112">When a private message is stored in the database, it’s visible to every user who can access [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] in the same organization.</span></span>  
  
## <a name="data-retention-when-deleting-a-social-profile"></a><span data-ttu-id="a2fca-113">Data retention when deleting a social profile</span><span class="sxs-lookup"><span data-stu-id="a2fca-113">Data retention when deleting a social profile</span></span>  

<span data-ttu-id="a2fca-114">If a solution has acquired private messages from a social profile, and its owner removes the social profile, all private messages from this profile are hidden in the user interface immediately after removal.</span><span class="sxs-lookup"><span data-stu-id="a2fca-114">If a solution has acquired private messages from a social profile, and its owner removes the social profile, all private messages from this profile are hidden in the user interface immediately after removal.</span></span>  
  
<span data-ttu-id="a2fca-115">However, the direct messages persist in the central database unless the solution is de-provisioned or the posts become older than 15 months.</span><span class="sxs-lookup"><span data-stu-id="a2fca-115">However, the direct messages persist in the central database unless the solution is de-provisioned or the posts become older than 15 months.</span></span>  
  
## <a name="data-retention-when-deleting-a-private-message"></a><span data-ttu-id="a2fca-116">Data retention when deleting a private message</span><span class="sxs-lookup"><span data-stu-id="a2fca-116">Data retention when deleting a private message</span></span>  

<span data-ttu-id="a2fca-117">If a solution has acquired private messages from a social profile and the owner of the social profile deletes one of these messages, the deleted message won’t show on the user interface anymore.</span><span class="sxs-lookup"><span data-stu-id="a2fca-117">If a solution has acquired private messages from a social profile and the owner of the social profile deletes one of these messages, the deleted message won’t show on the user interface anymore.</span></span>  
  
## <a name="data-retention-upon-deleting-an-organization-or-de-provisioning-an-organization"></a><span data-ttu-id="a2fca-118">Data retention upon deleting an organization or de-provisioning an organization</span><span class="sxs-lookup"><span data-stu-id="a2fca-118">Data retention upon deleting an organization or de-provisioning an organization</span></span>  

<span data-ttu-id="a2fca-119">If the global administrator decides to de-provision the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution for an organization, all related data such as posts, search topics, direct messages, and user permissions are deleted 180 days after the organization’s subscription is canceled.</span><span class="sxs-lookup"><span data-stu-id="a2fca-119">If the global administrator decides to de-provision the [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution for an organization, all related data such as posts, search topics, direct messages, and user permissions are deleted 180 days after the organization’s subscription is canceled.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a2fca-120">See Also</span><span class="sxs-lookup"><span data-stu-id="a2fca-120">See Also</span></span>  

<span data-ttu-id="a2fca-121">[Manage social profiles](manage-social-profiles.md) </span><span class="sxs-lookup"><span data-stu-id="a2fca-121">[Manage social profiles](manage-social-profiles.md) </span></span>  
<span data-ttu-id="a2fca-122">[Understand user roles](user-roles.md) </span><span class="sxs-lookup"><span data-stu-id="a2fca-122">[Understand user roles](user-roles.md) </span></span>  
[<span data-ttu-id="a2fca-123">Work with posts</span><span class="sxs-lookup"><span data-stu-id="a2fca-123">Work with posts</span></span>](work-with-posts.md)
 
