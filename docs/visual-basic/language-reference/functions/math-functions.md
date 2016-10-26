---
title: "Math Functions (Visual Basic)"
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
helpviewer_keywords: 
  - "math functions, Visual Basic"
  - "arithmetic operations, math functions"
  - "math routines"
  - "Atn function"
ms.assetid: 4d2d82e7-6924-42fe-a4a7-b4dd5bebbd0c
caps.latest.revision: 23
author: "stevehoag"
ms.author: "shoag"
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
# Math Functions (Visual Basic)
The methods of the <xref:System.Math?displayProperty=fullName> class provide trigonometric, logarithmic, and other common mathematical functions.  
  
## Remarks  
 The following table lists methods of the <xref:System.Math?displayProperty=fullName> class. You can use these in a Visual Basic program.  
  
|.NET Framework method|Description|  
|---------------------------|-----------------|  
|<xref:System.Math.Abs*>|Returns the absolute value of a number.|  
|<xref:System.Math.Acos*>|Returns the angle whose cosine is the specified number.|  
|<xref:System.Math.Asin*>|Returns the angle whose sine is the specified number.|  
|<xref:System.Math.Atan*>|Returns the angle whose tangent is the specified number.|  
|<xref:System.Math.Atan2*>|Returns the angle whose tangent is the quotient of two specified numbers.|  
|<xref:System.Math.BigMul*>|Returns the full product of two 32-bit numbers.|  
|<xref:System.Math.Ceiling*>|Returns the smallest integral value that's greater than or equal to the specified `Decimal` or `Double`.|  
|<xref:System.Math.Cos*>|Returns the cosine of the specified angle.|  
|<xref:System.Math.Cosh*>|Returns the hyperbolic cosine of the specified angle.|  
|<xref:System.Math.DivRem*>|Returns the quotient of two 32-bit or 64-bit signed integers, and also returns the remainder in an output parameter.|  
|<xref:System.Math.Exp*>|Returns e (the base of natural logarithms) raised to the specified power.|  
|<xref:System.Math.Floor*>|Returns the largest integer that's less than or equal to the specified `Decimal` or `Double` number.|  
|<xref:System.Math.IEEERemainder*>|Returns the remainder that results from the division of a specified number by another specified number.|  
|<xref:System.Math.Log*>|Returns the natural (base e) logarithm of a specified number or the logarithm of a specified number in a specified base.|  
|<xref:System.Math.Log10*>|Returns the base 10 logarithm of a specified number.|  
|<xref:System.Math.Max*>|Returns the larger of two numbers.|  
|<xref:System.Math.Min*>|Returns the smaller of two numbers.|  
|<xref:System.Math.Pow*>|Returns a specified number raised to the specified power.|  
|<xref:System.Math.Round*>|Returns a `Decimal` or `Double` value rounded to the nearest integral value or to a specified number of fractional digits.|  
|<xref:System.Math.Sign*>|Returns an `Integer` value indicating the sign of a number.|  
|<xref:System.Math.Sin*>|Returns the sine of the specified angle.|  
|<xref:System.Math.Sinh*>|Returns the hyperbolic sine of the specified angle.|  
|<xref:System.Math.Sqrt*>|Returns the square root of a specified number.|  
|<xref:System.Math.Tan*>|Returns the tangent of the specified angle.|  
|<xref:System.Math.Tanh*>|Returns the hyperbolic tangent of the specified angle.|  
|<xref:System.Math.Truncate*>|Calculates the integral part of a specified `Decimal` or `Double` number.|  
  
 To use these functions without qualification, import the <xref:System.Math?displayProperty=fullName> namespace into your project by adding the following code to the top of your source file:  
  
```  
Imports System.Math  
```  
  
## Example  
 This example uses the <xref:System.Math.Abs*> method of the <xref:System.Math> class to compute the absolute value of a number.  
  
