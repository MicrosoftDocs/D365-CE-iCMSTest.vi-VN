---
title: Use the generic listener adapter in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use generic listener adapter that can be used as a testing tool for integrating Unified Service Desk with the CTI middleware applications that have the ability to open a URL on the user's computer when a CTI event occurs.
ms.custom:
- dyn365-USD
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
ms.assetid: b51a92d6-5f3f-4bf4-b326-37e4d7b728ce
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 4b8c6b6d53384ea076c0bf5775819b30e27181d2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387939"
---
# <a name="use-the-generic-listener-adapter-in-unified-service-desk"></a><span data-ttu-id="610ce-103">Use the generic listener adapter in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="610ce-103">Use the generic listener adapter in Unified Service Desk</span></span>
[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="610ce-104">provides a generic listener adapter that can be used as a testing tool for integrating [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] with the [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] middleware applications that have the ability to open a URL on the user's computer when a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] event occurs.</span><span class="sxs-lookup"><span data-stu-id="610ce-104">provides a generic listener adapter that can be used as a testing tool for integrating [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] with the [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] middleware applications that have the ability to open a URL on the user's computer when a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] event occurs.</span></span> <span data-ttu-id="610ce-105">The generic listener adapter listens for HTTP request on a known port (5000): `http://localhost:5000/`</span><span class="sxs-lookup"><span data-stu-id="610ce-105">The generic listener adapter listens for HTTP request on a known port (5000): `http://localhost:5000/`</span></span>  

<a name="How"></a>   
## <a name="how-does-the-generic-listener-work"></a><span data-ttu-id="610ce-106">How does the generic listener work</span><span class="sxs-lookup"><span data-stu-id="610ce-106">How does the generic listener work</span></span>  
 <span data-ttu-id="610ce-107">The generic listener adapter extracts a query string from the URL, uses the values in the string as parameters to evaluate them as a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] event, and then raises a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] screen pop in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="610ce-107">The generic listener adapter extracts a query string from the URL, uses the values in the string as parameters to evaluate them as a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] event, and then raises a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] screen pop in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="610ce-108">Once the adapter starts listening on the specified port, it waits for the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] middleware to open a URL such as:</span><span class="sxs-lookup"><span data-stu-id="610ce-108">Once the adapter starts listening on the specified port, it waits for the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] middleware to open a URL such as:</span></span>  

```  
http://localhost:5000/?ani=1234&dnis=4355&type=phonecall&customerid=49383433  
```  

 <span data-ttu-id="610ce-109">In the example URL, the query string is split out and passed to the Global Manager hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] as the following parameters.</span><span class="sxs-lookup"><span data-stu-id="610ce-109">In the example URL, the query string is split out and passed to the Global Manager hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] as the following parameters.</span></span>  


