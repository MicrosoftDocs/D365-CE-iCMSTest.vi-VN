---
title: Browse the metadata for your organization (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: You can use the Entity Metadata Browser to view entities and their properties in Dynamics 365 for Customer Engagement apps. The Entity Metadata Browser is a managed solution you can download and install on your organization.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 46306470-dca2-4d4e-8a98-d7a6eb47ecfe
author: JimDaly
ms.author: jdaly
manager: amyla
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 40
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9729d8d6eef2eaffbfe0b015086a2d350b71384e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388428"
---
# <a name="browse-the-metadata-for-your-organization"></a>Browse the metadata for your organization

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

You can use the Entity Metadata Browser to view entities and their properties in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps. The Entity Metadata Browser is a managed solution you can download using the links below.


|                                                                                               Phiên bản                                                                                                |                                                                                     Download                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                              [!INCLUDE[pn_crm_9_0_0_online](../includes/pn-crm-9-0-0-online.md)] (v9.0)                                                              | [Microsoft Downloads: MetadataBrowser_3_0_0_5_managed.zip](http://download.microsoft.com/download/8/E/3/8E3279FE-7915-48FE-A68B-ACAFB86DA69C/MetadataBrowser_3_0_0_5_managed.zip) |
| [!INCLUDE[pn_dyn_365](../includes/pn-dyn-365.md)] (v8.2\) [!INCLUDE[pn_crm_8_1_0_online](../includes/pn-crm-8-1-0-online.md)] và [!INCLUDE[pn_crm_8_1_0_op](../includes/pn-crm-8-1-0-op.md)] (v8.1) | [Microsoft Downloads: MetadataBrowser_3_0_0_4_managed.zip](http://download.microsoft.com/download/C/5/D/C5DEA99B-5CD1-40BA-BAB8-15CDC956FDAB/MetadataBrowser_3_0_0_4_managed.zip) |
|                                                                         Dynamics CRM Online 2016 Update and CRM 2016 (v8.0)                                                                          | [Microsoft Downloads: MetadataBrowser_3_0_0_2_managed.zip](http://download.microsoft.com/download/6/D/3/6D341DDC-01B4-44A3-925D-D9188342E3B4/MetadataBrowser_3_0_0_2_managed.zip) |

Sau khi bạn tải xuống giải pháp, bạn phải cài đặt nó. Để biết thêm chi tiết về cách cài đặt một giải pháp được quản lý, hãy xem [Giải pháp nhập, cập nhật và xuất](../customize/import-update-export-solutions.md)  

## <a name="open-as-an-app"></a>Mở dưới dạng một ứng dụng
Phiên bản [!INCLUDE[pn_crm_9_0_0_online](../includes/pn-crm-9-0-0-online.md)] (v9.0) được định cấu hình như một ứng dụng. Sau khi bạn cài đặt giải pháp **Trình duyệt Siêu dữ liệu Thực thể**, xác định vị trí ứng dụng **Công cụ Siêu dữ liệu** và mở nó ra. **Thực thể** là dạng xem mặc định. Từ khu vực điều hướng **Công cụ** bạn có thể chọn **Siêu dữ liệu Thực thể** để kiểm tra các thực thể riêng lẻ.

## <a name="open-from-the-solution-configuration-page"></a>Mở từ trang định cấu hình giải pháp
Đối với các phiên bản trước đó, bạn phải dùng những bước sau, nhưng các bước này không làm việc với phiên bản mới nhất.  

Sau khi bạn cài đặt giải pháp **Trình duyệt Siêu dữ liệu Thực thể**, mở giải pháp được quản lý bằng cách bấm đúp vào hàng trong danh sách giải pháp và xem trang **Cấu hình** để xem thông tin về Trình duyệt Siêu dữ liệu Thực thể và các nút để khởi chạy hai dạng xem khác nhau.
- **Trình duyệt Siêu dữ liệu** tương đương với dạng xem **Thực thể** trong ứng dụng.
- **Trình duyệt Siêu dữ liệu Thực thể** tương đương với dạng xem **Siêu dữ liệu Thực thể** trong ứng dụng.

## <a name="entities-view"></a>Dạng xem Thực thể
Bạn có thể thực hiện các hành động sau:

- **Xem Chi tiết Thực thể**: Chọn một thực thể để xem sử dụng dạng xem **Siêu dữ liệu Thực thể**.
- **Chỉnh sửa Thực thể**: Mở biểu mẫu thực thể được chọn trong tổ chức mặc định, nếu thực thể hỗ trợ.
- **Text Search**: Perform a text search to filter displayed entities using the following entity properties: <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.SchemaName>, <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.LogicalName>, <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.DisplayName>, <xref:Microsoft.Xrm.Sdk.Metadata.EntityMetadata.ObjectTypeCode>, or <xref:Microsoft.Xrm.Sdk.Metadata.MetadataBase.MetadataId>.
- **Lọc Thực thể**: Đặt các tiêu chí đơn giản để xem một tập con của các thực thể. Tất cả các tiêu chí được đánh giá sử dụng lô-gic AND.
- **Lọc Thuộc tính**: Lọc thuộc tính được hiển thị cho bất kỳ thực thể được chọn nào. Có gần 100 thuộc tính trong danh sách. Sử dụng cái này để chọn những cái mà bạn quan tâm.

## <a name="entity-metadata-view"></a>Dạng xem Siêu dữ liệu Thực thể
 Bạn có thể thực hiện các hành động sau cho một thực thể đơn lẻ:

- **Thực thể**: Thay đổi thực thể bạn muốn xem.
- **Thuộc tính**: Xem tất cả thuộc tính cho thực thể và lọc thuộc tính được hiển thị.

    - **Chỉnh sửa Thực thể**: Mở thực biểu mẫu chỉnh sửa thực thể đã chọn trong tổ chức mặc định, nếu thực thể hỗ trợ điều này.
    - **Lọc Thuộc tính**: Lọc thuộc tính được hiển thị cho bất kỳ thực thể được chọn nào. Có gần 100 thuộc tính trong danh sách. Sử dụng cái này để chọn những cái mà bạn quan tâm.

- **Thuộc tính**: Xem các thuộc tính thực thể trong một dạng xem chính/chi tiết. Với dạng xem này bạn có thể:

    - **Chỉnh sửa Thuộc tính**: Mở biểu mẫu thuộc tính đã chọn trong tổ chức mặc định, nếu thuộc tính hỗ trợ điều này.
    - **Text Search**: Perform a text search to filter displayed attributes using the following attribute properties: <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.SchemaName>, <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.LogicalName>, <xref:Microsoft.Xrm.Sdk.Metadata.AttributeMetadata.DisplayName>, or <xref:Microsoft.Xrm.Sdk.Metadata.MetadataBase.MetadataId>.
    - **Lọc Thuộc tính**: Lọc thuộc tính theo bất kỳ giá trị tính chất thuộc tính nào.
    - **Lọc Đặc tính**: Lọc đặc tính được hiển thị cho thuộc tính được chọn.

- **Khoá**: Nếu các khoá thay thế được bật cho một thực thể, bạn có thể kiểm tra cách chúng được định cấu hình.

- **Mối quan hệ**: Xem ba loại mối quan hệ của thực thể: Một đến nhiều, Nhiều đến một và Nhiều đến rất nhiều. Với các dạng xem này bạn có thể:  
    - **Chỉnh sửa Mối quan hệ**: Mở biểu mẫu mối quan hệ được chọn trong tổ chức mặc đinh, nếu mối quan hệ hỗ trợ điều này.  
    - **Tìm kiếm Văn bản**: Thực hiện một tìm kiếm văn bản để lọc các mối quan hệ được hiển thị sử dụng các giá trị liên quan đến loại mối quan hệ.  
    - **Lọc Đặc tính**: Lọc mối quan hệ theo bất kỳ giá trị thuộc tính mối quan hệ nào.

- **Đặc quyền**: Xem đặc quyền của thực thể. Với dạng xem này bạn có thể:  
    - Lọc đặc quyền được hiển thị sử dụng `PrivilegeId`.

> [!NOTE]
> Khi xe, đặc tính chi tiết của thực thể, bạn sẽ nhìn thấy nhiều đặc tính phức tạp có thể mở rộng. Giá trị hữu ích nhất được hiển thị với một liên kết cho phép chuyển đổi sang một dạng xem chi tiết hơn. Dạng xem chi tiết này phản ánh cấu trúc của dữ liệu nếu bạn muốn truy xuất nó theo lập trình. Dạng xem chi tiết cũng cho thấy các dữ liệu có liên quan khác có thể được truy xuất trong cùng một khu vực, ví dụ: nếu có bất kỳ nhãn nào được bản địa hóa hiện diện cho thuộc tính **Tên Hiển thị**.

> [!TIP]
> Để sao chép văn bản từ trang, chỉ cần chọn văn bản và sử dụng phím tắt Ctrl + C hoặc menu lệnh **Sao chép**.

## <a name="community-tools"></a>Các công cụ dành cho cộng đồng

**Metadata Browser** is a tool that XrmToolbox community developed for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps. Please see the [Developer tools](developer-tools.md) topic for community developed tools.

> [!NOTE]
> Các công cụ dành cho cộng đồng không phải là sản phẩm của [!include[pn_microsoft_dynamics](../includes/pn-microsoft-dynamics.md)] và không mở rộng hỗ trợ đối với các công cụ dành cho cộng đồng. If you have questions pertaining to the tool, please contact the publisher. More Information: [XrmToolBox](https://www.xrmtoolbox.com).

### <a name="see-also"></a>Xem thêm

 [Developer Tools for Dynamics 365 for Customer Engagement apps](developer-tools.md)<br />
 [Customize Entity Metadata](customize-entity-metadata.md)<br />
 [Extend the Metadata Model for Dynamics 365 for Customer Engagement apps](org-service/use-organization-service-metadata.md)<br />
 [Create Early Bound Entity Classes with the Code Generation Tool (CrmSvcUtil.exe)](org-service/create-early-bound-entity-classes-code-generation-tool.md)<br />
 [Analyze Plug-in Performance](analyze-plugin-performance.md)<br />
 [Solution Tools for Team Development](solution-tools-team-development.md)<br />
