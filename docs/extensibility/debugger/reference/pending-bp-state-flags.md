---
title: "PENDING_BP_STATE_FLAGS | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: 
  - "vs-ide-sdk"
ms.topic: "conceptual"
f1_keywords: 
  - "PENDING_BP_STATE_FLAGS"
helpviewer_keywords: 
  - "PENDING_BP_STATE_FLAGS enumeration"
ms.assetid: 85522449-3fd8-4da5-b0fe-a43160e0c33b
author: "gregvanl"
ms.author: "gregvanl"
manager: douge
ms.workload: 
  - "vssdk"
---
# PENDING_BP_STATE_FLAGS
Specifies the pending breakpoint state flags.  
  
## Syntax  
  
```cpp  
enum enum_PENDING_BP_STATE_FLAGS {   
   PBPSF_NONE        = 0x0000,  
   PBPSF_VIRTUALIZED = 0x0001  
};  
typedef DWORD PENDING_BP_STATE_FLAGS;  
```  
  
```csharp  
public enum enum_PENDING_BP_STATE_FLAGS {   
   PBPSF_NONE        = 0x0000,  
   PBPSF_VIRTUALIZED = 0x0001  
};  
```  
  
## Members  
 PBPSF_NONE  
 Placeholder.  
  
 PBPSF_VIRTUALIZED  
 Specifies a virtualized pending breakpoint, one that is to be bound every time new code is loaded.  
  
## Remarks  
 Used for the `flags` member of the [PENDING_BP_STATE_INFO](../../../extensibility/debugger/reference/pending-bp-state-info.md) structure.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [PENDING_BP_STATE_INFO](../../../extensibility/debugger/reference/pending-bp-state-info.md)