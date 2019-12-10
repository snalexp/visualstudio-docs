---
title: "IDebugProcess3 | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: "visual-studio-dev14"
ms.technology: "vs-ide-sdk"
ms.topic: reference
f1_keywords: 
  - "IDebugProcess3"
helpviewer_keywords: 
  - "IDebugProcess3 interface"
ms.assetid: 7bd6b952-cf34-4e66-b8f6-d472dac3748f
caps.latest.revision: 25
ms.author: gregvanl
manager: jillfra
---
# IDebugProcess3
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

This interface represents a running process and its programs. This interface exists as a replacement to several methods in the [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) interface. It provides control over all programs in the process.  
  
> [!NOTE]
> [Continue](../../../extensibility/debugger/reference/idebugprogram2-continue.md), [Execute](../../../extensibility/debugger/reference/idebugprogram2-execute.md), and [Step](../../../extensibility/debugger/reference/idebugprogram2-step.md) methods are deprecated and should no longer be used. Use the corresponding methods on the `IDebugProcess3` interface instead.  
  
## Syntax  
  
```  
IDebugProcess3 : IDebugProcess2  
```  
  
## Notes for Implementers  
 This interface is implemented by a custom port supplier to manage programs as a group. When programs are managed as a group, you can control their execution and establish a language for an expression evaluator. This interface must be implemented by the port supplier.  
  
## Notes for Callers  
 This interface is called primarily by the session debug manager (SDM) in order to interact with a group of programs identified in this process.  
  
 Call [QueryInterface](https://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) on an [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) interface to obtain this interface.  
  
## Methods in Vtable Order  
 In addition to the methods inherited from [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md), `IDebugProcess3` implements the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[Continue](../../../extensibility/debugger/reference/idebugprocess3-continue.md)|Continues execution of or stepping through a process.|  
|[Execute](../../../extensibility/debugger/reference/idebugprocess3-execute.md)|Begins execution of a process.|  
|[Step](../../../extensibility/debugger/reference/idebugprocess3-step.md)|Steps forward one instruction or statement in the process.|  
|[GetDebugReason](../../../extensibility/debugger/reference/idebugprocess3-getdebugreason.md)|Gets the reason that the process was launched for debugging.|  
|[SetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-sethostingprocesslanguage.md)|Sets the hosting language so that the debug engine can load the appropriate expression evaluator.|  
|[GetHostingProcessLanguage](../../../extensibility/debugger/reference/idebugprocess3-gethostingprocesslanguage.md)|Retrieves the language currently set for this process.|  
|[DisableENC](../../../extensibility/debugger/reference/idebugprocess3-disableenc.md)|Disables Edit and Continue (ENC) for this process.<br /><br /> A custom port supplier does not implement this method (it should always return `E_NOTIMPL`).|  
|[GetENCAvailableState](../../../extensibility/debugger/reference/idebugprocess3-getencavailablestate.md)|Get the ENC state for this process.<br /><br /> A custom port supplier does not implement this method (it should always return `E_NOTIMPL`).|  
|[GetEngineFilter](../../../extensibility/debugger/reference/idebugprocess3-getenginefilter.md)|Retrieves an array of unique identifiers for available debug engines.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)