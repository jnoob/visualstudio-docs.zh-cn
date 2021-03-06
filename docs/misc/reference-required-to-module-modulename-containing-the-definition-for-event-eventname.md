---
title: "需要对模块“&lt;modulename&gt;”（包含事件“&lt;eventname&gt;”的定义）的引用 | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30006"
  - "bc30006"
helpviewer_keywords: 
  - "BC30006"
ms.assetid: 7ab80acd-b47b-4920-bb15-6a3206b984e4
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 需要对模块“&lt;modulename&gt;”（包含事件“&lt;eventname&gt;”的定义）的引用
需要对模块“\<`modulename`\>”（包含事件“\<`eventname`\>”的定义）的引用。 请向项目中添加一个。  
  
 事件在项目不直接引用的模块中定义。 如果事件在多个模块中定义，则 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 编译器需要一个引用以避免多义性。  
  
 **错误 ID：**BC30006  
  
### 更正此错误  
  
-   将未引用模块的名称包括在项目引用中。  
  
## 请参阅  
 [NIB：引用命名空间和组件](http://msdn.microsoft.com/zh-cn/568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [有关无效的引用的疑难解答](../ide/troubleshooting-broken-references.md)