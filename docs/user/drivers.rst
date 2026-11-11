Driver Installation
###################

This chapter guides through the Xillybus PCIe driver installation for the LimeSDR PCIe board under Windows.

.. note::
  PCIe drivers do not need to be installed on Linux.

Windows PCIe driver installation procedure
******************************************

Download the `latest drivers`_, select the xillybus-windriver-1.2.0.0.zip package and unzip it. The first time the LimeSDR PCIe board is connected to the PC, follow the installation procedure below.

1. Press Start Menu and right click on Computer, select Properties and Device Manager.

.. figure:: /images/LimeSDR-PCIe_drivers_computer_properties.png

  Figure 5. Open computer properties

.. figure:: /images/LimeSDR-PCIe_device_manager.png

  Figure 6. Open device manager

2. When the LimeSDR PCIe board is plugged in, it appears in Device Manager as PCI Device under Other devices. Right click on the PCI device and select Update Driver Software.

3. Select Browse my computer for driver software (Figure 7) and in the browse window (Figure 8) choose the driver from the downloaded package (extracted files from xillybus-windriver-1.2.0.0.zip).

.. figure:: /images/LimeSDR-PCIe_drivers_select_drivers.png
  :width: 600

  Figure 7. Browse for driver software

.. figure:: /images/LimeSDR-PCIe_drivers_select_path.png
  :width: 600

  Figure 8. Select driver location

4. After selecting the driver files and clicking the Next button, a Windows security warning might appear. Check Always trust software from “Xillybus Ltd” and click Install.

.. figure:: /images/LimeSDR-PCIe_drivers_security_warning.png
  :width: 600

  Figure 9. Windows security warning

5. After successful installation (Figure 10), “Xillybus driver for generic FPGA interface” will appear under Xillybus device (Figure 11).

.. figure:: /images/LimeSDR-PCIe_drivers_success.png
  :width: 600

  Figure 10. Successful LimeSDR PCIe driver installation

.. figure:: /images/LimeSDR-PCIe_drivers_device_manager_after_installation.png

  Figure 11. Device manager window after installation

.. _latest drivers: http://xillybus.com/downloads/xillybus-windriver-1.2.0.0.zip
