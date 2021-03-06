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
# <a name="helper-code-serverconnection-class"></a>Helper code: ServerConnection class

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The primary purpose of the `ServerConnection` class is to show how to connect to the [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] web services to invoke web methods. In addition, applications must typically perform other tasks such as obtaining server and organization information, obtaining user login credentials, creating a service proxy, and refreshing the WCF connection security token. The `ServerConnection` class provides this needed functionality.  
  
> [!CAUTION]
>  The `ServerConnection` class is used by most samples that are included in the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)]. The class is updated periodically with new functionality. Do not simply reuse the helper code for authentication in your applications. It is code that the [!INCLUDE [pn-sdk](../../includes/pn-sdk.md)] uses to provide the optimum experience when you run our Console application samples included in the SDK. It contains all the key elements of authentication and demonstrates their use, but it may not represent the best solution for your application. It is sample code that you can use as a basis for designing an authentication management system that fits the requirements of your application. Refer to the topic [Use connection strings in XRM tooling to connect to Dynamics 365 for Customer Engagement apps](../xrm-tooling/use-connection-strings-xrm-tooling-connect.md) for an alternate method for authenticating with the web services.  
  
 The file is present in code samples' folder that you download.
 
 Path: `<download-directory>\<sample name>\C#\CrmServiceHelpers.cs`.
 
 For example, if you download the **Work with attribute metadata** sample to D drive, you can find the sample in the following folder path.

 Path: `D:\Work with attribute metadata\CrmServiceHelpers.cs`
  
 Use the class source code in the CrmServiceHelpers files as a basis for your own classes or use the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> class for just the basic functionality of setting up a service connection.  
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 The `ServerConnection` class demonstrates how to establish a connection to the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services for the purpose of invoking web methods. Before a connection can be created, information about the server, organization, and user must first be obtained. This information is gathered in either of two ways: by interactively prompting the user in the console window, or by loading saved server configuration information from the local disk. The server connection information is persisted to a file named Credentials.xml located at `C:\Users\<username>\AppData\Roaming\CrmServer`.  
  
 For each server configuration saved in the Credentials.xml file, the user’s logon password is stored as a generic credential in the Windows Credential Manager. The credential naming format is Microsoft_CRMSDK:\<*server*>:\<*organization*>:\<*userID*>.  
  
 Useful code for authentication can be found in the `GetProxy` and `GetOrganizationProxy` methods. Also, the code that creates and reads a user’s password in the [!INCLUDE[pn_Windows_Credential_Manager](../../includes/pn-windows-credential-manager.md)] may be of interest.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[HelperCode#crmservicehelper](../../snippets/csharp/CRMV8/helpercode/cs/crmservicehelper.cs#crmservicehelper)] 
  
### <a name="see-also"></a>Xem thêm  
 [Use the Sample and Helper Code](use-sample-helper-code.md)  
 [Sample: Quick start for Dynamics 365 for Customer Engagement apps](../sample-quick-start.md)   
 [Access the Web Services in Dynamics 365 for Customer Engagement](../authenticate-users.md)
