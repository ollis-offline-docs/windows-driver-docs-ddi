---
UID: NS:1394._SPEED_MAP
title: _SPEED_MAP (1394.h)
description: The SPEED_MAP structure is stores an IEEE 1394 bus speed map.
old-location: ieee\speed_map.htm
tech.root: IEEE
ms.date: 02/15/2018
keywords: ["SPEED_MAP structure"]
ms.keywords: "*PSPEED_MAP, 1394/PSPEED_MAP, 1394/SPEED_MAP, 1394stct_0df32f88-2279-4df2-a7f3-856ddfdacb56.xml, IEEE.speed_map, PSPEED_MAP, PSPEED_MAP structure pointer [Buses], SPEED_MAP, SPEED_MAP structure [Buses], _SPEED_MAP"
req.header: 1394.h
req.include-header: 1394.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
req.typenames: SPEED_MAP, *PSPEED_MAP
f1_keywords:
 - _SPEED_MAP
 - 1394/_SPEED_MAP
 - PSPEED_MAP
 - 1394/PSPEED_MAP
 - SPEED_MAP
 - 1394/SPEED_MAP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - 1394.h
api_name:
 - _SPEED_MAP
 - PSPEED_MAP
 - SPEED_MAP
---

# _SPEED_MAP structure


## -description

The SPEED_MAP structure is stores an IEEE 1394 bus speed map.

## -struct-fields

### -field SPD_Length

Specifies the number of quadlets in the speed map.

### -field SPD_CRC

Specifies the CRC value for the speed map.

### -field SPD_Generation

Specifies the generation count for the bus reset that corresponds to this speed map.

### -field SPD_Speed_Code

Specifies an array of speed codes. Currently, the possible values are:

SCODE_100_RATE

SCODE_200_RATE

SCODE_400_RATE

## -remarks

The SPEED_MAP structure describes the maximum speed that devices on the bus can attain. All values in this structure are recorded in big-endian format.

## -see-also

<a href="/windows-hardware/drivers/ddi/1394/ni-1394-ioctl_1394_class">REQUEST_GET_SPEED_TOPOLOGY_MAPS</a>

