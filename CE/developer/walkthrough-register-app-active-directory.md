---
title: 'Walkthrough: Register a Dynamics 365 for Customer Engagement app with Active Directory (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: This walkthrough describes how to register an application with Azure Active Directory so that it can connect to the Dynamics 365 for Customer Engagement server, authenticate using OAuth, and access the web services
ms.custom: ''
ms.date: 10/31/2017
ms.prod: crm-2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (on-premises)
helpviewer_keywords:
- mobile, modern
- register, registration
- app
ms.assetid: dd48aa30-7b05-4b15-a039-ff6522da8613
caps.latest.revision: 57
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 214247c2aef2f16b3ee9dc4d38eaf299c831ae2a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388383"
---
# <a name="walkthrough-register-a-dynamics-365-for-customer-engagement-app-with-active-directory"></a><span data-ttu-id="c38a6-103">Walkthrough: Register a Dynamics 365 for Customer Engagement app with Active Directory</span><span class="sxs-lookup"><span data-stu-id="c38a6-103">Walkthrough: Register a Dynamics 365 for Customer Engagement app with Active Directory</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="c38a6-104">This walkthrough describes how to register a desktop client or mobile application so that it can connect to and authenticate with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement server and access the Web services.</span><span class="sxs-lookup"><span data-stu-id="c38a6-104">This walkthrough describes how to register a desktop client or mobile application so that it can connect to and authenticate with the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement server and access the Web services.</span></span> <span data-ttu-id="c38a6-105">Once registered, an application can access the Web services using HTTP requests through the server’s SOAP or Web API endpoints.</span><span class="sxs-lookup"><span data-stu-id="c38a6-105">Once registered, an application can access the Web services using HTTP requests through the server’s SOAP or Web API endpoints.</span></span>  
  
[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 

## <a name="prerequisites"></a><span data-ttu-id="c38a6-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="c38a6-106">Prerequisites</span></span>  
 <span data-ttu-id="c38a6-107">For an on-premises or Internet-facing deployment (IFD):</span><span class="sxs-lookup"><span data-stu-id="c38a6-107">For an on-premises or Internet-facing deployment (IFD):</span></span>  
  
- <span data-ttu-id="c38a6-108">A [!INCLUDE[pn_windows_server_2012_r2](../includes/pn-windows-server-2012-r2.md)] with [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c38a6-108">A [!INCLUDE[pn_windows_server_2012_r2](../includes/pn-windows-server-2012-r2.md)] with [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)].</span></span>  
  
- <span data-ttu-id="c38a6-109">You must have administrator access to the server hosting the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] deployment services role and the [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] server.</span><span class="sxs-lookup"><span data-stu-id="c38a6-109">You must have administrator access to the server hosting the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] deployment services role and the [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] server.</span></span>  
  
- <span data-ttu-id="c38a6-110">The on-premises server must be configured to use claims authentication.</span><span class="sxs-lookup"><span data-stu-id="c38a6-110">The on-premises server must be configured to use claims authentication.</span></span>  
  
