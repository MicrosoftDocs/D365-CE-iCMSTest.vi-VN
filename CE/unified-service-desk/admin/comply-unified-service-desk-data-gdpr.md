---
title: Unified Service Desk data compliance under GDPR (Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about data in Unified Service Desk that comes under General Data Protection Regulation (GDPR)
ms.custom: ''
ms.date: 04/24/2018
ms.reviewer: ''
ms.service: usd
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement (on-premises)
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: FA8D5702-C698-42B0-89BF-CD444BF3FB73
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 9656a2edade9bd989f02a4f2a752dd9c8fc53e77
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382380"
---
# <a name="includepnunifiedservicedeskincludespn-unified-service-deskmd-data-compliance-under-gdpr"></a>[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="518dc-103">data compliance under GDPR</span><span class="sxs-lookup"><span data-stu-id="518dc-103">data compliance under GDPR</span></span>

<span data-ttu-id="518dc-104">Data definitions and stages are outlined in the GDPR.</span><span class="sxs-lookup"><span data-stu-id="518dc-104">Data definitions and stages are outlined in the GDPR.</span></span> <span data-ttu-id="518dc-105">Let's look at the following data contained in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and see how they relate to those outlined in the GDPR:</span><span class="sxs-lookup"><span data-stu-id="518dc-105">Let's look at the following data contained in [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and see how they relate to those outlined in the GDPR:</span></span>

- <span data-ttu-id="518dc-106">Audit log files</span><span class="sxs-lookup"><span data-stu-id="518dc-106">Audit log files</span></span>
- <span data-ttu-id="518dc-107">Diagnostic log files</span><span class="sxs-lookup"><span data-stu-id="518dc-107">Diagnostic log files</span></span>
- <span data-ttu-id="518dc-108">Telemetry data</span><span class="sxs-lookup"><span data-stu-id="518dc-108">Telemetry data</span></span>

## <a name="audit-log-files"></a><span data-ttu-id="518dc-109">Audit log files</span><span class="sxs-lookup"><span data-stu-id="518dc-109">Audit log files</span></span>

### <a name="standard-auditing-by-using-an-audit--diagnostic-record"></a><span data-ttu-id="518dc-110">Standard auditing by using an Audit & Diagnostic record</span><span class="sxs-lookup"><span data-stu-id="518dc-110">Standard auditing by using an Audit & Diagnostic record</span></span>

<span data-ttu-id="518dc-111">If you configure standard or custom auditing using an Audit & Diagnostics record, you can write a custom listener to send the log to files.</span><span class="sxs-lookup"><span data-stu-id="518dc-111">If you configure standard or custom auditing using an Audit & Diagnostics record, you can write a custom listener to send the log to files.</span></span> <span data-ttu-id="518dc-112">The audit data log files are present in your local computer, or you can configure a path to store the file in your local computer or another computer in the network.</span><span class="sxs-lookup"><span data-stu-id="518dc-112">The audit data log files are present in your local computer, or you can configure a path to store the file in your local computer or another computer in the network.</span></span> 

<span data-ttu-id="518dc-113">Using a custom listener, you can send the log output to files, the event log, or other sources.</span><span class="sxs-lookup"><span data-stu-id="518dc-113">Using a custom listener, you can send the log output to files, the event log, or other sources.</span></span>

<span data-ttu-id="518dc-114">To delete audit logging that you configure using an Audit & Diagnostic record by writing a standard or custom listener:</span><span class="sxs-lookup"><span data-stu-id="518dc-114">To delete audit logging that you configure using an Audit & Diagnostic record by writing a standard or custom listener:</span></span>

1. <span data-ttu-id="518dc-115">Navigate to the location where you store the audit data log files.</span><span class="sxs-lookup"><span data-stu-id="518dc-115">Navigate to the location where you store the audit data log files.</span></span>
2. <span data-ttu-id="518dc-116">Select the files that you want to delete, and then press **Delete**.</span><span class="sxs-lookup"><span data-stu-id="518dc-116">Select the files that you want to delete, and then press **Delete**.</span></span>

### <a name="standard-auditing-by-adding-an-audit-flag"></a><span data-ttu-id="518dc-117">Standard auditing by adding an audit flag</span><span class="sxs-lookup"><span data-stu-id="518dc-117">Standard auditing by adding an audit flag</span></span>

<span data-ttu-id="518dc-118">If you configure audit logging using the standard auditing by adding an audit flag, the events and logs are present in the **UII_auditBase** table in the organization database.</span><span class="sxs-lookup"><span data-stu-id="518dc-118">If you configure audit logging using the standard auditing by adding an audit flag, the events and logs are present in the **UII_auditBase** table in the organization database.</span></span>

<span data-ttu-id="518dc-119">To delete audit logging that you configure using standard auditing by adding an audit flag:</span><span class="sxs-lookup"><span data-stu-id="518dc-119">To delete audit logging that you configure using standard auditing by adding an audit flag:</span></span>

1. <span data-ttu-id="518dc-120">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="518dc-120">Sign in to [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>
2. <span data-ttu-id="518dc-121">From a productivity area, select **Advanced Find**.</span><span class="sxs-lookup"><span data-stu-id="518dc-121">From a productivity area, select **Advanced Find**.</span></span></br>
   <span data-ttu-id="518dc-122">![Click Advanced Find](../../unified-service-desk/media/advance-find-usd-gdpr-crm-server.PNG "Click Advanced Find")</span><span class="sxs-lookup"><span data-stu-id="518dc-122">![Click Advanced Find](../../unified-service-desk/media/advance-find-usd-gdpr-crm-server.PNG "Click Advanced Find")</span></span>
3. <span data-ttu-id="518dc-123">In the **Look for** list, select **UII Audit**.</span><span class="sxs-lookup"><span data-stu-id="518dc-123">In the **Look for** list, select **UII Audit**.</span></span></br>
   <span data-ttu-id="518dc-124">![Click UII Audit option](../../unified-service-desk/media/look-usd-gdpr-crm-server.PNG "Click UII Audit option")</span><span class="sxs-lookup"><span data-stu-id="518dc-124">![Click UII Audit option](../../unified-service-desk/media/look-usd-gdpr-crm-server.PNG "Click UII Audit option")</span></span>
4. <span data-ttu-id="518dc-125">To see all audit logging details, select **Results**.</span><span class="sxs-lookup"><span data-stu-id="518dc-125">To see all audit logging details, select **Results**.</span></span></br>
   <span data-ttu-id="518dc-126">![Click on Results option](../../unified-service-desk/media/results-usd-gdpr-crm-server.PNG "Click on Results option")</span><span class="sxs-lookup"><span data-stu-id="518dc-126">![Click on Results option](../../unified-service-desk/media/results-usd-gdpr-crm-server.PNG "Click on Results option")</span></span>
5. <span data-ttu-id="518dc-127">Select the records that you want to delete.</span><span class="sxs-lookup"><span data-stu-id="518dc-127">Select the records that you want to delete.</span></span></br>
   <span data-ttu-id="518dc-128">![Select records to delete](../../unified-service-desk/media/select-records-usd-gdpr-crm-server.PNG "Select records to delete")</span><span class="sxs-lookup"><span data-stu-id="518dc-128">![Select records to delete](../../unified-service-desk/media/select-records-usd-gdpr-crm-server.PNG "Select records to delete")</span></span>
6. <span data-ttu-id="518dc-129">To delete the records, select **Delete UII Audit**.</span><span class="sxs-lookup"><span data-stu-id="518dc-129">To delete the records, select **Delete UII Audit**.</span></span></br>
   <span data-ttu-id="518dc-130">![Click Delete UII Audit option](../../unified-service-desk/media/delete-records-uii-audit-usd-gdpr-crm-server.PNG "Click Delete UII Audit option")</span><span class="sxs-lookup"><span data-stu-id="518dc-130">![Click Delete UII Audit option](../../unified-service-desk/media/delete-records-uii-audit-usd-gdpr-crm-server.PNG "Click Delete UII Audit option")</span></span>

## <a name="diagnostic-log-files"></a><span data-ttu-id="518dc-131">Diagnostic log files</span><span class="sxs-lookup"><span data-stu-id="518dc-131">Diagnostic log files</span></span>

<span data-ttu-id="518dc-132">The diagnostic logging records operational events and errors in the client application.</span><span class="sxs-lookup"><span data-stu-id="518dc-132">The diagnostic logging records operational events and errors in the client application.</span></span> <span data-ttu-id="518dc-133">UTF-8 encoded text files that are named UnifiedServiceDesk-<date>.log are maintained at the following location on the client computer:</span><span class="sxs-lookup"><span data-stu-id="518dc-133">UTF-8 encoded text files that are named UnifiedServiceDesk-<date>.log are maintained at the following location on the client computer:</span></span>

`c:\Users\<UserName>\AppData\Roaming\Microsoft\Microsoft Dynamics 365 for Customer Engagement Unified Service Desk\<Version>`

<span data-ttu-id="518dc-134">To delete diagnostic logging:</span><span class="sxs-lookup"><span data-stu-id="518dc-134">To delete diagnostic logging:</span></span>

1. <span data-ttu-id="518dc-135">Go to the default or configured folder path where you store the diagnostic log files.</span><span class="sxs-lookup"><span data-stu-id="518dc-135">Go to the default or configured folder path where you store the diagnostic log files.</span></span>
<span data-ttu-id="518dc-136">The default folder path is:</span><span class="sxs-lookup"><span data-stu-id="518dc-136">The default folder path is:</span></span> </br>
`c:\Users\<UserName>\AppData\Roaming\Microsoft\Microsoft Dynamics 365 for Customer Engagement Unified Service Desk\<Version>`
2. <span data-ttu-id="518dc-137">Select the **UnifiedServiceDesk-<date>.log** file, and then select **Delete**.</span><span class="sxs-lookup"><span data-stu-id="518dc-137">Select the **UnifiedServiceDesk-<date>.log** file, and then select **Delete**.</span></span>

## <a name="telemetry-data"></a><span data-ttu-id="518dc-138">Telemetry data</span><span class="sxs-lookup"><span data-stu-id="518dc-138">Telemetry data</span></span>

[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="518dc-139">client application collects telemetry data ([!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] application-specific information) that is maintained in Microsoft Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="518dc-139">client application collects telemetry data ([!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] application-specific information) that is maintained in Microsoft Dynamics 365 for Customer Engagement apps.</span></span> <span data-ttu-id="518dc-140">In these cases, the natural or legal person, public authority, agency, or other body which, alone or jointly with others, becomes the controller, and the processor is Microsoft, which processes the data on behalf of the controller.</span><span class="sxs-lookup"><span data-stu-id="518dc-140">In these cases, the natural or legal person, public authority, agency, or other body which, alone or jointly with others, becomes the controller, and the processor is Microsoft, which processes the data on behalf of the controller.</span></span>

<span data-ttu-id="518dc-141">The category of telemetry that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] collects are:</span><span class="sxs-lookup"><span data-stu-id="518dc-141">The category of telemetry that [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] collects are:</span></span>

- <span data-ttu-id="518dc-142">Action call results data</span><span class="sxs-lookup"><span data-stu-id="518dc-142">Action call results data</span></span>
- <span data-ttu-id="518dc-143">Start-up performance data</span><span class="sxs-lookup"><span data-stu-id="518dc-143">Start-up performance data</span></span>
- <span data-ttu-id="518dc-144">Error and exit data</span><span class="sxs-lookup"><span data-stu-id="518dc-144">Error and exit data</span></span>
- <span data-ttu-id="518dc-145">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="518dc-145">Feedback</span></span>
- <span data-ttu-id="518dc-146">Freeze or performance data</span><span class="sxs-lookup"><span data-stu-id="518dc-146">Freeze or performance data</span></span>
- <span data-ttu-id="518dc-147">Session start and end data</span><span class="sxs-lookup"><span data-stu-id="518dc-147">Session start and end data</span></span>

[!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="518dc-148">[Microsoft Dynamics 365 for Customer Engagement apps and GDPR](https://docs.microsoft.com/en-us/dynamics365/get-started/gdpr/index)</span><span class="sxs-lookup"><span data-stu-id="518dc-148">[Microsoft Dynamics 365 for Customer Engagement apps and GDPR](https://docs.microsoft.com/en-us/dynamics365/get-started/gdpr/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="518dc-149">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="518dc-149">See also</span></span>

[<span data-ttu-id="518dc-150">Comply with General Data Protection Regulation (GDPR)</span><span class="sxs-lookup"><span data-stu-id="518dc-150">Comply with General Data Protection Regulation (GDPR)</span></span>](comply-gdpr.md)
