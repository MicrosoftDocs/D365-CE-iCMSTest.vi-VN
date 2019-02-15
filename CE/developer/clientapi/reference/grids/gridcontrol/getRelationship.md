---
title: getRelationship (Client API reference) in Dynamics 365 for Customer Engagement| MicrosoftDocs
ms.date: 11/10/2017
ms.service: crm-online
ms.topic: reference
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: 4d025f92-db16-440c-9f82-e40d71e09862
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: be233583a9e932b37e1dd769895093ecf928b8e4
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388136"
---
# <a name="getrelationship-client-api-reference"></a>getRelationship (Client API reference)

[!INCLUDE[](../../../../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[./includes/getRelationship-description.md](./includes/getRelationship-description.md)]

## <a name="grid-types-supported"></a>Grid types supported

Read-only and editable grids

## <a name="syntax"></a>Cú pháp

`gridContext.getRelationship();`

## <a name="return-value"></a>Giá trị trả lại

**Type**: Object.

**Description**: A relationship object with the following attributes:
- **attributeName**: String. Name of the attribute.
- **name**: String. Name of the relationship. 
- **navigationPropertyName**: String. Name of the navigation property for this relationship.
- **relationshipType**: Number. Returns one of the following values to indicate the relationship type:
    - 0: OneToMany
    - 1: ManyToMany
- **roleType**: Number. Returns one of the following values to indicate the role type of relationship:
    - 1: Referencing
    - 2: AssociationEntity

## <a name="remarks"></a>Chú thích

To get the `gridContext`, see [Getting the grid context](../../grids.md#bkmk_gridcontext).

### <a name="related-topics"></a>Chủ đề liên quan

[openRelatedGrid](openRelatedGrid.md)

[Customize entity relationship metadata](../../../../customize-entity-relationship-metadata.md)


