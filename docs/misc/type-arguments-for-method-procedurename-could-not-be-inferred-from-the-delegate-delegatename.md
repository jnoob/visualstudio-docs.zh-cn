---
title: "无法从委托“&lt;delegatename&gt;”中推理方法“&lt;procedurename&gt;”的类型参数 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30952"
  - "bc30952"
helpviewer_keywords: 
  - "BC30952"
ms.assetid: 5eb804ce-2e93-4668-b655-7fe00815e552
caps.latest.revision: 6
caps.handback.revision: 6
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 无法从委托“&lt;delegatename&gt;”中推理方法“&lt;procedurename&gt;”的类型参数
赋值语句使用 `AddressOf` 将泛型过程的地址赋给委托，但它不会为泛型过程提供任何类型参数。  
  
 通常，在调用某个泛型类型时，要为该泛型类型定义的每个类型形参提供一个类型实参。 如果未提供任何类型实参，编译器将尝试推断要传递给类型形参的类型。 如果上下文未提供足够的信息供编译器推导类型，将产生错误。  
  
 **错误 ID：**BC30952  
  
### 更正此错误  
  
-   为 `AddressOf` 表达式中的泛型过程指定类型参数。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [AddressOf 运算符](/dotnet/visual-basic/language-reference/operators/addressof-operator)   
 [Visual Basic 中的泛型过程](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures)   
 [类型列表](/dotnet/visual-basic/language-reference/statements/type-list)