---
UID: NF:ucmtypes.UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG
title: UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG function (ucmtypes.h)
description: Initializes a UCM_PD_REQUEST_DATA_OBJECT structure by interpreting Request Data Object values and sets each field correctly.
old-location: buses\ucm_pd_request_data_object_init_ulong.htm
tech.root: usbref
ms.date: 05/07/2018
keywords: ["UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG function"]
ms.keywords: UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG, UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG function [Buses], buses.ucm_pd_request_data_object_init_ulong, ucmtypes/UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG
req.header: ucmtypes.h
req.include-header: Ucmcx.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 1.15
req.umdf-ver: 2.15
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG
 - ucmtypes/UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ucmtypes.h
api_name:
 - UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG
---

# UCM_PD_REQUEST_DATA_OBJECT_INIT_ULONG function


## -description

Initializes a <a href="/windows-hardware/drivers/ddi/ucmtypes/ns-ucmtypes-_ucm_pd_request_data_object">UCM_PD_REQUEST_DATA_OBJECT</a>  structure by interpreting Request Data Object values and sets each field correctly.

## -parameters

### -param Rdo

<p>A pointer to a <a href="/windows-hardware/drivers/ddi/ucmtypes/ns-ucmtypes-_ucm_pd_request_data_object"><b>UCM_PD_REQUEST_DATA_OBJECT</b></a> structure.</p>

### -param UlongInLittleEndian [in]


The ULONG value to set in the <b>Ul</b> member of   <a href="/windows-hardware/drivers/ddi/ucmtypes/ns-ucmtypes-_ucm_pd_request_data_object">UCM_PD_REQUEST_DATA_OBJECT</a>.

## -remarks

For information about Request Data Objects, see the Power Delivery specification. There are different types of Request Data Objects and the type depends on the Power Data Object that is specified in the <b>ObjectPosition</b> member of <a href="/windows-hardware/drivers/ddi/ucmtypes/ns-ucmtypes-_ucm_pd_request_data_object">UCM_PD_REQUEST_DATA_OBJECT</a>. The source buffer is little-endian format. The client driver can call the [**memcpy**](/cpp/c-runtime-library/reference/memcpy-wmemcpy) function to get the Request Data Objects from the hardware into an array of <b>UCM_PD_REQUEST_DATA_OBJECT</b> structures.


## -see-also

<a href="/windows-hardware/drivers/ddi/ucmtypes/ns-ucmtypes-_ucm_pd_request_data_object">UCM_PD_REQUEST_DATA_OBJECT</a>
