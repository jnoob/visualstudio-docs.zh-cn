---
title: "编译器警告（等级 1）CS3013 | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS3013"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS3013"
ms.assetid: 00b3bbe1-f2a0-465c-be0e-1af700c5753d
caps.latest.revision: 9
caps.handback.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器警告（等级 1）CS3013
添加的模块必须用 CLSCompliant 特性标记才能与程序集匹配  
  
 已将使用 [\/target: module](../Topic/-target:module%20\(C%23%20Compiler%20Options\).md) 编译器选项编译的模块添加到使用 [\/addmodule](/dotnet/csharp/language-reference/compiler-options/addmodule-compiler-option) 的编译中。 但是，该模块对公共语言规范 \(CLS\) 的遵从性与当前编译的 CLS 状态不一致。  
  
 CLS 遵从性由模块特性表示。 例如，`[module:CLSCompliant(true)]` 表示模块符合 CLS，`[module:CLSCompliant(false)]` 表示模块不符合 CLS。 默认值为 `[module:CLSCompliant(false)]`。 有关 CLS 的详细信息，请参见 [语言独立性和与语言无关的组件](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md)。