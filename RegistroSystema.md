# NTP

```
# timedatectl
# timedatectl list-timezones
# tzselect
# timedatectl set-timezone Antartica/Syowa
setao de hora
# timedatectl set-time 9:00:00
activo el servicio NTP
# timedatectl set-ntp true

Para escoger mi timezone
# tzselect
# timedatectl set-timezone America/Argentina/Buenos_Aires
```

## chronyd

Cambiar los servidores de NTP

```
verifico si esta instalado el paquete
# rpm -qa | grep chrony
# systemctl status chronyd
# chronyc tracking
# chronyc sources -v
# vim /etc/chrony.conf
lo qeu debemos cambiar en la qeu dice pool al prncipio
comentamos 3pool
server ntpserver.com.ar iburst

verifico si mi clietne puede resolver esa direccion
# host ntpserver.com.ar

# systemctl restart chronyd
# chronyc sources -v

CAMBIOS EN EL SERVIDOR
# vim /etc/chrony.conf
Hay una linea qeu dice allow
allow 192.168.20.0/24

# firewall-cmd --list-all
# systemctl restart chronyd


```




























