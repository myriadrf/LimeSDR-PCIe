Reference Clock
###############

The LimeSDR PCIe clock system is based on a high stability 30.72 MHz VCTCXO (Voltage Controlled Temperature Compensated Crystal Oscillator), which can be tuned via the onboard DAC or locked to an external reference clock via the onboard phase detector.

The board provides U.FL connectors for reference clock input (J16) and output (J15). The clock output is not connected by default. To enable it, fit R122 (v1.3) or R121 (v1.2).

.. figure:: /images/LimeSDR-PCIe_v1.3_user_clockcon.png
  :width: 600

  Figure 4. LimeSDR PCIe v1.3 board top with reference clock connector positions

Figure 4 shows the reference clock connector positions on LimeSDR PCIe v1.3. LimeSDR PCIe v1.2 boards use the same connector designators. Clock functions are listed in Table 3.

.. list-table:: Table 3. Clock functions
   :header-rows: 1
   :stub-columns: 1

   * - Function
     - Specification
     - Notes
   * - Onboard oscillator
     - 30.72 MHz VCTCXO
     - Rakon E5280LF, ±0.2 ppm stability
   * - External clock input
     - U.FL (J16)
     - 10–52 MHz, 1.8 V–3.3 V
   * - Clock output
     - U.FL (J15)
     - 3.3 V CMOS, not connected by default

.. warning::
   When using external clock references, ensure signal levels and frequencies match specifications.

   Improper clock signals may cause unstable operation and potential damage to the device.
