---
title: "ProjectCollection 元素 （Visual Studio 模板） |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/developer/vstemplate/2005#ProjectCollection
helpviewer_keywords:
- <ProjectCollection> element [Visual Studio Templates]
- ProjectCollection element [Visual Studio Templates]
ms.assetid: deb27180-2035-49ed-b835-c47bb3cd2f8f
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.workload: vssdk
ms.openlocfilehash: d97fd1e1d2c840279eec3b2769efc42f98894b92
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="projectcollection-element-visual-studio-templates"></a>ProjectCollection 元素（Visual Studio 模板）
指定多项目模板的组织和内容。  
  
 \<VSTemplate >  
 \<TemplateContent >  
 \<ProjectCollection >  
  
## <a name="syntax"></a>语法  
  
```  
<ProjectCollection>  
    <ProjectTemplateLink> ... </ProjectTemplateLink>  
    <SolutionFolder> ... </SolutionFolder>  
</ProjectCollection>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 以下各部分描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
 无。  
  
### <a name="child-elements"></a>子元素  
  
|元素|描述|  
|-------------|-----------------|  
|[ProjectTemplateLink](../extensibility/projecttemplatelink-element-visual-studio-templates.md)|可选元素。<br /><br /> 指定多项目模板中一个项目。|  
|[SolutionFolder](../extensibility/solutionfolder-element-visual-studio-templates.md)|可选元素。<br /><br /> 对多项目模板中的项目进行分组。|  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|必需的元素。<br /><br /> 指定模板的内容。|  
  
## <a name="remarks"></a>备注  
 多项目模板用作两个或多个项目的容器。 `ProjectCollection`元素用于指定要包含在此模板的项目。 有关多项目模板的详细信息，请参阅[如何： 创建多项目模板](../ide/how-to-create-multi-project-templates.md)。  
  
## <a name="example"></a>示例  
 此示例演示一个简单的多项目 .vstemplate 根文件。 在此示例中，模板包含两个项目：`My Windows Application` 和 `My Class Library`。 `ProjectName` 元素的 `ProjectTemplateLink` 特性可为 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 设置要分配给此项目的名称。 如果不存在 `ProjectName` 特性，则会使用 .vstemplate 文件的名称作为项目名称。  
  
```  
<VSTemplate Version="3.0.0" Type="ProjectGroup"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>Multi-Project Template Sample</Name>  
        <Description>An example of a multi-project template</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>VisualBasic</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectCollection>  
            <ProjectTemplateLink ProjectName="My Windows Application">  
                WindowsApp\MyTemplate.vstemplate  
            </ProjectTemplateLink>  
            <ProjectTemplateLink ProjectName="My Class Library">  
                ClassLib\MyTemplate.vstemplate  
            </ProjectTemplateLink>  
        </ProjectCollection>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>请参阅  
 [Visual Studio 模板架构参考](../extensibility/visual-studio-template-schema-reference.md)   
 [创建项目和项模板](../ide/creating-project-and-item-templates.md)   
 [如何：创建多项目模板](../ide/how-to-create-multi-project-templates.md)