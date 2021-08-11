NFS

Metodo indirecto

cat /etc/auto.master.d/public.autofs
nfs -rw,sync 10.0.0.24:/srv/nfs


Metodo directo
```
# vim /etc/auto.master.d/public.autofs
/- 
```

LAB_NFS:

```
# yum install autofs -y
# echo "/- /etc/auto.direct"  >> /etc/auto.master.d/direct.autofs
# echo "/externo  -rw,sync,fstype=nfs4 10.0.0.24:/srv/direct/externo" >> /etc/auto.direct
# sytemctl enable --now autofs
# systemctl stauts autofs
# cd /externo/

```

