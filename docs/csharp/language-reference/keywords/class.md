---
title: "class (C# Reference)"
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
  - "class_CSharpKeyword"
  - "class"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "class keyword [C#]"
ms.assetid: b95d8815-de18-4c3f-a8cc-a0a53bdf8690
caps.latest.revision: 30
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
# class (C# Reference)
Classes are declared using the keyword `class`, as shown in the following example:  
  
```  
  
      class TestClass  
{  
    // Methods, properties, fields, events, delegates   
    // and nested classes go here.  
}  
```  
  
## Remarks  
 Only single inheritance is allowed in C#. In other words, a class can inherit implementation from one base class only. However, a class can implement more than one interface. The following table shows examples of class inheritance and interface implementation:  
  
|Inheritance|Example|  
|-----------------|-------------|  
|None|`class ClassA { }`|  
|Single|`class DerivedClass: BaseClass { }`|  
|None, implements two interfaces|`class ImplClass: IFace1, IFace2 { }`|  
|Single, implements one interface|`class ImplDerivedClass: BaseClass, IFace1 { }`|  
  
 Classes that you declare directly within a namespace, not nested within other classes, can be either [public](../../../csharp\language-reference\keywords/public.md) or [internal](../../../csharp\language-reference\keywords/internal.md). Classes are `internal` by default.  
  
 Class members, including nested classes, can be [public](../../../csharp\language-reference\keywords/public.md), `protected internal`, [protected](../../../csharp\language-reference\keywords/protected.md), [internal](../../../csharp\language-reference\keywords/internal.md), or [private](../../../csharp\language-reference\keywords/private.md). Members are [private](../../../csharp\language-reference\keywords/private.md) by default.  
  
 For more information, see [Access Modifiers](../../../csharp\programming-guide\classes-and-structs/access-modifiers.md).  
  
 You can declare generic classes that have type parameters. For more information, see [Generic Classes](../../../csharp\programming-guide\generics/generic-classes.md).  
  
 A class can contain declarations of the following members:  
  
-   [Constructors](../../../csharp\programming-guide\classes-and-structs/constructors.md)  
  
-   [Destructors](../../../csharp\programming-guide\classes-and-structs/destructors.md)  
  
-   [Constants](../../../csharp\programming-guide\classes-and-structs/constants.md)  
  
-   [Fields](../../../csharp\programming-guide\classes-and-structs/fields.md)  
  
-   [Methods](../../../csharp\programming-guide\classes-and-structs/methods.md)  
  
-   [Properties](../../../csharp\programming-guide\classes-and-structs/properties.md)  
  
-   [Indexers](../../../csharp\programming-guide\indexers/index.md)  
  
-   [Operators](../../../csharp\programming-guide\statements-expressions-operators/operators.md)  
  
-   [Events](../../../csharp\programming-guide\events/index.md)  
  
-   [Delegates](../../../csharp\programming-guide\delegates/index.md)  
  
-   [Classes](../../../csharp\programming-guide\classes-and-structs/classes.md)  
  
-   [Interfaces](../../../csharp\programming-guide\interfaces/index.md)  
  
-   [Structs](../../../csharp\programming-guide\classes-and-structs/structs.md)  
  
## Example  
 The following example demonstrates declaring class fields, constructors, and methods. It also demonstrates object instantiation and printing instance data. In this example, two classes are declared, the `Child` class, which contains two private fields (`name` and `age`) and two public methods. The second class, `StringTest`, is used to contain `Main`.  
  
 [!code-cs[csrefKeywordsTypes#5](../../../csharp\language-reference\keywords/codesnippet/CSharp/class_1.cs)]  
  
## Comments  
 Notice, in the preceding example, that the private fields (`name` and `age`) can only be accessed through the public methods of the `Child` class. For example, you cannot print the child's name, from the `Main` method, using a statement like this:  
  
```  
Console.Write(child1.name);   // Error  
```  
  
 Accessing private members of `Child` from `Main` would only be possible if `Main` were a member of the class.  
  
 Types declared inside a class without an access modifier default to `private`, so the data members in this example would still be `private` if the keyword were removed.  
  
 Finally, notice that for the object created using the default constructor (`child3`), the age field was initialized to zero by default.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../../../csharp\language-reference\keywords/includes/csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../../../csharp\language-reference/index.md)   
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [C# Keywords](../../../csharp\language-reference\keywords/index.md)   
 [Reference Types](../../../csharp\language-reference\keywords/reference-types.md)