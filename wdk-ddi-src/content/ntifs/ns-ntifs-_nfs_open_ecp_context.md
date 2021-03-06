---
UID: NS:ntifs._NFS_OPEN_ECP_CONTEXT
title: _NFS_OPEN_ECP_CONTEXT (ntifs.h)
description: The NFS_OPEN_ECP_CONTEXT structure is used by the Network File System (NFS) server to open files in response to client requests.
old-location: ifsk\nfs_open_ecp_context.htm
tech.root: ifsk
ms.date: 04/16/2018
keywords: ["NFS_OPEN_ECP_CONTEXT structure"]
ms.keywords: "*PNFS_OPEN_ECP_CONTEXT, ECP_Structures_d19b2618-0b21-424c-b5bd-abc9b6bdc518.xml, NFS_OPEN_ECP_CONTEXT, NFS_OPEN_ECP_CONTEXT structure [Installable File System Drivers], PNFS_OPEN_ECP_CONTEXT, PNFS_OPEN_ECP_CONTEXT structure pointer [Installable File System Drivers], PPNFS_OPEN_ECP_CONTEXT, PPNFS_OPEN_ECP_CONTEXT structure pointer [Installable File System Drivers], _NFS_OPEN_ECP_CONTEXT, ifsk.nfs_open_ecp_context, ntifs/NFS_OPEN_ECP_CONTEXT, ntifs/PNFS_OPEN_ECP_CONTEXT, ntifs/PPNFS_OPEN_ECP_CONTEXT"
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Windows
req.target-min-winverclnt: This structure is available starting with Windows 7.
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
req.typenames: NFS_OPEN_ECP_CONTEXT, *PNFS_OPEN_ECP_CONTEXT, PPNFS_OPEN_ECP_CONTEXT
f1_keywords:
 - _NFS_OPEN_ECP_CONTEXT
 - ntifs/_NFS_OPEN_ECP_CONTEXT
 - PNFS_OPEN_ECP_CONTEXT
 - ntifs/PNFS_OPEN_ECP_CONTEXT
 - NFS_OPEN_ECP_CONTEXT
 - ntifs/NFS_OPEN_ECP_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - _NFS_OPEN_ECP_CONTEXT
 - PNFS_OPEN_ECP_CONTEXT
 - NFS_OPEN_ECP_CONTEXT
---

# _NFS_OPEN_ECP_CONTEXT structure


## -description

The NFS_OPEN_ECP_CONTEXT structure is used by the Network File System (NFS) server to open files in response to client requests.

## -struct-fields

### -field ExportAlias

A pointer to a [UNICODE_STRING](/windows/win32/api/ntdef/ns-ntdef-_unicode_string) structure that supplies the export alias (share name) for the NFS server that contains the files to be opened. This member is a hint and can be a name, **NULL**, or a zero-length string.

### -field ClientSocketAddress

A pointer to a [SOCKADDR_STORAGE](/windows/win32/api/ws2def/ns-ws2def-sockaddr_storage_lh) structure that specifies the transport address of the client computer. This client originates the open file request.

## -remarks

The file-system stack can determine whether NFS_OPEN_ECP_CONTEXT is attached to the create file request. The file-system stack can then use the information in NFS_OPEN_ECP_CONTEXT to determine the client that requested that the file be opened and why it was requested. For information about how to retrieve the NFS_OPEN_ECP_CONTEXT extra information that is attached to a create file request, see [Retrieving ECPs](/windows-hardware/drivers/ifs/using-ecps-to-process-irp-mj-create-operations-in-a-file-system-minifilter).

The NFS_OPEN_ECP_CONTEXT structure is read-only. You should use it to retrieve information about the open file ECP only. For more information about this issue, see [System-Defined ECPs](/windows-hardware/drivers/ifs/system-defined-ecps).

## -see-also

[SOCKADDR_STORAGE](/windows/win32/api/ws2def/ns-ws2def-sockaddr_storage_lh)

[UNICODE_STRING](/windows/win32/api/ntdef/ns-ntdef-_unicode_string)

