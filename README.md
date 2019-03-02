# RDP-on-remote-server
 
 Configure RDP on remote Centos 7 server, which has no graphical interface 
 
 1.Install GNOME
 
  yum groups -y remove "GNOME Desktop"
 
  yum groups -y install "GNOME Desktop"
 
 2.Enable EPEL and NUX repositories
 
  rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
 
  rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-1.el7.nux.noarch.rpm
 
 3.Install and setup xrdp and tigervnc
 
  yum -y install xrdp tigervnc-server
 
  systemctl start xrdp.service
 
  To start xrdp with the system start:
 
  systemctl enable xrdp.service
 
