---
title: setProgress (Client API reference) in Dynamics 365 for Customer Engagement apps| MicrosoftDocs
ms.date: 11/20/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 649fe7b0-016d-409f-ba3c-b14e0f1953e0
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ac2881feaf964219e17243887c3dea9520898caa
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387541"
---
# <a name="setprogress-client-api-reference"></a>setProgress (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/setProgress-description.md](./includes/setProgress-description.md)]

## <a name="syntax"></a>Cú pháp

`stepObj.setProgress(stepProgress,message);`

## <a name="parameters"></a>Tham số

<table style="width:100%">
<tr>
<th>Tên</th>
<th>Loại</th>
<th>Bắt buộc</th>
<th>Mô tả</th>
</tr>
<tr>
<td>stepProgress</td>
<td>Số</td>
<td>Có</td>
<td>Specify one of the following values to specify the step progress:
<ul>
<li>0: None</li>
<li>1: Processing</li>
<li>2: Đã hoàn thành</li>
<li>3: Failure</li>
<li>4: Invalid</li>
</ul>
</td>
</tr>
<tr>
<td>message</td>
<td>Chuỗi</td>
<td>Không</td>
<td><p>An optional message that is set as the Alt text on the icon for the step.</td>
</tr>
</table>


## <a name="return-value"></a>Giá trị trả lại

**Type**: String. 

**Description**: Returns "invalid" or "success" depending on whether the step progress was updated.

## <a name="remarks"></a>Chú thích

This method is supported only for the action steps. Action steps are buttons on the business process stages that users can click to trigger an on-demand workflow or action. Action step is a preview feature introduced in the [!INCLUDE[pn_crm_9_0_0_online](../../../../../includes/pn-crm-9-0-0-online.md)] release. Thông tin khác: Xem phần **Tự động hóa Dòng quy trình Công việc qua Các bước Hành động** trong [Blog: Các tính năng trực quan hóa và tự động hóa dành cho Dòng Quy trình Công việc (bản xem trước công khai)](https://blogs.msdn.microsoft.com/crm/2017/10/25/new-automation-and-visualization-features-for-business-process-flows-public-preview/).

### <a name="related-topics"></a>Chủ đề liên quan

[getProgress](getprogress.md)
 
[formContext.data.process](../../formContext-data-process.md)

