---
UID: NF:storport.StorPortFreeDmaMemory
title: StorPortFreeDmaMemory function (storport.h)
description: This function is the extended version of the StorPortFreeContiguousMemorySpecifyCache function. It deallocates a range of noncached memory in the nonpaged portion of the system address space.
tech.root: storage
ms.date: 10/19/2018
keywords: ["StorPortFreeDmaMemory function"]
ms.keywords: StorPortFreeDmaMemory
req.header: storport.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Windows 10 (Version 1803)
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
f1_keywords:
 - StorPortFreeDmaMemory
 - storport/StorPortFreeDmaMemory
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - StorPortFreeDmaMemory
---

# StorPortFreeDmaMemory function


## -description

This function is the extended version of the [StorPortFreeContiguousMemorySpecifyCache function](./nf-storport-storportfreecontiguousmemoryspecifycache.md). It deallocates a range of noncached memory in the nonpaged portion of the system address space.

## -parameters

### -param HwDeviceExtension [in]


A pointer to the hardware device extension for the host bus adapter (HBA).

### -param BaseAddress [in]


The base virtual address to free.

### -param NumberOfBytes [in]


The number of bytes that are allocated to the request. This must be the same number that was supplied as a parameter when the [StorPortAllocateContiguousMemorySpecifyCacheNode](./nf-storport-storportallocatecontiguousmemoryspecifycachenode.md) routine was previously called.

### -param CacheType [in]


The cache type that is used in the call to the [StorPortAllocateContiguousMemorySpecifyCacheNode](./nf-storport-storportallocatecontiguousmemoryspecifycachenode.md) routine.

## -returns

This function returns one of the following status codes:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STOR_STATUS_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not implemented on the active operating system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STOR_STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
</table>

## -see-also

<a href="/windows-hardware/drivers/ddi/storport/nf-storport-storportallocatecontiguousmemoryspecifycachenode">StorPortAllocateContiguousMemorySpecifyCacheNode</a>
