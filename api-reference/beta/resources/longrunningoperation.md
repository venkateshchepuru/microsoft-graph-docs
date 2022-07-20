---
title: "longRunningOperation resource type"
description: "**TODO: Add Description**"
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industrydata"
doc_type: resourcePageType
---

# longRunningOperation resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**

## Properties

| Property           | Type                       | Description                                                                                                              |
| :----------------- | :------------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| createdDateTime    | DateTimeOffset             | **TODO: Add Description**                                                                                                |
| id                 | String                     | **TODO: Add Description**                                                                                                |
| lastActionDateTime | DateTimeOffset             | **TODO: Add Description**                                                                                                |
| resourceLocation   | String                     | **TODO: Add Description**                                                                                                |
| status             | longRunningOperationStatus | **TODO: Add Description**.The possible values are: `notStarted`, `running`, `succeeded`, `failed`, `unknownFutureValue`. |
| statusDetail       | String                     | **TODO: Add Description**                                                                                                |

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.longRunningOperation",
  "openType": false
}
-->

```json
{
  "@odata.type": "#microsoft.graph.longRunningOperation",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resourceLocation": "String",
  "status": "String",
  "statusDetail": "String"
}
```
