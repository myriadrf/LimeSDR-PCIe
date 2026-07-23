RF Transceiver Digital
######################

The `LMS7002M`_ digital interface and control signals are described below.

Digital Interface
*****************

LMS7002 is using data bus LMS_DIQ1_D[11:0] and LMS_DIQ2_D[11:0], LMS_ENABLE_IQSEL1 and LMS_ENABLE_IQSEL2, LMS_FCLK1 and LMS_FCLK2, LMS_MCLK1 and LMS_MCLK2 signals to transfer data to/from FPGA. Indexes 1 and 2 indicate transceiver digital data PORT-1 or PORT-2. Any of these ports can be used to transmit or receive data.

By default PORT-1 is selected as transmitter port and PORT-2 is selected as receiver port. The FCLK# is input clock and MCLK# is output clock for the LMS7002M transceiver. TXNRX signals are used to indicate ports direction. Please refer to `LMS7002M transceiver datasheet`_ page 12-13 for the LMS7002M interface timing.

Control
*******

These signals are used for the following functions within the LMS7002 RFIC:

* LMS_RXEN, LMS_TXEN – receiver and transmitter enable/disable signals.
* LMS_RESET – LMS7002M reset.
* SPI Interface: LMS7002M transceiver is configured via 4-wire SPI interface; FPGA_SPI0_SCLK, FPGA_SPI0_MOSI, FPGA_SPI0_MISO, FPGA_SPI0_LMS_SS.
* I2C Interface: used access EEPROM memories for LMS7002M MCU firmware and data. I2C interface is using LMS_I2C_SCL, LMS_I2C_SDA signals.

LMS7002M Pins
*************

