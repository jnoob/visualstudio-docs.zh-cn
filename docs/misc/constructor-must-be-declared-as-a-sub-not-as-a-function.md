---
title: "构造函数必须声明为 Sub，而不能声明为 Function。 | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30493"
  - "vbc30493"
helpviewer_keywords: 
  - "BC30493"
ms.assetid: bcacfd4b-cac0-4ad3-a6df-5fb37c189e8f
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 构造函数必须声明为 Sub，而不能声明为 Function。
你已尝试声明 `Function New`。 构造函数必须声明为 `Sub New`。  
  
 **错误 ID：**BC30493  
  
### 更正此错误  
  
-   使用 `Sub` 而非 `Function`。  
  
## 请参阅  
 [Sub 语句](/dotnet/visual-basic/language-reference/statements/sub-statement)