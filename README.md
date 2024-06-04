<<<<<<< HEAD
#This project demonstrates how to use rclone to transfer files to Google drive, using a virtual linux environment from the host os as windows

## Prerequisites

- Chocolatey (package manager for windows for easy installation)
- Vagrant
- VirtualBox
- Amazon S3 account with Access Key ID and Secret Access Key
- Gitbash ( I have used the gitbash terminal to integrate Virtual Box and Vagrant)
## Setup

1. Install chocolatey package manager for windows
2. Install Vagrant,Gitbash and VirtualBox using chocolatey.
3. Set up and start your Vagrant CentOS VM:
   vagrant init centos/8
   vagrant up
   vagrant ssh
4. Install rclone on the CentOS VM:

   #using yum (if rclone is available in your yum repository)
   - check if rclone is available
   - sudo yum update -y
   - sudo yum whatprovides rclone
   - if present: sudo yum install rclone -y

   #manually ( helps you install the latest version of rclone)
   - sudo yum install -y curl unzip
   - curl -O https://downloads.rclone.org/rclone-current-linux-amd64.zip
   - unzip rclone-current-linux-amd64.zip
   - cd rclone-(special char)-linux-amd64
   - sudo cp rclone /usr/local/bin/
   - sudo chown root:root /usr/local/bin/rclone
   - sudo chmod 755 /usr/local/bin/rclone
5. Configure rclone with your google drive client-id :
   - rclone config
   - enter the scopes
6. To copy a file to Google drive, use the following command:
   - rclone copy testfile.txt remote/folder (for any folders)
   - rclone copy testfile.txt remote (to copy into the root folder)
   - rclone copy testfile.txt gdrive


=======
# rclone-gdrive-project
rclone is used to copy files to google drive
>>>>>>> b8884d0ecb1be06c1f67fc22f09a84c240f3d9f2
