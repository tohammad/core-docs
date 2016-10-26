---
title: "How to: Dynamically Specify Predicate Filters at Runtime (C# Programming Guide)"
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
  - "queries [LINQ in C#], predicate filters"
  - "dynamic queries [LINQ in C#]"
  - "predicate filters [C#]"
  - "predicates [C#]"
  - "query expressions [LINQ in C#], predicate filters"
ms.assetid: 52f2dc7a-8353-4c6e-98d3-eec99a907a5f
caps.latest.revision: 22
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
# How to: Dynamically Specify Predicate Filters at Runtime (C# Programming Guide)
In some cases you do not know until run time how many predicates you have to apply to source elements in the `where` clause. One way to dynamically specify multiple predicate filters is to use the <xref:System.Linq.Enumerable.Contains*> method, as shown in the following example. The example is constructed in two ways. First, the project is run by filtering on values that are provided in the program. Then the project is run again by using input provided at run time.  
  
### To filter by using the Contains method  
  
1.  Open a new console application in Visual Studio. Name it `PredicateFilters`.  
  
2.  Copy the `StudentClass` class from [How to: Query a Collection of Objects](../../../csharp\programming-guide\linq-query-expressions/how-to-query-a-collection-of-objects.md) and paste it into namespace `PredicateFilters` underneath class `Program`. `StudentClass` provides a list of `Student` objects.  
  
3.  Comment out the `Main` method in `StudentClass`.  
  
4.  Replace class `Program` with the following code.  
  
     [!code-cs[csProgGuideLINQ#26](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-dynamically-specify-predicate-filters-at-runtime_1.cs)]  
  
5.  Add the following line to the `Main` method in class `DynamicPredicates`, under the declaration of `ids`.  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
6.  Press F5 to run the project.  
  
7.  The following output is displayed in a Command Prompt window:  
  
     Garcia: 114  
  
     O'Donnell: 112  
  
     Omelchenko: 111  
  
8.  The next step is to run the project again, this time by using input entered at run time instead of array `ids`. In **Solution Explorer**, right-click **PredicateFilters** and then click **Properties**.  
  
9. Click the **Debug** tab.  
  
10. In the **Command line arguments** window, type 122, 117, 120, and 115, separated by spaces: `122 117 120 115`. When the project is run, those values become elements of `args`, the parameter of the `Main` method.  
  
11. Change `QueryByID(ids)` to `QueryByID(args)` in the `Main` method.  
  
12. Press F5 to run the project.  
  
13. The following output is displayed in a Command Prompt window:  
  
     Adams: 120  
  
     Feng: 117  
  
     Garcia: 115  
  
     Tucker: 122  
  
### To filter by using a switch statement  
  
1.  You can use a `switch` statement to select among predetermined alternative queries. In the following example, `studentQuery` uses a different `where` clause depending on which grade level, or year, is specified at run time.  
  
2.  Copy the following method and paste it into class `DynamicPredicates`.  
  
     [!code-cs[csProgGuideLINQ#27](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-dynamically-specify-predicate-filters-at-runtime_2.cs)]  
  
3.  In the **Command line arguments** window, replace the ID numbers from the previous procedure with an integer value between 1 and 4.  
  
4.  In the `Main` method, replace the call to `QueryByID` with the following call, which sends the first element from the `args` array as its argument: `QueryByYear(args[0])`.  
  
5.  Press F5 to run the project.  
  
### To use this method in your own applications  
  
-   When you adapt this method to your own application, remember that LINQ requires version 3.5 or 4 of the [!INCLUDE[dnprdnshort](../../../csharp\getting-started/includes/dnprdnshort_md.md)], and that the project must contain a reference to System.Core.dll and a `using` directive for `System.Linq`. LINQ to SQL, LINQ to XML, and LINQ to DataSet types require additional `using` directives and references. For more information, see [How to: Create a LINQ Project](../Topic/How%20to:%20Create%20a%20LINQ%20Project.md).  
  
## See Also  
 [LINQ Query Expressions](../../../csharp\programming-guide\linq-query-expressions/index.md)   
 [where clause](../../../csharp\language-reference\keywords/where-clause.md)