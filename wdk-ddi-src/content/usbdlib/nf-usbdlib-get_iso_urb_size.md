---
UID: NF:usbdlib.GET_ISO_URB_SIZE
title: GET_ISO_URB_SIZE macro (usbdlib.h)
description: The GET_ISO_URB_SIZE macro returns the number of bytes required to hold an isochronous transfer request.
old-location: buses\get_iso_urb_size.htm
tech.root: usbref
ms.date: 05/07/2018
keywords: ["GET_ISO_URB_SIZE macro"]
ms.keywords: GET_ISO_URB_SIZE, GET_ISO_URB_SIZE macro [Buses], buses.get_iso_urb_size, usbdlib/GET_ISO_URB_SIZE, usbfunc_949a4f14-4bc8-4ba1-821c-f81c6bcec0fa.xml
req.header: usbdlib.h
req.include-header: Usbdlib.h
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
req.typenames: 
f1_keywords:
 - GET_ISO_URB_SIZE
 - usbdlib/GET_ISO_URB_SIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - usbdlib.h
api_name:
 - GET_ISO_URB_SIZE
---

# GET_ISO_URB_SIZE macro


## -description

The <b>GET_ISO_URB_SIZE</b> macro returns the number of bytes required to hold an isochronous transfer request.

## -parameters

### -param n

<p>Specifies the number of isochronous transfer packets that will be part of the transfer request.</p>

## -returns

GET_ISO_URB_SIZE returns the number of bytes required to hold an isochronous request with the given NumberOfPackets.

## -see-also

<a href="/windows/iot-core/learn-about-hardware/hardwarecompatlist">Routines for USB Client Drivers</a>



<a href="/windows-hardware/drivers/ddi/usb/ns-usb-_urb">URB</a>



<a href="/windows-hardware/drivers/ddi/usb/ns-usb-_usbd_iso_packet_descriptor">USBD_ISO_PACKET_DESCRIPTOR</a>



<a href="/windows-hardware/drivers/ddi/usb/ns-usb-_urb_isoch_transfer">_URB_ISOCH_TRANSFER</a>
