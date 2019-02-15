---
title: 'Sample: Simplified connection quick start (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'This sample shows you how to connect to the Dynamics 365 for Customer Engagement (online) Customer Engagement web services using the CrmServiceClient and perform basic create, update, retrieve, and delete operations on an entity. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a4fb3634-948e-4bac-a32f-f626c78d83a0
caps.latest.revision: 29
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b942fa6494e478ce6baebfca466af35894304d0a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386584"
---
# <a name="sample-simplified-connection-quick-start-using-dynamics-365-for-customer-engagement"></a><span data-ttu-id="50bf1-103">Sample: Simplified connection quick start using Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="50bf1-103">Sample: Simplified connection quick start using Dynamics 365 for Customer Engagement</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="50bf1-104">This sample shows you how to connect to the [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] web services using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> and perform basic create, update, retrieve, and delete operations on an entity.</span><span class="sxs-lookup"><span data-stu-id="50bf1-104">This sample shows you how to connect to the [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] web services using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> and perform basic create, update, retrieve, and delete operations on an entity.</span></span> <span data-ttu-id="50bf1-105">For more information about the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient>, see [Use CrmServiceClient constructors to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md).</span><span class="sxs-lookup"><span data-stu-id="50bf1-105">For more information about the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient>, see [Use CrmServiceClient constructors to connect to Dynamics 365 for Customer Engagement apps](use-crmserviceclient-constructors-connect.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="50bf1-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="50bf1-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]

## <a name="requirements"></a><span data-ttu-id="50bf1-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="50bf1-107">Requirements</span></span>

