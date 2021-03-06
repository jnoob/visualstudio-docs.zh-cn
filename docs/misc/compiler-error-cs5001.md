---
title: "编译器错误 CS5001 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS5001"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS5001"
ms.assetid: e1e26e75-84e0-47c7-be8a-3c4fd0d6f497
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 编译器错误 CS5001
程序“program”不包含适合于入口点的静态“Main”方法  
  
 当生成可执行文件的代码内未找到具有正确签名的静态 [Main](/dotnet/csharp/programming-guide/main-and-command-args/main-and-command-line-arguments) 方法时，将出现此错误。 如果用错误的大小写（例如小写的 `main`）定义了入口点函数 `Main`，则也将出现此错误。  
  
-   `Main` 必须声明为静态且返回 [void](/dotnet/csharp/language-reference/keywords/void) 或 [int](/dotnet/csharp/language-reference/keywords/int)，并且它必须无参数或具有一个 `string[]` 类型的参数。  
  
## 示例  
 下面的示例生成 CS5001：  
  
```  
// CS5001.cs // CS5001 expected public class a { // Uncomment the following line to resolve. // static void Main() {} }  
```  
  
## 请参阅  
 [Main\(\) 和命令行参数](/dotnet/csharp/programming-guide/main-and-command-args/main-and-command-line-arguments)