Launch to Ubuntu VM in GCP.
SSH into the VM.
sudo su
apt update 
apt upgrade
apt install ubuntu-desktop -y
apt install kde-plasma-desktop -y
apt install ubuntu-mate-core -y
apt install xubuntu-core -y
apt install lightdm -y
systemctl start lightdm.service
service ligthdm start

How to Remove desktop version

apt autoremove ubuntu-desktop
systemctl stop lightdm.service
apt autoremove lightdm



SECOND METHOD TO INSTALL

sudo apt update
sudo apt install --assume-yes wget tasksel
wget https://dl.google.com/linux/direct/chrome-remote-desktop_current_amd64.deb
sudo apt-get install --assume-yes ./chrome-remote-desktop_current_amd64.deb

# need to install a desktop environment and window manager for Chrome Remote Desktop to communicate with the VM instance.

sudo tasksel install ubuntu-desktop
sudo bash -c ‘echo “exec /etc/X11/Xsession /usr/bin/gnome-session” > /etc/chrome-remote-desktop-session’
sudo reboot   (loose connectivity)
https://remotedesktop.google.com/headless    (setup via ssh)
Copy the command for Debian Linux
