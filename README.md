# Quick PSA 
1. create vm, I am using Ubuntu 24-04

2. Wait for it to start and send the public ip + the port to Rokas, or maybe append this readme. also use the password i sent in groupchat

3. Log in to the VNC through nebula enter your username nasuxxxx

4. Set the password
   sudo passwd nasuxxxx

Thats it, everything else will be set up from the main vm
	 
# The ansible-vm part
1. create ubuntu 22.04 vm with 8 GB of disk
2. enter into it
3. run: 
```
su # to become root
cd ~ # to go to root's home dir (important!)
apt update
apt -y install git
git clone https://github.com/dmitru4ok/virtualization-project.git
cd virtualization-project/telecomms/shell
chmod +x Main.sh
./Main.sh
```
4. The script will ask you for your OpenNebula creadentials.
5. then ansible-vm long updating will start
6. after that, it will create webserver-vm, client-vm, and db-vm without any config. It will also populate hosts file with VM private ips
