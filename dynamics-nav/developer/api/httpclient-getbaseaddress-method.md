---
title: "GetBaseAddress Method"
ms.author: solsen
ms.custom: na
ms.date: 06/29/2017
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2017"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 9
manager: edupont
author: SusanneWindfeldPedersen
---

[!INCLUDE[newdev_dev_preview](../includes/newdev_dev_preview.md)]

# GetBaseAddress Method
Gets the base address of Uniform Resource Identifier (URI) of the Internet resource used when sending requests.

```
[Ok := ] HttpClient.GetBaseAddress
```
## Parameters
*HttpClient*  
&emsp;Type: HttpClient  
&emsp;The HttpClient whose BaseAddress we are trying to get.

## Return value
*Address*  
&emsp;Type: Boolean

The base address of URI of the Internet resource used when sending requests.

## See Also
[Getting Started](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)