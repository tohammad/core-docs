---
title: "How to: Initialize Objects by Using an Object Initializer (C# Programming Guide)"
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
  - "object initializers [C#], how to use"
  - "objects [C#], initializing"
ms.assetid: 4b75ebb2-2e29-43de-929c-d736a8f27ce6
caps.latest.revision: 20
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
# How to: Initialize Objects by Using an Object Initializer (C# Programming Guide)
You can use object initializers to initialize type objects in a declarative manner without explicitly invoking a constructor for the type.  
  
 The following examples show how to use object initializers with named objects. The compiler processes object initializers by first accessing the default instance constructor and then processing the member initializations. Therefore, if the default constructor is declared as `private` in the class, object initializers that require public access will fail.  
  
 You must use an object initializer if you're defining an anonymous type. For more information, see [How to: Return Subsets of Element Properties in a Query](../../../csharp\programming-guide\classes-and-structs/how-to-return-subsets-of-element-properties-in-a-query.md).  
  
## Example  
 The following example shows how to initialize a new `StudentName` type by using object initializers.  
  
 [!code-cs[csProgGuideLINQ#35](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-initialize-objects-by-using-an-object-initializer_1.cs)]  
  
## Example  
 The following example shows how to initialize a collection of `StudentName` types by using a collection initializer. Note that a collection initializer is a series of comma-separated object initializers.  
  
 [!code-cs[csProgGuideLINQ#36](../../../csharp\programming-guide\classes-and-structs/codesnippet/CSharp/how-to-initialize-objects-by-using-an-object-initializer_2.cs)]  
  
## Compiling the Code  
 To run this code, copy and paste the class into a Visual C# console application project that has been created in [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)]. For more information, see [How to: Create a LINQ Project](../Topic/How%20to:%20Create%20a%20LINQ%20Project.md).  
  
## See Also  
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [Object and Collection Initializers](../../../csharp\programming-guide\classes-and-structs/object-and-collection-initializers.md)