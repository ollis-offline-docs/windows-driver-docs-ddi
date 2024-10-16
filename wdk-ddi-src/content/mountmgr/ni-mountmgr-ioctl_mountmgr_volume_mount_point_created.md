---
UID: NI:mountmgr.IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED
title: IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED (mountmgr.h)
description: Learn about the IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED IOCTL.
tech.root: storage
ms.date: 06/04/2024
keywords: ["IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED IOCTL"]
ms.keywords: IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED, IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED control, IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED control code [Storage Devices], k307_939215e3-3e33-401e-a1d4-c8d82b68f0e8.xml, mountmgr/IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED, storage.ioctl_mountmgr_volume_mount_point_created
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
req.typenames: 
f1_keywords:
 - IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED
 - mountmgr/IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mountmgr.h
api_name:
 - IOCTL_MOUNTMGR_VOLUME_MOUNT_POINT_CREATED
---

## -description

This IOCTL alerts the mount manager that a volume mount point has been created, so that the mount manager can replicate the database entry for the given mount point. Its primary function is to allow volume mount points to persist even when the volumes are moved from one system to another.

The Microsoft Win32 routine **SetVolumeMountPoint** sends this IOCTL to the mount manager, to inform the mount manager that a newly-created directory junction is pointing to a volume name. The mount manager responds by storing the volume name contained in the directory junction along with its unique ID on the volume hosting the directory junction.

## -ioctlparameters

### -ioctl-major-code

[IRP_MJ_DEVICE_CONTROL](/windows-hardware/drivers/kernel/irp-mj-device-control)

### -input-buffer

The mount manager client initializes the [**MOUNTMGR_VOLUME_MOUNT_POINT**](ns-mountmgr-_mountmgr_volume_mount_point.md) structure at the beginning of the buffer at **Irp->AssociatedIrp.SystemBuffer**.

### -input-buffer-length

**Parameters.DeviceIoControl.InputBufferLength** in the I/O stack location of the IRP indicates the size, in bytes, of the input buffer, which must be greater than or equal to ```sizeof(MOUNTMGR_VOLUME_MOUNT_POINT)```.

### -output-buffer

None.

### -output-buffer-length

None.

### -in-out-buffer

N/A

### -inout-buffer-length

N/A

### -status-block

If the operation is successful, the **Status** field is set to STATUS_SUCCESS.

If **InputBufferLength** is less than ```sizeof(MOUNTMGR_VOLUME_MOUNT_POINT)```, the **Status** field is set to STATUS_INVALID_PARAMETER.

## -remarks

For more information, see [Supporting Mount Manager Requests in a Storage Class Driver](/windows-hardware/drivers/storage/supporting-mount-manager-requests-in-a-storage-class-driver).

## -see-also

[**MOUNTMGR_VOLUME_MOUNT_POINT**](ns-mountmgr-_mountmgr_volume_mount_point.md)
