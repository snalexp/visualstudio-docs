---
title: "IDebugObject | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: "visual-studio-dev14"
ms.technology: "vs-ide-sdk"
ms.topic: reference
f1_keywords: 
  - "IDebugObject"
helpviewer_keywords: 
  - "IDebugObject interface"
ms.assetid: 05cd8bf4-c9ee-4b49-b782-2263c33067d6
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
---
# IDebugObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

> [!IMPORTANT]
> In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface represents an object that the binder creates to encapsulate the values of symbols and expressions.  
  
## Syntax  
  
```  
IDebugObject : IUnknown  
```  
  
## Notes for Implementers  
 An expression evaluator implements this interface to represent an object.  
  
## Notes for Callers  
 This interface is the base class for all objects that the expression evaluator uses in parsed expressions. It is returned by a call to the [Bind](../../../extensibility/debugger/reference/idebugbinder-bind.md) method. [QueryInterface](https://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) obtains the more specialized interfaces from this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugObject`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetSize](../../../extensibility/debugger/reference/idebugobject-getsize.md)|Gets the size of the object.|  
|[GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)|Gets the value of the object as a consecutive series of bytes.|  
|[SetValue](../../../extensibility/debugger/reference/idebugobject-setvalue.md)|Sets the value of the object from a consecutive series of bytes.|  
|[SetReferenceValue](../../../extensibility/debugger/reference/idebugobject-setreferencevalue.md)|Sets the reference value of this object.|  
|[GetMemoryContext](../../../extensibility/debugger/reference/idebugobject-getmemorycontext.md)|Gets the memory context that represents the address of the value of the object.|  
|[GetManagedDebugObject](../../../extensibility/debugger/reference/idebugobject-getmanageddebugobject.md)|Creates a copy of the managed object in the address space of the debug engine.|  
|[IsNullReference](../../../extensibility/debugger/reference/idebugobject-isnullreference.md)|Tests whether this object is a null reference.|  
|[IsEqual](../../../extensibility/debugger/reference/idebugobject-isequal.md)|Compares an object to this one.|  
|[IsReadOnly](../../../extensibility/debugger/reference/idebugobject-isreadonly.md)|Determines if this object is read-only.|  
|[IsProxy](../../../extensibility/debugger/reference/idebugobject-isproxy.md)|Determines if the object is a transparent proxy.|  
  
## Remarks  
 The expression evaluator uses this interface as the base class to represent objects in a parse tree.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Expression Evaluation Interfaces](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [GetElement](../../../extensibility/debugger/reference/idebugarrayobject-getelement.md)   
 [Bind](../../../extensibility/debugger/reference/idebugbinder-bind.md)