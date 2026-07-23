LEDs
####

LimeSDR PCIe board comes with 6 indication LEDs which can be controlled from FPGA. By default, two of them (FPGA_LED1 and FPGA_LED2) are trough-hole dual colour LEDs and are mounted on the back edge of the board using right-angle plastic holder. The remaining four LEDs (FPGA_LED3 to FPGA_LED6) are SMD single green colour LEDs. There is one SMD single green colour LED named VDD3P3_PWR which is hardwired to VCC3P3 power rail and lit up whenever the board is powered on.

.. figure:: /images/LimeSDR-PCIe_v1.3_LEDs.png
  :width: 600

  Figure 7. LimeSDR PCIe v1.3 indication LEDs (top)

Each LED has it is own function. Most of LEDs are connected to FPGA and their function can be changed. Default LEDs functions and other information are listed in the Table 8.

.. table:: Table 8. Default LEDs configuration

  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+
  |                 | **Schematic** |            | **Schematic**   |              |                  |                                        |
  |                 |               |            |                 |              |                  |                                        |
  | **Board label** | **reference** | **Colour** | **signal name** | **FPGA pin** | **I/O standard** | **Comment**                            |
  +=================+===============+============+=================+==============+==================+========================================+
  | FPGA_LED1       | LEDS1 (LED1)  | Red/green  | FPGA_LED1_R     | E20          | 3.3V             | LEDS1 - trough-holeLED1 - optional SMD |
  |                 |               |            +-----------------+--------------+------------------+                                        |
  |                 |               |            | FPGA_LED1_G     | H21          | 3.3V             |                                        |
  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+
  | FPGA_LED2       | LEDS1 (LED4)  | Red/green  | FPGA_LED2_R     | G21          | 3.3V             | LEDS1 - trough-holeLED4 - optional SMD |
  |                 |               |            +-----------------+--------------+------------------+                                        |
  |                 |               |            | FPGA_LED2_G     | G20          | 3.3V             |                                        |
  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+
  | FPGA_LED3       | LED5          | Green      | FPGA_LED3       | K20          | 3.3V             |                                        |
  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+
  | FPGA_LED4       | LED6          | Green      | FPGA_LED4       | K19          | 3.3V             |                                        |
  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+
  | FPGA_LED5       | LED7          | Green      | FPGA_LED5       | K22          | 3.3V             |                                        |
  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+
  | FPGA_LED6       | LED8          | Green      | FPGA_LED6       | H20          | 3.3V             |                                        |
  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+
  | VDD3P3_PWR      | LED9          | Green      |                 |              |                  | Power LED                              |
  +-----------------+---------------+------------+-----------------+--------------+------------------+----------------------------------------+