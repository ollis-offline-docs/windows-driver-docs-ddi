---
UID: NN:dbgmodel.IDebugHostData
title: IDebugHostData (dbgmodel.h)
description: An (IDebugHostSymbol derived) interface to data.
ms.date: 07/13/2018
keywords: ["IDebugHostData interface"]
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
 - IDebugHostData
 - dbgmodel/IDebugHostData
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dbgmodel.h
api_name:
 - IDebugHostData
---

# IDebugHostData interface


## -description

An ([IDebugHostSymbol](nn-dbgmodel-idebughostsymbol.md) derived) interface to data.

Represents data within a module (were this within a structure or class it would be an [IDebugHostField](nn-dbgmodel-idebughostfield.md)).

## -inheritance

IDebugHostData inherits from [IDebugHostSymbol](nn-dbgmodel-idebughostsymbol.md).

## -remarks

Data in modules which is not a member of another type is represented by the IDebugHostData interface.

## -see-also

[Debugger Data Model C++ Overview](/windows-hardware/drivers/debugger/data-model-cpp-overview)
