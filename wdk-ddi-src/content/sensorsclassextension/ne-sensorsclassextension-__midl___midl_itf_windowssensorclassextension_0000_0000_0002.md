---
UID: NE:sensorsclassextension.__MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002
title: __MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002 (sensorsclassextension.h)
description: The SensorConnectionType enumeration type defines values for the SENSOR_CONNECTION_TYPE property.
old-location: sensors\sensorconnectiontype.htm
tech.root: sensors
ms.date: 05/03/2018
keywords: ["_MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002 enumeration"]
ms.keywords: SENSOR_CONNECTION_TYPE_PC_ATTACHED, SENSOR_CONNECTION_TYPE_PC_EXTERNAL, SENSOR_CONNECTION_TYPE_PC_INTEGRATED, SensorConnectionType, SensorConnectionType enumeration [Sensor Devices], Sensor_Enums_bca4556b-94f3-4213-9daa-3571f403d556.xml, __MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002, sensors.sensorconnectiontype, sensorsclassextension/SENSOR_CONNECTION_TYPE_PC_ATTACHED, sensorsclassextension/SENSOR_CONNECTION_TYPE_PC_EXTERNAL, sensorsclassextension/SENSOR_CONNECTION_TYPE_PC_INTEGRATED, sensorsclassextension/SensorConnectionType
req.header: sensorsclassextension.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7,Available in Windows 7.
req.target-min-winversvr: None supported
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
req.typenames: SensorConnectionType
f1_keywords:
 - __MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002
 - sensorsclassextension/__MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002
 - SensorConnectionType
 - sensorsclassextension/SensorConnectionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SensorsClassExtension.h
api_name:
 - __MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002
 - SensorConnectionType
---

# __MIDL___MIDL_itf_windowssensorclassextension_0000_0000_0002 enumeration


## -description

The <b>SensorConnectionType</b> enumeration type defines values for the <a href="/windows-hardware/drivers/sensors/sensor-properties2">SENSOR_CONNECTION_TYPE</a> property.

## -enum-fields

### -field SENSOR_CONNECTION_TYPE_PC_INTEGRATED

Indicates that the sensor is built into the computer.

### -field SENSOR_CONNECTION_TYPE_PC_ATTACHED

Indicates that the sensor is attached to the computer, such as through a peripheral device.

### -field SENSOR_CONNECTION_TYPE_PC_EXTERNAL

Indicates that the sensor is connected by external means, such as through a network connection.

## -see-also

<a href="/windows-hardware/drivers/sensors/enumeration-properties">Enumeration properties</a>



<a href="/windows-hardware/drivers/ddi/sensorsclassextension/nf-sensorsclassextension-isensordriver-ongetproperties">ISensorDriver::OnGetProperties</a>

