---
title: "编译器错误 CS0736 | Microsoft Docs"
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
  - "CS0736"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0736"
ms.assetid: 06b14feb-81d5-495f-ab2d-6dc3f5e7216f
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0736
“type name”不实现接口成员“member name”。 “method name”无法实现接口成员，因为它是静态的。  
  
 在将静态方法隐式或显式声明为接口成员的实现时，会生成此错误。  
  
### 更正此错误  
  
-   从方法声明中删除 [static](/dotnet/csharp/language-reference/keywords/static) 修饰符。  
  
-   更改接口方法的名称。  
  
-   重新定义包含类型，使其不从接口继承。  
  
## 示例  
 下面的代码生成 CS0736，因为 `Program.testMethod` 被声明为静态的：  
  
```  
// cs0736.cs namespace CS0736 { interface ITest { int testMethod(int x); } class Program : ITest // CS0736 { public static int testMethod(int x) { return 0; } // Try the following line instead. // public int testMethod(int x) { return 0; } public static void Main() { } } }  
```  
  
## 请参阅  
 [接口](/dotnet/csharp/programming-guide/interfaces/index)