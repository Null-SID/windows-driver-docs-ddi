---
UID: NF:mbbcx.MbbDeviceSetWakeCapabilities
title: MbbDeviceSetWakeCapabilities function (mbbcx.h)
description: The MbbDeviceSetWakeCapabilities method sets the wake capabilities for a MBBCx device.
tech.root: netvista
ms.date: 11/07/2019
keywords: ["MbbDeviceSetWakeCapabilities function"]
ms.keywords: MbbDeviceSetWakeCapabilities
req.header: mbbcx.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
ms.custom: Vb
f1_keywords:
 - MbbDeviceSetWakeCapabilities
 - mbbcx/MbbDeviceSetWakeCapabilities
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - mbbcxstub.lib
api_name:
 - MbbDeviceSetWakeCapabilities
product:
 - Windows
---

# MbbDeviceSetWakeCapabilities function


## -description

The **MbbDeviceSetWakeCapabilities** method sets the wake capabilities for a MBBCx device.

## -parameters

### -param Device

The WDFDEVICE object the driver previously obtained from a call to [**WdfDeviceCreate**](../wdfdevice/nf-wdfdevice-wdfdevicecreate.md).

### -param Capabilities

A pointer to a driver-allocated and initialized [**MBB_DEVICE_WAKE_CAPABILITIES**](../mbbcx/ns-mbbcx-_mbb_device_wake_capabilities.md) structure.


## -remarks

The client driver typically calls this method from within [*EVT_DEVICE_PREPARE_HARDWARE*](../wdfdevice/nc-wdfdevice-evt_wdf_device_prepare_hardware.md).

## -see-also

