# TP-Link-UE300-UE330-Linux-Driver
TP-Link UE300/UE330 Linux Driver (based on Realtek 8153 chipset)

# Linux driver for TP-Link UE300/UE330 (based on Realtek RTL8153)

This repository features a Linux driver for TP-Link UE300/UE330 USB to Ethernet adapters, which are based on Realtek RTL8153 chipset.

Even though the driver for this chipset is now included in the Kernel tree, but for some odd reasons, devices utilising this driver misbehave significantly. One of which is random connection dropouts that happens without any reason!

This is the only driver release that I found addressing the above mentioned issue permamnently. 

Tested with UE330 on 'Ubuntu 18.04.1' with kernel '4.15.0-43-generic' and the issue is completely eliminated since.

# Prerequisite

  <code>apt install build-essential dkms libelf-dev</code>
  
  <code>git clone https://github.com/JulAlx/TP-Link-UE300-UE330-Linux-Driver.git</code>
  
# Compile and Install
  
  <code>cd ./TP-Link-UE300-UE330-Linux-Driver/r8152-2.08.0</code>
  
  <code>make && make install</code>
  
  <code>depmod -a</code>
  
# Configuring DKMS

This step is optional but it would help to auto-compile the driver upon a kernel upgrade.

  <code>make clean</code>
  
  <code>cd ..</code>
  
  <code>cp -R . /usr/src/</code>
  
  <code>dkms add -m r8152 -v 2.08.0</code>

That's it!
