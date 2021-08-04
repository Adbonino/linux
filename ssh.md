# SSH

Archivos involucrados:

/etc/ssh/ssh_known_hosts
~/.ssh/known_hosts
~/.ssh/config


### Generar una llave SSH sin passphrase

```
$ ssh-keygen
$ ls .ssh
$ ssh-copy-id 10.54.118.28
$ ssh 10.54.118.28
```

Permisos de los archivos generados:

```
[abonino@server1 ~]$ ls -al .ssh
total 28
drwx------.  2 abonino abonino  116 Aug  4 15:16 .
drwx--x--x. 14 abonino abonino 4096 Aug  4 15:12 ..
-rw-------.  1 abonino abonino  569 Aug  4 15:10 authorized_keys
-rw-------.  1 abonino abonino 2622 Aug  4 15:07 id_rsa
-rw-r--r--.  1 abonino abonino  582 Aug  4 15:07 id_rsa.pub
-rw-------.  1 abonino abonino 2675 Aug  4 15:13 key_pass
-rw-r--r--.  1 abonino abonino  582 Aug  4 15:13 key_pass.pub
-rw-r--r--.  1 abonino abonino  174 Aug  4 15:08 known_hosts
[abonino@server1 ~]$
```

### Generar una llave SSH con passphrase

```
$ ssh-keygen
$ ls .ssh
$ ssh-copy-id -i .ssh/key_pass.pub 10.54.118.28
$ ssh 10.54.118.28
$ ssh -i .ssh/key-pass 10.54.118.28
```

### Automatizar el ingreso del passphrase

```
$ eval $(ssh-agent)
$ ssh-add .ssh/key_pass
$ ssh 10.54.118.28
$ ssh -i .ssh/key_pass 10.54.118.28
```
