---
title: "编译器错误 CS0081 | Microsoft Docs"
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
  - "CS0081"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0081"
ms.assetid: a5649abc-89ea-4f64-8c3c-eb36df926561
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0081
类型形参声明必须是标识符，不能是类型  
  
 声明泛型方法或类型时，请将类型形参指定为标识符，例如“T”或“inputType”。 当客户端代码调用该方法时，它会提供类型，该类型将替换该标识符在该方法或类正文中的每个匹配项。 有关详细信息，请参阅[泛型类型参数](/dotnet/csharp/programming-guide/generics/generic-type-parameters)。  
  
```  
// CS0081.cs class MyClass { public void F<int>() {}   // CS0081 public void F<T>(T input) {}   // OK public static void Main() { MyClass a = new MyClass(); a.F<int>(2); a.F<double>(.05); } }  
```  
  
## 请参阅  
 [泛型](/dotnet/csharp/programming-guide/generics/index)