---
UID: NF:printerextension.IPrintSchemaTicket.GetCapabilities
title: IPrintSchemaTicket::GetCapabilities (printerextension.h)
description: Gets an IPrintSchemaCapabilities object that represents the printer capabilities based on the current settings of this IPrintSchemaTicket object.
old-location: print\iprintschematicket_getcapabilities.htm
tech.root: print
ms.date: 04/20/2018
keywords: ["IPrintSchemaTicket::GetCapabilities"]
ms.keywords: GetCapabilities, GetCapabilities method [Print Devices], GetCapabilities method [Print Devices],IPrintSchemaTicket interface, IPrintSchemaTicket, IPrintSchemaTicket interface [Print Devices],GetCapabilities method, IPrintSchemaTicket.GetCapabilities, IPrintSchemaTicket::GetCapabilities, print.iprintschematicket_getcapabilities, printerextension/IPrintSchemaTicket::GetCapabilities
req.header: printerextension.h
req.include-header: 
req.target-type: Desktop
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
 - IPrintSchemaTicket::GetCapabilities
 - printerextension/IPrintSchemaTicket::GetCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - printerextension.h
api_name:
 - IPrintSchemaTicket::GetCapabilities
---

# IPrintSchemaTicket::GetCapabilities


## -description

Gets an <a href="/windows-hardware/drivers/ddi/printerextension/nn-printerextension-iprintschemacapabilities">IPrintSchemaCapabilities</a> object that represents the printer capabilities based on the current settings of this <a href="/windows-hardware/drivers/ddi/printerextension/nn-printerextension-iprintschematicket">IPrintSchemaTicket</a> object.

## -parameters

### -param ppCapabilities

### -param ppPrintCapabilities [out, retval]

The returned <a href="/windows-hardware/drivers/ddi/printerextension/nn-printerextension-iprintschemacapabilities">IPrintSchemaCapabilities</a> object.

## -returns

This method returns an <b>HRESULT</b> value.

## -remarks

Because this method retrieves a new PrintCapabilities document every time it is invoked, it is recommended that you invoke this method only when the <a href="/windows-hardware/drivers/ddi/printerextension/nn-printerextension-iprintschematicket">IPrintSchemaTicket</a> object has been modified.

## -see-also

<a href="/windows-hardware/drivers/ddi/printerextension/nn-printerextension-iprintschemacapabilities">IPrintSchemaCapabilities</a>



<a href="/windows-hardware/drivers/ddi/printerextension/nf-printerextension-iprintschemaelement-get_xmlnode">IPrintSchemaElement::XmlNode</a>



<a href="/windows-hardware/drivers/ddi/printerextension/nf-printerextension-iprintschemafeature-get_selectedoption">IPrintSchemaFeature::SelectedOption</a>



<a href="/windows-hardware/drivers/ddi/printerextension/nn-printerextension-iprintschematicket">IPrintSchemaTicket</a>



<a href="/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize">IPrintSchemaTicket::put_JobCopiesAllDocuments</a>

