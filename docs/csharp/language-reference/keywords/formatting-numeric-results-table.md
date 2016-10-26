---
title: "Formatting Numeric Results Table (C# Reference)"
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
  - "formatting [C#]"
  - "numeric formatting [C#]"
  - "String.Format method"
  - "Console.Write method"
ms.assetid: 120ba537-4448-4c62-8676-7a8fdd98f496
caps.latest.revision: 14
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
# Formatting Numeric Results Table (C# Reference)
You can format numeric results by using the <xref:System.String.Format*?displayProperty=fullName> method, or through the <xref:System.Console.Write*?displayProperty=fullName> or <xref:System.Console.WriteLine*?displayProperty=fullName> method, which calls `String.Format`. The format is specified by using format strings. The following table contains the supported standard format strings. The format string takes the following form: `Axx`, where `A` is the format specifier and `xx` is the precision specifier. The format specifier controls the type of formatting applied to the numeric value, and the precision specifier controls the number of significant digits or decimal places of the formatted output. The value of the precision specifier ranges from 0 to 99.  
  
 For more information about standard and custom formatting strings, see [Formatting Types](../Topic/Formatting%20Types%20in%20the%20.NET%20Framework.md). For more information about the `String.Format` method, see <xref:System.String.Format*?displayProperty=fullName>.  
  
|Format Specifier|Description|Examples|Output|  
|----------------------|-----------------|--------------|------------|  
|C or c|Currency|Console.Write("{0:C}", 2.5);<br /><br /> Console.Write("{0:C}", -2.5);|$2.50<br /><br /> ($2.50)|  
|D or d|Decimal|Console.Write("{0:D5}", 25);|00025|  
|E or e|Scientific|Console.Write("{0:E}", 250000);|2.500000E+005|  
|F or f|Fixed-point|Console.Write("{0:F2}", 25);<br /><br /> Console.Write("{0:F0}", 25);|25.00<br /><br /> 25|  
|G or g|General|Console.Write("{0:G}", 2.5);|2.5|  
|N or n|Number|Console.Write("{0:N}", 2500000);|2,500,000.00|  
|X or x|Hexadecimal|Console.Write("{0:X}", 250);<br /><br /> Console.Write("{0:X}", 0xffff);|FA<br /><br /> FFFF|  
  
## See Also  
 [C# Reference](../../../csharp\language-reference/index.md)   
 [C# Programming Guide](../../../csharp\programming-guide/index.md)   
 [Standard Numeric Format Strings](../Topic/Standard%20Numeric%20Format%20Strings.md)   
 [Reference Tables for Types](../../../csharp\language-reference\keywords/reference-tables-for-types.md)   
 [string](../../../csharp\language-reference\keywords/string.md)