|     <span data-ttu-id="610ce-110">Tham số</span><span class="sxs-lookup"><span data-stu-id="610ce-110">Parameter</span></span>     |                                                                                                                                                                                    <span data-ttu-id="610ce-111">Mô tả</span><span class="sxs-lookup"><span data-stu-id="610ce-111">Description</span></span>                                                                                                                                                                                    | <span data-ttu-id="610ce-112">Values in the example URL</span><span class="sxs-lookup"><span data-stu-id="610ce-112">Values in the example URL</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
|       `ANI`       |                                                                                                                                           <span data-ttu-id="610ce-113">Stands for *automatic number identification*.</span><span class="sxs-lookup"><span data-stu-id="610ce-113">Stands for *automatic number identification*.</span></span> <span data-ttu-id="610ce-114">This is the phone number of the incoming call.</span><span class="sxs-lookup"><span data-stu-id="610ce-114">This is the phone number of the incoming call.</span></span>                                                                                                                                            |        `ani=1234`         |
|      `DNIS`       |                                                                                                                                       <span data-ttu-id="610ce-115">Stands for *dialed number identification service*.</span><span class="sxs-lookup"><span data-stu-id="610ce-115">Stands for *dialed number identification service*.</span></span> <span data-ttu-id="610ce-116">This is the phone number that the customer called.</span><span class="sxs-lookup"><span data-stu-id="610ce-116">This is the phone number that the customer called.</span></span>                                                                                                                                       |        `dnis=4355`        |
|      `Type`       | <span data-ttu-id="610ce-117">This is corresponding to the **Initiating Activity** information in your window navigation rule to route the call, and take appropriate actions.</span><span class="sxs-lookup"><span data-stu-id="610ce-117">This is corresponding to the **Initiating Activity** information in your window navigation rule to route the call, and take appropriate actions.</span></span> <span data-ttu-id="610ce-118">Common values include `phonecall` and `chat`.</span><span class="sxs-lookup"><span data-stu-id="610ce-118">Common values include `phonecall` and `chat`.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="610ce-119">[CTI search](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#CTISearch)</span><span class="sxs-lookup"><span data-stu-id="610ce-119">[CTI search](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md#CTISearch)</span></span> |     `type=phonecall`      |
| `Key=value pairs` |                                                                                                                    <span data-ttu-id="610ce-120">A collection of key-value pairs that enables the Global Manager hosted control to raise a `CTILookUpRequest` to search the customer record.</span><span class="sxs-lookup"><span data-stu-id="610ce-120">A collection of key-value pairs that enables the Global Manager hosted control to raise a `CTILookUpRequest` to search the customer record.</span></span>                                                                                                                    |   `customerid=49383433`   |

 <span data-ttu-id="610ce-121">For [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] searches, each of these parameters may be used as replacement parameters.</span><span class="sxs-lookup"><span data-stu-id="610ce-121">For [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] searches, each of these parameters may be used as replacement parameters.</span></span> <span data-ttu-id="610ce-122">Once a session starts, these parameters can be accessed with the `cti` prefix such as:</span><span class="sxs-lookup"><span data-stu-id="610ce-122">Once a session starts, these parameters can be accessed with the `cti` prefix such as:</span></span>  

```  
[[cti.ani]]  
```  

 <span data-ttu-id="610ce-123">To view a walkthrough that demonstrates the usage of the generic listener adapter for handling [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] events, see [Walkthrough: Use generic listener adapter for CTI events](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md).</span><span class="sxs-lookup"><span data-stu-id="610ce-123">To view a walkthrough that demonstrates the usage of the generic listener adapter for handling [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] events, see [Walkthrough: Use generic listener adapter for CTI events](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md).</span></span>  

<a name="Configure"></a>   
## <a name="configure-the-cti-desktop-manager-hosted-control-for-generic-listener-adapter"></a><span data-ttu-id="610ce-124">Configure the CTI Desktop Manager hosted control for generic listener adapter</span><span class="sxs-lookup"><span data-stu-id="610ce-124">Configure the CTI Desktop Manager hosted control for generic listener adapter</span></span>  
 <span data-ttu-id="610ce-125">When using the generic listener adapter, you only have to configure the CTI Desktop Manager component; the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] connector and the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] control aren’t required.</span><span class="sxs-lookup"><span data-stu-id="610ce-125">When using the generic listener adapter, you only have to configure the CTI Desktop Manager component; the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] connector and the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] control aren’t required.</span></span> <span data-ttu-id="610ce-126">The CTI Desktop Manager hosted control should be configured to be placed on a `HiddenPanel`, and the following standard values apply for the generic listener adapter in the hosted control configuration page in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="610ce-126">The CTI Desktop Manager hosted control should be configured to be placed on a `HiddenPanel`, and the following standard values apply for the generic listener adapter in the hosted control configuration page in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  

- <span data-ttu-id="610ce-127">**Assembly URI**: Microsoft.Crm.UnifiedServiceDesk.GenericListener</span><span class="sxs-lookup"><span data-stu-id="610ce-127">**Assembly URI**: Microsoft.Crm.UnifiedServiceDesk.GenericListener</span></span>  

