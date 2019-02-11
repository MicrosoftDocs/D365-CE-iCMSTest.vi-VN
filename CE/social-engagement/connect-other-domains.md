---
title: Allow requests from other domains with Social Engagement | Microsoft Docs
description: Learn how to add URLs to the list of allowed domains so they can request data from Social Engagement.
ms.custom:
- dyn365-socialengagement
ms.date: 09/12/2017
ms.reviewer: ''
ms.service: dynamics-365-marketing
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to: Social Engagement
ms.assetid: dbde8454-c0e6-4914-9818-6eee4c6aeb0f
caps.latest.revision: 27
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
ms.openlocfilehash: a58b60f0591fa595c6b10398a2f263593240cc68
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "375411"
---
# <a name="connect-includepnnetbreezeshortincludespn-social-engagement-shortmd-to-other-domains"></a><span data-ttu-id="73b0e-103">Connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to other domains</span><span class="sxs-lookup"><span data-stu-id="73b0e-103">Connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to other domains</span></span>

<span data-ttu-id="73b0e-104">Enable communication between [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] and other compatible applications (such as [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]) by adding domains that are allowed to make requests for your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] data to a list.</span><span class="sxs-lookup"><span data-stu-id="73b0e-104">Enable communication between [!INCLUDE[pn_netbreeze_long](../includes/pn-social-engagement-long.md)] and other compatible applications (such as [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]) by adding domains that are allowed to make requests for your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] data to a list.</span></span> <span data-ttu-id="73b0e-105">You can remove domains from the list to disallow communications.</span><span class="sxs-lookup"><span data-stu-id="73b0e-105">You can remove domains from the list to disallow communications.</span></span>

