# FUTURE_CS_02
# Setting Up a Firewall

Step-by-Step Procedure: Parrot OS Firewall Setup
Below is a detailed procedure for setting up and managing a firewall in Parrot OS, limiting and allowing traffic, and ensuring robust documentation.

1. Setting Up a Firewall in Parrot OS
Step 1: Verify Firewall Installation

Open a terminal in Parrot OS.
Check if ufw (Uncomplicated Firewall) is installed:
bash
Copy code
sudo ufw status
If ufw is not installed, install it:
bash
Copy code
sudo apt update
sudo apt install ufw
Step 2: Enable the Firewall

Enable ufw to protect the system:
bash
Copy code
sudo ufw enable
Step 3: Check the Status

Verify the firewall status:
bash
Copy code
sudo ufw status verbose
2. Limiting and Allowing Traffic
Step 1: Allow Specific Traffic

Allow SSH traffic:
bash
Copy code
sudo ufw allow ssh
Allow traffic on a specific port, e.g., HTTP (port 80):
bash
Copy code
sudo ufw allow 80/tcp
Step 2: Block Specific Traffic

Block traffic from a specific IP:
bash
Copy code
sudo ufw deny from 192.168.1.100
Block a specific port, e.g., FTP (port 21):
bash
Copy code
sudo ufw deny 21/tcp
Step 3: Set Default Policies

Deny all incoming traffic by default:
bash
Copy code
sudo ufw default deny incoming
Allow all outgoing traffic by default:
bash
Copy code
sudo ufw default allow outgoing
Step 4: Advanced Rule Management

Limit connections on a port to prevent brute-force attacks:
bash
Copy code
sudo ufw limit ssh
Allow traffic only for a specific subnet:
bash
Copy code
sudo ufw allow from 192.168.1.0/24 to any port 22
