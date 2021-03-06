---
UID: NS:hbapiwmi._GetFCPStatistics_OUT
title: _GetFCPStatistics_OUT (hbapiwmi.h)
description: The GetFCPStatistics_OUT structure is used by the miniport driver to report the output parameters of the GetFCPStatistics WMI method.
old-location: storage\getfcpstatistics_out.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["GetFCPStatistics_OUT structure"]
ms.keywords: "*PGetFCPStatistics_OUT, GetFCPStatistics_OUT, GetFCPStatistics_OUT structure [Storage Devices], PGetFCPStatistics_OUT, PGetFCPStatistics_OUT structure pointer [Storage Devices], _GetFCPStatistics_OUT, hbapiwmi/GetFCPStatistics_OUT, hbapiwmi/PGetFCPStatistics_OUT, storage.getfcpstatistics_out, structs-Fibre_cb7a0157-9213-4c4f-adbe-5855d8cca225.xml"
req.header: hbapiwmi.h
req.include-header: Hbapiwmi.h
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
req.typenames: GetFCPStatistics_OUT, *PGetFCPStatistics_OUT
f1_keywords:
 - _GetFCPStatistics_OUT
 - hbapiwmi/_GetFCPStatistics_OUT
 - PGetFCPStatistics_OUT
 - hbapiwmi/PGetFCPStatistics_OUT
 - GetFCPStatistics_OUT
 - hbapiwmi/GetFCPStatistics_OUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - hbapiwmi.h
api_name:
 - _GetFCPStatistics_OUT
 - PGetFCPStatistics_OUT
 - GetFCPStatistics_OUT
---

# _GetFCPStatistics_OUT structure


## -description

The GetFCPStatistics_OUT structure is used by the miniport driver to report the output parameters of the <a href="/windows-hardware/drivers/storage/getfcpstatistics">GetFCPStatistics</a> WMI method.

## -struct-fields

### -field HBAStatus

Contains a value associated with the WMI class qualifier <a href="/windows-hardware/drivers/storage/hba-status">HBA_STATUS</a> that indicates the result of an HBA query operation.

### -field FC4Statistics

Contains a structure of type <a href="/windows-hardware/drivers/ddi/hbapiwmi/ns-hbapiwmi-_msfc_fc4statistics">MSFC_FC4STATISTICS</a> that holds statistics for the specified FC-4 protocol.

## -remarks

The WMI tool suite generates a declaration of the GetFCPStatistics_OUT structure in <i>Hbapiwmi.h </i>when it compiles the <a href="/windows-hardware/drivers/storage/msfc-hbaadaptermethods-wmi-class">MSFC_HBAAdapterMethods WMI Class</a>.

## -see-also

<a href="/windows-hardware/drivers/storage/getfcpstatistics">GetFCPStatistics</a>



<a href="/windows-hardware/drivers/ddi/hbapiwmi/ns-hbapiwmi-_getfcpstatistics_in">GetFCPStatistics_IN</a>

