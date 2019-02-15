---
title: Web API Samples (C#) (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This topic provides a description of various Web API samples that are implemented using C#
ms.custom: ''
ms.date: 06/12/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 66e26684-819e-45f7-bec4-c250be4d6fed
caps.latest.revision: 14
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ee79677801fd3f8537b505c4c4e3eff57b69d0c2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386222"
---
# <a name="web-api-samples-c"></a><span data-ttu-id="f4cf5-103">Web API Samples (C#)</span><span class="sxs-lookup"><span data-stu-id="f4cf5-103">Web API Samples (C#)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="f4cf5-104">This topic provides information about the Web API samples implemented with C#.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-104">This topic provides information about the Web API samples implemented with C#.</span></span> <span data-ttu-id="f4cf5-105">While each sample focuses on a different aspect of the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API, they share similar characteristics and structure.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-105">While each sample focuses on a different aspect of the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API, they share similar characteristics and structure.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f4cf5-106">This implementation approach uses low-level object creation and explicit HTTP message calls.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-106">This implementation approach uses low-level object creation and explicit HTTP message calls.</span></span> <span data-ttu-id="f4cf5-107">This approach allows for control and demonstration  of the low level object properties which control the behavior of the Web API.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-107">This approach allows for control and demonstration  of the low level object properties which control the behavior of the Web API.</span></span> <span data-ttu-id="f4cf5-108">This is intended to help you understand the inner workings  but doesn't necessarily represent an approach which will provide the best developer productivity experience.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-108">This is intended to help you understand the inner workings  but doesn't necessarily represent an approach which will provide the best developer productivity experience.</span></span>  
>   
>  <span data-ttu-id="f4cf5-109">In contrast, higher-level libraries, such as the [OData Library](https://msdn.microsoft.com/library/hh525392\(v=vs.103\).aspx), abstract away much of this low-level client logic.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-109">In contrast, higher-level libraries, such as the [OData Library](https://msdn.microsoft.com/library/hh525392\(v=vs.103\).aspx), abstract away much of this low-level client logic.</span></span>  <span data-ttu-id="f4cf5-110">The [OData T4 Template](https://blogs.msdn.microsoft.com/odatateam/2012/07/02/trying-out-the-prerelease-odata-client-t4-template/) can optionally be used in conjunction with the OData Library to auto-generate client entity classes.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-110">The [OData T4 Template](https://blogs.msdn.microsoft.com/odatateam/2012/07/02/trying-out-the-prerelease-odata-client-t4-template/) can optionally be used in conjunction with the OData Library to auto-generate client entity classes.</span></span>  

<a name="bkmk_prerequisites"></a>   
## <a name="prerequisites"></a><span data-ttu-id="f4cf5-111">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="f4cf5-111">Prerequisites</span></span>  
 <span data-ttu-id="f4cf5-112">The following is required to build and run the Dynamics 365 for Customer Engagement Web API C# samples :</span><span class="sxs-lookup"><span data-stu-id="f4cf5-112">The following is required to build and run the Dynamics 365 for Customer Engagement Web API C# samples :</span></span>  
  
- <span data-ttu-id="f4cf5-113">A version of Microsoft Visual Studio 2015 or later.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-113">A version of Microsoft Visual Studio 2015 or later.</span></span>  <span data-ttu-id="f4cf5-114">A free version, [Visual Studio Community](https://www.visualstudio.com/products/visual-studio-community-vs.aspx), is available for download [here](https://www.visualstudio.com/downloads/download-visual-studio-vs.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-114">A free version, [Visual Studio Community](https://www.visualstudio.com/products/visual-studio-community-vs.aspx), is available for download [here](https://www.visualstudio.com/downloads/download-visual-studio-vs.aspx).</span></span>  
  
- <span data-ttu-id="f4cf5-115">An Internet connection to download and update the referenced NuGet packages.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-115">An Internet connection to download and update the referenced NuGet packages.</span></span>  
  
- <span data-ttu-id="f4cf5-116">Access to  Dynamics 365 for Customer Engagement apps Online or on-premises (or later).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-116">Access to  Dynamics 365 for Customer Engagement apps Online or on-premises (or later).</span></span> <span data-ttu-id="f4cf5-117">For all Dynamics 365 for Customer Engagement apps installation types, a user account with privileges to perform CRUD operations is required.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-117">For all Dynamics 365 for Customer Engagement apps installation types, a user account with privileges to perform CRUD operations is required.</span></span>  
  
- <span data-ttu-id="f4cf5-118">In order to run samples against [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you must register your application with Azure Active Directory to obtain a client ID and redirect URL.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-118">In order to run samples against [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps, you must register your application with Azure Active Directory to obtain a client ID and redirect URL.</span></span> <span data-ttu-id="f4cf5-119">For more information, see [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](../walkthrough-register-dynamics-365-app-azure-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-119">For more information, see [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](../walkthrough-register-dynamics-365-app-azure-active-directory.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="f4cf5-120">These samples require version 2.x of assembly [Microsoft.IdentityModel.Client.ActiveDirectory](https://docs.microsoft.com/en-us/dotnet/api/microsoft.identitymodel.clients.activedirectory?view=azure-dotnet) for OAuth based authentication with [!INCLUDE[](../../includes/pn-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-120">These samples require version 2.x of assembly [Microsoft.IdentityModel.Client.ActiveDirectory](https://docs.microsoft.com/en-us/dotnet/api/microsoft.identitymodel.clients.activedirectory?view=azure-dotnet) for OAuth based authentication with [!INCLUDE[](../../includes/pn-crm-online.md)] apps.</span></span>
  
<a name="bkmk_webApiSamplesListing"></a>   
## <a name="web-api-samples-listing-c"></a><span data-ttu-id="f4cf5-121">Web API samples listing (C#)</span><span class="sxs-lookup"><span data-stu-id="f4cf5-121">Web API samples listing (C#)</span></span>  
 <span data-ttu-id="f4cf5-122">The following table lists the samples implemented in C#.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-122">The following table lists the samples implemented in C#.</span></span>  <span data-ttu-id="f4cf5-123">Each sample is described in a more general manner in a corresponding sample group topic that focuses on the HTTP request and response messages, as detailed in the topic [Web API Samples](web-api-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-123">Each sample is described in a more general manner in a corresponding sample group topic that focuses on the HTTP request and response messages, as detailed in the topic [Web API Samples](web-api-samples.md).</span></span>  
  
|<span data-ttu-id="f4cf5-124">Sample</span><span class="sxs-lookup"><span data-stu-id="f4cf5-124">Sample</span></span>|<span data-ttu-id="f4cf5-125">Sample Group</span><span class="sxs-lookup"><span data-stu-id="f4cf5-125">Sample Group</span></span>|<span data-ttu-id="f4cf5-126">Mô tả</span><span class="sxs-lookup"><span data-stu-id="f4cf5-126">Description</span></span>|  
|------------|------------------|-----------------|  
|[<span data-ttu-id="f4cf5-127">Web API Basic Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="f4cf5-127">Web API Basic Operations Sample (C#)</span></span>](web-api-basic-operations-sample-csharp.md)|[<span data-ttu-id="f4cf5-128">Web API Basic Operations Sample</span><span class="sxs-lookup"><span data-stu-id="f4cf5-128">Web API Basic Operations Sample</span></span>](web-api-basic-operations-sample.md)|<span data-ttu-id="f4cf5-129">Demonstrates how to create, retrieve, update, delete, associate and disassociate Dynamics 365 for Customer Engagement apps entity records.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-129">Demonstrates how to create, retrieve, update, delete, associate and disassociate Dynamics 365 for Customer Engagement apps entity records.</span></span>|  
|[<span data-ttu-id="f4cf5-130">Web API Query Data Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="f4cf5-130">Web API Query Data Sample (C#)</span></span>](web-api-query-data-sample-csharp.md)|[<span data-ttu-id="f4cf5-131">Web API Query Data Sample</span><span class="sxs-lookup"><span data-stu-id="f4cf5-131">Web API Query Data Sample</span></span>](web-api-query-data-sample.md)|<span data-ttu-id="f4cf5-132">Demonstrates how to use OData v4 query syntax and functions as well as Dynamics 365 for Customer Engagement apps query functions.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-132">Demonstrates how to use OData v4 query syntax and functions as well as Dynamics 365 for Customer Engagement apps query functions.</span></span> <span data-ttu-id="f4cf5-133">Includes examples of working with pre-defined queries and using FetchXML to perform queries.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-133">Includes examples of working with pre-defined queries and using FetchXML to perform queries.</span></span>|  
|[<span data-ttu-id="f4cf5-134">Web API Conditional Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="f4cf5-134">Web API Conditional Operations Sample (C#)</span></span>](web-api-conditional-operations-sample-csharp.md)|[<span data-ttu-id="f4cf5-135">Web API Conditional Operations Sample</span><span class="sxs-lookup"><span data-stu-id="f4cf5-135">Web API Conditional Operations Sample</span></span>](web-api-conditional-operations-sample.md)|<span data-ttu-id="f4cf5-136">Demonstrates how to perform conditional operations you specify with ETag criteria.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-136">Demonstrates how to perform conditional operations you specify with ETag criteria.</span></span>|  
|[<span data-ttu-id="f4cf5-137">Web API Functions and Actions Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="f4cf5-137">Web API Functions and Actions Sample (C#)</span></span>](web-api-functions-actions-sample-csharp.md)|[<span data-ttu-id="f4cf5-138">Web API Functions and Actions Sample</span><span class="sxs-lookup"><span data-stu-id="f4cf5-138">Web API Functions and Actions Sample</span></span>](web-api-functions-actions-sample.md)|<span data-ttu-id="f4cf5-139">Demonstrates how to use bound and unbound functions and actions, including custom actions.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-139">Demonstrates how to use bound and unbound functions and actions, including custom actions.</span></span>|  
  
<a name="bkmk_howDownloadRun"></a>   
## <a name="how-to-download-and-run-the-samples"></a><span data-ttu-id="f4cf5-140">How to download and run the samples</span><span class="sxs-lookup"><span data-stu-id="f4cf5-140">How to download and run the samples</span></span>  
 <span data-ttu-id="f4cf5-141">The source code for each sample is available on [MSDN Code Gallery](https://code.msdn.microsoft.com/site/search?f%5b0%5d.type=user&f%5b0%5d.value=microsoft%20dynamics%20crm%20sdk%20documentation%20team).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-141">The source code for each sample is available on [MSDN Code Gallery](https://code.msdn.microsoft.com/site/search?f%5b0%5d.type=user&f%5b0%5d.value=microsoft%20dynamics%20crm%20sdk%20documentation%20team).</span></span> <span data-ttu-id="f4cf5-142">The link to download each sample is included in the sample topic.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-142">The link to download each sample is included in the sample topic.</span></span> <span data-ttu-id="f4cf5-143">The sample download is a compressed .zip file, which contains the Visual Studio 2015 solution files for the sample.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-143">The sample download is a compressed .zip file, which contains the Visual Studio 2015 solution files for the sample.</span></span> <span data-ttu-id="f4cf5-144">For more information, see the **Run this sample** section in each sample topic.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-144">For more information, see the **Run this sample** section in each sample topic.</span></span>  
  
<a name="bkmk_commonElements"></a>   
## <a name="common-elements-found-in-each-sample"></a><span data-ttu-id="f4cf5-145">Common elements found in each sample</span><span class="sxs-lookup"><span data-stu-id="f4cf5-145">Common elements found in each sample</span></span>  
 <span data-ttu-id="f4cf5-146">Most of the samples have a similar structure and contain common methods and resources, typically to provide the basic infrastructure for a Web API C# program.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-146">Most of the samples have a similar structure and contain common methods and resources, typically to provide the basic infrastructure for a Web API C# program.</span></span>  
  
 <span data-ttu-id="f4cf5-147">Many of these common elements are also present when creating a new solution that will access the Dynamics 365 for Customer Engagement Web API.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-147">Many of these common elements are also present when creating a new solution that will access the Dynamics 365 for Customer Engagement Web API.</span></span> <span data-ttu-id="f4cf5-148">For more information, see [Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-148">For more information, see [Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md).</span></span>  
  
### <a name="utilized-libraries-and-frameworks"></a><span data-ttu-id="f4cf5-149">Utilized libraries and frameworks</span><span class="sxs-lookup"><span data-stu-id="f4cf5-149">Utilized libraries and frameworks</span></span>  
 <span data-ttu-id="f4cf5-150">This C# implementation depends upon the following helper code for HTTP communication, application configuration, authentication, error handling, and JSON serialization.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-150">This C# implementation depends upon the following helper code for HTTP communication, application configuration, authentication, error handling, and JSON serialization.</span></span>  
  
-   <span data-ttu-id="f4cf5-151">The standard .NET Framework HTTP messaging classes that are contained in the  [System.Net.Http namespace](https://msdn.microsoft.com/library/system.net.http\(v=vs.110\).aspx), particularly [HttpClient](https://docs.microsoft.com/en-us/dotnet/api/system.net.http.httpclient?view=netframework-4.7.1), [HttpRequestMessage](https://docs.microsoft.com/en-us/dotnet/api/system.net.http.httprequestmessage?view=netframework-4.7.1), and [HttpResponseMessage](https://msdn.microsoft.com/library/system.net.http.httpresponsemessage\(v=vs.110\).aspx), are used for HTTP messaging.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-151">The standard .NET Framework HTTP messaging classes that are contained in the  [System.Net.Http namespace](https://msdn.microsoft.com/library/system.net.http\(v=vs.110\).aspx), particularly [HttpClient](https://docs.microsoft.com/en-us/dotnet/api/system.net.http.httpclient?view=netframework-4.7.1), [HttpRequestMessage](https://docs.microsoft.com/en-us/dotnet/api/system.net.http.httprequestmessage?view=netframework-4.7.1), and [HttpResponseMessage](https://msdn.microsoft.com/library/system.net.http.httpresponsemessage\(v=vs.110\).aspx), are used for HTTP messaging.</span></span>  
  
-   <span data-ttu-id="f4cf5-152">The Dynamics 365 for Customer Engagement Web API Helper Library is used to read the application configuration file, authenticate with the Dynamics 365 for Customer Engagement server, and assist in operation error handling.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-152">The Dynamics 365 for Customer Engagement Web API Helper Library is used to read the application configuration file, authenticate with the Dynamics 365 for Customer Engagement server, and assist in operation error handling.</span></span>  <span data-ttu-id="f4cf5-153">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-153">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span></span>  
  
-   <span data-ttu-id="f4cf5-154">The Newtonsoft [Json.NET](http://www.newtonsoft.com/json) library supports the JSON data format.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-154">The Newtonsoft [Json.NET](http://www.newtonsoft.com/json) library supports the JSON data format.</span></span>  
  
#### <a name="jsonnet-library"></a><span data-ttu-id="f4cf5-155">Json.NET Library</span><span class="sxs-lookup"><span data-stu-id="f4cf5-155">Json.NET Library</span></span>  
 <span data-ttu-id="f4cf5-156">Because C# and most other managed languages do not natively support the JSON data format, the best current approach is to use a library for this functionality.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-156">Because C# and most other managed languages do not natively support the JSON data format, the best current approach is to use a library for this functionality.</span></span> <span data-ttu-id="f4cf5-157">For more information, see [An Introduction to JavaScript Object Notation (JSON) in JavaScript and .NET](https://msdn.microsoft.com/library/bb299886.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-157">For more information, see [An Introduction to JavaScript Object Notation (JSON) in JavaScript and .NET](https://msdn.microsoft.com/library/bb299886.aspx).</span></span> <span data-ttu-id="f4cf5-158">Json.NET is a popular choice for .NET projects.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-158">Json.NET is a popular choice for .NET projects.</span></span> <span data-ttu-id="f4cf5-159">It provides a robust, performant, open-source ([MIT licensed](https://opensource.org/licenses/MIT)) framework for serializing, converting, parsing, querying, and formatting JSON data.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-159">It provides a robust, performant, open-source ([MIT licensed](https://opensource.org/licenses/MIT)) framework for serializing, converting, parsing, querying, and formatting JSON data.</span></span> <span data-ttu-id="f4cf5-160">For more information, see the [Json.NET documentation](http://www.newtonsoft.com/json/help/html/Introduction.htm).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-160">For more information, see the [Json.NET documentation](http://www.newtonsoft.com/json/help/html/Introduction.htm).</span></span>  
  
 <span data-ttu-id="f4cf5-161">In the C# samples, this library is primarily used to serialize data between .NET objects and HTTP message bodies.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-161">In the C# samples, this library is primarily used to serialize data between .NET objects and HTTP message bodies.</span></span> <span data-ttu-id="f4cf5-162">Although the library provides several methods to accomplish this task, the approach used by the samples is to create individual [JObject](http://www.newtonsoft.com/json/help/html/T_Newtonsoft_Json_Linq_JObject.htm) instances to represent Dynamics 365 for Customer Engagement apps entity instances (records).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-162">Although the library provides several methods to accomplish this task, the approach used by the samples is to create individual [JObject](http://www.newtonsoft.com/json/help/html/T_Newtonsoft_Json_Linq_JObject.htm) instances to represent Dynamics 365 for Customer Engagement apps entity instances (records).</span></span>  <span data-ttu-id="f4cf5-163">For example, the following code creates the variable `contact1` that represents a Dynamics 365 for Customer Engagement apps <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" /> instance, then supplies values for a select set of properties for this type.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-163">For example, the following code creates the variable `contact1` that represents a Dynamics 365 for Customer Engagement apps <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" /> instance, then supplies values for a select set of properties for this type.</span></span>  
  
```csharp  
  
JObject contact1 = new JObject();  
contact1.Add("firstname", "Peter");  
contact1.Add("lastname", "Cambel");  
contact1.Add("annualincome", 80000);  
contact1["jobtitle"] = "Junior Developer";  
  
```  
  
 <span data-ttu-id="f4cf5-164">The use of the bracket notation in the last statement is equivalent to the [Add](http://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_Linq_JObject_Add.htm) method.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-164">The use of the bracket notation in the last statement is equivalent to the [Add](http://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_Linq_JObject_Add.htm) method.</span></span> <span data-ttu-id="f4cf5-165">This instantiation could also be accomplished through the use of the [Parse](http://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_Linq_JObject_Parse.htm) static method:</span><span class="sxs-lookup"><span data-stu-id="f4cf5-165">This instantiation could also be accomplished through the use of the [Parse](http://www.newtonsoft.com/json/help/html/M_Newtonsoft_Json_Linq_JObject_Parse.htm) static method:</span></span>  
  
```csharp  
  
JObject contact1 = JObject.Parse(@"{firstname: 'Peter', lastname: 'Cambel', "  
+ @"annualincome: 80000, jobtitle: 'Junior Developer'}");  
  
```  
  
 <span data-ttu-id="f4cf5-166">Because `JObject` represents a general JSON type, its use precludes much runtime type checking.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-166">Because `JObject` represents a general JSON type, its use precludes much runtime type checking.</span></span>  <span data-ttu-id="f4cf5-167">For example, while the following statement is syntactically valid, it will potentially lead to runtime errors because the <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" /> does not contain an `age` property.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-167">For example, while the following statement is syntactically valid, it will potentially lead to runtime errors because the <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" /> does not contain an `age` property.</span></span>  
  
 `contact1.Add("age", 37);    //Possible error--no age property exists in contact!`  
  
 <span data-ttu-id="f4cf5-168">Once the entity variable has been initialized, it can then be sent in a message body, with assistance from several System.Net.Http classes, for example:</span><span class="sxs-lookup"><span data-stu-id="f4cf5-168">Once the entity variable has been initialized, it can then be sent in a message body, with assistance from several System.Net.Http classes, for example:</span></span>  
  
```csharp  
  
HttpRequestMessage request = new HttpRequestMessage(HttpMethod.Post, "contacts");  
request.Content = new StringContent(contact1.ToString(), Encoding.UTF8, "application/json");  
HttpResponseMessage response = await httpClient.SendAsync(request1);  
  
```  
  
 <span data-ttu-id="f4cf5-169">You can also create JObject instances by deserializing entity instances during retrieval operations, for example:</span><span class="sxs-lookup"><span data-stu-id="f4cf5-169">You can also create JObject instances by deserializing entity instances during retrieval operations, for example:</span></span>  
  
```csharp  
  
//contact2Uri contains a reference to an existing CRM contact instance.  
string queryOptions = "?$select=fullname,annualincome,jobtitle,description";  
HttpResponseMessage response = await httpClient.GetAsync(contact2Uri + queryOptions);  
JObject contact2 = JsonConvert.DeserializeObject<JObject>(await response.Content.ReadAsStringAsync());  
  
```  
  
### <a name="response-success-and-error-handling"></a><span data-ttu-id="f4cf5-170">Response success and error handling</span><span class="sxs-lookup"><span data-stu-id="f4cf5-170">Response success and error handling</span></span>  
 <span data-ttu-id="f4cf5-171">In general, the samples take a straightforward approach to processing HTTP responses.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-171">In general, the samples take a straightforward approach to processing HTTP responses.</span></span> <span data-ttu-id="f4cf5-172">If the request succeeds, information about the operation is typically output to the console.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-172">If the request succeeds, information about the operation is typically output to the console.</span></span> <span data-ttu-id="f4cf5-173">If the response also carries a JSON payload or useful headers, this information is only processed upon success.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-173">If the response also carries a JSON payload or useful headers, this information is only processed upon success.</span></span> <span data-ttu-id="f4cf5-174">And lastly, if a Dynamics 365 for Customer Engagement apps entity was created, the `entityUris` collection is updated with the URI of that resource.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-174">And lastly, if a Dynamics 365 for Customer Engagement apps entity was created, the `entityUris` collection is updated with the URI of that resource.</span></span> <span data-ttu-id="f4cf5-175">The [DeleteRequiredRecords](#bkmk_deleteRequiredRecords) method uses this collection to optionally delete data created by the sample from your Dynamics 365 for Customer Engagement server.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-175">The [DeleteRequiredRecords](#bkmk_deleteRequiredRecords) method uses this collection to optionally delete data created by the sample from your Dynamics 365 for Customer Engagement server.</span></span>  
  
 <span data-ttu-id="f4cf5-176">If the request failed, the program outputs a contextual message about the operation that failed, and then it throws a custom exception of type `CrmHttpResponseException`.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-176">If the request failed, the program outputs a contextual message about the operation that failed, and then it throws a custom exception of type `CrmHttpResponseException`.</span></span> <span data-ttu-id="f4cf5-177">The exception-handler outputs more information about the exception and then control passes to a `finally` block that includes cleanup logic, again including a call to `DeleteRequiredRecords`.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-177">The exception-handler outputs more information about the exception and then control passes to a `finally` block that includes cleanup logic, again including a call to `DeleteRequiredRecords`.</span></span> <span data-ttu-id="f4cf5-178">The following code demonstrates this error-handling approach on a POST request to create a record.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-178">The following code demonstrates this error-handling approach on a POST request to create a record.</span></span>  
  
```csharp  
  
if (response.StatusCode == HttpStatusCode.NoContent)  //204  
{  
Console.WriteLine("POST succeeded, entity created!");  
//optionally process response message headers or body here, for example:  
entityUri = response.Headers.GetValues("OData-EntityId").FirstOrDefault();  
entityUris.Add(entityUri);  
}  
else  
{  
Console.WriteLine("Operation failed: {0}", response.ReasonPhrase);  
throw new CrmHttpResponseException(response.Content);  
}  
  
```  
  
 <span data-ttu-id="f4cf5-179">[HttpStatusCode](https://msdn.microsoft.com/library/hh435235.aspx).NoContent is equivalent to an HTTP status code 204, “No content”.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-179">[HttpStatusCode](https://msdn.microsoft.com/library/hh435235.aspx).NoContent is equivalent to an HTTP status code 204, “No content”.</span></span> <span data-ttu-id="f4cf5-180">Here, this status code indicates that the POST request succeeded.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-180">Here, this status code indicates that the POST request succeeded.</span></span> <span data-ttu-id="f4cf5-181">For more information, see [Compose HTTP requests and handle errors](https://msdn.microsoft.com/en-us/library/gg334391.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-181">For more information, see [Compose HTTP requests and handle errors](https://msdn.microsoft.com/en-us/library/gg334391.aspx).</span></span>  
  
### <a name="characteristics-and-methods"></a><span data-ttu-id="f4cf5-182">Characteristics and methods</span><span class="sxs-lookup"><span data-stu-id="f4cf5-182">Characteristics and methods</span></span>  
 <span data-ttu-id="f4cf5-183">Most of the samples have the same general architectural pattern, with the following characteristics:</span><span class="sxs-lookup"><span data-stu-id="f4cf5-183">Most of the samples have the same general architectural pattern, with the following characteristics:</span></span>  
  
-   <span data-ttu-id="f4cf5-184">All of the pertinent C# sample code is contained in the primary source file named `Program.cs`, which contains a single class with the same name as the sample project.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-184">All of the pertinent C# sample code is contained in the primary source file named `Program.cs`, which contains a single class with the same name as the sample project.</span></span>  
  
-   <span data-ttu-id="f4cf5-185">The sample classes, as well as the [Dynamics 365 for Customer Engagement Web API Helper Library](use-microsoft-dynamics-365-web-api-helper-library-csharp.md), is contained in the namespace `Microsoft.Crm.Sdk.Samples`.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-185">The sample classes, as well as the [Dynamics 365 for Customer Engagement Web API Helper Library](use-microsoft-dynamics-365-web-api-helper-library-csharp.md), is contained in the namespace `Microsoft.Crm.Sdk.Samples`.</span></span>  
  
-   <span data-ttu-id="f4cf5-186">The samples are liberally commented: summaries are provided at the class and method levels, and most key individual statements have associated same- or single-line comments.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-186">The samples are liberally commented: summaries are provided at the class and method levels, and most key individual statements have associated same- or single-line comments.</span></span>  <span data-ttu-id="f4cf5-187">Supplemental files, such as the application configuration file `App.config`, also often contain important comments.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-187">Supplemental files, such as the application configuration file `App.config`, also often contain important comments.</span></span>  
  
-   <span data-ttu-id="f4cf5-188">The primary sample class is typically structured to contain the following common set of methods: [Main](#bkmk_main), [ConnectToCRM](#bkmk_connectToCrm), [CreateRequiredRecords](#bkmk_createRequiredRecords), [RunAsync](#bkmk_runAsync), [DisplayException](#bkmk_displayException), and [DeleteRequiredRecords](#bkmk_deleteRequiredRecords).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-188">The primary sample class is typically structured to contain the following common set of methods: [Main](#bkmk_main), [ConnectToCRM](#bkmk_connectToCrm), [CreateRequiredRecords](#bkmk_createRequiredRecords), [RunAsync](#bkmk_runAsync), [DisplayException](#bkmk_displayException), and [DeleteRequiredRecords](#bkmk_deleteRequiredRecords).</span></span>  
  
<a name="bkmk_main"></a>   
#### <a name="main-method"></a><span data-ttu-id="f4cf5-189">Main method</span><span class="sxs-lookup"><span data-stu-id="f4cf5-189">Main method</span></span>  
 <span data-ttu-id="f4cf5-190">By definition, this method begins execution of the sample.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-190">By definition, this method begins execution of the sample.</span></span>  <span data-ttu-id="f4cf5-191">It only contains high-level control flow and exception-handling logic, often exactly the following code:</span><span class="sxs-lookup"><span data-stu-id="f4cf5-191">It only contains high-level control flow and exception-handling logic, often exactly the following code:</span></span>  
  
```csharp  
  
static void Main(string[] args)  
{  
FunctionsAndActions app = new FunctionsAndActions();  
try  
{  
//Read configuration file and connect to specified CRM server.  
app.ConnectToCRM(args);  
app.CreateRequiredRecords();  
Task.WaitAll(Task.Run(async () => await app.RunAsync()));  
}  
catch (System.Exception ex) { DisplayException(ex);  
}  
finally  
{  
if (app.httpClient != null)  
{  
app.DeleteRequiredRecords(true);  
app.httpClient.Dispose();  
}  
Console.WriteLine("Press <Enter> to exit the program.");  
Console.ReadLine();  
}  
}  
  
```  
  
<a name="bkmk_connectToCrm"></a>   
#### <a name="connecttocrm-method"></a><span data-ttu-id="f4cf5-192">ConnectToCRM method</span><span class="sxs-lookup"><span data-stu-id="f4cf5-192">ConnectToCRM method</span></span>  
 <span data-ttu-id="f4cf5-193">This method calls upon the helper libraries to read the application configuration file and then establishes a connection to the specified Dynamics 365 for Customer Engagement server.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-193">This method calls upon the helper libraries to read the application configuration file and then establishes a connection to the specified Dynamics 365 for Customer Engagement server.</span></span> <span data-ttu-id="f4cf5-194">The result of these steps is the initialization of a [HttpClient](https://msdn.microsoft.com/en-us/library/system.net.http.httpclient\(v=vs.110\).aspx) class property that is used throughout the program to send web requests and receive responses.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-194">The result of these steps is the initialization of a [HttpClient](https://msdn.microsoft.com/en-us/library/system.net.http.httpclient\(v=vs.110\).aspx) class property that is used throughout the program to send web requests and receive responses.</span></span>  <span data-ttu-id="f4cf5-195">Note the following properties are set on this object:</span><span class="sxs-lookup"><span data-stu-id="f4cf5-195">Note the following properties are set on this object:</span></span>  
  
```csharp  
  
//Define the Web API address, the max period of execute time, the Odata  
// version, and the expected response payload format.  
httpClient.BaseAddress = new Uri(config.ServiceUrl + "api/data/v8.1/");  
httpClient.Timeout = new TimeSpan(0, 2, 0);  // 2 minute timeout  
httpClient.DefaultRequestHeaders.Add("OData-MaxVersion", "4.0");  
httpClient.DefaultRequestHeaders.Add("OData-Version", "4.0");  
httpClient.DefaultRequestHeaders.Accept.Add(new MediaTypeWithQualityHeaderValue("application/json"));  
  
```  
  
 <span data-ttu-id="f4cf5-196">For more information about sample application configuration and authentication, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="f4cf5-196">For more information about sample application configuration and authentication, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span></span>  
  
<a name="bkmk_createRequiredRecords"></a>   
#### <a name="createrequiredrecords-method"></a><span data-ttu-id="f4cf5-197">CreateRequiredRecords method</span><span class="sxs-lookup"><span data-stu-id="f4cf5-197">CreateRequiredRecords method</span></span>  
 <span data-ttu-id="f4cf5-198">This method creates and initializes entity records required by the sample, only when these operations are not of primary interest in the sample.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-198">This method creates and initializes entity records required by the sample, only when these operations are not of primary interest in the sample.</span></span>  <span data-ttu-id="f4cf5-199">For example, the [Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md) does not contain this method because record creation is a primary consideration of the sample.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-199">For example, the [Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md) does not contain this method because record creation is a primary consideration of the sample.</span></span>  
  
<a name="bkmk_runAsync"></a>   
#### <a name="runasync-method"></a><span data-ttu-id="f4cf5-200">RunAsync method</span><span class="sxs-lookup"><span data-stu-id="f4cf5-200">RunAsync method</span></span>  
 <span data-ttu-id="f4cf5-201">This asynchronous method either contains the pertinent source code or, for longer programs, calls methods that group the pertinent sample code.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-201">This asynchronous method either contains the pertinent source code or, for longer programs, calls methods that group the pertinent sample code.</span></span> <span data-ttu-id="f4cf5-202">The contained code is explained by embedded comments and commentary located in the **Remarks** section of  each corresponding sample topic.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-202">The contained code is explained by embedded comments and commentary located in the **Remarks** section of  each corresponding sample topic.</span></span>  
  
<a name="bkmk_displayException"></a>   
#### <a name="displayexception-method"></a><span data-ttu-id="f4cf5-203">DisplayException method</span><span class="sxs-lookup"><span data-stu-id="f4cf5-203">DisplayException method</span></span>  
 <span data-ttu-id="f4cf5-204">This helper method displays exception information, including for inner exceptions, to the standard console.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-204">This helper method displays exception information, including for inner exceptions, to the standard console.</span></span>  
  
<a name="bkmk_deleteRequiredRecords"></a>   
#### <a name="deleterequiredrecords-method"></a><span data-ttu-id="f4cf5-205">DeleteRequiredRecords method</span><span class="sxs-lookup"><span data-stu-id="f4cf5-205">DeleteRequiredRecords method</span></span>  
 <span data-ttu-id="f4cf5-206">This companion method optionally deletes sample records and other Dynamics 365 for Customer Engagement server resources created in the program and particularly by the [CreateRequiredRecords](#bkmk_createRequiredRecords) method.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-206">This companion method optionally deletes sample records and other Dynamics 365 for Customer Engagement server resources created in the program and particularly by the [CreateRequiredRecords](#bkmk_createRequiredRecords) method.</span></span> <span data-ttu-id="f4cf5-207">It queries the user for verification of this operation, then it iterates through the `entityUris` collection and attempts to delete each element with a HTTP DELETE message.</span><span class="sxs-lookup"><span data-stu-id="f4cf5-207">It queries the user for verification of this operation, then it iterates through the `entityUris` collection and attempts to delete each element with a HTTP DELETE message.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f4cf5-208">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f4cf5-208">See also</span></span>  
 <span data-ttu-id="f4cf5-209">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="f4cf5-209">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span></span>  
 <span data-ttu-id="f4cf5-210">[Web API Samples](web-api-samples.md) </span><span class="sxs-lookup"><span data-stu-id="f4cf5-210">[Web API Samples](web-api-samples.md) </span></span>  
 <span data-ttu-id="f4cf5-211">[Web API Samples (Client-side JavaScript)](web-api-samples-client-side-javascript.md) </span><span class="sxs-lookup"><span data-stu-id="f4cf5-211">[Web API Samples (Client-side JavaScript)](web-api-samples-client-side-javascript.md) </span></span>  
 <span data-ttu-id="f4cf5-212">[Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="f4cf5-212">[Web API Basic Operations Sample (C#)](web-api-basic-operations-sample-csharp.md) </span></span>  
 <span data-ttu-id="f4cf5-213">[Web API Query Data Sample (C#)](web-api-query-data-sample-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="f4cf5-213">[Web API Query Data Sample (C#)](web-api-query-data-sample-csharp.md) </span></span>  
 <span data-ttu-id="f4cf5-214">[Web API Conditional Operations Sample (C#)](web-api-conditional-operations-sample-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="f4cf5-214">[Web API Conditional Operations Sample (C#)](web-api-conditional-operations-sample-csharp.md) </span></span>  
 [<span data-ttu-id="f4cf5-215">Web API Functions and Actions Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="f4cf5-215">Web API Functions and Actions Sample (C#)</span></span>](web-api-functions-actions-sample-csharp.md)
