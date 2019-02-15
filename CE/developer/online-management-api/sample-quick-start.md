---
title: 'Quick Start Sample: Retrieve Customer Enagament instances using Online Management API for Dynamics 365 for Customer Engagement| MicrosoftDocs'
description: The C# sample demonstrates how to authenticate to the Online Management API and then retrieve all Customer Engagement instances from your Office 365 tenant.
ms.date: 12/13/2018
ms.service: crm-online
ms.topic: conceptual
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 63600a55-a1f0-491f-83f6-b3252566d27e
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1725187456472c9ec9f37014660dc20dc315d0be
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385595"
---
# <a name="quick-start-sample-retrieve-customer-engagement-instances-using-online-management-api"></a><span data-ttu-id="92158-103">Quick Start Sample: Retrieve Customer Engagement instances using Online Management API</span><span class="sxs-lookup"><span data-stu-id="92158-103">Quick Start Sample: Retrieve Customer Engagement instances using Online Management API</span></span> 

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="92158-104">The C# sample demonstrates how to authenticate to the Online Management API and then retrieve all Customer Engagement instances from your Office 365 tenant.</span><span class="sxs-lookup"><span data-stu-id="92158-104">The C# sample demonstrates how to authenticate to the Online Management API and then retrieve all Customer Engagement instances from your Office 365 tenant.</span></span>

<span data-ttu-id="92158-105">The sample uses the authentication [helper code](sample-authentication-helper.md) to easily authenticate to Online Management API using the OAuth 2.0 protocol and pass in the access token in header of your request.</span><span class="sxs-lookup"><span data-stu-id="92158-105">The sample uses the authentication [helper code](sample-authentication-helper.md) to easily authenticate to Online Management API using the OAuth 2.0 protocol and pass in the access token in header of your request.</span></span>

## <a name="what-this-sample-does"></a><span data-ttu-id="92158-106">What this sample does?</span><span class="sxs-lookup"><span data-stu-id="92158-106">What this sample does?</span></span>

<span data-ttu-id="92158-107">The sample performs the following tasks:</span><span class="sxs-lookup"><span data-stu-id="92158-107">The sample performs the following tasks:</span></span>

1. <span data-ttu-id="92158-108">Uses the **ConnectToAPI** method to connect to the Online Management API.</span><span class="sxs-lookup"><span data-stu-id="92158-108">Uses the **ConnectToAPI** method to connect to the Online Management API.</span></span>

    <span data-ttu-id="92158-109">a.</span><span class="sxs-lookup"><span data-stu-id="92158-109">a.</span></span> <span data-ttu-id="92158-110">Calls the **DiscoverAuthority** method in the authentication helper code, and passes in the service URL to get the authority information.</span><span class="sxs-lookup"><span data-stu-id="92158-110">Calls the **DiscoverAuthority** method in the authentication helper code, and passes in the service URL to get the authority information.</span></span>

    <span data-ttu-id="92158-111">b.</span><span class="sxs-lookup"><span data-stu-id="92158-111">b.</span></span> <span data-ttu-id="92158-112">Uses an HttpClient instance to connect to Online Management API service.</span><span class="sxs-lookup"><span data-stu-id="92158-112">Uses an HttpClient instance to connect to Online Management API service.</span></span>

    <span data-ttu-id="92158-113">c.</span><span class="sxs-lookup"><span data-stu-id="92158-113">c.</span></span> <span data-ttu-id="92158-114">Specifies the API service base address and the max period of execution time.</span><span class="sxs-lookup"><span data-stu-id="92158-114">Specifies the API service base address and the max period of execution time.</span></span>
1. <span data-ttu-id="92158-115">Uses the **RetrieveInstancesAsync** method to execute a http request to retrieve all Customer Enagement instances in your Office 365 tenant, and then displays the reponse.</span><span class="sxs-lookup"><span data-stu-id="92158-115">Uses the **RetrieveInstancesAsync** method to execute a http request to retrieve all Customer Enagement instances in your Office 365 tenant, and then displays the reponse.</span></span>

