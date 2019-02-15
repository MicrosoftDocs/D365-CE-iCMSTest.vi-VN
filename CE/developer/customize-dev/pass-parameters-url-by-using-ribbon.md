---
title: Pass parameters to a URL by using the ribbon (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: Learn about passing parameters to a URL by using the ribbon
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- ribbon
ms.assetid: 27ae5df1-fbd3-404b-bf52-40bbd2773cf6
caps.latest.revision: 24
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: db0552ec2c6c694b177cbebd335a7431c344db81
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388749"
---
# <a name="pass-parameters-to-a-url-by-using-the-ribbon"></a><span data-ttu-id="ed4cc-103">Pass parameters to a URL by using the ribbon</span><span class="sxs-lookup"><span data-stu-id="ed4cc-103">Pass parameters to a URL by using the ribbon</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ed4cc-104">Ribbon actions are defined in the `<Actions>` element of a `<CommandDefinition>` element.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-104">Ribbon actions are defined in the `<Actions>` element of a `<CommandDefinition>` element.</span></span> <span data-ttu-id="ed4cc-105">There are several ways to pass contextual [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement information as query string parameters to a URL by using the ribbon.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-105">There are several ways to pass contextual [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement information as query string parameters to a URL by using the ribbon.</span></span>  
  
-   <span data-ttu-id="ed4cc-106">Use a `<Url>` element.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-106">Use a `<Url>` element.</span></span> <span data-ttu-id="ed4cc-107">Within the `Url` element, use the **PassParams** attribute.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-107">Within the `Url` element, use the **PassParams** attribute.</span></span>  
  
-   <span data-ttu-id="ed4cc-108">Use a `<Url>` element together with a `<CrmParameter>` element.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-108">Use a `<Url>` element together with a `<CrmParameter>` element.</span></span> <span data-ttu-id="ed4cc-109">When used from a `Url` element, the name attribute value must be set.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-109">When used from a `Url` element, the name attribute value must be set.</span></span>  
  
-   <span data-ttu-id="ed4cc-110">Use a `<JavaScriptFunction>` element together with a `<CrmParameter>` element.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-110">Use a `<JavaScriptFunction>` element together with a `<CrmParameter>` element.</span></span>  
  
## <a name="use-the-passparams-attribute-to-set-dynamic-values"></a><span data-ttu-id="ed4cc-111">Use the PassParams attribute to set dynamic values</span><span class="sxs-lookup"><span data-stu-id="ed4cc-111">Use the PassParams attribute to set dynamic values</span></span>  
 <span data-ttu-id="ed4cc-112">Passing parameters to the target URL by using the **PassParams** attribute provides information to the target application about the context of the record or the user.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-112">Passing parameters to the target URL by using the **PassParams** attribute provides information to the target application about the context of the record or the user.</span></span> <span data-ttu-id="ed4cc-113">All the parameters are passed if the ribbon control is configured by using the **PassParams** attribute.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-113">All the parameters are passed if the ribbon control is configured by using the **PassParams** attribute.</span></span> <span data-ttu-id="ed4cc-114">The following table lists the parameters that are passed.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-114">The following table lists the parameters that are passed.</span></span>  
  
|<span data-ttu-id="ed4cc-115">Tham số</span><span class="sxs-lookup"><span data-stu-id="ed4cc-115">Parameter</span></span>|<span data-ttu-id="ed4cc-116">Tên</span><span class="sxs-lookup"><span data-stu-id="ed4cc-116">Name</span></span>|<span data-ttu-id="ed4cc-117">Mô tả</span><span class="sxs-lookup"><span data-stu-id="ed4cc-117">Description</span></span>|  
|---------------|----------|-----------------|  
|`typename`|<span data-ttu-id="ed4cc-118">Tên Thực thể</span><span class="sxs-lookup"><span data-stu-id="ed4cc-118">Entity Name</span></span>|<span data-ttu-id="ed4cc-119">Name of the entity.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-119">Name of the entity.</span></span> <span data-ttu-id="ed4cc-120">For custom entities, this includes the customization prefix, for example, new_entityname.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-120">For custom entities, this includes the customization prefix, for example, new_entityname.</span></span>|  
|`type`|<span data-ttu-id="ed4cc-121">Entity Type Code</span><span class="sxs-lookup"><span data-stu-id="ed4cc-121">Entity Type Code</span></span>|<span data-ttu-id="ed4cc-122">Integer that uniquely identifies the entity in the current organization.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-122">Integer that uniquely identifies the entity in the current organization.</span></span> <span data-ttu-id="ed4cc-123">**Note:**  `Entity Type Code` values are determined by the order in which an entity is created in an organization.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-123">**Note:**  `Entity Type Code` values are determined by the order in which an entity is created in an organization.</span></span> <span data-ttu-id="ed4cc-124">`Entity Type Codes` for custom entities are usually different in different organizations.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-124">`Entity Type Codes` for custom entities are usually different in different organizations.</span></span>|  
|`id`|<span data-ttu-id="ed4cc-125">Object GUID</span><span class="sxs-lookup"><span data-stu-id="ed4cc-125">Object GUID</span></span>|<span data-ttu-id="ed4cc-126">Globally unique identifier (GUID) that represents a record.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-126">Globally unique identifier (GUID) that represents a record.</span></span>|  
|`orgname`|<span data-ttu-id="ed4cc-127">Tên tổ chức</span><span class="sxs-lookup"><span data-stu-id="ed4cc-127">Organization Name</span></span>|<span data-ttu-id="ed4cc-128">Unique name of the organization.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-128">Unique name of the organization.</span></span>|  
|`userlcid`|<span data-ttu-id="ed4cc-129">User Language Code</span><span class="sxs-lookup"><span data-stu-id="ed4cc-129">User Language Code</span></span>|<span data-ttu-id="ed4cc-130">Language code identifier that is used by the current user.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-130">Language code identifier that is used by the current user.</span></span>|  
|`orglcid`|<span data-ttu-id="ed4cc-131">Organization Language Code</span><span class="sxs-lookup"><span data-stu-id="ed4cc-131">Organization Language Code</span></span>|<span data-ttu-id="ed4cc-132">Language code identifier that represents the base language for the organization.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-132">Language code identifier that represents the base language for the organization.</span></span>|  
  
[!INCLUDE[languagecode](../../includes/languagecode.md)]
  
> [!NOTE]
>  <span data-ttu-id="ed4cc-133">We recommend that you use the entity name instead of the entity type code because the entity type code may be different between [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] installations.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-133">We recommend that you use the entity name instead of the entity type code because the entity type code may be different between [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] installations.</span></span>  
  
### <a name="example"></a><span data-ttu-id="ed4cc-134">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="ed4cc-134">Example</span></span>  
 <span data-ttu-id="ed4cc-135">The following sample shows the URL without parameters:</span><span class="sxs-lookup"><span data-stu-id="ed4cc-135">The following sample shows the URL without parameters:</span></span>  
  
```  
http://myserver/mypage.aspx  
```  
  
 <span data-ttu-id="ed4cc-136">The following sample shows the parameters included when the ribbon control is presented for the account entity, for an organization called ‘AdventureWorksCycle’, when the user’s language and the organization base language is English, and the GUID for the account record is DBD5DBFB-0666-DC11-A5D9-0003FF9CE217:</span><span class="sxs-lookup"><span data-stu-id="ed4cc-136">The following sample shows the parameters included when the ribbon control is presented for the account entity, for an organization called ‘AdventureWorksCycle’, when the user’s language and the organization base language is English, and the GUID for the account record is DBD5DBFB-0666-DC11-A5D9-0003FF9CE217:</span></span>  
  
```  
http://myserver/mypage.aspx?orgname=AdventureWorksCycle&userlcid=1033&orglcid=1033&type=1&typename=account&id=%7BDBD5DBFB-0666-DC11-A5D9-0003FF9CE217%7D  
```  
  
## <a name="use-a-querystring-parameter-in-the-url"></a><span data-ttu-id="ed4cc-137">Use a Querystring parameter in the URL</span><span class="sxs-lookup"><span data-stu-id="ed4cc-137">Use a Querystring parameter in the URL</span></span>  
 <span data-ttu-id="ed4cc-138">You can include a `querystring` parameter in the URL attribute.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-138">You can include a `querystring` parameter in the URL attribute.</span></span> <span data-ttu-id="ed4cc-139">This can be very useful if you want to open a specific [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] record or view by using [Open forms, views, dialogs, and reports with a URL](../open-forms-views-dialogs-reports-url.md).</span><span class="sxs-lookup"><span data-stu-id="ed4cc-139">This can be very useful if you want to open a specific [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] record or view by using [Open forms, views, dialogs, and reports with a URL](../open-forms-views-dialogs-reports-url.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ed4cc-140">You will not be able to import the ribbon if the URL includes the ampersand (&) character that is used to separate multiple `querystring` parameters in the URL.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-140">You will not be able to import the ribbon if the URL includes the ampersand (&) character that is used to separate multiple `querystring` parameters in the URL.</span></span> <span data-ttu-id="ed4cc-141">This character makes the XML invalid.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-141">This character makes the XML invalid.</span></span> <span data-ttu-id="ed4cc-142">You must escape the ampersand character in the URL attribute value with "&amp;".</span><span class="sxs-lookup"><span data-stu-id="ed4cc-142">You must escape the ampersand character in the URL attribute value with "&amp;".</span></span>  
  
## <a name="reading-passed-parameters"></a><span data-ttu-id="ed4cc-143">Reading passed parameters</span><span class="sxs-lookup"><span data-stu-id="ed4cc-143">Reading passed parameters</span></span>  
 <span data-ttu-id="ed4cc-144">Passed parameters are usually read in the target .aspx page by using the `HttpRequest.QueryString` property.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-144">Passed parameters are usually read in the target .aspx page by using the `HttpRequest.QueryString` property.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ed4cc-145">[HttpRequest.QueryString Property](https://msdn.microsoft.com/library/system.web.httprequest.querystring.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed4cc-145">[HttpRequest.QueryString Property](https://msdn.microsoft.com/library/system.web.httprequest.querystring.aspx)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ed4cc-146">If the target of your URL is a Web resource, it can accept only the parameters identified in the topic [Passing Parameters to HTMLWeb Resources](../webpage-html-web-resources.md#BKMK_PassingParametersToWebResources).</span><span class="sxs-lookup"><span data-stu-id="ed4cc-146">If the target of your URL is a Web resource, it can accept only the parameters identified in the topic [Passing Parameters to HTMLWeb Resources](../webpage-html-web-resources.md#BKMK_PassingParametersToWebResources).</span></span> <span data-ttu-id="ed4cc-147">The only opportunity to pass custom values is by including them within the `data` parameter.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-147">The only opportunity to pass custom values is by including them within the `data` parameter.</span></span> <span data-ttu-id="ed4cc-148">Some special handling is required to include multiple values in a single parameter.</span><span class="sxs-lookup"><span data-stu-id="ed4cc-148">Some special handling is required to include multiple values in a single parameter.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ed4cc-149">[Sample: Passing Multiple Values to a Web Page Web Resource Through the Data Parameter](../sample-pass-multiple-values-web-resource-through-data-parameter.md)</span><span class="sxs-lookup"><span data-stu-id="ed4cc-149">[Sample: Passing Multiple Values to a Web Page Web Resource Through the Data Parameter](../sample-pass-multiple-values-web-resource-through-data-parameter.md)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ed4cc-150">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ed4cc-150">See also</span></span>

 <span data-ttu-id="ed4cc-151">[Customize commands and the ribbon](customize-commands-ribbon.md) </span><span class="sxs-lookup"><span data-stu-id="ed4cc-151">[Customize commands and the ribbon](customize-commands-ribbon.md) </span></span>  
 <span data-ttu-id="ed4cc-152">[Open Forms And Views with a URL](../open-forms-views-dialogs-reports-url.md)  </span><span class="sxs-lookup"><span data-stu-id="ed4cc-152">[Open Forms And Views with a URL](../open-forms-views-dialogs-reports-url.md)  </span></span>  
 <span data-ttu-id="ed4cc-153">[Define Ribbon Tab Display Rules](define-ribbon-tab-display-rules.md) </span><span class="sxs-lookup"><span data-stu-id="ed4cc-153">[Define Ribbon Tab Display Rules](define-ribbon-tab-display-rules.md) </span></span>  
 [<span data-ttu-id="ed4cc-154">Sample: Export Ribbon Definitions</span><span class="sxs-lookup"><span data-stu-id="ed4cc-154">Sample: Export Ribbon Definitions</span></span>](sample-export-ribbon-definitions.md)