.. list-table:: Table 2. LMS7002M RF transceiver digital interface pins
   :header-rows: 1
   :stub-columns: 1


   * - Chip pin (IC1)
     - Chip reference (IC1)
     - Schematic signal name
     - FPGA pin
     - FPGA I/O standard
     - Comment
   * - AM24
     - xoscin_rx
     - RxPLL_CLK
     - 
     - 2.5V (3.3V)
     - Connected to 30.72 MHz clock
   * - E5
     - xoscin_tx
     - TxPLL_CLK
     - 
     - 2.5V (3.3V)
     - Connected to 30.72 MHz clock
   * - E27
     - RESET
     - LMS_RESET
     - A1
     - 2.5V (3.3V)
     -
   * - U29
     - TXEN
     - LMS_TXEN
     - A7
     - 2.5V (3.3V)
     -
   * - D28
     - SEN
     - FPGA_SPI0_LMS_SS
     - B1
     - 2.5V (3.3V)
     - SPI interface
   * - C29
     - SCLK
     - FPGA_SPI0_SCLK
     - B3
     - 2.5V (3.3V)
     - SPI interface
   * - F30
     - SDIO
     - FPGA_SPI0_MOSI
     - C1
     - 2.5V (3.3V)
     - SPI interface
   * - F28
     - SDO
     - FPGA_SPI0_MISO
     - A3
     - 2.5V (3.3V)
     - SPI interface
   * - D26
     - SDA
     - LMS_I2C_SDA
     - A2 (via R46)
     - 2.5V (3.3V)
     - Connected to EEPROMS
   * - C27
     - SCL
     - LMS_I2C_SCL
     - G11 (via R51)
     - 2.5V (3.3V)
     - Connected to EEPROMS
   * - AB34
     - MCLK1
     - LMS_MCLK1
     - K10
     - 2.5V (3.3V)
     -
   * - AA33
     - FCLK1
     - LMS_FCLK1
     - H9
     - 2.5V (3.3V)
     -
   * - V32
     - TXNRX1
     - LMS_TXNRX1
     - C3
     - 2.5V (3.3V)
     -
   * - V34
     - RXEN
     - LMS_RXEN
     - C2
     - 2.5V (3.3V)
     -
   * - Y32
     - ENABLE_IQSEL1
     - LMS_ENABLE_IQSEL1
     - D6
     - 2.5V (3.3V)
     -
   * - AG31
     - DIQ1_D0
     - LMS_DIQ1_D0
     - D9
     - 2.5V (3.3V)
     -
   * - AF30
     - DIQ1_D1
     - LMS_DIQ1_D1
     - B7
     - 2.5V (3.3V)
     -
   * - AF34
     - DIQ1_D2
     - LMS_DIQ1_D2
     - H8
     - 2.5V (3.3V)
     -
   * - AE31
     - DIQ1_D3
     - LMS_DIQ1_D3
     - C8
     - 2.5V (3.3V)
     -
   * - AD30
     - DIQ1_D4
     - LMS_DIQ1_D4
     - C7
     - 2.5V (3.3V)
     -
   * - AC29
     - DIQ1_D5
     - LMS_DIQ1_D5
     - C9
     - 2.5V (3.3V)
     -
   * - AE33
     - DIQ1_D6
     - LMS_DIQ1_D6
     - H7
     - 2.5V (3.3V)
     -
   * - AD32
     - DIQ1_D7
     - LMS_DIQ1_D7
     - G8
     - 2.5V (3.3V)
     -
   * - AC31
     - DIQ1_D8
     - LMS_DIQ1_D8
     - E8
     - 2.5V (3.3V)
     -
   * - AC33
     - DIQ1_D9
     - LMS_DIQ1_D9
     - G7
     - 2.5V (3.3V)
     -
   * - AB30
     - DIQ1_D10
     - LMS_DIQ1_D10
     - F8
     - 2.5V (3.3V)
     -
   * - AB32
     - DIQ1_D11
     - LMS_DIQ1_D11
     - E6
     - 2.5V (3.3V)
     -
   * - U33
     - CORE_LDO_EN
     - LMS_CORE_LDO_EN
     - C4
     - 2.5V (3.3V)
     -
   * - P34
     - MCLK2
     - LMS_MCLK2
     - M11
     - 2.5V (3.3V)
     -
   * - R29
     - FCLK2
     - LMS_FCLK2
     - C5
     - 2.5V (3.3V)
     -
   * - U31
     - TXNRX2
     - LMS_TXNRX2
     - A4
     - 2.5V (3.3V)
     -
   * - R33
     - ENABLE_IQSEL2
     - LMS_ENABLE_IQSEL2
     - B6
     - 2.5V (3.3V)
     -
   * - H30
     - DIQ2_D0
     - LMS_DIQ2_D0
     - G6
     - 2.5V (3.3V)
     -
   * - J31
     - DIQ2_D1
     - LMS_DIQ2_D1
     - E5
     - 2.5V (3.3V)
     -
   * - K30
     - DIQ2_D2
     - LMS_DIQ2_D2
     - A8
     - 2.5V (3.3V)
     -
   * - K32
     - DIQ2_D3
     - LMS_DIQ2_D3
     - D7
     - 2.5V (3.3V)
     -
   * - L31
     - DIQ2_D4
     - LMS_DIQ2_D4
     - D8
     - 2.5V (3.3V)
     -
   * - K34
     - DIQ2_D5
     - LMS_DIQ2_D5
     - F6
     - 2.5V (3.3V)
     -
   * - M30
     - DIQ2_D6
     - LMS_DIQ2_D6
     - C6
     - 2.5V (3.3V)
     -
   * - M32
     - DIQ2_D7
     - LMS_DIQ2_D7
     - D4
     - 2.5V (3.3V)
     -
   * - N31
     - DIQ2_D8
     - LMS_DIQ2_D8
     - A5
     - 2.5V (3.3V)
     -
   * - N33
     - DIQ2_D9
     - LMS_DIQ2_D9
     - D5
     - 2.5V (3.3V)
     -
   * - P30
     - DIQ2_D10
     - LMS_DIQ2_D10
     - B4
     - 2.5V (3.3V)
     -
   * - P32
     - DIQ2_D11
     - LMS_DIQ2_D11
     - A6
     - 2.5V (3.3V)
     -