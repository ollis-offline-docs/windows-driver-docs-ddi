---
UID: NC:netpacketqueue.EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED
title: EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED (netpacketqueue.h)
description: The EvtPacketQueueSetNotificationEnabled callback function is implemented by the client driver to perform client-specific processing when there are new packets received in the specified queue's ring buffer.
tech.root: netvista
ms.date: 04/01/2022
keywords: ["EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED callback function"]
req.header: netpacketqueue.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.27
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
targetos: Windows
ms.custom: RS5
f1_keywords:
 - EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED
 - netpacketqueue/EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - netpacketqueue.h
api_name:
 - EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED
---

# EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED callback function


## -description

The *EvtPacketQueueSetNotificationEnabled* callback function is implemented by the client driver to perform client-specific processing when there are new packets received in the specified queue's ring buffer.

## -parameters

### -param PacketQueue [_In_]

A handle to a packet queue.

### -param NotificationEnabled [_In_]

A value of **TRUE** requests that the client enable packet queue notification. A value of **FALSE** requests that the client disable packet queue notification.

## -prototype

```C++
//Declaration

EVT_PACKET_QUEUE_SET_NOTIFICATION_ENABLED EvtPacketQueueSetNotificationEnabled; 

// Definition

VOID EvtPacketQueueSetNotificationEnabled 
(
	NETPACKETQUEUE PacketQueue
	BOOLEAN NotificationEnabled
)
{...}

```

## -remarks

Register this callback function in your *EVT_NET_ADAPTER_CREATE_TX(RX)QUEUE* callback. Set the appropriate member of a [**NET_PACKET_QUEUE_CONFIG**](ns-netpacketqueue-_net_packet_queue_config.md) structure when you are initializing the structure with [**NET_PACKET_QUEUE_CONFIG_INIT**](nf-netpacketqueue-net_packet_queue_config_init.md), then call **NetTx(Rx)QueueCreate**.

NetAdapterCx serializes this callback function along with the packet queue's [*EVT_PACKET_QUEUE_CANCEL*](nc-netpacketqueue-evt_packet_queue_cancel.md) and [*EVT_PACKET_QUEUE_ADVANCE*](nc-netpacketqueue-evt_packet_queue_advance.md) callback functions.

For more info and a diagram showing the NetAdapterCx data path polling model, see [Transmit and receive queues](/windows-hardware/drivers/netcx/transmit-and-receive-queues).

## -see-also

[*EVT_NET_ADAPTER_CREATE_RXQUEUE*](../netadapter/nc-netadapter-evt_net_adapter_create_rxqueue.md)

[*EVT_NET_ADAPTER_CREATE_TXQUEUE*](../netadapter/nc-netadapter-evt_net_adapter_create_txqueue.md)

[**NetRxQueueCreate**](../netrxqueue/nf-netrxqueue-netrxqueuecreate.md)

[**NetTxQueueCreate**](../nettxqueue/nf-nettxqueue-nettxqueuecreate.md)

[*EVT_PACKET_QUEUE_START*](nc-netpacketqueue-evt_packet_queue_start.md)

[*EVT_PACKET_QUEUE_ADVANCE*](nc-netpacketqueue-evt_packet_queue_advance.md)

[*EVT_PACKET_QUEUE_CANCEL*](nc-netpacketqueue-evt_packet_queue_cancel.md)

[*EVT_PACKET_QUEUE_STOP*](nc-netpacketqueue-evt_packet_queue_stop.md)

[**NetTxQueueNotifyMoreCompletedPacketsAvailable**](../nettxqueue/nf-nettxqueue-nettxqueuenotifymorecompletedpacketsavailable.md)

[**NetRxQueueNotifyMoreReceivedPacketsAvailable**](../netrxqueue/nf-netrxqueue-netrxqueuenotifymorereceivedpacketsavailable.md)
