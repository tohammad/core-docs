---
title: "delegate (C# Reference)"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "delegate_CSharpKeyword"
  - "delegate"
  - "CS0123"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "delegate keyword [C#]"
  - "function pointers [C#]"
ms.assetid: 0bb8cb6d-2f87-47c7-9d1f-d65c1cd01e9f
caps.latest.revision: 24
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
# delegate (C# Reference)
The declaration of a delegate type is similar to a method signature. It has a return value and any number of parameters of any type:  
  
```  
public delegate void TestDelegate(string message);  
public delegate int TestDelegate(MyType m, long num);  
```  
  
 A `delegate` is a reference type that can be used to encapsulate a named or an anonymous method. Delegates are similar to function pointers in C++; however, delegates are type-safe and secure. For applications of delegates, see [Delegates](../../../csharp\programming-guide\delegates/index.md) and [Generic Delegates](../../../csharp\programming-guide\generics/generic-delegates.md).  
  
## Remarks  
 Delegates are the basis for [Events](../../../csharp\programming-guide\events/index.md).  
  
 A delegate can be instantiated by associating it either with a named or anonymous method. For more information, see [Named Methods](../../../csharp\programming-guide\delegates/delegates-with-named-vs-anonymous-methods.md) and [Anonymous Methods](../../../csharp\programming-guide\statements-expressions-operators/anonymous-methods.md).  
  
 The delegate must be instantiated with a method or lambda expression that has a compatible return type and input parameters. For more information on the degree of variance that is allowed in the method signature, see [Variance in Delegates](../Topic/Variance%20in%20Delegates%20\(C%23%20and%20Visual%20Basic\).md). For use with anonymous methods, the delegate and the code to be associated with it are declared together. Both ways of instantiating delegates are discussed in this section.  
  
## Example  
 [!code-cs[csrefKeywordsTypes#8](../../../csharp\language-reference\keywords/codesnippet/CSharp/delegate_1.cs)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../../../csharp\language-reference\keywords/includes/csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../../../csharp\language-reference/index.md)   
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [C# Keywords](../../../csharp\language-reference\keywords/index.md)   
 [Reference Types](../../../csharp\language-reference\keywords/reference-types.md)   
 [Delegates](../../../csharp\programming-guide\delegates/index.md)   
 [Events](../../../csharp\programming-guide\events/index.md)   
 [Delegates with Named vs. Anonymous Methods](../../../csharp\programming-guide\delegates/delegates-with-named-vs-anonymous-methods.md)   
 [Anonymous Methods](../../../csharp\programming-guide\statements-expressions-operators/anonymous-methods.md)