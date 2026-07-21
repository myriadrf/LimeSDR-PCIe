Board temperature control
#########################

LimeSDR PCIe has integrated temperature sensor which can control FAN to keep board in operating temperature range. FAN must be connected to J14 (0.1” pitch) connector. FAN control voltage is 12V. Fan will be turned on if board will heat up to 55°C and FAN will be turned off if board will cool down to 45°C. FAN control temperature range is set by FPGA.



.. figure:: /images/LimeSDR-USB_1v4_fan_control_hyst.png
  :width: 600
  
  Figure 10: FAN control temperature hysteresis 

Temperature sensor output (LM75_OS) is connected to FPGA pin K14. FAN MOSFET can be controlled from FPGA pin K13 (FAN_CTRL).

Measured temperature value can read by using LimeSuiteGUI.

