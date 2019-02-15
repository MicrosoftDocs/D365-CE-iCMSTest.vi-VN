---
title: API Limits | MicrosoftDocs
description: Understand the limits for API requests.
ms.custom: ''
ms.date: 03/08/2018
ms.reviewer: sriknair
ms.service: crm-online
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6cba6191-4e10-4b21-823a-b0cf71ef21d5
author: MicroSri
ms.author: jdaly
manager: faisalmo
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 926c2c7da4848847d0ae26f4c37baa5cec407797
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385877"
---
# <a name="api-limits"></a><span data-ttu-id="f7689-103">API Limits</span><span class="sxs-lookup"><span data-stu-id="f7689-103">API Limits</span></span>

- [!INCLUDE [cc_applies_to_update_9_0_0](../includes/cc_applies_to_update_9_0_0.md)]
- [!INCLUDE [cc_applies_to_update_8_2_0](../includes/cc_applies_to_update_8_2_0.md)]

<span data-ttu-id="f7689-104">Beginning March 19, 2018 we will limit the number of API requests made by each user, per organization instance, within a five minute interval.</span><span class="sxs-lookup"><span data-stu-id="f7689-104">Beginning March 19, 2018 we will limit the number of API requests made by each user, per organization instance, within a five minute interval.</span></span> <span data-ttu-id="f7689-105">Khi vượt quá giới hạn này, nền tảng sẽ đưa ra ngoại lệ.</span><span class="sxs-lookup"><span data-stu-id="f7689-105">When this limit is exceeded, an exception will be thrown by the platform.</span></span>

<span data-ttu-id="f7689-106">Giới hạn sẽ giúp đảm bảo rằng trong trường hợp người dùng chạy các ứng dụng thực hiện lượng yêu cầu đặc biệt lớn trên các máy chủ, họ sẽ không làm ảnh hưởng đến những người dùng khác.</span><span class="sxs-lookup"><span data-stu-id="f7689-106">The limit will help ensure that users running applications that make extraordinarily large demands on servers will not affect other users.</span></span> <span data-ttu-id="f7689-107">Giới hạn sẽ không ảnh hưởng đến người dùng thông thường trên nền tảng.</span><span class="sxs-lookup"><span data-stu-id="f7689-107">The limit will not affect normal users of the platform.</span></span> <span data-ttu-id="f7689-108">Chỉ những ứng dụng thực hiện một lượng rất lớn các yêu cầu API mới bị ảnh hưởng.</span><span class="sxs-lookup"><span data-stu-id="f7689-108">Only applications that perform a very large number of API requests will be affected.</span></span> <span data-ttu-id="f7689-109">Dựa trên phân tích dữ liệu qua phương pháp đo từ xa, giới hạn này vẫn nằm trong biên của hầu hết các ứng dụng thực hiện một lượng lớn yêu cầu API.</span><span class="sxs-lookup"><span data-stu-id="f7689-109">Based on telemetry data analysis, this limit is well within the bounds of most applications that perform a large number of API requests.</span></span> <span data-ttu-id="f7689-110">Giới hạn sẽ đưa ra một mức độ bảo vệ chống đột biến ngẫu nhiên và ngoài ý muốn từ một lượng lớn các yêu cầu mà có thể đe dọa tới tính khả dụng và đặc tính hiệu suất của nền tảng [!INCLUDE [pn-dyn-365](../includes/pn-dyn-365.md)].</span><span class="sxs-lookup"><span data-stu-id="f7689-110">The limit will help provide a level of protection from random and unexpected surges in request volumes that threaten the availability and performance characteristics of the [!INCLUDE [pn-dyn-365](../includes/pn-dyn-365.md)] platform.</span></span>

