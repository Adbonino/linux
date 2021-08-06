 ### Acceso remoto a un Servidor Linux
 
 ```
 # yum install xrdp
 # systemctl status xrdp
 # systemctl enable --now xrdp
 # systemclt status xrdp
 # systemctl status xrdp
 # firewall-cmd --permanent --add-service=vnc-server
 # firewall-cmd --reload
 # systemctl status xrdp
 # firewall-cmd --add-port=3389/tcp --permanent
 # firewall-cmd -reload
 ```
