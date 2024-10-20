---
UID: NS:dispmprt._DXGK_VIDEO_OUTPUT_CAPABILITIES
title: _DXGK_VIDEO_OUTPUT_CAPABILITIES (dispmprt.h)
description: The DXGK_VIDEO_OUTPUT_CAPABILITIES structure contains information about the capabilities of a video output on a display adapter.
old-location: display\dxgk_video_output_capabilities.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["DXGK_VIDEO_OUTPUT_CAPABILITIES structure"]
ms.keywords: "*PDXGK_VIDEO_OUTPUT_CAPABILITIES, DXGK_VIDEO_OUTPUT_CAPABILITIES, DXGK_VIDEO_OUTPUT_CAPABILITIES structure [Display Devices], DmStructs_018a3f8f-c9bd-4000-b27d-b3dc3e46f14a.xml, PDXGK_VIDEO_OUTPUT_CAPABILITIES, PDXGK_VIDEO_OUTPUT_CAPABILITIES structure pointer [Display Devices], _DXGK_VIDEO_OUTPUT_CAPABILITIES, display.dxgk_video_output_capabilities, dispmprt/DXGK_VIDEO_OUTPUT_CAPABILITIES, dispmprt/PDXGK_VIDEO_OUTPUT_CAPABILITIES"
req.header: dispmprt.h
req.include-header: Dispmprt.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.typenames: DXGK_VIDEO_OUTPUT_CAPABILITIES, *PDXGK_VIDEO_OUTPUT_CAPABILITIES
f1_keywords:
 - _DXGK_VIDEO_OUTPUT_CAPABILITIES
 - dispmprt/_DXGK_VIDEO_OUTPUT_CAPABILITIES
 - PDXGK_VIDEO_OUTPUT_CAPABILITIES
 - dispmprt/PDXGK_VIDEO_OUTPUT_CAPABILITIES
 - DXGK_VIDEO_OUTPUT_CAPABILITIES
 - dispmprt/DXGK_VIDEO_OUTPUT_CAPABILITIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dispmprt.h
api_name:
 - _DXGK_VIDEO_OUTPUT_CAPABILITIES
 - PDXGK_VIDEO_OUTPUT_CAPABILITIES
 - DXGK_VIDEO_OUTPUT_CAPABILITIES
---

# _DXGK_VIDEO_OUTPUT_CAPABILITIES structure


## -description

The DXGK_VIDEO_OUTPUT_CAPABILITIES structure contains information about the capabilities of a video output on a display adapter.

## -struct-fields

### -field InterfaceTechnology

A <a href="/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_video_output_technology">D3DKMDT_VIDEO_OUTPUT_TECHNOLOGY</a> enumerator that indicates the type of connector the video output uses to connect to an external display device.

### -field MonitorOrientationAwareness

A <a href="/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_monitor_orientation_awareness">D3DKMDT_MONITOR_ORIENTATION_AWARENESS</a> enumerator that describes the video output's ability to detect the rotation angle of an external display device.

### -field SupportsSdtvModes

Indicates whether the video output supports standard definition TV (SDTV) modes.

## -remarks

All child devices of a display adapter are onboard devices. Monitors and other external devices that connect to the display adapter are not considered child devices. Display adapters have two types of child devices: <b>TypeVideoOutput</b> and <b>TypeOther</b>. This structure applies only to child devices of type <b>TypeVideoOutput</b>.

The <b>ChildCapabilities</b> member of a <a href="/windows-hardware/drivers/ddi/dispmprt/ns-dispmprt-_dxgk_child_descriptor">DXGK_CHILD_DESCRIPTOR</a> structure is a DXGK_CHILD_CAPABILITIES structure. The <b>Type.VideoOutput</b> member of a DXGK_CHILD_CAPABILITIES structure is a DXGK_VIDEO_OUTPUT_CAPABILITIES structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/dispmprt/ns-dispmprt-_dxgk_child_capabilities">DXGK_CHILD_CAPABILITIES</a>



<a href="/windows-hardware/drivers/ddi/dispmprt/ns-dispmprt-_dxgk_child_descriptor">DXGK_CHILD_DESCRIPTOR</a>



<a href="/windows-hardware/drivers/ddi/dispmprt/nc-dispmprt-dxgkddi_query_child_relations">DxgkDdiQueryChildRelations</a>

