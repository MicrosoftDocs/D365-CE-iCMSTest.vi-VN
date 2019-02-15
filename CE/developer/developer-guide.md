---
title: Developer Guide for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: This SDK contains a wealth of resources, including code samples, which are designed to help you build powerful vertical applications using the Customer Engagement platform. It is a guide for developers writing solutions, server-side code, client applications and extensions, custom business logic, plug-ins, integration modules, custom workflow modules and more. The SDK contains an architectural overview of Customer Engagement, the entity model, security model, web services, and sample code.
ms.custom: ''
ms.date: 12/15/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: e926cfed-f581-4f1f-83bd-75a06292212b
author: JimDaly
ms.author: jdaly
manager: amyla
tags:
- aug2017
- MigrationHO
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9db6529499c9c0d283ac8b52dd336b290364decf
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385879"
---
# <a name="developer-guide-for-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="6401a-105">Developer Guide for Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="6401a-105">Developer Guide for Dynamics 365 for Customer Engagement apps</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6401a-106">Welcome to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]  apps Developer Guide (formerly referred to as the Dynamics 365 for Customer Engagement apps SDK).</span><span class="sxs-lookup"><span data-stu-id="6401a-106">Welcome to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]  apps Developer Guide (formerly referred to as the Dynamics 365 for Customer Engagement apps SDK).</span></span> <span data-ttu-id="6401a-107">This documentation is for version 9.0.</span><span class="sxs-lookup"><span data-stu-id="6401a-107">This documentation is for version 9.0.</span></span>

<table>
<tr>
<td>

<h2> <span data-ttu-id="6401a-108">Bắt đầu</span><span class="sxs-lookup"><span data-stu-id="6401a-108">Get started</span></span> </h2>
<li><span data-ttu-id="6401a-109"><a href="get-started-sdk.md" data-raw-source="[Get started with the SDK](get-started-sdk.md)">Get started with the SDK</a></span><span class="sxs-lookup"><span data-stu-id="6401a-109"><a href="get-started-sdk.md" data-raw-source="[Get started with the SDK](get-started-sdk.md)">Get started with the SDK</a></span></span></li>
<li><span data-ttu-id="6401a-110"><a href="developer-tools.md" data-raw-source="[Developer tools](developer-tools.md)">Developer tools</a></span><span class="sxs-lookup"><span data-stu-id="6401a-110"><a href="developer-tools.md" data-raw-source="[Developer tools](developer-tools.md)">Developer tools</a></span></span></li>
<li><span data-ttu-id="6401a-111"><a href="choose-development-style.md" data-raw-source="[Choose your development style](choose-development-style.md)">Choose your development style</a></span><span class="sxs-lookup"><span data-stu-id="6401a-111"><a href="choose-development-style.md" data-raw-source="[Choose your development style](choose-development-style.md)">Choose your development style</a></span></span></li>
<li><span data-ttu-id="6401a-112"><a href="security-dev/security-model.md" data-raw-source="[Understand security model](security-dev/security-model.md)">Understand security model</a></span><span class="sxs-lookup"><span data-stu-id="6401a-112"><a href="security-dev/security-model.md" data-raw-source="[Understand security model](security-dev/security-model.md)">Understand security model</a></span></span></li>
</td>
<td>

<h2> <span data-ttu-id="6401a-113">Kết nối</span><span class="sxs-lookup"><span data-stu-id="6401a-113">Connect</span></span> </h2>

