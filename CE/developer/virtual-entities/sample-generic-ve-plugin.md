---
title: 'Sample: Generic virtual entity data provider plug-in (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: Sample demonstrates how to implement a generic custom Dynamics 365 for Customer Engagement virtual entity plug-in.
ms.custom: ''
ms.date: 05/01/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d329dade-16c5-46e9-8dec-4b8efb996d24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: bd8420c1a8b78fd6b12407b1948467c2e101051f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385900"
---
# <a name="sample-generic-virtual-entity-data-provider-plug-in"></a><span data-ttu-id="27b8f-103">Sample: Generic virtual entity data provider plug-in</span><span class="sxs-lookup"><span data-stu-id="27b8f-103">Sample: Generic virtual entity data provider plug-in</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="27b8f-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="27b8f-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps.</span></span> 

## <a name="demonstrates"></a><span data-ttu-id="27b8f-105">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="27b8f-105">Demonstrates</span></span>  
<span data-ttu-id="27b8f-106">This sample shows a minimal implementation for a generic [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps virtual entity data provider plug-in, **DropboxRetrieveMultiplePlugin**, for the [Dropbox](https://www.dropbox.com/) file-sharing service.</span><span class="sxs-lookup"><span data-stu-id="27b8f-106">This sample shows a minimal implementation for a generic [!INCLUDE[pn-dynamics365](../../includes/pn-dynamics-365.md)] for Customer Engagement apps virtual entity data provider plug-in, **DropboxRetrieveMultiplePlugin**, for the [Dropbox](https://www.dropbox.com/) file-sharing service.</span></span> <span data-ttu-id="27b8f-107">It uses the "bare metal" approach, translating the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> through the creation of the custom visitor class, **DropBoxExpressionVisitor**.</span><span class="sxs-lookup"><span data-stu-id="27b8f-107">It uses the "bare metal" approach, translating the <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> through the creation of the custom visitor class, **DropBoxExpressionVisitor**.</span></span> <span data-ttu-id="27b8f-108">It returns a collection of the files that satisfy the search criteria as an <xref:Microsoft.Xrm.Sdk.EntityCollection>.</span><span class="sxs-lookup"><span data-stu-id="27b8f-108">It returns a collection of the files that satisfy the search criteria as an <xref:Microsoft.Xrm.Sdk.EntityCollection>.</span></span> 

## <a name="getting-started"></a><span data-ttu-id="27b8f-109">Bắt đầu</span><span class="sxs-lookup"><span data-stu-id="27b8f-109">Getting started</span></span>
<span data-ttu-id="27b8f-110">In order to build this sample, you must first install the [Dropbox.Api](https://www.nuget.org/packages/Dropbox.Api/) and [Microsoft.CrmSdk.Data](https://www.nuget.org/packages/Microsoft.CrmSdk.Data/) NuGet packages in your solution.</span><span class="sxs-lookup"><span data-stu-id="27b8f-110">In order to build this sample, you must first install the [Dropbox.Api](https://www.nuget.org/packages/Dropbox.Api/) and [Microsoft.CrmSdk.Data](https://www.nuget.org/packages/Microsoft.CrmSdk.Data/) NuGet packages in your solution.</span></span>  <span data-ttu-id="27b8f-111">You'll also need a DropBox account and pass a real access token when creating an instance of the **DropboxClient**.</span><span class="sxs-lookup"><span data-stu-id="27b8f-111">You'll also need a DropBox account and pass a real access token when creating an instance of the **DropboxClient**.</span></span>

<span data-ttu-id="27b8f-112">Add the following using statements to your code:</span><span class="sxs-lookup"><span data-stu-id="27b8f-112">Add the following using statements to your code:</span></span>

```csharp
using Microsoft.Xrm.Sdk;
using Microsoft.Xrm.Sdk.Query;
using Dropbox.Api;
using Dropbox.Api.Files;
```

## <a name="sample-code"></a><span data-ttu-id="27b8f-113">Mã mẫu</span><span class="sxs-lookup"><span data-stu-id="27b8f-113">Sample code</span></span>  

```csharp  

public class DropBoxExpressionVisitor : QueryExpressionVisitorBase
{
    public string SearchKeyWords { get; private set; }

    public override QueryExpression Visit(QueryExpression query)
    {
        // Very simple visitor that extracts search keywords
        var filter = query.Criteria;
        if (filter.Conditions.Count > 0)
        {
            foreach (ConditionExpression condition in filter.Conditions)
            {
                if (condition.Operator == ConditionOperator.Like && condition.Values.Count > 0)
                {
                    string exprVal = (string)condition.Values[0];

                    if (exprVal.Length > 2)
                    {
                        this.SearchKeyWords += " " + exprVal.Substring(1, exprVal.Length - 2);
                    }
                }
            }
            return query;
        }
    }
}

public class DropboxRetrieveMultiplePlugin : IPlugin
{
    public void Execute(IServiceProvider serviceProvider)
    {
        var context = (IPluginExecutionContext)serviceProvider.GetService(typeof(IPluginExecutionContext));
        var qe = (QueryExpression)context.InputParameters["Query"];
        if (qe != null)
        {
            var visitor = new DropBoxExpressionVisitor();
            qe.Accept(visitor);
            using (var dbx = new DropboxClient(AccessToken))
            {
                if (visitor.SearchKeyWords != string.Empty)
                {
                    var searchCriteria = new SearchArg(string.Empty, visitor.SearchKeyWords);
                    var task = Task.Run(() => this.SearchFile(dbx, searchCriteria));
                    context.OutputParameters["BusinessEntityCollection"] = task.Result;
                }
            }
        }
    }

    public async Task<EntityCollection> SearchFile(DropboxClient dbx, SearchArg arg)
    {
        EntityCollection ec = new EntityCollection();
        var list = await dbx.Files.SearchAsync(arg);
        foreach (var item in list.Matches)
        {
            if (item.Metadata.IsFile)
            {
                Entity e = new Entity("new_dropbox");
                e.Attributes.Add("new_dropboxid", Guid.NewGuid());
                e.Attributes.Add("new_filename", item.Metadata.AsFile.Name);
                e.Attributes.Add("new_filesize", item.Metadata.AsFile.Size);
                e.Attributes.Add("new_modifiedon", item.Metadata.AsFile.ServerModified);
                ec.Entities.Add(e);
            }
        }
        return ec;
    }
}

``` 

### <a name="see-also"></a><span data-ttu-id="27b8f-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="27b8f-114">See also</span></span>

[<span data-ttu-id="27b8f-115">Get started with virtual entities</span><span class="sxs-lookup"><span data-stu-id="27b8f-115">Get started with virtual entities</span></span>](get-started-ve.md)<br />
[<span data-ttu-id="27b8f-116">Custom virtual entity data providers</span><span class="sxs-lookup"><span data-stu-id="27b8f-116">Custom virtual entity data providers</span></span>](custom-ve-data-providers.md)