<span data-ttu-id="f7689-111">If your application has the potential to exceed the limit, please consider the guidance given in the [What should I do if my application exceeds the limit?](#what-should-i-do-if-my-application-exceeds-the-limit) section below.</span><span class="sxs-lookup"><span data-stu-id="f7689-111">If your application has the potential to exceed the limit, please consider the guidance given in the [What should I do if my application exceeds the limit?](#what-should-i-do-if-my-application-exceeds-the-limit) section below.</span></span>

## <a name="what-is-the-limit"></a><span data-ttu-id="f7689-112">What is the limit?</span><span class="sxs-lookup"><span data-stu-id="f7689-112">What is the limit?</span></span>

<span data-ttu-id="f7689-113">Each user will be allowed up to 60,000 API requests, per organization instance, within five minute sliding interval.</span><span class="sxs-lookup"><span data-stu-id="f7689-113">Each user will be allowed up to 60,000 API requests, per organization instance, within five minute sliding interval.</span></span>

## <a name="what-happens-when-the-limit-is-exceeded"></a><span data-ttu-id="f7689-114">What happens when the limit is exceeded?</span><span class="sxs-lookup"><span data-stu-id="f7689-114">What happens when the limit is exceeded?</span></span>

<span data-ttu-id="f7689-115">When the limit is exceeded, any requests will return error responses.</span><span class="sxs-lookup"><span data-stu-id="f7689-115">When the limit is exceeded, any requests will return error responses.</span></span>

<span data-ttu-id="f7689-116">If you use the .NET SDK assemblies, the platform will respond with a `FaultException<OrganizationServiceFault>` WCF Fault with the error code `-2147015902` and the message `Number of requests exceeded the limit of 60000, measured over time window of 300 seconds.`</span><span class="sxs-lookup"><span data-stu-id="f7689-116">If you use the .NET SDK assemblies, the platform will respond with a `FaultException<OrganizationServiceFault>` WCF Fault with the error code `-2147015902` and the message `Number of requests exceeded the limit of 60000, measured over time window of 300 seconds.`</span></span>

<span data-ttu-id="f7689-117">If you use HTTP requests, the response will include these properties:</span><span class="sxs-lookup"><span data-stu-id="f7689-117">If you use HTTP requests, the response will include these properties:</span></span><br />
<span data-ttu-id="f7689-118">`StatusCode` : `429`</span><span class="sxs-lookup"><span data-stu-id="f7689-118">`StatusCode` : `429`</span></span><br />
<span data-ttu-id="f7689-119">`Message` : `Number of requests exceeded the limit of 60000, measured over time window of 300 seconds.`</span><span class="sxs-lookup"><span data-stu-id="f7689-119">`Message` : `Number of requests exceeded the limit of 60000, measured over time window of 300 seconds.`</span></span>

<span data-ttu-id="f7689-120">All requests will return these error responses until the volume of API requests falls below the limit.</span><span class="sxs-lookup"><span data-stu-id="f7689-120">All requests will return these error responses until the volume of API requests falls below the limit.</span></span> <span data-ttu-id="f7689-121">If you get these responses, your application should stop sending API requests until the volume of requests is below the limit.</span><span class="sxs-lookup"><span data-stu-id="f7689-121">If you get these responses, your application should stop sending API requests until the volume of requests is below the limit.</span></span>

## <a name="how-is-this-limit-calculated"></a><span data-ttu-id="f7689-122">How is this limit calculated?</span><span class="sxs-lookup"><span data-stu-id="f7689-122">How is this limit calculated?</span></span>

<span data-ttu-id="f7689-123">Within an organization instance, API requests made by each of your licensed users (including the licensed identity used for running automation) will be measured against this limit.</span><span class="sxs-lookup"><span data-stu-id="f7689-123">Within an organization instance, API requests made by each of your licensed users (including the licensed identity used for running automation) will be measured against this limit.</span></span> <span data-ttu-id="f7689-124">The platform will measure the number of API requests made in five minutes, which keeps sliding by a definite period.</span><span class="sxs-lookup"><span data-stu-id="f7689-124">The platform will measure the number of API requests made in five minutes, which keeps sliding by a definite period.</span></span> <span data-ttu-id="f7689-125">During each measurement interval, at the end of five minutes, the number of API requests by the user is counted.</span><span class="sxs-lookup"><span data-stu-id="f7689-125">During each measurement interval, at the end of five minutes, the number of API requests by the user is counted.</span></span> <span data-ttu-id="f7689-126">In the figure below, three users are making API call requests over a six-minute period.</span><span class="sxs-lookup"><span data-stu-id="f7689-126">In the figure below, three users are making API call requests over a six-minute period.</span></span>  

![api-limit-implementation](media/api-limit-implementation-1.png)

|<span data-ttu-id="f7689-128">Interval</span><span class="sxs-lookup"><span data-stu-id="f7689-128">Interval</span></span>|<span data-ttu-id="f7689-129">Mô tả</span><span class="sxs-lookup"><span data-stu-id="f7689-129">Description</span></span>|
|--|--|
|<span data-ttu-id="f7689-130">A</span><span class="sxs-lookup"><span data-stu-id="f7689-130">A</span></span>|<span data-ttu-id="f7689-131">At the end of five minutes, the total number of API requests for user 1 is 6K, user 2 is 3K, and user 3 is 10K.</span><span class="sxs-lookup"><span data-stu-id="f7689-131">At the end of five minutes, the total number of API requests for user 1 is 6K, user 2 is 3K, and user 3 is 10K.</span></span>|
|<span data-ttu-id="f7689-132">B</span><span class="sxs-lookup"><span data-stu-id="f7689-132">B</span></span>|<span data-ttu-id="f7689-133">At 5+X minutes, X being a constant slice of time (say, a few seconds), which is the sliding interval constant, the platform measures the total for each of these users who are still active.</span><span class="sxs-lookup"><span data-stu-id="f7689-133">At 5+X minutes, X being a constant slice of time (say, a few seconds), which is the sliding interval constant, the platform measures the total for each of these users who are still active.</span></span> <span data-ttu-id="f7689-134">According to the diagram above, this would be user 1 = 7K, user 2 is 6K and user 3 is 25K.</span><span class="sxs-lookup"><span data-stu-id="f7689-134">According to the diagram above, this would be user 1 = 7K, user 2 is 6K and user 3 is 25K.</span></span> <span data-ttu-id="f7689-135">All the cumulative numbers are still below the 60,000 limit, so no change in behavior is expected for these users.</span><span class="sxs-lookup"><span data-stu-id="f7689-135">All the cumulative numbers are still below the 60,000 limit, so no change in behavior is expected for these users.</span></span>|
|<span data-ttu-id="f7689-136">C</span><span class="sxs-lookup"><span data-stu-id="f7689-136">C</span></span>|<span data-ttu-id="f7689-137">As time passes and reaches 5+2X, user 3 makes about 40K API requests, while user 1 and user 2 make 8K and 9K calls, respectively.</span><span class="sxs-lookup"><span data-stu-id="f7689-137">As time passes and reaches 5+2X, user 3 makes about 40K API requests, while user 1 and user 2 make 8K and 9K calls, respectively.</span></span> <span data-ttu-id="f7689-138">This results in user 3 reaching 65K API requests within five minutes, which causes 5K (65K-60K=5K) of his requests to be denied.</span><span class="sxs-lookup"><span data-stu-id="f7689-138">This results in user 3 reaching 65K API requests within five minutes, which causes 5K (65K-60K=5K) of his requests to be denied.</span></span>|

> [!NOTE]
> <span data-ttu-id="f7689-139">Requests that perform multiple API requests like <xref:Microsoft.Xrm.Sdk.Messages.ExecuteMultipleRequest> or <xref:Microsoft.Xrm.Sdk.Messages.ExecuteTransactionRequest> using the .NET SDK assemblies, or `$batch` using the Web API, count as a single request to calculate this limit.</span><span class="sxs-lookup"><span data-stu-id="f7689-139">Requests that perform multiple API requests like <xref:Microsoft.Xrm.Sdk.Messages.ExecuteMultipleRequest> or <xref:Microsoft.Xrm.Sdk.Messages.ExecuteTransactionRequest> using the .NET SDK assemblies, or `$batch` using the Web API, count as a single request to calculate this limit.</span></span> <span data-ttu-id="f7689-140">However, these API requests must follow the [Run-time limitations](org-service/use-executemultiple-improve-performance-bulk-data-load.md#run-time-limitations) for these types of operations.</span><span class="sxs-lookup"><span data-stu-id="f7689-140">However, these API requests must follow the [Run-time limitations](org-service/use-executemultiple-improve-performance-bulk-data-load.md#run-time-limitations) for these types of operations.</span></span>

## <a name="what-should-i-do-if-my-application-exceeds-the-limit"></a><span data-ttu-id="f7689-141">What should I do if my application exceeds the limit?</span><span class="sxs-lookup"><span data-stu-id="f7689-141">What should I do if my application exceeds the limit?</span></span>

<span data-ttu-id="f7689-142">When your application exceeds the limit, the error response from the server specifies the amount of time you should wait before sending more requests.</span><span class="sxs-lookup"><span data-stu-id="f7689-142">When your application exceeds the limit, the error response from the server specifies the amount of time you should wait before sending more requests.</span></span> <span data-ttu-id="f7689-143">The response object is slightly different if you are using SDK assemblies or HTTP requests.</span><span class="sxs-lookup"><span data-stu-id="f7689-143">The response object is slightly different if you are using SDK assemblies or HTTP requests.</span></span>

<span data-ttu-id="f7689-144">For a discussion of best practices, see [Azure Architecture Best Practices Transient fault handling](/azure/architecture/best-practices/transient-faults)</span><span class="sxs-lookup"><span data-stu-id="f7689-144">For a discussion of best practices, see [Azure Architecture Best Practices Transient fault handling](/azure/architecture/best-practices/transient-faults)</span></span>

<span data-ttu-id="f7689-145">[The Polly Project](http://www.thepollyproject.org/) is a library which includes capabilities for dealing with transient faults using execution policies.</span><span class="sxs-lookup"><span data-stu-id="f7689-145">[The Polly Project](http://www.thepollyproject.org/) is a library which includes capabilities for dealing with transient faults using execution policies.</span></span>

### <a name="http-requests"></a><span data-ttu-id="f7689-146">HTTP requests</span><span class="sxs-lookup"><span data-stu-id="f7689-146">HTTP requests</span></span>

<span data-ttu-id="f7689-147">If you are using HTTP requests, you can look for the `Retry-After` HTTP header included in the error response.</span><span class="sxs-lookup"><span data-stu-id="f7689-147">If you are using HTTP requests, you can look for the `Retry-After` HTTP header included in the error response.</span></span> <span data-ttu-id="f7689-148">This will contain a value in seconds indicating how long you should wait before making a follow-up request.</span><span class="sxs-lookup"><span data-stu-id="f7689-148">This will contain a value in seconds indicating how long you should wait before making a follow-up request.</span></span> <span data-ttu-id="f7689-149">More information [MDN web docs Retry-After](https://developer.mozilla.org/docs/Web/HTTP/Headers/Retry-After)</span><span class="sxs-lookup"><span data-stu-id="f7689-149">More information [MDN web docs Retry-After](https://developer.mozilla.org/docs/Web/HTTP/Headers/Retry-After)</span></span>

### <a name="sdk-assemblies"></a><span data-ttu-id="f7689-150">SDK assemblies</span><span class="sxs-lookup"><span data-stu-id="f7689-150">SDK assemblies</span></span>

<span data-ttu-id="f7689-151">If you are using the SDK assemblies, you can look for the `Retry-After` delay in the <xref:Microsoft.Xrm.Sdk.OrganizationServiceFault>.<xref:Microsoft.Xrm.Sdk.BaseServiceFault.ErrorDetails></span><span class="sxs-lookup"><span data-stu-id="f7689-151">If you are using the SDK assemblies, you can look for the `Retry-After` delay in the <xref:Microsoft.Xrm.Sdk.OrganizationServiceFault>.<xref:Microsoft.Xrm.Sdk.BaseServiceFault.ErrorDetails></span></span> <span data-ttu-id="f7689-152">property, using the key `"Retry-After"`.</span><span class="sxs-lookup"><span data-stu-id="f7689-152">property, using the key `"Retry-After"`.</span></span> <span data-ttu-id="f7689-153">The value returned is a [TimeSpan](/dotnet/api/system.timespan) object.</span><span class="sxs-lookup"><span data-stu-id="f7689-153">The value returned is a [TimeSpan](/dotnet/api/system.timespan) object.</span></span>

### <a name="net-sdk-assembly-example"></a><span data-ttu-id="f7689-154">.NET SDK Assembly Example</span><span class="sxs-lookup"><span data-stu-id="f7689-154">.NET SDK Assembly Example</span></span>

<span data-ttu-id="f7689-155">The following example uses the [Retry class](#retry-class) described below to retrieve one account using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span><span class="sxs-lookup"><span data-stu-id="f7689-155">The following example uses the [Retry class](#retry-class) described below to retrieve one account using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*></span></span> <span data-ttu-id="f7689-156">method.</span><span class="sxs-lookup"><span data-stu-id="f7689-156">method.</span></span> <span data-ttu-id="f7689-157">If the request fails because an API limit has been exceeded, the `Retry` class will wait according to a delay specified by the server and try again.</span><span class="sxs-lookup"><span data-stu-id="f7689-157">If the request fails because an API limit has been exceeded, the `Retry` class will wait according to a delay specified by the server and try again.</span></span>

```csharp
var qe = new QueryExpression("account") { TopCount = 1 };
EntityCollection result = Retry.Do(() => service.RetrieveMultiple(qe));
```

#### <a name="retry-class"></a><span data-ttu-id="f7689-158">Retry class</span><span class="sxs-lookup"><span data-stu-id="f7689-158">Retry class</span></span>

<span data-ttu-id="f7689-159">The `Retry` class demonstrates how to retry requests that fail with transient errors based on known <xref:Microsoft.Xrm.Sdk.OrganizationServiceFault> error codes.</span><span class="sxs-lookup"><span data-stu-id="f7689-159">The `Retry` class demonstrates how to retry requests that fail with transient errors based on known <xref:Microsoft.Xrm.Sdk.OrganizationServiceFault> error codes.</span></span> <span data-ttu-id="f7689-160">The `Retry` class waits before retrying.</span><span class="sxs-lookup"><span data-stu-id="f7689-160">The `Retry` class waits before retrying.</span></span> <span data-ttu-id="f7689-161">If the fault specifies a retry delay, wait according to the delay specified by the server.</span><span class="sxs-lookup"><span data-stu-id="f7689-161">If the fault specifies a retry delay, wait according to the delay specified by the server.</span></span> <span data-ttu-id="f7689-162">Else use exponential backoff to calculate the delay based on the number of retry attempts made.</span><span class="sxs-lookup"><span data-stu-id="f7689-162">Else use exponential backoff to calculate the delay based on the number of retry attempts made.</span></span>

```csharp
using System;
using System.ServiceModel;
using System.Threading;

public class Retry
{
    private const int RateLimitExceededErrorCode = -2147015902;

    public static TResult Do<TResult>(Func<TResult> func, int maxRetries = 3)
    {
        int retryCount = 0;

        while (true)
        {
            try
            {
                return func();
            }
            catch (FaultException<Microsoft.Xrm.Sdk.OrganizationServiceFault> ex) 
                when (IsTransientError(ex))
            {
                if (++retryCount >= maxRetries)
                {
                    throw;
                }

                if (ex.Detail.ErrorCode == RateLimitExceededErrorCode)
                {
                    // Use Retry-After delay when specified
                    delay = (TimeSpan)ex.Detail.ErrorDetails["Retry-After"];
                }
                else
                {
                    // else use exponential backoff delay
                    delay = TimeSpan.FromSeconds(Math.Pow(2, retryCount));
                }

                Thread.Sleep(delay);
            }
        }
    }

    private static bool IsTransientError(FaultException<Microsoft.Xrm.Sdk.OrganizationServiceFault> ex)
    {
        // You can add more transient fault codes to retry here
        if (ex.Detail.ErrorCode == RateLimitExceededErrorCode)
        {
            return true;
        }

        return false;
    }
}
```



### <a name="see-also"></a><span data-ttu-id="f7689-163">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f7689-163">See also</span></span>

[<span data-ttu-id="f7689-164">Use the Dynamics 365 for Customer Engagement Organization apps service</span><span class="sxs-lookup"><span data-stu-id="f7689-164">Use the Dynamics 365 for Customer Engagement Organization apps service</span></span>](use-microsoft-dynamics-365-organization-service.md)<br />
[<span data-ttu-id="f7689-165">Use the Dynamics 365 for Customer Engagement Web API</span><span class="sxs-lookup"><span data-stu-id="f7689-165">Use the Dynamics 365 for Customer Engagement Web API</span></span>](use-microsoft-dynamics-365-web-api.md)<br />
[<span data-ttu-id="f7689-166">Execute batch operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="f7689-166">Execute batch operations using the Web API</span></span>](webapi/execute-batch-operations-using-web-api.md)<br />
[<span data-ttu-id="f7689-167">Use ExecuteMultiple to improve performance for bulk data load</span><span class="sxs-lookup"><span data-stu-id="f7689-167">Use ExecuteMultiple to improve performance for bulk data load</span></span>](org-service/use-executemultiple-improve-performance-bulk-data-load.md)



