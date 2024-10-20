---
UID: NS:mountmgr._MOUNTMGR_TARGET_NAME
title: MOUNTMGR_TARGET_NAME (mountmgr.h)
description: Learn about the MOUNTMGR_TARGET_NAME structure.
tech.root: storage
ms.date: 06/04/2024
keywords: ["MOUNTMGR_TARGET_NAME structure"]
ms.keywords: "*PMOUNTMGR_TARGET_NAME, MOUNTMGR_TARGET_NAME, MOUNTMGR_TARGET_NAME structure [Storage Devices], PMOUNTMGR_TARGET_NAME, PMOUNTMGR_TARGET_NAME structure pointer [Storage Devices], _MOUNTMGR_TARGET_NAME, mountmgr/MOUNTMGR_TARGET_NAME, mountmgr/PMOUNTMGR_TARGET_NAME, storage.mountmgr_target_name, structs-mntmgr_abcf0a10-ecbb-433e-9848-c2d5065ca1ac.xml"
req.header: mountmgr.h
req.include-header: Mountmgr.h
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
req.typenames: MOUNTMGR_TARGET_NAME, *PMOUNTMGR_TARGET_NAME
f1_keywords:
 - _MOUNTMGR_TARGET_NAME
 - mountmgr/_MOUNTMGR_TARGET_NAME
 - PMOUNTMGR_TARGET_NAME
 - mountmgr/PMOUNTMGR_TARGET_NAME
 - MOUNTMGR_TARGET_NAME
 - mountmgr/MOUNTMGR_TARGET_NAME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mountmgr.h
api_name:
 - _MOUNTMGR_TARGET_NAME
 - PMOUNTMGR_TARGET_NAME
 - MOUNTMGR_TARGET_NAME
---

## -description

The MOUNTMGR_TARGET_NAME structure contains the nonpersistent target device name for a device and is used by mount manager clients with the [IOCTL_MOUNTMGR_KEEP_LINKS_WHEN_OFFLINE](ni-mountmgr-ioctl_mountmgr_keep_links_when_offline.md) request to tell the mount manager to keep the symbolic link for a device active even after the device has gone offline.

## -struct-fields

### -field DeviceNameLength

Contains the length, in bytes, of the device name stored in **DeviceName**.

### -field DeviceName

Contains the nonpersistent target device name.

## -remarks

Nonpersistent target names must contain the full path of a target object name in the system object tree. For example: "\Device\HarddiskVolume1".

For more information, see [Supporting Mount Manager Requests in a Storage Class Driver](/windows-hardware/drivers/storage/supporting-mount-manager-requests-in-a-storage-class-driver).

## -see-also

[IOCTL_MOUNTMGR_KEEP_LINKS_WHEN_OFFLINE](ni-mountmgr-ioctl_mountmgr_keep_links_when_offline.md)