## <a name="run-this-sample"></a><span data-ttu-id="92158-116">Run this sample</span><span class="sxs-lookup"><span data-stu-id="92158-116">Run this sample</span></span>
<span data-ttu-id="92158-117">Before you can run this sample, make sure that you have:</span><span class="sxs-lookup"><span data-stu-id="92158-117">Before you can run this sample, make sure that you have:</span></span>
- <span data-ttu-id="92158-118">One of the admin roles in your Office 365 tenant.</span><span class="sxs-lookup"><span data-stu-id="92158-118">One of the admin roles in your Office 365 tenant.</span></span> <span data-ttu-id="92158-119">See [Office 365 Admin roles](get-started-online-management-api.md#office-365-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="92158-119">See [Office 365 Admin roles](get-started-online-management-api.md#office-365-admin-roles)</span></span>
- <span data-ttu-id="92158-120">Visual Studio 2015 or later; Internet connectivity is required to download/restore assemblies in the NuGet package.</span><span class="sxs-lookup"><span data-stu-id="92158-120">Visual Studio 2015 or later; Internet connectivity is required to download/restore assemblies in the NuGet package.</span></span>
- <span data-ttu-id="92158-121">.NET Framework 4.6.2</span><span class="sxs-lookup"><span data-stu-id="92158-121">.NET Framework 4.6.2</span></span>

<span data-ttu-id="92158-122">To run the sample:</span><span class="sxs-lookup"><span data-stu-id="92158-122">To run the sample:</span></span>
1. <span data-ttu-id="92158-123">[Download](https://code.msdn.microsoft.com/Sample-Retrieve-Customer-94e4076d) the sample, and extract it.</span><span class="sxs-lookup"><span data-stu-id="92158-123">[Download](https://code.msdn.microsoft.com/Sample-Retrieve-Customer-94e4076d) the sample, and extract it.</span></span>
2. <span data-ttu-id="92158-124">Double-click the Visual Studio solution file (.sln) under the C# folder at the extracted location to open the solution in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="92158-124">Double-click the Visual Studio solution file (.sln) under the C# folder at the extracted location to open the solution in Visual Studio.</span></span>
3. <span data-ttu-id="92158-125">In the **Programs.cs** file, specify a different service URL if the region is not North America.</span><span class="sxs-lookup"><span data-stu-id="92158-125">In the **Programs.cs** file, specify a different service URL if the region is not North America.</span></span> <span data-ttu-id="92158-126">For a list of service URL values for worldwide regions, see [Service URL](get-started-online-management-api.md#service-url).</span><span class="sxs-lookup"><span data-stu-id="92158-126">For a list of service URL values for worldwide regions, see [Service URL](get-started-online-management-api.md#service-url).</span></span>
    ```csharp
    //TODO: Change this value if your Office 365 tenant is in a different region than North America

    private static string _serviceUrl = "https://admin.services.crm.dynamics.com";
    ```
4. <span data-ttu-id="92158-127">In the **HelperCode** > **AuthenticationHelper.cs** file, update the values of the `_clientId` and `_redirectURL` values appropriately.</span><span class="sxs-lookup"><span data-stu-id="92158-127">In the **HelperCode** > **AuthenticationHelper.cs** file, update the values of the `_clientId` and `_redirectURL` values appropriately.</span></span>

    ```csharp
    // TODO: Substitute your app registration values here.
    // These values are obtained on registering your application with the 
    // Azure Active Directory.
    private static string _clientId = "<GUID>";    //e.g. "e5cf0024-a66a-4f16-85ce-99ba97a24bb2"
    private static string _redirectUrl = "<Url>";  //e.g. "app://e5cf0024-a66a-4f16-85ce-99ba97a24bb2"
    ```
5. <span data-ttu-id="92158-128">Save changes, and then start debugging by pressing F5 or select **Debug** > **Start Debugging**.</span><span class="sxs-lookup"><span data-stu-id="92158-128">Save changes, and then start debugging by pressing F5 or select **Debug** > **Start Debugging**.</span></span>

## <a name="code-sample-listing"></a><span data-ttu-id="92158-129">Code sample listing</span><span class="sxs-lookup"><span data-stu-id="92158-129">Code sample listing</span></span> 

<span data-ttu-id="92158-130">Here is the complete sample code:</span><span class="sxs-lookup"><span data-stu-id="92158-130">Here is the complete sample code:</span></span>

```csharp
using Microsoft.Crm.Sdk.Samples.HelperCode;
using System;
using System.Net.Http;
using System.Threading.Tasks;


namespace Microsoft.Crm.Sdk.Samples
{
    /// <summary>
    /// This sample retrieves Customer Engagement instances
    /// in your Office 365 tenant.
    /// </summary>    

    class RetrieveInstances
    {
        private HttpClient httpClient;

        //TODO: Change this value if your Office 365 tenant is in a different region than North America
        private static string _serviceUrl = "https://admin.services.crm.dynamics.com";

        private void ConnectToAPI()
        {
            Console.WriteLine("Connecting to the Online Management API service...");

            // Discover authority for the Online Management API service
            var authority = Authentication.DiscoverAuthority(_serviceUrl);

            // Authenticate to the Online Management API service by 
            // passing in the discovered authority 
            Authentication auth = new Authentication(authority.Result.ToString());            

            // Use an HttpClient object to connect to Online Management API service.           
            httpClient = new HttpClient(auth.ClientHandler, true);

            // Specify the API service base address and the max period of execution time 
            httpClient.BaseAddress = new Uri(_serviceUrl);
            httpClient.Timeout = new TimeSpan(0, 2, 0);            
        }

        public async Task RetrieveInstancesAsync()
        {
            HttpRequestMessage myRequest = new HttpRequestMessage(HttpMethod.Get, "/api/v1.1/instances");
            HttpResponseMessage myResponse = await httpClient.SendAsync(myRequest);

            if (myResponse.IsSuccessStatusCode)
            {
                var result = myResponse.Content.ReadAsStringAsync().Result;
                Console.WriteLine("Your instances retrieved from Office 365 tenant: \n{0}", result);
            }
            else
            {
                Console.WriteLine("The request failed with a status of '{0}'",
                       myResponse.ReasonPhrase);
            }
        }

        static public void Main(string[] args)
        {
            RetrieveInstances app = new RetrieveInstances();
            try
            {
                // Connect to the Online Management API. 
                app.ConnectToAPI();

                // Run your request
                Task.WaitAll(Task.Run(async () => await app.RetrieveInstancesAsync()));
            }
            catch (System.Exception ex) { DisplayException(ex); }
            finally
            {
                if (app.httpClient != null)
                { app.httpClient.Dispose(); }
                Console.WriteLine("Press <Enter> to exit the program.");
                Console.ReadLine();
            }
        }

        /// <summary> Helper method to display exceptions </summary> 
        private static void DisplayException(Exception ex)
        {
            Console.WriteLine("The application terminated with an error.");
            Console.WriteLine(ex.Message);
            while (ex.InnerException != null)
            {
                Console.WriteLine("\t* {0}", ex.InnerException.Message);
                ex = ex.InnerException;
            }
        }
    }
}
```

### <a name="related-topics"></a><span data-ttu-id="92158-131">Related Topics</span><span class="sxs-lookup"><span data-stu-id="92158-131">Related Topics</span></span>  

[<span data-ttu-id="92158-132">Get started with Online Management API</span><span class="sxs-lookup"><span data-stu-id="92158-132">Get started with Online Management API</span></span>](get-started-online-management-api.md)

[<span data-ttu-id="92158-133">Operations supported by Online Management API</span><span class="sxs-lookup"><span data-stu-id="92158-133">Operations supported by Online Management API</span></span>](operations-supported.md)

[<span data-ttu-id="92158-134">Online Management API Reference</span><span class="sxs-lookup"><span data-stu-id="92158-134">Online Management API Reference</span></span>](/rest/api/admin.services.crm.dynamics.com)
