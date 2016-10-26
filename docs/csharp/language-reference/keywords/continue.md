---
title: "continue (C# Reference)"
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
  - "continue_CSharpKeyword"
  - "continue"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "continue keyword [C#]"
ms.assetid: 8a5ac96f-f98a-4519-b32d-345847ed7be0
caps.latest.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# continue (C# Reference)
The `continue` statement passes control to the next iteration of the enclosing [while](../../../csharp\language-reference\keywords/while.md), [do](../../../csharp\language-reference\keywords/do.md), [for](../../../csharp\language-reference\keywords/for.md), or [foreach](../../../csharp\language-reference\keywords/foreach-in.md) statement in which it appears.  
  
## Example  
 In this example, a counter is initialized to count from 1 to 10. By using the `continue` statement in conjunction with the expression `(i < 9)`, the statements between `continue` and the end of the `for` body are skipped.  
  
 [!code-cs[csrefKeywordsJump#3](../../../csharp\language-reference\keywords/codesnippet/CSharp/continue_1.cs)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../../../csharp\language-reference\keywords/includes/csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../../../csharp\language-reference/index.md)   
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [C# Keywords](../../../csharp\language-reference\keywords/index.md)   
 [break Statement](../Topic/break%20Statement%20\(C++\).md)   
 [Jump Statements](../../../csharp\language-reference\keywords/jump-statements.md)