<span data-ttu-id="73b0e-106">To add or remove domains, or to connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to another application, you must be a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] Administrator.</span><span class="sxs-lookup"><span data-stu-id="73b0e-106">To add or remove domains, or to connect [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to another application, you must be a [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] Administrator.</span></span>

<span data-ttu-id="73b0e-107">You can enter the following values in your list of allowed domains:</span><span class="sxs-lookup"><span data-stu-id="73b0e-107">You can enter the following values in your list of allowed domains:</span></span>  
  
- <span data-ttu-id="73b0e-108">Full domain names: This enables communication between the specified domain and your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution, for example, `app.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="73b0e-108">Full domain names: This enables communication between the specified domain and your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution, for example, `app.contoso.com`</span></span>  
  
- <span data-ttu-id="73b0e-109">Domain names with wildcards: This enables communication between all subdomains of the entered domain and your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution, for example, `*.contoso.com`</span><span class="sxs-lookup"><span data-stu-id="73b0e-109">Domain names with wildcards: This enables communication between all subdomains of the entered domain and your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution, for example, `*.contoso.com`</span></span>  
  
- <span data-ttu-id="73b0e-110">Host names: This enables communication between a custom host name and your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution, for example, `http://hostname`</span><span class="sxs-lookup"><span data-stu-id="73b0e-110">Host names: This enables communication between a custom host name and your [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] solution, for example, `http://hostname`</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="73b0e-111">Make sure to remove trailing slashes from the domain name.</span><span class="sxs-lookup"><span data-stu-id="73b0e-111">Make sure to remove trailing slashes from the domain name.</span></span>

## <a name="add-a-domain"></a><span data-ttu-id="73b0e-112">Add a domain</span><span class="sxs-lookup"><span data-stu-id="73b0e-112">Add a domain</span></span>
  
1.  <span data-ttu-id="73b0e-113">Go to **Settings** > **Connections** > **Allowed Domains**.</span><span class="sxs-lookup"><span data-stu-id="73b0e-113">Go to **Settings** > **Connections** > **Allowed Domains**.</span></span>  
  
2.  <span data-ttu-id="73b0e-114">Type the domain name in the input field, and then click the **Add** button ![New or Add button](media/plus-icon.png "New or Add button").</span><span class="sxs-lookup"><span data-stu-id="73b0e-114">Type the domain name in the input field, and then click the **Add** button ![New or Add button](media/plus-icon.png "New or Add button").</span></span>  
  
## <a name="remove-a-domain"></a><span data-ttu-id="73b0e-115">Remove a domain</span><span class="sxs-lookup"><span data-stu-id="73b0e-115">Remove a domain</span></span>  
  
1.  <span data-ttu-id="73b0e-116">Go to **Settings** > **Connections** >**Allowed Domains**.</span><span class="sxs-lookup"><span data-stu-id="73b0e-116">Go to **Settings** > **Connections** >**Allowed Domains**.</span></span>  
  
2.  <span data-ttu-id="73b0e-117">Locate the domain you want to remove, click the **Delete** button ![Delete button](media/delete-icon.png "Delete button"), and then confirm the deletion.</span><span class="sxs-lookup"><span data-stu-id="73b0e-117">Locate the domain you want to remove, click the **Delete** button ![Delete button](media/delete-icon.png "Delete button"), and then confirm the deletion.</span></span>  
  
## <a name="add-the-solution-url-to-the-configuration-page"></a><span data-ttu-id="73b0e-118">Add the solution URL to the configuration page</span><span class="sxs-lookup"><span data-stu-id="73b0e-118">Add the solution URL to the configuration page</span></span>

<span data-ttu-id="73b0e-119">In the **Solution URL** pane of the **Allowed Domains** page, you’ll find the **URL** to connect to this instance of [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="73b0e-119">In the **Solution URL** pane of the **Allowed Domains** page, you’ll find the **URL** to connect to this instance of [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>  
  
<span data-ttu-id="73b0e-120">Copy the solution URL and paste it into the configuration page of the application that you want to connect to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span><span class="sxs-lookup"><span data-stu-id="73b0e-120">Copy the solution URL and paste it into the configuration page of the application that you want to connect to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)].</span></span>  
  
> [!NOTE]
> <span data-ttu-id="73b0e-121">Make sure to add the domain or host name of the application you plan to connect to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to your list of allowed domains.</span><span class="sxs-lookup"><span data-stu-id="73b0e-121">Make sure to add the domain or host name of the application you plan to connect to [!INCLUDE[pn_netbreeze_short](../includes/pn-social-engagement-short.md)] to your list of allowed domains.</span></span>  
> 
>  <span data-ttu-id="73b0e-122">To make sure only the domains you own can make requests to your data, we recommend you add your organization’s domain to the list of allowed domains.</span><span class="sxs-lookup"><span data-stu-id="73b0e-122">To make sure only the domains you own can make requests to your data, we recommend you add your organization’s domain to the list of allowed domains.</span></span> <span data-ttu-id="73b0e-123">When a specific domain is added to the list of allowed domains, \*.dynamics.com is automatically removed from the allowed domains.</span><span class="sxs-lookup"><span data-stu-id="73b0e-123">When a specific domain is added to the list of allowed domains, \*.dynamics.com is automatically removed from the allowed domains.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="73b0e-124">See Also</span><span class="sxs-lookup"><span data-stu-id="73b0e-124">See Also</span></span>

<span data-ttu-id="73b0e-125">[Administer Microsoft Social Engagement](administer-microsoft-social-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="73b0e-125">[Administer Microsoft Social Engagement](administer-microsoft-social-engagement.md) </span></span>  
<span data-ttu-id="73b0e-126">[Get started with Social Engagement](get-started.md) </span><span class="sxs-lookup"><span data-stu-id="73b0e-126">[Get started with Social Engagement](get-started.md) </span></span>  
[<span data-ttu-id="73b0e-127">Get connected to the social conversation</span><span class="sxs-lookup"><span data-stu-id="73b0e-127">Get connected to the social conversation</span></span>](get-connected-social-conversation.md)
 