<li><span data-ttu-id="6401a-114"><a href="connect-customer-engagement-web-services-using-oauth.md" data-raw-source="[Using OAuth](connect-customer-engagement-web-services-using-oauth.md)">Using OAuth</a></span><span class="sxs-lookup"><span data-stu-id="6401a-114"><a href="connect-customer-engagement-web-services-using-oauth.md" data-raw-source="[Using OAuth](connect-customer-engagement-web-services-using-oauth.md)">Using OAuth</a></span></span></li>
<li><span data-ttu-id="6401a-115"><a href="oauth-cross-origin-resource-sharing-connect-single-page-application.md" data-raw-source="[Using Oauth with CORS](oauth-cross-origin-resource-sharing-connect-single-page-application.md)">Using Oauth with CORS</a></span><span class="sxs-lookup"><span data-stu-id="6401a-115"><a href="oauth-cross-origin-resource-sharing-connect-single-page-application.md" data-raw-source="[Using Oauth with CORS](oauth-cross-origin-resource-sharing-connect-single-page-application.md)">Using Oauth with CORS</a></span></span></li>
<li><span data-ttu-id="6401a-116"><a href="active-directory-claims-based-authentication.md" data-raw-source="[Active Directory and claims-based auth](active-directory-claims-based-authentication.md)">Active Directory and claims-based auth</a></span><span class="sxs-lookup"><span data-stu-id="6401a-116"><a href="active-directory-claims-based-authentication.md" data-raw-source="[Active Directory and claims-based auth](active-directory-claims-based-authentication.md)">Active Directory and claims-based auth</a></span></span></li>
<li><span data-ttu-id="6401a-117"><a href="build-windows-client-applications-xrm-tools.md" data-raw-source="[XRM tooling](build-windows-client-applications-xrm-tools.md)">XRM tooling</a></span><span class="sxs-lookup"><span data-stu-id="6401a-117"><a href="build-windows-client-applications-xrm-tools.md" data-raw-source="[XRM tooling](build-windows-client-applications-xrm-tools.md)">XRM tooling</a></span></span></li>
<li><span data-ttu-id="6401a-118"><a href="build-web-applications-server-server-s2s-authentication.md" data-raw-source="[Server-to-Server (S2S) auth](build-web-applications-server-server-s2s-authentication.md)">Server-to-Server (S2S) auth</a></span><span class="sxs-lookup"><span data-stu-id="6401a-118"><a href="build-web-applications-server-server-s2s-authentication.md" data-raw-source="[Server-to-Server (S2S) auth](build-web-applications-server-server-s2s-authentication.md)">Server-to-Server (S2S) auth</a></span></span></li>
</td>
</tr>

<tr>
<td>
<h2> <span data-ttu-id="6401a-119">Manage customer data</span><span class="sxs-lookup"><span data-stu-id="6401a-119">Manage customer data</span></span> </h2>

<li><span data-ttu-id="6401a-120"><a href="model-business-data.md" data-raw-source="[Model your business data](model-business-data.md)">Model your business data</a></span><span class="sxs-lookup"><span data-stu-id="6401a-120"><a href="model-business-data.md" data-raw-source="[Model your business data](model-business-data.md)">Model your business data</a></span></span></li>
<li><span data-ttu-id="6401a-121"><a href="audit-entity-data-changes.md" data-raw-source="[Audit data changes](audit-entity-data-changes.md)">Kiểm tra những thay đổi về dữ liệu</a></span><span class="sxs-lookup"><span data-stu-id="6401a-121"><a href="audit-entity-data-changes.md" data-raw-source="[Audit data changes](audit-entity-data-changes.md)">Audit data changes</a></span></span></li>
<li><span data-ttu-id="6401a-122"><a href="detect-duplicate-data-for-developers.md" data-raw-source="[Detect duplicate data](detect-duplicate-data-for-developers.md)">Phát dữ liệu trùng lặp</a></span><span class="sxs-lookup"><span data-stu-id="6401a-122"><a href="detect-duplicate-data-for-developers.md" data-raw-source="[Detect duplicate data](detect-duplicate-data-for-developers.md)">Detect duplicate data</a></span></span></li>
<li><span data-ttu-id="6401a-123"><a href="import-data.md" data-raw-source="[Import data](import-data.md)">Nhập dữ liệu</a></span><span class="sxs-lookup"><span data-stu-id="6401a-123"><a href="import-data.md" data-raw-source="[Import data](import-data.md)">Import data</a></span></span></li>
<li><span data-ttu-id="6401a-124"><a href="virtual-entities/get-started-ve.md" data-raw-source="[Virtual entities](virtual-entities/get-started-ve.md)">Thực thể ảo</a></span><span class="sxs-lookup"><span data-stu-id="6401a-124"><a href="virtual-entities/get-started-ve.md" data-raw-source="[Virtual entities](virtual-entities/get-started-ve.md)">Virtual entities</a></span></span></li>
</td>
<td>
<h2> <span data-ttu-id="6401a-125">Use web services</span><span class="sxs-lookup"><span data-stu-id="6401a-125">Use web services</span></span></h2>

