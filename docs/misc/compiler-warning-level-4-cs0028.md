---
title: "编译器警告（等级 4）CS0028 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0028"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0028"
ms.assetid: 47df919f-01fa-45ae-a4b7-912445e679e2
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 4）CS0028
“function declaration”的签名错误，不能作为入口点  
  
 `Main` 的方法声明无效：声明它时使用的签名无效。`Main` 必须声明为静态，且它必须返回 [int](/dotnet/csharp/language-reference/keywords/int) 或 [void](/dotnet/csharp/language-reference/keywords/void)。 有关详细信息，请参阅[Main\(\) 和命令行参数](/dotnet/csharp/programming-guide/main-and-command-args/main-and-command-line-arguments)。  
  
 下面的示例生成 CS0028：  
  
```  
// CS0028.cs // compile with: /W:4 /warnaserror public class a { public static double Main(int i)   // CS0028 // Try the following line instead: // public static void Main() { } }  
```