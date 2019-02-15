---
title: Distribute custom hosted controls using Customization Files with Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how to deploy customization files.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 08/23/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 22e677e6-5d00-43da-9c24-52eacd0a3c70
caps.latest.revision: 13
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 892abe0066543e18244c51ca5977898af30ef6ba
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382400"
---
# <a name="customization-files-and-how-to-distribute-custom-hosted-controls-overview"></a><span data-ttu-id="d02ba-103">Customization Files and how to distribute custom hosted controls overview</span><span class="sxs-lookup"><span data-stu-id="d02ba-103">Customization Files and how to distribute custom hosted controls overview</span></span>
<span data-ttu-id="d02ba-104">Use the customization files feature to distribute custom hosted controls and functionality to agent computers.</span><span class="sxs-lookup"><span data-stu-id="d02ba-104">Use the customization files feature to distribute custom hosted controls and functionality to agent computers.</span></span> <span data-ttu-id="d02ba-105">To control the distribution, create or update a customization file record and associate it with a configuration.</span><span class="sxs-lookup"><span data-stu-id="d02ba-105">To control the distribution, create or update a customization file record and associate it with a configuration.</span></span> <span data-ttu-id="d02ba-106">When agents who are associated with the configuration sign in to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, the custom controls and functionality are downloaded to the agent’s computer and available for use.</span><span class="sxs-lookup"><span data-stu-id="d02ba-106">When agents who are associated with the configuration sign in to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] using the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client, the custom controls and functionality are downloaded to the agent’s computer and available for use.</span></span>  
  
 <span data-ttu-id="d02ba-107">To distribute custom controls and functionality:</span><span class="sxs-lookup"><span data-stu-id="d02ba-107">To distribute custom controls and functionality:</span></span>  
  
