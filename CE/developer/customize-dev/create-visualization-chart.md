---
title: Create a visualization (chart) (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs
description: 'The topic shows how to create a chart visualization and a web resource visualization. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: a93ac45e-aa61-4a0b-be4c-f63ccc4a2c91
caps.latest.revision: 42
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3d5b1250689eca72d3d9b388d136d7606cca2fa2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388562"
---
# <a name="create-a-visualization-chart"></a><span data-ttu-id="12151-103">Create a visualization (chart)</span><span class="sxs-lookup"><span data-stu-id="12151-103">Create a visualization (chart)</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="12151-104">To create a visualization programmatically, you must create a record for the [SavedQueryVisualization Entity](../entities/savedqueryvisualization.md) or [UserQueryVisualization Entity](../entities/userqueryvisualization.md) entity to create an organization-owned or user-owned chart respectively.</span><span class="sxs-lookup"><span data-stu-id="12151-104">To create a visualization programmatically, you must create a record for the [SavedQueryVisualization Entity](../entities/savedqueryvisualization.md) or [UserQueryVisualization Entity](../entities/userqueryvisualization.md) entity to create an organization-owned or user-owned chart respectively.</span></span> <span data-ttu-id="12151-105">This topic shows how to create a chart visualization and a web resource visualization.</span><span class="sxs-lookup"><span data-stu-id="12151-105">This topic shows how to create a chart visualization and a web resource visualization.</span></span>  
  
<a name="Before"></a>   

## <a name="before-you-create-a-visualization"></a><span data-ttu-id="12151-106">Before you create a visualization</span><span class="sxs-lookup"><span data-stu-id="12151-106">Before you create a visualization</span></span>  

 <span data-ttu-id="12151-107">Before creating a visualization, make sure that you are aware of the following:</span><span class="sxs-lookup"><span data-stu-id="12151-107">Before creating a visualization, make sure that you are aware of the following:</span></span>  
  
- <span data-ttu-id="12151-108">**Type of visualization**: If you want your visualizations to be available across the organization and don’t want to manage the access levels at a more detailed level, you might want to create an organization-owned visualization.</span><span class="sxs-lookup"><span data-stu-id="12151-108">**Type of visualization**: If you want your visualizations to be available across the organization and don’t want to manage the access levels at a more detailed level, you might want to create an organization-owned visualization.</span></span> <span data-ttu-id="12151-109">However, if you’re concerned about the access privileges and security of your visualization, consider creating a user-owned visualization where you have more control over who can access it.</span><span class="sxs-lookup"><span data-stu-id="12151-109">However, if you’re concerned about the access privileges and security of your visualization, consider creating a user-owned visualization where you have more control over who can access it.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="12151-110">Organization-owned visualizations can only be created by those users who have the System Administrator or System Customizer role.</span><span class="sxs-lookup"><span data-stu-id="12151-110">Organization-owned visualizations can only be created by those users who have the System Administrator or System Customizer role.</span></span>  
  
- <span data-ttu-id="12151-111">**Associated Entity**: Visualizations are attached to entities.</span><span class="sxs-lookup"><span data-stu-id="12151-111">**Associated Entity**: Visualizations are attached to entities.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="12151-112">[Entities Supported for Visualizations](view-data-with-visualizations-charts.md#SupportedVisualizationEntities).</span><span class="sxs-lookup"><span data-stu-id="12151-112">[Entities Supported for Visualizations](view-data-with-visualizations-charts.md#SupportedVisualizationEntities).</span></span> <span data-ttu-id="12151-113">You can attach a chart to a supported entity by using the [SavedQueryVisualization.PrimaryEntityTypeCode](../entities/savedqueryvisualization.md#BKMK_PrimaryEntityTypeCode) or [UserQueryVisualization.PrimaryEntityTypeCode](../entities/userqueryvisualization.md#BKMK_PrimaryEntityTypeCode) attribute.</span><span class="sxs-lookup"><span data-stu-id="12151-113">You can attach a chart to a supported entity by using the [SavedQueryVisualization.PrimaryEntityTypeCode](../entities/savedqueryvisualization.md#BKMK_PrimaryEntityTypeCode) or [UserQueryVisualization.PrimaryEntityTypeCode](../entities/userqueryvisualization.md#BKMK_PrimaryEntityTypeCode) attribute.</span></span>  
  
<a name="CreateChart"></a>   

## <a name="create-a-chart-visualization"></a><span data-ttu-id="12151-114">Create a chart visualization</span><span class="sxs-lookup"><span data-stu-id="12151-114">Create a chart visualization</span></span>  

 <span data-ttu-id="12151-115">Charts require you to specify the underlying data for the charts and how the charts will look in the form of *data description* and *presentation description* XML strings.</span><span class="sxs-lookup"><span data-stu-id="12151-115">Charts require you to specify the underlying data for the charts and how the charts will look in the form of *data description* and *presentation description* XML strings.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="12151-116">[Specifying Chart Data](understand-charts-underlying-data-chart-representation.md) and [Sample Charts](sample-charts.md).</span><span class="sxs-lookup"><span data-stu-id="12151-116">[Specifying Chart Data](understand-charts-underlying-data-chart-representation.md) and [Sample Charts](sample-charts.md).</span></span>  
  
 <span data-ttu-id="12151-117">For a complete sample on how to create an organization-owned chart, see [Sample: Create, Retrieve, Update, and Delete (CRUD) a Chart](sample-create-retrieve-update-delete-chart.md).</span><span class="sxs-lookup"><span data-stu-id="12151-117">For a complete sample on how to create an organization-owned chart, see [Sample: Create, Retrieve, Update, and Delete (CRUD) a Chart](sample-create-retrieve-update-delete-chart.md).</span></span>  
  
### <a name="create-a-multi-series-chart"></a><span data-ttu-id="12151-118">Create a multi-series chart</span><span class="sxs-lookup"><span data-stu-id="12151-118">Create a multi-series chart</span></span>  

 <span data-ttu-id="12151-119">Multi-series charts map multiple series (vertical) axis values to a single category (horizontal) axis value.</span><span class="sxs-lookup"><span data-stu-id="12151-119">Multi-series charts map multiple series (vertical) axis values to a single category (horizontal) axis value.</span></span> <span data-ttu-id="12151-120">The only difference from a single series chart is that these charts have multiple `<measurecollection>` and corresponding `<series>` elements specified in the XML strings.</span><span class="sxs-lookup"><span data-stu-id="12151-120">The only difference from a single series chart is that these charts have multiple `<measurecollection>` and corresponding `<series>` elements specified in the XML strings.</span></span> <span data-ttu-id="12151-121">Each `<measurecollection>` element contains a child element called `<measure>` that defines a series (vertical) axis value for the same category (horizontal) value.</span><span class="sxs-lookup"><span data-stu-id="12151-121">Each `<measurecollection>` element contains a child element called `<measure>` that defines a series (vertical) axis value for the same category (horizontal) value.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="12151-122">[Understanding Charts: Underlying Data and Chart Representation](understand-charts-underlying-data-chart-representation.md).</span><span class="sxs-lookup"><span data-stu-id="12151-122">[Understanding Charts: Underlying Data and Chart Representation](understand-charts-underlying-data-chart-representation.md).</span></span>  
  
 <span data-ttu-id="12151-123">For a sample multi-series chart and the corresponding data description and presentation descriptions XML strings, see [Multi-Series Chart](sample-charts.md#MultiSeriesChart).</span><span class="sxs-lookup"><span data-stu-id="12151-123">For a sample multi-series chart and the corresponding data description and presentation descriptions XML strings, see [Multi-Series Chart](sample-charts.md#MultiSeriesChart).</span></span>  
  
<a name="CreateWRVisualization"></a>   

## <a name="create-a-web-resource-visualization"></a><span data-ttu-id="12151-124">Create a web resource visualization</span><span class="sxs-lookup"><span data-stu-id="12151-124">Create a web resource visualization</span></span>  

 <span data-ttu-id="12151-125">Visualizations containing web resources don’t require you to specify the data description and presentation description XML strings.</span><span class="sxs-lookup"><span data-stu-id="12151-125">Visualizations containing web resources don’t require you to specify the data description and presentation description XML strings.</span></span> <span data-ttu-id="12151-126">The following sample demonstrates how to create an organization-owned visualization containing a web resource by using the SDK.</span><span class="sxs-lookup"><span data-stu-id="12151-126">The following sample demonstrates how to create an organization-owned visualization containing a web resource by using the SDK.</span></span>  
  
```csharp  
SavedQueryVisualization newWebResourceVisualization = new SavedQueryVisualization()  
{  
   Name = "Sample Dashboard Visualization",  
   Description = "Sample organization-owned visualization",  
                           PrimaryEntityTypeCode = Account.EntityLogicalName,  
   WebResourceId = new EntityReference(WebResource.EntityLogicalName, _webResourceId))  
  
};  
_orgOwnedVisualizationId = _serviceProxy.Create(newWebResourceVisualization);  
  
```  
  
 <span data-ttu-id="12151-127">If you want to create a web resource visualization by using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement web application, you must create an XML file in the following format, and then use **Import Chart** in the ribbon to import the visualization.</span><span class="sxs-lookup"><span data-stu-id="12151-127">If you want to create a web resource visualization by using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement web application, you must create an XML file in the following format, and then use **Import Chart** in the ribbon to import the visualization.</span></span>  
  
```xml  
<visualization>  
  <name>Visualization_Name</name>  
  <description>Description</description>  
  <webresourcename>Name_Of_An_Existing_Web_Resource</webresourcename>  
  <primaryentitytypecode>Entity_Logical_Name</primaryentitytypecode>  
  <isdefault>Value: true or false</isdefault>  
</visualization>  
```  
  
 <span data-ttu-id="12151-128">For example, to create a *Sample Visualization* that displays an existing Web resource called *new_TestWebResource*, and the visualization should be attached to the *account* entity, the XML should look like.</span><span class="sxs-lookup"><span data-stu-id="12151-128">For example, to create a *Sample Visualization* that displays an existing Web resource called *new_TestWebResource*, and the visualization should be attached to the *account* entity, the XML should look like.</span></span>  
  
```xml  
<visualization>  
  <name>Sample Visualization</name>  
  <description>Sample Web Resource Visualization.</description>  
  <webresourcename>new_TestWebResource</webresourcename>  
  <primaryentitytypecode>account</primaryentitytypecode>  
  <isdefault>false</isdefault>  
</visualization>  
```  
  
### <a name="see-also"></a><span data-ttu-id="12151-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="12151-129">See also</span></span>  
 <span data-ttu-id="12151-130">[Charts](view-data-with-visualizations-charts.md) </span><span class="sxs-lookup"><span data-stu-id="12151-130">[Charts](view-data-with-visualizations-charts.md) </span></span>  
 <span data-ttu-id="12151-131">[Specifying Chart Data](understand-charts-underlying-data-chart-representation.md) </span><span class="sxs-lookup"><span data-stu-id="12151-131">[Specifying Chart Data](understand-charts-underlying-data-chart-representation.md) </span></span>  
 <span data-ttu-id="12151-132">[Actions on Chart](actions-visualizations-charts.md) </span><span class="sxs-lookup"><span data-stu-id="12151-132">[Actions on Chart](actions-visualizations-charts.md) </span></span>  
 <span data-ttu-id="12151-133">[Sample Charts](sample-charts.md) </span><span class="sxs-lookup"><span data-stu-id="12151-133">[Sample Charts](sample-charts.md) </span></span>  
 <span data-ttu-id="12151-134">[Data Visualization and Analytics](customize-visualizations-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="12151-134">[Data Visualization and Analytics](customize-visualizations-dashboards.md) </span></span>  
 [<span data-ttu-id="12151-135">Sample: Create, Retrieve, Update, and Delete (CRUD) a Chart</span><span class="sxs-lookup"><span data-stu-id="12151-135">Sample: Create, Retrieve, Update, and Delete (CRUD) a Chart</span></span>](sample-create-retrieve-update-delete-chart.md)
