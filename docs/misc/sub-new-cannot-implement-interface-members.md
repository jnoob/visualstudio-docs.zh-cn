---
title: "“Sub New”无法实现接口成员 | Microsoft Docs"
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
  - "bc31042"
  - "vbc31042"
helpviewer_keywords: 
  - "BC31042"
ms.assetid: 43ad231f-878d-4d08-b43c-06bf167ddd7d
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Sub New”无法实现接口成员
`Sub New` 是构造函数，它不能实现成员。  
  
 **错误 ID：**BC31042  
  
### 更正此错误  
  
-   从 `Sub New` 过程删除 `Implements` 语句。  
  
## 请参阅  
 [接口](/dotnet/visual-basic/programming-guide/language-features/interfaces/index)   
 [Implements](/dotnet/visual-basic/language-reference/statements/implements-clause)