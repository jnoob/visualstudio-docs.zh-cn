---
title: "演练：VSTO 外接程序项目中的复杂数据绑定"
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
  - "数据绑定 [Visual Studio 中的 Office 开发]，Excel"
  - "数据 [Visual Studio 中的 Office 开发]，绑定数据"
  - "复杂数据 [Visual Studio 中的 Office 开发]"
ms.assetid: ff52fb56-1f67-4ae2-a3d1-93038619d4e6
caps.latest.revision: 38
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
caps.handback.revision: 37
---
# 演练：VSTO 外接程序项目中的复杂数据绑定
  可以将数据绑定到 VSTO 外接程序项目中的宿主控件和 Windows 窗体控件。 本演练演示如何在运行时向 Microsoft Office Excel 工作表中添加控件并将控件绑定到数据。  
  
 [!INCLUDE[appliesto_xlallapp](../vsto/includes/appliesto-xlallapp-md.md)]  
  
 本演练阐释了以下任务：  
  
-   在运行时将 <xref:Microsoft.Office.Tools.Excel.ListObject> 控件添加到工作表。  
  
-   创建用于将该控件连接到某个数据集实例的 <xref:System.Windows.Forms.BindingSource>。  
  
 [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]  
  
## 系统必备  
 你需要以下组件来完成本演练：  
  
-   [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]  
  
-   [!INCLUDE[Excel_15_short](../vsto/includes/excel-15-short-md.md)] 或 [!INCLUDE[Excel_14_short](../vsto/includes/excel-14-short-md.md)]。  
  
