---
title: Create allowedUser for printerShare
description: Grant the specified user access to submit print jobs to the associated printer share.
author: braedenp-msft
ms.localizationpriority: medium
ms.prod: cloud-printing
doc_type: apiPageType
---

# Create allowedUser for printerShare

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Grant the specified user access to submit print jobs to the associated [printerShare](../resources/printershare.md).

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

To use the Universal Print service, the user or app's tenant must have an active Universal Print subscription, in addition to the permissions listed in the following table. The signed in user must be a [Printer Administrator](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#printer-administrator).

|Permission type | Permissions (from least to most privileged) |
|:---------------|:--------------------------------------------|
|Delegated (work or school account)| PrinterShare.ReadWrite.All |
|Delegated (personal Microsoft account)|Not Supported.|
|Application|Not Supported.|

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /print/shares/{id}/allowedUsers/$ref
```
## Request headers
| Name          | Description   |
|:--------------|:--------------|
| Authorization | Bearer {token}. Required. |
| Content-type  | application/json. Required.|

## Request body
In the request body, supply a reference to a user entity by using the `@odata.id` format, as shown in the following example.

## Response
If successful, this method returns a `204 No Content` response code.

## Example
### Request
The following is an example of the request.


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_alloweduser_from_printers"
}-->
```http
POST https://graph.microsoft.com/beta/print/shares/{id}/allowedUsers/$ref
Content-type: application/json

{
  "@odata.id": "https://graph.microsoft.com/beta/users/{id}"
}
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-alloweduser-from-printers-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/create-alloweduser-from-printers-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-alloweduser-from-printers-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-alloweduser-from-printers-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/create-alloweduser-from-printers-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/create-alloweduser-from-printers-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/create-alloweduser-from-printers-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

In the request body, supply a reference to a user entity by including the user's Microsoft Graph URI in the `@odata.id` field of the JSON body.

### Response
The following is an example of the response. 
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create allowedUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
