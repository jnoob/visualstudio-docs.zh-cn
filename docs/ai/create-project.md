---
title: "在 AI Tools for Visual Studio 中创建项目"
description: "使用来自 Azure 机器学习库的示例创建项目"
keywords: "ai, visual studio, azure 机器学习"
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: how to article
ms.technology: visual studio
ms.devlang: multiple
ms.service: multiple
ms.openlocfilehash: 2d8b5f1d06d31eaba9c75e0f0515b2526fc7efdf
ms.sourcegitcommit: fb751e41929f031d1a9247bc7c8727312539ad35
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2017
---
## <a name="create-an-ai-project-from-the-azure-machine-learning-gallery-in-visual-studio"></a>在 Visual Studio 中通过 Azure 机器学习库创建 AI 项目

Azure 机器学习与 Visual Studio Tools for AI 集成在一起。 可以使用它将机器学习将作业提交到远程计算目标，如 Azure 虚拟机、Spark 群集等。 详细了解 [Azure 机器学习试验](https://docs.microsoft.com/azure/machine-learning/preview/experimentation-service-configuration) 

[安装 Visual Studio Tools for AI](installation.md) 之后，可以使用 Azure 机器学习示例库中的预制方案轻松地创建新 Python 项目。

> ! 必须安装 Azure 机器学习工作台。 若要安装它，请参阅 [Azure 机器学习安装快速入门](https://docs.microsoft.com/azure/machine-learning/preview/quickstart-installation) 

1. 启动 Visual Studio。 通过打开“AI 工具”菜单，然后选择“选择群集”，来打开“服务器资源管理器”  

    ![群集选择器](media\create-project\select-cluster.png)

1. 通过在服务器资源管理器中右键单击“Azure 机器学习”节点，然后选择“登录”并按照说明进行操作，来登录你的 Azure 机器学习订阅。

    ![登录](media\create-project\azureml-login.png)
 
2. 选择“AI 工具”>“Azure 机器学习示例库”。 
    
    ![示例库](media\create-project\gallery.png)

1. 对于本快速入门，选择“使用 TensorFlow 的 MNIST”示例，然后单击“安装”。 提供 
2.
 - **资源组**：用于存储元数据的 Azure 资源组
 - **帐户**：Azure 机器学习试验帐户
 - **工作区**：Azure 机器学习工作区
 - **项目类型**：机器学习框架。 在此例中选择“TensorFlow”
 - **添加到解决方案**：确定是添加到当前 Visual Studio 解决方案还是创建并打开新解决方案
 - **项目路径**：用于保存代码的位置
 - **项目名称**：输入 **TensorFlowMNIST**
   

    ![使用“Python 应用程序”模板时生成的项目](media\create-project\new-AzureSampleProject.png)

1. Visual Studio 随即创建项目文件（磁盘上的 `.pyproj` 文件）以及示例中定义的其他文件。 对于“MNIST”模板，项目包含多个文件。

    ![mnist](media\create-project\azml-mnist.png)

1. 将作业提交到 Azure 机器学习。 

    ![mnist](media\create-project\submit-azml.png)

1. 在 Docker 容器中或本地计算机上运行

    ![mnist](media\create-project\azml-local.png)