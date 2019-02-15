---
title: Create and manage custom business apps using code for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn about how to create, manage, and publish business apps in Customer Engagement using code. Dynamics 365 for Customer Engagement business apps are purpose built that provide a limited set of functionality that is relevant for a particular area of work.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: d1980bd7-ea0d-4a66-84c4-de602bdd867d
author: KumarVivek
ms.author: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 4a5bdc0c96f6566ff7a4d93395315419a10dd899
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386387"
---
# <a name="create-and-manage-custom-business-apps-in-customer-engagement-using-code"></a><span data-ttu-id="76a2c-104">Tạo và quản lý các ứng dụng doanh nghiệp tùy chỉnh trong Customer Engagement bằng cách dùng mã</span><span class="sxs-lookup"><span data-stu-id="76a2c-104">Create and manage custom business apps in Customer Engagement using code</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="76a2c-105">Business apps in Customer Engagement are modular, purpose built apps that provide role-based functionality relevant for a particular area of work.</span><span class="sxs-lookup"><span data-stu-id="76a2c-105">Business apps in Customer Engagement are modular, purpose built apps that provide role-based functionality relevant for a particular area of work.</span></span> <span data-ttu-id="76a2c-106">These apps make it easier for users to quickly find things they need to do every day by providing a simple and intuitive interface.</span><span class="sxs-lookup"><span data-stu-id="76a2c-106">These apps make it easier for users to quickly find things they need to do every day by providing a simple and intuitive interface.</span></span> <span data-ttu-id="76a2c-107">For example, the **Sales** business app provides a simpler, smaller sitemap with only the appropriate set of forms, views, dashboards, and process flows that are relevant for sales people.</span><span class="sxs-lookup"><span data-stu-id="76a2c-107">For example, the **Sales** business app provides a simpler, smaller sitemap with only the appropriate set of forms, views, dashboards, and process flows that are relevant for sales people.</span></span> 

<span data-ttu-id="76a2c-108">System administrators and customizers can provide users access to these business apps using security roles; users can access only those apps that they have permission to.</span><span class="sxs-lookup"><span data-stu-id="76a2c-108">System administrators and customizers can provide users access to these business apps using security roles; users can access only those apps that they have permission to.</span></span> <span data-ttu-id="76a2c-109">More information: [Business apps in Dynamics 365 for Customer Engagement apps](../basics/business-apps-dynamics-365.md)</span><span class="sxs-lookup"><span data-stu-id="76a2c-109">More information: [Business apps in Dynamics 365 for Customer Engagement apps](../basics/business-apps-dynamics-365.md)</span></span>

<span data-ttu-id="76a2c-110">In addition to creating custom business apps using the app designer, you can now programmatically create and manage custom business apps in Dynamics 365 for Customer Engagementm apps.</span><span class="sxs-lookup"><span data-stu-id="76a2c-110">In addition to creating custom business apps using the app designer, you can now programmatically create and manage custom business apps in Dynamics 365 for Customer Engagementm apps.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="76a2c-111">You don't have to write code to build custom business apps if you don't need to!</span><span class="sxs-lookup"><span data-stu-id="76a2c-111">You don't have to write code to build custom business apps if you don't need to!</span></span> <span data-ttu-id="76a2c-112">The app designer provides a much simpler and intuitive experience for building custom business apps without having to write code by providing a tile-based information structure and simplified interface.</span><span class="sxs-lookup"><span data-stu-id="76a2c-112">The app designer provides a much simpler and intuitive experience for building custom business apps without having to write code by providing a tile-based information structure and simplified interface.</span></span> <span data-ttu-id="76a2c-113">Check it out here: [Design custom business apps by using the app designer](../customize/design-custom-business-apps-using-app-designer.md)</span><span class="sxs-lookup"><span data-stu-id="76a2c-113">Check it out here: [Design custom business apps by using the app designer](../customize/design-custom-business-apps-using-app-designer.md)</span></span>  
  
