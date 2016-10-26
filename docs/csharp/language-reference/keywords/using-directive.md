---
title: "using Directive (C# Reference)"
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
  - "using directive [C#]"
ms.assetid: b42b8e61-5e7e-439c-bb71-370094b44ae8
caps.latest.revision: 31
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
# using Directive (C# Reference)
The `using` directive has three uses:  
  
-   To allow the use of types in a namespace so that you do not have to qualify the use of a type in that namespace:  
  
    ```c#  
    using System.Text;  
    ```  
  
-   To allow you to access static members of a type without having to qualify the access with the type name:  
  
    ```c#  
    using static System.Math;  
    ```  
  
-   To create an alias for a namespace or a type. This is called a *using alias directive*.  
  
    ```c#  
    using Project = PC.MyCompany.Project;  
    ```  
  
 The `using` keyword is also used to create *using statements*, which help ensure that <xref:System.IDisposable> objects such as files and fonts are handled correctly. See [using Statement](../../../csharp\language-reference\keywords/using-statement.md) for more information.  
  
## Using Static Type  
 You can access static members of a type without having to qualify the access with the type name:  
  
```c#  
using static System.Console;   
using static System.Math;  
class Program   
{   
    static void Main()   
    {   
        WriteLine(Sqrt(3*3 + 4*4));   
    }   
}  
  
```  
  
 `Using static` imports only accessible static members and nested types declared in the specified type.  Inherited members are not imported.  You can import from any named type with a using static directive, including Visual Basic modules.  If an F# top-level functions appear in metadata as static members of a named type whose name is a valid C# identifier, then the F# functions can be imported.  
  
 `Using static` makes extension methods declared in the specified type available for extension method lookup.  However, the names of the extension methods are not imported into scope for unqualified reference in code.  
  
 Methods with the same name imported from different types by different using static directives in the same compilation unit or namespace form a method group.  Overload resolution within these method groups follows normal C# rules.  
  
## Remarks  
 The scope of a `using` directive is limited to the file in which it appears.  
  
 Create a `using` alias to make it easier to qualify an identifier to a namespace or type. The right side of a using alias directive must always be a fully-qualified type regardless of the using directives that come before it.  
  
 Create a `using` directive to use the types in a namespace without having to specify the namespace. A `using` directive does not give you access to any namespaces that are nested in the namespace you specify.  
  
 Namespaces come in two categories: user-defined and system-defined. User-defined namespaces are namespaces defined in your code. For a list of the system-defined namespaces, see [.NET Framework Class Library](http://go.microsoft.com/fwlink/?LinkID=227195).  
  
 For examples on referencing methods in other assemblies, see [Creating and Using C# DLLs](../Topic/How%20to:%20Create%20and%20Use%20Assemblies%20Using%20the%20Command%20Line%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Example 1  
  
### Description  
 The following example shows how to define and use a `using` alias for a namespace:  
  
### Code  
 [!code-cs[csrefKeywordsNamespace#8](../../../csharp\language-reference\keywords/codesnippet/CSharp/using-directive_1.cs)]  
  
### Comments  
 A using alias directive cannot have an open generic type on the right hand side. For example, you cannot create a using alias for a List\<T>, but you can create one for a List\<int>.  
  
## Example 2  
  
### Description  
 The following example shows how to define a `using` directive and a `using` alias for a class:  
  
### Code  
 [!code-cs[csrefKeywordsNamespace#9](../../../csharp\language-reference\keywords/codesnippet/CSharp/using-directive_2.cs)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../../../csharp\language-reference\keywords/includes/csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../../../csharp\language-reference/index.md)   
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [Using Namespaces](../../../csharp\programming-guide\namespaces/using-namespaces.md)   
 [C# Keywords](../../../csharp\language-reference\keywords/index.md)   
 [Namespace Keywords](../../../csharp\language-reference\keywords/namespace-keywords.md)   
 [Namespaces](../../../csharp\programming-guide\namespaces/index.md)   
 [using Statement](../../../csharp\language-reference\keywords/using-statement.md)