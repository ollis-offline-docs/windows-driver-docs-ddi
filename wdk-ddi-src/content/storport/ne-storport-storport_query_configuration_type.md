---
UID: NE:storport._STORPORT_QUERY_CONFIGURATION_TYPE
title: STORPORT_QUERY_CONFIGURATION_TYPE
description: The STORPORT_QUERY_CONFIGURATION_TYPE enumerator identifies the configuration being queried in StorPortQueryConfiguration.
tech.root: storage
ms.date: 02/28/2024
keywords: ["STORPORT_QUERY_CONFIGURATION_TYPE enumeration"]
ms.keywords: STORPORT_QUERY_CONFIGURATION_TYPE, STORPORT_QUERY_CONFIGURATION_TYPE, *PSTORPORT_QUERY_CONFIGURATION_TYPE,
req.header: storport.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: STORPORT_QUERY_CONFIGURATION_TYPE, *PSTORPORT_QUERY_CONFIGURATION_TYPE
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - _STORPORT_QUERY_CONFIGURATION_TYPE
 - storport/_STORPORT_QUERY_CONFIGURATION_TYPE
 - PSTORPORT_QUERY_CONFIGURATION_TYPE
 - storport/PSTORPORT_QUERY_CONFIGURATION_TYPE
 - STORPORT_QUERY_CONFIGURATION_TYPE
 - storport/STORPORT_QUERY_CONFIGURATION_TYPE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - storport.h
api_name:
 - _STORPORT_QUERY_CONFIGURATION_TYPE
 - PSTORPORT_QUERY_CONFIGURATION_TYPE
 - STORPORT_QUERY_CONFIGURATION_TYPE
dev_langs:
 - c++
---

# STORPORT_QUERY_CONFIGURATION_TYPE enumeration

## -description

The **STORPORT_QUERY_CONFIGURATION_TYPE** enumerator identifies the configuration type being queried in **[StorPortQueryConfiguration](nf-storport-storportqueryconfiguration.md)**.

## -enum-fields

### -field StorportQueryConfigurationD3

Query whether the device has a D3 configuration.

### -field StorportQueryConfigurationNvmeIce

Query whether the device has an NVMe ICE configuration.

### -field StorportQueryConfigurationMax

First illegal configuration value; do not use.

## -remarks

## -see-also

- **[StorPortQueryConfiguration](nf-storport-storportqueryconfiguration.md)**
