---
title: "不再支持“Get”语句 (Visual Basic) | Microsoft Docs"
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
  - "vbc30767"
  - "bc30767"
helpviewer_keywords: 
  - "BC30767"
ms.assetid: 6aa62dcc-99aa-4051-a81e-3bbb6a8c355f
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 不再支持“Get”语句 (Visual Basic)
不再支持 `Get` 语句。 文件 I\/O 功能在 `Microsoft.VisualBasic` 命名空间中通常是可用的，但目标版本的 .NET Compact Framewor 不支持它。  
  
 **错误 ID：**BC30767  
  
### 更正此错误  
  
-   利用 <xref:System.IO> 命名空间中定义的函数执行文件操作。  
  
## 请参阅  
 <xref:System.IO>   
 [Get 语句](/dotnet/visual-basic/language-reference/statements/get-statement)   
 [使用 Visual Basic 访问文件](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/file-access)