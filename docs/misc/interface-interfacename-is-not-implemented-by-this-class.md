---
title: "此类未实现接口“&lt;interfacename&gt;” | Microsoft Docs"
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
  - "bc31035"
  - "vbc31035"
helpviewer_keywords: 
  - "BC31035"
ms.assetid: 99ddabb5-20e0-4cf6-a8d4-1ca91f3c7511
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 此类未实现接口“&lt;interfacename&gt;”
此类或结构的成员尝试实现类或结构未实现的接口的成员。  
  
 **错误 ID：**BC31035  
  
### 更正此错误  
  
-   在类或结构的开头添加 `Implements` 语句，使它实现相应的接口。  
  
-   从导致此错误的成员中删除 `Implements` 关键字。  
  
## 请参阅  
 [接口](/dotnet/visual-basic/programming-guide/language-features/interfaces/index)   
 [Implements](/dotnet/visual-basic/language-reference/statements/implements-clause)   
 [Implements 语句](/dotnet/visual-basic/language-reference/statements/implements-statement)