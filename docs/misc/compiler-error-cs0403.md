---
title: "编译器错误 CS0403 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0403"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0403"
ms.assetid: 6e5d55ce-d6bf-419d-aded-aaa2e5963bb6
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0403
无法将 null 转换为类型参数“name”，因为它可能是不可以为 null 的值类型。 请考虑改用 default\('T'\)。  
  
 不能将 null 分配给指定的未知类型，因为它可能是不允许进行 null 赋值的值类型。 如果泛型类不打算接受值类型，请使用类类型约束。 如果它可以接受值类型（如内置类型），则你可能能够使用表达式 `default(T)` 替换 null 赋值，如下面的示例所示。  
  
## 示例  
 下面的示例生成 CS0403。  
  
```  
// CS0403.cs // compile with: /target:library class C<T> { public void f() { T t = null;  // CS0403 T t2 = default(T);   // OK } } class D<T> where T : class { public void f() { T t = null;  // OK } }  
```