---
title: "编译器错误 CS0819 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0819"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0819"
ms.assetid: a5369e03-eb7d-4c88-b390-51304bd8d1ae
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0819
隐式类型化的局部变量不能有多个声明符。  
  
 显式类型声明中允许有多个声明符，而隐式类型化的变量不允许。  
  
### 更正此错误  
  
1.  在单独的行上声明每个隐式类型化的局部变量并为其赋值。  
  
## 示例  
 下面的代码生成 CS0819：  
  
```  
// cs0819.cs class A { public static int Main() { var a = 3, b = 2; // CS0819 return -1; } }  
```  
  
## 请参阅  
 [隐式类型的局部变量](/dotnet/csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables)