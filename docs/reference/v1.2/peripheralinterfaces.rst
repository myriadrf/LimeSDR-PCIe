Peripheral Interfaces
#####################

LimeSDR PCIe board peripheral interfaces is presented in Figure 8.

.. figure:: /images/LimeSDR-PCIe_v1.2_LSI.png
  :width: 600

  Figure 8: LimeSDR PCIe v1.2 peripheral interfaces block diagram

SPI
***

LimeSDR PCIe board has four SPI interfaces with their own slave devices:

Flash for FPGA gateware
=======================

Flash memory (IC9 or IC10) is used to store FPGA gateware.

.. list-table:: Table 9. FPGA configuration flash interface pins
   :header-rows: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - FPGA_AS_DCLK
     - D3
     - 3.3V
     -
   * - FPGA_AS_ASDO
     - D1
     - 3.3V
     -
   * - FPGA_AS_DATA0
     - K4
     - 3.3V
     -
   * - FPGA_AS_NCSO
     - J4
     - 3.3V
     - SPI flash slave select

RFIC
====

RFIC is connected to FPGA_SPI0.
  
.. list-table:: Table 10. FPGA SPI0 interface pins
   :header-rows: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - FPGA_SPI0_SCLK
     - B3
     - 2.5V (3.3V)
     -
   * - FPGA_SPI0_MOSI
     - C1
     - 2.5V (3.3V)
     -
   * - FPGA_SPI0_MISO
     - A3
     - 2.5V (3.3V)
     -
   * - FPGA_SPI0_LMS_SS
     - B1
     - 2.5V (3.3V)
     - IC1 (LMS7002) SPI slave select


Phase detector and DAC
======================

Phase detector with VCTCXO DAC are connected to FPGA_SPI1.

  
.. list-table:: Table 11. FPGA SPI1 interface pins
   :header-rows: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - FPGA_SPI1_SCLK
     - C20
     - 2.5V (3.3V)
     -
   * - FPGA_SPI1_MOSI
     - C19
     - 2.5V (3.3V)
     -
   * - FPGA_SPI1_DAC_SS
     - A20
     - 2.5V (3.3V)
     - IC17 XO DAC Slave select
   * - FPGA_SPI1_ADF_SS
     - B19
     - 2.5V (3.3V)
     - IC18 Phase detector Slave select

Flash memory
============

Flash memory is connected to FPGA_SPI2.

.. list-table:: Table 12. FPGA SPI2 interface pins
   :header-rows: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - FPGA_SPI2_SCLK
     - J19
     - 3.3V
     -
   * - FPGA_SPI2_MOSI
     - H22
     - 3.3V
     -
   * - FPGA_SPI2_MISO
     - J21
     - 3.3V
     -
   * - FPGA_SPI2_FLASH_SS
     - J22
     - 3.3V
     - FPGA flash (IC13) slave select

I2C
***

Board has two independent I2C interfaces: FPGA_I2C and LMS_I2C.

FPGA_I2C
========

This interface has several slave devices temperature sensor, EEPROM and clock generator. Information for slave devices are provided in Table 13, signal connectivity information is in Table 14.

.. list-table:: Table 13. FPGA_I2C interface devices
   :header-rows: 1

   * - I2C slave device
     - Slave device
     - I2C address
     - I/O standard
     - Comment
   * - IC14
     - Temperature sensor
     - 1001000 (R/W)
     - 3.3V
     - LM75
   * - IC15
     - EEPROM
     - 1010000 (R/W)
     - 3.3V
     - M24128
   * - IC19
     - Clock generator
     - 1100000 (R/W)
     - 3.3V
     - Si5351C

.. list-table:: Table 14. FPGA_I2C pins
   :header-rows: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - FPGA_I2C_SDA
     - G16
     - 3.3V
     -
   * - FPGA_I2C_SCL
     - G17
     - 3.3V
     -


LMS_I2C
=======

This interface has two EEPROMs. In Table 15 are listed all LMS_I2C slave devices and their information.

.. list-table:: Table 15. LMS_I2C interface devices
   :header-rows: 1

   * - I2C slave device
     - Slave device
     - I2C address
     - I/O standard
     - Comment
   * - IC2
     - EEPROM for LMS7 MCU firmware
     - 1010000 (R/W)
     - 3.3V
     - M24128
   * - IC3
     - EEPROM
     - 1010111 (R/W)
     - 3.3V
     - 24FC512

LMS_I2C interface (LMS_I2C_SCL, LMS_I2C_SDA) is connected via 0R resistors to FPGA pins for debugging purposes, see Table 16.

.. list-table:: Table 16. LLMS_I2C pins
   :header-rows: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - LMS_I2C_SCL
     - G11
     - 2.5V (3.3V)
     - 0R resistor R51
   * - LMS_I2C_SDA
     - A2
     - 2.5V (3.3V)
     - 0R resistor R46
