---
UID: NF:ntifs.FsRtlFreeFileLock
title: FsRtlFreeFileLock function (ntifs.h)
description: The FsRtlFreeFileLock routine uninitializes and frees a file lock structure.
old-location: ifsk\fsrtlfreefilelock.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["FsRtlFreeFileLock function"]
ms.keywords: FsRtlFreeFileLock, FsRtlFreeFileLock routine [Installable File System Drivers], fsrtlref_112afa00-3370-4671-ad22-0743f8dd1c52.xml, ifsk.fsrtlfreefilelock, ntifs/FsRtlFreeFileLock
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: This routine is available on Microsoft Windows 2000 and later.
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
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - FsRtlFreeFileLock
 - ntifs/FsRtlFreeFileLock
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - FsRtlFreeFileLock
---

# FsRtlFreeFileLock function


## -description

The <b>FsRtlFreeFileLock</b> routine uninitializes and frees a file lock structure.

## -parameters

### -param FileLock [in]


Pointer to the FILE_LOCK structure. This structure must have been allocated by a previous call to <b>FsRtlAllocateFileLock</b>.

## -remarks

<b>FsRtlFreeFileLock</b> should be used only for file locks that were allocated and initialized by <b>FsRtlAllocateFileLock</b>.

It is a programming error to call <b>FsRtlFreeFileLock</b> for a FILE_LOCK structure that has already been uninitialized by a call to <a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtluninitializefilelock">FsRtlUninitializeFileLock</a>.

Minifilters must call <a href="/windows-hardware/drivers/ddi/fltkernel/nf-fltkernel-fltfreefilelock">FltFreeFileLock</a> instead of <b>FsRtlFreeFileLock</b>.

## -see-also

<a href="/windows-hardware/drivers/ddi/fltkernel/nf-fltkernel-fltfreefilelock">FltFreeFileLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlaretherecurrentfilelocks">FsRtlAreThereCurrentFileLocks</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlchecklockforreadaccess">FsRtlCheckLockForReadAccess</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlchecklockforwriteaccess">FsRtlCheckLockForWriteAccess</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlfastchecklockforread">FsRtlFastCheckLockForRead</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlfastchecklockforwrite">FsRtlFastCheckLockForWrite</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-fsrtlfastlock">FsRtlFastLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlfastunlockall">FsRtlFastUnlockAll</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlfastunlockallbykey">FsRtlFastUnlockAllByKey</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlfastunlocksingle">FsRtlFastUnlockSingle</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlgetnextfilelock">FsRtlGetNextFileLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlinitializefilelock">FsRtlInitializeFileLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlprocessfilelock">FsRtlProcessFileLock</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-_fsrtl_advanced_fcb_header-fsrtluninitializefilelock">FsRtlUninitializeFileLock</a>
