---
title: Configure tracing for XRM tooling (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn how you can configure tracing for components such as operation calls, warnings, exceptions, and other significant events in XRM Tooling
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d7586a5a-40da-427e-bbeb-4f8a371a8dcf
caps.latest.revision: 8
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ce8821c56f97de2981cfda23fa3196e3be29571b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385833"
---
# <a name="configure-tracing-for-xrm-tooling"></a><span data-ttu-id="8ccce-103">Configure tracing for XRM tooling</span><span class="sxs-lookup"><span data-stu-id="8ccce-103">Configure tracing for XRM tooling</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8ccce-104">You can enable tracing to record data related to process milestones across all components of XRM tooling, such as operation calls, warnings, exceptions, and other significant events.</span><span class="sxs-lookup"><span data-stu-id="8ccce-104">You can enable tracing to record data related to process milestones across all components of XRM tooling, such as operation calls, warnings, exceptions, and other significant events.</span></span> <span data-ttu-id="8ccce-105">This information can be used for troubleshooting operational and performance issues in your Windows client applications.</span><span class="sxs-lookup"><span data-stu-id="8ccce-105">This information can be used for troubleshooting operational and performance issues in your Windows client applications.</span></span> <span data-ttu-id="8ccce-106">Tracing in XRM tooling is built on top of [System.Tracing](https://msdn.microsoft.com/library/vstudio/system.diagnostics\(v=vs.100\).aspx).</span><span class="sxs-lookup"><span data-stu-id="8ccce-106">Tracing in XRM tooling is built on top of [System.Tracing](https://msdn.microsoft.com/library/vstudio/system.diagnostics\(v=vs.100\).aspx).</span></span> <span data-ttu-id="8ccce-107">To enable tracing for an assembly or component, for example Microsoft.Xrm.Tooling.Connector, you must define the following three things for each component in your code or in the application configuration file (*\<AppName>*.exe.config):</span><span class="sxs-lookup"><span data-stu-id="8ccce-107">To enable tracing for an assembly or component, for example Microsoft.Xrm.Tooling.Connector, you must define the following three things for each component in your code or in the application configuration file (*\<AppName>*.exe.config):</span></span>  
  
- <span data-ttu-id="8ccce-108">A trace source</span><span class="sxs-lookup"><span data-stu-id="8ccce-108">A trace source</span></span>  
  
- <span data-ttu-id="8ccce-109">A trace listener</span><span class="sxs-lookup"><span data-stu-id="8ccce-109">A trace listener</span></span>  
  
- <span data-ttu-id="8ccce-110">A trace level other than **Off**.</span><span class="sxs-lookup"><span data-stu-id="8ccce-110">A trace level other than **Off**.</span></span> <span data-ttu-id="8ccce-111">These are the other values that you can specify: **Error**, **Warning**, **Info**, and **Verbose**.</span><span class="sxs-lookup"><span data-stu-id="8ccce-111">These are the other values that you can specify: **Error**, **Warning**, **Info**, and **Verbose**.</span></span>  
  
  <span data-ttu-id="8ccce-112">Here is the configuration for enabling tracing for a component in XRM tooling.</span><span class="sxs-lookup"><span data-stu-id="8ccce-112">Here is the configuration for enabling tracing for a component in XRM tooling.</span></span> <span data-ttu-id="8ccce-113">For example, the following configuration only enables tracing for the Microsoft.Xrm.Tooling.CrmConnectControl component:</span><span class="sxs-lookup"><span data-stu-id="8ccce-113">For example, the following configuration only enables tracing for the Microsoft.Xrm.Tooling.CrmConnectControl component:</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="true" />  
    <sources>  
      <source name="DynamicsCrm.CrmConnectControl"  
        switchName="DynamicsCrm.CrmConnectControl"  
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console" type="System.Diagnostics.DefaultTraceListener" />  
          <remove name="Default"/>  
          <add name ="fileListener"/>  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <!--   
            Possible values for switches: Off, Error, Warning, Info, Verbose  
                Verbose:    includes Error, Warning, Info, Trace levels  
                Info:       includes Error, Warning, Info levels  
                Warning:    includes Error, Warning levels  
                Error:      includes Error level  
        -->  
      <add name="DynamicsCrm.CrmConnectControl" value="Verbose"/>  
    </switches>  
    <sharedListeners>  
      <add name="fileListener" type="System.Diagnostics.TextWriterTraceListener" initializeData="XRMLoginControl.log"/>  
      <add name="eventLogListener" type="System.Diagnostics.EventLogTraceListener" initializeData="XRMLogin"/>  
    </sharedListeners>  
  </system.diagnostics>  
</configuration>  
```  
  
 <span data-ttu-id="8ccce-114">If you want to enable tracing for all of the components in XRM tooling, you can do that as well.</span><span class="sxs-lookup"><span data-stu-id="8ccce-114">If you want to enable tracing for all of the components in XRM tooling, you can do that as well.</span></span> <span data-ttu-id="8ccce-115">Here is the configuration for a combined tracing of all three of the components in XRM tooling:</span><span class="sxs-lookup"><span data-stu-id="8ccce-115">Here is the configuration for a combined tracing of all three of the components in XRM tooling:</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <trace autoflush="true" />  
    <sources>  
      <source name="Microsoft.Xrm.Tooling.Connector.CrmServiceClient"  
              switchName="Microsoft.Xrm.Tooling.Connector.CrmServiceClient"  
              switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console" type="System.Diagnostics.DefaultTraceListener" />  
          <remove name="Default"/>  
          <add name ="fileListener"/>  
        </listeners>  
      </source>  
  
      <source name="Microsoft.Xrm.Tooling.CrmConnectControl"  
              switchName="Microsoft.Xrm.Tooling.CrmConnectControl"  
              switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console" type="System.Diagnostics.DefaultTraceListener" />  
          <remove name="Default"/>  
          <add name ="fileListener"/>  
        </listeners>  
      </source>  
  
      <source name="Microsoft.Xrm.Tooling.WebResourceUtility"  
        switchName="Microsoft.Xrm.Tooling.WebResourceUtility"  
        switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <add name="console" type="System.Diagnostics.DefaultTraceListener" />  
          <remove name="Default"/>  
          <add name ="fileListener"/>  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <!--   
            Possible values for switches: Off, Error, Warning, Info, Verbose  
                Verbose:    includes Error, Warning, Info, Trace levels  
                Info:       includes Error, Warning, Info levels  
                Warning:    includes Error, Warning levels  
                Error:      includes Error level  
        -->  
      <add name="Microsoft.Xrm.Tooling.Connector.CrmServiceClient" value="Verbose" />  
      <add name="Microsoft.Xrm.Tooling.CrmConnectControl" value="Verbose"/>  
      <add name="Microsoft.Xrm.Tooling.WebResourceUtility" value="Verbose" />  
  
    </switches>  
    <sharedListeners>  
      <add name="fileListener" type="System.Diagnostics.TextWriterTraceListener" initializeData="XRMToolingLogs.log"/>        
      <add name="eventLogListener" type="System.Diagnostics.EventLogTraceListener" initializeData="XRMTooling" />  
    </sharedListeners>  
  
  </system.diagnostics>  
</configuration>  
```  
  
### <a name="see-also"></a><span data-ttu-id="8ccce-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8ccce-116">See also</span></span>  
 [<span data-ttu-id="8ccce-117">Build Windows client applications using the XRM tools</span><span class="sxs-lookup"><span data-stu-id="8ccce-117">Build Windows client applications using the XRM tools</span></span>](../build-windows-client-applications-xrm-tools.md)