---
title: Troubleshooting tips (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This topic contains tips to diagnose and fix certain common issues that may arise when developing Dynamics 365 for Customer Engagement apps SDK–based applications
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 79667e12-19eb-4942-bb44-3212a7e42899
caps.latest.revision: 40
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ca9f0814e00497892bcdf00f186eb34878ebcbd8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386104"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="867a9-103">Troubleshooting tips</span><span class="sxs-lookup"><span data-stu-id="867a9-103">Troubleshooting tips</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="867a9-104">The following information is provided as an aid in diagnosing certain common issues that may arise when developing applications using the .NET SDK assemblies.</span><span class="sxs-lookup"><span data-stu-id="867a9-104">The following information is provided as an aid in diagnosing certain common issues that may arise when developing applications using the .NET SDK assemblies.</span></span> <span data-ttu-id="867a9-105">More content will be added to this topic as time goes on.</span><span class="sxs-lookup"><span data-stu-id="867a9-105">More content will be added to this topic as time goes on.</span></span>  
  
 <span data-ttu-id="867a9-106">For more information about enabling tracing in an on-premises [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server, see [Monitor and troubleshooting Microsoft Dynamics CRM](https://technet.microsoft.com/library/hh699694.aspx).</span><span class="sxs-lookup"><span data-stu-id="867a9-106">For more information about enabling tracing in an on-premises [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server, see [Monitor and troubleshooting Microsoft Dynamics CRM](https://technet.microsoft.com/library/hh699694.aspx).</span></span>  
  
## <a name="handle-the-messagesecurityexception-exception-when-you-use-the-includepndynamicscrmincludespn-dynamics-crmmd-web-services"></a><span data-ttu-id="867a9-107">Handle the MessageSecurityException exception when you use the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services</span><span class="sxs-lookup"><span data-stu-id="867a9-107">Handle the MessageSecurityException exception when you use the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services</span></span>
  
 <span data-ttu-id="867a9-108">When you use the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] APIs to connect to the [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps organization or discovery services you could receive the following exception:</span><span class="sxs-lookup"><span data-stu-id="867a9-108">When you use the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] APIs to connect to the [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)] apps organization or discovery services you could receive the following exception:</span></span>  
  
```ms-dos  
Unhandled Exception: System.ServiceModel.Security.MessageSecurityException: An unsecured or incorrectly secured fault was received from the other party. See the inner FaultException for the fault code and detail.  
```  
  
 <span data-ttu-id="867a9-109">To fix this, you can try deleting the device registration folder named `LiveDeviceID` in your profile folder `C:\Users\<username>`.</span><span class="sxs-lookup"><span data-stu-id="867a9-109">To fix this, you can try deleting the device registration folder named `LiveDeviceID` in your profile folder `C:\Users\<username>`.</span></span> <span data-ttu-id="867a9-110">Then, try to connect again.</span><span class="sxs-lookup"><span data-stu-id="867a9-110">Then, try to connect again.</span></span>  
  
## <a name="exceptions-that-can-occur-when-running-crmsvcutil"></a><span data-ttu-id="867a9-111">Exceptions that can occur when running CrmSvcUtil</span><span class="sxs-lookup"><span data-stu-id="867a9-111">Exceptions that can occur when running CrmSvcUtil</span></span>  

 <span data-ttu-id="867a9-112">When you run the CrmSvcUtil.exe tool to generate early-bound entity types, you might receive an exception with the following message.</span><span class="sxs-lookup"><span data-stu-id="867a9-112">When you run the CrmSvcUtil.exe tool to generate early-bound entity types, you might receive an exception with the following message.</span></span>  
  
```ms-dos  
The type initializer for Microsoft.Xrm.Client.CodeGeneration.CodeCustomization threw an exception.  
```  
  
 <span data-ttu-id="867a9-113">This error can be caused if the build version of the CrmSvcUtil tool and `Microsoft.Xrm.Client.CodeGeneration.dll` assembly aren’t the same.</span><span class="sxs-lookup"><span data-stu-id="867a9-113">This error can be caused if the build version of the CrmSvcUtil tool and `Microsoft.Xrm.Client.CodeGeneration.dll` assembly aren’t the same.</span></span> <span data-ttu-id="867a9-114">When you develop applications using the .NET SDK assemblies, always use the CrmSvcUtil tool and assemblies that are provided in the same version of the NuGet package.</span><span class="sxs-lookup"><span data-stu-id="867a9-114">When you develop applications using the .NET SDK assemblies, always use the CrmSvcUtil tool and assemblies that are provided in the same version of the NuGet package.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="867a9-115">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="867a9-115">See also</span></span>  
 <span data-ttu-id="867a9-116">[Troubleshooting and Error Handling](troubleshooting-error-handling.md) </span><span class="sxs-lookup"><span data-stu-id="867a9-116">[Troubleshooting and Error Handling](troubleshooting-error-handling.md) </span></span>  
 [<span data-ttu-id="867a9-117">Web Service Error Codes</span><span class="sxs-lookup"><span data-stu-id="867a9-117">Web Service Error Codes</span></span>](web-service-error-codes.md)
