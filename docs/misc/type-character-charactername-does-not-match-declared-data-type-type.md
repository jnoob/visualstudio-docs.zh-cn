---
title: "类型字符“&lt;charactername&gt;”与声明的数据类型“&lt;type&gt;”不匹配 | Microsoft Docs"
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
  - "vbc30277"
  - "bc30277"
helpviewer_keywords: 
  - "BC30277"
ms.assetid: 9808f57e-a46c-43f9-b5e7-275794627763
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 类型字符“&lt;charactername&gt;”与声明的数据类型“&lt;type&gt;”不匹配
变量使用一种数据类型进行了声明，但是使用表示不兼容数据类型的类型字符进行了引用（例如 `K` 声明为 `Integer` 时的 `K$ = 10`）。  
  
 **错误 ID：**BC30277  
  
### 更正此错误  
  
-   更改变量的已声明数据类型，或更改或删除引用中的类型字符。  
  
## 请参阅  
 [类型字符](/dotnet/visual-basic/programming-guide/language-features/data-types/type-characters)