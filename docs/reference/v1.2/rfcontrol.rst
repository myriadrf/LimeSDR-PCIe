RF Network
##########

The RF network contains matching networks, RF switches, two -25 dB loopback attenuators and ten U.FL connectors.

Frequency Range
===============

Each LMS7002M RF transceiver TX and RX port is connected to a dedicated RF path, and the appropriate path should be selected according to the operating frequency. On the receive side, the low-band paths (RX1_L, RX2_L) are recommended for frequencies below 1.5 GHz, the wideband paths (RX1_W, RX2_W) for 1.5 GHz to 2.2 GHz and the high-band paths (RX1_H, RX2_H) for frequencies of 2.2 GHz and above. On the transmit side, the TX1_1 and TX2_1 paths are recommended for frequencies below 2 GHz and the TX1_2 and TX2_2 paths for frequencies of 2 GHz and above. The recommended frequency ranges for all ports are summarised in Table 3.

.. note::
   The recommended frequency ranges are approximate values that cover most use cases, not hard limits of the RF paths. The optimum path may vary depending on other factors, such as the antenna and RF front-end parameters.

.. list-table:: Table 3. LMS7002M RF transceiver ports and recommended frequency ranges
   :header-rows: 1

   * - RF transceiver port
     - Connector
     - Recommended frequency range
   * - TX1_1/TX2_1
     - J1/J6
     - Below 2 GHz
   * - TX1_2/TX2_2
     - J2/J7
     - 2 GHz and above
   * - RX1_L/RX2_L
     - J3/J8
     - Below 1.5 GHz
   * - RX1_W/RX2_W
     - J5/J10
     - 1.5 GHz to 2.2 GHz
   * - RX1_H/RX2_H
     - J4/J9
     - 2.2 GHz and above

Control
=======

In each channel, the TX1_2/TX2_2 output and the RX1_H/RX2_H input can be connected together through a loopback path with a fixed -25 dB attenuator. When the loopback is not used, the attenuator can be shunted to GND by RF MOSFETs for better isolation. The RF switches and the shunt MOSFETs are controlled by FPGA outputs in Bank 6 (VCC3P3, 3.3 V). RF network control signals are described in Table 4.

.. list-table:: Table 4. RF network control signals
   :header-rows: 1

   * - Schematic signal name
     - FPGA pin
     - I/O standard
     - Description
   * - TX1_2_LB_L
     - A22
     - 3.3 V
     - Channel 1 RF switches (IC4, IC5). LB_L high, LB_H low: TX1_2 to J2, RX1_H to J4.
   * - TX1_2_LB_H
     - A21
     - 3.3 V
     - Channel 1 RF switches (IC4, IC5). LB_L low, LB_H high: TX1_2 to RX1_H via attenuator.
   * - TX1_2_LB_SH
     - B20
     - 3.3 V
     - Channel 1 loopback shunt (VT1, VT2). High: attenuator shunted to GND.
   * - TX2_2_LB_L
     - B22
     - 3.3 V
     - Channel 2 RF switches (IC6, IC7). LB_L high, LB_H low: TX2_2 to J7, RX2_H to J9.
   * - TX2_2_LB_H
     - B21
     - 3.3 V
     - Channel 2 RF switches (IC6, IC7). LB_L low, LB_H high: TX2_2 to RX2_H via attenuator.
   * - TX2_2_LB_SH
     - C22
     - 3.3 V
     - Channel 2 loopback shunt (VT3, VT4). High: attenuator shunted to GND.
