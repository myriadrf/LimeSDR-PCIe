Clock Distribution
##################

LimeSDR PCIe board clock distribution block diagram is presented in Figure 6.

.. figure:: /images/LimeSDR-PCIe_v1.2_clock.png
  :width: 600

  Figure 6. LimeSDR PCIe v1.2 board clock distribution block diagram

LimeSDR PCIe board has onboard 30.72 MHz ±250 ppb VCTCXO that is reference clock for LMS_PLLs. See block diagram of the clock distribution system in Figure 6.

VCTCXO can be tuned by onboard phase detector (IC19, ADF4002) or by DAC (IC18). The onboard phase detector is used to synchronise onboard VCTCXO with external equipment (via J16 U.FL connector) to calibrate frequency error. At the same time only ADF or DAC can control VCTCXO. DAC and ADF is controlled by FPGA and selection between ADF and DAC is done automatically. When board is powered, by default VCTCXO is controlled by DAC.

J16 connector (REF_CLK_IN) can also be used to supply external reference clock (fitting R117, removing R107, C345).

The external reference clock frequency range is 10–52 MHz, with signal levels from 1.8 V to 3.3 V.

J15 connector (REF_CLK_OUT) can be used to feed clock to another board for synchronisation purposes. For this purpose R121 resistor has to be fitted.

The programmable clock generator (IC20, Si5351C) can generate any reference clock frequency, starting from 8 kHz – 160 MHz, for FPGA and LMS PLLs.

.. table:: Table 5. LimeSDR PCIe clock pins

  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  |                                     | **Schematic**   |                  |              |                                |
  |                                     |                 |                  |              |                                |
  | **Source**                          | **signal name** | **I/O standard** | **FPGA pin** | **Description**                |
  +=====================================+=================+==================+==============+================================+
  | Programmable clock generator (IC20) | SI_CLK0         | 2.5 V (3.3 V)    | M7           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK1         | 2.5 V (3.3 V)    | N7           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK2         | 2.5 V (3.3 V)    | N8           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK3         | 2.5 V (3.3 V)    | J10          |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK4         | 3.3 V            |              | Can be used as reference clock |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | SI_CLK6         | 3.3 V            | L22          |                                |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  | Clock buffer (IC16)                 | LMK_CLK         | 3.3 V            | B9           | Reference clock (30.72 MHz)    |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  | RF transceiver (IC1)                | LMS_MCLK1       | 2.5 V (3.3 V)    | K10          |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | LMS_FCLK1       | 2.5 V (3.3 V)    | H9           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | LMS_MCLK2       | 2.5 V (3.3 V)    | M8           |                                |
  |                                     +-----------------+------------------+--------------+--------------------------------+
  |                                     | LMS_FCLK2       | 2.5 V (3.3 V)    | C5           |                                |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
  | FPGA (IC8)                          | FPGA_CLK_OUT    | 3.3 V            | C18          | Can be used as reference clock |
  +-------------------------------------+-----------------+------------------+--------------+--------------------------------+
