---
UID: NF:wudfddi.IWDFCmResourceList.GetCount
title: IWDFCmResourceList::GetCount (wudfddi.h)
description: The GetCount method returns the number of resource descriptors that are contained in this interface's resource list.
old-location: wdf\iwdfcmresourcelist_getcount.htm
tech.root: wdf
ms.date: 02/26/2018
keywords: ["IWDFCmResourceList::GetCount"]
ms.keywords: GetCount, GetCount method, GetCount method,IWDFCmResourceList interface, IWDFCmResourceList interface,GetCount method, IWDFCmResourceList.GetCount, IWDFCmResourceList::GetCount, umdf.iwdfcmresourcelist_getcount, wdf.iwdfcmresourcelist_getcount, wudfddi/IWDFCmResourceList::GetCount
req.header: wudfddi.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.11
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IWDFCmResourceList::GetCount
 - wudfddi/IWDFCmResourceList::GetCount
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WUDFx.dll
api_name:
 - IWDFCmResourceList::GetCount
---

# IWDFCmResourceList::GetCount


## -description

<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]


The <b>GetCount</b> method returns the number of resource descriptors that are contained in this interface's resource list.

## -returns

<b>GetCount</b> returns the number of resource descriptors that are contained in this interface's resource list.

## -remarks

Typically, a UMDF driver calls the <b>GetCount</b> method from its <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-ipnpcallbackhardware2-onpreparehardware">OnPrepareHardware</a> method. For more information about parsing hardware resources, see <a href="/windows-hardware/drivers/wdf/finding-and-mapping-hardware-resources-in-umdf-1-x-drivers">Finding and Mapping Hardware Resources in a UMDF Driver</a>.


#### Examples

See example code in <a href="/windows-hardware/drivers/ddi/wudfddi/nf-wudfddi-iwdfdevice3-mapiospace">IWDFDevice3::MapIoSpace</a>.

<div class="code"></div>

## -see-also

<a href="/windows-hardware/drivers/ddi/wudfddi/nn-wudfddi-iwdfcmresourcelist">IWDFCmResourceList</a>

