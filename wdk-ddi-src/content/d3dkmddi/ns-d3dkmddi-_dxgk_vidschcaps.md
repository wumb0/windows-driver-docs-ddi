---
UID: NS:d3dkmddi._DXGK_VIDSCHCAPS
title: _DXGK_VIDSCHCAPS (d3dkmddi.h)
description: The DXGK_VIDSCHCAPS structure identifies the graphics processing unit (GPU) scheduling capabilities, in bit-field flags, that a driver can support.
old-location: display\dxgk_vidschcaps.htm
ms.date: 05/10/2018
keywords: ["DXGK_VIDSCHCAPS structure"]
ms.keywords: DXGK_VIDSCHCAPS, DXGK_VIDSCHCAPS structure [Display Devices], DmStructs_01f721e4-8585-46b1-a911-9fa904a29f7e.xml, _DXGK_VIDSCHCAPS, d3dkmddi/DXGK_VIDSCHCAPS, display.dxgk_vidschcaps
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Windows
req.target-min-winverclnt: Available beginning with Windows Vista.
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
tech.root: display
req.typenames: DXGK_VIDSCHCAPS
f1_keywords:
 - _DXGK_VIDSCHCAPS
 - d3dkmddi/_DXGK_VIDSCHCAPS
 - DXGK_VIDSCHCAPS
 - d3dkmddi/DXGK_VIDSCHCAPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dkmddi.h
api_name:
 - _DXGK_VIDSCHCAPS
 - DXGK_VIDSCHCAPS
---

# _DXGK_VIDSCHCAPS structure


## -description

The DXGK_VIDSCHCAPS structure identifies the graphics processing unit (GPU) scheduling capabilities, in bit-field flags, that a driver can support.

## -struct-fields

### -field MultiEngineAware

A UINT value that specifies whether the driver supports the creation and destruction of a device context (through the [**DxgkDdiCreateContext**](./nc-d3dkmddi-dxgkddi_createcontext.md) and [**DxgkDdiDestroyContext**](./nc-d3dkmddi-dxgkddi_destroycontext.md) functions) and the use of a device context (through the [**DxgkDdiPresent**](./nc-d3dkmddi-dxgkddi_present.md) and [**DxgkDdiRender**](./nc-d3dkmddi-dxgkddi_render.md) functions). If the driver does not support context creation, for every call to the driver that would pass a handle to a context, the Microsoft DirectX graphics kernel subsystem replaces the handle to the context with a handle to the device.

Setting this member is equivalent to setting the first bit of the 32-bit **Value** member (0x00000001).

### -field VSyncPowerSaveAware

A UINT value that specifies whether the driver supports vertical-sync power-saving functionality.

If **VSyncPowerSaveAware** is set to 1 (**TRUE**), the operating system can save power by disabling and enabling the vertical-sync interrupt that occurs from the usage of some applications. If **VSyncPowerSaveAware** is set to zero (**FALSE**), the operating system will never disable the vertical-sync interrupt for applications that might cause the vertical-sync interrupt to occur.

Setting this member is equivalent to setting the second bit of the 32-bit **Value** member (0x00000002).

Supported starting with Windows Server 2008 and Windows Vista with SP1.

### -field PreemptionAware

