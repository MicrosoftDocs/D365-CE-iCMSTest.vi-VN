---
title: 'Web API Helper code: CrmHttpResponseException class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: CrmHttpResponseException class is used to represent HTTP status errors generated during Dynamics 365 for Customer Engagement Web API calls
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 8deb0bc5-6f4a-4ca7-a3a2-75c06dc7f967
caps.latest.revision: 11
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c051f170dac19f1ec3f121fab8f0dc747f7fb8d1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387520"
---
# <a name="web-api-helper-code-crmhttpresponseexception-class"></a><span data-ttu-id="ff59a-103">Web API Helper code: CrmHttpResponseException class</span><span class="sxs-lookup"><span data-stu-id="ff59a-103">Web API Helper code: CrmHttpResponseException class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ff59a-104">Use the `CrmHttpResponseException` class to represent [HTTP status errors](https://msdn.microsoft.com/library/gg334391.aspx) generated during [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API calls.</span><span class="sxs-lookup"><span data-stu-id="ff59a-104">Use the `CrmHttpResponseException` class to represent [HTTP status errors](https://msdn.microsoft.com/library/gg334391.aspx) generated during [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API calls.</span></span>  <span data-ttu-id="ff59a-105">This class is derived from the standard .NET System.[Exception](https://msdn.microsoft.com/library/system.exception.aspx) class to easily integrate with your existing exception-handling mechanisms.</span><span class="sxs-lookup"><span data-stu-id="ff59a-105">This class is derived from the standard .NET System.[Exception](https://msdn.microsoft.com/library/system.exception.aspx) class to easily integrate with your existing exception-handling mechanisms.</span></span> <span data-ttu-id="ff59a-106">For more general information, see [Handling and Throwing Exceptions](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/index).</span><span class="sxs-lookup"><span data-stu-id="ff59a-106">For more general information, see [Handling and Throwing Exceptions](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/index).</span></span>  

 <span data-ttu-id="ff59a-107">The `CrmHttpResponseException` class is located in the file Exceptions.cs in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode/).</span><span class="sxs-lookup"><span data-stu-id="ff59a-107">The `CrmHttpResponseException` class is located in the file Exceptions.cs in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode/).</span></span>  <span data-ttu-id="ff59a-108">It is used extensively in the other helper library classes and C# Web API samples.</span><span class="sxs-lookup"><span data-stu-id="ff59a-108">It is used extensively in the other helper library classes and C# Web API samples.</span></span> <span data-ttu-id="ff59a-109">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span><span class="sxs-lookup"><span data-stu-id="ff59a-109">For more information, see [Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md).</span></span>  

 <span data-ttu-id="ff59a-110">This class utilizes JSON string-handling functionality from the open source [Json.NET](http://www.newtonsoft.com/json) library.</span><span class="sxs-lookup"><span data-stu-id="ff59a-110">This class utilizes JSON string-handling functionality from the open source [Json.NET](http://www.newtonsoft.com/json) library.</span></span>  

## <a name="class-members"></a><span data-ttu-id="ff59a-111">Class members</span><span class="sxs-lookup"><span data-stu-id="ff59a-111">Class members</span></span>  

 <span data-ttu-id="ff59a-112">The following table shows the public members of the `CrmHttpResponseException` class.</span><span class="sxs-lookup"><span data-stu-id="ff59a-112">The following table shows the public members of the `CrmHttpResponseException` class.</span></span>  


|                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff59a-113">![Dynamics 365 for Customer Engagement Web API Helper Library-CrmHttpResponseException Class Diagram](../media/web-api-helper-library-crm-exception-class-diagram.png "Dynamics 365 for Customer Engagement Web API Helper Library-CrmHttpResponseException Class Diagram")</span><span class="sxs-lookup"><span data-stu-id="ff59a-113">![Dynamics 365 for Customer Engagement Web API Helper Library-CrmHttpResponseException Class Diagram](../media/web-api-helper-library-crm-exception-class-diagram.png "Dynamics 365 for Customer Engagement Web API Helper Library-CrmHttpResponseException Class Diagram")</span></span> | <span data-ttu-id="ff59a-114">**CrmHttpResponseException  class**</span><span class="sxs-lookup"><span data-stu-id="ff59a-114">**CrmHttpResponseException  class**</span></span><br /><br /> <span data-ttu-id="ff59a-115">*Properties:*</span><span class="sxs-lookup"><span data-stu-id="ff59a-115">*Properties:*</span></span><br /><br /> <span data-ttu-id="ff59a-116">`StackTrace` – the string representation of the immediate frames on the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server’s call stack when the exception was thrown, if available.</span><span class="sxs-lookup"><span data-stu-id="ff59a-116">`StackTrace` – the string representation of the immediate frames on the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps server’s call stack when the exception was thrown, if available.</span></span><br /><br /> <span data-ttu-id="ff59a-117">*Methods*:</span><span class="sxs-lookup"><span data-stu-id="ff59a-117">*Methods*:</span></span><br /><br /> <span data-ttu-id="ff59a-118">The constructors initialize an instance of this class, and require a [HttpContent](https://msdn.microsoft.com/library/hh193687\(v=vs.110\).aspx) parameter and an optional inner exception parameter.</span><span class="sxs-lookup"><span data-stu-id="ff59a-118">The constructors initialize an instance of this class, and require a [HttpContent](https://msdn.microsoft.com/library/hh193687\(v=vs.110\).aspx) parameter and an optional inner exception parameter.</span></span><br /><br /> <span data-ttu-id="ff59a-119">`ExtractMessageFromContent` – this static method extracts the error message from the specified HTTP content parameter.</span><span class="sxs-lookup"><span data-stu-id="ff59a-119">`ExtractMessageFromContent` – this static method extracts the error message from the specified HTTP content parameter.</span></span> |

## <a name="usage"></a><span data-ttu-id="ff59a-120">Sử dụng</span><span class="sxs-lookup"><span data-stu-id="ff59a-120">Usage</span></span>  

 <span data-ttu-id="ff59a-121">Typically, you create and throw a `CrmHttpResponseException` object when processing a status error returned with a HTTP response message.</span><span class="sxs-lookup"><span data-stu-id="ff59a-121">Typically, you create and throw a `CrmHttpResponseException` object when processing a status error returned with a HTTP response message.</span></span> <span data-ttu-id="ff59a-122">For example, the following code throws such an error when the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /> call fails.</span><span class="sxs-lookup"><span data-stu-id="ff59a-122">For example, the following code throws such an error when the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /> call fails.</span></span>  

```csharp  
response = await httpClient.GetAsync("WhoAmI", HttpCompletionOption.ResponseContentRead);  
if (!response.IsSuccessStatusCode)  
{   
    throw new CrmHttpResponseException(response.Content);   
}  
```  

 <span data-ttu-id="ff59a-123">You can catch and process thrown `CrmHttpResponseException` objects similarly to other standard .NET exceptions.</span><span class="sxs-lookup"><span data-stu-id="ff59a-123">You can catch and process thrown `CrmHttpResponseException` objects similarly to other standard .NET exceptions.</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="ff59a-124">If you are using the HttpResponseMessage.[EnsureSuccessStatusCode](https://msdn.microsoft.com/library/system.net.http.httpresponsemessage.ensuresuccessstatuscode\(v=vs.110\).aspx) method to automatically convert HTTP response errors into thrown [HttpRequestException](https://msdn.microsoft.com/library/system.net.http.httprequestexception\(v=vs.110\).aspx) objects,    then this approach precludes the use of the `CrmHttpResponseException` class.</span><span class="sxs-lookup"><span data-stu-id="ff59a-124">If you are using the HttpResponseMessage.[EnsureSuccessStatusCode](https://msdn.microsoft.com/library/system.net.http.httpresponsemessage.ensuresuccessstatuscode\(v=vs.110\).aspx) method to automatically convert HTTP response errors into thrown [HttpRequestException](https://msdn.microsoft.com/library/system.net.http.httprequestexception\(v=vs.110\).aspx) objects,    then this approach precludes the use of the `CrmHttpResponseException` class.</span></span> <span data-ttu-id="ff59a-125">Note that if you use this approach, much of the response message details, including the status code, will not be available during exception handling.</span><span class="sxs-lookup"><span data-stu-id="ff59a-125">Note that if you use this approach, much of the response message details, including the status code, will not be available during exception handling.</span></span>  

## <a name="class-listing"></a><span data-ttu-id="ff59a-126">Class listing</span><span class="sxs-lookup"><span data-stu-id="ff59a-126">Class listing</span></span>

 <span data-ttu-id="ff59a-127">The most current source for this class is found in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode) NuGet package.</span><span class="sxs-lookup"><span data-stu-id="ff59a-127">The most current source for this class is found in the [CRM SDK Web API Helper Library](https://www.nuget.org/packages/Microsoft.CrmSdk.WebApi.Samples.HelperCode) NuGet package.</span></span>  

```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.Threading.Tasks;  
using System.Net.Http;  
using Newtonsoft.Json;  
using Newtonsoft.Json.Linq;  

namespace Microsoft.Crm.Sdk.Samples.HelperCode  
{  
    /// <summary>  
    /// Produces a populated exception from an error message in the content of an HTTP response.   
    /// </summary>  
    public class CrmHttpResponseException : System.Exception  
    {  
        #region Properties  
        private static string _stackTrace;  

        /// <summary>  
        /// Gets a string representation of the immediate frames on the call stack.  
        /// </summary>  
        public override string StackTrace  
        {  
            get { return _stackTrace; }  
        }  
        #endregion Properties  

        #region Constructors  
        /// <summary>  
        /// Initializes a new instance of the CrmHttpResponseException class.  
        /// </summary>  
        /// <param name="content">The populated HTTP content in Json format.</param>  
        public CrmHttpResponseException(HttpContent content)  
            : base(ExtractMessageFromContent(content)) { }  

        /// <summary>  
        /// Initializes a new instance of the CrmHttpResponseException class.  
        /// </summary>  
        /// <param name="content">The populated HTTP content in Json format.</param>  
        /// <param name="innerexception">The exception that is the cause of the current exception, or a null reference  
        /// if no inner exception is specified.</param>  
        public CrmHttpResponseException(HttpContent content, Exception innerexception)  
            : base(ExtractMessageFromContent(content), innerexception) { }  

        #endregion Constructors  

        #region Methods  
        /// <summary>  
        /// Extracts the CRM specific error message and stack trace from an HTTP content.   
        /// </summary>  
        /// <param name="content">The HTTP content in Json format.</param>  
        /// <returns>The error message.</returns>  
        private static string ExtractMessageFromContent(HttpContent content)  
        {  
            string message = String.Empty;  
            string downloadedContent = content.ReadAsStringAsync().Result;  
            if (content.Headers.ContentType.MediaType.Equals("text/plain"))  
            {  
                message = downloadedContent;  
            }  
            else if (content.Headers.ContentType.MediaType.Equals("application/json"))  
            {  
                JObject jcontent = (JObject)JsonConvert.DeserializeObject(downloadedContent);  
                IDictionary<string, JToken> d = jcontent;  

                // An error message is returned in the content under the 'error' key.   
                if (d.ContainsKey("error"))  
                {  
                    JObject error = (JObject)jcontent.Property("error").Value;  
                    message = (String)error.Property("message").Value;  
                }  
                else if (d.ContainsKey("Message"))  
                    message = (String)jcontent.Property("Message").Value;  

                if (d.ContainsKey("StackTrace"))  
                    _stackTrace = (String)jcontent.Property("StackTrace").Value;  
            }  
            else if (content.Headers.ContentType.MediaType.Equals("text/html"))  
            {  
                message = "HTML content that was returned is shown below.";  
                message += "\n\n" + downloadedContent;  
            }  
            else  
            {  
                message = String.Format("No handler is available for content in the {0} format.",    
                    content.Headers.ContentType.MediaType.ToString());  
            }  
            return message;  
            #endregion Methods  
        }  
    }  
}  

```  

### <a name="see-also"></a><span data-ttu-id="ff59a-128">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ff59a-128">See also</span></span>

 <span data-ttu-id="ff59a-129">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="ff59a-129">[Get Started with the Web API (C#)](get-started-dynamics-365-web-api-csharp.md) </span></span>  
 <span data-ttu-id="ff59a-130">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="ff59a-130">[Start a Web API project in Visual Studio (C#)](start-web-api-project-visual-studio-csharp.md) </span></span>  
 <span data-ttu-id="ff59a-131">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="ff59a-131">[Use the Dynamics 365 for Customer Engagement Web API Helper Library (C#)](use-microsoft-dynamics-365-web-api-helper-library-csharp.md) </span></span>  
 <span data-ttu-id="ff59a-132">[Helper code: Authentication class](web-api-helper-code-authentication-class.md) </span><span class="sxs-lookup"><span data-stu-id="ff59a-132">[Helper code: Authentication class](web-api-helper-code-authentication-class.md) </span></span>  
 [<span data-ttu-id="ff59a-133">Helper code: Configuration class</span><span class="sxs-lookup"><span data-stu-id="ff59a-133">Helper code: Configuration class</span></span>](web-api-helper-code-configuration-classes.md)
