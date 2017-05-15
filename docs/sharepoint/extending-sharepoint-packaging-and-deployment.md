---
title: "Extending SharePoint Packaging and Deployment"
ms.custom: ""
ms.date: "02/02/2017"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "office-development"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
helpviewer_keywords: 
  - "SharePoint development in Visual Studio, extending deployment"
ms.assetid: 4789ebb2-12bc-42b9-9427-e63d77137765
caps.latest.revision: 19
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
caps.handback.revision: 18
---
# Extending SharePoint Packaging and Deployment
  可以扩展 SharePoint 项目的打包和部署过程。  
  
 [!INCLUDE[autoOutline](../Token/autoOutline_md.md)]  
  
##  <a name="creating_deployment_steps"></a> 创建部署步骤  
 部署 SharePoint 项目时，[!INCLUDE[vs_current_short](../sharepoint/includes/vs-current-short-md.md)] 会执行一系列部署步骤。  Visual Studio 包含用于很多任务的内置部署步骤，如收回和添加解决方案。  但是，还可以创建自己的部署步骤。  
  
 有关演示如何创建部署步骤的演练，请参阅[Walkthrough: Creating a Custom Deployment Step for SharePoint Projects](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md)。  
  
##  <a name="creating_deployment_configurations"></a> 创建部署配置  
 部署配置是一组针对给定项目执行，但可能会影响所有 SharePoint 项目项的部署步骤。  每个部署配置都包含一组在部署项目时执行的步骤，以及在收回项目时执行的另一组步骤。  [!INCLUDE[vs_current_short](../sharepoint/includes/vs-current-short-md.md)] 包含两个内置部署配置，不过你也可以创建自己的配置。  创建部署配置时，可以包含内置部署步骤和你创建的部署步骤。  
  
 有关演示如何创建部署配置的演练，请参阅[Walkthrough: Creating a Custom Deployment Step for SharePoint Projects](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md)。  
  
##  <a name="run_code_before_and_after_each_deployment_step"></a> 在部署或收回 SharePoint 解决方案时运行代码  
 可以处理事件以在部署或收回 SharePoint 解决方案时执行其他任务。  Visual Studio 会在以下情况下引发你可以处理的事件：  
  
-   为 SharePoint 项目项执行每个部署步骤之前和之后。  有关详细信息，请参阅[How to: Run Code When Deployment Steps are Executed](../sharepoint/how-to-run-code-when-deployment-steps-are-executed.md)。  
  
-   在部署或收回 SharePoint 项目之前和之后  有关详细信息，请参阅[How to: Run Code When a SharePoint Project is Deployed or Retracted](../sharepoint/how-to-run-code-when-a-sharepoint-project-is-deployed-or-retracted.md)。  
  
##  <a name="deployment_conflicts"></a> 处理部署冲突  
 某些类型的 SharePoint 项目项（包括模块、Web 部件、列表实例和内容类型）提供了内置部署冲突解决方法。  部署包含这些项目项之一的解决方案时，Visual Studio 会首先检查 SharePoint 站点上是否已存在与所部署项中的文件具有相同名称、URL 或 ID 的文件。  如果存在冲突，则 Visual Studio 可以自动解决冲突，或者它可以提示你以确定你是要让 Visual Studio 解决冲突还是取消部署。  有关详细信息，请参阅 [SharePoint 打包和部署疑难解答](../sharepoint/troubleshooting-sharepoint-packaging-and-deployment.md)。  
  
 可以通过提供自己的检查和解决部署冲突的代码，来扩展此功能。  有关详细信息，请参阅[How to: Handle Deployment Conflicts](../sharepoint/how-to-handle-deployment-conflicts.md)。  
  
##  <a name="run_command_line_operations_before_or_after_a_project_is_deployed"></a> 部署项目之前或之后运行命令行操作  
 如果要在部署 SharePoint 解决方案时运行命令行操作，则可以设置 <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> 对象的 <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject.PreDeploymentCommand%2A> 和 <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject.PostDeploymentCommand%2A> 属性。  Visual Studio 会在部署项目之前和之后执行这些命令。  
  
 在某些情况下，可能会发生部署冲突。  可通过多种不同的方式来解决冲突。  有关详细信息，请参阅 [SharePoint 打包和部署疑难解答](../sharepoint/troubleshooting-sharepoint-packaging-and-deployment.md)。  
  
##  <a name="customizing_validation_rules"></a> 自定义验证规则  
 部署解决方案包 \(.wsp\) 之前，可以创建自定义功能和包验证规则来验证功能或包是否有效。  例如，可以向开发人员报告信息、警告或错误以帮助他们解决验证问题。  有关详细信息，请参阅[How to: Create Custom Feature and Package Validation Rules for SharePoint Solutions](../sharepoint/how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions.md)。  
  
## 请参阅  
 [How to: Run Code When Deployment Steps are Executed](../sharepoint/how-to-run-code-when-deployment-steps-are-executed.md)   
 [Walkthrough: Creating a Custom Deployment Step for SharePoint Projects](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md)   
 [How to: Create Custom Feature and Package Validation Rules for SharePoint Solutions](../sharepoint/how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions.md)   
 [Extending the SharePoint Project System](../sharepoint/extending-the-sharepoint-project-system.md)  
  
  