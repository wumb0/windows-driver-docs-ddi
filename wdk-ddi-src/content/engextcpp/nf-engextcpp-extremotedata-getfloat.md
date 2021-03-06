---
UID: NF:engextcpp.ExtRemoteData.GetFloat
title: ExtRemoteData::GetFloat (engextcpp.h)
description: The GetFloat method returns a float version of the ExtRemoteData object, which represents the contents of the target's memory.
old-location: debugger\extremotedata_getfloat.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["ExtRemoteData::GetFloat"]
ms.keywords: EngExtCpp_Ref_f1ca75e4-6dea-4237-b76a-04b3af234060.xml, ExtRemoteData class [Windows Debugging],GetFloat method, ExtRemoteData.GetFloat, ExtRemoteData::GetFloat, GetFloat, GetFloat method [Windows Debugging], GetFloat method [Windows Debugging],ExtRemoteData class, debugger.extremotedata_getfloat
req.header: engextcpp.hpp
req.include-header: Engextcpp.hpp
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
 - ExtRemoteData::GetFloat
 - engextcpp/ExtRemoteData::GetFloat
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - engextcpp.hpp
api_name:
 - ExtRemoteData::GetFloat
---

# ExtRemoteData::GetFloat


## -description

The <b>GetFloat</b> method returns a <b>float</b> version of the <a href="/windows-hardware/drivers/ddi/engextcpp/nf-engextcpp-extremotedata-extremotedata(pcstr_ulong64_ulong)">ExtRemoteData</a> object, which represents the contents of the target's memory.

## -returns

<b>GetFloat</b> returns the <b>float</b> version of the <a href="/windows-hardware/drivers/ddi/engextcpp/nf-engextcpp-extremotedata-extremotedata(pcstr_ulong64_ulong)">ExtRemoteData</a> object.

## -remarks

The size of the memory represented by the <a href="/windows-hardware/drivers/ddi/engextcpp/nf-engextcpp-extremotedata-extremotedata(pcstr_ulong64_ulong)">ExtRemoteData</a> object must be <code>sizeof(float)</code>.

## -see-also

<a href="/windows-hardware/drivers/ddi/engextcpp/nf-engextcpp-extremotedata-extremotedata(pcstr_ulong64_ulong)">ExtRemoteData</a>



<a href="/windows-hardware/drivers/ddi/engextcpp/nf-engextcpp-extremotedata-getdata">ExtRemoteData::GetData</a>



<a href="/windows-hardware/drivers/ddi/engextcpp/nf-engextcpp-extremotedata-getdouble">ExtRemoteData::GetDouble</a>

