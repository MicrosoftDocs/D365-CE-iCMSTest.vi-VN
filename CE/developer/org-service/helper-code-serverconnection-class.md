---
title: 'Helper code: ServerConnection class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: The ServerConnection class demonstrates how to establish a connection to the Dynamics 365 for Customer Engagement web services for the purpose of invoking web methods
ms.custom: ''
ms.date: 12/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 84056850-972d-4209-a293-acd5a5503fbf
caps.latest.revision: 41
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fe63fd12c9e6e7d7819905097b1461ff1376d7d2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386865"
---
# <a name="helper-code-serverconnection-class"></a><span data-ttu-id="ae107-103">Helper code: ServerConnection class</span><span class="sxs-lookup"><span data-stu-id="ae107-103">Helper code: ServerConnection class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ae107-104">The primary purpose of the `ServerConnection` class is to show how to connect to the [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] web services to invoke web methods.</span><span class="sxs-lookup"><span data-stu-id="ae107-104">The primary purpose of the `ServerConnection` class is to show how to connect to the [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] web services to invoke web methods.</span></span> <span data-ttu-id="ae107-105">In addition, applications must typically perform other tasks such as obtaining server and organization information, obtaining user login credentials, creating a service proxy, and refreshing the WCF connection security token.</span><span class="sxs-lookup"><span data-stu-id="ae107-105">In addition, applications must typically perform other tasks such as obtaining server and organization information, obtaining user login credentials, creating a service proxy, and refreshing the WCF connection security token.</span></span> <span data-ttu-id="ae107-106">The `ServerConnection` class provides this needed functionality.</span><span class="sxs-lookup"><span data-stu-id="ae107-106">The `ServerConnection` class provides this needed functionality.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="ae107-107">The `ServerConnection` class is used by most samples that are included in the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)].</span><span class="sxs-lookup"><span data-stu-id="ae107-107">The `ServerConnection` class is used by most samples that are included in the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)].</span></span> <span data-ttu-id="ae107-108">The class is updated periodically with new functionality.</span><span class="sxs-lookup"><span data-stu-id="ae107-108">The class is updated periodically with new functionality.</span></span> <span data-ttu-id="ae107-109">Do not simply reuse the helper code for authentication in your applications.</span><span class="sxs-lookup"><span data-stu-id="ae107-109">Do not simply reuse the helper code for authentication in your applications.</span></span> <span data-ttu-id="ae107-110">It is code that the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] uses to provide the optimum experience when you run our Console application samples included in the SDK.</span><span class="sxs-lookup"><span data-stu-id="ae107-110">It is code that the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] uses to provide the optimum experience when you run our Console application samples included in the SDK.</span></span> <span data-ttu-id="ae107-111">It contains all the key elements of authentication and demonstrates their use, but it may not represent the best solution for your application.</span><span class="sxs-lookup"><span data-stu-id="ae107-111">It contains all the key elements of authentication and demonstrates their use, but it may not represent the best solution for your application.</span></span> <span data-ttu-id="ae107-112">It is sample code that you can use as a basis for designing an authentication management system that fits the requirements of your application.</span><span class="sxs-lookup"><span data-stu-id="ae107-112">It is sample code that you can use as a basis for designing an authentication management system that fits the requirements of your application.</span></span> <span data-ttu-id="ae107-113">Refer to the topic [Use connection strings in XRM tooling to connect to Dynamics 365 for Customer Engagement apps](../xrm-tooling/use-connection-strings-xrm-tooling-connect.md) for an alternate method for authenticating with the web services.</span><span class="sxs-lookup"><span data-stu-id="ae107-113">Refer to the topic [Use connection strings in XRM tooling to connect to Dynamics 365 for Customer Engagement apps](../xrm-tooling/use-connection-strings-xrm-tooling-connect.md) for an alternate method for authenticating with the web services.</span></span>  
  
 <span data-ttu-id="ae107-114">The file is present in code samples' folder that you download.</span><span class="sxs-lookup"><span data-stu-id="ae107-114">The file is present in code samples' folder that you download.</span></span>
 
 <span data-ttu-id="ae107-115">Path: `<download-directory>\<sample name>\C#\CrmServiceHelpers.cs`.</span><span class="sxs-lookup"><span data-stu-id="ae107-115">Path: `<download-directory>\<sample name>\C#\CrmServiceHelpers.cs`.</span></span>
 
 <span data-ttu-id="ae107-116">For example, if you download the **Work with attribute metadata** sample to D drive, you can find the sample in the following folder path.</span><span class="sxs-lookup"><span data-stu-id="ae107-116">For example, if you download the **Work with attribute metadata** sample to D drive, you can find the sample in the following folder path.</span></span>

 <span data-ttu-id="ae107-117">Path: `D:\Work with attribute metadata\CrmServiceHelpers.cs`</span><span class="sxs-lookup"><span data-stu-id="ae107-117">Path: `D:\Work with attribute metadata\CrmServiceHelpers.cs`</span></span>
  
 <span data-ttu-id="ae107-118">Use the class source code in the CrmServiceHelpers files as a basis for your own classes or use the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for just the basic functionality of setting up a service connection.</span><span class="sxs-lookup"><span data-stu-id="ae107-118">Use the class source code in the CrmServiceHelpers files as a basis for your own classes or use the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for just the basic functionality of setting up a service connection.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae107-119">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="ae107-119">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="ae107-120">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="ae107-120">Demonstrates</span></span>  
 <span data-ttu-id="ae107-121">The `ServerConnection` class demonstrates how to establish a connection to the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services for the purpose of invoking web methods.</span><span class="sxs-lookup"><span data-stu-id="ae107-121">The `ServerConnection` class demonstrates how to establish a connection to the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services for the purpose of invoking web methods.</span></span> <span data-ttu-id="ae107-122">Before a connection can be created, information about the server, organization, and user must first be obtained.</span><span class="sxs-lookup"><span data-stu-id="ae107-122">Before a connection can be created, information about the server, organization, and user must first be obtained.</span></span> <span data-ttu-id="ae107-123">This information is gathered in either of two ways: by interactively prompting the user in the console window, or by loading saved server configuration information from the local disk.</span><span class="sxs-lookup"><span data-stu-id="ae107-123">This information is gathered in either of two ways: by interactively prompting the user in the console window, or by loading saved server configuration information from the local disk.</span></span> <span data-ttu-id="ae107-124">The server connection information is persisted to a file named Credentials.xml located at `C:\Users\<username>\AppData\Roaming\CrmServer`.</span><span class="sxs-lookup"><span data-stu-id="ae107-124">The server connection information is persisted to a file named Credentials.xml located at `C:\Users\<username>\AppData\Roaming\CrmServer`.</span></span>  
  
 <span data-ttu-id="ae107-125">For each server configuration saved in the Credentials.xml file, the user’s logon password is stored as a generic credential in the Windows Credential Manager.</span><span class="sxs-lookup"><span data-stu-id="ae107-125">For each server configuration saved in the Credentials.xml file, the user’s logon password is stored as a generic credential in the Windows Credential Manager.</span></span> <span data-ttu-id="ae107-126">The credential naming format is Microsoft_CRMSDK:\<*server*>:\<*organization*>:\<*userID*>.</span><span class="sxs-lookup"><span data-stu-id="ae107-126">The credential naming format is Microsoft_CRMSDK:\<*server*>:\<*organization*>:\<*userID*>.</span></span>  
  
 <span data-ttu-id="ae107-127">Useful code for authentication can be found in the `GetProxy` and `GetOrganizationProxy` methods.</span><span class="sxs-lookup"><span data-stu-id="ae107-127">Useful code for authentication can be found in the `GetProxy` and `GetOrganizationProxy` methods.</span></span> <span data-ttu-id="ae107-128">Also, the code that creates and reads a user’s password in the [!INCLUDE[pn_Windows_Credential_Manager](../../includes/pn-windows-credential-manager.md)] may be of interest.</span><span class="sxs-lookup"><span data-stu-id="ae107-128">Also, the code that creates and reads a user’s password in the [!INCLUDE[pn_Windows_Credential_Manager](../../includes/pn-windows-credential-manager.md)] may be of interest.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ae107-129">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="ae107-129">Example</span></span>  
 [!code-csharp[HelperCode#crmservicehelper](../../snippets/csharp/CRMV8/helpercode/cs/crmservicehelper.cs#crmservicehelper)] 
  
### <a name="see-also"></a><span data-ttu-id="ae107-130">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ae107-130">See also</span></span>  
 [<span data-ttu-id="ae107-131">Use the Sample and Helper Code</span><span class="sxs-lookup"><span data-stu-id="ae107-131">Use the Sample and Helper Code</span></span>](use-sample-helper-code.md)  
 <span data-ttu-id="ae107-132">[Sample: Quick start for Dynamics 365 for Customer Engagement apps](../sample-quick-start.md) </span><span class="sxs-lookup"><span data-stu-id="ae107-132">[Sample: Quick start for Dynamics 365 for Customer Engagement apps](../sample-quick-start.md) </span></span>  
 [<span data-ttu-id="ae107-133">Access the Web Services in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="ae107-133">Access the Web Services in Dynamics 365 for Customer Engagement</span></span>](../authenticate-users.md)
