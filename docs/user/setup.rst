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
  
  Figure 3: LimeSDR PCIe v1.3 board top with RF connectors positions

.. list-table:: Table 1. RF Connectors
   :header-rows: 1
   :stub-columns: 1

   * - Connector
     - Frequency Range
     - Notes
   * - J1
     - 0.03 GHz - 1.9 GHz
     - Channel 1 transmit low frequency range
   * - J2
     - 2 GHz - 2.6 GHz
     - Channel 1 transmit high frequency range
   * - J3
     - 0.7 GHz - 0.9 GHz
     - Channel 1 receive low frequency range
   * - J4
     - 2 GHz - 2.6 GHz
     - Channel 1 receive high frequency range
   * - J5
     - 0.7 GHz - 2.6 GHz
     - Channel 1 receive wide frequency range
   * - J6
     - 0.03 GHz - 1.9 GHz
     - Channel 2 transmit low frequency range
   * - J7
     - 2 GHz - 2.6 GHz
     - Channel 2 transmit high frequency range
   * - J8
     - 0.7 GHz - 0.9 GHz
     - Channel 2 receive low frequency range
   * - J9
     - 2 GHz - 2.6 GHz
     - Channel 2 receive high frequency range
   * - J10
     - 0.7 GHz - 2.6 GHz
     - Channel 2 receive wide frequency range

.. note::
   TX and RX bands frequency ranges are determined by matching networks. These bands frequency ranges can be changed by replacing their matching networks components.

.. warning::
   Care should be taken when connecting external RF signals to the RX inputs, to ensure that the maximum safe input power of +10 dBm is not exceeded, as this may cause permanent damage to the device.
