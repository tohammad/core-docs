---
title: "Arrays (C# Programming Guide)"
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
  - "arrays [C#]"
  - "C# language, arrays"
ms.assetid: bb79bdde-e570-4c30-adb0-1dd5759ae041
caps.latest.revision: 33
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
# Arrays (C# Programming Guide)
You can store multiple variables of the same type in an array data structure. You declare an array by specifying the type of its elements.  
  
 `type[] arrayName;`  
  
 The following examples create single-dimensional, multidimensional, and jagged arrays:  
  
 [!code-cs[csProgGuideArrays#1](../../../csharp\programming-guide\arrays/codesnippet/CSharp/index_1.cs)]  
  
## Array Overview  
 An array has the following properties:  
  
-   An array can be [Single-Dimensional](../../../csharp\programming-guide\arrays/single-dimensional-arrays.md), [Multidimensional](../../../csharp\programming-guide\arrays/multidimensional-arrays.md) or [Jagged](../../../csharp\programming-guide\arrays/jagged-arrays.md).  
  
-   The number of dimensions and the length of each dimension are established when the array instance is created. These values can't be changed during the lifetime of the instance.  
  
-   The default values of numeric array elements are set to zero, and reference elements are set to null.  
  
-   A jagged array is an array of arrays, and therefore its elements are reference types and are initialized to `null`.  
  
-   Arrays are zero indexed: an array with `n` elements is indexed from `0` to `n-1`.  
  
-   Array elements can be of any type, including an array type.  
  
-   Array types are [reference types](../../../csharp\language-reference\keywords/reference-types.md) derived from the abstract base type <xref:System.Array>. Since this type implements <xref:System.Collections.IEnumerable> and <xref:System.Collections.Generic.IEnumerable`1>, you can use [foreach](../../../csharp\language-reference\keywords/foreach-in.md) iteration on all arrays in C#.  
  
## Related Sections  
  
-   [Arrays as Objects](../../../csharp\programming-guide\arrays/arrays-as-objects.md)  
  
-   [Using foreach with Arrays](../../../csharp\programming-guide\arrays/using-foreach-with-arrays.md)  
  
-   [Passing Arrays as Arguments](../../../csharp\programming-guide\arrays/passing-arrays-as-arguments.md)  
  
-   [Passing Arrays Using ref and out](../../../csharp\programming-guide\arrays/passing-arrays-using-ref-and-out.md)  
  
-   [More About Variables](http://go.microsoft.com/fwlink/?LinkId=221230) in [Beginning Visual C# 2010](http://go.microsoft.com/fwlink/?LinkId=221214)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../../../csharp\language-reference\keywords/includes/csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [Collections](../Topic/Collections%20\(C%23%20and%20Visual%20Basic\).md)   
 [Array Collection Type](http://msdn.microsoft.com/en-us/8a9964de-8941-47b1-a3cf-a01bc88db9e8)