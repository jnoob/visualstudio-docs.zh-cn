---
title: "项目“&lt;projectname&gt;”要求对程序集“&lt;assemblyname&gt;”的版本“&lt;versionnumber1&gt;”的引用，但却引用了程序集“&lt;assemblyname&gt;”（Visual Basic 错误）的版本“&lt;versionnumber2&gt;” | Microsoft Docs"
ms.custom: ""
ms.date: "12/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc32209"
  - "bc32209"
helpviewer_keywords: 
  - "BC32209"
ms.assetid: fe50736b-444f-4e40-8f80-9760ff13a153
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 项目“&lt;projectname&gt;”要求对程序集“&lt;assemblyname&gt;”的版本“&lt;versionnumber1&gt;”的引用，但却引用了程序集“&lt;assemblyname&gt;”（Visual Basic 错误）的版本“&lt;versionnumber2&gt;”
项目间接引用了在其他位置定义的程序集，但该项目还直接引用了该程序集的早期版本。  
  
 如果编译器允许代码使用间接引用，则可能无法访问在较新版本中而不是在较早版本中定义的类型和编程元素。  
  
 **错误 ID：**BC32209  
  
### 更正此错误  
  
-   删除对该程序集的较早版本的间接引用，并使用较新版本的直接引用。  
  
## 请参阅  
 [公共语言运行时中的程序集](../Topic/Assemblies%20in%20the%20Common%20Language%20Runtime.md)   
 [NIB：引用命名空间和组件](http://msdn.microsoft.com/zh-cn/568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [管理项目中的引用](../ide/managing-references-in-a-project.md)   
 [NIB：管理引用](http://msdn.microsoft.com/zh-cn/910912ce-0dc9-4569-9274-32c44a20cb2c)   
 [NIB 如何：使用“添加引用”对话框添加或删除引用](http://msdn.microsoft.com/zh-cn/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)