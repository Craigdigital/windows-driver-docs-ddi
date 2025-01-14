---
UID: NF:sensorsutils.PropVariantGetInformation
title: PropVariantGetInformation function (sensorsutils.h)
description: This routine gets offset, size, location pointer and DEVPROPTYPE, of a PROPVARIANT.
ms.date: 08/08/2018
keywords: ["PropVariantGetInformation function"]
tech.root: sensors
ms.keywords: PropVariantGetInformation
req.header: sensorsutils.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
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
ms.custom: RS5
f1_keywords:
 - PropVariantGetInformation
 - sensorsutils/PropVariantGetInformation
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - sensorsutils.h
api_name:
 - PropVariantGetInformation
product:
 - Windows
---

# PropVariantGetInformation function


## -description

This routine gets offset, size, location pointer and DEVPROPTYPE, of a PROPVARIANT.

## -parameters

### -param PropVariantValue [in]

Pointer to a PROPVARIANT.

### -param PropVariantOffset [out]

The offset of the location pointer in PROPVARIANT.

### -param PropVariantSize [out]

Size of data.

### -param PropVariantPointer [out]

C
The location of data.

### -param RemappedType [out]

The DEVPROPTYPE.

## -returns

This function returns STATUS_NOT_SUPPORTED if the PROPVARIANT is not a supported type, STATUS_SUCCESS otherwise.

## -remarks

## -see-also

