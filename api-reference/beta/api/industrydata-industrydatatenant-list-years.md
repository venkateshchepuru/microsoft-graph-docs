---
title: "List yearTimePeriodDefinitions"
description: "Get a list of the yearTimePeriodDefinitions objects and their properties."
author: "mlafleur"
ms.localizationpriority: medium
ms.prod: "industrydata"
doc_type: apiPageType
---

# List yearTimePeriodDefinition

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [yearTimePeriodDefinition](../resources/industrydata-yearTimePeriodDefinition.md) objects and their properties.

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

If successful, this method returns a `200 OK` response code and a collection of [yearTimePeriodDefinition](../resources/industrydata-yearTimePeriodDefinition.md) objects in the response body.

## Examples

### Request

The following is an example of a request.

<!-- {
  "blockType": "request",
  "name": "list_yeartimeperioddefinition"
}
-->

```http
GET https://graph.microsoft.com/beta/external/industryData/years
```

### Response

The following is an example of the response

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.industryData.yearTimePeriodDefinition)"
}
-->

```http
HTTP/1.1 201 Created
Content-Type: application/json
{
  "value": [
    {
      "@odata.type": "#microsoft.graph.industryData.yearTimePeriodDefinition",
      "displayName": "String",
      "endDate": "Date",
      "startDate": "Date",
      "year": {
        "@odata.type": "microsoft.graph.industryData.yearReferenceValue"
      }
    }
  ]
}
```
