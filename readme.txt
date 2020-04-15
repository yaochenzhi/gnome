Centos7.7

yum groupinstall -y "GNOME Desktop"
Xorg :1 -configure
mv xorg.conf.new /etc/X11/xorg.conf
systemctl isolate graphical
yum install tigervnc-server
yum install xrdp
yum start xrdp
yum enable xrdp
firewall-cmd --add-port=3389/tcp --zone=public --permanent
firewall-cmd --reload
systemctl list-units --type service


# vnc
# xrdp
# isolate
# rescue mode
# single-user mode
# sshd
# pam
# nologin
# firewall