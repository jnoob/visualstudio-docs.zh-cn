---
title: "编译器错误 CS1679 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1679"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1679"
ms.assetid: c42e9bca-212a-458e-88f8-b81c812436bb
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS1679
无效的“\/reference”外部别名；“identifier”不是有效的标识符  
  
 使用 **\/reference** 选项的外部程序集别名功能时，根据 C\# 语言规范，位于 **\/reference:** 之后、“\=”之前的文本必须为有效的 C\# 标识符或关键字。  
  
 若要更正此错误，将“\=”之前的文本更改为有效的 C\# 标识符或关键字。  
  
## 示例  
 以下示例生成 CS1679。  
  
```  
// CS1679.cs // compile with: /reference:123$BadIdentifier%=System.dll class TestClass { static void Main() { } }  
```