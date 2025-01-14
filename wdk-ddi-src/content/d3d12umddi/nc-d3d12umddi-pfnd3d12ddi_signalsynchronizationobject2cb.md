---
UID: NC:d3d12umddi.PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB
title: PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB
description: Inserts a signal for the specified synchronization objects in the specified context stream.
tech.root: display
ms.date: 04/04/2019
keywords: ["PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB callback function"]
req.header: d3d12umddi.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1903
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
ms.custom: UMD DDI Min Version D3D12DDI_SUPPORTED_0021, 19H1
f1_keywords:
 - PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB
 - d3d12umddi/PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - d3d12umddi.h
api_name:
 - PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB
product:
 - Windows
dev_langs:
 - c++
---

# PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB callback function


## -description

Inserts a signal for the specified synchronization objects in the specified context stream.

## -parameters

### -param hDevice

Handle to a device.

### -param unnamedParam2

Pointer to a [D3D12DDICB_SIGNALSYNCHRONIZATIONOBJECT2](ns-d3d12umddi-d3d12ddicb_signalsynchronizationobject2.md) structure.

## -returns

Returns HRESULT.

## -prototype

```
//Declaration

PFND3D12DDI_SIGNALSYNCHRONIZATIONOBJECT2CB Pfnd3d12ddiSignalsynchronizationobject2cb; 

// Definition

HRESULT Pfnd3d12ddiSignalsynchronizationobject2cb 
(
	D3D12DDI_HRTDEVICE hDevice
	 const D3D12DDICB_SIGNALSYNCHRONIZATIONOBJECT2 *
)
{...}

```

## -remarks

## -see-also

