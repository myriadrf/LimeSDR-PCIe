FPGA Switch
###########

Four poles slide switch SW1 is connected to FPGA. Each switch line has external pull up resistors. When switch is in position “On”, it pulls down the line.

.. figure:: /images/LimeSDR-PCIe_FPGA_switch.png
  :width: 600

  Figure 9. LimeSDR PCIe v1.3 FPGA switch schematics

.. list-table:: Table 19. FPGA Switch connections
   :header-rows: 1
   :stub-columns: 1

   * - Switch pole
     - Schematic signal name
     - FPGA pin
     - I/O standard
   * - 1
     - FPGA_SW0
     - D22
     - 3.3V
   * - 2
     - FPGA_SW1
     - E21
     - 3.3V
   * - 3
     - FPGA_SW2
     - E22
     - 3.3V
   * - 4
     - FPGA_SW3
     - G22
     - 3.3V
