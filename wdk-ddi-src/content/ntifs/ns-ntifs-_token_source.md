---
UID: NS:ntifs._TOKEN_SOURCE
title: _TOKEN_SOURCE (ntifs.h)
description: TOKEN_SOURCE identifies the source of an access token.
old-location: ifsk\token_source.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["TOKEN_SOURCE structure"]
ms.keywords: "*PTOKEN_SOURCE, PTOKEN_SOURCE, PTOKEN_SOURCE structure pointer [Installable File System Drivers], TOKEN_SOURCE, TOKEN_SOURCE structure [Installable File System Drivers], _TOKEN_SOURCE, ifsk.token_source, ntifs/PTOKEN_SOURCE, ntifs/TOKEN_SOURCE, securitystructures_caf23dc4-0bfe-40e1-9b94-b58bb0eb893e.xml"
req.header: ntifs.h
req.include-header: Ntifs.h
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
req.typenames: TOKEN_SOURCE, *PTOKEN_SOURCE
f1_keywords:
 - _TOKEN_SOURCE
 - ntifs/_TOKEN_SOURCE
 - PTOKEN_SOURCE
 - ntifs/PTOKEN_SOURCE
 - TOKEN_SOURCE
 - ntifs/TOKEN_SOURCE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - _TOKEN_SOURCE
 - PTOKEN_SOURCE
 - TOKEN_SOURCE
---

# _TOKEN_SOURCE structure


## -description

TOKEN_SOURCE identifies the source of an access token.

## -struct-fields

### -field SourceName

Specifies an 8-byte character string used to identify the source of an access token. This is used to distinguish between such sources as Session Manager, LAN Manager, and RPC Server. A string, rather than a constant, is used to identify the source so users and developers can make extensions to the system, such as by adding other networks, that act as the source of access tokens. Note that TOKEN_SOURCE_LENGTH currently equals 8.

### -field SourceIdentifier

Specifies a locally unique identifier (LUID) provided by the source component named by the <b>SourceName</b> member. This value aids the source component in relating context blocks, such as session-control structures, to the token. This value is typically, but not necessarily, an LUID.

## -see-also

<a href="/windows-hardware/drivers/ddi/igpupvdev/ns-igpupvdev-_luid">LUID</a>



<a href="/windows-hardware/drivers/ddi/ntifs/nf-ntifs-sequeryinformationtoken">SeQueryInformationToken</a>



<a href="/windows-hardware/drivers/ddi/ntifs/ne-ntifs-_token_information_class">TOKEN_INFORMATION_CLASS</a>



<a href="/previous-versions/ff567055(v=vs.85)">ZwQueryInformationToken</a>



<a href="/previous-versions/ff567102(v=vs.85)">ZwSetInformationToken</a>

