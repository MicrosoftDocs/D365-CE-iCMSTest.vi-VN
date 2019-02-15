---
title: Extend Connected Field Service solutions (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Connected Field Service supports the customization of each standard component or service and the easy addition of custom Azure-based components and services.
ms.custom:
- dyn365-developer
- dyn365-fieldservice
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.technology:
- field-service
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d29a9353-73cf-4b49-b74f-d9050dc96bd7
caps.latest.revision: 7
author: JimDaly
ms.author: jdaly
manager: jdaly
search.audienceType:
- developer
search.app:
- D365CE
- D365FS
ms.openlocfilehash: c58564568d7e5a4a4940af164f1789307ad49605
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387344"
---
# <a name="extend-connected-field-service-solutions"></a><span data-ttu-id="89e00-103">Mở rộng các giải pháp Connected Field Service</span><span class="sxs-lookup"><span data-stu-id="89e00-103">Extend Connected Field Service solutions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_connected_field_service_msdyn365](../../includes/pn-connected-field-service-msdyn365.md)] <span data-ttu-id="89e00-104">supports the customization of each standard component or service and the easy addition of custom Azure-based components and services.</span><span class="sxs-lookup"><span data-stu-id="89e00-104">supports the customization of each standard component or service and the easy addition of custom Azure-based components and services.</span></span> <span data-ttu-id="89e00-105">This flexible architecture is required to support the wide range of current and future IoT devices and the envisioned supporting services for these devices.</span><span class="sxs-lookup"><span data-stu-id="89e00-105">This flexible architecture is required to support the wide range of current and future IoT devices and the envisioned supporting services for these devices.</span></span>  
  
## <a name="extend-azure-services"></a><span data-ttu-id="89e00-106">Extend Azure Services</span><span class="sxs-lookup"><span data-stu-id="89e00-106">Extend Azure Services</span></span>

 <span data-ttu-id="89e00-107">The Azure services and components, including the ones detailed in [Connected Field Service architecture](connected-field-service-architecture.md), are designed for reliability, scalability, and extensibility.</span><span class="sxs-lookup"><span data-stu-id="89e00-107">The Azure services and components, including the ones detailed in [Connected Field Service architecture](connected-field-service-architecture.md), are designed for reliability, scalability, and extensibility.</span></span>  <span data-ttu-id="89e00-108">They support management and customization through UI-based and PowerShell administration, JSON-based template-driven deployment and initialization, and REST-based programming interfaces (often including client libraries for specific languages, such as C#/.NET, Python, Java, and Node.js).</span><span class="sxs-lookup"><span data-stu-id="89e00-108">They support management and customization through UI-based and PowerShell administration, JSON-based template-driven deployment and initialization, and REST-based programming interfaces (often including client libraries for specific languages, such as C#/.NET, Python, Java, and Node.js).</span></span>  
  
 <span data-ttu-id="89e00-109">After the standard installation, Connected Field Services will configure your resource group with a set of Azure services similar to the following.</span><span class="sxs-lookup"><span data-stu-id="89e00-109">After the standard installation, Connected Field Services will configure your resource group with a set of Azure services similar to the following.</span></span>  
  
 <span data-ttu-id="89e00-110">![Connected Field Service Standard Azure Services](../media/iot-standard-azure-service.jpg "Connected Field Service Standard Azure Services")</span><span class="sxs-lookup"><span data-stu-id="89e00-110">![Connected Field Service Standard Azure Services](../media/iot-standard-azure-service.jpg "Connected Field Service Standard Azure Services")</span></span>  
  
 <span data-ttu-id="89e00-111">Although extending these Azure services (or adding additional ones) is beyond the scope of this topic, there are ample resources available to the developer, including the following from Microsoft:</span><span class="sxs-lookup"><span data-stu-id="89e00-111">Although extending these Azure services (or adding additional ones) is beyond the scope of this topic, there are ample resources available to the developer, including the following from Microsoft:</span></span>  
  
-   <span data-ttu-id="89e00-112">The [Microsoft Azure](https://azure.microsoft.com/) site for product descriptions, pricing and trial offers, documentation, downloads, blogs, and related resources, including the [Azure Documentation Center](https://azure.microsoft.com/documentation/) for developers and administrators.</span><span class="sxs-lookup"><span data-stu-id="89e00-112">The [Microsoft Azure](https://azure.microsoft.com/) site for product descriptions, pricing and trial offers, documentation, downloads, blogs, and related resources, including the [Azure Documentation Center](https://azure.microsoft.com/documentation/) for developers and administrators.</span></span> <span data-ttu-id="89e00-113">Most developers will want to download one or more [Azure SDKs](https://azure.microsoft.com/en-us/downloads/) and tools such as the [Azure Storage Explorer](http://storageexplorer.com/) and the [Azure Device Explorer](https://github.com/Azure/azure-iot-sdks/blob/master/tools/DeviceExplorer/doc/how_to_use_device_explorer.md).</span><span class="sxs-lookup"><span data-stu-id="89e00-113">Most developers will want to download one or more [Azure SDKs](https://azure.microsoft.com/en-us/downloads/) and tools such as the [Azure Storage Explorer](http://storageexplorer.com/) and the [Azure Device Explorer](https://github.com/Azure/azure-iot-sdks/blob/master/tools/DeviceExplorer/doc/how_to_use_device_explorer.md).</span></span>  
  
-   <span data-ttu-id="89e00-114">[MSDN Azure Technical Documentation Library](https://msdn.microsoft.com/library/azure/dn578280.aspx) for developer-oriented information and downloads</span><span class="sxs-lookup"><span data-stu-id="89e00-114">[MSDN Azure Technical Documentation Library](https://msdn.microsoft.com/library/azure/dn578280.aspx) for developer-oriented information and downloads</span></span>  
  
-   <span data-ttu-id="89e00-115">[MSDN Channel 9](https://channel9.msdn.com/) for a wide selection of current and ever-growing [Azure videos and posts](https://channel9.msdn.com/tags/Azure/)</span><span class="sxs-lookup"><span data-stu-id="89e00-115">[MSDN Channel 9](https://channel9.msdn.com/) for a wide selection of current and ever-growing [Azure videos and posts](https://channel9.msdn.com/tags/Azure/)</span></span>  
  
-   <span data-ttu-id="89e00-116">Books from [Microsoft Press](https://www.microsoftpressstore.com/) (including [free eBooks](https://mva.microsoft.com/ebooks/)) and supplemental training through [Microsoft Virtual Academy](https://mva.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="89e00-116">Books from [Microsoft Press](https://www.microsoftpressstore.com/) (including [free eBooks](https://mva.microsoft.com/ebooks/)) and supplemental training through [Microsoft Virtual Academy](https://mva.microsoft.com/)</span></span>  
  
## <a name="extend-connected-field-service"></a><span data-ttu-id="89e00-117">Extend Connected Field Service</span><span class="sxs-lookup"><span data-stu-id="89e00-117">Extend Connected Field Service</span></span>  
 <span data-ttu-id="89e00-118">The following table lists the custom entities and processes that Connected Field Service supplies to interface with the associated Azure services and components.</span><span class="sxs-lookup"><span data-stu-id="89e00-118">The following table lists the custom entities and processes that Connected Field Service supplies to interface with the associated Azure services and components.</span></span> <span data-ttu-id="89e00-119">These types are more fully described in <xref:Microsoft.Dynamics.CRM.IoTConnector>.</span><span class="sxs-lookup"><span data-stu-id="89e00-119">These types are more fully described in <xref:Microsoft.Dynamics.CRM.IoTConnector>.</span></span>
  
|<span data-ttu-id="89e00-120">Display Name (ID)</span><span class="sxs-lookup"><span data-stu-id="89e00-120">Display Name (ID)</span></span>|<span data-ttu-id="89e00-121">Loại</span><span class="sxs-lookup"><span data-stu-id="89e00-121">Type</span></span>|<span data-ttu-id="89e00-122">Mô tả</span><span class="sxs-lookup"><span data-stu-id="89e00-122">Description</span></span>|  
|-------------------------|----------|-----------------|  
|<span data-ttu-id="89e00-123">IoT – Debounce IoT Alerts (<xref:Microsoft.Dynamics.CRM.msdyn_ParentIoTAlerts>)</span><span class="sxs-lookup"><span data-stu-id="89e00-123">IoT – Debounce IoT Alerts (<xref:Microsoft.Dynamics.CRM.msdyn_ParentIoTAlerts>)</span></span>|<span data-ttu-id="89e00-124">Hành động</span><span class="sxs-lookup"><span data-stu-id="89e00-124">Action</span></span>|<span data-ttu-id="89e00-125">Links potential redundant alerts to an existing parent alert</span><span class="sxs-lookup"><span data-stu-id="89e00-125">Links potential redundant alerts to an existing parent alert</span></span>|  
|<span data-ttu-id="89e00-126">IoT - Parent IoT Alerts</span><span class="sxs-lookup"><span data-stu-id="89e00-126">IoT - Parent IoT Alerts</span></span>|<span data-ttu-id="89e00-127">Quy trình</span><span class="sxs-lookup"><span data-stu-id="89e00-127">Workflow</span></span>|<span data-ttu-id="89e00-128">Calls the `IoT - Debounce IoT Alerts` action and passes 60 for the `TimespanSeconds` parameter</span><span class="sxs-lookup"><span data-stu-id="89e00-128">Calls the `IoT - Debounce IoT Alerts` action and passes 60 for the `TimespanSeconds` parameter</span></span>|  
|<span data-ttu-id="89e00-129">IoT – Register Custom Entity (<xref:Microsoft.Dynamics.CRM.msdyn_RegisterCustomEntity>)</span><span class="sxs-lookup"><span data-stu-id="89e00-129">IoT – Register Custom Entity (<xref:Microsoft.Dynamics.CRM.msdyn_RegisterCustomEntity>)</span></span>|<span data-ttu-id="89e00-130">Hành động</span><span class="sxs-lookup"><span data-stu-id="89e00-130">Action</span></span>|<span data-ttu-id="89e00-131">Registers any custom entity that may or may not already have connected IoT devices.</span><span class="sxs-lookup"><span data-stu-id="89e00-131">Registers any custom entity that may or may not already have connected IoT devices.</span></span> <span data-ttu-id="89e00-132">This action invokes the `IoT – Register Device` action.</span><span class="sxs-lookup"><span data-stu-id="89e00-132">This action invokes the `IoT – Register Device` action.</span></span>|  
|<span data-ttu-id="89e00-133">IoT – Register Device (<xref:Microsoft.Dynamics.CRM.msdyn_RegisterIoTDevice>)</span><span class="sxs-lookup"><span data-stu-id="89e00-133">IoT – Register Device (<xref:Microsoft.Dynamics.CRM.msdyn_RegisterIoTDevice>)</span></span>|<span data-ttu-id="89e00-134">Hành động</span><span class="sxs-lookup"><span data-stu-id="89e00-134">Action</span></span>|<span data-ttu-id="89e00-135">Publishes the registration requests for an IoT device</span><span class="sxs-lookup"><span data-stu-id="89e00-135">Publishes the registration requests for an IoT device</span></span>|  
|<span data-ttu-id="89e00-136">IoT – Send Test Alert (<xref:Microsoft.Dynamics.CRM.msdyn_IoTSendTestAlert>)</span><span class="sxs-lookup"><span data-stu-id="89e00-136">IoT – Send Test Alert (<xref:Microsoft.Dynamics.CRM.msdyn_IoTSendTestAlert>)</span></span>|<span data-ttu-id="89e00-137">Hành động</span><span class="sxs-lookup"><span data-stu-id="89e00-137">Action</span></span>|<span data-ttu-id="89e00-138">*Reserved for future use*</span><span class="sxs-lookup"><span data-stu-id="89e00-138">*Reserved for future use*</span></span>|  
|<span data-ttu-id="89e00-139">JSON-based Field Value – Get Boolean (<xref:Microsoft.Dynamics.CRM.msdyn_JsonGetBoolean>)</span><span class="sxs-lookup"><span data-stu-id="89e00-139">JSON-based Field Value – Get Boolean (<xref:Microsoft.Dynamics.CRM.msdyn_JsonGetBoolean>)</span></span>|<span data-ttu-id="89e00-140">Hành động</span><span class="sxs-lookup"><span data-stu-id="89e00-140">Action</span></span>|<span data-ttu-id="89e00-141">Reads a Boolean property in the specified JSON object</span><span class="sxs-lookup"><span data-stu-id="89e00-141">Reads a Boolean property in the specified JSON object</span></span>|  
|<span data-ttu-id="89e00-142">JSON-based Field Value – Get Number (<xref:Microsoft.Dynamics.CRM.msdyn_JsonGetNumber>)</span><span class="sxs-lookup"><span data-stu-id="89e00-142">JSON-based Field Value – Get Number (<xref:Microsoft.Dynamics.CRM.msdyn_JsonGetNumber>)</span></span>|<span data-ttu-id="89e00-143">Hành động</span><span class="sxs-lookup"><span data-stu-id="89e00-143">Action</span></span>|<span data-ttu-id="89e00-144">Reads a numeric property in the specified JSON object</span><span class="sxs-lookup"><span data-stu-id="89e00-144">Reads a numeric property in the specified JSON object</span></span>|  
|<span data-ttu-id="89e00-145">JSON-based Field Value – Get String (<xref:Microsoft.Dynamics.CRM.msdyn_JsonGetString>)</span><span class="sxs-lookup"><span data-stu-id="89e00-145">JSON-based Field Value – Get String (<xref:Microsoft.Dynamics.CRM.msdyn_JsonGetString>)</span></span>|<span data-ttu-id="89e00-146">Hành động</span><span class="sxs-lookup"><span data-stu-id="89e00-146">Action</span></span>|<span data-ttu-id="89e00-147">Reads a string property in the specified JSON object</span><span class="sxs-lookup"><span data-stu-id="89e00-147">Reads a string property in the specified JSON object</span></span>|  
|<span data-ttu-id="89e00-148">IoT Alert (<xref:Microsoft.Dynamics.CRM.msdyn_iotalert>)</span><span class="sxs-lookup"><span data-stu-id="89e00-148">IoT Alert (<xref:Microsoft.Dynamics.CRM.msdyn_iotalert>)</span></span>|<span data-ttu-id="89e00-149">Thực thể</span><span class="sxs-lookup"><span data-stu-id="89e00-149">Entity</span></span>|<span data-ttu-id="89e00-150">Represents a notable event sent from the associated IoT Hub</span><span class="sxs-lookup"><span data-stu-id="89e00-150">Represents a notable event sent from the associated IoT Hub</span></span>|  
|<span data-ttu-id="89e00-151">IoT Device (<xref:Microsoft.Dynamics.CRM.msdyn_iotdevice>)</span><span class="sxs-lookup"><span data-stu-id="89e00-151">IoT Device (<xref:Microsoft.Dynamics.CRM.msdyn_iotdevice>)</span></span>|<span data-ttu-id="89e00-152">Thực thể</span><span class="sxs-lookup"><span data-stu-id="89e00-152">Entity</span></span>|<span data-ttu-id="89e00-153">Represents a connected device that can be registered with a IoT Hub</span><span class="sxs-lookup"><span data-stu-id="89e00-153">Represents a connected device that can be registered with a IoT Hub</span></span>|  
|<span data-ttu-id="89e00-154">IoT Device Category (<xref:Microsoft.Dynamics.CRM.msdyn_iotdevicecategory>)</span><span class="sxs-lookup"><span data-stu-id="89e00-154">IoT Device Category (<xref:Microsoft.Dynamics.CRM.msdyn_iotdevicecategory>)</span></span>|<span data-ttu-id="89e00-155">Thực thể</span><span class="sxs-lookup"><span data-stu-id="89e00-155">Entity</span></span>|<span data-ttu-id="89e00-156">Represents a logical grouping of IoT devices</span><span class="sxs-lookup"><span data-stu-id="89e00-156">Represents a logical grouping of IoT devices</span></span>|  
|<span data-ttu-id="89e00-157">IoT Device Command (<xref:Microsoft.Dynamics.CRM.msdyn_iotdevicecommand>)</span><span class="sxs-lookup"><span data-stu-id="89e00-157">IoT Device Command (<xref:Microsoft.Dynamics.CRM.msdyn_iotdevicecommand>)</span></span>|<span data-ttu-id="89e00-158">Thực thể</span><span class="sxs-lookup"><span data-stu-id="89e00-158">Entity</span></span>|<span data-ttu-id="89e00-159">Represents an outgoing message to a device connected to the IoT Hub</span><span class="sxs-lookup"><span data-stu-id="89e00-159">Represents an outgoing message to a device connected to the IoT Hub</span></span>|  
|<span data-ttu-id="89e00-160">IoT Device Registration History (<xref:Microsoft.Dynamics.CRM.msdyn_iotdeviceregistrationhistory>)</span><span class="sxs-lookup"><span data-stu-id="89e00-160">IoT Device Registration History (<xref:Microsoft.Dynamics.CRM.msdyn_iotdeviceregistrationhistory>)</span></span>|<span data-ttu-id="89e00-161">Thực thể</span><span class="sxs-lookup"><span data-stu-id="89e00-161">Entity</span></span>|<span data-ttu-id="89e00-162">Tracks registration activities of an IoT device</span><span class="sxs-lookup"><span data-stu-id="89e00-162">Tracks registration activities of an IoT device</span></span>|  
  
### <a name="iot-enabling-an-entity-type"></a><span data-ttu-id="89e00-163">IOT enabling an entity type</span><span class="sxs-lookup"><span data-stu-id="89e00-163">IOT enabling an entity type</span></span>

 [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] <span data-ttu-id="89e00-164">entities can be associated to IoT entities listed above so that within [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] they can participate in IoT-related business processes and analyses.</span><span class="sxs-lookup"><span data-stu-id="89e00-164">entities can be associated to IoT entities listed above so that within [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] they can participate in IoT-related business processes and analyses.</span></span> <span data-ttu-id="89e00-165">There are two methods of “IoT enabling” a [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] entity; you can:</span><span class="sxs-lookup"><span data-stu-id="89e00-165">There are two methods of “IoT enabling” a [!INCLUDE[pn_dyn_365](../../includes/pn-dyn-365.md)] entity; you can:</span></span>  
  
- <span data-ttu-id="89e00-166">Programmatically form an association through the standard Dynamics 365 for Customer Engagement [Connection entities](../../developer/connection-entities.md) capability.</span><span class="sxs-lookup"><span data-stu-id="89e00-166">Programmatically form an association through the standard Dynamics 365 for Customer Engagement [Connection entities](../../developer/connection-entities.md) capability.</span></span> <span data-ttu-id="89e00-167">You can alternatively accomplish this same association through the administration UI; for more information, see [Create connections to view relationships between records](https://www.microsoft.com/dynamics/crm-customer-center/create-connections-to-view-relationships-between-records.aspx).</span><span class="sxs-lookup"><span data-stu-id="89e00-167">You can alternatively accomplish this same association through the administration UI; for more information, see [Create connections to view relationships between records](https://www.microsoft.com/dynamics/crm-customer-center/create-connections-to-view-relationships-between-records.aspx).</span></span>  
  
- <span data-ttu-id="89e00-168">Call the `IoT – Register Custom Entity` action to associate an entity with an existing or new `IoT Device`.</span><span class="sxs-lookup"><span data-stu-id="89e00-168">Call the `IoT – Register Custom Entity` action to associate an entity with an existing or new `IoT Device`.</span></span>  
  
  <span data-ttu-id="89e00-169">A common example of this capability is to associate a [Customer Asset](https://www.microsoft.com/dynamics/crm-customer-center/configure-and-set-up-customer-assets-field-service.aspx) to an `IoT Device`.</span><span class="sxs-lookup"><span data-stu-id="89e00-169">A common example of this capability is to associate a [Customer Asset](https://www.microsoft.com/dynamics/crm-customer-center/configure-and-set-up-customer-assets-field-service.aspx) to an `IoT Device`.</span></span>