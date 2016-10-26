---
title: "typeof (C# Reference)"
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
  - "typeof"
  - "typeof_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "typeof keyword [C#]"
ms.assetid: 0c08d880-515e-46bb-8cd2-48b8dd62c08d
caps.latest.revision: 21
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
# typeof (C# Reference)
Used to obtain the `System.Type` object for a type. A `typeof` expression takes the following form:  
  
```  
System.Type type = typeof(int);  
```  
  
## Remarks  
 To obtain the run-time type of an expression, you can use the .NET Framework method <xref:System.Object.GetType*>, as in the following example:  
  
```  
int i = 0;  
System.Type type = i.GetType();  
```  
  
 The `typeof` operator cannot be overloaded.  
  
 The `typeof` operator can also be used on open generic types. Types with more than one type parameter must have the appropriate number of commas in the specification. The following example shows how to determine whether the return type of a method is a generic <xref:System.Collections.Generic.IEnumerable`1>. Assume that method is an instance of a MethodInfo type:  
  
```  
string s = method.ReturnType.GetInterface  
    (typeof(System.Collections.Generic.IEnumerable<>).FullName);  
```  
  
## Example  
 [!code-cs[csrefKeywordsOperator#12](../../../csharp\language-reference\keywords/codesnippet/CSharp/typeof_1.cs)]  
  
## Example  
 This sample uses the <xref:System.Object.GetType*> method to determine the type that is used to contain the result of a numeric calculation. This depends on the storage requirements of the resulting number.  
  
 [!code-cs[csrefKeywordsOperator#13](../../../csharp\language-reference\keywords/codesnippet/CSharp/typeof_2.cs)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../../../csharp\language-reference\keywords/includes/csharplangspec_md.md)]  
  
## See Also  
 <xref:System.Type?displayProperty=fullName>   
 [C# Reference](../../../csharp\language-reference/index.md)   
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [C# Keywords](../../../csharp\language-reference\keywords/index.md)   
 [is](../../../csharp\language-reference\keywords/is.md)   
 [Operator Keywords](../../../csharp\language-reference\keywords/operator-keywords.md)