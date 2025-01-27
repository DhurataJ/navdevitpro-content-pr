---
title: "GETRANGEMIN Function (Record)"
description: GETRANGEMIN Function (Record)
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 1966769f-3491-49ba-bfa0-6569883120cc
caps.latest.revision: 12
manager: edupont
---
# GETRANGEMIN Function (Record)
Gets the minimum value in a range for a field.  
  
## Syntax  
  
```  
  
Value := Record.GETRANGEMIN(Field)  
```  
  
#### Parameters  
 *Record*  
 Type: Record  
  
 The record that contains the field.  
  
 *Field*  
 Type: Field  
  
 The field for which you want to find the minimum value.  
  
## Property Value/Return Value  
 Type: Depends on *Field*  
  
 Contains the minimum value of the range set for *Field*. The type of the return value must match the type of *Field*.  
  
## Remarks  
 The current filter on *Field* must be a single range filter; otherwise, a run-time error occurs. This means that field cannot be included in two different FILTERGROUPs, as shown in the following code example:  
  
```  
WITH GLAcc DO BEGIN  
  FILTERGROUP(2);  
    SETRANGE("Date Filter",010415D,300415D);  
  FILTERGROUP(0);  
    SETRANGE("Date Filter",TODAY,CLOSINGDATE(CALCDATE('<CM>',TODAY)));  
  
  MESSAGE('%1',GETRANGEMIN("Date Filter"));  
END;  
```  
  
## Example 1  
 In this example, you have a filter that defines a single range.  
  
 This example requires that you create the following variables and text constant in the **C/AL Globals** window.  
  
|Variable name|DataType|Subtype|Length|  
|-------------------|--------------|-------------|------------|  
|CustomerRec|Record|Customer|Not applicable|  
|Val|Code|Not applicable|10|  
  
|Text constant|ENU value|  
|-------------------|---------------|  
|Text000|The minimum value is: %1.|  
  
```  
CustomerRec.SETFILTER("No.",'100..200');  
Val := CustomerRec.GETRANGEMIN("No.");  
MESSAGE(Text000, Val);  
```  
  
 The following message is displayed:  
  
 **The minimum value is: 100.**  
  
## Example 2 
 In this example, you have a filter that is a single value.  
  
 This example requires that you create the following variables and text constant in the **C/AL Globals** window.  
  
|Variable name|DataType|Subtype|Length|  
|-------------------|--------------|-------------|------------|  
|CustomerRec|Record|Customer|Not applicable|  
|Val|Code|Not applicable|10|  
  
|Text constant|ENU value|  
|-------------------|---------------|  
|Text000|The minimum value is: %1.|  
  
```  
CustomerRec.SETFILTER("No.",'100');  
Val := CustomerRec.GETRANGEMIN("No.");  
MESSAGE(Text000, Val);  
```  
  
 The following message is displayed:  
  
 **The minimum value is: 100.**  
  
## Example 3  
 In this example, you have a filter which is not a single range.  
  
 This example requires that you create the following variables and text constant in the **C/AL Globals** window.  
  
|Variable name|DataType|Subtype|Length|  
|-------------------|--------------|-------------|------------|  
|CustomerRec|Record|Customer|Not applicable|  
|Val|Code|Not applicable|10|  
  
|Text constant|ENU value|  
|-------------------|---------------|  
|Text000|The minimum value is: %1.|  
  
```  
CustomerRec.SETFILTER("No.",'200|300');  
Val := CustomerRec.GETRANGEMIN("No.");  
MESSAGE(Text000, Val);  
```  
  
 This example causes a run-time error to occur.  
  
## See Also  
 [GETRANGEMAX Function \(Record\)](GETRANGEMAX-Function--Record-.md)   
 [Record Data Type](Record-Data-Type.md)