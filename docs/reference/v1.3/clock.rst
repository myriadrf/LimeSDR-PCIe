Clock Distribution
##################

LimeSDR PCIe board clock distribution block diagram is presented in Figure 6.

.. figure:: /images/LimeSDR-PCIe_v1.3_clock.png
  :width: 600

  Figure 6. LimeSDR PCIe v1.3 board clock distribution block diagram

LimeSDR PCIe board has onboard 30.72 MHz ±250 ppb VCTCXO that is reference clock for LMS_PLLs. See block diagram of the clock distribution system in Figure 7.

VCTCXO can be tuned by onboard phase detector (IC18, ADF4002) or by DAC (IC17). The onboard phase detector is used to synchronize onboard VCTCXO with external equipment (via J16 U.FL connector) to calibrate frequency error. At the same time only ADF or DAC can control VCTCXO. DAC and ADF is controlled by FPGA and selection between ADF and DAC is done automatically. When board is powered, by default VCTCXO is controlled by DAC.

J16 connector (REF_CLK_IN) can also be used to supply external reference clock (fitting R109, removing R107, C347).

J15 connector (REF_CLK_OUT) can be used to feed clock to another board for synchronization purposes. For this purpose R122 resistor has to be fitted.

External reference clock frequency range is 5 MHz - 400 MHz. For frequencies less than 5 MHz, ensure slew rate is more than 4 V/μ. This is a CMOS input with a nominal threshold of VDD/2 (3.3 V / 2 = 1.65 V) and a DC equivalent input resistance of 100 kΩ. This input can be driven from a TTL or CMOS crystal oscillator or it can be AC-coupled.

The programmable clock generator (IC19, Si5351C) can generate any reference clock frequency, starting from 8 kHz – 160 MHz, for FPGA and LMS PLLs.

How to configure clocks using LMS7Suite read in chapter 7.4 Clock configuration.

.. table:: Table 4. LimeSDR PCIe clock pins

  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  |                                     | **Schematic**   |                  |              |                                |
  |                                     |                 |                  |              |                                |
  | **Source**                          | **signal name** | **I/O standard** | **FPGA pin** | **Description**                |
  +=====================================+=================+==================+==============+================================+
  | Programmable clock generator (IC19) | SI_CLK0         | 2.5V (3.3V)      | M7           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK1         | 2.5V (3.3V)      | N7           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK2         | 2.5V (3.3V)      | N8           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK3         | 2.5V (3.3V)      | J10          |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK4         | 3.3V             |              | Can be used as reference clock |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK6         | 3.3V             | L22          |                                |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  | Clock buffer (IC16)                 | LMK_CLK         | 3.3V             | B9           | Reference clock (30.72 MHz)    |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  | RF transceiver (IC1)                | LMS_MCLK1       | 2.5V (3.3V)      | K10          |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | LMS_FCLK1       | 2.5V (3.3V)      | H9           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | LMS_MCLK2       | 2.5V (3.3V)      | M8           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | LMS_FCLK2       | 2.5V (3.3V)      | C5           |                                |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  | FPGA (IC8)                          | FPGA_CLK_OUT    | 3.3V             | C18          | Can be used as reference clock |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
