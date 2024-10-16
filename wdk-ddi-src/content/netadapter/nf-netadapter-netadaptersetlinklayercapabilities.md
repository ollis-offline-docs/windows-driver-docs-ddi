---
UID: NF:netadapter.NetAdapterSetLinkLayerCapabilities
title: NetAdapterSetLinkLayerCapabilities function (netadapter.h)
description: Sets the link layer capabilities of the network adapter.
tech.root: netvista
ms.date: 03/30/2022
keywords: ["NetAdapterSetLinkLayerCapabilities function"]
ms.keywords: NetAdapterSetLinkLayerCapabilities
req.header: netadapter.h
req.include-header: netadaptercx.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.21
req.umdf-ver: 2.33 
req.lib: 
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
req.typenames: NetAdapterSetLinkLayerCapabilities
targetos: Windows
f1_keywords:
 - NetAdapterSetLinkLayerCapabilities
 - netadapter/NetAdapterSetLinkLayerCapabilities
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - netadapter.h
api_name:
 - NetAdapterSetLinkLayerCapabilities
---

# NetAdapterSetLinkLayerCapabilities function


## -description

Sets the link layer capabilities of the network adapter.

## -parameters

### -param Adapter [_In_]

The network adapter object that the client created in a prior call to [**NetAdapterCreate**](nf-netadapter-netadaptercreate.md).

### -param LinkLayerCapabilities [_In_]

A pointer to an allocated and initialized [**NET_ADAPTER_LINK_LAYER_CAPABILITIES**](ns-netadapter-_net_adapter_link_layer_capabilities.md) structure.

## -remarks

The client driver calls this function when starting a net adapter, before calling [**NetAdapterStart**](nf-netadapter-netadapterstart.md).

This function, along with a few other set capability functions (see below), is the replacement for the [**NDIS_MINIPORT_ADAPTER_GENERAL_ATTRIBUTES**](../ndis/ns-ndis-_ndis_miniport_adapter_general_attributes.md) union that a (non-WDF) client of Ndis.sys sets by calling [**NdisMSetMiniportAttributes**](../ndis/nf-ndis-ndismsetminiportattributes.md).

## -see-also

[**NetAdapterSetDataPathCapabilities**](nf-netadapter-netadaptersetdatapathcapabilities.md)

