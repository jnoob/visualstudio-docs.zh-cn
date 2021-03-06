---
title: "Option Strict On 要求所有函数、属性和运算符声明都有“As”子句 | Microsoft Docs"
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
  - "vbc30210"
  - "bc30210"
helpviewer_keywords: 
  - "BC30210"
ms.assetid: 4d217e56-0eac-4834-bcad-234a69809390
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Option Strict On 要求所有函数、属性和运算符声明都有“As”子句
声明中包含没有 `As` 子句的已声明属性或函数返回。 当 `Option Strict` 为 `On` 时，必须用 `As` 子句来声明每个变量、属性、过程参数和函数返回，以指定其数据类型；例如 `Dim MyNum As Short`。  
  
 **错误 ID：**BC30210  
  
### 更正此错误  
  
1.  检查 `As` 关键字是否拼写错误。  
  
2.  为声明的属性或函数返回提供 `As` 子句，或改为 `Option Strict Off`。  
  
## 请参阅  
 [Option Strict 语句](/dotnet/visual-basic/language-reference/statements/option-strict-statement)   
 [Property 过程](/dotnet/visual-basic/programming-guide/language-features/procedures/property-procedures)   
 [Function 过程](/dotnet/visual-basic/programming-guide/language-features/procedures/function-procedures)