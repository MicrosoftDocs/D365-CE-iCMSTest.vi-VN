---
title: 'Understand charts: Underlying data and chart representation (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'Charts display data visually by mapping textual values on two axes: horizontal (x) and vertical (y). In Dynamics 365 for Customer Engagement, the x axis is called the category axis and the y axis is called the series axis.'
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
- charts, understand
ms.assetid: 05ada555-b535-4371-8029-176c454ada26
caps.latest.revision: 41
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7dfbccc28b4457a757c6a1ef5d03131f6e5933f7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386287"
---
# <a name="understand-charts-underlying-data-and-chart-representation"></a><span data-ttu-id="81490-104">Understand charts: Underlying data and chart representation</span><span class="sxs-lookup"><span data-stu-id="81490-104">Understand charts: Underlying data and chart representation</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="81490-105">Charts display data visually by mapping textual values on two axes: horizontal (x) and vertical (y).</span><span class="sxs-lookup"><span data-stu-id="81490-105">Charts display data visually by mapping textual values on two axes: horizontal (x) and vertical (y).</span></span> <span data-ttu-id="81490-106">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, the x axis is called the *category* axis and the y axis is called the *series* axis.</span><span class="sxs-lookup"><span data-stu-id="81490-106">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] Customer Engagement, the x axis is called the *category* axis and the y axis is called the *series* axis.</span></span> <span data-ttu-id="81490-107">The category axis can display numeric as well as non-numeric values whereas the series axis only displays numeric values.</span><span class="sxs-lookup"><span data-stu-id="81490-107">The category axis can display numeric as well as non-numeric values whereas the series axis only displays numeric values.</span></span>  
  
 <span data-ttu-id="81490-108">Charts in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] can be further classified into the following:</span><span class="sxs-lookup"><span data-stu-id="81490-108">Charts in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] can be further classified into the following:</span></span>  
  
- <span data-ttu-id="81490-109">**Single-series charts**: Charts that display data with a series (y) value mapped to a category (x) value.</span><span class="sxs-lookup"><span data-stu-id="81490-109">**Single-series charts**: Charts that display data with a series (y) value mapped to a category (x) value.</span></span>  
  
- <span data-ttu-id="81490-110">**Multi-series charts**:  Charts that display data with multiple series values mapped to a single category value.</span><span class="sxs-lookup"><span data-stu-id="81490-110">**Multi-series charts**:  Charts that display data with multiple series values mapped to a single category value.</span></span> <span data-ttu-id="81490-111">Multi-series charts include stacked column charts, which vertically display the contribution of each series to a total across categories, and 100% stacked column charts, which compare the percentage that each series contributes to a total across categories.</span><span class="sxs-lookup"><span data-stu-id="81490-111">Multi-series charts include stacked column charts, which vertically display the contribution of each series to a total across categories, and 100% stacked column charts, which compare the percentage that each series contributes to a total across categories.</span></span> <span data-ttu-id="81490-112">You can combine different compatible chart types in multi-series charts, for example, column and line, bar and line, and so on.</span><span class="sxs-lookup"><span data-stu-id="81490-112">You can combine different compatible chart types in multi-series charts, for example, column and line, bar and line, and so on.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="81490-113">Multi-category charts can be created through the web application or by modifying the XML strings described here.</span><span class="sxs-lookup"><span data-stu-id="81490-113">Multi-category charts can be created through the web application or by modifying the XML strings described here.</span></span>  
  
 <span data-ttu-id="81490-114">While authoring a chart in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] using the SDK, you need to consider the following two important aspects:</span><span class="sxs-lookup"><span data-stu-id="81490-114">While authoring a chart in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] using the SDK, you need to consider the following two important aspects:</span></span>  
  
- <span data-ttu-id="81490-115">**Underlying data for the chart**: Specified using the *data description* XML string.</span><span class="sxs-lookup"><span data-stu-id="81490-115">**Underlying data for the chart**: Specified using the *data description* XML string.</span></span>  
  
- <span data-ttu-id="81490-116">**Data representation (appearance)**: Specified using the *presentation description* XML string.</span><span class="sxs-lookup"><span data-stu-id="81490-116">**Data representation (appearance)**: Specified using the *presentation description* XML string.</span></span>  
  
