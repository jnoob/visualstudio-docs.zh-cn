---
title: "类型参数已使用名称“&lt;类型参数名称&gt;”声明 | Microsoft Docs"
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
  - "vbc32049"
  - "bc32049"
helpviewer_keywords: 
  - "BC32049"
ms.assetid: d7affad0-0c3d-4fce-a1c2-a17f65514471
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 类型参数已使用名称“&lt;类型参数名称&gt;”声明
泛型类型的类型参数名称使用与同一泛型类型的另一个类型参数相同的名称声明。  
  
 在泛型类型的类型形参列表中，每个类型形参的名称必须与以下所有名称均不同：  
  
-   相同类型形参列表中的每个其他类型形参，  
  
-   在任何包含泛型类型的类型形参列表中的每个类型形参，以及  
  
-   泛型类型本身的名称。  
  
 **错误 ID：**BC32049  
  
### 更正此错误  
  
-   重命名类型形参，使其有别于此帮助页上的列表中引用的每个名称。  
  
## 请参阅  
 [Visual Basic 中的泛型类型](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [类型列表](/dotnet/visual-basic/language-reference/statements/type-list)