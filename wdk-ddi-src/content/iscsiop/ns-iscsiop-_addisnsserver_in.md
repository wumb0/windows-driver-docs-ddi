---
UID: NS:iscsiop._AddiSNSServer_IN
title: _AddiSNSServer_IN (iscsiop.h)
description: The AddiSNSServer_IN structure holds the input data for the user-mode AddISNSServer method, which is used to add a new iSNS server entry to the list of iSNS server names that the initiator maintains.
old-location: storage\addisnsserver_in.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["AddiSNSServer_IN structure"]
ms.keywords: "*PAddiSNSServer_IN, AddiSNSServer_IN, AddiSNSServer_IN structure [Storage Devices], PAddiSNSServer_IN, PAddiSNSServer_IN structure pointer [Storage Devices], _AddiSNSServer_IN, iscsiop/AddiSNSServer_IN, iscsiop/PAddiSNSServer_IN, storage.addisnsserver_in, structs-iSCSI_2c317c93-3fea-4749-98ef-fba28c0cc93f.xml"
req.header: iscsiop.h
req.include-header: Iscsiop.h
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
req.typenames: AddiSNSServer_IN, *PAddiSNSServer_IN
f1_keywords:
 - _AddiSNSServer_IN
 - iscsiop/_AddiSNSServer_IN
 - PAddiSNSServer_IN
 - iscsiop/PAddiSNSServer_IN
 - AddiSNSServer_IN
 - iscsiop/AddiSNSServer_IN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iscsiop.h
api_name:
 - _AddiSNSServer_IN
 - PAddiSNSServer_IN
 - AddiSNSServer_IN
---

# _AddiSNSServer_IN structure


## -description

The AddiSNSServer_IN structure holds the input data for the user-mode <b>AddISNSServer</b> method, which is used to add a new iSNS server entry to the list of iSNS server names that the initiator maintains.

## -struct-fields

### -field iSNSServerName

The iSNS server name to add to the list of iSNS servers that the iSCSI initiator maintains.

## -remarks

It is optional that you implement this method.

## -see-also

<a href="/windows-hardware/drivers/ddi/iscsiop/ns-iscsiop-_addisnsserver_out">AddiSNSServer_OUT</a>



<a href="/windows-hardware/drivers/storage/msiscsi-operations-wmi-class">MSiSCSI_Operations WMI Class</a>

