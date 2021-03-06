---
title: "ResolveComReference 任务 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/msbuild/2003#ResolveComReference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, ResolveCOMReference task
- ResolveCOMReference task [MSBuild]
ms.assetid: c9bf5fcf-6453-40ea-b50f-a212adc3e9b5
caps.latest.revision: "26"
author: kempb
ms.author: kempb
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: f00f7464d44423be4d37694c42ad3bfddaaea3e0
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="resolvecomreference-task"></a>ResolveComReference 任务
获取一个或多个类型库名称或 .tlb 文件的列表，将这些类型库解析为磁盘上的位置。  
  
## <a name="parameters"></a>参数  
 下表描述了 `ResolveCOMReference` 任务的参数。  
  
|参数|描述|  
|---------------|-----------------|  
|`DelaySign`|可选 `Boolean` 参数。<br /><br /> 如果为 `true`，任务会在程序集中放入公钥。 如果为 `false`，任务会对程序集进行完全签名。|  
|`EnvironmentVariables`|可选 `String[]` 参数。<br /><br /> 环境变量对的数组（使用等号分隔）。 这些变量会传递给生成的 tlbimp.exe 和 aximp.exe 以及常规环境块，或有选择地重写常规环境块。|  
|`ExecuteAsTool`|可选 `Boolean` 参数。<br /><br /> 如果为 `true`，请于进程外从适当的目标框架运行 tlbimp.exe 和 aximp.exe 来生成所需的包装器程序集。 此参数支持多目标。|  
|`IncludeVersionInInteropName`|可选 `Boolean` 参数。<br /><br /> 如果为 `true`，包装器名称中将包含 TypeLib 版本。 默认值为 `false`。|  
|`KeyContainer`|可选 `String` 参数。<br /><br /> 指定保存公钥/私钥对<br /><br /> 的容器。|  
|`KeyFile`|可选 `String` 参数。<br /><br /> 指定保存公钥/私钥对<br /><br /> 的项。|  
|`NoClassMembers`|可选 `Boolean` 参数。|  
|`ResolvedAssemblyReferences`|可选的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 输出参数。<br /><br /> 指定已解析的程序集引用。|  
|`ResolvedFiles`|可选的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 输出参数。<br /><br /> 指定磁盘上的完全限定文件，这些文件与作为此任务的输入提供的类型库的物理位置相对应。|  
|`ResolvedModules`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。|  
|`SdkToolsPath`|可选 <xref:System.String?displayProperty=fullName> 参数。<br /><br /> 如果 `ExecuteAsTool` 为 `true`，则必须将此参数设置为作为目标的框架版本的 SDK 工具路径。|  
|`StateFile`|可选 `String` 参数。<br /><br /> 指定 COM 组件时间戳的缓存文件。 如果不存在，则每次运行将重新生成所有包装器。|  
|`TargetFrameworkVersion`|可选 `String` 参数。<br /><br /> 指定项目目标框架版本。<br /><br /> 默认值为 `String.Empty`。 这意味着没有基于目标框架的引用的筛选。|  
|`TargetProcessorArchitecture`|可选 `String` 参数。<br /><br /> 指定首选的目标处理器体系结构。 转换后传递给 tlbimp.exe /machine 标志。<br /><br /> 参数值应属于 <xref:Microsoft.Build.Utilities.ProcessorArchitecture>。|  
|`TypeLibFiles`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定 COM 引用的类型库文件路径。 此参数中包含的项可能包含项元数据。 有关详细信息，请参阅下面的“TypeLibFiles 项元数据”部分。|  
|`TypeLibNames`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定要解析的类型库名称。 此参数中包含的项必须包含一些项元数据。 有关详细信息，请参阅下面的“TypeLibNames 项元数据”部分。|  
|`WrapperOutputDirectory`|可选 `String` 参数。<br /><br /> 生成的互操作程序集放置在磁盘上的位置。 如果未指定此项元数据，任务将使用项目文件所在目录的绝对路径。|  
  
## <a name="remarks"></a>备注  
  
## <a name="typelibnames-item-metadata"></a>TypeLibNames 项元数据  
 下表介绍了传递给 `TypeLibNames` 参数的项可用的项元数据。  
  
|元数据|描述|  
|--------------|-----------------|  
|`GUID`|所需的项元数据。<br /><br /> 类型库的 GUID。 如果未指定此项元数据，则任务失败。|  
|`VersionMajor`|所需的项元数据。<br /><br /> 类型库的主版本。 如果未指定此项元数据，则任务失败。|  
|`VersionMinor`|所需的项元数据。<br /><br /> 类型库的次版本。 如果未指定此项元数据，则任务失败。|  
|`LocaleIdentifier`|可选项元数据。<br /><br /> 类型库的区域设置标识符（或 LCID）。 被指定为 32 位值，可标识用户、区域或应用程序首选的人类语言。 如果未指定此项元数据，任务将使用默认区域设置标识符“0”。|  
|`WrapperTool`|可选项元数据。<br /><br /> 指定用于生成此类型库的程序集包装器的包装工具。 如果未指定此项元数据，任务将使用默认包装工具“tlbimp”。 可供类型库使用且区分大小写的选项有：<br /><br /> -   `Primary`：如果希望使用 COM 组件已经生成的主互操作程序集，请使用此包装工具。 使用此包装工具时，请勿指定包装器输出目录，否则任务会失败。<br />-   `TLBImp`：如果希望为 COM 组件生成互操作程序集，请使用此包装工具。<br />-   `AXImp`：如果希望为 ActiveX 控件生成互操作程序集，请使用此包装工具。|  
  
## <a name="typelibfiles-item-metadata"></a>TypeLibFiles 项元数据  
 下表介绍了传递给 `TypeLibFiles` 参数的项可用的项元数据。  
  
|元数据|描述|  
|--------------|-----------------|  
|`WrapperTool`|可选项元数据。<br /><br /> 指定用于生成此类型库的程序集包装器的包装工具。 如果未指定此项元数据，任务将使用默认包装工具“tlbimp”。 可供类型库使用且区分大小写的选项有：<br /><br /> -   `Primary`：如果希望使用 COM 组件已经生成的主互操作程序集，请使用此包装工具。 使用此包装工具时，请勿指定包装器输出目录，否则任务会失败。<br />-   `TLBImp`：如果希望为 COM 组件生成互操作程序集，请使用此包装工具。<br />-   `AXImp`：如果希望为 ActiveX 控件生成互操作程序集，请使用此包装工具。|  
  
> [!NOTE]
>  为类型库提供的唯一标识符信息越多，任务能解析磁盘上正确文件的可能性就越大。  
  
## <a name="remarks"></a>备注  
 除上面列出的参数外，此任务还从 <xref:Microsoft.Build.Utilities.Task> 类继承参数。 有关这些其他参数的列表及其说明，请参阅[任务基类](../msbuild/task-base-class.md)。  
  
## <a name="see-also"></a>请参阅  
 [任务](../msbuild/msbuild-tasks.md)   
 [任务参考](../msbuild/msbuild-task-reference.md)