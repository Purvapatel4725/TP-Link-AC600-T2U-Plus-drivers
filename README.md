# TP-Link AC600 T2U Plus Drivers Installation on Linux

Welcome to the TP-Link AC600 T2U Plus drivers installation guide for Linux! This repository provides a comprehensive step-by-step process to get your TP-Link AC600 T2U Plus wireless adapter up and running on a Linux system.

## Prerequisites

Before starting, ensure you have the following:

- A Linux system with `apt` package manager.
- An active internet connection.
- USB settings configured correctly if using a virtual machine.
- Most importantly a **TP-Link AC600 T2U Plus** Network adapter

## Step-by-Step Installation

Follow these steps to install the drivers:

### 1. Update the Current Repository

First, update the current repository to ensure you have the latest package information:

```bash
sudo apt update
```

### 2. Upgrade System Packages

Upgrade your system to the latest versions of all packages:

```bash
sudo apt upgrade
```

**Note:** After updating and upgrading, it is recommended to restart your machine.

### 3. Install DKMS and Git

Install the DKMS (Dynamic Kernel Module Support) and Git tools:

```bash
sudo apt install dkms git
```

### 4. Install Build Dependencies

Install the necessary build dependencies for compiling the drivers:

```bash
sudo apt install build-essential libelf-dev linux-headers-$(uname -r)
```

### 5. Clone the Driver Repository

Clone the official drivers repository from GitHub:

```bash
git clone https://github.com/aircrack-ng/rtl8812au
```

### 6. Navigate to the Local Repository

Change directory to the newly cloned repository:

```bash
cd rtl8812au
```

### 7. Install the Drivers

Finally, install the drivers using DKMS:

```bash
sudo make dkms_install
```

### Additional Notes

- Ensure you manually select the USB from the settings if you are running a virtual machine and the network adapter is not detected after the `lsusb` command.
- Restart your machine if the network adapter is still not recognized after installation.

## Conclusion

You should now have the TP-Link AC600 T2U Plus drivers installed and your wireless adapter ready for use. If you encounter any issues, refer to the [official GitHub repository](https://github.com/aircrack-ng/rtl8812au) for additional support and updates.

## Author
**Purva Patel**