- <span data-ttu-id="c38a6-111">The redirect URL for your application.</span><span class="sxs-lookup"><span data-stu-id="c38a6-111">The redirect URL for your application.</span></span> <span data-ttu-id="c38a6-112">Instructions for finding that URL are provided in the section named [Obtain the redirect URL](walkthrough-register-app-active-directory.md#bkmk_redirect).</span><span class="sxs-lookup"><span data-stu-id="c38a6-112">Instructions for finding that URL are provided in the section named [Obtain the redirect URL](walkthrough-register-app-active-directory.md#bkmk_redirect).</span></span>  
  
<a name="bkmk_redirect"></a>   
## <a name="obtain-the-redirect-uri"></a><span data-ttu-id="c38a6-113">Obtain the redirect URI</span><span class="sxs-lookup"><span data-stu-id="c38a6-113">Obtain the redirect URI</span></span>  
 <span data-ttu-id="c38a6-114">One method to obtain the redirect URI for a native client [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] application is to execute the following line of code in a debug session of your application and examine the returned URI value.</span><span class="sxs-lookup"><span data-stu-id="c38a6-114">One method to obtain the redirect URI for a native client [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] application is to execute the following line of code in a debug session of your application and examine the returned URI value.</span></span> <span data-ttu-id="c38a6-115">In a WinJS debug session, select the `RawUri` property.</span><span class="sxs-lookup"><span data-stu-id="c38a6-115">In a WinJS debug session, select the `RawUri` property.</span></span>  
  
```csharp  
string redirectUri = WebAuthenticationBroker.GetCurrentApplicationCallbackUri().ToString();  
```  
  
```vb  
Dim redirectUri As String = WebAuthenticationBroker.GetCurrentApplicationCallbackUri().ToString()  
```  
  
```javascript  
Windows.Security.Authentication.Web.WebAuthenticationBroker.getCurrentApplicationCallbackUri()  
```  
  
 <span data-ttu-id="c38a6-116">The `WebAuthenticationBroker` class can be found in the `Windows.Security.Authentication.Web` namespace.</span><span class="sxs-lookup"><span data-stu-id="c38a6-116">The `WebAuthenticationBroker` class can be found in the `Windows.Security.Authentication.Web` namespace.</span></span> <span data-ttu-id="c38a6-117">Use the string value returned from the method call when you register the app.</span><span class="sxs-lookup"><span data-stu-id="c38a6-117">Use the string value returned from the method call when you register the app.</span></span> 
 
 <!--The C# line of code is shown in the topic [Sample: Windows 8 desktop modern OData app](sample-windows-8-desktop-modern-odata-app.md).  -->
  
 <span data-ttu-id="c38a6-118">For a non-[!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] native client application such as a console application, use any valid URI value.</span><span class="sxs-lookup"><span data-stu-id="c38a6-118">For a non-[!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] native client application such as a console application, use any valid URI value.</span></span> <span data-ttu-id="c38a6-119">In this case, the URI doesn’t need to actually exist but it must be unique in the tenant.</span><span class="sxs-lookup"><span data-stu-id="c38a6-119">In this case, the URI doesn’t need to actually exist but it must be unique in the tenant.</span></span>  
  
<a name="bkmk_ifd"></a>   
## <a name="app-registration-for-dynamics-365-for-customer-engagement-on-premises-ifd"></a><span data-ttu-id="c38a6-120">App registration for Dynamics 365 for Customer Engagement on-premises (IFD)</span><span class="sxs-lookup"><span data-stu-id="c38a6-120">App registration for Dynamics 365 for Customer Engagement on-premises (IFD)</span></span>  
 <span data-ttu-id="c38a6-121">**Scenario**: A customer or other person registers a custom application to access organization data on a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server provided by an ISV or Partner.</span><span class="sxs-lookup"><span data-stu-id="c38a6-121">**Scenario**: A customer or other person registers a custom application to access organization data on a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server provided by an ISV or Partner.</span></span>  
  
#### <a name="the-isv-or-partner-performs-the-following-tasks"></a><span data-ttu-id="c38a6-122">The ISV or Partner performs the following tasks:</span><span class="sxs-lookup"><span data-stu-id="c38a6-122">The ISV or Partner performs the following tasks:</span></span>  
  
1. <span data-ttu-id="c38a6-123">Configures the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] on-premises (IFD) server and [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] server using [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] commands that are provided later in this section.</span><span class="sxs-lookup"><span data-stu-id="c38a6-123">Configures the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] on-premises (IFD) server and [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] server using [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] commands that are provided later in this section.</span></span>  
  
2. <span data-ttu-id="c38a6-124">Provides the client ID and server address URL information to the customer.</span><span class="sxs-lookup"><span data-stu-id="c38a6-124">Provides the client ID and server address URL information to the customer.</span></span>  
  
#### <a name="the-customer-or-other-person-performs-the-following-tasks"></a><span data-ttu-id="c38a6-125">The customer or other person performs the following tasks:</span><span class="sxs-lookup"><span data-stu-id="c38a6-125">The customer or other person performs the following tasks:</span></span>  
  
1.  <span data-ttu-id="c38a6-126">Configures the external application by entering the client ID and server address URL in the app as instructed.</span><span class="sxs-lookup"><span data-stu-id="c38a6-126">Configures the external application by entering the client ID and server address URL in the app as instructed.</span></span>  
  
### <a name="includepndynamicscrmincludespn-dynamics-crmmd-server-setup"></a>[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="c38a6-127">server setup</span><span class="sxs-lookup"><span data-stu-id="c38a6-127">server setup</span></span>  
 <span data-ttu-id="c38a6-128">To configure the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server to enable federated claims, follow these steps.</span><span class="sxs-lookup"><span data-stu-id="c38a6-128">To configure the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server to enable federated claims, follow these steps.</span></span>  
  
##### <a name="configure-claims-settings"></a><span data-ttu-id="c38a6-129">Configure claims settings</span><span class="sxs-lookup"><span data-stu-id="c38a6-129">Configure claims settings</span></span>  
  
