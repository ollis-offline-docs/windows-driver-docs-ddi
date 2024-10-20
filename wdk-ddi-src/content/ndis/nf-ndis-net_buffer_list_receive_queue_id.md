---
UID: NF:ndis.NET_BUFFER_LIST_RECEIVE_QUEUE_ID
title: NET_BUFFER_LIST_RECEIVE_QUEUE_ID macro (ndis.h)
description: The NET_BUFFER_LIST_RECEIVE_QUEUE_ID macro sets or gets the identifier of a virtual machine queue (VMQ) or single root I/O virtualization (SR-IOV) receive queue identifier within the out-of-band (OOB) data of a NET_BUFFER_LIST structure.
tech.root: netvista
ms.date: 04/13/2018
keywords: ["NET_BUFFER_LIST_RECEIVE_QUEUE_ID macro"]
ms.keywords: NET_BUFFER_LIST_RECEIVE_QUEUE_ID
req.header: ndis.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Supported in NDIS 6.20 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
returns-override: true
f1_keywords:
 - NET_BUFFER_LIST_RECEIVE_QUEUE_ID
 - ndis/NET_BUFFER_LIST_RECEIVE_QUEUE_ID
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ndis.h
api_name:
 - NET_BUFFER_LIST_RECEIVE_QUEUE_ID
---

# NET_BUFFER_LIST_RECEIVE_QUEUE_ID macro


## -description

The **NET_BUFFER_LIST_RECEIVE_QUEUE_ID** macro sets or gets the identifier of a virtual machine queue (VMQ) or single root I/O virtualization (SR-IOV) receive queue identifier within the out-of-band (OOB) data of a [**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md) structure.

For the SR-IOV interface, the receive queue is created on a default or nondefault virtual port (VPort). Starting with Windows Server 2012, only the default receive queue of a VPort is supported.

## -parameters

### -param _NBL

A pointer to a **NET_BUFFER_LIST** structure.

## -returns

**NET_BUFFER_LIST_RECEIVE_QUEUE_ID** returns a USHORT value for a receive queue identifier.

## -remarks

Any NDIS 6.20 or later driver can use **NET_BUFFER_LIST_RECEIVE_QUEUE_ID** to set or get the receive queue identifier from a [**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md) structure. **NET_BUFFER_LIST_RECEIVE_QUEUE_ID** accesses the receive queue identifier from the **QueueId** member of the [**NDIS_NET_BUFFER_LIST_FILTERING_INFO**](ns-ndis-_ndis_net_buffer_list_filtering_info.md) structure.

> [!NOTE]
> When a VMQ is deleted (for example, during VM live migration), it is possible for the miniport driver to receive an NBL that contains an invalid **QueueId** value. If this happens, the miniport should ignore the invalid queue ID and use 0 (the default queue) instead. The **QueueId** is found in the **NetBufferListFilteringInfo** portion of the NBL's OOB data, and is retrieved by using the **NET_BUFFER_LIST_RECEIVE_QUEUE_ID** macro.

## -see-also

[**NET_BUFFER_LIST**](../nbl/ns-nbl-net_buffer_list.md)

[**NDIS_NET_BUFFER_LIST_FILTERING_INFO**](ns-ndis-_ndis_net_buffer_list_filtering_info.md)

