# TP-Link-UE300-UE330-Linux-Driver
TP-Link UE300/UE330 Linux Driver (based on Realtek 8153 chipset)

# Linux driver for TP-Link UE300/UE330 (based on Realtek RTL8153)

This repository features a Linux driver for TP-Link UE300/UE330 USB to Ethernet adapters, which are based on Realtek RTL8153 chipset.

Even though the driver for this chipset is now included in the Kernel, but for some odd reasons, devices utilising this driver misbehave significantly. One of which is random connection dropouts that happens without any reason!

This is the only driver release that I found addressing the above mentioned issue permamnently. 

Tested on 'Ubuntu 18.04.1' with kernel '4.15.0-43-generic' and the issue is completely eliminated since.

# Prerequisite

  apt install build-essential dkms libelf-dev
  git clone https://github.com/JulAlx/TP-Link-UE300-UE330-Linux-Driver.git
  
# Compile and Install

  
