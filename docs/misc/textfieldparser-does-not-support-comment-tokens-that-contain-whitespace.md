---
title: "TextFieldParser 不支持包含空格的注释标记 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbrTextFieldParser_WhitespaceInToken"
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# TextFieldParser 不支持包含空格的注释标记
提供了包含空格的注释标记。`TextFieldParser` 不支持包含空格的注释标记，除非空格出现在标记的开头。 出现在标记开头的空格将被忽略。  
  
### 更正此错误  
  
-   提供正确的注释标记。  
  
## 请参阅  
 [TextFieldParser.CommentTokens 属性](http://msdn.microsoft.com/zh-cn/2e6b6435-4bee-4c14-a353-e8f2c82e2d61)   
 [使用 TextFieldParser 对象分析文本文件](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object)   
 [TextFieldParser 对象](/dotnet/visual-basic/language-reference/objects/textfieldparser-object)