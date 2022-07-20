---
title: "fileUploadSession resource type"
description: "The file upload session containing the session and container details."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industrydata"
doc_type: resourcePageType
---

# fileUploadSession resource type

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The file upload session containing the session and container details.

## Properties

| Property                    | Type           | Description                                         |
| :-------------------------- | :------------- | :-------------------------------------------------- |
| containerExpirationDateTime | DateTimeOffset | Container expiration date time.                     |
| containerId                 | String         | Container id where the files will be uploaded.      |
| sessionExpirationDateTime   | DateTimeOffset | The file upload session expiration date time.       |
| sessionUrl                  | String         | The Azure storage SasUri to upload source files to. |

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.industryData.fileUploadSession"
}
-->

```json
{
  "@odata.type": "#microsoft.graph.industryData.fileUploadSession",
  "containerExpirationDateTime": "String (timestamp)",
  "containerId": "String",
  "sessionExpirationDateTime": "String (timestamp)",
  "sessionUrl": "String"
}
```
