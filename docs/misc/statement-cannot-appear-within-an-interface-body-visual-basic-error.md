---
title: "语句不能出现在接口体内(Visual Basic 错误) | Microsoft Docs"
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
  - "bc30604"
  - "vbc30604"
helpviewer_keywords: 
  - "BC30604"
ms.assetid: ce4759fe-5e49-43ad-8405-a3f46ed0a36f
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 语句不能出现在接口体内(Visual Basic 错误)
遇到意外的语言构造。 假定缺少 `End Interface` 构造，而且此点后的所有源代码都在接口外。  
  
 **错误 ID：**BC30604  
  
### 更正此错误  
  
1.  验证接口定义中所用代码的语法是否正确。  
  
2.  确保接口定义以 `End Interface` 构造结束。  
  
## 请参阅  
 [接口](/dotnet/visual-basic/programming-guide/language-features/interfaces/index)   
 [Interface 语句](/dotnet/visual-basic/language-reference/statements/interface-statement)