---
UID: NF:netconfiguration.NetConfigurationQueryMultiString
title: NetConfigurationQueryMultiString function (netconfiguration.h)
description: Retrieves the MultiString-valued registry entry associated with a value name in the specified configuration object.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetConfigurationQueryMultiString function"]
ms.keywords: NetConfigurationQueryMultiString
req.header: netconfiguration.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.21
req.umdf-ver: 2.33 
req.lib: NetAdapterCxStub.lib
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.alt-api: 
req.alt-loc: 
targetos: Windows
f1_keywords:
 - NetConfigurationQueryMultiString
 - netconfiguration/NetConfigurationQueryMultiString
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netconfiguration.h
api_name:
 - NetConfigurationQueryMultiString
---

# NetConfigurationQueryMultiString function


## -description

Retrieves the MultiString-valued registry entry associated with a value name in the specified configuration object.

## -parameters

### -param Configuration [_In_]

Handle to a NETCONFIGURATION object that represents an opened registry key.

### -param ValueName [_In_]

A pointer to a [**UNICODE_STRING**](/windows/win32/api/ntdef/ns-ntdef-_unicode_string) structure that contains a value name in the device's software key.

### -param StringsAttributes [_In_opt_]

A pointer to a [WDF_OBJECT_ATTRIBUTES](../wdfobject/ns-wdfobject-_wdf_object_attributes.md) structure that contains driver-supplied attributes for the new WDFSTRING objects. This parameter is optional and can be WDF_NO_OBJECT_ATTRIBUTES.

### -param Collection [_Inout_]

A handle to a driver-supplied collection object. If the function succeeds, contains a WDFSTRING object for each string assigned to *ValueName*.

## -returns

The function returns STATUS_SUCCESS if the operation succeeds. If the registry value is NULL, **NetConfigurationQueryMultiString** returns **STATUS_OBJECT_NAME_NOT_FOUND**.

## -remarks

The client driver obtains a handle to a NETCONFIGURATION object by calling [NetAdapterOpenConfiguration](../netadapter/nf-netadapter-netadapteropenconfiguration.md) or [NetConfigurationOpenSubConfiguration](nf-netconfiguration-netconfigurationopensubconfiguration.md).

By default, the strings are parented to the collection object. The client driver can change this by setting the **ParentObject** member of the [WDF_OBJECT_ATTRIBUTES](../wdfobject/ns-wdfobject-_wdf_object_attributes.md) structure.

## -see-also
