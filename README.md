# My Cybersecurity Homelab Setup

![License Badge](https://img.shields.io/badge/license-MIT-blue.svg)
![Version Badge](https://img.shields.io/badge/version-1.0.0-green.svg)

## Description
A brief description of your project, its purpose, and what problem it solves.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Installation
In order to successfully setup a homelab, all the necessary software must be installed. Here I will present a list of handy tools that can be used by anyone who is interested in building his/her own homelab.

### Step 1 - Hypervisor

Choose a **hosted** or **type 2 hypervisor** of your choice. Among the most commonly used hypervisors in the industry we can find:

- VMware Workstation Pro
- Oracle VM VirtualBox
- Microsoft Hyper-V

**Additional security tip:** When downloading a hypervisor installer remember to get it <ins>checksum</ins> to ensure if the file you downloaded is approved by its developer and doesn't contain any malicious code.

For Windows - to get the **hash** - Open PowerShell > type ``` Get-FileHash "INSERT YOUR FILE PATH"  ```

Then you copy the hash directly from the official website you downloaded the installer-file from and compare it with the hash gotten from PowerShell - a handy text compare tool is <a href="https://www.diffchecker.com/text-compare">Diffchecker</a>.

### Step 2 - Installer Image / Virtual Machine

As soon as your hypervisor is correctly installed on your device, you can get into downloading a **operation system** that will be run on your hypervisor as a **virtual machine**

In the realm of cybersecurity one of the most widely used Linux distribution is called <a href="https://www.kali.org/">Kali</a>. This distribution is known as a penetration testing platform that contains vast amount of tools an utilities used by cybersecurity professionals.

**Kali** offers two ways of installation:

- **Image installer** (requires more configuration, yet offers more control over hardware access).
- **Pre-built Virtual Machine** (faster to setup but offers less hardware access).

The suggested way of installation for absolute beginners is to choose the method number two - **Pre-built Virtual Machine**.

### Things to keep in mind:
- #### Virtual Machine =/= Sandbox
    - An execution of malware on your VM can lead to infecting your host machine.
- #### Create Snapshot, then "break things"
    - It's crucial to always have ability to bring back your machine to its previous state in which the infection hasn't happened yet.

- #### Properly allocate your resources
    - Be fully aware of how much of your machine's resources can be allocated to your VMs. Going overboard with allocating too large amount of resources can be fatal for your host machine's hardware.

### Step 3 - (IMPORTANT) Properly setting up your VMs
#### Common networking configurations
- Bridged (not recommended) - This configuration links yours guest machine directly to your host machine's network, which may cause potential infection and damage of your host.
- NAT (Network Address Translation) Networking - assigns  a single IP to your private network devices - this helps to conserve the limited amount of your IPv4 addresses and also enhances security by obscuring your internal IP address.
- Host-Only Networking
- Custom Networking Configuration

# FINISHED HERE - Properly setting up your VMs - (2/3)


## Features
- Feature 1
- Feature 2
- Feature 3

## Installation
Step-by-step instructions to set up your project locally.

```bash
# Clone the repository
git clone https://github.com/yourusername/your-repo.git

# Navigate to the project directory
cd your-repo

# Install dependencies
npm install
