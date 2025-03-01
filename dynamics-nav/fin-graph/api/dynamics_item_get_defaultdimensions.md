---
title: Get item defaultDimensions | Microsoft Docs
description: Gets an item default dimensions in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen

ms.service: dynamics365-financials
ms.topic: reference
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/20/2018
ms.author: solsen
ROBOTS: NOINDEX
---

# Get item defaultDimensions
Gets the default dimensions of the item in [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)] depending on environment following the [guideline](../../endpoints-apis-for-dynamics.md). 
The following example gets the default dimensions of the item entity in the response body.

```
GET businesscentralPrefix/companies({companyId})/items({itemId})/defaultDimensions
```
## Request header

|Header|Value|
|------|-----|
|Authorization| Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response 

If successful, this method returns a `200 OK` response code and the **default dimensions** in the response body.

## Example 
**Request**

```json
GET https://{businesscentralPrefix}/api/beta/companies({companyId})/items({itemId})/defaultDimensions
```

**Response**  
Here is an example of the response.

> [!NOTE]  
> The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.

```json
{
    "@odata.context":"https://api.businesscentral.dynamics.com/v1.0/api/beta/$metadata#companies(5106c77d-af37-4e2d-bb88-45d87aba1033)/items(b3fbe87a-61b8-4a6c-85de-0555f1627a67)/defaultDimensions",
    "value":
    [
        {
            "@odata.etag":"W/\"JzQ0OzNPaHFuS0ZQdk5oc3ZkSW9KdzVkdXk2LytjcmNqeHJJOU05SjZ1aFBYVjQ9MTswMDsn\"",
            "parentId":"b3fbe87a-61b8-4a6c-85de-0555f1627a67","dimensionId":"d5fc81ea-8687-4e9d-9c49-7fde28ccdb1a",
            "dimensionCode":"DEPARTMENT",
            "dimensionValueId":"1045a902-070a-4d31-b2b1-b9431e9e5b26",
            "dimensionValueCode":"PROD",
            "postingValidation":"Same Code"
        }
    ]
} 
```

## See also
[Tips for working with the APIs](/dynamics365/business-central/dev-itpro/developer/devenv-connect-apps-tips)  
[Graph Reference](../api/dynamics_graph_reference.md)  
[Working with [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)] in Microsoft Graph](../resources/dynamics_overview.md)  
[Enabling the APIs for Dynamics 365 Business Central](../../enabling-apis-for-dynamics-nav.md)  
[Endpoints for the APIs](../../endpoints-apis-for-dynamics.md)  
[Error Codes](../dynamics_error_codes.md)  
[Items](../resources/dynamics_item.md)  
[Create item defaultDimensions](dynamics_item_create_defaultdimensions.md)  
[Update item defaultDimensions](dynamics_item_update_defaultdimensions.md)  
[Delete item defaultDimensions](dynamics_item_delete_defaultdimensions.md)  

