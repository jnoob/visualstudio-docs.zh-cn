---
title: "从“Finally”中分支无效 | Microsoft Docs"
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
  - "bc30101"
  - "vbc30101"
helpviewer_keywords: 
  - "BC30101"
ms.assetid: 16a0dc29-3657-4373-b77f-38f3cb80e6c9
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 从“Finally”中分支无效
`Finally` 块中的 `GoTo` 语句在块外分支。 分支到 `Catch` 或 `Finally` 块或从两个块进行分支是无效的。  
  
 **错误 ID：**BC30101  
  
### 更正此错误  
  
-   删除 `GoTo` 语句，并考虑实现具有决策或循环控制结构的程序逻辑。  
  
## 请参阅  
 [Try...Catch...Finally 语句](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)   
 [GoTo 语句](/dotnet/visual-basic/language-reference/statements/goto-statement)   
 [控制流](/dotnet/visual-basic/programming-guide/language-features/control-flow/index)