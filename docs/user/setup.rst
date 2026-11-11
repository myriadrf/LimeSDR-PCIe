Hardware Setup
##############

Host Interface
**************

LimeSDR PCIe should be plugged into a PCI Express x4 slot on the host device. 

The host must provide a PCIe Gen1 x4 interface, and supply power via the PCIe x4 connector.

Cooling
*******

Depending on the application, host system and ambient temperature, additional cooling may be required to ensure reliable operation of the LimeSDR PCIe board. This may be in the form of airflow through the host system, or a dedicated heatsink fitted to the board.

When designing a cooling solution for a LimeSDR PCIe–based system, power dissipation should be evaluated based on the specific user configuration and use case. In general, the LimeSDR PCIe cooling solution should be designed to dissipate at least 30 W of power, providing sufficient thermal margin to ensure safe and reliable operation during peak loads.

.. note::
   In the event of errors, instability or reduced performance, check the board temperature to ensure that it is within the specified operating range.

RF Connections
**************

.. figure:: /images/LimeSDR-PCIe_v1.3_user_rfcon.png
  :width: 600
  
  Figure 3. LimeSDR PCIe v1.3 board top with RF connector positions

Figure 3 shows the RF connector positions on LimeSDR PCIe v1.3. LimeSDR PCIe v1.2 boards use the same RF connector designators, which are listed in Table 1.

.. list-table:: Table 1. RF connectors
   :header-rows: 1
   :stub-columns: 1

   * - RF port
     - Connector
     - Recommended range
   * - TX1_1
     - J1
     - Below 2 GHz
   * - TX1_2
     - J2
     - 2 GHz and above
   * - RX1_L
     - J3
     - Below 1.5 GHz
   * - RX1_W
     - J5
     - 1.5 GHz to 2.2 GHz
   * - RX1_H
     - J4
     - 2.2 GHz and above
   * - TX2_1
     - J6
     - Below 2 GHz
   * - TX2_2
     - J7
     - 2 GHz and above
   * - RX2_L
     - J8
     - Below 1.5 GHz
   * - RX2_W
     - J10
     - 1.5 GHz to 2.2 GHz
   * - RX2_H
     - J9
     - 2.2 GHz and above

.. note::
   The recommended frequency ranges are approximate values that cover most use cases, not hard limits of the RF paths. The optimum path may vary depending on other factors, such as the antenna and RF front-end parameters.

.. warning::
   Care should be taken when connecting external RF signals to the RX inputs, to ensure that the maximum safe input power of +10 dBm is not exceeded, as this may cause permanent damage to the device.
