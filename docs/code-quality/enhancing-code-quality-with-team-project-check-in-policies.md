---
title: "利用团队项目签入策略提高代码质量 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- code quality, using check-in policies
- team-based development, enhancing code quality
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 36e0ab96c1c0c3deeced62ff9808737c903e682b
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="enhancing-code-quality-with-team-project-check-in-policies"></a>利用团队项目签入策略提高代码质量

使用 Team Foundation 版本控制 (TFVC) 时，可以为团队项目创建签入策略。 若要强制实施可获得更好代码和提升组开发效率的实践。 签入策略是在团队项目级别设置的，并在允许代码签入之前在开发人员计算机上强制实施的规则。

你可以指定这些团队项目签入策略：

- **生成**：要求必须在新签入之前修复在生成过程中创建的生成中断。

- **变更集注释**：要求用户在签入更改时提供注释。

- **代码分析**：要求在执行签入之前先运行代码分析。

- **工作项**：需要将一个或多个工作项与签入关联。

> [!IMPORTANT]
> 若要使用签入策略，你必须连接到 [!INCLUDE[vststfsLong](../code-quality/includes/vststfslong_md.md)]。

## <a name="common-tasks"></a>常规任务

|任务|支持内容|
|----------|------------------------|
|**创建和使用代码分析签入策略：** 可以从一组标准的代码分析规则中选择，或者也可以创建一组自定义规则。|[创建和使用代码分析签入策略](../code-quality/creating-and-using-code-analysis-check-in-policies.md)|

## <a name="related-tasks"></a>相关任务

|任务|支持内容|
|----------|------------------------|
|**在开发过程中使用代码分析：** 团队成员在其开发计算机上运行代码分析。 在 Visual Studio 中，开发人员配置并运行各个代码项目的代码分析运行，查看和分析各个运行所发现的问题，并创建警告工作项。|[分析应用程序质量](../code-quality/analyzing-application-quality-by-using-code-analysis-tools.md)|
|**创建和运行单元测试：** 单元测试为开发人员和测试人员提供了一种快捷的方式来查找 C#、Visual Basic .NET 和 C++ 项目中类的方法的逻辑错误。 可以创建一次单元测试，并在每次源代码更改时运行单元测试以确保没有引入任何 bug。|[单元测试代码](../test/unit-test-your-code.md)|
|**跟踪工作项和缺陷：** 可以使用工作项来跟踪和管理有关你的团队项目的工作和信息。 工作项是一个 [!INCLUDE[esprfound](../code-quality/includes/esprfound_md.md)] 用于跟踪工作分配和进度的数据库记录。 你可以使用不同类型的工作项来跟踪不同类型的工作，例如，客户要求、产品 Bug 和开发任务。|[工作项 (VSTS)](/vsts/work/work-items/index)|

## <a name="external-resources"></a>外部资源

[使用 Visual Studio 2012 测试连续交付 - 第 2 章：单元测试：测试内部](http://go.microsoft.com/fwlink/?LinkID=255188)