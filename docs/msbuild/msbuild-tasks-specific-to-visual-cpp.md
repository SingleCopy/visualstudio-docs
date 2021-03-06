---
title: "MSBuild Tasks Specific to Visual C++ | Microsoft Docs"
ms.custom: ""
ms.date: "06/27/2018"
ms.technology: msbuild
ms.topic: "reference"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "MSBuild, tasks specific to Visual C++"
ms.assetid: 05410f0c-7356-4692-bc00-20664421c9ff
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload: 
  - "cplusplus"
---
# MSBuild tasks specific to Visual C++
Tasks provide the code that runs during the build process. When Visual C++ is installed, the following tasks are available, in addition to those that are installed with [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]. For more information, see [MSBuild (Visual C++) overview](/cpp/build/msbuild-visual-cpp-overview).  
  
 In addition to the parameters for each task, every task also has the following parameters.  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Condition`|Optional `String` parameter.<br /><br /> A `Boolean` expression that the [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] engine uses to determine whether this task will be executed. For information about the conditions that are supported by [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)], see [Conditions](../msbuild/msbuild-conditions.md).|  
|`ContinueOnError`|Optional parameter. Can contain one of the following values:<br /><br /> -   **WarnAndContinue** or **true**. When a task fails, subsequent tasks in the [Target](../msbuild/target-element-msbuild.md) element and the build continue to execute, and all errors from the task are treated as warnings<br />-   **ErrorAndContinue**. When a task fails, subsequent tasks in the `Target` element and the build continue to execute, and all errors from the task are treated as errors.<br />-   **ErrorAndStop** or **false** (default). When a task fails, the remaining tasks in the`Target` element and the build aren't executed, and the entire `Target` element and the build are considered to have failed.<br /><br /> Versions of the .NET Framework before 4.5 supported only the `true` and `false` values.<br /><br /> For more information, see [How to: Ignore errors in tasks](../msbuild/how-to-ignore-errors-in-tasks.md).|  
  
### Related topics  
  
|Title|Description|  
|-----------|-----------------|  
|[BscMake task](../msbuild/bscmake-task.md)|Wraps the Microsoft Browse Information Maintenance Utility tool (*bscmake.exe*).|  
|[CL task](../msbuild/cl-task.md)|Wraps the Visual C++ compiler tool (*cl.exe*).|  
|[CPPClean task](../msbuild/cppclean-task.md)|Deletes the temporary files that MSBuild creates when a Visual C++ project is built.|  
|[LIB task](../msbuild/lib-task.md)|Wraps the Microsoft 32-Bit Library Manager tool (*lib.exe*).|  
|[Link task](../msbuild/link-task.md)|Wraps the Visual C++ linker tool (*link.exe*).|  
|[MIDL task](../msbuild/midl-task.md)|Wraps the Microsoft Interface Definition Language (MIDL) compiler tool (*midl.exe*).|  
|[MT task](../msbuild/mt-task.md)|Wraps the Microsoft Manifest Tool (*mt.exe*).|  
|[RC task](../msbuild/rc-task.md)|Wraps the Microsoft Windows Resource Compiler tool (*rc.exe*).|  
|[SetEnv task](../msbuild/setenv-task.md)|Sets or deletes the value of a specified environment variable.|  
|[VCMessage task](../msbuild/vcmessage-task.md)|Logs warning messages and error messages during a build. (Not extendable. Internal use only.)|  
|[XDCMake task](../msbuild/xdcmake-task.md)|Wraps the XML Documentation tool (*xdcmake.exe*), which merges XML document comment (*.xdc*) files into an *.xml* file.|  
|[XSD task](../msbuild/xsd-task.md)|Wraps the XML Schema Definition tool (*xsd.exe*), which generates schema or class files from a source. *See note below.*|  
|[MSBuild reference](../msbuild/msbuild-reference.md)|Describes the elements of the MSBuild system.|  
|[Tasks](../msbuild/msbuild-tasks.md)|Describes tasks, which are units of code that can be combined to produce a build.|  
|[Task writing](../msbuild/task-writing.md)|Describes how to create a task.|

> [!NOTE]
> In Visual Studio 2017, C++ project support for *xsd.exe* is deprecated. You can still use the **Microsoft.VisualC.CppCodeProvider** APIs by manually adding *CppCodeProvider.dll* to the GAC.