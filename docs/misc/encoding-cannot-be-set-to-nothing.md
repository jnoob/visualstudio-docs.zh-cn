---
title: "编码不能设置为 Nothing。 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 59f7c731-8291-4a85-bf51-c225e48cdc84
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 编码不能设置为 Nothing。
尝试读取或写入文件失败，因为已将参数 `encoding` 设置为 `Nothing`，但需要有效值。  
  
 <xref:System.Text.Encoding> 用于确定写入文件时使用何种编码。 默认为 UTF\-8。  
  
### 更正此错误  
  
-   为 `encoding` 参数提供有效值。  
  
## 请参阅  
 [文件编码](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/file-encodings)   
 [从文件读取](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/reading-from-files)   
 [写入文件](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/writing-to-files)   
 [My.Computer.FileSystem.ReadAllText 方法](http://msdn.microsoft.com/zh-cn/3a7ac8be-fb1d-4087-bc65-167d6754d57f)   
 [My.Computer.FileSystem.WriteAllText 方法](http://msdn.microsoft.com/zh-cn/f507460c-87d9-4504-b74f-3ff825c7d5c4)