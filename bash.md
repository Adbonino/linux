
```
[abonino@localhost ~]# echo $SHELL
[abonino@localhost ~]# which bash
/usr/bin/bash
[abonino@localhost ~]# vim s1.sh
read largo
echo "longitud=${#largo}"
((sum=20+30+40))

for ((x=1 ; x<=10 ; x++))
do
   echo $x
done

#otra forma
x=1
while [ $x -le 10 ]
do
   echo "$x"
   ((x++))
done

# otro ejemplo
read id
if [ 0 eq "$id" ]
then
    echo "sos admin"
else
    echo "no sos admin"
fi

# ejemplo final
list=('Centos' 'Redhat' 'Fedora' 'Ubuntu')
for ((x=1 ; x<=3 ; x++))
do
   echo ${list[x]}
done
```
