---
UID: NC:usbpmapi.EVT_USBPM_EVENT_CALLBACK
title: EVT_USBPM_EVENT_CALLBACK (usbpmapi.h)
description: Sends notifications about hub arrival/removal and connector state changes.
ms.date: 09/30/2018
keywords: ["EVT_USBPM_EVENT_CALLBACK callback function"]
tech.root: usbref
req.header: usbpmapi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1809
req.target-min-winversvr: 
req.kmdf-ver: 1.27
req.umdf-ver: 2.27
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: RS5
f1_keywords:
 - EVT_USBPM_EVENT_CALLBACK
 - usbpmapi/EVT_USBPM_EVENT_CALLBACK
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - usbpmapi.h
api_name:
 - EVT_USBPM_EVENT_CALLBACK
---

# EVT_USBPM_EVENT_CALLBACK callback function


## -description

Sends notifications about hub arrival/removal and connector state changes.

## -parameters

### -param Params [In]

A pointer to the caller-supplied [**USBPM_EVENT_CALLBACK_PARAMS**](ns-usbpmapi-_usbpm_event_callback_params.md) structure that the client driver fills with event-specific data.

## -prototype

```cpp
//Declaration

EVT_USBPM_EVENT_CALLBACK EvtUsbpmEventCallback; 

// Definition

VOID EvtUsbpmEventCallback 
(
	PUSBPM_EVENT_CALLBACK_PARAMS Params
)
{...}

```

## -remarks

The client driver registers its implementation of this callback function by setting the appropriate member of [**USBPM_CLIENT_CONFIG**](ns-usbpmapi-_usbpm_client_config.md) and then calling [**UsbPm_Register**](nf-usbpmapi-usbpm_register.md). Policy Manager can invoke the client driver's implementation before [**UsbPm_Register**] returns.

To stop Policy Manager from invoking the callback function, the client driver must call [**UsbPm_Deregister**](nf-usbpmapi-usbpm_deregister.md).

Callback function calls are serialized. Only one call is active at a time.

## -see-also

[**USBPM_EVENT_CALLBACK_PARAMS**](ns-usbpmapi-_usbpm_event_callback_params.md)

