---
title: "MSBuild 12.0 中的新增功能 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 9976a6ad-c052-4017-b848-35b5ae4a2f66
caps.latest.revision: 23
author: kempb
ms.author: kempb
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Human Translation
ms.sourcegitcommit: 3ba7680d46345f2b49019659c715cfb418933d39
ms.openlocfilehash: d299c4959ddf23a8c249f5577ee03fda99e636f7

---
# <a name="what39s-new-in-msbuild-120"></a>MSBuild 12.0 中的新增功能
MSBuild 现已作为 Visual Studio 的一部分而不是 .NET Framework 的一部分进行安装。 当前 MSBuild 版本号为 12.0。 如果要单独安装 MSBuild，请从 [MSBuild 下载](http://go.microsoft.com/fwlink/?LinkId=309745)下载安装包。  
  
## <a name="changed-path"></a>更改的路径  
 MSBuild 现直接安装在 *%ProgramFiles%* 下，例如安装在 C:\Program Files\MSBuild\\ 中。  
  
## <a name="changed-properties"></a>更改的属性  
 下面的 MSBuild 属性由于新版本号而更改：  
  
-   此版工具的 `MSBuildToolsVersion` 为 12.0。  
  
-   `MSBuildToolsPath` 现在为 %ProgramFiles%\MSBuild\12.0\bin（对于 32 位操作系统）或 %ProgramFiles%\MSBuild\12.0\bin\amd64（对于 64 位操作系统）。  
  
-   `ToolsVersion` 值可以在 HKLM\SOFTWARE\Microsoft\MSBuild\ToolsVersions\12.0（对于 32 位操作系统）或 HKLM\SOFTWARE\Wow6432Node\Microsoft\MSBuild\ToolsVersions\12.0（64 位操作系统）中找到。  
  
-   `SDK35ToolsPath` 和 `SDK40ToolsPath` 属性指向与此版 Visual Studio 一起打包的 .NET Framework SDK（例如，对于 4.X 工具，则指向 8.1A）。  
  
## <a name="new-properties"></a>新增的属性  
  
-   `MSBuildFrameworkToolsPath` 是一个新属性，其值为 %windir%\Microsoft.NET\Framework\v4.0.30319（对于 32 位操作系统）或 %windir%\Microsoft.NET\Framework64\v4.0.30319（对于 64 位操作系统）。 它替代了 `MSBuildToolsPath`，可用于指向 .NET Framework 工具和实用程序。  
  
-   `MSBuildToolsPath` 和 `MSBuildFrameworkToolsPath` 具有 32 位等效项 `MSBuildToolsPath32` 和 `MSBuildFrameworkToolsPath32`，它们始终指向 32 位位置，而不论使用 32 位还是 64 位的 MSBuild。

## <a name="see-also"></a>另请参阅
[MSBuild](../msbuild/msbuild.md)


<!--HONumber=Feb17_HO4-->


