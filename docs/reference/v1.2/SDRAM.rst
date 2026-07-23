SDRAM
#####

LimeSDR PCIe board has two 128MB (16bit bus) DDR2 SDRAM ICs (AS4C64M16D2-25BCN) connected to double data rate pins on Cyclone IV GX 1.8V Bank 3, 4 and 5. RAM chips (IC11, IC12) are connected to separate memory controllers so RAM chips works in dual channel mode. The memory can be used for data manipulation at high data rates between transceiver and FPGA. Pin connection and corresponding signal names are listed in Table 6 and Table 7.

.. list-table:: Table 6. DDR2 memory (IC11 - DDR2_1 BOT_L) pins
   :header-rows: 1
   :stub-columns: 1


   * - RAM reference
     - RAM pin
     - Schematic signal name
     - FPGA pin
     - FPGA I/O standard
     - Comments
   * - A0
     - M8
     - DDR2_1_A0
     - W20
     - SSTL-18 Class I
     - Active termination
   * - A1
     - M3
     - DDR2_1_A1
     - AA19
     - SSTL-18 Class I
     - Active termination
   * - A2
     - M7
     - DDR2_1_A2
     - AA21
     - SSTL-18 Class I
     - Active termination
   * - A3
     - N2
     - DDR2_1_A3
     - AB19
     - SSTL-18 Class I
     - Active termination
   * - A4
     - N8
     - DDR2_1_A4
     - V21
     - SSTL-18 Class I
     - Active termination
   * - A5
     - N3
     - DDR2_1_A5
     - AB20
     - SSTL-18 Class I
     - Active termination
   * - A6
     - N7
     - DDR2_1_A6
     - W22
     - SSTL-18 Class I
     - Active termination
   * - A7
     - P2
     - DDR2_1_A7
     - AA20
     - SSTL-18 Class I
     - Active termination
   * - A8
     - P8
     - DDR2_1_A8
     - V22
     - SSTL-18 Class I
     - Active termination
   * - A9
     - P3
     - DDR2_1_A9
     - AB21
     - SSTL-18 Class I
     - Active termination
   * - A10
     - M2
     - DDR2_1_A10
     - AB17
     - SSTL-18 Class I
     - Active termination
   * - A11
     - P7
     - DDR2_1_A11
     - U22
     - SSTL-18 Class I
     - Active termination
   * - A12
     - R2
     - DDR2_1_A12
     - Y22
     - SSTL-18 Class I
     - Active termination
   * - DQ0
     - G8
     - DDR2_1_DQ0
     - AB10
     - SSTL-18 Class I
     -
   * - DQ1
     - G2
     - DDR2_1_DQ1
     - AB14
     - SSTL-18 Class I
     -
   * - DQ2
     - H7
     - DDR2_1_DQ2
     - AB15
     - SSTL-18 Class I
     -
   * - DQ3
     - H3
     - DDR2_1_DQ3
     - Y13
     - SSTL-18 Class I
     -
   * - DQ4
     - H1
     - DDR2_1_DQ4
     - Y14
     - SSTL-18 Class I
     -
   * - DQ5
     - H9
     - DDR2_1_DQ5
     - W13
     - SSTL-18 Class I
     -
   * - DQ6
     - F1
     - DDR2_1_DQ6
     - W14
     - SSTL-18 Class I
     -
   * - DQ7
     - F9
     - DDR2_1_DQ7
     - W15
     - SSTL-18 Class I
     -
   * - DQ8
     - C8
     - DDR2_1_DQ8
     - AB18
     - SSTL-18 Class I
     -
   * - DQ9
     - C2
     - DDR2_1_DQ9
     - AA16
     - SSTL-18 Class I
     -
   * - DQ10
     - D7
     - DDR2_1_DQ10
     - AA18
     - SSTL-18 Class I
     -
   * - DQ11
     - D3
     - DDR2_1_DQ11
     - Y15
     - SSTL-18 Class I
     -
   * - DQ12
     - D1
     - DDR2_1_DQ12
     - Y16
     - SSTL-18 Class I
     -
   * - DQ13
     - D9
     - DDR2_1_DQ13
     - Y18
     - SSTL-18 Class I
     -
   * - DQ14
     - B1
     - DDR2_1_DQ14
     - Y19
     - SSTL-18 Class I
     -
   * - DQ15
     - B9
     - DDR2_1_DQ15
     - W17
     - SSTL-18 Class I
     -
   * - BA0
     - L2
     - DDR2_1_BA0
     - T20
     - SSTL-18 Class I
     - Active termination
   * - BA1
     - L3
     - DDR2_1_BA1
     - R20
     - SSTL-18 Class I
     - Active termination
   * - BA2
     - L1
     - DDR2_1_BA2
     - U20
     - SSTL-18 Class I
     - Active termination
   * - CKE
     - K2
     - DDR2_1_CKE
     - T19
     - SSTL-18 Class I
     - Active termination
   * - CK
     - J8
     - DDR2_1_CK_P
     - R9
     - SSTL-18 Class I
     - Termination resistor R73
   * - CK#
     - K8
     - DDR2_1_CK_N
     - T9
     - SSTL-18 Class I
     - Termination resistor R73
   * - WE#
     - K3
     - DDR2_1_WEn
     - V20
     - SSTL-18 Class I
     - Active termination
   * - CAS#
     - L7
     - DDR2_1_CASn
     - P22
     - SSTL-18 Class I
     - Active termination
   * - RAS#
     - K7
     - DDR2_1_RASn
     - T21
     - SSTL-18 Class I
     - Active termination
   * - CS#
     - L8
     - DDR2_1_CSn
     - T22
     - SSTL-18 Class I
     - Active termination
   * - ODT
     - K9
     - DDR2_1_ODT
     - R21
     - SSTL-18 Class I
     - Active termination
   * - LDM
     - F3
     - DDR2_1_DM0
     - R13
     - SSTL-18 Class I
     -
   * - UDM
     - B3
     - DDR2_1_DM1
     - U15
     - SSTL-18 Class I
     -
   * - LDQS
     - F7
     - DDR2_1_DQS0
     - T13
     - SSTL-18 Class I
     -
   * - LDQS#
     - E8
     - DDR2_1_DQS0n
     - 
     -
     - To GND via R76
   * - UDQS
     - B7
     - DDR2_1_DQS1
     - AA15
     - SSTL-18 Class I
     -
   * - UDQS#
     - A8
     - DDR2_1_DQS1n
     - 
     -
     - To GND via R77
   * - VREF
     - J2
     - VREF_DDR2
     - 
     -
     - IC8 Banks 3, 4, 5 VREF