> [!NOTE]
> [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)] <span data-ttu-id="81490-117">lets you create various types of charts such as column, bar, area, line, pie, funnel, bubble, and radar.</span><span class="sxs-lookup"><span data-stu-id="81490-117">lets you create various types of charts such as column, bar, area, line, pie, funnel, bubble, and radar.</span></span> <span data-ttu-id="81490-118">The chart designer in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] lets you create only certain types of charts.</span><span class="sxs-lookup"><span data-stu-id="81490-118">The chart designer in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] lets you create only certain types of charts.</span></span> <span data-ttu-id="81490-119">However, using the SDK, you can create most of the chart types that are supported by [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)].</span><span class="sxs-lookup"><span data-stu-id="81490-119">However, using the SDK, you can create most of the chart types that are supported by [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)].</span></span>  
  
## <a name="use-the-data-description-xml-string-to-specify-chart-data"></a><span data-ttu-id="81490-120">Use the data description XML string to specify chart data</span><span class="sxs-lookup"><span data-stu-id="81490-120">Use the data description XML string to specify chart data</span></span>  
 <span data-ttu-id="81490-121">The data description XML string defines the data that will displayed on the chart.</span><span class="sxs-lookup"><span data-stu-id="81490-121">The data description XML string defines the data that will displayed on the chart.</span></span> <span data-ttu-id="81490-122">The contents of the XML string are validated against the visualization data description schema.</span><span class="sxs-lookup"><span data-stu-id="81490-122">The contents of the XML string are validated against the visualization data description schema.</span></span> <span data-ttu-id="81490-123">For more information about the schema, see [Visualization Data Description Schema](visualization-data-description-schema.md).</span><span class="sxs-lookup"><span data-stu-id="81490-123">For more information about the schema, see [Visualization Data Description Schema](visualization-data-description-schema.md).</span></span>  
  
 <span data-ttu-id="81490-124">You can specify the data description XML string while you are creating a chart using the `SavedQueryVisualization.DataDescription` or the `UserQueryVisualization.DataDescription` attribute for the organization-owned or user-owned chart respectively.</span><span class="sxs-lookup"><span data-stu-id="81490-124">You can specify the data description XML string while you are creating a chart using the `SavedQueryVisualization.DataDescription` or the `UserQueryVisualization.DataDescription` attribute for the organization-owned or user-owned chart respectively.</span></span>  
  
 <span data-ttu-id="81490-125">The data description XML string contains the following two elements: `<FetchCollection>` and `<CategoryCollection>`.</span><span class="sxs-lookup"><span data-stu-id="81490-125">The data description XML string contains the following two elements: `<FetchCollection>` and `<CategoryCollection>`.</span></span>  
  
