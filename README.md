# Firewall-configuration-homelab

## Overview
This project demonstrates host-based firewall configuration using UFW on Ubuntu 22.04 LTS.
The goal is to enforce network security by applying a default-deny inbound policy while allowing essential services, verified through controlled testing.

## Lab Setup
  - Target VM: Ubuntu 22.04 LTS
  - Client VM: Ubuntu
  - Firewall: UFW(Uncomplicated Firewall)

## Video Demonstration
https://github.com/user-attachments/assets/90406503-0de3-4ba0-9ac3-62727e46e56e

**Key steps demonstrated:** 
1. Baseline testing: SSH allowed with firewall inactive
2. Configure UFW:
   - Default deny incoming
   - Default allow outgoing
3. Enable firewall and observe blocked connections
4. Allow SSH (port 22) through firewall
5. Verify SSH access while other traffic remains blocked 

## Commands Used 

# Check UFW status sudo 
- ufw status verbose 

# Set default policies 
- sudo ufw default deny incoming 
- sudo ufw default allow outgoing 

# Enable firewall 
- sudo ufw enable 

# Allow SSH 
- sudo ufw allow 22/tcp 

# Verify SSH service 
- sudo systemctl status ssh
