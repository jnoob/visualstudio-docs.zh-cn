---
title: "“&lt;typename&gt;”是泛型类型，需要类型参数 | Microsoft Docs"
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
  - "BC32076"
  - "vbc32076"
helpviewer_keywords: 
  - "BC32076"
ms.assetid: 57f63727-c544-4012-8f03-5d77fbdd1135
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;typename&gt;”是泛型类型，需要类型参数
变量、过程参数或函数返回声明具有泛型类类型或结构类型，但是此声明未提供任何类型参数。  
  
 按其性质，使用至少一个类型参数定义每个泛型类和结构。 当使用泛型类型来声明构造的类或结构时，必须为每个由泛型类型定义的类型形参提供一个类型实参。  
  
 **错误 ID：**BC32076  
  
### 更正此错误  
  
-   将类型列表添加到声明，用括号括起来并以 `Of` 关键字开头。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Of](/dotnet/visual-basic/language-reference/statements/of-clause)   
 [类型列表](/dotnet/visual-basic/language-reference/statements/type-list)