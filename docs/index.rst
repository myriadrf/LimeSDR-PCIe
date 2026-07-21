Introduction
============

.. toctree::
   :maxdepth: 2
   :hidden:

   Introduction <self>
   user/index
   reference/index
   developer

.. figure:: /images/LimeSDR-PCIe_v1.3_iso.png
   :align: center
   :width: 600



The LimeSDR PCIe is a software-defined radio (SDR), with 2T2R MIMO capability and covering frequency range from 100 kHz to 3.8 GHz, with up to 61.44 MHz bandwidth. It is designed for flexible, wideband wireless communication development and experimentation.

The LimeSDR PCIe development board provides a hardware platform for developing and prototyping high-performance and logic-intensive digital and RF designs using Altera’s Cyclone IV FPGA and Lime Microsystems transceiver, through which apps can be programmed to support any type of wireless standard, e.g. UMTS, LTE, LoRa, GPS, WiFi, Zigbee, RFID, Digital Broadcasting, Radar and many more.

Specifications
**************

RF
==

.. list-table:: 
   :header-rows: 1
   :stub-columns: 1

   * - Parameter
     - Value
     - Notes
   * - Configuration
     - MIMO (2T2R)
     - Full duplex
   * - Frequency Range
     - 100 kHz – 3.8 GHz
     - Continuous coverage
   * - Bandwidth
     - up to 61.44 MHz
     - Software configurable
   * - Sample rate
     - 61.44 MSPS
     - 
   * - Sample depth
     - 12 bit
     - 
   * - Power Ouput (CW)
     - Up to 10 dBm
     - Dependent on frequency
   * - Max. Safe Rx Input Power
     - 10 dBm
     - Absolute maximum



Digital Interface
=================

PCIe 1.0 x4 (4 lanes)

Power Supply
============

.. table:: 

   +---------------+--------------+---------------------+
   | **Parameter** | **Value**    | **Notes**           |
   +===============+==============+=====================+
   | Input Voltage | 12 V DC      | PCIe x4 connector   |
   |               +              +---------------------+
   |               |              | DC barrel connector |
   +---------------+--------------+---------------------+
   | Maximum Power | 30 W         |                     |
   +---------------+--------------+---------------------+

.. note::
   Power consumption depends on configuration.

.. warning::
   Incorrect voltage or inadequate current capacity may cause damage or unstable operation.

Environmental
=============

.. list-table:: 
   :header-rows: 1
   :stub-columns: 1

   * - Parameter
     - Value
     - Notes
   * - Operating Temperature
     - 0 °C to +70 °C
     - Commercial-grade
   * - Storage Temperature
     - 0 °C to +70 °C
     - N/A
   * - Operating Humidity
     - 10% to 90% RH  
     - Non-condensing

Mechanical
==========

Low profile form factor: 68,9mm x 136,85mm.

Features
********

Devices
=======

* RF transceiver: Lime Microsystems LMS7002M
*  FPGA: Cyclone IV GX (EP4CGX30CF23C7N) device in 484-pin FBGA
 
   * 29’440 logic elements
   * 1080 Kbits embedded memory
   * 80 embedded 18x18 multipliers
   * 4 general and 2 multipurpose PLLs
   * 4 high-speed transceivers
   * PCIe (PIPE) hard IP block
  
* Temperature sensor: LM75
  
Clock system
============

* 30.72MHz ±250 ppb onboard VCTCXO
* Possibility to lock VCTCXO to external clock or tune VCTCXO by onboard DAC
* Programmable clock generator for the FPGA reference clock input or LMS PLLs
* 100 MHz and 2x 50MHz crystal oscillators for FPGA

Memory
======

* 2x 1Gbit (64M x 16) dual channel DDR2 SDRAM
* 4Mbit flash for FPGA data
* 64Mbit flash for FPGA gateware
* 128Kb (16K x 8) EEPROM for LMS MCU firmware and 512Kb (64K x 8) LMS MCU data

Connections
===========

* PCI Express x4 (4 lanes)
* Coaxial RF (U.FL) connectors
* FPGA GPIO 2x8 (3.3V) headers
* FPGA and JTAG connector
* DC (12V) power jack and pinheader
* FAN (12V) connector

Purchasing
**********

Please contact us for purchasing information.

RoHS
====

This product is RoHS compliant and does not contain hazardous substances as defined by Directive 2011/65/EU.

WEEE
====

This product must be disposed of properly according to local regulations. Do not dispose of with general household waste.

RF Transmission Notice
======================

.. warning::
   Operating RF transmitting equipment may require appropriate licensing. Users are responsible for ensuring compliance with local regulations. Unauthorised transmission may result in legal penalties.
