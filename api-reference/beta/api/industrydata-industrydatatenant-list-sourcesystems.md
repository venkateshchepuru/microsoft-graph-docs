---
title: "List sourceSystemDefinitions"
description: "Get a list of the sourceSystemDefinitions objects and their properties."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industrydata"
doc_type: apiPageType
---

# List sourceSystemDefinition

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [sourceSystemDefinition](../resources/industrydata-sourceSystemDefinition.md) objects and their properties.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | **TODO: Provide applicable permissions.**   |
| Delegated (personal Microsoft account) | **TODO: Provide applicable permissions.**   |
| Application                            | **TODO: Provide applicable permissions.**   |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http
GET /external/industryData/years
```

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [sourceSystemDefinition](../resources/industrydata-sourceSystemDefinition.md) objects in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "list_sourceSystemDefinition"
}
-->

```http
GET https://graph.microsoft.com/beta/external/industryData/sourceSystems
```

### Response

The following is an example of the response

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.industryData.sourceSystemDefinition)"
}
-->

```http
Content-Type: application/json
Content-length: 250

{
  value: [
    {
      "@odata.type": "#microsoft.graph.industryData.sourceSystemDefinition",
      "displayName": "String",
      "userMatchingSettings": [
        {
          "@odata.type": "microsoft.graph.industryData.userMatchingSetting"
        }
      ],
      "vendor": "String"
    }
  ]
}
```
