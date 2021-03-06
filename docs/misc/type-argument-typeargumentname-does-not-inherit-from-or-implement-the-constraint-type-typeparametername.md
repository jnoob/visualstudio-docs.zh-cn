---
title: "类型参数“&lt;typeargumentname&gt;”不继承自或实现约束类型“&lt;typeparametername&gt;”。 | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc32044"
  - "vbc32044"
helpviewer_keywords: 
  - "BC32044"
ms.assetid: be91f648-c07d-4991-8ed1-28b1327619c4
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 类型参数“&lt;typeargumentname&gt;”不继承自或实现约束类型“&lt;typeparametername&gt;”。
提供给泛型类型的类型实参不满足其对应类型形参上的继承或实现约束。  
  
 约束列表对传递给类型形参的类型实参有一定要求。 可能的要求如下：  
  
-   该类型实参必须实现一个或多个接口  
  
-   该类型实参最多从一个类继承  
  
 你可以为单个类型参数将上述要求进行组合。[!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 无法构造类型，除非代码提供了满足每个泛型类型上定义的类型形参的约束的类型实参。  
  
 **错误 ID：**BC32044  
  
### 更正此错误  
  
-   选择一个类型的类型实参，该类型实现为该类型形参指定的每个接口的类型，且继承自指定的类（如果存在）。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [如何：使用泛型类](../Topic/How%20to:%20Use%20a%20Generic%20Class%20\(Visual%20Basic\).md)