```  
' Returns 50.3.  
Dim MyNumber1 As Double = Math.Abs(50.3)  
' Returns 50.3.  
Dim MyNumber2 As Double = Math.Abs(-50.3)  
```  
  
## Example  
 This example uses the <xref:System.Math.Atan*> method of the <xref:System.Math> class to calculate the value of pi.  
  
```  
Public Function GetPi() As Double  
    ' Calculate the value of pi.  
    Return 4.0 * Math.Atan(1.0)  
End Function  
```  
  
## Example  
 This example uses the <xref:System.Math.Cos*> method of the <xref:System.Math> class to return the cosine of an angle.  
  
```  
Public Function Sec(ByVal angle As Double) As Double  
    ' Calculate the secant of angle, in radians.  
    Return 1.0 / Math.Cos(angle)  
End Function  
```  
  
## Example  
 This example uses the <xref:System.Math.Exp*> method of the <xref:System.Math> class to return e raised to a power.  
  
```  
Public Function Sinh(ByVal angle As Double) As Double  
    ' Calculate hyperbolic sine of an angle, in radians.  
    Return (Math.Exp(angle) - Math.Exp(-angle)) / 2.0  
End Function  
```  
  
## Example  
 This example uses the <xref:System.Math.Log*> method of the <xref:System.Math> class to return the natural logarithm of a number.  
  
```  
Public Function Asinh(ByVal value As Double) As Double  
    ' Calculate inverse hyperbolic sine, in radians.  
    Return Math.Log(value + Math.Sqrt(value * value + 1.0))  
End Function  
```  
  
## Example  
 This example uses the <xref:System.Math.Round*> method of the <xref:System.Math> class to round a number to the nearest integer.  
  
```  
' Returns 3.  
Dim MyVar2 As Double = Math.Round(2.8)  
```  
  
## Example  
 This example uses the <xref:System.Math.Sign*> method of the <xref:System.Math> class to determine the sign of a number.  
  
```  
' Returns 1.  
Dim MySign1 As Integer = Math.Sign(12)  
' Returns -1.  
Dim MySign2 As Integer = Math.Sign(-2.4)  
' Returns 0.  
Dim MySign3 As Integer = Math.Sign(0)  
```  
  
## Example  
 This example uses the <xref:System.Math.Sin*> method of the <xref:System.Math> class to return the sine of an angle.  
  
```  
Public Function Csc(ByVal angle As Double) As Double  
    ' Calculate cosecant of an angle, in radians.  
    Return 1.0 / Math.Sin(angle)  
End Function  
```  
  
## Example  
 This example uses the <xref:System.Math.Sqrt*> method of the <xref:System.Math> class to calculate the square root of a number.  
  
```  
' Returns 2.  
Dim MySqr1 As Double = Math.Sqrt(4)  
' Returns 4.79583152331272.  
Dim MySqr2 As Double = Math.Sqrt(23)  
' Returns 0.  
Dim MySqr3 As Double = Math.Sqrt(0)  
' Returns NaN (not a number).  
Dim MySqr4 As Double = Math.Sqrt(-4)  
```  
  
## Example  
 This example uses the <xref:System.Math.Tan*> method of the <xref:System.Math> class to return the tangent of an angle.  
  
```  
Public Function Ctan(ByVal angle As Double) As Double  
    ' Calculate cotangent of an angle, in radians.  
    Return 1.0 / Math.Tan(angle)  
End Function  
```  
  
## Requirements  
 **Class:** <xref:System.Math>  
  
 **Namespace:** <xref:System>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
## See Also  
 <xref:Microsoft.VisualBasic.VBMath.Rnd*>   
 <xref:Microsoft.VisualBasic.VBMath.Randomize*>   
 <xref:System.Double.NaN>   
 [Derived Math Functions](../../../visual-basic\language-reference\keywords/derived-math-functions.md)   
 [Arithmetic Operators](../../../visual-basic\language-reference\operators/arithmetic-operators.md)