-   对附加了 `AdventureWorksLT` 示例数据库且正在运行的 SQL Server 2005 或 SQL Server 2005 Express 实例的访问权限。 你可以从 [CodePlex 网站](http://go.microsoft.com/fwlink/?LinkId=115611)下载 `AdventureWorksLT` 数据库。 有关附加数据库的详细信息，请参阅下列主题：  
  
    -   若要使用 SQL Server Management Studio 或 SQL Server Management Studio Express 来附加数据库，请参阅[如何：附加数据库 \(SQL Server Management Studio\)](http://msdn.microsoft.com/zh-cn/b4efb0ae-cfe6-4d81-a4b4-6e4916885caa)。  
  
    -   若要使用命令行来附加数据库，请参阅[如何：将数据库文件附加到 SQL Server Express](http://msdn.microsoft.com/zh-cn/0f8e42b5-7a8c-4c30-8c98-7d2bdc8dcc68)。  
  
## 创建新项目  
 第一步是创建 Excel VSTO 外接程序项目。  
  
#### 创建新项目  
  
1.  使用 Visual Basic 或 C\# 创建一个名为“从数据库填充工作表”的 Excel VSTO 外接程序项目。  
  
     有关详细信息，请参阅[如何：在 Visual Studio 中创建 Office 项目](../vsto/how-to-create-office-projects-in-visual-studio.md)。  
  
     Visual Studio 会打开 `ThisAddIn.vb` 或 `ThisAddIn.cs` 文件，并将“从数据库填充工作表”项目附加到“解决方案资源管理器”中。  
  
## 创建数据源  
 使用**“数据源”**窗口将类型化数据集添加到项目中。  
  
#### 向项目中添加类型化数据集  
  
1.  如果**“数据源”**窗口不可见，则在菜单栏上，通过选择**“查看”**，**“其他窗口”**、**“数据源”**显示它。  
  
2.  选择**“添加新数据源”**以启动**“数据源配置向导”**。  
  
3.  单击“数据库”，然后单击“下一步”。  
  
4.  如果已与 `AdventureWorksLT` 数据库建立连接，请选择此连接，然后单击“下一步”。  
  
     否则，单击“新建连接”，然后使用“添加连接”对话框创建新连接。 有关详细信息，请参阅[如何：连接到数据库中的数据](~/data-tools/how-to-connect-to-data-in-a-database.md)。  
  
5.  在“将连接字符串保存到应用程序配置文件中”页中，单击“下一步”。  
  
6.  在“选择数据库对象”页中展开“表”，再选择“Address \(SalesLT\)”。  
  
7.  单击**“完成”**。  
  
     AdventureWorksLTDataSet.xsd 文件即会添加到“解决方案资源管理器”中。 此文件定义以下各项：  
  
    -   一个名为 `AdventureWorksLTDataSet` 的类型化数据集。 此数据集表示 AdventureWorksLT 数据库中“Address \(SalesLT\)”表的内容。  
  
    -   一个名为 TableAdapter 的 `AddressTableAdapter`。 此 TableAdapter 可用来在 `AdventureWorksLTDataSet` 中读取和写入数据。 有关详细信息，请参阅[TableAdapter 概述](/visual-studio/data-tools/tableadapter-overview)。  
  
     在本演练后面的部分中，你将使用这两个对象。  
  
## 创建控件并将控件绑定到数据  
 对于本演练，只要用户打开工作薄，<xref:Microsoft.Office.Tools.Excel.ListObject> 控件就会在所选表中显示所有数据。 列表对象使用 <xref:System.Windows.Forms.BindingSource> 将控件连接到数据库。  
  
 有关将控件绑定到数据的详细信息，请参阅 [将数据绑定到 Office 解决方案中的控件](../vsto/binding-data-to-controls-in-office-solutions.md)。  
  
#### 添加列表对象、数据集和表适配器  
  
1.  在 `ThisAddIn` 类中，声明以下控件以显示 `AdventureWorksLTDataSet` 数据集的 `Address` 表。  
  
     [!code-csharp[Trin_ExcelAddInDatabase#1](../snippets/csharp/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/CS/ThisAddIn.cs#1)]
     [!code-vb[Trin_ExcelAddInDatabase#1](../snippets/visualbasic/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/VB/ThisAddIn.vb#1)]  
  
2.  在 `ThisAddIn_Startup` 方法中，添加以下代码以初始化数据集，并使用 `AdventureWorksLTDataSet` 数据集的信息来填充此数据集。  
  
     [!code-csharp[Trin_ExcelAddInDatabase#2](../snippets/csharp/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/CS/ThisAddIn.cs#2)]
     [!code-vb[Trin_ExcelAddInDatabase#2](../snippets/visualbasic/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/VB/ThisAddIn.vb#2)]  
  
3.  将以下代码添加到 `ThisAddIn_Startup` 方法中。 这会生成一个可扩展工作表的宿主项。 有关详细信息，请参阅[在运行时在 VSTO 外接程序中扩展 Word 文档和 Excel 工作簿](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)。  
  
     [!code-csharp[Trin_ExcelAddInDatabase#3](../snippets/csharp/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/CS/ThisAddIn.cs#3)]
     [!code-vb[Trin_ExcelAddInDatabase#3](../snippets/visualbasic/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/VB/ThisAddIn.vb#3)]  
  
4.  创建一个范围并添加 <xref:Microsoft.Office.Tools.Excel.ListObject> 控件。  
  
     [!code-csharp[Trin_ExcelAddInDatabase#4](../snippets/csharp/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/CS/ThisAddIn.cs#4)]
     [!code-vb[Trin_ExcelAddInDatabase#4](../snippets/visualbasic/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/VB/ThisAddIn.vb#4)]  
  
5.  使用 <xref:System.Windows.Forms.BindingSource> 将列表对象绑定到 `AdventureWorksLTDataSet`。 传入你想要绑定到列表对象的列的名称。  
  
     [!code-csharp[Trin_ExcelAddInDatabase#5](../snippets/csharp/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/CS/ThisAddIn.cs#5)]
     [!code-vb[Trin_ExcelAddInDatabase#5](../snippets/visualbasic/VS_Snippets_OfficeSP/Trin_ExcelAddInDatabase/VB/ThisAddIn.vb#5)]  
  
## 测试外接程序  
 打开 Excel 时，<xref:Microsoft.Office.Tools.Excel.ListObject> 会显示来自 `AdventureWorksLTDataSet` 数据集的 `Address` 表的数据。  
  
#### 若要测试 VSTO 外接程序  
  
-   按 F5。  
  
     已在工作表中创建了一个名为 `addressListObject` 的 <xref:Microsoft.Office.Tools.Excel.ListObject> 控件。 同时，向项目添加了一个名为 `adventureWorksLTDataSet` 的数据集对象和一个名为 `addressBindingSource` 的 <xref:System.Windows.Forms.BindingSource>。 已将 <xref:Microsoft.Office.Tools.Excel.ListObject> 绑定到 <xref:System.Windows.Forms.BindingSource>，而后者又绑定到该数据集对象。  
  
## 请参阅  
 [Office 解决方案中的数据](../vsto/data-in-office-solutions.md)   
 [将数据绑定到 Office 解决方案中的控件](../vsto/binding-data-to-controls-in-office-solutions.md)   
 [如何：用数据库中的数据填充工作表](../vsto/how-to-populate-worksheets-with-data-from-a-database.md)   
 [如何：用数据库中的数据填充文档](../vsto/how-to-populate-documents-with-data-from-a-database.md)   
 [如何：用服务中的数据填充文档](../vsto/how-to-populate-documents-with-data-from-services.md)   
 [如何：用对象中的数据填充文档](../vsto/how-to-populate-documents-with-data-from-objects.md)   
 [如何：在工作表中滚动查看数据库记录](../vsto/how-to-scroll-through-database-records-in-a-worksheet.md)   
 [如何：使用宿主控件中的数据更新数据源](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)   
 [演练：文档级项目中的简单数据绑定](../vsto/walkthrough-simple-data-binding-in-a-document-level-project.md)   
 [演练：文档级项目中的复杂数据绑定](../vsto/walkthrough-complex-data-binding-in-a-document-level-project.md)   
 [在 Office 解决方案中使用本地数据库文件概述](../vsto/using-local-database-files-in-office-solutions-overview.md)   
 [数据源概述](../data-tools/add-new-data-sources.md)   
 [在 Visual Studio 中将 Windows 窗体控件绑定到数据](../Topic/Binding%20Windows%20Forms%20controls%20to%20data%20in%20Visual%20Studio.md)   
 [在 Office 解决方案中使用本地数据库文件概述](../vsto/using-local-database-files-in-office-solutions-overview.md)   
 [连接到 Windows 窗体应用程序中的数据](/visual-studio/data-tools/connecting-to-data-in-windows-forms-applications)   
 [BindingSource 组件概述](http://msdn.microsoft.com/library/be838caf-fcb0-4b68-827f-58b2c04b747f)  
  
  