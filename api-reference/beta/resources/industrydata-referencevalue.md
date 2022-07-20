---
title: "referenceValue resource type"
description: "Represents a pointer to an entry in the referenceDefinitions collection."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industrydata"
doc_type: resourcePageType
---

# referenceValue resource type

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a pointer to a [referenceDefinition](../resources/industrydata-referencedefinition.md) with a specific `referenceType`.

This is an abstract type.

| Type                                                                                        | ReferenceType        |
| ------------------------------------------------------------------------------------------- | -------------------- |
| [identifierTypeReferenceValue](../resources/industrydata-identifiertypereferencevalue.md) ] | `RefIdentifierType`  |
| [roleReferenceValue](../resources/industrydata-rolereferencevalue.md)                       | `RefRole`            |
| [userMatchTargetReferenceValue](../resources/industrydata-usermatchtargetreferencevalue.md) | `RefUserMatchTarget` |
| [yearReferenceValue](../resources/industrydata-yearreferencevalue.md)                       | `RefAcademicYear`    |

## Properties

| Property | Type   | Description                                                                                            |
| :------- | :----- | :----------------------------------------------------------------------------------------------------- |
| code     | String | The code of the desired [referenceDefinition](../resources/industrydata-referencedefinition.md) entry. |

## Relationships

| Relationship | Type                                                                    | Description                                        |
| :----------- | :---------------------------------------------------------------------- | :------------------------------------------------- |
| value        | [referenceDefinition](../resources/industrydata-referencedefinition.md) | Reference to the bound referenceDefinition entity. |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.industryData.referenceValue"
}
-->

```json
{
  "@odata.type": "#microsoft.graph.industryData.referenceValue",
  "code": "String"
}
```
