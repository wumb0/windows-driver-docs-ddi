---
UID: NS:dispmprt._DXGKARG_GETBACKINGRESOURCE
title: _DXGKARG_GETBACKINGRESOURCE (dispmprt.h)
description: Arguments used to get backing resources for the virtual device MMIO (memory mapped input output) bars.
ms.date: 10/19/2018
keywords: ["DXGKARG_GETBACKINGRESOURCE structure"]
ms.keywords: _DXGKARG_GETBACKINGRESOURCE, DXGKARG_GETBACKINGRESOURCE, *PDXGKARG_GETBACKINGRESOURCE,
req.header: dispmprt.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1809
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: DXGKARG_GETBACKINGRESOURCE, *PDXGKARG_GETBACKINGRESOURCE
targetos: Windows
tech.root: display
ms.custom: RS5
f1_keywords:
 - _DXGKARG_GETBACKINGRESOURCE
 - dispmprt/_DXGKARG_GETBACKINGRESOURCE
 - PDXGKARG_GETBACKINGRESOURCE
 - dispmprt/PDXGKARG_GETBACKINGRESOURCE
 - DXGKARG_GETBACKINGRESOURCE
 - dispmprt/DXGKARG_GETBACKINGRESOURCE
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dispmprt.h
api_name:
 - _DXGKARG_GETBACKINGRESOURCE
 - PDXGKARG_GETBACKINGRESOURCE
 - DXGKARG_GETBACKINGRESOURCE
dev_langs:
 - c++
---

# _DXGKARG_GETBACKINGRESOURCE structure


## -description

Arguments used to get backing resources for the virtual device MMIO (memory mapped input output) bars.

## -struct-fields

### -field VirtualFunctionIndex

The particular Virtual function to query security.

### -field ResourceIndex

The resource index.

### -field Resource

The return resource descriptor, containing the host base address and resource length.

### -field pMdl

 
Pointer to an MDL (memory descriptor list). 

Alternative to returning a Resource, the driver can return an already created MDL to use as a backing resource. Any MDL returned must point to contiguous physical RAM or MMIO space, with no offset into the first page, along with a length divisible by PAGE_SIZE.

## -remarks

Note that the backing resource is currently limited to MAX_FLEXIO_RESOURCES (32) ranges. These resources are then used by the scatter/gather mechanism present in the MMIO mappings to build up full guest bars. If a physical device does not use a resource at a specific Index, the device should set all return values and return STATUS_SUCCESS.

## -see-also

