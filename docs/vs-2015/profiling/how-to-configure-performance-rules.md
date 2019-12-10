---
title: "How to: Configure Performance Rules | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: "visual-studio-dev14"
ms.technology: "vs-ide-debug"
ms.topic: conceptual
f1_keywords: 
  - "vs.performance.ruleseditor"
ms.assetid: a148b468-b849-4858-880a-808a6b47e596
caps.latest.revision: 19
author: MikeJo5000
ms.author: mikejo
manager: jillfra
---
# How to: Configure Performance Rules
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The performance warnings of th Visual Studio Profiling Tools indicate issues in a profiled application that can slow program execution. Warnings can also indicate that you might need to change collection methods to collect more useful data. Performance warnings are generated automatically in a profiling session and appear in the **Error List** window when a profiling data file is opened in [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)]. Certain warnings might not apply to the scenarios that you are interested in, and some warnings might be raised inaccurately. You can configure performance warnings to show or hide specific warnings.  
  
### To configure profiler performance warnings  
  
1. On the **Tools** menu, click **Options**.  
  
2. Expand **Performance Tools**, and then click **Rules**.  
  
3. To enable or disable a warning, select or clear the check box next to the warning **ID** and name.  
  
4. To specify the warring level of a rule, click the **Action** cell next to the rule and then click the warning level.  
  
    - **Disabled** - disables the rule (this is the same as clearing the check box next to the rule ID).  
  
    - **Warning** - displays rule as a warning.  
  
    - **Error** - halts profiling execution and displays rule as a error.  
  
    - **Information** - displays rule as information only.