<span data-ttu-id="76a2c-114">Creating a custom business app involves the following steps:</span><span class="sxs-lookup"><span data-stu-id="76a2c-114">Creating a custom business app involves the following steps:</span></span>
1. <span data-ttu-id="76a2c-115">Create an [AppModule Entity](entities/appmodule.md) instance to define your app and its properties.</span><span class="sxs-lookup"><span data-stu-id="76a2c-115">Create an [AppModule Entity](entities/appmodule.md) instance to define your app and its properties.</span></span>
2. <span data-ttu-id="76a2c-116">Add or remove components to your app such as entity, sitemap, and other components for your custom app using the <xref:Microsoft.Dynamics.CRM.AddAppComponents> and <xref:Microsoft.Dynamics.CRM.RemoveAppComponents> actions.</span><span class="sxs-lookup"><span data-stu-id="76a2c-116">Add or remove components to your app such as entity, sitemap, and other components for your custom app using the <xref:Microsoft.Dynamics.CRM.AddAppComponents> and <xref:Microsoft.Dynamics.CRM.RemoveAppComponents> actions.</span></span>
3. <span data-ttu-id="76a2c-117">Check your app for any required components thats missing by using the <xref:Microsoft.Dynamics.CRM.ValidateApp> function.</span><span class="sxs-lookup"><span data-stu-id="76a2c-117">Check your app for any required components thats missing by using the <xref:Microsoft.Dynamics.CRM.ValidateApp> function.</span></span>
4. <span data-ttu-id="76a2c-118">Publish your app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-118">Publish your app.</span></span>
5. <span data-ttu-id="76a2c-119">Associate appropriate security roles to your custom business app to provide access to users.</span><span class="sxs-lookup"><span data-stu-id="76a2c-119">Associate appropriate security roles to your custom business app to provide access to users.</span></span>


## <a name="create-your-business-app-and-define-its-properties"></a><span data-ttu-id="76a2c-120">Create your business app and define its properties</span><span class="sxs-lookup"><span data-stu-id="76a2c-120">Create your business app and define its properties</span></span>

