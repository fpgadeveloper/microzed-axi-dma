SDK Project files
=================

How to make use of these files
------------------------------

In order to make use of these source files, you must first generate
the Vivado project hardware design (the bitstream) and export the design
to SDK. Check the Vivado folder for instructions on doing this from Vivado.

Once the bitstream is generated and exported to SDK, you will then have
to create an SDK workspace from scratch.

How to build the SDK workspace
------------------------------

### Create the hardware platform

1. Run Xilinx SDK
2. Select this folder as your SDK workspace (the folder where this
readme file is located).
3. SDK will then open an empty workspace. Select File->New->Project.
4. In the New Project Wizard, select Xilinx->Hardware Platform
Specification. Click Next.
5. In the Target Hardware Specification window, click Browse.
6. Browse to the "EDK/SDK/SDK_Export/hw" folder and select the
"system.xml" file.
7. The project name should be automatically named "EDK_hw_platform".
Make sure that the name is spelt exactly like that and click Finish.

After completing those steps you should have an SDK workspace with a
single project named "EDK_hw_platform".

### Import the application and BSP

1. Select File->Import.
2. In the Import window, select General->Existing projects into
workspace. Click Next.
3. Click Browse, and select this folder (the folder where this
readme file is located).
4. Ensure that both the application and BSP are ticked, then click
Finish.

Build and run your application
------------------------------

Before trying to run your code, wait a while for SDK to build the
application. It should be automatic, but if it doesn't start by
itself, you can always select Project->Build All. It can sometimes
take a while, check the progress at the bottom right corner of the
SDK window.

### To run the application:

1. Power up your hardware platform and ensure that the JTAG is
connected properly.
2. Select Xilinx Tools->Launch Hardware Server. You only have to
do this once, only do it again after rebooting your PC.
3. Select Xilinx Tools->Program FPGA. You only have to do this
once, each time you power up your hardware platform.
4. Select Run->Run to run your application. You can modify the code
and click Run as many times as you like, without going through
the other steps.


Jeff Johnson
http://www.fpgadeveloper.com
