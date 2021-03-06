---
title: "编译器错误 CS0459 | Microsoft Docs"
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
  - "CS0459"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0459"
ms.assetid: 01b058dd-8d65-4e9d-9de1-d47f9488d22a
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0459
无法获得只读局部变量的地址  
  
 C\# 语言中有三种可生成只读局部变量的常见方案：`foreach``using` 和 `fixed`。 在每种情况下，不允许写入只读本地变量，或获取其地址。 编译器发现尝试获取只读局部变量的地址时，会生成此错误。  
  
## 示例  
 以下示例当尝试获取 `foreach` 循环和 `fixed` 语句块中的只读局部变量的地址时，将生成 CS0459。  
  
```  
// CS0459.cs // compile with: /unsafe class A { public unsafe void M1() { int[] ints = new int[] { 1, 2, 3 }; foreach (int i in ints) { int *j = &i;  // CS0459 } fixed (int *i = &_i) { int **j = &i;  // CS0459 } } private int _i = 0; }  
```