<span data-ttu-id="76a2c-121">You must have the System Administrator or System Customizer security role or equivalent permissions to be able to create an app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-121">You must have the System Administrator or System Customizer security role or equivalent permissions to be able to create an app.</span></span> <span data-ttu-id="76a2c-122">You can select from one of the following types for your app to specify the client that the app will the app will be used for:</span><span class="sxs-lookup"><span data-stu-id="76a2c-122">You can select from one of the following types for your app to specify the client that the app will the app will be used for:</span></span> 
- <span data-ttu-id="76a2c-123">**Web**:  This is the classic Dynamics 365 for Customer Engagement apps web browser client.</span><span class="sxs-lookup"><span data-stu-id="76a2c-123">**Web**:  This is the classic Dynamics 365 for Customer Engagement apps web browser client.</span></span>
- <span data-ttu-id="76a2c-124">**Unified Interface**: Runs on the new Unified Interface, which provides key accessibility and responsive design benefits.</span><span class="sxs-lookup"><span data-stu-id="76a2c-124">**Unified Interface**: Runs on the new Unified Interface, which provides key accessibility and responsive design benefits.</span></span> <span data-ttu-id="76a2c-125">For more information about Unified Interface, see [Unified Interface framework for new apps](/dynamics365/get-started/whats-new/customer-engagement/new-in-july-2017-update#unified-interface-framework-for-new-apps).</span><span class="sxs-lookup"><span data-stu-id="76a2c-125">For more information about Unified Interface, see [Unified Interface framework for new apps](/dynamics365/get-started/whats-new/customer-engagement/new-in-july-2017-update#unified-interface-framework-for-new-apps).</span></span> 

<span data-ttu-id="76a2c-126">You select the app type by specifying an integer value for the **clienttype** attribute: 2 for **Web** and 4 for **Unified Interface**.</span><span class="sxs-lookup"><span data-stu-id="76a2c-126">You select the app type by specifying an integer value for the **clienttype** attribute: 2 for **Web** and 4 for **Unified Interface**.</span></span> <span data-ttu-id="76a2c-127">If you do not specify the type for an app, the type is set to **Web** by default.</span><span class="sxs-lookup"><span data-stu-id="76a2c-127">If you do not specify the type for an app, the type is set to **Web** by default.</span></span> 

<span data-ttu-id="76a2c-128">You must specify the following properties at a minimum to create an app:</span><span class="sxs-lookup"><span data-stu-id="76a2c-128">You must specify the following properties at a minimum to create an app:</span></span>
- <span data-ttu-id="76a2c-129">**name**: Unique for your app</span><span class="sxs-lookup"><span data-stu-id="76a2c-129">**name**: Unique for your app</span></span>
- <span data-ttu-id="76a2c-130">**uniquename**: This can be different than the name of your app, and can only have English characters and numbers.</span><span class="sxs-lookup"><span data-stu-id="76a2c-130">**uniquename**: This can be different than the name of your app, and can only have English characters and numbers.</span></span> <span data-ttu-id="76a2c-131">On creating this app, the name is automatically prefixed with your solution publisher prefix (for example 'new_').</span><span class="sxs-lookup"><span data-stu-id="76a2c-131">On creating this app, the name is automatically prefixed with your solution publisher prefix (for example 'new_').</span></span> 
- <span data-ttu-id="76a2c-132">**webresourceid**: ID of the web resource that you want to be set as the image icon for your app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-132">**webresourceid**: ID of the web resource that you want to be set as the image icon for your app.</span></span> <span data-ttu-id="76a2c-133">The system provides you with a default web resource (ID: 953b9fac-1e5e-e611-80d6-00155ded156f) that you can use as an icon for your app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-133">The system provides you with a default web resource (ID: 953b9fac-1e5e-e611-80d6-00155ded156f) that you can use as an icon for your app.</span></span>

<span data-ttu-id="76a2c-134">The following Web API request creates an Unified Interface type of an app:</span><span class="sxs-lookup"><span data-stu-id="76a2c-134">The following Web API request creates an Unified Interface type of an app:</span></span>

```http
POST [Organization URI]/api/data/v9.0/appmodules HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "name": "SDKTestApp",
    "uniquename":"SDKTestApp",
    "webresourceid":"953b9fac-1e5e-e611-80d6-00155ded156f",
    "clienttype": 4
}
```

<span data-ttu-id="76a2c-135">The response **OData-EntityId** header contains the Uri of the created app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-135">The response **OData-EntityId** header contains the Uri of the created app.</span></span>

```http
HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/appmodules(dd621d4a-d898-e711-80e7-00155db763be)
```  

## <a name="add-or-remove-components-from-your-business-app"></a><span data-ttu-id="76a2c-136">Add or remove components from your business app</span><span class="sxs-lookup"><span data-stu-id="76a2c-136">Add or remove components from your business app</span></span>

<span data-ttu-id="76a2c-137">You can add or remove components in an app such as sitemap, entity, dashboard, business process flows, views, and forms that you want to be included in your business app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-137">You can add or remove components in an app such as sitemap, entity, dashboard, business process flows, views, and forms that you want to be included in your business app.</span></span> <span data-ttu-id="76a2c-138">For detailed information about components that can be added to a business app, see [Add or edit app components in the app designer](../customize/add-edit-app-components.md).</span><span class="sxs-lookup"><span data-stu-id="76a2c-138">For detailed information about components that can be added to a business app, see [Add or edit app components in the app designer](../customize/add-edit-app-components.md).</span></span>

<span data-ttu-id="76a2c-139">Use the <xref:Microsoft.Dynamics.CRM.AddAppComponents> action or the <xref:Microsoft.Crm.Sdk.Messages.AddAppComponentsRequest> message to add components to your business app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-139">Use the <xref:Microsoft.Dynamics.CRM.AddAppComponents> action or the <xref:Microsoft.Crm.Sdk.Messages.AddAppComponentsRequest> message to add components to your business app.</span></span> <span data-ttu-id="76a2c-140">The action requires you to specify the following:</span><span class="sxs-lookup"><span data-stu-id="76a2c-140">The action requires you to specify the following:</span></span>
- <span data-ttu-id="76a2c-141">**AppId**: ID of the app where you want to add components</span><span class="sxs-lookup"><span data-stu-id="76a2c-141">**AppId**: ID of the app where you want to add components</span></span>
- <span data-ttu-id="76a2c-142">**Components** A collection of components to be added.</span><span class="sxs-lookup"><span data-stu-id="76a2c-142">**Components** A collection of components to be added.</span></span> <span data-ttu-id="76a2c-143">You need to specify the ID and the entity type of the component you want to add.</span><span class="sxs-lookup"><span data-stu-id="76a2c-143">You need to specify the ID and the entity type of the component you want to add.</span></span> <span data-ttu-id="76a2c-144">For a list of entity types in Customer Engagement Web API, see <xref:Microsoft.Dynamics.CRM.EntityTypeIndex>.</span><span class="sxs-lookup"><span data-stu-id="76a2c-144">For a list of entity types in Customer Engagement Web API, see <xref:Microsoft.Dynamics.CRM.EntityTypeIndex>.</span></span>

<span data-ttu-id="76a2c-145">The following Web API request adds a view (savedquery) and a form (systemform) to your app:</span><span class="sxs-lookup"><span data-stu-id="76a2c-145">The following Web API request adds a view (savedquery) and a form (systemform) to your app:</span></span>

```http
POST [Organization URI]/api/data/v9.0/AddAppComponents HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "AppId":"dd621d4a-d898-e711-80e7-00155db763be",
    "Components":[
        {
            "savedqueryid":"00000000-0000-0000-00aa-000000666000",
            "@odata.type":"Microsoft.Dynamics.CRM.savedquery"
        },
        {
            "formid":"c9e7ec2d-efca-4e4c-b3e3-f63c4bba5e4b",
            "@odata.type":"Microsoft.Dynamics.CRM.systemform"
        }
    ]
}
```

<span data-ttu-id="76a2c-146">To remove a component from an app, use the <xref:Microsoft.Dynamics.CRM.RemoveAppComponents> action or the <xref:Microsoft.Crm.Sdk.Messages.RemoveAppComponentsRequest> message.</span><span class="sxs-lookup"><span data-stu-id="76a2c-146">To remove a component from an app, use the <xref:Microsoft.Dynamics.CRM.RemoveAppComponents> action or the <xref:Microsoft.Crm.Sdk.Messages.RemoveAppComponentsRequest> message.</span></span> <span data-ttu-id="76a2c-147">This action takes the same set of parameters as the **AddAppComponents** action.</span><span class="sxs-lookup"><span data-stu-id="76a2c-147">This action takes the same set of parameters as the **AddAppComponents** action.</span></span>

<span data-ttu-id="76a2c-148">The following Web API request removes a view (savedquery) from your app:</span><span class="sxs-lookup"><span data-stu-id="76a2c-148">The following Web API request removes a view (savedquery) from your app:</span></span> 

```http
POST [Organization URI]/api/data/v9.0/RemoveAppComponents HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "AppId":"dd621d4a-d898-e711-80e7-00155db763be",
    "Components":[
        {
            "savedqueryid":"00000000-0000-0000-00aa-000000666000",
            "@odata.type":"Microsoft.Dynamics.CRM.savedquery"
        }
    ]
}
```

## <a name="validate-your-business-app"></a><span data-ttu-id="76a2c-149">Validate your business app</span><span class="sxs-lookup"><span data-stu-id="76a2c-149">Validate your business app</span></span>

<span data-ttu-id="76a2c-150">Validating an app involves checking for any dependencies for the components you have added in your business app to ensure that your app works fine.</span><span class="sxs-lookup"><span data-stu-id="76a2c-150">Validating an app involves checking for any dependencies for the components you have added in your business app to ensure that your app works fine.</span></span> <span data-ttu-id="76a2c-151">This is the same as clicking **Validate** in the app designer.</span><span class="sxs-lookup"><span data-stu-id="76a2c-151">This is the same as clicking **Validate** in the app designer.</span></span> <span data-ttu-id="76a2c-152">More information: [Validate your app](../customize/validate-app.md)</span><span class="sxs-lookup"><span data-stu-id="76a2c-152">More information: [Validate your app](../customize/validate-app.md)</span></span>

<span data-ttu-id="76a2c-153">Use the <xref:Microsoft.Dynamics.CRM.ValidateApp> function or the <xref:Microsoft.Crm.Sdk.Messages.ValidateAppRequest> message to validate your app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-153">Use the <xref:Microsoft.Dynamics.CRM.ValidateApp> function or the <xref:Microsoft.Crm.Sdk.Messages.ValidateAppRequest> message to validate your app.</span></span> <span data-ttu-id="76a2c-154">The following Web API request shows how to validate your business app with ID: dd621d4a-d898-e711-80e7-00155db763be:</span><span class="sxs-lookup"><span data-stu-id="76a2c-154">The following Web API request shows how to validate your business app with ID: dd621d4a-d898-e711-80e7-00155db763be:</span></span>

`GET [Organization URI]/api/data/v9.0/ValidateApp(AppModuleId=dd621d4a-d898-e711-80e7-00155db763be)`

<span data-ttu-id="76a2c-155">If there are no validation errors, the response is as follows:</span><span class="sxs-lookup"><span data-stu-id="76a2c-155">If there are no validation errors, the response is as follows:</span></span>

```http
HTTP/1.1 200 OK
OData-Version: 4.0

{
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.ValidateAppResponse",
    "AppValidationResponse": {
        "ValidationSuccess": true,
        "ValidationIssueList": []
    }
}
```

<span data-ttu-id="76a2c-156">If there are validation issues in your app, the response displays errors/warnings in the **ValidationIssueList** collection:</span><span class="sxs-lookup"><span data-stu-id="76a2c-156">If there are validation issues in your app, the response displays errors/warnings in the **ValidationIssueList** collection:</span></span>

```http
HTTP/1.1 200 OK
OData-Version: 4.0

{
    "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.ValidateAppResponse",
    "AppValidationResponse": {
        "ValidationSuccess": false,
        "ValidationIssueList": [
            {
                "ErrorType": "Error",
                "Message": "App does not contain Site Map",
                "DisplayName": null,
                "ComponentId": "00000000-0000-0000-0000-000000000000",
                "ComponentType": 0,
                "ComponentSubType": 0,
                "ParentEntityId": "00000000-0000-0000-0000-000000000000",
                "ParentEntityName": null,
                "CRMErrorCode": -2147155684,
                "RequiredComponents": []
            },
            {
                "ErrorType": "Warning",
                "Message": "Account doesn’t reference a form or view. App users will see all forms and views.",
                "DisplayName": null,
                "ComponentId": "00000000-0000-0000-0000-000000000000",
                "ComponentType": 0,
                "ComponentSubType": 0,
                "ParentEntityId": "00000000-0000-0000-0000-000000000000",
                "ParentEntityName": null,
                "CRMErrorCode": -2147155691,
                "RequiredComponents": []
            }
        ]
    }
}
```

## <a name="publish-your-business-app"></a><span data-ttu-id="76a2c-157">Publish your business app</span><span class="sxs-lookup"><span data-stu-id="76a2c-157">Publish your business app</span></span>

<span data-ttu-id="76a2c-158">After you have added required components to your custom business app and validated it, you must publish it to make it available to users.</span><span class="sxs-lookup"><span data-stu-id="76a2c-158">After you have added required components to your custom business app and validated it, you must publish it to make it available to users.</span></span>

<span data-ttu-id="76a2c-159">Use the <xref:Microsoft.Dynamics.CRM.PublishXml> action or the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest> messageto publish your custom business app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-159">Use the <xref:Microsoft.Dynamics.CRM.PublishXml> action or the <xref:Microsoft.Crm.Sdk.Messages.PublishXmlRequest> messageto publish your custom business app.</span></span> <span data-ttu-id="76a2c-160">The following request shows how to publish your business app with ID: dd621d4a-d898-e711-80e7-00155db763be:</span><span class="sxs-lookup"><span data-stu-id="76a2c-160">The following request shows how to publish your business app with ID: dd621d4a-d898-e711-80e7-00155db763be:</span></span>

```http
POST [Organization URI]/api/data/v9.0/PublishXml HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{  
  "ParameterXml":"<importexportxml><appmodules><appmodule>dd621d4a-d898-e711-80e7-00155db763be</appmodule></appmodules></importexportxml>"
}
```

## <a name="manage-access-to-business-app-using-security-roles"></a><span data-ttu-id="76a2c-161">Manage access to business app using security roles</span><span class="sxs-lookup"><span data-stu-id="76a2c-161">Manage access to business app using security roles</span></span>

<span data-ttu-id="76a2c-162">To provide users access to your apps so that they can access it from their **Settings** > **My Apps** area or the Dynamics 365 for Customer Engagement apps home page, you can associate security roles to your business apps.</span><span class="sxs-lookup"><span data-stu-id="76a2c-162">To provide users access to your apps so that they can access it from their **Settings** > **My Apps** area or the Dynamics 365 for Customer Engagement apps home page, you can associate security roles to your business apps.</span></span> <span data-ttu-id="76a2c-163">Users assigned to the associated security roles and can see and use your business apps in Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="76a2c-163">Users assigned to the associated security roles and can see and use your business apps in Customer Engagement.</span></span> 

<span data-ttu-id="76a2c-164">Use the **appmoduleroles_association** navigation property of the [AppModule Entity](entities/appmodule.md) entity to associate a business app with a security role.</span><span class="sxs-lookup"><span data-stu-id="76a2c-164">Use the **appmoduleroles_association** navigation property of the [AppModule Entity](entities/appmodule.md) entity to associate a business app with a security role.</span></span> <span data-ttu-id="76a2c-165">The following request shows how to associate a business app with a security role:</span><span class="sxs-lookup"><span data-stu-id="76a2c-165">The following request shows how to associate a business app with a security role:</span></span>

```http
POST [Organization URI]/api/data/v9.0/appmodules(dd621d4a-d898-e711-80e7-00155db763be)appmoduleroles_association/$ref HTTP/1.1
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{  
  "@odata.id":"[Organization URI]/api/data/v9.0/roles(<roleId>)"
}
```

<span data-ttu-id="76a2c-166">To disassociate a security role from a business app, you use the DELETE request with the same navigation property.</span><span class="sxs-lookup"><span data-stu-id="76a2c-166">To disassociate a security role from a business app, you use the DELETE request with the same navigation property.</span></span> <span data-ttu-id="76a2c-167">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="76a2c-167">For example:</span></span>

`DELETE [Organization URI]/api/data/v9.0/appmodules(dd621d4a-d898-e711-80e7-00155db763be)/appmoduleroles_association/$ref?$id=[Organization URI]/api/data/v9.0/roles(<roleId)
`

## <a name="manage-your-business-apps-and-its-components"></a><span data-ttu-id="76a2c-168">Manage your business apps and its components</span><span class="sxs-lookup"><span data-stu-id="76a2c-168">Manage your business apps and its components</span></span>

<span data-ttu-id="76a2c-169">This section provides you information about retrieving your apps, updating app properties, retrieving app components, and deleting apps.</span><span class="sxs-lookup"><span data-stu-id="76a2c-169">This section provides you information about retrieving your apps, updating app properties, retrieving app components, and deleting apps.</span></span>

### <a name="retrieve-published-apps"></a><span data-ttu-id="76a2c-170">Retrieve published apps</span><span class="sxs-lookup"><span data-stu-id="76a2c-170">Retrieve published apps</span></span>
<span data-ttu-id="76a2c-171">To retrieve published apps, use the following request:</span><span class="sxs-lookup"><span data-stu-id="76a2c-171">To retrieve published apps, use the following request:</span></span>

`GET [Organization URI]/api/data/v9.0/appmodules?$select=name,clienttype`

### <a name="retrieve-unpublished-apps"></a><span data-ttu-id="76a2c-172">Retrieve unpublished apps</span><span class="sxs-lookup"><span data-stu-id="76a2c-172">Retrieve unpublished apps</span></span>
<span data-ttu-id="76a2c-173">To retrieve unpublished apps, use the <xref:Microsoft.Dynamics.CRM.RetrieveUnpublishedMultiple> function.</span><span class="sxs-lookup"><span data-stu-id="76a2c-173">To retrieve unpublished apps, use the <xref:Microsoft.Dynamics.CRM.RetrieveUnpublishedMultiple> function.</span></span> <span data-ttu-id="76a2c-174">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="76a2c-174">For example:</span></span>

`GET [Organization URI]/api/data/v9.0/appmodules/Microsoft.Dynamics.CRM.RetrieveUnpublishedMultiple()?$select=name,clienttype`

### <a name="retrieve-components-in-a-published-business-app"></a><span data-ttu-id="76a2c-175">Retrieve components in a published business app</span><span class="sxs-lookup"><span data-stu-id="76a2c-175">Retrieve components in a published business app</span></span>
<span data-ttu-id="76a2c-176">To retrieve app components for a business app, use the <xref:Microsoft.Dynamics.CRM.RetrieveAppComponents> function or the <xref:Microsoft.Crm.Sdk.Messages.RetrieveAppComponentsRequest> message.</span><span class="sxs-lookup"><span data-stu-id="76a2c-176">To retrieve app components for a business app, use the <xref:Microsoft.Dynamics.CRM.RetrieveAppComponents> function or the <xref:Microsoft.Crm.Sdk.Messages.RetrieveAppComponentsRequest> message.</span></span> <span data-ttu-id="76a2c-177">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="76a2c-177">For example:</span></span>

`GET [Organization URI]/api/data/v9.0/RetrieveAppComponents(AppModuleId=dd621d4a-d898-e711-80e7-00155db763be)`

### <a name="retrieve-security-roles-associated-with-published-business-app"></a><span data-ttu-id="76a2c-178">Retrieve security roles associated with published business app</span><span class="sxs-lookup"><span data-stu-id="76a2c-178">Retrieve security roles associated with published business app</span></span>

<span data-ttu-id="76a2c-179">To retrieve the security roles associated with your business app, use the `$expand` system query option with the **appmoduleroles_association** navigation property.</span><span class="sxs-lookup"><span data-stu-id="76a2c-179">To retrieve the security roles associated with your business app, use the `$expand` system query option with the **appmoduleroles_association** navigation property.</span></span> <span data-ttu-id="76a2c-180">For example, here is the request to retrieve all the security roles associated to a business app with ID: dd621d4a-d898-e711-80e7-00155db763be:</span><span class="sxs-lookup"><span data-stu-id="76a2c-180">For example, here is the request to retrieve all the security roles associated to a business app with ID: dd621d4a-d898-e711-80e7-00155db763be:</span></span>

`GET [Organization URI]/api/data/v9.0/appmodules(dd621d4a-d898-e711-80e7-00155db763be)?$expand=appmoduleroles_association&$select=name,appmoduleroles_association`

### <a name="delete-business-apps"></a><span data-ttu-id="76a2c-181">Delete business apps</span><span class="sxs-lookup"><span data-stu-id="76a2c-181">Delete business apps</span></span>

<span data-ttu-id="76a2c-182">Use the DELETE request to delete a business app.</span><span class="sxs-lookup"><span data-stu-id="76a2c-182">Use the DELETE request to delete a business app.</span></span> <span data-ttu-id="76a2c-183">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="76a2c-183">For example:</span></span>

`DELETE [Organization URI]/api/data/v9.0/appmodules(dd621d4a-d898-e711-80e7-00155db763be)`

## <a name="client-api-support-for-business-apps"></a><span data-ttu-id="76a2c-184">Client API support for business apps</span><span class="sxs-lookup"><span data-stu-id="76a2c-184">Client API support for business apps</span></span>

<span data-ttu-id="76a2c-185">You can use the following client APIs to work with business apps:</span><span class="sxs-lookup"><span data-stu-id="76a2c-185">You can use the following client APIs to work with business apps:</span></span>

- [<span data-ttu-id="76a2c-186">getCurrentAppName</span><span class="sxs-lookup"><span data-stu-id="76a2c-186">getCurrentAppName</span></span>](clientapi/reference/xrm-utility/getglobalcontext/getcurrentappname.md)
- [<span data-ttu-id="76a2c-187">getCurrentAppProperties</span><span class="sxs-lookup"><span data-stu-id="76a2c-187">getCurrentAppProperties</span></span>](clientapi/reference/xrm-utility/getglobalcontext/getCurrentAppProperties.md)
- [<span data-ttu-id="76a2c-188">getCurrentAppUrl</span><span class="sxs-lookup"><span data-stu-id="76a2c-188">getCurrentAppUrl</span></span>](clientapi/reference/xrm-utility/getglobalcontext/getCurrentAppUrl.md) 
  
### <a name="see-also"></a><span data-ttu-id="76a2c-189">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="76a2c-189">See also</span></span>  
[<span data-ttu-id="76a2c-190">Thiết kế ứng dụng tùy chỉnh dành cho doanh nghiệp bằng trình thiết kế ứng dụng</span><span class="sxs-lookup"><span data-stu-id="76a2c-190">Design custom business apps by using the app designer</span></span>](../customize/design-custom-business-apps-using-app-designer.md)
 