<li><span data-ttu-id="6401a-126"><a href="use-microsoft-dynamics-365-web-api.md" data-raw-source="[Web API](use-microsoft-dynamics-365-web-api.md)">API Web</a></span><span class="sxs-lookup"><span data-stu-id="6401a-126"><a href="use-microsoft-dynamics-365-web-api.md" data-raw-source="[Web API](use-microsoft-dynamics-365-web-api.md)">Web API</a></span></span></li>
<li><span data-ttu-id="6401a-127"><a href="org-service/get-started-managed-code-application-development.md" data-raw-source="[Organization service](org-service/get-started-managed-code-application-development.md)">Organization service</a></span><span class="sxs-lookup"><span data-stu-id="6401a-127"><a href="org-service/get-started-managed-code-application-development.md" data-raw-source="[Organization service](org-service/get-started-managed-code-application-development.md)">Organization service</a></span></span></li>
<li><span data-ttu-id="6401a-128"><a href="use-discovery-service.md" data-raw-source="[Discovery service](use-discovery-service.md)">Discovery service</a></span><span class="sxs-lookup"><span data-stu-id="6401a-128"><a href="use-discovery-service.md" data-raw-source="[Discovery service](use-discovery-service.md)">Discovery service</a></span></span></li>
<li><span data-ttu-id="6401a-129"><a href="online-management-api.md" data-raw-source="[Online Management API](online-management-api.md)">API Quản lý Trực tuyến</a></span><span class="sxs-lookup"><span data-stu-id="6401a-129"><a href="online-management-api.md" data-raw-source="[Online Management API](online-management-api.md)">Online Management API</a></span></span></li>
</td>
</tr>

<tr>
<td>
<h2> <span data-ttu-id="6401a-130">Mở rộng</span><span class="sxs-lookup"><span data-stu-id="6401a-130">Extend</span></span> </h2>
<li><span data-ttu-id="6401a-131"><a href="create-manage-custom-business-apps-using-code.md" data-raw-source="[Custom business apps](create-manage-custom-business-apps-using-code.md)">Custom business apps</a></span><span class="sxs-lookup"><span data-stu-id="6401a-131"><a href="create-manage-custom-business-apps-using-code.md" data-raw-source="[Custom business apps](create-manage-custom-business-apps-using-code.md)">Custom business apps</a></span></span></li>
<li><span data-ttu-id="6401a-132"><a href="write-plugin-extend-business-processes.md" data-raw-source="[Plug-ins](write-plugin-extend-business-processes.md)">Phần bổ trợ</a></span><span class="sxs-lookup"><span data-stu-id="6401a-132"><a href="write-plugin-extend-business-processes.md" data-raw-source="[Plug-ins](write-plugin-extend-business-processes.md)">Plug-ins</a></span></span></li>
<li><span data-ttu-id="6401a-133"><a href="automate-business-processes-customer-engagement.md" data-raw-source="[Automate business processes](automate-business-processes-customer-engagement.md)">Quy trình công việc tự động</a></span><span class="sxs-lookup"><span data-stu-id="6401a-133"><a href="automate-business-processes-customer-engagement.md" data-raw-source="[Automate business processes](automate-business-processes-customer-engagement.md)">Automate business processes</a></span></span></li>
<li><span data-ttu-id="6401a-134"><a href="asynchronous-service.md" data-raw-source="[Asynchronous service](asynchronous-service.md)">Asynchronous service</a></span><span class="sxs-lookup"><span data-stu-id="6401a-134"><a href="asynchronous-service.md" data-raw-source="[Asynchronous service](asynchronous-service.md)">Asynchronous service</a></span></span></li>
<li><span data-ttu-id="6401a-135"><a href="azure-extensions.md" data-raw-source="[Azure extensions](azure-extensions.md)">Azure extensions</a></span><span class="sxs-lookup"><span data-stu-id="6401a-135"><a href="azure-extensions.md" data-raw-source="[Azure extensions](azure-extensions.md)">Azure extensions</a></span></span></li>
<li><span data-ttu-id="6401a-136"><a href="use-webhooks.md" data-raw-source="[Webhooks](use-webhooks.md)">Webhooks</a></span><span class="sxs-lookup"><span data-stu-id="6401a-136"><a href="use-webhooks.md" data-raw-source="[Webhooks](use-webhooks.md)">Webhooks</a></span></span></li>
<li><span data-ttu-id="6401a-137"><a href="clientapi/client-scripting.md" data-raw-source="[Client scripting (Client API)](clientapi/client-scripting.md)">Client scripting (Client API)</a></span><span class="sxs-lookup"><span data-stu-id="6401a-137"><a href="clientapi/client-scripting.md" data-raw-source="[Client scripting (Client API)](clientapi/client-scripting.md)">Client scripting (Client API)</a></span></span></li>
</td>
<td>

<h2> <span data-ttu-id="6401a-138">Tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="6401a-138">Customize</span></span> </h2>