1. <span data-ttu-id="c38a6-130">Log on as administrator on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server that hosts the deployment service role and open a [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] command window.</span><span class="sxs-lookup"><span data-stu-id="c38a6-130">Log on as administrator on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server that hosts the deployment service role and open a [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] command window.</span></span>  
  
2. <span data-ttu-id="c38a6-131">Add the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)][!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] snap-in (Microsoft.Crm.PowerShell.dll).</span><span class="sxs-lookup"><span data-stu-id="c38a6-131">Add the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)][!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] snap-in (Microsoft.Crm.PowerShell.dll).</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="c38a6-132">[Quản lý việc triển khai bằng cách sử dụng Windows PowerShell](https://technet.microsoft.com/library/dn531202.aspx)</span><span class="sxs-lookup"><span data-stu-id="c38a6-132">[Administer the deployment using Windows PowerShell](https://technet.microsoft.com/library/dn531202.aspx)</span></span>  
  
   ```powershell  
   Add-PSSnapin Microsoft.Crm.PowerShell  
   ```  
  
3. <span data-ttu-id="c38a6-133">Enter the following [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] commands.</span><span class="sxs-lookup"><span data-stu-id="c38a6-133">Enter the following [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] commands.</span></span>  
  
   ```powershell  
  
   $ClaimsSettings = Get-CrmSetting -SettingType OAuthClaimsSettings  
   $ClaimsSettings.Enabled = $true  
   Set-CrmSetting -Setting $ClaimsSettings  
  
   ```  
  
<a name="bkmk_adfs"></a>   
### <a name="ad-fs-server-setup"></a><span data-ttu-id="c38a6-134">AD FS server setup</span><span class="sxs-lookup"><span data-stu-id="c38a6-134">AD FS server setup</span></span>  
 <span data-ttu-id="c38a6-135">To register the external application with [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)], follow these steps.</span><span class="sxs-lookup"><span data-stu-id="c38a6-135">To register the external application with [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)], follow these steps.</span></span>  
  
##### <a name="register-the-application-in-active-directory"></a><span data-ttu-id="c38a6-136">Register the application in Active Directory</span><span class="sxs-lookup"><span data-stu-id="c38a6-136">Register the application in Active Directory</span></span>  
  
1. <span data-ttu-id="c38a6-137">Log on to the [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] server as administrator and open a [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] command window.</span><span class="sxs-lookup"><span data-stu-id="c38a6-137">Log on to the [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] server as administrator and open a [!INCLUDE[pn_PowerShell](../includes/pn-powershell.md)] command window.</span></span>  
  
2. <span data-ttu-id="c38a6-138">Enter the following command.</span><span class="sxs-lookup"><span data-stu-id="c38a6-138">Enter the following command.</span></span>  
  
   ```powershell  
   Add-AdfsClient -ClientId <CLIENT_ID> -Name <APP_NAME> -RedirectUri <REDIRECT_URI>  
   ```  
  
    <span data-ttu-id="c38a6-139">Where <CLIENT_ID> is a unique number, <APP_NAME> is a name for the application, and <REDIRECT_URI> is any valid URI that [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] is to redirect to after authentication has completed.</span><span class="sxs-lookup"><span data-stu-id="c38a6-139">Where <CLIENT_ID> is a unique number, <APP_NAME> is a name for the application, and <REDIRECT_URI> is any valid URI that [!INCLUDE[pn_adfs_short](../includes/pn-adfs-short.md)] is to redirect to after authentication has completed.</span></span> <span data-ttu-id="c38a6-140">It is recommended that the client ID be a GUID.</span><span class="sxs-lookup"><span data-stu-id="c38a6-140">It is recommended that the client ID be a GUID.</span></span> <span data-ttu-id="c38a6-141">You can generate a GUID in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] by opening the **Tools** menu and clicking **Create GUID**.</span><span class="sxs-lookup"><span data-stu-id="c38a6-141">You can generate a GUID in [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] by opening the **Tools** menu and clicking **Create GUID**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c38a6-142">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c38a6-142">See also</span></span>  
 <span data-ttu-id="c38a6-143">[Adding, Updating, and Removing an Application](https://msdn.microsoft.com/library/dn132599.aspx) </span><span class="sxs-lookup"><span data-stu-id="c38a6-143">[Adding, Updating, and Removing an Application](https://msdn.microsoft.com/library/dn132599.aspx) </span></span>  
 [<span data-ttu-id="c38a6-144">Authenticate Users with Dynamics 365 for Customer Engagement Web Services</span><span class="sxs-lookup"><span data-stu-id="c38a6-144">Authenticate Users with Dynamics 365 for Customer Engagement Web Services</span></span>](authenticate-users.md)
