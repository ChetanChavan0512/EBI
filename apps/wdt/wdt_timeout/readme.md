---
parent: Harmony 3 peripheral library application examples for PIC32MZ EF family
title: WDT timeout 
has_children: false
has_toc: false
---

[![MCHP](https://www.microchip.com/ResourcePackages/Microchip/assets/dist/images/logo.png)](https://www.microchip.com)

# WDT timeout

This example application shows how the watchdog timer resets by not feeding the watchdog on switch press.

## Description

This example application shows how the WDT peripheral library resets the watchdog timer by not feeding the watchdog on switch press. The application sets up the watchdog to reset the device. The application also sets up the timer to blink an LED to emulate a process. A user switch press forces the device to wait in an infinite loop to emulate a deadlock. As a result a device reset is triggered as the watchdog counter overflows the bounded value.

## Downloading and building the application

To clone or download this application from Github, go to the [main page of this repository](https://github.com/Microchip-MPLAB-Harmony/csp_apps_pic32mz_ef) and then click **Clone** button to clone this repository or download as zip file.
This content can also be downloaded using content manager by following these [instructions](https://github.com/Microchip-MPLAB-Harmony/contentmanager/wiki).

Path of the application within the repository is **apps/wdt/wdt_timeout/firmware** .

To build the application, refer to the following table and open the project using its IDE.

| Project Name      | Description                                    |
| ----------------- | ---------------------------------------------- |
| pic32mz_ef_sk.X | MPLABX project for [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007) |
|||

## Setting up the hardware

The following table shows the target hardware for the application projects.

| Project Name| Board|
|:---------|:---------:|
| pic32mz_ef_sk.X | [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007) |
|||

### Setting up [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007)

- Connect mini USB cables from the ???Debug USB??? and ???USB-to-UART??? connectors on the board to the computer

## Running the Application

1. Open the Terminal application (Ex.:Tera term) on the computer
2. Connect to the EDBG Virtual COM port and configure the serial settings as follows:
    - Baud : 115200
    - Data : 8 Bits
    - Parity : None
    - Stop : 1 Bit
    - Flow Control : None
3. Build and Program the application project using its IDE
4. LED should be blinking and the console displays the following message

    ![output](images/output_wdt_timeout_1.png)

5. Press the switch to put the system in a deadlock
6. LED should stop blinking and the console should print the following message

    ![output](images/output_wdt_timeout_2.png)

7. WDT will reset the device in four seconds and the demonstration should restart

Refer the table below for details of switch and LED:

| Board      | Switch Name| LED Name |
| ---------- |--------- | --------- |
| [PIC32MZ Embedded Connectivity with FPU (EF) Starter Kit](https://www.microchip.com/DevelopmentTools/ProductDetails/dm320007) | SW1 | LED1 |
||||
