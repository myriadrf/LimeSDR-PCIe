Reference Clock
###############

The LimeSDR PCIe clock system is based on a high stability 30.72 MHz VCTCXO (Voltage Controlled Temperature Compensated Crystal Oscillator) which can be tuned via on-board DAC. 

The board provides dedicated U.FL connectors for reference clock input (J16) and output (J15).

.. figure:: /images/LimeSDR-PCIe_v1.3_user_clockcon.png
  :width: 600
  
  Figure 4: LimeSDR PCIe v1.3 board top with reference clock connectors positions


.. list-table:: Table 2. Clock Functions
   :header-rows: 1
   :stub-columns: 1

   * - Function
     - Specification
     - Notes
   * - On-board Oscillator
     - 30.72 MHz VCTCXO
     - Rakon E5280LF, ±0.2 ppm stability
   * - External Clock Input
     - U.FL (J16)
     - 10-52 MHz, 1.8V - 3.3V
   * - Clock Output
     - U.FL (J15)
     - 3.3V CMOS

.. warning::
   When using external clock references, ensure signal levels and frequencies match specifications. 
   
   Improper clock signals may cause unstable operation and potential damage to the device.

