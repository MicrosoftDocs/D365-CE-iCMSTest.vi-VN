---
title: 'Walkthrough: Configure assembly security for an offline plug-in  (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The topic provides a walkthrough on configuring assembly security for an offline plug-in.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: bb9ff0b6-ef76-473e-a24b-2921c8acec23
caps.latest.revision: 12
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 079b09494eac4b7fefd0a0d8e3a1290331f62568
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388690"
---
# <a name="walkthrough-configure-assembly-security-for-an-offline-plug-in"></a><span data-ttu-id="7da05-103">Walkthrough: Configure assembly security for an offline plug-in</span><span class="sxs-lookup"><span data-stu-id="7da05-103">Walkthrough: Configure assembly security for an offline plug-in</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7da05-104">The [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement platform applies an additional security restriction to registered offline plug-in assemblies.</span><span class="sxs-lookup"><span data-stu-id="7da05-104">The [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement platform applies an additional security restriction to registered offline plug-in assemblies.</span></span> <span data-ttu-id="7da05-105">When [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)] is installed, an AllowList key is added to the system registry on the client computer.</span><span class="sxs-lookup"><span data-stu-id="7da05-105">When [!INCLUDE[pn_crm_outlook_offline_access](../includes/pn-crm-outlook-offline-access.md)] is installed, an AllowList key is added to the system registry on the client computer.</span></span> <span data-ttu-id="7da05-106">For each assembly containing an offline plug-in that you register, you must add a registry sub-key under the AllowList key with the key name derived from the assembly's public key token.</span><span class="sxs-lookup"><span data-stu-id="7da05-106">For each assembly containing an offline plug-in that you register, you must add a registry sub-key under the AllowList key with the key name derived from the assembly's public key token.</span></span> <span data-ttu-id="7da05-107">Failure to add this key results in the offline plug-in not being executed by the platform even though the plug-in is registered.</span><span class="sxs-lookup"><span data-stu-id="7da05-107">Failure to add this key results in the offline plug-in not being executed by the platform even though the plug-in is registered.</span></span> <span data-ttu-id="7da05-108">This walkthrough describes how to add this sub-key for a plug-in assembly.</span><span class="sxs-lookup"><span data-stu-id="7da05-108">This walkthrough describes how to add this sub-key for a plug-in assembly.</span></span>  
  
### <a name="get-the-public-key-token"></a><span data-ttu-id="7da05-109">Get the public key token</span><span class="sxs-lookup"><span data-stu-id="7da05-109">Get the public key token</span></span>  
  
1.  <span data-ttu-id="7da05-110">Load the assembly containing the offline plug-in into the Plug-in Registration tool.</span><span class="sxs-lookup"><span data-stu-id="7da05-110">Load the assembly containing the offline plug-in into the Plug-in Registration tool.</span></span> <span data-ttu-id="7da05-111">For more information about how to use the tool, see [Walkthrough: Register a Plug-in using the Plug-in Registration Tool](walkthrough-register-plugin-using-plugin-registration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="7da05-111">For more information about how to use the tool, see [Walkthrough: Register a Plug-in using the Plug-in Registration Tool](walkthrough-register-plugin-using-plugin-registration-tool.md).</span></span>  
  
2.  <span data-ttu-id="7da05-112">Select the plug-in assembly in the tree view of the tool.</span><span class="sxs-lookup"><span data-stu-id="7da05-112">Select the plug-in assembly in the tree view of the tool.</span></span>  
  
3.  <span data-ttu-id="7da05-113">Copy (Ctrl+C) the value in the **Public Key Token** field into the paste buffer.</span><span class="sxs-lookup"><span data-stu-id="7da05-113">Copy (Ctrl+C) the value in the **Public Key Token** field into the paste buffer.</span></span>  
  
### <a name="add-an-allowlist-key"></a><span data-ttu-id="7da05-114">Add an AllowList key</span><span class="sxs-lookup"><span data-stu-id="7da05-114">Add an AllowList key</span></span>  
  
1.  <span data-ttu-id="7da05-115">Run the registry editor by selecting **Start**, then select **Run** and type `regedit.exe`.</span><span class="sxs-lookup"><span data-stu-id="7da05-115">Run the registry editor by selecting **Start**, then select **Run** and type `regedit.exe`.</span></span>  
  
2.  <span data-ttu-id="7da05-116">In the tree view pane, navigate to the **AllowList** key.</span><span class="sxs-lookup"><span data-stu-id="7da05-116">In the tree view pane, navigate to the **AllowList** key.</span></span> <span data-ttu-id="7da05-117">The complete path of the key is `HKEY_CURRENT_USER\Software\Microsoft\MSCRMClient\AllowList`.</span><span class="sxs-lookup"><span data-stu-id="7da05-117">The complete path of the key is `HKEY_CURRENT_USER\Software\Microsoft\MSCRMClient\AllowList`.</span></span>  
  
3.  <span data-ttu-id="7da05-118">Select the **AllowList** key and right click to display the context menu.</span><span class="sxs-lookup"><span data-stu-id="7da05-118">Select the **AllowList** key and right click to display the context menu.</span></span>  
  
4.  <span data-ttu-id="7da05-119">Select **New** then click **Key** to create a new sub-key.</span><span class="sxs-lookup"><span data-stu-id="7da05-119">Select **New** then click **Key** to create a new sub-key.</span></span>  
  
5.  <span data-ttu-id="7da05-120">Paste the public key token value into the name of the new sub-key.</span><span class="sxs-lookup"><span data-stu-id="7da05-120">Paste the public key token value into the name of the new sub-key.</span></span>  
  
6.  <span data-ttu-id="7da05-121">Close the registry editor.</span><span class="sxs-lookup"><span data-stu-id="7da05-121">Close the registry editor.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7da05-122">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7da05-122">See also</span></span>  
 <span data-ttu-id="7da05-123">[Plug-in Development](plugin-development.md) </span><span class="sxs-lookup"><span data-stu-id="7da05-123">[Plug-in Development](plugin-development.md) </span></span>  
 <span data-ttu-id="7da05-124">[Sample: Basic Plug-in](sample-create-basic-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="7da05-124">[Sample: Basic Plug-in](sample-create-basic-plugin.md) </span></span>  
 [<span data-ttu-id="7da05-125">Register and Deploy Plug-ins</span><span class="sxs-lookup"><span data-stu-id="7da05-125">Register and Deploy Plug-ins</span></span>](register-deploy-plugins.md)
