---
title: "构造间接引用包含“&lt;typename&gt;”的项目“&lt;projectname&gt;” | Microsoft Docs"
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
  - "vbc31533"
  - "bc31533"
helpviewer_keywords: 
  - "BC31533"
ms.assetid: e3f55f9f-92be-4ecb-bc8f-9e57049a0805
caps.latest.revision: 6
caps.handback.revision: 6
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 构造间接引用包含“&lt;typename&gt;”的项目“&lt;projectname&gt;”
构造间接引用包含“\<typename\>”的项目“\<projectname\>”。 将指向“\<projectname\>”的项目引用添加到项目。  
  
 表达式或语句可访问另一项目中定义的类型，但你的项目不具有对该定义项目的直接引用。  
  
 类型可能是类、结构、接口、模块或枚举。  
  
 定义引用类型的项目生成包含该类型的程序集。 如果你的项目不直接引用该定义项目，编译器无法保证包含该类型的程序集是在解决方案中且可供访问。  
  
 **错误 ID：**BC31533  
  
### 更正此错误  
  
-   确定可定义引用类型的项目，并向其添加项目引用。  
  
## 请参阅  
 [NIB：引用命名空间和组件](http://msdn.microsoft.com/zh-cn/568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [管理项目中的引用](../ide/managing-references-in-a-project.md)   
 [NIB：管理引用](http://msdn.microsoft.com/zh-cn/910912ce-0dc9-4569-9274-32c44a20cb2c)   
 [NIB 如何：使用“添加引用”对话框添加或删除引用](http://msdn.microsoft.com/zh-cn/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)