<li><span data-ttu-id="6401a-139"><a href="customize-dev/customize-entity-forms.md" data-raw-source="[Entity forms](customize-dev/customize-entity-forms.md)">Entity forms</a></span><span class="sxs-lookup"><span data-stu-id="6401a-139"><a href="customize-dev/customize-entity-forms.md" data-raw-source="[Entity forms](customize-dev/customize-entity-forms.md)">Entity forms</a></span></span></li>
<li><span data-ttu-id="6401a-140"><a href="customize-dev/customize-entity-views.md" data-raw-source="[Entity views](customize-dev/customize-entity-views.md)">Dạng xem thực thể</a></span><span class="sxs-lookup"><span data-stu-id="6401a-140"><a href="customize-dev/customize-entity-views.md" data-raw-source="[Entity views](customize-dev/customize-entity-views.md)">Entity views</a></span></span></li>
<li><span data-ttu-id="6401a-141"><a href="customize-dev/customize-visualizations-dashboards.md" data-raw-source="[Visualizations and dashboards](customize-dev/customize-visualizations-dashboards.md)">Visualizations and dashboards</a></span><span class="sxs-lookup"><span data-stu-id="6401a-141"><a href="customize-dev/customize-visualizations-dashboards.md" data-raw-source="[Visualizations and dashboards](customize-dev/customize-visualizations-dashboards.md)">Visualizations and dashboards</a></span></span></li>
<li><span data-ttu-id="6401a-142"><a href="customize-dev/customize-commands-ribbon.md" data-raw-source="[Commands and the ribbon](customize-dev/customize-commands-ribbon.md)">Commands and the ribbon</a></span><span class="sxs-lookup"><span data-stu-id="6401a-142"><a href="customize-dev/customize-commands-ribbon.md" data-raw-source="[Commands and the ribbon](customize-dev/customize-commands-ribbon.md)">Commands and the ribbon</a></span></span></li>
<li><span data-ttu-id="6401a-143"><a href="customize-dev/when-edit-customization-file.md" data-raw-source="[Edit customizations file](customize-dev/when-edit-customization-file.md)">Edit customizations file</a></span><span class="sxs-lookup"><span data-stu-id="6401a-143"><a href="customize-dev/when-edit-customization-file.md" data-raw-source="[Edit customizations file](customize-dev/when-edit-customization-file.md)">Edit customizations file</a></span></span></li>
</td>
</tr>

<tr>
<td>
<h2> <span data-ttu-id="6401a-144">Package extensions and customizations</span><span class="sxs-lookup"><span data-stu-id="6401a-144">Package extensions and customizations</span></span> </h2>
<li><span data-ttu-id="6401a-145"><a href="package-distribute-extensions-use-solutions.md" data-raw-source="[Use solutions](package-distribute-extensions-use-solutions.md)">Sử dụng các giải pháp</a></span><span class="sxs-lookup"><span data-stu-id="6401a-145"><a href="package-distribute-extensions-use-solutions.md" data-raw-source="[Use solutions](package-distribute-extensions-use-solutions.md)">Use solutions</a></span></span></li>
<li><span data-ttu-id="6401a-146"><a href="create-packages-package-deployer.md" data-raw-source="[Use Package Deployer](create-packages-package-deployer.md)">Use Package Deployer</a></span><span class="sxs-lookup"><span data-stu-id="6401a-146"><a href="create-packages-package-deployer.md" data-raw-source="[Use Package Deployer](create-packages-package-deployer.md)">Use Package Deployer</a></span></span></li>
<li><span data-ttu-id="6401a-147"><a href="compress-extract-solution-file-solutionpackager.md" data-raw-source="[Use SolutionPackager](compress-extract-solution-file-solutionpackager.md)">Use SolutionPackager</a></span><span class="sxs-lookup"><span data-stu-id="6401a-147"><a href="compress-extract-solution-file-solutionpackager.md" data-raw-source="[Use SolutionPackager](compress-extract-solution-file-solutionpackager.md)">Use SolutionPackager</a></span></span></li>
<li><span data-ttu-id="6401a-148"><a href="publish-app-appsource.md" data-raw-source="[Publish your app on AppSource](publish-app-appsource.md)">Publish your app on AppSource</a></span><span class="sxs-lookup"><span data-stu-id="6401a-148"><a href="publish-app-appsource.md" data-raw-source="[Publish your app on AppSource](publish-app-appsource.md)">Publish your app on AppSource</a></span></span></li>
</td>

<td>
<h2> <span data-ttu-id="6401a-149">Tham chiếu chương trình</span><span class="sxs-lookup"><span data-stu-id="6401a-149">Programming reference</span></span> </h2>

