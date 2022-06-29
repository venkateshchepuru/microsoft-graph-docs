---
title: "Syntax for using the $filter OData query parameter"
description: "Learn how to use the $filter OData query parameter and its operators against different types of properties in Microsoft Graph."
author: "FaithOmbongi"
ms.localizationpriority: high
ms.custom: graphiamtop20, scenarios:getting-started
---

# Syntax for using the $filter OData query parameter

The following article demonstrates the syntax for using the `$filter` OData query parameter and its associated operators. The examples are provided for guidance only and do not reflect a comprehensive list for the application of `$filter`.

These examples show how to use `$filter` to match against properties that are primitive types, complex types, enumeration types, or a collection of one of these types.

> [!IMPORTANT]
> The examples marked with * are only supported with [advanced query capabilities](/graph/aad-advanced-queries)

## $filter on single primitive types like String, Int, and dates

| Operator (s)           | Syntax                                                              |
| ---------------------- | ------------------------------------------------------------------- |
| `eq`                   | `/users?$filter=userType eq 'Member'`                               |
| `not`                  | `/users?$filter=not userType eq 'Member'`*                          |
| `ne`                   | `/users?$filter=companyName ne null`*                               |
| `startsWith`           | `/users?$filter=startsWith(userPrincipalName, 'admin')`             |
| `endsWith`             | `/users?$count=true&$filter=endsWith(mail,'@outlook.com')`          |
| `contains`             |                                                                     |
| `in`                   | `/users?$filter=userType in ('Guest')`                              |
| `le`                   | `/devices?$filter=registrationDateTime le 2021-01-02T12:00:00Z`     |
| `ge`                   | `/devices?$filter=registrationDateTime ge 2021-01-02T12:00:00Z`     |
| `not` and `endsWith`   | `/users?$filter=NOT endsWith(mail, 'OnMicrosoft.com')&$count=true`* |
| `not` and `startsWith` | `/users?$filter=NOT startsWith(mail, 'A')&$count=true`()            |
| `not` and `eq`         | `/users?$filter=not(companyName eq 'Contoso E.A.')&$count=true`*    |
| `not` and `in`         | `/users?$filter=not (userType in ('Member'))&$count=true`*          |

## $filter on a collection of primitive types

| Operator (s)           | Syntax                                                          |
| ---------------------- | --------------------------------------------------------------- |
| `eq`                   | `/groups?$filter=groupTypes/any(c:c eq 'Unified')`              |
| `not`                  | `/groups?$filter=not groupTypes/any(c:c eq 'Unified')`*         |
| `ne`                   | `/users?$filter=companyName ne null`*                           |
| `startsWith`           | `/users?$filter=businessPhones/any(p:startsWith(p, '44 121'))`* |
| `endsWith`             | `/users?$filter=endsWith(mail,'@outlook.com')`*                 |
| `contains`             |                                                                 |
| `in`                   | otherMails                                                      |
| `le`                   |                                                                 |
| `ge`                   |                                                                 |
| `gt`                   |                                                                 |
| `lt`                   |                                                                 |
| `any` and `eq`         | `/groups?$filter=groupTypes/any(c:c eq 'Unified')`              |
| `not` and `endsWith`   |                                                                 |
| `not` and `startsWith` |                                                                 |
| `not` and `eq`         |                                                                 |
| `not` and `in`         |                                                                 |

>**Note:** Some properties also support filtering on empty collections with the following syntax: `users?$filter=assignedLicenses/$count eq 0`


<!--

## $filter on a collection of GUID types



## $filter GUID types

RULE: GUID values are not enclosed in quotes in $filter queries

1. `eq` operator - /servicePrincipals?$filter=appOwnerOrganizationId eq cab01047-8ad9-4792-8e42-569340767f1b


## $filter Integer types


## $filter Boolean types


## $filter Date types


## $filter DateTimeOffset types

`ge` - users?$filter=employeeHireDate ge 2021-01-02T12:00:00Z
`ge` - groups?$filter=createdOnBehalfOf/deletedDateTime ge 2021-01-02T12:00:00Z



## $filter Complex types

### A single complex type

1. `ge` - /users?$filter=manager/deletedDateTime ge 2021-01-02T12:00:00Z


### A complex type that's a collection of objects

/devices?$filter=alternativeSecurityIds/any(a:a/type ge 12345)

### A complex type that includes a property that's a collection of objects

1. `eq` operator - /users?$filter=authorizationInfo/certificateUserIds/any(x:x eq '9876543210@mil')

2. `startsWith` operator - /users?$filter=authorizationInfo/certificateUserIds/any(x:startswith(x,'987654321'))
1. `endsWith` - /users?$filter=proxyAddresses/any(p:endsWith(p,'OnMicrosoft.com'))$count=true
1. `ge` - /servicePrincipals?$filter=keyCredentials/any(k:k/endDateTime ge 2021-01-02T12:00:00Z)
1. `

## $filter Enumeration types






## Use of and/or operators and ampersand

Single-valued vs collections

? Tooltip. Check if this query requires advanced query capabilities.


## $count of empty collections

$count with `eq` - applications?$filter=federatedIdentityCredentials/$count+eq+0&$count=true

$count with not equals - applications?$filter=federatedIdentityCredentials/$count ne 0
                       - applications?$filter=NOT(federatedIdentityCredentials/$count eq 0)

/applications?$filter=federatedIdentityCredentials/$count+eq+0&$count=true&$filter=startsWith(displayName, 'B')


/users?$filter=proxyAddresses/$count ne 0 and assignedLicenses/$count eq 0&$count=true


Filter with Disjunctive/OR Conjunctive operators

--> 
