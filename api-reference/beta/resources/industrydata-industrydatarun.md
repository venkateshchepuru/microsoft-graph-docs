---
title: "industryDataRun resource type"
description: "A pipeline run containing data for all subordinate activities."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industrydata"
doc_type: resourcePageType
---

# industryDataRun resource type

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A pipeline run containing data for all subordinate activities.

## Methods

| Method                                                                       | Return type                                                                                                             | Description                                                                                                         |
| :--------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------ |
| [List industryDataRuns](../api/industrydata-industrydatatenant-list-runs.md) | [microsoft.graph.industryData.industryDataRun](../resources/industrydata-industrydatarun.md) collection                 | Get a list of the [industryDataRun](../resources/industrydata-industrydatarun.md) objects and their properties.     |
| [Get industryDataRun](../api/industrydata-industrydatarun-get.md)            | [microsoft.graph.industryData.industryDataRun](../resources/industrydata-industrydatarun.md)                            | Read the properties and relationships of an [industryDataRun](../resources/industrydata-industrydatarun.md) object. |
| [getStatistics](../api/industrydata-industrydatarun-getstatistics.md)        | [microsoft.graph.industryData.industryDataRunStatistics](../resources/industrydata-industrydatarunstatistics.md)        | Calculate statistics for a run or runs.                                                                             |
| [List activities](../api/industrydata-industrydatarun-list-activities.md)    | [microsoft.graph.industryData.industryDataRunActivity](../resources/industrydata-industrydatarunactivity.md) collection | Get the industryDataRunActivity resources from the activities navigation property.                                  |

## Properties

| Property      | Type                                                       | Description                                                                                                                                                |
| :------------ | :--------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- |
| blockingError | [microsoft.graph.publicError](../resources/publicerror.md) | An error object to diagnose critical failures in the run.                                                                                                  |
| displayName   | String                                                     | The name of the run for rendering in a user interface.                                                                                                     |
| endDateTime   | DateTimeOffset                                             | The time the run finished in ISO 8601 format, or null if the run is still in-progress.                                                                     |
| startDateTime | DateTimeOffset                                             | The time the run started in ISO 8601 format.                                                                                                               |
| status        | industryDataRunStatus                                      | Current status of the run.The possible values are: `running`, `failed`, `completed`, `completedWithErrors`, `completedWithWarnings`, `unknownFutureValue`. |

## Relationships

| Relationship | Type                                                                                                                    | Description                                    |
| :----------- | :---------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------- |
| activities   | [microsoft.graph.industryData.industryDataRunActivity](../resources/industrydata-industrydatarunactivity.md) collection | The set of activities executed during the run. |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.industryData.industryDataRun",
  "openType": false
}
-->

```json
{
  "@odata.type": "#microsoft.graph.industryData.industryDataRun",
  "blockingError": {
    "@odata.type": "microsoft.graph.publicError"
  },
  "displayName": "String",
  "endDateTime": "String (timestamp)",
  "startDateTime": "String (timestamp)",
  "status": "String"
}
```
