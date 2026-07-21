PCI Express x4 Connector
########################

For data transfer LimeSDR PCIe board has PCI express connector with four lanes. PCI express interface is implemented in FPGA. Pin connection and corresponding signal names are listed in Table 5.

.. list-table:: Table 5. PCIe connector pins
   :header-rows: 1
   :stub-columns: 1
   
   * - Connector pin
     - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - B5
     - PCIE_SMCLK
     - A10
     - 3.3V
     -
   * - B6
     - PCIE_SMDAT
     - B10
     - 3.3V
     -
   * - B11
     - PCIE_WAKEn
     - G12
     - 3.3V
     - Signal is disconnected with not fitted R100 resistor
   * - B14
     - PCIE_HSO0_P
     - Y2
     - 1.5-V PCML
     -
   * - B15
     - PCIE_HSO0_N
     - Y1
     - 1.5-V PCML
     -
   * - B19
     - PCIE_HSO1_P
     - T2
     - 1.5-V PCML
     -
   * - B20
     - PCIE_HSO1_N
     - T1
     - 1.5-V PCML
     -
   * - B23
     - PCIE_HSO2_P
     - M2
     - 1.5-V PCML
     -
   * - B24
     - PCIE_HSO2_N
     - M1
     - 1.5-V PCML
     -
   * - B27
     - PCIE_HSO3_P
     - H2
     - 1.5-V PCML
     -
   * - B28
     - PCIE_HSO3_N
     - H1
     - 1.5-V PCML
     -
   * - A11
     - PCIE_PERSTn
     - H12
     - 3.3V
     -
   * - A13
     - PCIE_REFCLK_P
     - M7
     - HCSL
     -
   * - A14
     - PCIE_REFCLK_N
     - N7
     - HCSL
     -
   * - A16
     - PCIE_HSI0_P
     - V2
     - 1.5-V PCML
     - AC coupled
   * - A17
     - PCIE_HSI0_N
     - V1
     - 1.5-V PCML
     - AC coupled
   * - A21
     - PCIE_HSI1_P
     - P2
     - 1.5-V PCML
     - AC coupled
   * - A22
     - PCIE_HSI1_N
     - P1
     - 1.5-V PCML
     - AC coupled
   * - A25
     - PCIE_HSI2_P
     - K2
     - 1.5-V PCML
     - AC coupled
   * - A26
     - PCIE_HSI2_N
     - K1
     - 1.5-V PCML
     - AC coupled
   * - A29
     - PCIE_HSI3_P
     - F2
     - 1.5-V PCML
     - AC coupled
   * - A30
     - PCIE_HSI3_N
     - F1
     - 1.5-V PCML
     - AC coupled