- <span data-ttu-id="610ce-128">**Assembly Type**: Microsoft.Crm.UnifiedServiceDesk.GenericListener.DesktopManager</span><span class="sxs-lookup"><span data-stu-id="610ce-128">**Assembly Type**: Microsoft.Crm.UnifiedServiceDesk.GenericListener.DesktopManager</span></span>  

  <span data-ttu-id="610ce-129">![Configure CTI Dekstop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager.png "Configure CTI Dekstop Manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="610ce-129">![Configure CTI Dekstop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager.png "Configure CTI Dekstop Manager hosted control")</span></span>  

  <span data-ttu-id="610ce-130">For detailed information about configuring a CTI Desktop Manager hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Configure CTI Desktop Manager hosted control in Unified Service Desk](../unified-service-desk/create-cti-desktop-manager.md#Configure).</span><span class="sxs-lookup"><span data-stu-id="610ce-130">For detailed information about configuring a CTI Desktop Manager hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Configure CTI Desktop Manager hosted control in Unified Service Desk](../unified-service-desk/create-cti-desktop-manager.md#Configure).</span></span>  

<a name="ChangePort"></a>   
## <a name="change-the-port-of-generic-listener"></a><span data-ttu-id="610ce-131">Change the port of generic listener</span><span class="sxs-lookup"><span data-stu-id="610ce-131">Change the port of generic listener</span></span>  
 <span data-ttu-id="610ce-132">By default, the generic listener adapter listens for HTTP request on port 5000: `http://localhost:5000/`.</span><span class="sxs-lookup"><span data-stu-id="610ce-132">By default, the generic listener adapter listens for HTTP request on port 5000: `http://localhost:5000/`.</span></span>  

 <span data-ttu-id="610ce-133">You can use the **Options** setting in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to define a different port for the generic listener, if required.</span><span class="sxs-lookup"><span data-stu-id="610ce-133">You can use the **Options** setting in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to define a different port for the generic listener, if required.</span></span> <span data-ttu-id="610ce-134">To do so:</span><span class="sxs-lookup"><span data-stu-id="610ce-134">To do so:</span></span>  

1. <span data-ttu-id="610ce-135">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="610ce-135">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="610ce-136">Bấm vào **Tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="610ce-136">Click **Options**.</span></span>  

4. <span data-ttu-id="610ce-137">Click **New** to add a new option.</span><span class="sxs-lookup"><span data-stu-id="610ce-137">Click **New** to add a new option.</span></span>  

5. <span data-ttu-id="610ce-138">Type the following values in the fields:</span><span class="sxs-lookup"><span data-stu-id="610ce-138">Type the following values in the fields:</span></span>  

   |<span data-ttu-id="610ce-139">Trường</span><span class="sxs-lookup"><span data-stu-id="610ce-139">Field</span></span>|<span data-ttu-id="610ce-140">Value</span><span class="sxs-lookup"><span data-stu-id="610ce-140">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="610ce-141">Tên</span><span class="sxs-lookup"><span data-stu-id="610ce-141">Name</span></span>|<span data-ttu-id="610ce-142">GenericListener</span><span class="sxs-lookup"><span data-stu-id="610ce-142">GenericListener</span></span>|  
   |<span data-ttu-id="610ce-143">Value</span><span class="sxs-lookup"><span data-stu-id="610ce-143">Value</span></span>|<span data-ttu-id="610ce-144">Specify the new URL for the listener.</span><span class="sxs-lookup"><span data-stu-id="610ce-144">Specify the new URL for the listener.</span></span> <span data-ttu-id="610ce-145">Ví dụ: `http://localhost:5001/`</span><span class="sxs-lookup"><span data-stu-id="610ce-145">For example: `http://localhost:5001/`</span></span>|  

   <span data-ttu-id="610ce-146">![Define a port for a generic listener](../unified-service-desk/media/usd-change-listener-port.png "Define a port for a generic listener")</span><span class="sxs-lookup"><span data-stu-id="610ce-146">![Define a port for a generic listener](../unified-service-desk/media/usd-change-listener-port.png "Define a port for a generic listener")</span></span>  

6. <span data-ttu-id="610ce-147">Click **Save & Close**.</span><span class="sxs-lookup"><span data-stu-id="610ce-147">Click **Save & Close**.</span></span>  

### <a name="see-also"></a><span data-ttu-id="610ce-148">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="610ce-148">See also</span></span>  
 <span data-ttu-id="610ce-149">[Build a custom CTI adapter for Unified Service Desk](../unified-service-desk/build-custom-cti-adapter-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="610ce-149">[Build a custom CTI adapter for Unified Service Desk](../unified-service-desk/build-custom-cti-adapter-unified-service-desk.md) </span></span>  
 <span data-ttu-id="610ce-150">[Considerations for creating a CTI adapter for Unified Service Desk](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="610ce-150">[Considerations for creating a CTI adapter for Unified Service Desk](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="610ce-151">UII Computer Telephony Integration (CTI) framework</span><span class="sxs-lookup"><span data-stu-id="610ce-151">UII Computer Telephony Integration (CTI) framework</span></span>](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)
