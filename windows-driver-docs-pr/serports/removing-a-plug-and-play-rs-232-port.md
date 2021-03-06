---
title: Removing a Plug and Play RS-232 Port
author: windows-driver-content
description: Removing a Plug and Play RS-232 Port
MS-HAID:
- 'sseovr\_64d6356a-543f-40bd-ba17-26c411c4e420.xml'
- 'serports.removing\_a\_plug\_and\_play\_rs\_232\_port'
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: b439dc51-09f2-4149-a562-2e376bb504c5
keywords: ["RS-232 ports WDK serial devices", "Serenum driver WDK , Plug and Play devices", "Plug and Play serial devices WDK", "serial devices WDK , Plug and Play", "removing RS-232 ports"]
---

# Removing a Plug and Play RS-232 Port


## <a href="" id="ddk-removing-a-plug-and-play-rs-232-port-kg"></a>


The Plug and Play manager removes an RS-232 port by sending a remove request to the top of the RS-232 port stack. Serenum passes the request down the device stack, removes the filter DO in the port stack, and removes an associated PDO, if one exists. Removal of the RS-232 port also removes the serial device attached to the port.

 

 


--------------------
[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bserports\serports%5D:%20Removing%20a%20Plug%20and%20Play%20RS-232%20Port%20%20RELEASE:%20%288/4/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")