### <a name="the-fetchcollection-element"></a><span data-ttu-id="81490-126">The \<FetchCollection> element</span><span class="sxs-lookup"><span data-stu-id="81490-126">The \<FetchCollection> element</span></span>  
 <span data-ttu-id="81490-127">The `<FetchCollection>` element uses FetchXML to retrieve data for the chart.</span><span class="sxs-lookup"><span data-stu-id="81490-127">The `<FetchCollection>` element uses FetchXML to retrieve data for the chart.</span></span> <span data-ttu-id="81490-128">The FetchXML query specifies information about the entity attributes, aggregate functions, and the group by clauses for the data to be displayed in a chart.</span><span class="sxs-lookup"><span data-stu-id="81490-128">The FetchXML query specifies information about the entity attributes, aggregate functions, and the group by clauses for the data to be displayed in a chart.</span></span> <span data-ttu-id="81490-129">All the FetchXML aggregate functions are supported for charts.</span><span class="sxs-lookup"><span data-stu-id="81490-129">All the FetchXML aggregate functions are supported for charts.</span></span> <span data-ttu-id="81490-130">For more information about the FetchXML aggregate functions, see [Using FetchXML Aggregration](../org-service/use-fetchxml-aggregation.md).</span><span class="sxs-lookup"><span data-stu-id="81490-130">For more information about the FetchXML aggregate functions, see [Using FetchXML Aggregration](../org-service/use-fetchxml-aggregation.md).</span></span>  
  
 <span data-ttu-id="81490-131">The FetchXML query enables you to filter your data.</span><span class="sxs-lookup"><span data-stu-id="81490-131">The FetchXML query enables you to filter your data.</span></span> <span data-ttu-id="81490-132">Also, filters are applied on charts through views.</span><span class="sxs-lookup"><span data-stu-id="81490-132">Also, filters are applied on charts through views.</span></span> <span data-ttu-id="81490-133">Therefore, if a filter condition is already specified in the FetchXML query in the `<FetchCollection>` element, and additionally a filter is applied through a view, the chart will display data that is returned after it applies all the filters.</span><span class="sxs-lookup"><span data-stu-id="81490-133">Therefore, if a filter condition is already specified in the FetchXML query in the `<FetchCollection>` element, and additionally a filter is applied through a view, the chart will display data that is returned after it applies all the filters.</span></span> <span data-ttu-id="81490-134">For more information about how to use the FetchXML query to filter data, see [Building Queries with FetchXML](../org-service/build-queries-fetchxml.md).</span><span class="sxs-lookup"><span data-stu-id="81490-134">For more information about how to use the FetchXML query to filter data, see [Building Queries with FetchXML](../org-service/build-queries-fetchxml.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="81490-135">Although the data description XML string is validated again the visualization data description schema, the FetchXML query inside the `<FetchCollection>` element is not.</span><span class="sxs-lookup"><span data-stu-id="81490-135">Although the data description XML string is validated again the visualization data description schema, the FetchXML query inside the `<FetchCollection>` element is not.</span></span> <span data-ttu-id="81490-136">The FetchXML query is validated against the FetchXML schema.</span><span class="sxs-lookup"><span data-stu-id="81490-136">The FetchXML query is validated against the FetchXML schema.</span></span> <span data-ttu-id="81490-137">For more information, see [Fetch XML Schema](../org-service/fetchxml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="81490-137">For more information, see [Fetch XML Schema](../org-service/fetchxml-schema.md).</span></span>  
  
 <span data-ttu-id="81490-138">If the chart is a comparison chart, the `<FetchCollection>` element will contain two *group by* clauses.</span><span class="sxs-lookup"><span data-stu-id="81490-138">If the chart is a comparison chart, the `<FetchCollection>` element will contain two *group by* clauses.</span></span>  
  
### <a name="the-categorycollection-element"></a><span data-ttu-id="81490-139">The \<CategoryCollection> element</span><span class="sxs-lookup"><span data-stu-id="81490-139">The \<CategoryCollection> element</span></span>  
 <span data-ttu-id="81490-140">The `<CategoryCollection>` element contains information about the category (horizontal) and the series (vertical) axes in a chart.</span><span class="sxs-lookup"><span data-stu-id="81490-140">The `<CategoryCollection>` element contains information about the category (horizontal) and the series (vertical) axes in a chart.</span></span>  
  
-   <span data-ttu-id="81490-141">Each `<Category>` sub-element has a child element called `<MeasureCollection>` that maps to the `<Series>` element in the presentation description XML.</span><span class="sxs-lookup"><span data-stu-id="81490-141">Each `<Category>` sub-element has a child element called `<MeasureCollection>` that maps to the `<Series>` element in the presentation description XML.</span></span> <span data-ttu-id="81490-142">A single series chart has a single `<MeasureCollection>` child element whereas a multi-series chart will have multiple `<MeasureCollection>` child elements, each mapped to the respective `<Series>` element in the presentation description XML.</span><span class="sxs-lookup"><span data-stu-id="81490-142">A single series chart has a single `<MeasureCollection>` child element whereas a multi-series chart will have multiple `<MeasureCollection>` child elements, each mapped to the respective `<Series>` element in the presentation description XML.</span></span>  
  
-   <span data-ttu-id="81490-143">Each `<MeasureCollection>` child element has an element called `<Measure>` that corresponds to the series (vertical) axis value, corresponding to each value on the category (horizontal) axis.</span><span class="sxs-lookup"><span data-stu-id="81490-143">Each `<MeasureCollection>` child element has an element called `<Measure>` that corresponds to the series (vertical) axis value, corresponding to each value on the category (horizontal) axis.</span></span>  
  
### <a name="example"></a><span data-ttu-id="81490-144">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="81490-144">Example</span></span>  
 <span data-ttu-id="81490-145">The following is a sample data description XML string:</span><span class="sxs-lookup"><span data-stu-id="81490-145">The following is a sample data description XML string:</span></span>  
  
```xml  
<datadefinition>  
  <fetchcollection>  
    <fetch mapping="logical" count="10">  
      <entity name="opportunity">  
        <attribute name="estimatedvalue" />  
        <order attribute="estimatedvalue" descending="true" />  
      </entity>  
    </fetch>  
  </fetchcollection>  
  <categorycollection>  
    <category>  
      <measurecollection>  
        <measure alias="estimatedvalue" />  
      </measurecollection>  
    </category>  
  </categorycollection></datadefinition>  
```  
  
 <span data-ttu-id="81490-146">For more sample data description XML strings, see [Sample Charts](sample-charts.md).</span><span class="sxs-lookup"><span data-stu-id="81490-146">For more sample data description XML strings, see [Sample Charts](sample-charts.md).</span></span>  
  
## <a name="use-the-presentation-description-xml-string-to-specify-data-representation"></a><span data-ttu-id="81490-147">Use the presentation description XML string to specify data representation</span><span class="sxs-lookup"><span data-stu-id="81490-147">Use the presentation description XML string to specify data representation</span></span>  
 <span data-ttu-id="81490-148">The presentation description XML string contains information about the appearance of the chart such as chart title, chart color, and chart type (bar, column, line, and so on).</span><span class="sxs-lookup"><span data-stu-id="81490-148">The presentation description XML string contains information about the appearance of the chart such as chart title, chart color, and chart type (bar, column, line, and so on).</span></span> <span data-ttu-id="81490-149">There is no schema definition for this XML string.</span><span class="sxs-lookup"><span data-stu-id="81490-149">There is no schema definition for this XML string.</span></span> <span data-ttu-id="81490-150">However, the XML is a serialization of the [Chart](https://msdn.microsoft.com/library/system.web.ui.datavisualization.charting.chart.aspx) class in [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)].</span><span class="sxs-lookup"><span data-stu-id="81490-150">However, the XML is a serialization of the [Chart](https://msdn.microsoft.com/library/system.web.ui.datavisualization.charting.chart.aspx) class in [!INCLUDE[pn_ms_chart_controls_short](../../includes/pn-ms-chart-controls-short.md)].</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="81490-151">[Chart Controls](http://go.microsoft.com/fwlink/p/?LinkId=128301)</span><span class="sxs-lookup"><span data-stu-id="81490-151">[Chart Controls](http://go.microsoft.com/fwlink/p/?LinkId=128301)</span></span>  
  
 <span data-ttu-id="81490-152">You can specify the presentation description XML string while you are creating a chart using the `SavedQueryVisualization.PresentationDescription` or `UserQueryVisualization.PresentationDescription` attribute for the organization-owned or user-owned chart, respectively.</span><span class="sxs-lookup"><span data-stu-id="81490-152">You can specify the presentation description XML string while you are creating a chart using the `SavedQueryVisualization.PresentationDescription` or `UserQueryVisualization.PresentationDescription` attribute for the organization-owned or user-owned chart, respectively.</span></span>  
  
### <a name="example"></a><span data-ttu-id="81490-153">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="81490-153">Example</span></span>  
 <span data-ttu-id="81490-154">The following is a sample presentation description XML string:</span><span class="sxs-lookup"><span data-stu-id="81490-154">The following is a sample presentation description XML string:</span></span>  
  
```xml  
<Chart Palette="BrightPastel">  
  <Series>  
    <Series _Template_="All" Color="153, 204, 255" BorderColor="164, 164, 164" BorderDashStyle="Solid" BorderWidth="1" ShadowColor="128, 128, 128, 128" ShadowOffset="1" IsValueShownAsLabel="true" Font="{0}, 6.75pt" BackGradientStyle="TopBottom" BackSecondaryColor="0, 102, 153" LabelForeColor="100, 100, 100" ChartType="Column">  
      <SmartLabelStyle Enabled="True" />  
      <Points />  
    </Series>  
  </Series>  
  <ChartAreas>  
    <ChartArea _Template_="All" BackColor="White" BorderColor="26, 59, 105" BorderWidth="0" BorderDashStyle="Solid">      <AxisY LineColor="204, 204, 204" TitleFont="{0}, 8pt, GdiCharSet=0" TitleForeColor="100, 100, 100" LabelAutoFitMaxFontSize="7" LabelAutoFitMinFontSize="7">  
        <MajorTickMark LineColor="Gray" />  
        <MajorGrid Enabled="false" />  
        <LabelStyle Font="{0}, 6.75pt, GdiCharSet=0" ForeColor="100, 100, 100" />  
      </AxisY>  
      <AxisX LineColor="204, 204, 204" TitleFont="{0}, 8pt, GdiCharSet=0" TitleForeColor="100, 100, 100" LabelAutoFitMaxFontSize="7" LabelAutoFitMinFontSize="7">        <MajorTickMark LineColor="Gray" />        <MajorGrid Enabled="false" />  
        <LabelStyle Font="{0}, 6.75pt, GdiCharSet=0" ForeColor="100, 100, 100" />  
      </AxisX>  
    </ChartArea>  
  </ChartAreas>  
  <Titles>  
    <Title _Template_="All" Font="{0}, 9pt, style=Bold, GdiCharSet=0" ForeColor="100, 100, 100"></Title>  
  </Titles>  
  <BorderSkin PageColor="Control" BackColor="CornflowerBlue" BackSecondaryColor="CornflowerBlue" />  
</Chart>  
```  
  
 <span data-ttu-id="81490-155">For more sample presentation description XML strings, see [Sample Charts](sample-charts.md).</span><span class="sxs-lookup"><span data-stu-id="81490-155">For more sample presentation description XML strings, see [Sample Charts](sample-charts.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="81490-156">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="81490-156">See also</span></span>  
 <span data-ttu-id="81490-157">[Visualizations (Charts)](view-data-with-visualizations-charts.md) </span><span class="sxs-lookup"><span data-stu-id="81490-157">[Visualizations (Charts)](view-data-with-visualizations-charts.md) </span></span>  
 <span data-ttu-id="81490-158">[Actions on Visualizations (Charts)](actions-visualizations-charts.md) </span><span class="sxs-lookup"><span data-stu-id="81490-158">[Actions on Visualizations (Charts)](actions-visualizations-charts.md) </span></span>  
 <span data-ttu-id="81490-159">[Create a Chart](create-visualization-chart.md) </span><span class="sxs-lookup"><span data-stu-id="81490-159">[Create a Chart](create-visualization-chart.md) </span></span>  
 <span data-ttu-id="81490-160">[Building Queries with FetchXML](../org-service/build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="81490-160">[Building Queries with FetchXML](../org-service/build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="81490-161">[Fetch XML Schema](../org-service/fetchxml-schema.md) </span><span class="sxs-lookup"><span data-stu-id="81490-161">[Fetch XML Schema](../org-service/fetchxml-schema.md) </span></span>  
 <span data-ttu-id="81490-162">[Visualization Data Description Schema](visualization-data-description-schema.md) </span><span class="sxs-lookup"><span data-stu-id="81490-162">[Visualization Data Description Schema](visualization-data-description-schema.md) </span></span>  
 <span data-ttu-id="81490-163">[Sample Charts](sample-charts.md) </span><span class="sxs-lookup"><span data-stu-id="81490-163">[Sample Charts](sample-charts.md) </span></span>  
 [<span data-ttu-id="81490-164">Chart Class (Microsoft Chart Controls)</span><span class="sxs-lookup"><span data-stu-id="81490-164">Chart Class (Microsoft Chart Controls)</span></span>](https://msdn.microsoft.com/library/system.web.ui.datavisualization.charting.chart.aspx)
