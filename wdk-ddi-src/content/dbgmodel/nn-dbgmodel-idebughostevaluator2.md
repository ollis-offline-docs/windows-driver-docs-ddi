---
UID: NN:dbgmodel.IDebugHostEvaluator2
title: IDebugHostEvaluator2 (dbgmodel.h)
description: The IDebugHostEvaluator2 (dbgmodel.h) interface provides access to the language based expression evaluator in the underlying debugger.
ms.date: 06/11/2019
keywords: ["IDebugHostEvaluator2 interface"]
req.header: dbgmodel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: debugger
ms.custom: RS5
f1_keywords:
 - IDebugHostEvaluator2
 - dbgmodel/IDebugHostEvaluator2
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dbgmodel.h
api_name:
 - IDebugHostEvaluator2
---

# IDebugHostEvaluator2 interface


## -description

The expression evaluator interface to the underlying debugger.

This version 2 of the interface supports all of the previous methods with identical signatures and includes additional new methods that provide added functionality. The new methods are listed in the header at the end of the section for that interface.

## -inheritance

IDebugHostEvaluator2 inherits from [IDebugHostEvaluator](nn-dbgmodel-idebughostevaluator.md).

## -remarks

One of the most important pieces of functionality which the debug host provides to clients is access to its language based expression evaluator. The [IDebugHostEvaluator](nn-dbgmodel-idebughostevaluator.md) and IDebugHostEvaluator2 interfaces are the means to access that functionality from the debug host.

## -see-also

[Debugger Data Model C++ Overview](/windows-hardware/drivers/debugger/data-model-cpp-overview)
