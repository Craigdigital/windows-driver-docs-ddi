---
UID: NF:ntifs.CcCanIWrite
title: CcCanIWrite function (ntifs.h)
description: The CcCanIWrite routine determines whether the caller can write to a cached file.
old-location: ifsk\cccaniwrite.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["CcCanIWrite function"]
ms.keywords: CcCanIWrite, CcCanIWrite routine [Installable File System Drivers], ccref_b964dbf1-d1ad-4929-ab9c-21b1e6f69077.xml, ifsk.cccaniwrite, ntifs/CcCanIWrite
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - CcCanIWrite
 - ntifs/CcCanIWrite
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - CcCanIWrite
---

# CcCanIWrite function


## -description

The <b>CcCanIWrite</b> routine determines whether the caller can write to a cached file.

## -parameters

### -param FileObject [in]


Pointer to a file object for the cached file.

### -param BytesToWrite [in]


Number of bytes to be written.

### -param Wait [in]


Set to <b>TRUE</b> if the caller can be put into a wait state until it can write to the cached file, <b>FALSE</b> otherwise.

### -param Retrying [in]


Set to <b>FALSE</b> if this is the first time <b>CcCanIWrite</b> is being called for this write request, <b>TRUE</b> otherwise.

## -returns

<b>CcCanIWrite</b> returns <b>TRUE</b> if the cache manager can accept the write request, <b>FALSE</b> otherwise.

## -remarks

<b>CcCanIWrite</b> should be called before calling <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-cccopywrite">CcCopyWrite</a> or <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccfastcopywrite">CcFastCopyWrite</a>.

If <b>CcCanIWrite</b> returns <b>TRUE</b>, the caller can immediately call <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-cccopywrite">CcCopyWrite</a> or <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccfastcopywrite">CcFastCopyWrite</a>.

If <b>CcCanIWrite</b> returns <b>FALSE</b>, the caller must instead call <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccdeferwrite">CcDeferWrite</a> to defer the write request.

Generally speaking, the cache manager can accept a write request if the following conditions are true:

<ul>
<li>
The amount of data to be written is not too large.

</li>
<li>
There is enough memory to perform the write operation.

</li>
<li>
The number of dirty pages in the system cache does not exceed the dirty page threshold (CcDirtyPageThreshold).

</li>
<li>
If a per-file dirty page threshold exists for this file, it is not exceeded by the number of dirty pages for this file in the system cache.

</li>
</ul>
To cache a file, use <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccinitializecachemap">CcInitializeCacheMap</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-cccopywrite">CcCopyWrite</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccdeferwrite">CcDeferWrite</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccfastcopywrite">CcFastCopyWrite</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccinitializecachemap">CcInitializeCacheMap</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ccsetdirtypagethreshold">CcSetDirtyPageThreshold</a>
