---
title: "错误： 工作组远程登录失败 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: vs.debug.error.workgroup_remote_logon_failure
dev_langs:
- CSharp
- VB
- FSharp
- JScript
- C++
helpviewer_keywords:
- logon failure, remote debugging
- remote debugging, logon failure
caps.latest.revision: "19"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 38ec2de37279e1f383751c9652aeeac74473c50f
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="error-workgroup-remote-logon-failure"></a>错误：工作组远程登录失败
此错误显示如下：  
  
 登录失败: 未知的用户名或密码不正确  
  
 **原因**  
  
 当从工作组上的计算机进行调试并尝试连接到远程计算机时可能发生此错误。 可能的原因包括：  
  
-   远程计算机上没有匹配用户名和密码的帐户。  
  
-   如果在 Visual Studio 计算机和远程计算机都在工作组上，由于默认值可能发生此错误**本地安全策略**远程计算机上设置。 默认设置**本地安全策略**设置**仅来宾-本地用户以来宾身份验证**。 若要在此设置上调试，必须更改到远程计算机上的设置**经典-本地用户以自己的身份验证**。  
  
> [!NOTE]
>  你必须是管理员才能执行以下任务。  
  
### <a name="to-open-the-local-security-policy-window"></a>打开“本地安全策略”窗口  
  
1.  启动**secpol.msc** Microsoft 管理控制台管理单元中。 在 Windows 搜索、Windows“运行”框中或命令提示符处键入 secpol.msc。  
  
### <a name="to-add-user-rights-assignments"></a>添加用户权限分配  
  
1.  打开**本地安全策略**窗口。  
  
2.  展开**本地策略**文件夹。  
  
3.  单击**用户权限分配**。  
  
4.  在**策略**列中，双击**调试程序**若要查看当前本地组策略分配中的**本地安全策略设置**对话框。  
  
     ![本地安全策略用户权限](../debugger/media/dbg_err_localsecuritypolicy_userrightsdebugprograms.png "DBG_ERR_LocalSecurityPolicy_UserRightsDebugPrograms")  
  
5.  若要添加新用户，请单击**添加用户或组**按钮。  
  
### <a name="to-change-the-sharing-and-security-model"></a>更改“共享和安全模型”  
  
1.  打开**本地安全策略**窗口。  
  
2.  展开**本地策略**文件夹。  
  
3.  单击**安全选项**。  
  
4.  在**策略**列中，双击**网络访问： 本地帐户的共享和安全模型**。  
  
5.  在**网络访问： 本地帐户的共享和安全模型**对话框框中，将值更改**经典-本地用户以自己的身份验证**单击**应用**按钮。  
  
     ![本地安全策略安全选项](../debugger/media/dbg_err_localsecuritypolicy_securityoptions_networkaccess.png "DBG_ERR_LocalSecurityPolicy_SecurityOptions_NetworkAccess")  
  
## <a name="see-also"></a>请参阅  
 [远程调试错误和疑难解答](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [远程调试](../debugger/remote-debugging.md)