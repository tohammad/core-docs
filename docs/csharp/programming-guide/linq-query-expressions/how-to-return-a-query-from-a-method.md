---
title: "How to: Return a Query from a Method (C# Programming Guide)"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "queries [LINQ in C#], method returns query"
  - "query expressions [LINQ in C#], method returns query"
  - "method returns query [C#]"
ms.assetid: 9d6f20a7-f085-44cf-9df3-71948255ec68
caps.latest.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# How to: Return a Query from a Method (C# Programming Guide)
This example shows how to return a query from a method as the return value and as an `out` parameter.  
  
 Any query must have a type of <xref:System.Collections.IEnumerable> or <xref:System.Collections.Generic.IEnumerable`1>, or a derived type such as <xref:System.Linq.IQueryable`1>. Therefore any return value or `out` parameter of a method that returns a query must also have that type. If a method materializes a query into a concrete <xref:System.Collections.Generic.List`1> or <xref:System.Array> type, it is considered to be returning the query results instead of the query itself. A query variable that is returned from a method can still be composed or modified.  
  
## Example  
 In the following example, the first method returns a query as a return value, and the second method returns a query as an `out` parameter. Note that in both cases it is a query that is  returned, not query results.  
  
 [!code-cs[csProgGuideLINQ#80](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-return-a-query-from-a-method_1.cs)]  
  
## Compiling the Code  
  
-   Create a [!INCLUDE[vs_current_short](../../../csharp\programming-guide\classes-and-structs/includes/vs_current_short_md.md)] project that targets the .NET Framework version 3.5 or a later version. By default, the project has a reference to System.Core.dll and a `using` directive for the System.Linq namespace.  
  
-   Replace the class with the code in the example.  
  
-   Press F5 to compile and run the program.  
  
-   Press any key to exit the console window.  
  
## See Also  
 [LINQ Query Expressions](../../../csharp\programming-guide\linq-query-expressions/index.md)