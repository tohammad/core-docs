---
title: "Using Variance in Interfaces for Generic Collections (Visual Basic)"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
ms.assetid: c867fcea-7462-4995-b9c5-542feec74036
caps.latest.revision: 3
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Using Variance in Interfaces for Generic Collections (Visual Basic)
A covariant interface allows its methods to return more derived types than those specified in the interface. A contravariant interface allows its methods to accept parameters of less derived types than those specified in the interface.  
  
 In .NET Framework 4, several existing interfaces became covariant and contravariant. These include <xref:System.Collections.Generic.IEnumerable`1> and <xref:System.IComparable`1>. This enables you to reuse methods that operate with generic collections of base types for collections of derived types.  
  
 For a list of variant interfaces in the .NET Framework, see [Variance in Generic Interfaces (Visual Basic)](../../../../visual-basic\programming-guide\concepts\covariance-contravariance/variance-in-generic-interfaces.md).  
  
## Converting Generic Collections  
 The following example illustrates the benefits of covariance support in the <xref:System.Collections.Generic.IEnumerable`1> interface. The `PrintFullName` method accepts a collection of the `IEnumerable(Of Person)` type as a parameter. However, you can reuse it for a collection of the `IEnumerable(Of Person)` type because `Employee` inherits `Person`.  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
## Comparing Generic Collections  
 The following example illustrates the benefits of contravariance support in the <xref:System.Collections.Generic.IComparer`1> interface. The `PersonComparer` class implements the `IComparer(Of Person)` interface. However, you can reuse this class to compare a sequence of objects of the `Employee` type because `Employee` inherits `Person`.  
  
```vb  
' Simple hierarhcy of classes.  
Public Class Person  
    Public Property FirstName As String  
    Public Property LastName As String  
End Class  
  
Public Class Employee  
    Inherits Person  
End Class  
' The custom comparer for the Person type  
' with standard implementations of Equals()  
' and GetHashCode() methods.  
Class PersonComparer  
    Implements IEqualityComparer(Of Person)  
  
    Public Function Equals1(  
        ByVal x As Person,  
        ByVal y As Person) As Boolean _  
        Implements IEqualityComparer(Of Person).Equals  
  
        If x Is y Then Return True  
        If x Is Nothing OrElse y Is Nothing Then Return False  
        Return (x.FirstName = y.FirstName) AndAlso  
            (x.LastName = y.LastName)  
    End Function  
    Public Function GetHashCode1(  
        ByVal person As Person) As Integer _  
        Implements IEqualityComparer(Of Person).GetHashCode  
  
        If person Is Nothing Then Return 0  
        Dim hashFirstName =  
            If(person.FirstName Is Nothing,  
            0, person.FirstName.GetHashCode())  
        Dim hashLastName = person.LastName.GetHashCode()  
        Return hashFirstName Xor hashLastName  
    End Function  
End Class  
  
Sub Main()  
    Dim employees = New List(Of Employee) From {  
        New Employee With {.FirstName = "Michael", .LastName = "Alexander"},  
        New Employee With {.FirstName = "Jeff", .LastName = "Price"}  
    }  
  
    ' You can pass PersonComparer,   
    ' which implements IEqualityComparer(Of Person),  
    ' although the method expects IEqualityComparer(Of Employee)  
  
    Dim noduplicates As IEnumerable(Of Employee) = employees.Distinct(New PersonComparer())  
  
    For Each employee In noduplicates  
        Console.WriteLine(employee.FirstName & " " & employee.LastName)  
    Next  
End Sub  
```  
  
## See Also  
 [Variance in Generic Interfaces (Visual Basic)](../../../../visual-basic\programming-guide\concepts\covariance-contravariance/variance-in-generic-interfaces.md)