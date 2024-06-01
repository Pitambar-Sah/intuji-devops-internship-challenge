# intuji-devops-internship-challenge
<br>
##Bash Script for Installing Docker 
Introduction:
Docker is a powerful tool that enables developers to build, deploy, and manage applications using containers. These containers allow for seamless deployment across different environments, making it easier to maintain consistency and portability. Installing Docker on Kali Linux, a popular distribution used for penetration testing and digital forensics, can provide developers with a flexible and efficient environment for their projects.

Step 1:
Update Package Lists Before installing Docker, it’s essential to ensure that the package lists are up-to-date. This helps in fetching the latest versions of packages and dependencies.

#!/bin/bash
# Update package lists
echo "Updating package lists…"
sudo apt-get update
# Upgrade installed packages
echo "Upgrading installed packages…"
sudo apt-get upgrade -y
# Perform distribution upgrade (if available)
echo "Performing distribution upgrade (if available)…"
sudo apt-get dist-upgrade -y
# Remove unused packages
echo "Removing unused packages…"
sudo apt-get autoremove -y
# Clean up package cache
echo "Cleaning up package cache…"
sudo apt-get autoclean
echo "Kali Linux system is now fully updated."
Save the script to a file, for example, kali_update.sh, and make it executable using the following command

Then, you can execute the script by running:

chmod +x kali_update.sh
./kali_update.sh
Step:02
here’s a Bash script that automates the installation of Docker on Kali Linux:

#!/bin/bash

# Update package lists
sudo apt-get update

# Install Docker
sudo apt-get install -y docker.io

# Start Docker service
sudo systemctl start docker

# Enable Docker to start on boot
sudo systemctl enable docker

# Verify Docker installation
docker --version
You can save this script in a file, for example, install_docker.sh, make it executable, and then run it:

chmod +x install_docker.sh
./install_docker.sh
Conclusion:
In this guide, we’ve covered the step-by-step process of installing Docker on Kali Linux. 
