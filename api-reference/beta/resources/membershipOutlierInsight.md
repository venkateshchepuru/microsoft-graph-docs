---
title: "membershipOutlierInsight resource type"
description: "In the Azure AD access reviews, the membershipOutlierInsight resource represents insights provided to reviewers based on whether a user is a peer outlier w.r.t other group members"
author: "shubhamguptacal"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: resourcePageType
---

# membershipOutlierInsight resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[!INCLUDE [accessreviews-disclaimer-v2](../../includes/accessreviews-disclaimer-v2.md)]

Represents an insight provided to reviewers based on whether a user is a peer outlier w.r.t to other group members

Inherits from [governanceInsight](governanceinsight.md).

## Properties
| Property    | Type   | Description |
| :---------------| :---------- | :---------- |
| memberId | String | Indicates the user Id of the member |
| containerId | String | Indicates the id of the container(for ex: group Id) |
| outlierContainerType | outlierContainerType | Indicates the type of container. For ex: group  |
| outlierMemberType | outlierMemberType | Indicates the type of outlier member. For ex: user |

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.membershipOutlierInsight",
  "baseType": "microsoft.graph.governanceInsight"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.membershipOutlierInsight",
  "memberId": "String",
  "containerId": "String",
  "outlierContainerType": "String",
  "outlierMemberType": "String",
}
```

<!--
{
  "type": "#page.annotation",
  "description": "membershipOutlierInsight resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
