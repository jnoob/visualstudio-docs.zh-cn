---
title: "Option Strict On 禁止将 Object 类型的操作数用于运算符“&lt;运算符名称&gt;” | Microsoft Docs"
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
  - "bc30038"
  - "vbc30038"
helpviewer_keywords: 
  - "BC30038"
ms.assetid: eb047d36-1fb4-460d-ae98-c76f31a89bed
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Option Strict On 禁止将 Object 类型的操作数用于运算符“&lt;运算符名称&gt;”
为对象变量定义的唯一运算符是 `Is` 和 `TypeOf...Is`。 当 `Option Strict` 是 `On` 时，所有操作数必须都属于为给定运算符定义的数据类型。  
  
 **错误 ID：**BC30038  
  
### 更正此错误  
  
-   使用适当的类型转换函数（如 `CInt` 或 `CStr`）将操作数转换为对运算符定义的数据类型。  
  
## 请参阅  
 [Is 运算符](/dotnet/visual-basic/language-reference/operators/is-operator)   
 [比较运算符 \(Visual Basic\)](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators)   
 [类型转换函数](/dotnet/visual-basic/language-reference/functions/type-conversion-functions)