<span data-ttu-id="50bf1-108">The complete sample code can be found here [Sample: Quick start for Microsoft Dynamics 365 for Customer Engagement apps](https://code.msdn.microsoft.com/Sample-Quick-start-for-650dbcaa)</span><span class="sxs-lookup"><span data-stu-id="50bf1-108">The complete sample code can be found here [Sample: Quick start for Microsoft Dynamics 365 for Customer Engagement apps](https://code.msdn.microsoft.com/Sample-Quick-start-for-650dbcaa)</span></span> 

<!--[!INCLUDE[sdk_download](../../includes/sdk-download.md)]-->

<span data-ttu-id="50bf1-109">You must modify the supplied app.config file with connection information for your [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server before running the sample.</span><span class="sxs-lookup"><span data-stu-id="50bf1-109">You must modify the supplied app.config file with connection information for your [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server before running the sample.</span></span> <span data-ttu-id="50bf1-110">For more information, see the commented out example connection strings in the app.config file.</span><span class="sxs-lookup"><span data-stu-id="50bf1-110">For more information, see the commented out example connection strings in the app.config file.</span></span>  

## <a name="demonstrates"></a><span data-ttu-id="50bf1-111">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="50bf1-111">Demonstrates</span></span>

<span data-ttu-id="50bf1-112">This sample authenticates the user with the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services by using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> and methods.</span><span class="sxs-lookup"><span data-stu-id="50bf1-112">This sample authenticates the user with the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services by using the <xref:Microsoft.Xrm.Tooling.Connector.CrmServiceClient> and methods.</span></span> <span data-ttu-id="50bf1-113">After obtaining a reference to the Organization web service, the sample performs basic create, update, retrieve, and delete operations on an account entity.</span><span class="sxs-lookup"><span data-stu-id="50bf1-113">After obtaining a reference to the Organization web service, the sample performs basic create, update, retrieve, and delete operations on an account entity.</span></span> <span data-ttu-id="50bf1-114">The sample also handles common exceptions.</span><span class="sxs-lookup"><span data-stu-id="50bf1-114">The sample also handles common exceptions.</span></span> <span data-ttu-id="50bf1-115">No helper code is used to establish a connection to the Organization web service.</span><span class="sxs-lookup"><span data-stu-id="50bf1-115">No helper code is used to establish a connection to the Organization web service.</span></span>  

<span data-ttu-id="50bf1-116">In addition, this sample supports OAuth authentication and advanced connection diagnostics.</span><span class="sxs-lookup"><span data-stu-id="50bf1-116">In addition, this sample supports OAuth authentication and advanced connection diagnostics.</span></span> <span data-ttu-id="50bf1-117">For more information on using diagnostics, see [Configure tracing for XRM Tooling](configure-tracing-xrm-tooling.md).</span><span class="sxs-lookup"><span data-stu-id="50bf1-117">For more information on using diagnostics, see [Configure tracing for XRM Tooling](configure-tracing-xrm-tooling.md).</span></span>

## <a name="example"></a><span data-ttu-id="50bf1-118">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="50bf1-118">Example</span></span>

<span data-ttu-id="50bf1-119">The following shows a sample app.config file.</span><span class="sxs-lookup"><span data-stu-id="50bf1-119">The following shows a sample app.config file.</span></span> <span data-ttu-id="50bf1-120">To use this, remove the comment characters “<!- -” at the beginning of the \<add …</span><span class="sxs-lookup"><span data-stu-id="50bf1-120">To use this, remove the comment characters “<!- -” at the beginning of the \<add …</span></span> <span data-ttu-id="50bf1-121">/> line and the “- ->” at the end on the line for the line that is relevant to your server and organization.</span><span class="sxs-lookup"><span data-stu-id="50bf1-121">/> line and the “- ->” at the end on the line for the line that is relevant to your server and organization.</span></span> <span data-ttu-id="50bf1-122">Next, modify the attribute values as appropriate for your configuration.</span><span class="sxs-lookup"><span data-stu-id="50bf1-122">Next, modify the attribute values as appropriate for your configuration.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <connectionStrings>  
    <!-- Online using Office 365 -->  
    <!-- <add name="Server=CRM Online, organization=contoso, user=someone"  
         connectionString="Url=https://contoso.crm.dynamics.com; Username=someone@contoso.onmicrosoft.com; Password=password; authtype=Office365"/> -->  

    <!-- On-premises with provided user credentials -->  
    <!-- <add name="Server=myserver, organization=AdventureWorksCycle, user=administrator"  
         connectionString="Url=http://myserver/AdventureWorksCycle; Domain=mydomain; Username=administrator; Password=password; authtype=AD"/> -->  

    <!-- On-premises using Windows integrated security -->  
    <!-- <add name="Server=myserver, organization=AdventureWorksCycle"  
         connectionString="Url=http://myserver/AdventureWorksCycle; authtype=AD"/> -->  

    <!-- On-Premises (IFD) with claims -->  
    <!--<add name="Server=litware.com, organization=contoso, user=someone@litware.com"  
         connectionString="Url=https://contoso.litware.com/contoso; Username=someone@litware.com; Password=password; authtype=IFD"/>-->  
  </connectionStrings>  
  <startup>  
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5.2" />  
  </startup>  
<system.diagnostics>  
    <trace autoflush="true"/>  
    <sources>  
      <source name="Microsoft.Xrm.Tooling.Connector.CrmServiceClient" switchName="Microsoft.Xrm.Tooling.Connector.CrmServiceClient" switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console" type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="fileListener"/>  
        </listeners>  
      </source>  
      <source name="Microsoft.Xrm.Tooling.CrmConnectControl" switchName="Microsoft.Xrm.Tooling.CrmConnectControl" switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console" type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="fileListener"/>  
        </listeners>  
      </source>  
      <source name="CrmSvcUtil" switchName="CrmSvcUtil" switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console" type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="fileListener"/>  
        </listeners>  
      </source>  
    </sources>  
    <switches>  

      <!--Possible values for switches: Off, Error, Warning, Information, Verbose  
                        Verbose:      includes Error, Warning, Info, Trace levels  
                        Information:  includes Error, Warning, Info levels  
                        Warning:      includes Error, Warning levels  
                        Error:        includes Error level-->  

      <add name="Microsoft.Xrm.Tooling.CrmConnectControl" value="Off"/>  
      <add name="Microsoft.Xrm.Tooling.Connector.CrmServiceClient" value="Error"/>  
      <add name="CrmSvcUtil" value="Off"/>  
    </switches>  

    <sharedListeners>  
      <add name="fileListener" type="System.Diagnostics.TextWriterTraceListener" initializeData="CrmSvcUtil.log"/>  
    </sharedListeners>  

  </system.diagnostics>  
  <runtime>  
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">  
      <dependentAssembly>  
        <assemblyIdentity name="Microsoft.Xrm.Sdk" publicKeyToken="31bf3856ad364e35" culture="neutral" />  
        <bindingRedirect oldVersion="0.0.0.0-7.0.0.0" newVersion="8.0.0.0" />  
      </dependentAssembly>  
      <dependentAssembly>  
        <assemblyIdentity name="Microsoft.Xrm.Sdk.Deployment" publicKeyToken="31bf3856ad364e35" culture="neutral" />  
        <bindingRedirect oldVersion="0.0.0.0-7.0.0.0" newVersion="8.0.0.0" />  
      </dependentAssembly>  
      <dependentAssembly>  
        <assemblyIdentity name="Microsoft.ServiceBus" publicKeyToken="31bf3856ad364e35" culture="neutral" />  
        <bindingRedirect oldVersion="0.0.0.0-2.4.0.0" newVersion="2.4.0.0" />  
      </dependentAssembly>  
    </assemblyBinding>  
  </runtime>  
</configuration>  
```

## <a name="example"></a><span data-ttu-id="50bf1-123">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="50bf1-123">Example</span></span>

[!code-csharp[QuickStartCS#SimplifiedConnection](../../snippets/csharp/CRMV8/quickstartcs/cs/simplifiedconnection.cs#simplifiedconnection)]  

### <a name="see-also"></a><span data-ttu-id="50bf1-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="50bf1-124">See also</span></span>
[<span data-ttu-id="50bf1-125">Use connection strings in XRM tooling to connect to Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="50bf1-125">Use connection strings in XRM tooling to connect to Dynamics 365 for Customer Engagement apps</span></span>](use-connection-strings-xrm-tooling-connect.md)<br />
[<span data-ttu-id="50bf1-126">Tutorials for Learning About Dynamics 365 for Customer Engagement apps Development</span><span class="sxs-lookup"><span data-stu-id="50bf1-126">Tutorials for Learning About Dynamics 365 for Customer Engagement apps Development</span></span>](../tutorials-resources-sdk.md)<br />
[<span data-ttu-id="50bf1-127">Run a Simple Program Using Dynamics 365 for Customer Engagement Web Services</span><span class="sxs-lookup"><span data-stu-id="50bf1-127">Run a Simple Program Using Dynamics 365 for Customer Engagement Web Services</span></span>](../simple-program-web-services.md)<br />
[<span data-ttu-id="50bf1-128">Sample: Quick Start for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="50bf1-128">Sample: Quick Start for Dynamics 365 for Customer Engagement apps</span></span>](../sample-quick-start.md)<br />
[<span data-ttu-id="50bf1-129">Sample: Quick start for XRM Tooling API</span><span class="sxs-lookup"><span data-stu-id="50bf1-129">Sample: Quick start for XRM Tooling API</span></span>](sample-quick-start-xrm-tooling-api.md)<br />
