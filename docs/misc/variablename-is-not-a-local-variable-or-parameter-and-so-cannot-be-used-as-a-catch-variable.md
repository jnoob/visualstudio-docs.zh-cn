---
title: "“&lt;variablename&gt;”不是局部变量或参数，因此不能用作“Catch”变量 | Microsoft Docs"
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
  - "bc31082"
  - "vbc31082"
helpviewer_keywords: 
  - "BC31082"
ms.assetid: de197563-5848-4c1a-a519-cc4b5ea9a4c9
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# “&lt;variablename&gt;”不是局部变量或参数，因此不能用作“Catch”变量
`Try...Catch...Finally` 语句中的变量必须在本地声明，或者是当前过程的参数。  
  
 **错误 ID：**BC31082  
  
### 更正此错误  
  
1.  声明 `Try...Catch...Finally` 语句的本地变量或参数。  
  
## 请参阅  
 [Try...Catch...Finally 语句](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)