1. <span data-ttu-id="d02ba-108">Create or update one or more custom hosted controls and functionality.</span><span class="sxs-lookup"><span data-stu-id="d02ba-108">Create or update one or more custom hosted controls and functionality.</span></span> <span data-ttu-id="d02ba-109">This task is typically completed by a developer who has experience with creating hosted controls and includes the following:</span><span class="sxs-lookup"><span data-stu-id="d02ba-109">This task is typically completed by a developer who has experience with creating hosted controls and includes the following:</span></span>  
  
   - <span data-ttu-id="d02ba-110">The custom hosted controls files.</span><span class="sxs-lookup"><span data-stu-id="d02ba-110">The custom hosted controls files.</span></span> <span data-ttu-id="d02ba-111">Typically, these are assemblies.</span><span class="sxs-lookup"><span data-stu-id="d02ba-111">Typically, these are assemblies.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="d02ba-112">[Create custom Unified Service Desk host control](../../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="d02ba-112">[Create custom Unified Service Desk host control](../../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md)</span></span>  
  
   - <span data-ttu-id="d02ba-113">A [Content_Types].xml file that describes the customization.</span><span class="sxs-lookup"><span data-stu-id="d02ba-113">A [Content_Types].xml file that describes the customization.</span></span> <span data-ttu-id="d02ba-114">This file is an OpenXML file that provides MIME type information by listing the default file extensions for the files that are included in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] customization.</span><span class="sxs-lookup"><span data-stu-id="d02ba-114">This file is an OpenXML file that provides MIME type information by listing the default file extensions for the files that are included in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] customization.</span></span> <span data-ttu-id="d02ba-115">Typically, these are .dll, .xml, .exe, and .config file types, but you can add almost any file type that’s supported by the [!INCLUDE[pn_ms_Windows_short](../../includes/pn-ms-windows-short.md)] PC where the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]client will run.</span><span class="sxs-lookup"><span data-stu-id="d02ba-115">Typically, these are .dll, .xml, .exe, and .config file types, but you can add almost any file type that’s supported by the [!INCLUDE[pn_ms_Windows_short](../../includes/pn-ms-windows-short.md)] PC where the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]client will run.</span></span>  
  
   [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="d02ba-116">[Create custom listeners for auditing, diagnostics, and traces](../../unified-service-desk/create-custom-listeners-auditing-diagnostics-traces.md)</span><span class="sxs-lookup"><span data-stu-id="d02ba-116">[Create custom listeners for auditing, diagnostics, and traces](../../unified-service-desk/create-custom-listeners-auditing-diagnostics-traces.md)</span></span>  
  
2. <span data-ttu-id="d02ba-117">Package the custom control files that you want to distribute as a compressed zip folder.</span><span class="sxs-lookup"><span data-stu-id="d02ba-117">Package the custom control files that you want to distribute as a compressed zip folder.</span></span> <span data-ttu-id="d02ba-118">To do this, in Windows File Explorer select the files, right-click and point to **Send to**, and then click **Compressed (zipped) folder**.</span><span class="sxs-lookup"><span data-stu-id="d02ba-118">To do this, in Windows File Explorer select the files, right-click and point to **Send to**, and then click **Compressed (zipped) folder**.</span></span>  
  
3. <span data-ttu-id="d02ba-119">Create a customization file record and add the compressed (.zip) folder as the attachment.</span><span class="sxs-lookup"><span data-stu-id="d02ba-119">Create a customization file record and add the compressed (.zip) folder as the attachment.</span></span>  
  
4. <span data-ttu-id="d02ba-120">Associate the Customization File record with a Configuration.</span><span class="sxs-lookup"><span data-stu-id="d02ba-120">Associate the Customization File record with a Configuration.</span></span>  
  
## <a name="create-or-update-a-customization-file-record-for-custom-functionality-distribution"></a><span data-ttu-id="d02ba-121">Create or update a customization file record for custom functionality distribution</span><span class="sxs-lookup"><span data-stu-id="d02ba-121">Create or update a customization file record for custom functionality distribution</span></span>  
  
1. <span data-ttu-id="d02ba-122">Go to **Settings** > **Unified Service Desk** > **Customization Files**.</span><span class="sxs-lookup"><span data-stu-id="d02ba-122">Go to **Settings** > **Unified Service Desk** > **Customization Files**.</span></span>  
  
2. <span data-ttu-id="d02ba-123">Select an existing customization file record in the list or click **New** to create a new one.</span><span class="sxs-lookup"><span data-stu-id="d02ba-123">Select an existing customization file record in the list or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="d02ba-124">In the **Name** box, type a name for the record.</span><span class="sxs-lookup"><span data-stu-id="d02ba-124">In the **Name** box, type a name for the record.</span></span>  
  
    <span data-ttu-id="d02ba-125">In the **Customization Version** box, enter a software version number that corresponds to the version of the zipped folder containing the customization files.</span><span class="sxs-lookup"><span data-stu-id="d02ba-125">In the **Customization Version** box, enter a software version number that corresponds to the version of the zipped folder containing the customization files.</span></span> <span data-ttu-id="d02ba-126">For example, if this is the original version of the customization, you can enter 1.0.</span><span class="sxs-lookup"><span data-stu-id="d02ba-126">For example, if this is the original version of the customization, you can enter 1.0.</span></span> <span data-ttu-id="d02ba-127">If it is a minor update, you can enter 1.1.</span><span class="sxs-lookup"><span data-stu-id="d02ba-127">If it is a minor update, you can enter 1.1.</span></span>  
  
    <span data-ttu-id="d02ba-128">Optionally, add a description in the **Description** box.</span><span class="sxs-lookup"><span data-stu-id="d02ba-128">Optionally, add a description in the **Description** box.</span></span>  
  
4. <span data-ttu-id="d02ba-129">If this is a new customization file record, click **Save** to save the record so you can attach customization compressed (.zip) folder.</span><span class="sxs-lookup"><span data-stu-id="d02ba-129">If this is a new customization file record, click **Save** to save the record so you can attach customization compressed (.zip) folder.</span></span> <span data-ttu-id="d02ba-130">Next, click **Attach**, and browse to the location of the compressed folder that contains the custom control and functionality files and the [Content_Types].xml file.</span><span class="sxs-lookup"><span data-stu-id="d02ba-130">Next, click **Attach**, and browse to the location of the compressed folder that contains the custom control and functionality files and the [Content_Types].xml file.</span></span>  
  
    <span data-ttu-id="d02ba-131">To update an existing customization file record with a new customization compressed (.zip) folder, remove the existing zipped folder by clicking **X** next to the folder.</span><span class="sxs-lookup"><span data-stu-id="d02ba-131">To update an existing customization file record with a new customization compressed (.zip) folder, remove the existing zipped folder by clicking **X** next to the folder.</span></span> <span data-ttu-id="d02ba-132">Then, click **Attach**, and browse to the location of the compressed folder that contains the updated custom control and functionality files.</span><span class="sxs-lookup"><span data-stu-id="d02ba-132">Then, click **Attach**, and browse to the location of the compressed folder that contains the updated custom control and functionality files.</span></span>  
  
5. <span data-ttu-id="d02ba-133">Bấm vào **Xong** .</span><span class="sxs-lookup"><span data-stu-id="d02ba-133">Click **Done**.</span></span>  
  
6. <span data-ttu-id="d02ba-134">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d02ba-134">Click **Save**.</span></span>  
  
7. <span data-ttu-id="d02ba-135">If the customization file record isn’t already associated with a Configuration, you must do so before the customization can be used by agents.</span><span class="sxs-lookup"><span data-stu-id="d02ba-135">If the customization file record isn’t already associated with a Configuration, you must do so before the customization can be used by agents.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="d02ba-136">[Manage access using Unified Service Desk configuration](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="d02ba-136">[Manage access using Unified Service Desk configuration](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d02ba-137">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d02ba-137">See also</span></span>  
 <span data-ttu-id="d02ba-138">[Quản trị và quản lý Unified Service Desk](../../unified-service-desk/admin/administer-manage-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="d02ba-138">[Administer and manage Unified Service Desk](../../unified-service-desk/admin/administer-manage-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="d02ba-139">Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server</span><span class="sxs-lookup"><span data-stu-id="d02ba-139">Migrate your Unified Service Desk configuration to another Dynamics 365 for Customer Engagement server</span></span>](../../unified-service-desk/admin/migrate-unified-service-desk-configuration-dynamics-365-server.md)
