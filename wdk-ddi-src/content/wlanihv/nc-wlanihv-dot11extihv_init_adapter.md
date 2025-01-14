---
UID: NC:wlanihv.DOT11EXTIHV_INIT_ADAPTER
title: DOT11EXTIHV_INIT_ADAPTER (wlanihv.h)
description: The DOT11EXTIHV_INIT_ADAPTER callback function is part of the Native 802.11 Wireless LAN interface, which is deprecated for Windows 10 and later.
old-location: netvista\dot11extihvinitadapter.htm
tech.root: netvista
ms.date: 02/16/2018
keywords: ["DOT11EXTIHV_INIT_ADAPTER callback"]
ms.keywords: DOT11EXTIHV_INIT_ADAPTER, Dot11ExtIhvInitAdapter, Dot11ExtIhvInitAdapter callback function [Network Drivers Starting with Windows Vista], Native_802.11_IHV_Ext_c2fbb863-6b05-4444-90f1-37f375db9b9e.xml, netvista.dot11extihvinitadapter, wlanihv/Dot11ExtIhvInitAdapter
req.header: wlanihv.h
req.include-header: Wlanihv.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
req.typenames: DRIVER_INFO_8W, *PDRIVER_INFO_8W, *LPDRIVER_INFO_8W
req.product: Windows 10 or later.
f1_keywords:
 - DOT11EXTIHV_INIT_ADAPTER
 - wlanihv/DOT11EXTIHV_INIT_ADAPTER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wlanihv.h
api_name:
 - DOT11EXTIHV_INIT_ADAPTER
---

# DOT11EXTIHV_INIT_ADAPTER callback


## -description

<div class="alert"><b>Important</b>  The <a href="/previous-versions/windows/hardware/wireless/ff560689(v=vs.85)">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="/windows-hardware/drivers/network/wifi-universal-driver-model">WLAN Universal Windows driver model</a>.</div><div> </div>The operating system calls the
  <i>Dot11ExtIhvInitAdapter</i> function to have the IHV Extensions DLL allocate and initialize an adapter
  context.

## -parameters

### -param pDot11Adapter [in]


A pointer to a
     <a href="..\wlclient\ns-wlclient-_dot11_adapter.md">DOT11_ADAPTER</a> structure, which identifies the
     adapter to be initialized.

### -param hDot11SvcHandle [in, optional]


A handle assigned by the operating system for the adapter. The IHV Extensions DLL must use this
     handle value when calling any IHV Extensibility function that declares an
     <i>hDot11SvcHandle</i> parameter, such as
     <a href="..\wlanihv\nc-wlanihv-dot11ext_pre_associate_completion.md">
     Dot11ExtPreAssociateCompletion</a>.

### -param phIhvExtAdapter [out]


A pointer to a handle variable. The IHV Extensions DLL must assign a unique handle value for the
     adapter and set *
     <i>phIhvExtAdapter</i> to the handle value. The operating system uses this handle value when it calls any
     IHV Handler function that declares an
     <i>hIhvExtAdapter</i> parameter, such as
     <a href="..\wlanihv\nc-wlanihv-dot11extihv_perform_pre_associate.md">
     Dot11ExtIhvPerformPreAssociate</a>.


Typically, the IHV Extensions DLL allocates a state array for the adapter context and returns the
     address of the array as the handle value.

## -returns

If the call succeeds, the function returns ERROR_SUCCESS. Otherwise, it returns an error code
     defined in
     Winerror.h.

## -prototype

```cpp
DOT11EXTIHV_INIT_ADAPTER Dot11ExtIhvInitAdapter;

DWORD APIENTRY Dot11ExtIhvInitAdapter(
  _In_     PDOT11_ADAPTER pDot11Adapter,
  _In_opt_ HANDLE         hDot11SvcHandle,
  _Out_    PHANDLE        phIhvExtAdapter
)
{ ... }
```

## -remarks

The operating system calls the
    <i>Dot11ExtIhvInitAdapter</i> function whenever a WLAN adapter becomes available and enabled for use, such
    as when a PCMCIA adapter is inserted.

For more information about WLAN adapter initialization, see
    <a href="/windows/win32/api/l2cmn/ns-l2cmn-l2_notification_data">802.11 WLAN Adapter Arrival</a>.

## -see-also

<a href="/windows-hardware/drivers/network/native-802-11-ihv-extensibility-functions">Native 802.11 IHV
   Extensibility Functions</a>



<a href="..\wlanihv\nc-wlanihv-dot11ext_pre_associate_completion.md">
   Dot11ExtPreAssociateCompletion</a>



<a href="..\wlanihv\nc-wlanihv-dot11extihv_perform_pre_associate.md">
   Dot11ExtIhvPerformPreAssociate</a>



<a href="..\wlclient\ns-wlclient-_dot11_adapter.md">DOT11_ADAPTER</a>

