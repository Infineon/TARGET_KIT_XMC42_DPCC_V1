# KIT_XMC42_DPCC_V1 BSP

## Overview

XMC4200 Digital Power Control Card - This kit has the XMC4200 device with debugger plus connector to the      XMC Digital Power Explorer Board. Equipped with an ARM® Cortex®-M4 based XMC™ Microcontroller from Infineon Technologies AG,     the XMC4200 Digital Power Control Card is designed to evaluate the capabilities of Infineon's XMC4200 Microcontroller for power stage control applications.     
**Note:**
Programming this kit requires installing 
[SEGGER J-Link software](https://www.segger.com/downloads/jlink/#J-LinkSoftwareAndDocumentationPack)

![](docs/html/board.png)

To use code from the BSP, simply include a reference to `cybsp.h`.

## Features

### Kit Features:

* XMC4200 (ARM® Cortex®-M4 based) Microcontroller
* On-board Debug Probe with USB interface supporting SWD 
* Detachable J-Link debugger and UART virtual COM port, with micro USB connector
* Virtual COM Port via Debug Probe

### Kit Contents:

* KIT_XMC42_DPCC_V1 evaluation board

## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the KIT_XMC42_DPCC_V1.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.

Defines:
* CYBSP_WIFI_CAPABLE - This define, disabled by default, causes the BSP to initialize the interface to an onboard wireless chip if it has one.
* CY_USING_HAL - This define, enabled by default, specifies that the HAL is intended to be used by the application. This will cause the BSP to include the applicable header file and to initialize the system level drivers.
* CYBSP_CUSTOM_SYSCLK_PM_CALLBACK - This define, disabled by default, causes the BSP to skip registering its default SysClk Power Management callback, if any, and instead to invoke the application-defined function `cybsp_register_custom_sysclk_pm_callback` to register an application-specific callback.



See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The KIT_XMC42_DPCC_V1 Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [KIT_XMC42_DPCC_V1 BSP API Reference Manual][api]
* [KIT_XMC42_DPCC_V1 Documentation](https://www.infineon.com/cms/en/product/microcontroller/32-bit-industrial-microcontroller-based-on-arm-cortex-m/)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_KIT_XMC42_DPCC_V1/html/modules.html
[settings]: https://infineon.github.io/TARGET_KIT_XMC42_DPCC_V1/html/md_bsp_settings.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2022.