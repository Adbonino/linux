# SSH

### Generar una llave SSH sin passphrase

```
$ ssh-keygen
$ ls .ssh
$ ssh-copy-id 10.54.118.28
$ ssh 10.54.118.28
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
