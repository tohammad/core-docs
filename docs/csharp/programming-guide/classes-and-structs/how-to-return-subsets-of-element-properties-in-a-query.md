---
title: "How to: Return Subsets of Element Properties in a Query (C# Programming Guide)"
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
  - "anonymous types [C#], for subsets of element properties"
ms.assetid: fabdf349-f443-4e3f-8368-6c471be1dd7b
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
# How to: Return Subsets of Element Properties in a Query (C# Programming Guide)
Use an anonymous type in a query expression when both of these conditions apply:  
  
-   You want to return only some of the properties of each source element.  
  
-   You do not have to store the query results outside the scope of the method in which the query is executed.  
  
 If you only want to return one property or field from each source element, then you can just use the dot operator in the `select` clause. For example, to return only the `ID` of each `student`, write the `select` clause as follows:  
  
```  
select student.ID;  
```  
  
## Example  
 The following example shows how to use an anonymous type to return only a subset of the properties of each source element that matches the specified condition.  
  
 [!code-cs[csProgGuideLINQ#31](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-return-subsets-of-element-properties-in-a-query_1.cs)]  
  
 Note that the anonymous type uses the source element's names for its properties if no names are specified. To give new names to the properties in the anonymous type, write the `select` statement as follows:  
  
```  
select new { First = student.FirstName, Last = student.LastName };  
```  
  
 If you try this in the previous example, then the `Console.WriteLine` statement must also change:  
  
```  
Console.WriteLine(student.First + " " + student.Last);  
```  
  
## Compiling the Code  
  
-   To run this code, copy and paste the class into a Visual C# console application project that has been created in [!INCLUDE[vs_current_short](../../../csharp\programming-guide\classes-and-structs/includes/vs_current_short_md.md)]. By default, this project targets version 3.5 of the [!INCLUDE[dnprdnshort](../../../csharp\getting-started/includes/dnprdnshort_md.md)], and it will have a reference to System.Core.dll and a `using` directive for System.Linq. If one or more of these requirements are missing from the project, you can add them manually. For more information, see [How to: Create a LINQ Project](../Topic/How%20to:%20Create%20a%20LINQ%20Project.md).  
  
## See Also  
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [Anonymous Types](../../../csharp\programming-guide\classes-and-structs/anonymous-types.md)   
 [LINQ Query Expressions](../../../csharp\programming-guide\linq-query-expressions/index.md)