---
title: 'Web API Helper code: Configuration classes (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: Configuration class hierarchy can be used to specify the required connection data for accessing Dynamics 365 for Customer Engagement web services from your application
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3b86c11a-15e1-40a1-aca0-34a9bab2f04a
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 61b589b6386981fb9a441f60e4af182df15958cb
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388068"
---
# <a name="web-api-helper-code-configuration-classes"></a><span data-ttu-id="008ab-103">Web API Helper code: Configuration classes</span><span class="sxs-lookup"><span data-stu-id="008ab-103">Web API Helper code: Configuration classes</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="008ab-104">Use the configuration class hierarchy to specify the required connection data for accessing [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services from your application.</span><span class="sxs-lookup"><span data-stu-id="008ab-104">Use the configuration class hierarchy to specify the required connection data for accessing [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] web services from your application.</span></span> <span data-ttu-id="008ab-105">You can supply this connection data either by setting values directly in your code, possibly from user input, using the `Configuration` base class.</span><span class="sxs-lookup"><span data-stu-id="008ab-105">You can supply this connection data either by setting values directly in your code, possibly from user input, using the `Configuration` base class.</span></span> <span data-ttu-id="008ab-106">More typically, you supply this information in settings stored in your application configuration file, using the derived class, `FileConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="008ab-106">More typically, you supply this information in settings stored in your application configuration file, using the derived class, `FileConfiguration`.</span></span>  

 <span data-ttu-id="008ab-107">The source code for the configuration class hierarchy is located in the file Configuration.cs in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode/).</span><span class="sxs-lookup"><span data-stu-id="008ab-107">The source code for the configuration class hierarchy is located in the file Configuration.cs in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode/).</span></span> <span data-ttu-id="008ab-108">The configuration class hierarchy is designed to work in conjunction with the `Authentication`class to enable you to establish a secure connection to your Dynamics 365 for Customer Engagement service.</span><span class="sxs-lookup"><span data-stu-id="008ab-108">The configuration class hierarchy is designed to work in conjunction with the `Authentication`class to enable you to establish a secure connection to your Dynamics 365 for Customer Engagement service.</span></span> <span data-ttu-id="008ab-109">For more information, see             [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="008ab-109">For more information, see             [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span></span>  

<a name="bkmk_Connectiondata"></a>

## <a name="connection-data"></a><span data-ttu-id="008ab-110">Connection data</span><span class="sxs-lookup"><span data-stu-id="008ab-110">Connection data</span></span>

 <span data-ttu-id="008ab-111">The `Configuration`class reads and parses the application configuration file to obtain the following connection data.</span><span class="sxs-lookup"><span data-stu-id="008ab-111">The `Configuration`class reads and parses the application configuration file to obtain the following connection data.</span></span>  


| <span data-ttu-id="008ab-112">Connection data</span><span class="sxs-lookup"><span data-stu-id="008ab-112">Connection data</span></span> |     <span data-ttu-id="008ab-113">Các triển khai</span><span class="sxs-lookup"><span data-stu-id="008ab-113">Deployments</span></span>     |                                                                                                                                  <span data-ttu-id="008ab-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="008ab-114">Description</span></span>                                                                                                                                  |
|-----------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="008ab-115">Service URL</span><span class="sxs-lookup"><span data-stu-id="008ab-115">Service URL</span></span>   |         <span data-ttu-id="008ab-116">Tất cả</span><span class="sxs-lookup"><span data-stu-id="008ab-116">All</span></span>         |                                                                                                                   <span data-ttu-id="008ab-117">The base URL to the Dynamics 365 for Customer Engagement service</span><span class="sxs-lookup"><span data-stu-id="008ab-117">The base URL to the Dynamics 365 for Customer Engagement service</span></span>                                                                                                                    |
|    <span data-ttu-id="008ab-118">Tên người dùng</span><span class="sxs-lookup"><span data-stu-id="008ab-118">Username</span></span>     |         <span data-ttu-id="008ab-119">Tất cả</span><span class="sxs-lookup"><span data-stu-id="008ab-119">All</span></span>         |                                                                                                                   <span data-ttu-id="008ab-120">The user name registered in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="008ab-120">The user name registered in Dynamics 365 for Customer Engagement apps</span></span>                                                                                                                    |
|    <span data-ttu-id="008ab-121">Mật khẩu</span><span class="sxs-lookup"><span data-stu-id="008ab-121">Password</span></span>     |         <span data-ttu-id="008ab-122">Tất cả</span><span class="sxs-lookup"><span data-stu-id="008ab-122">All</span></span>         |                                                                                                                          <span data-ttu-id="008ab-123">The password for that user</span><span class="sxs-lookup"><span data-stu-id="008ab-123">The password for that user</span></span>                                                                                                                           |
|     <span data-ttu-id="008ab-124">Domain</span><span class="sxs-lookup"><span data-stu-id="008ab-124">Domain</span></span>      |         <span data-ttu-id="008ab-125">Tất cả</span><span class="sxs-lookup"><span data-stu-id="008ab-125">All</span></span>         |                                                                                                  <span data-ttu-id="008ab-126">The domain of the Dynamics 365 for Customer Engagement apps service for Active Directory authentication</span><span class="sxs-lookup"><span data-stu-id="008ab-126">The domain of the Dynamics 365 for Customer Engagement apps service for Active Directory authentication</span></span>                                                                                                   |
|    <span data-ttu-id="008ab-127">Client ID</span><span class="sxs-lookup"><span data-stu-id="008ab-127">Client ID</span></span>    | <span data-ttu-id="008ab-128">Online and IFD only</span><span class="sxs-lookup"><span data-stu-id="008ab-128">Online and IFD only</span></span> | <span data-ttu-id="008ab-129">The client ID of the application as it was registered with Azure AD for [!INCLUDE[pn_dyn_365_online](../../includes/pn-crm-online.md)] apps or your Active Directory tenant for [!INCLUDE[pn_dyn_365_op](../../includes/pn-dyn-365-op.md)] using Internet-facing deployment (IFD).</span><span class="sxs-lookup"><span data-stu-id="008ab-129">The client ID of the application as it was registered with Azure AD for [!INCLUDE[pn_dyn_365_online](../../includes/pn-crm-online.md)] apps or your Active Directory tenant for [!INCLUDE[pn_dyn_365_op](../../includes/pn-dyn-365-op.md)] using Internet-facing deployment (IFD).</span></span> |
|  <span data-ttu-id="008ab-130">URL Chuyển hướng</span><span class="sxs-lookup"><span data-stu-id="008ab-130">Redirect URL</span></span>   | <span data-ttu-id="008ab-131">Online and IFD only</span><span class="sxs-lookup"><span data-stu-id="008ab-131">Online and IFD only</span></span> |                                                                                                                  <span data-ttu-id="008ab-132">A callback URI for the current application.</span><span class="sxs-lookup"><span data-stu-id="008ab-132">A callback URI for the current application.</span></span>                                                                                                                  |

 <span data-ttu-id="008ab-133">For more information on obtaining a client ID and a redirection URL for an application, see [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](../walkthrough-register-dynamics-365-app-azure-active-directory.md) for use with [!INCLUDE[pn_dyn_365_online](../../includes/pn-crm-online.md)] apps and                 [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Active Directory](../walkthrough-register-app-active-directory.md) for use with [!INCLUDE[pn_dyn_365_op](../../includes/pn-dyn-365-op.md)] using Internet-facing deployment (IFD).</span><span class="sxs-lookup"><span data-stu-id="008ab-133">For more information on obtaining a client ID and a redirection URL for an application, see [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](../walkthrough-register-dynamics-365-app-azure-active-directory.md) for use with [!INCLUDE[pn_dyn_365_online](../../includes/pn-crm-online.md)] apps and                 [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Active Directory](../walkthrough-register-app-active-directory.md) for use with [!INCLUDE[pn_dyn_365_op](../../includes/pn-dyn-365-op.md)] using Internet-facing deployment (IFD).</span></span>  

<a name="bkmk_FileConfigconnectionsettings"></a>

### <a name="fileconfiguration-connection-settings"></a><span data-ttu-id="008ab-134">FileConfiguration connection settings</span><span class="sxs-lookup"><span data-stu-id="008ab-134">FileConfiguration connection settings</span></span>

 <span data-ttu-id="008ab-135">Most of the Dynamics 365 for Customer Engagement Web API samples use the derived class, `FileConfiguration`, to extract the connection data from the application configuration file, App.config. This file has several application settings that apply to the different Dynamics 365 for Customer Engagementapps Server deployment modes.</span><span class="sxs-lookup"><span data-stu-id="008ab-135">Most of the Dynamics 365 for Customer Engagement Web API samples use the derived class, `FileConfiguration`, to extract the connection data from the application configuration file, App.config. This file has several application settings that apply to the different Dynamics 365 for Customer Engagementapps Server deployment modes.</span></span> <span data-ttu-id="008ab-136">The `connectionString` setting contains the service URL and user name.</span><span class="sxs-lookup"><span data-stu-id="008ab-136">The `connectionString` setting contains the service URL and user name.</span></span> <span data-ttu-id="008ab-137">Additionally, the `ClientId`and `RedirectUrl` settings are required for online or Internet-facing deployments (IFD).</span><span class="sxs-lookup"><span data-stu-id="008ab-137">Additionally, the `ClientId`and `RedirectUrl` settings are required for online or Internet-facing deployments (IFD).</span></span> <span data-ttu-id="008ab-138">The following lines, excerpted from the default App.config file provided with most of the Web API samples, contain this connection data as placeholder values.</span><span class="sxs-lookup"><span data-stu-id="008ab-138">The following lines, excerpted from the default App.config file provided with most of the Web API samples, contain this connection data as placeholder values.</span></span> <span data-ttu-id="008ab-139">You must replace these placeholders with values specific to the current user, your Dynamics 365 for Customer Engagement server, and your client application.</span><span class="sxs-lookup"><span data-stu-id="008ab-139">You must replace these placeholders with values specific to the current user, your Dynamics 365 for Customer Engagement server, and your client application.</span></span>  

```xml  
<connectionStrings> 
    <add name="default" connectionString="Url=http://myserver/myorg/; Username=name; Password=password; Domain=domain" /> 
</connectionStrings> 
<appSettings> 
    <add key="ClientId" value="e5cf0024-a66a-4f16-85ce-99ba97a24bb2" /> 
    <add key="RedirectUrl" value="http://localhost/SdkSample" /> 
</appSettings>  
```  

 <span data-ttu-id="008ab-140">The full contents of the default configuration file are provided in [Default configuration file listing](#bkmk_Defaultconfigurationfilelisting).</span><span class="sxs-lookup"><span data-stu-id="008ab-140">The full contents of the default configuration file are provided in [Default configuration file listing](#bkmk_Defaultconfigurationfilelisting).</span></span>  

<a name="bkmk_Classhierarchyandmembers"></a>

## <a name="class-hierarchy-and-members"></a><span data-ttu-id="008ab-141">Class hierarchy and members</span><span class="sxs-lookup"><span data-stu-id="008ab-141">Class hierarchy and members</span></span>

 <span data-ttu-id="008ab-142">The following diagram shows the public members of the configuration class hierarchy.</span><span class="sxs-lookup"><span data-stu-id="008ab-142">The following diagram shows the public members of the configuration class hierarchy.</span></span>  

 <span data-ttu-id="008ab-143">![Dynamics 365 for Customer Engagement Web API Helper Library-Configuration Class Diagram](../media/web-api-helper-library-configuration-class-diagram.png "Dynamics 365 for Customer Engagement Web API Helper Library-Configuration Class Diagram")</span><span class="sxs-lookup"><span data-stu-id="008ab-143">![Dynamics 365 for Customer Engagement Web API Helper Library-Configuration Class Diagram](../media/web-api-helper-library-configuration-class-diagram.png "Dynamics 365 for Customer Engagement Web API Helper Library-Configuration Class Diagram")</span></span>  

 <span data-ttu-id="008ab-144">**Configuration class**</span><span class="sxs-lookup"><span data-stu-id="008ab-144">**Configuration class**</span></span>  

 <span data-ttu-id="008ab-145">*Properties:*</span><span class="sxs-lookup"><span data-stu-id="008ab-145">*Properties:*</span></span>  

 <span data-ttu-id="008ab-146">All properties map directly to the corresponding connection data detailed in the previous section.</span><span class="sxs-lookup"><span data-stu-id="008ab-146">All properties map directly to the corresponding connection data detailed in the previous section.</span></span>  

 <span data-ttu-id="008ab-147">*Methods*:</span><span class="sxs-lookup"><span data-stu-id="008ab-147">*Methods*:</span></span>  

 <span data-ttu-id="008ab-148">The default constructor leaves all properties uninitialized (null).</span><span class="sxs-lookup"><span data-stu-id="008ab-148">The default constructor leaves all properties uninitialized (null).</span></span>  

 <span data-ttu-id="008ab-149">**FileConfiguration Class**</span><span class="sxs-lookup"><span data-stu-id="008ab-149">**FileConfiguration Class**</span></span>  

 <span data-ttu-id="008ab-150">*Properties:*</span><span class="sxs-lookup"><span data-stu-id="008ab-150">*Properties:*</span></span>  

 <span data-ttu-id="008ab-151">`Name`is the name of the connection string setting entry.</span><span class="sxs-lookup"><span data-stu-id="008ab-151">`Name`is the name of the connection string setting entry.</span></span>  

 <span data-ttu-id="008ab-152">`PathToConfig`is the full or relative path to the application configuration file.</span><span class="sxs-lookup"><span data-stu-id="008ab-152">`PathToConfig`is the full or relative path to the application configuration file.</span></span>  

 <span data-ttu-id="008ab-153">*Methods*:</span><span class="sxs-lookup"><span data-stu-id="008ab-153">*Methods*:</span></span>  

 <span data-ttu-id="008ab-154">The default constructor leaves all properties uninitialized (null).</span><span class="sxs-lookup"><span data-stu-id="008ab-154">The default constructor leaves all properties uninitialized (null).</span></span>  

 <span data-ttu-id="008ab-155">The non-default constructor takes a single string parameter that specifies the named connection string.</span><span class="sxs-lookup"><span data-stu-id="008ab-155">The non-default constructor takes a single string parameter that specifies the named connection string.</span></span> <span data-ttu-id="008ab-156">An empty string or null string value results in the first connection string entry being used.</span><span class="sxs-lookup"><span data-stu-id="008ab-156">An empty string or null string value results in the first connection string entry being used.</span></span>  

 <span data-ttu-id="008ab-157">The `Load`method opens, reads, and parses the specified configuration file.</span><span class="sxs-lookup"><span data-stu-id="008ab-157">The `Load`method opens, reads, and parses the specified configuration file.</span></span> <span data-ttu-id="008ab-158">It is used by the non-default constructor.</span><span class="sxs-lookup"><span data-stu-id="008ab-158">It is used by the non-default constructor.</span></span>  

<a name="bkmk_usage"></a>

## <a name="usage"></a><span data-ttu-id="008ab-159">Sử dụng</span><span class="sxs-lookup"><span data-stu-id="008ab-159">Usage</span></span>

 <span data-ttu-id="008ab-160">The `FileConfiguration` and `Authentication` classes are designed to be used in tandem to read the connection information in App.config and to then establish a secure connection to the target Dynamics 365 for Customer Engagement service.</span><span class="sxs-lookup"><span data-stu-id="008ab-160">The `FileConfiguration` and `Authentication` classes are designed to be used in tandem to read the connection information in App.config and to then establish a secure connection to the target Dynamics 365 for Customer Engagement service.</span></span> <span data-ttu-id="008ab-161">This can be implemented with the following statements.</span><span class="sxs-lookup"><span data-stu-id="008ab-161">This can be implemented with the following statements.</span></span>  

```csharp  
FileConfiguration config = new FileConfiguration(null); Authentication auth = new Authentication(config); httpClient = new HttpClient(auth.ClientHandler, true);  
```  

 <span data-ttu-id="008ab-162">The non-default constructor in the `Configuration` class enables the use of a named connection string, for example:</span><span class="sxs-lookup"><span data-stu-id="008ab-162">The non-default constructor in the `Configuration` class enables the use of a named connection string, for example:</span></span>  

```csharp  
Configuration config = new FileConfiguration(“TestServer”);  
```  

 <span data-ttu-id="008ab-163">If a null or empty connection string name is passed to the `FileConfiguration` class constructor, the first connection string from the top of the configuration file is used.</span><span class="sxs-lookup"><span data-stu-id="008ab-163">If a null or empty connection string name is passed to the `FileConfiguration` class constructor, the first connection string from the top of the configuration file is used.</span></span>  

 <span data-ttu-id="008ab-164">Furthermore, the SDK samples support a run-time command parameter, representing the name of the desired connection string, to be passed to the constructor.</span><span class="sxs-lookup"><span data-stu-id="008ab-164">Furthermore, the SDK samples support a run-time command parameter, representing the name of the desired connection string, to be passed to the constructor.</span></span> <span data-ttu-id="008ab-165">This option is implemented by the following code:</span><span class="sxs-lookup"><span data-stu-id="008ab-165">This option is implemented by the following code:</span></span>  

```csharp  
if (cmdargs.Length > 0) { config = new FileConfiguration(cmdargs[0]); } else { config = new FileConfiguration(null); }  
```  

<a name="bkmk_Configurationsearchorder"></a>

### <a name="configuration-search-order"></a><span data-ttu-id="008ab-166">Configuration search order</span><span class="sxs-lookup"><span data-stu-id="008ab-166">Configuration search order</span></span>

 <span data-ttu-id="008ab-167">Whether using the default or a custom application configuration file, the optional `AlternateConfig` application setting can be supplied within the file to specify an alternative configuration file.</span><span class="sxs-lookup"><span data-stu-id="008ab-167">Whether using the default or a custom application configuration file, the optional `AlternateConfig` application setting can be supplied within the file to specify an alternative configuration file.</span></span> <span data-ttu-id="008ab-168">If this file exists, its connection settings will be used instead.</span><span class="sxs-lookup"><span data-stu-id="008ab-168">If this file exists, its connection settings will be used instead.</span></span>  

```xml  
<add key="AlternateConfig" value="C:\Temp\crmsample.exe.config"/>  
```  

 <span data-ttu-id="008ab-169">One common use of this setting is to supply a global configuration file to be shared among multiple applications, instead of editing each application’s App.config file.</span><span class="sxs-lookup"><span data-stu-id="008ab-169">One common use of this setting is to supply a global configuration file to be shared among multiple applications, instead of editing each application’s App.config file.</span></span> <span data-ttu-id="008ab-170">This is especially useful for sharing configuration and registration information among                         multiple applications moving through the development and testing stages.</span><span class="sxs-lookup"><span data-stu-id="008ab-170">This is especially useful for sharing configuration and registration information among                         multiple applications moving through the development and testing stages.</span></span> <span data-ttu-id="008ab-171">Then only for production would you provide unique configuration and registration information for each application.</span><span class="sxs-lookup"><span data-stu-id="008ab-171">Then only for production would you provide unique configuration and registration information for each application.</span></span>  

<a name="bkmk_Defaultconfigurationfilelisting"></a>

## <a name="default-configuration-file-listing"></a><span data-ttu-id="008ab-172">Default configuration file listing</span><span class="sxs-lookup"><span data-stu-id="008ab-172">Default configuration file listing</span></span>

 <span data-ttu-id="008ab-173">The file App.config, provided with most Dynamics 365 for Customer Engagement Web API samples, contains placeholder connection values that must be edited by the developer or site administrator.</span><span class="sxs-lookup"><span data-stu-id="008ab-173">The file App.config, provided with most Dynamics 365 for Customer Engagement Web API samples, contains placeholder connection values that must be edited by the developer or site administrator.</span></span>  

```xml  
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
   <startup>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5.2" />
   </startup>
   <connectionStrings>
      <clear />
      <!-- When providing a password, make  
                sure to set the app.config file's security so that only you can read it. -->
      <add name="default" connectionString="Url=http://myserver/myorg/; Username=name; Password=password; Domain=domain" />
      <add name="CrmOnline" connectionString="Url=https://mydomain.crm.dynamics.com/;                   Username=someone@mydomain.onmicrosoft.com; Password=password" />
   </connectionStrings>
   <appSettings>
      <!--For information on how to register an app and obtain the ClientId and RedirectUrl values see https://msdn.microsoft.com/dynamics/crm/mt149065  
                -->
      <!--Active Directory application registration. -->
      <!--These are dummy values and should be replaced with your actual app registration values.-->
      <add key="ClientId" value="e5cf0024-a66a-4f16-85ce-99ba97a24bb2" />
      <add key="RedirectUrl" value="http://localhost/SdkSample" />
      <!-- Use an alternate configuration file for connection string and setting values. This optional setting enables use of an app.config file shared among multiple applications. If the specified file does not exist,  
                this setting is ignored.-->
      <add key="AlternateConfig" value="C:\Temp\crmsample.exe.config" />
   </appSettings>
</configuration>  
```  

## <a name="class-listing"></a><span data-ttu-id="008ab-174">Class listing</span><span class="sxs-lookup"><span data-stu-id="008ab-174">Class listing</span></span>

 <span data-ttu-id="008ab-175">The most current source for this class is found in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="008ab-175">The most current source for this class is found in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode) NuGet package.</span></span>  

```csharp  
using System;
using System.IO;
using System.Security;
using System.Configuration;

namespace Microsoft.Crm.Sdk.Samples.HelperCode
{
    /// <summary>
    /// An application configuration containing user logon, application, and web service information
    /// as required for CRM Web API authentication.
    /// </summary>
    public class Configuration
    {
        #region Properties
        /// <summary>
        /// The root address of the Dynamics CRM service.
        /// </summary>
        /// <example>https://myorg.crm.dynamics.com</example>
        public string ServiceUrl { get; set; }

        /// <summary>
        /// The redirect address provided when the application was registered in Microsoft Azure
        /// Active Directory or AD FS.
        /// </summary>
        /// <remarks>Required only with a web service configured for OAuth authentication.</remarks>
        /// <seealso cref="https://msdn.microsoft.com/library/dn531010.aspx#bkmk_redirect"/>
        public string RedirectUrl { get; set; }

        /// <summary>
        /// The client ID that was generated when the application was registered in Microsoft Azure
        /// Active Directory or AD FS.
        /// </summary>
        /// <remarks>Required only with a web service configured for OAuth authentication.</remarks>
        public string ClientId { get; set; }

        /// <summary>
        /// The user name of the logged on user or null.
        /// </summary>
        public string Username { get; set; }

        /// <summary>
        ///  The password of the logged on user or null.
        /// </summary>
        public SecureString Password { get; set; }

        /// <summary>
        ///  The domain of the logged on user account or null.
        /// </summary>
        /// <remarks>Required only with a web service configured for Active Directory authentication.</remarks>
        public string Domain { get; set; }

        #endregion Properties

        #region Constructors

        /// <summary>
        /// Constructs a configuration object.
        /// </summary>
        public Configuration() { }

        #endregion Constructors
    }

    /// <summary>
    /// A configuration that is persisted to file storage.
    /// </summary>
    /// <remarks>This implementation defaults to using an app.config file. However, you
    /// can derive a subclass and override the virtual methods to make use of other
    /// file formats.
    /// 
    /// One set of application registration settings and multiple named connection strings are supported.</remarks>
    public class FileConfiguration : Configuration
    {
        #region Properties
        /// <summary>
        /// The full or relative path to the application's configuration file.
        /// </summary>
        /// <remarks>The file name is in the format <appname>.exe.config.</appname></remarks>
        public string PathToConfig { get; set; }

        /// <summary>
        /// The name of the connection.
        /// </summary>
        public string Name { get; set; }

        #endregion Properties

        #region Constructors
        /// <summary>
        /// Constructs a file configuration.
        /// </summary>
        public FileConfiguration()
            : base()
        { }

        /// <summary>
        /// Loads a named connection string and application settings from persistent file storage.
        /// The configuration file must have the same name as the application and be located in the 
        /// run-time folder.
        /// </summary>
        /// <param name="name">The name of the target connection string. An empty or null string value 
        /// results in the first named configuration being used.</param>
        /// <remarks>The app.config file must exist in the run-time folder and have the name
        /// <appname>.exe.config. To specify an app.config file path, use the Load() method.</remarks>
        public FileConfiguration(string name)
            : base()
        {
            var path = System.IO.Path.Combine(Directory.GetCurrentDirectory(), Environment.GetCommandLineArgs()[0]);

            Load(name, String.Concat(path, ".config"));
        }

        #endregion Constructors

        #region Methods
        /// <summary>
        /// Loads server connection information and application settings from persistent file storage.
        /// </summary>
        /// <remarks>A setting named OverrideConfig can optionally be added. If a config file that this setting
        /// refers to exists, that config file is read instead of the config file specified in the path parameter.
        /// This allows for an alternate config file, for example a global config file shared by multiple applications.
        /// </summary>
        /// <param name="connectionName">The name of the connection string in the configuration file to use. 
        /// Each CRM organization can have its own connection string. A value of null or String.Empty results
        /// in the first (top most) connection string being used.</param>
        /// <param name="path">The full or relative pathname of the configuration file.</param>
        public virtual void Load(string connectionName, string path)
        {
            // Check passed parameters.
            if (string.IsNullOrEmpty(path) || !System.IO.File.Exists(path))
                throw new ArgumentException("The specified app.config file path is invalid.", this.ToString());
            else
                PathToConfig = path;

            try
            {
                // Read the app.config file and obtain the app settings.
                System.Configuration.Configuration config = null;
                ExeConfigurationFileMap configFileMap = new ExeConfigurationFileMap();
                configFileMap.ExeConfigFilename = PathToConfig;
                config = ConfigurationManager.OpenMappedExeConfiguration(configFileMap, ConfigurationUserLevel.None);

                var appSettings = config.AppSettings.Settings;

                // If an alternate config file exists, load that configuration instead. Note the test
                // for redirectTo.Equals(path) to avoid an infinite loop.
                if (appSettings["AlternateConfig"] != null)
                {
                    var redirectTo = appSettings["AlternateConfig"].Value;
                    if (redirectTo != null && !redirectTo.Equals(path) && System.IO.File.Exists(redirectTo))
                    {
                        Load(connectionName, redirectTo);
                        return;
                    }
                }

                // Get the connection string.
                ConnectionStringSettings connection;
                if (string.IsNullOrEmpty(connectionName))
                {
                    // No connection string name specified, so use the first one in the file.
                    connection = config.ConnectionStrings.ConnectionStrings[0];
                    Name = connection.Name;
                }
                else
                {
                    connection = config.ConnectionStrings.ConnectionStrings[connectionName];
                    Name = connectionName;
                }

                // Get the connection string parameter values.
                if (connection != null)
                {
                    var parameters = connection.ConnectionString.Split(';');
                    foreach (string parameter in parameters)
                    {
                        var trimmedParameter = parameter.Trim();
                        if (trimmedParameter.StartsWith("Url="))
                            ServiceUrl = parameter.Replace("Url=", String.Empty).TrimStart(' ');

                        if (trimmedParameter.StartsWith("Username="))
                            Username = parameters[1].Replace("Username=", String.Empty).TrimStart(' ');

                        if (trimmedParameter.StartsWith("Password="))
                        {
                            var password = parameters[2].Replace("Password=", String.Empty).TrimStart(' ');

                            Password = new SecureString();
                            foreach (char c in password) Password.AppendChar(c);
                        }
                        if (trimmedParameter.StartsWith("Domain="))
                            Domain = parameter.Replace("Domain=", String.Empty).TrimStart(' ');
                    }
                }
                else
                    throw new Exception("The specified connection string could not be found.");

                // Get the Azure Active Directory application registration settings.
                RedirectUrl = appSettings["RedirectUrl"]?.Value;
                ClientId = appSettings["ClientId"]?.Value;
            }
            catch (InvalidOperationException e)
            {
                throw new Exception("Required setting in app.config does not exist or is of the wrong type.", e);
            }
        }

        /// <summary>
        /// Save the current configuration to persistent file storage.
        /// </summary>
        /// <remarks>Any existing configuration is overwritten.</remarks>
        public virtual void Save()
        {
            throw new NotImplementedException();
        }

        /// <summary>
        /// Add a named connection string to persistent file storage.
        /// </summary>
        /// <remarks>A named connection string from the current configuration is added to an existing
        /// configuration file./remarks>
        public virtual void AddConnection()
        {
            throw new NotImplementedException();
        }

        #endregion Methods
    }
} 
```  

### <a name="see-also"></a><span data-ttu-id="008ab-176">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="008ab-176">See also</span></span>

 <span data-ttu-id="008ab-177">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="008ab-177">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span></span>  
 <span data-ttu-id="008ab-178">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="008ab-178">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span></span>  
 <span data-ttu-id="008ab-179">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="008ab-179">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span></span>  
 <span data-ttu-id="008ab-180">[Helper code: Authentication class](web-api-helper-code-authentication-class.md) </span><span class="sxs-lookup"><span data-stu-id="008ab-180">[Helper code: Authentication class](web-api-helper-code-authentication-class.md) </span></span>  
 <span data-ttu-id="008ab-181">[Helper code: CrmHttpResponseException class](web-api-helper-code-crmhttpresponseexception-class.md) </span><span class="sxs-lookup"><span data-stu-id="008ab-181">[Helper code: CrmHttpResponseException class](web-api-helper-code-crmhttpresponseexception-class.md) </span></span>  
 [<span data-ttu-id="008ab-182">SDK samples Helper code for Organization Service endpoint</span><span class="sxs-lookup"><span data-stu-id="008ab-182">SDK samples Helper code for Organization Service endpoint</span></span>](https://www.nuget.org/packages/Microsoft.CrmSdk.Samples.HelperCode-CS)  
