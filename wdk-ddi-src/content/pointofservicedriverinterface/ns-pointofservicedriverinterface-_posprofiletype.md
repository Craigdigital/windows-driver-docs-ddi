---
UID: NS:pointofservicedriverinterface._PosProfileType
title: _PosProfileType (pointofservicedriverinterface.h)
description: This structure describes the number of profile strings in a buffer.
old-location: pos\posprofiletype.htm
tech.root: pos
ms.date: 02/23/2018
keywords: ["PosProfileType structure"]
ms.keywords: PosProfileType, PosProfileType structure, _PosProfileType, pointofservicedriverinterface/PosProfileType, pos.posprofiletype
req.header: pointofservicedriverinterface.h
req.include-header: PointOfServiceDriverInterface.h
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
req.typenames: PosProfileType
f1_keywords:
 - _PosProfileType
 - pointofservicedriverinterface/_PosProfileType
 - PosProfileType
 - pointofservicedriverinterface/PosProfileType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - PointOfServiceDriverInterface.h
api_name:
 - _PosProfileType
 - PosProfileType
---

# _PosProfileType structure


## -description

This structure describes the number of profile strings in a buffer.

## -struct-fields

### -field BufferSize

### -field ProfileCount

 




### -field DataLength

The size in bytes of the buffer that follows this **PosProfileType**, including the size of the **PosProfileType** structure.


### -field EntryCount

Indicates the number of statistics that follow this header.

## -remarks

The buffer of profile *PosStringType* strings follows this structure in memory.