<li><span data-ttu-id="6401a-150"><a href="about-entity-reference.md" data-raw-source="[Entity Reference](about-entity-reference.md)">Tham chiếu Thực thể</a></span><span class="sxs-lookup"><span data-stu-id="6401a-150"><a href="about-entity-reference.md" data-raw-source="[Entity Reference](about-entity-reference.md)">Entity Reference</a></span></span></li>
<li><span data-ttu-id="6401a-151"><a href="/dynamics365/customer-engagement/web-api/about" data-raw-source="[Web API Reference](/dynamics365/customer-engagement/web-api/about)">Tham chiếu API Web</a></span><span class="sxs-lookup"><span data-stu-id="6401a-151"><a href="/dynamics365/customer-engagement/web-api/about" data-raw-source="[Web API Reference](/dynamics365/customer-engagement/web-api/about)">Web API Reference</a></span></span></li>
<li><span data-ttu-id="6401a-152"><a href="https://docs.microsoft.com/dotnet/api/?view=dynamics-general-ce-9" data-raw-source="[Organization Service Reference](https://docs.microsoft.com/dotnet/api/?view=dynamics-general-ce-9)">Organization Service Reference</a></span><span class="sxs-lookup"><span data-stu-id="6401a-152"><a href="https://docs.microsoft.com/dotnet/api/?view=dynamics-general-ce-9" data-raw-source="[Organization Service Reference](https://docs.microsoft.com/dotnet/api/?view=dynamics-general-ce-9)">Organization Service Reference</a></span></span></li>
<li><span data-ttu-id="6401a-153"><a href="clientapi/reference.md" data-raw-source="[Client API Reference](clientapi/reference.md)">Client API Reference</a></span><span class="sxs-lookup"><span data-stu-id="6401a-153"><a href="clientapi/reference.md" data-raw-source="[Client API Reference](clientapi/reference.md)">Client API Reference</a></span></span></li>
</td>
</tr>

<tr>
<td>
<h2> <span data-ttu-id="6401a-154">Tài nguyên bổ sung</span><span class="sxs-lookup"><span data-stu-id="6401a-154">Additional resources</span></span> </h2>

<li><span data-ttu-id="6401a-155"><a href="../field-service/developer/connected-field-service-developer-guide.md" data-raw-source="[Developer Guide for Connected Field Service](../field-service/developer/connected-field-service-developer-guide.md)">Developer Guide for Connected Field Service</a></span><span class="sxs-lookup"><span data-stu-id="6401a-155"><a href="../field-service/developer/connected-field-service-developer-guide.md" data-raw-source="[Developer Guide for Connected Field Service](../field-service/developer/connected-field-service-developer-guide.md)">Developer Guide for Connected Field Service</a></span></span></li>
<!--<li>[Developer Guide for Dynamics 365 for Customer Engagement for Marketing](../marketing/developer/marketing-developer-guide.md)</li>-->
<li><span data-ttu-id="6401a-156"><a href="sample-code-directory.md" data-raw-source="[Sample code directory](sample-code-directory.md)">Sample code directory</a></span><span class="sxs-lookup"><span data-stu-id="6401a-156"><a href="sample-code-directory.md" data-raw-source="[Sample code directory](sample-code-directory.md)">Sample code directory</a></span></span></li>
<li><span data-ttu-id="6401a-157"><a href="download-tools-nuget.md" data-raw-source="[Tools on NuGet](download-tools-nuget.md)">Tools on NuGet</a></span><span class="sxs-lookup"><span data-stu-id="6401a-157"><a href="download-tools-nuget.md" data-raw-source="[Tools on NuGet](download-tools-nuget.md)">Tools on NuGet</a></span></span></li>
</td>

<td>

</td>
</tr>


</table>


### <a name="see-also"></a><span data-ttu-id="6401a-158">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6401a-158">See also</span></span>

[<span data-ttu-id="6401a-159">Hướng dẫn cho Quản trị viên</span><span class="sxs-lookup"><span data-stu-id="6401a-159">Administrator Guide</span></span>](../admin/admin-guide.md)

[<span data-ttu-id="6401a-160">Hướng dẫn Tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="6401a-160">Customization Guide</span></span>](../customize/overview.md)

[<span data-ttu-id="6401a-161">Unified Service Desk Guide</span><span class="sxs-lookup"><span data-stu-id="6401a-161">Unified Service Desk Guide</span></span>](/dynamics365/customer-engagement/unified-service-desk/unified-service-desk)