A UINT value that specifies whether the driver supports the   GPU preemption policy of Windows 8 and later versions of Windows. With this policy, the operating system always issues preemption requests to the GPU before it initiates the [**Timeout Detection and Recovery
(TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery) process.

If **PreemptionAware** is set to 1 (**TRUE**), the driver supports the preemption policy of Windows 8 and later versions of Windows.

If **PreemptionAware** is set to zero (**FALSE**), the driver supports the preemption policy  of Windows 7. With this policy, the operating system may not issue preemption requests while potentially long running operations are being executed on the GPU. As a result, these GPU requests are not preempted  before the TDR process is initiated. This may cause the TDR process to repeatedly reset the GPU which could lead to a system stop error.

> [!NOTE]
> If **PreemptionAware** is set to 1, the **MultiEngineAware** member  must also be set to a value of 1. If **PreemptionAware** is set to 1 but **MultiEngineAware** is set to zero, the operating system will halt the driver initialization process and return a failure code.

Setting this member is equivalent to setting the third bit of the 32-bit **Value** member (0x00000004).

Supported starting with Windows 8.

### -field NoDmaPatching

A UINT value that specifies whether the driver disables leak detection for DMA buffers that are split into multiple parts. This detection is performed after the driver's [**DxgkDdiPatch**](./nc-d3dkmddi-dxgkddi_patch.md) function is called to assign, or *patch*, physical addresses to each part of the DMA buffer.

> [!NOTE]
> Display devices that support virtual addresses can reprogram a virtual address to a new video memory location without having to patch the value of the DMA buffer address. For these types of display devices, the driver should set **NoDmaPatching** to 1.

If **NoDmaPatching** is set to 1 (**TRUE**), the driver disables leak detection, and the behavior of DMA buffer splitting is the same as in Windows 7.

If **NoDmaPatching** is set to 0 (**FALSE**), the driver enables leak detection for patched DMA buffer addresses. The operating system performs leak detection before it calls the driver's [**DxgkDdiPatch**](./nc-d3dkmddi-dxgkddi_patch.md) function.

> [!NOTE]
> If **NoDmaPatching** is set to 1, the **PreemptionAware** and **MultiEngineAware** members  must also be set to a value of 1. If **NoDmaPatching** is set to 1 but **PreemptionAware** or **MultiEngineAware** are set to zero, the operating system will halt the driver initialization process and return a failure code.

Setting this member is equivalent to setting the fourth bit of the 32-bit **Value** member (0x0000008).

Supported starting with Windows 8.

### -field CancelCommandAware

A UINT value that specifies whether the driver supports cleaning up internal resources (through the [**DxgkDdiCancelCommand**](./nc-d3dkmddi-dxgkddi_cancelcommand.md) function) after a command is removed from the hardware queue.

If **CancelCommandAware** is set to 1 (**TRUE**), the driver supports cleaning up resources associated with a canceled DMA packet. If **CancelCommandAware** is set to zero (**FALSE**), the driver does not support cleaning up resources.

> [!NOTE]
> If **CancelCommandAware** is set to 1, the **MultiEngineAware** member  must also be set to a value of 1. If **CancelCommandAware** is set to 1 but **MultiEngineAware** is set to zero, the operating system returns a failure code.

Setting this member is equivalent to setting the fifth bit of the 32-bit **Value** member (0x0000010).

Supported starting with Windows 8.

### -field No64BitAtomics

|Value|Meaning|
|--- |--- |
|TRUE|Indicates a GPU is capable of only updating 32 bit values atomically. In this case, the OS will handle the fence wraparound case automatically, however it will place a restriction that an outstanding wait and signal fence values cannot be more than UINT_MAX/2 apart from the last signaled fence value.|
|FALSE|Indicates a GPU is capable of updating 64 bit values atomically as visible by the CPU.|

Supported starting with Windows 10.

### -field LowIrqlPreemptCommand

### -field HwQueuePacketCap

Maximum number of DMA packets allowed to be queued to a node.

### -field Reserved

This member is reserved and should be set to zero.

### -field Value

A member in the union that **DXGK_VIDSCHCAPS** contains that can hold a 32-bit value that identifies the GPU scheduling capabilities that the driver can support.

## -see-also

[**DXGK_DRIVERCAPS**](./ns-d3dkmddi-_dxgk_drivercaps.md)

[**DxgkDdiCancelCommand**](./nc-d3dkmddi-dxgkddi_cancelcommand.md)

[**DxgkDdiCreateContext**](./nc-d3dkmddi-dxgkddi_createcontext.md)

[**DxgkDdiDestroyContext**](./nc-d3dkmddi-dxgkddi_destroycontext.md)

[**DxgkDdiPatch**](./nc-d3dkmddi-dxgkddi_patch.md)

[**DxgkDdiPresent**](./nc-d3dkmddi-dxgkddi_present.md)

[**DxgkDdiRender**](./nc-d3dkmddi-dxgkddi_render.md)

