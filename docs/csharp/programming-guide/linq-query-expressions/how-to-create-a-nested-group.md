---
title: "How to: Create a Nested Group (C# Programming Guide)"
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
  - "queries [LINQ in C#], nested groups"
  - "grouping groups in LINQ queries"
  - "grouping LINQ queries"
  - "groups [LINQ in C#], nested"
  - "nested queries [C#]"
  - "query expressions [LINQ in C#], nested groups"
ms.assetid: f48c64af-6d4e-473c-ab27-02f78b5ec2b9
caps.latest.revision: 12
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
# How to: Create a Nested Group (C# Programming Guide)
The following example shows how to create nested groups in a [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)] query expression. Each group that is created according to student year or grade level is then further subdivided into groups based on the individuals' names.  
  
## Example  
 [!code-cs[csProgGuideLINQ#24](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-create-a-nested-group_1.cs)]  
  
 Note that three nested `foreach` loops are required to iterate over the inner elements of a nested group.  
  
## Compiling the Code  
 This example contains references to objects that are defined in the sample application in [How to: Query a Collection of Objects](../../../csharp\programming-guide\linq-query-expressions/how-to-query-a-collection-of-objects.md). To compile and run this method, paste it into the `StudentClass` class in that application and add a call to it from the `Main` method.  
  
 When you adapt this method to your own application, remember that LINQ requires version 3.5 of the [!INCLUDE[dnprdnshort](../../../csharp\getting-started/includes/dnprdnshort_md.md)], and the project must contain a reference to System.Core.dll and a using directive for System.Linq. LINQ to SQL, LINQ to XML and LINQ to DataSet types require additional usings and references. For more information, see [How to: Create a LINQ Project](../Topic/How%20to:%20Create%20a%20LINQ%20Project.md).  
  
## See Also  
 [LINQ Query Expressions](../../../csharp\programming-guide\linq-query-expressions/index.md)