.. list-table:: Table 7. DDR2 memory (IC12 - DDR2_2 BOT_R) pins
   :header-rows: 1
   :stub-columns: 1


   * - RAM reference
     - RAM pin
     - Schematic signal name
     - FPGA pin
     - FPGA I/O standard
     - Comments
   * - A0
     - M8
     - DDR2_2_A0
     - M13
     - SSTL-18 Class I
     - Active termination
   * - A1
     - M3
     - DDR2_2_A1
     - P14
     - SSTL-18 Class I
     - Active termination
   * - A2
     - M7
     - DDR2_2_A2
     - M14
     - SSTL-18 Class I
     - Active termination
   * - A3
     - N2
     - DDR2_2_A3
     - T11
     - SSTL-18 Class I
     - Active termination
   * - A4
     - N8
     - DDR2_2_A4
     - N13
     - SSTL-18 Class I
     - Active termination
   * - A5
     - N3
     - DDR2_2_A5
     - N15
     - SSTL-18 Class I
     - Active termination
   * - A6
     - N7
     - DDR2_2_A6
     - M15
     - SSTL-18 Class I
     - Active termination
   * - A7
     - P2
     - DDR2_2_A7
     - M16
     - SSTL-18 Class I
     - Active termination
   * - A8
     - P8
     - DDR2_2_A8
     - P13
     - SSTL-18 Class I
     - Active termination
   * - A9
     - P3
     - DDR2_2_A9
     - P15
     - SSTL-18 Class I
     - Active termination
   * - A10
     - M2
     - DDR2_2_A10
     - R15
     - SSTL-18 Class I
     - Active termination
   * - A11
     - P7
     - DDR2_2_A11
     - N14
     - SSTL-18 Class I
     - Active termination
   * - A12
     - R2
     - DDR2_2_A12
     - N17
     - SSTL-18 Class I
     - Active termination
   * - DQ0
     - G8
     - DDR2_2_DQ0
     - AB4
     - SSTL-18 Class I
     -
   * - DQ1
     - G2
     - DDR2_2_DQ1
     - AB5
     - SSTL-18 Class I
     -
   * - DQ2
     - H7
     - DDR2_2_DQ2
     - AA6
     - SSTL-18 Class I
     -
   * - DQ3
     - H3
     - DDR2_2_DQ3
     - Y5
     - SSTL-18 Class I
     -
   * - DQ4
     - H1
     - DDR2_2_DQ4
     - Y6
     - SSTL-18 Class I
     -
   * - DQ5
     - H9
     - DDR2_2_DQ5
     - Y7
     - SSTL-18 Class I
     -
   * - DQ6
     - F1
     - DDR2_2_DQ6
     - W5
     - SSTL-18 Class I
     -
   * - DQ7
     - F9
     - DDR2_2_DQ7
     - W6
     - SSTL-18 Class I
     -
   * - DQ8
     - C8
     - DDR2_2_DQ8
     - AB6
     - SSTL-18 Class I
     -
   * - DQ9
     - C2
     - DDR2_2_DQ9
     - W9
     - SSTL-18 Class I
     -
   * - DQ10
     - D7
     - DDR2_2_DQ10
     - Y9
     - SSTL-18 Class I
     -
   * - DQ11
     - D3
     - DDR2_2_DQ11
     - AA9
     - SSTL-18 Class I
     -
   * - DQ12
     - D1
     - DDR2_2_DQ12
     - AB8
     - SSTL-18 Class I
     -
   * - DQ13
     - D9
     - DDR2_2_DQ13
     - W11
     - SSTL-18 Class I
     -
   * - DQ14
     - B1
     - DDR2_2_DQ14
     - Y11
     - SSTL-18 Class I
     -
   * - DQ15
     - B9
     - DDR2_2_DQ15
     - AA10
     - SSTL-18 Class I
     -
   * - BA0
     - L2
     - DDR2_2_BA0
     - AB13
     - SSTL-18 Class I
     - Active termination
   * - BA1
     - L3
     - DDR2_2_BA1
     - AA13
     - SSTL-18 Class I
     - Active termination
   * - BA2
     - L1
     - DDR2_2_BA2
     - AA4
     - SSTL-18 Class I
     - Active termination
   * - CKE
     - K2
     - DDR2_2_CKE
     - T14
     - SSTL-18 Class I
     - Active termination
   * - CK
     - J8
     - DDR2_2_CK_P
     - W4
     - SSTL-18 Class I
     - Termination resistor R79
   * - CK#
     - K8
     - DDR2_2_CK_N
     - Y4
     - SSTL-18 Class I
     - Termination resistor R79
   * - WE#
     - K3
     - DDR2_2_WEn
     - T15
     - SSTL-18 Class I
     - Active termination
   * - CAS#
     - L7
     - DDR2_2_CASn
     - R19
     - SSTL-18 Class I
     - Active termination
   * - RAS#
     - K7
     - DDR2_2_RASn
     - U14
     - SSTL-18 Class I
     - Active termination
   * - CS#
     - L8
     - DDR2_2_CSn
     - AB11
     - SSTL-18 Class I
     - Active termination
   * - ODT
     - K9
     - DDR2_2_ODT
     - W18
     - SSTL-18 Class I
     - Active termination
   * - LDM
     - F3
     - DDR2_2_DM0
     - W7
     - SSTL-18 Class I
     -
   * - UDM
     - B3
     - DDR2_2_DM1
     - W12
     - SSTL-18 Class I
     -
   * - LDQS
     - F7
     - DDR2_2_DQS0
     - Y8
     - SSTL-18 Class I
     -
   * - LDQS#
     - E8
     - DDR2_2_DQS0n
     - 
     -
     - To GND via R82
   * - UDQS
     - B7
     - DDR2_2_DQS1
     - Y10
     - SSTL-18 Class I
     -
   * - UDQS#
     - A8
     - DDR2_2_DQS1n
     - 
     -
     - To GND via R83
   * - VREF
     - J2
     - VREF_DDR2
     - 
     -
     - IC8 Banks 3, 4, 5 VREF