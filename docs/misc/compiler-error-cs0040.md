---
title: "编译器错误 CS0040 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0040"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0040"
ms.assetid: 6a600166-0335-4b6d-b050-6821b4624c96
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS0040
创建调试信息文件时出现意外错误—“原因”  
  
 使用 [\/debug](/dotnet/csharp/language-reference/compiler-options/debug-compiler-option) 编译器选项时会出现此错误，表示编译器无法写 .pdb 文件。 针对此错误的可能解决方法包括重新安装 Visual Studio、确保编译器具有写入文件或目录的访问权限，或者不使用 \/debug 进行编译。