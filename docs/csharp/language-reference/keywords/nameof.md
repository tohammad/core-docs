---
title: "nameof (C# and Visual Basic Reference)"
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
ms.assetid: 33601bf3-cc2c-4496-846d-f9679bccf2a7
caps.latest.revision: 3
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
# nameof (C# and Visual Basic Reference)
Used to obtain the simple (unqualified) string name of a variable, type, or member.  When reporting errors in code, hooking up model-view-controller (MVC) links, firing property changed events, etc., you often want to capture the string name of a method.  Using `nameof` helps keep your code valid when renaming definitions.  Before you had to use string literals to refer to definitions, which is brittle when renaming code elements because tools do not know to check these string literals.  
  
 A `nameof` expression has this form:  
  
```c#  
if (x == null) throw new ArgumentNullException(nameof(x));  
WriteLine(nameof(person.Address.ZipCode)); // prints "ZipCode”  
  
```  
  
## Key Use Cases  
 These examples show the key use cases for `nameof`.  
  
 Validate parameters:  
 ```c#  
void f(string s) {  
    if (s == null) throw new ArgumentNullException(nameof(s));  
}  
  
```  
  
 MVC Action links:  
 ```html  
<%= Html.ActionLink("Sign up",  
             @typeof(UserController),  
             @nameof(UserController.SignUp))  
%>  
  
```  
  
 INotifyPropertyChanged:  
 ```c#  
int p {  
    get { return this.p; }  
    set { this.p = value; PropertyChanged(this, new PropertyChangedEventArgs(nameof(this.p)); } // nameof(p) works too  
}  
  
```  
  
 XAML dependency property:  
 ```c#  
public static DependencyProperty AgeProperty = DependencyProperty.Register(nameof(Age), typeof(int), typeof(C));  
  
```  
  
 Logging:  
 ```c#  
void f(int i) {  
    Log(nameof(f), "method entry");  
}  
  
```  
  
 Attributes:  
 ```c#  
[DebuggerDisplay("={" + nameof(GetString) + "()}")]  
class C {  
    string GetString() { }  
}  
```  
  
## Examples  
 Some C# examples:  
  
```c#  
using Stuff = Some.Cool.Functionality  
class C {  
    static int Method1 (string x, int y) {}  
    static int Method1 (string x, string y) {}  
    int Method2 (int z) {}  
    string f<T>() => nameof(T);  
}  
  
var c = new C()  
  
nameof(C) -> "C"  
nameof(C.Method1) -> "Method1"   
nameof(C.Method2) -> "Method2"  
nameof(c.Method1) -> "Method1"   
nameof(c.Method2) -> "Method2"  
nameof(z) -> "z" // inside of Method2 ok, inside Method1 is a compiler error  
nameof(Stuff) = "Stuff"  
nameof(T) -> "T" // works inside of method but not in attributes on the method  
nameof(f) -> “f”  
nameof(f<T>) -> syntax error  
nameof(f<>) -> syntax error  
nameof(Method2()) -> error “This expression does not have a name”  
  
```  
  
 Many of the above samples apply to Visual Basic.  Here are some specific Visual Basic examples:  
  
```vb  
NameOf(a!Foo) -> ' error  "This expression does not have a name"  
NameOf(dict("Foo")) -> ' error  "This expression does not have a name": default property access  
NameOf(dict.Item("Foo")) -> ' error  "This expression does not have a name"  
NameOf(arr(2)) -> ' error  "This expression does not have a name": array element index  
Dim x = Nothing   
NameOf(x.ToString(2)) -> ' error  "This expression does not have a name"  
Dim o = Nothing  
NameOf(o.Equals) -> ' result "Equals".  Warning: "Access of static member of instance; instance will not be evaluated"  
  
```  
  
## Remarks  
 The argument to `nameof` must be a simple name, qualified name, member access, base access with a specified member, or this access with a specified member.  The argument expression identifies a code definition, but it is never evaluated.  
  
 Because the argument needs to be an expression syntactically, there are many things disallowed that are not useful to list.  The following are worth mentioning that produce errors: predefined types (for example, `int` or `void`), nullable types (`Point?`), array types (`Customer[,]`), pointer types (`Buffer*`), qualified alias (`A::B`), and unbound generic types (`Dictionary<,>`), preprocessing symbols (`DEBUG`), and labels (`loop:`).  
  
 If you need to get the fully-qualified name, you can use the `typeof` expression along with `nameof`.  
  
 In the examples you see that you can use a type name and access an instance method name.  You do not need to have an instance of the type, as required in evaluated expressions.  Using the type name can be very convenient in some situations, and since you are just referring to the name and not using instance data, you do not need to contrive an instance variable or expression.  
  
 You can reference the members of a class in attribute expressions on the class.  
  
 There is no way to get a signatures information such as "`Method1 (str, str)`".  One way to do that is to use an Expression, `Expression e = () => A.B.Method1("s1", "s2")`, and pull the MemberInfo from the resulting expression tree.  
  
## Language Specifications  
 [!INCLUDE[CSharplangspec](../../../csharp\language-reference\keywords/includes/csharplangspec_md.md)]  
  
 For more information, see the [Visual Basic Language Reference](../../../visual-basic\language-reference/index.md).  
  
## See Also  
 [C# Reference](../../../csharp\language-reference/index.md)   
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [typeof](../../../csharp\language-reference\keywords/typeof.md)   
 [Visual Basic Language Reference](../../../visual-basic\language-reference/index.md)   
 [Visual Basic Programming Guide](../../../visual-basic\programming-guide/index.md)