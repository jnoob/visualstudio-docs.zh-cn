---
title: "“#If” 块必须以匹配的 “#End If” 结束 | Microsoft Docs"
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
  - "vbc30012"
  - "bc30012"
helpviewer_keywords: 
  - "BC30012"
ms.assetid: 9d51f3be-d2c3-4918-a36d-0d9e9763e47b
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “#If” 块必须以匹配的 “#End If” 结束
`#If` 是条件编译指令。`#End If` 指令未终止 `#If` 块。  
  
 **错误 ID：**BC30012  
  
### 更正此错误  
  
-   添加 `#End If` 指令至条件编译块的末尾。  
  
## 请参阅  
 [\#If...Then...\#Else 指令](/dotnet/visual-basic/language-reference/directives/if-then-else-directives)