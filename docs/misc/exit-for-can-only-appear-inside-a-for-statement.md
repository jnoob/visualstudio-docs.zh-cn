---
title: "“Exit For”只能出现在“For”语句内 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30096"
  - "vbc30096"
helpviewer_keywords: 
  - "BC30096"
ms.assetid: 1062a329-9364-4234-9175-4c70a51cb7ae
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “Exit For”只能出现在“For”语句内
`Exit For` 语句出现在 `For` 循环外部。`Exit For` 仅在 `For` 语句或 `For Each` 语句和相应 `Next` 语句之间有效。  
  
 **错误 ID：**BC30096  
  
### 更正此错误  
  
1.  确保 `Exit For` 之前有一个有效的 `For` 或 `For Each` 语句，之后有一个有效的 `Next` 语句。  
  
2.  验证 `For` 循环内的其他控制结构是否被正确终止。  
  
## 请参阅  
 [For...Next 语句](/dotnet/visual-basic/language-reference/statements/for-next-statement)   
 [For Each...Next 语句](/dotnet/visual-basic/language-reference/statements/for-each-next-statement)