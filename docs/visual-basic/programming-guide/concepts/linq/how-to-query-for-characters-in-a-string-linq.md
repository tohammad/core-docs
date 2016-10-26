---
title: "How to: Query for Characters in a String (LINQ) (Visual Basic)"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
ms.assetid: 499ebbe0-746c-4235-9dba-ce722c12b50e
caps.latest.revision: 4
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# How to: Query for Characters in a String (LINQ) (Visual Basic)
Because the <xref:System.String> class implements the generic <xref:System.Collections.Generic.IEnumerable`1> interface, any string can be queried as a sequence of characters. However, this is not a common use of LINQ. For complex pattern matching operations, use the <xref:System.Text.RegularExpressions.Regex> class.  
  
## Example  
 The following example queries a string to determine the number of numeric digits it contains. Note that the query is "reused" after it is executed the first time. This is possible because the query itself does not store any actual results.  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
## Compiling the Code  
 Create a project that targets the .NET Framework version 3.5 or higher with a reference to System.Core.dll and a `Imports` statement for the System.Linq namespace.  
  
## See Also  
 [LINQ and Strings (Visual Basic)](../../../../visual-basic\programming-guide\concepts\linq/linq-and-strings.md)   
 [How to: Combine LINQ Queries with Regular Expressions (Visual Basic)](../../../../visual-basic\programming-guide\concepts\linq/how-to-combine-linq-queries-with-regular-expressions.md)