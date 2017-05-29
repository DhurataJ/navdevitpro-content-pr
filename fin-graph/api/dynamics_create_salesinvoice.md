---
title: CREATE Sales Invoice method | Microsoft Docs
description: Creates a sales invoice.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/13/2017
ms.author: solsen
---

# Create sales invoice
Create a salesInvoice in Dynamics 365 for Financials.

## HTTP request

```
POST /financials/companies/{id}/salesInvoices
```

## Request headers

|Header|Value|
|------|-----|
|Authorization  |Bearer. Required.    |
|Content-Type  |application/json    |

## Request body
In the request body, supply a JSON representation of a salesInvoice object.

## Response
If successful, this method returns ```201 Created``` response code and a salesInvoice object in the response body.

## Example

**Request**

Here is an example of a request.

```json
POST https://graph.microsoft.com/beta/financials/companies/{id}/salesInvoices
Content-type: application/json

{
  "id": "id-value",
  "number": "1009",
  "invoiceDate": "2015-12-31",
  "customerNumber": "GL00000008",
  "currencyCode": "GBP",
  "paymentTerms": "COD"
}

## See also
[Working with Dynamics 365 for Financials in Microsoft Graph](../resources/dynamics_overview.md) 