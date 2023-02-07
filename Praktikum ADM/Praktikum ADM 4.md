# INSTALLASI WEB SERVER
![[Pasted image 20230206092535.png]]

## Install Apache
lakukan install apache dengan:
```centos7
yum install httpd
```

## Activate Apache
aktivasi dengan:
```centos7
systemctl start httpd
```

## Verifikasi Apache
verifikasi dengan:
```centos7
systemctl status httpd
```

## Konfigurasi Firewall
![[Pasted image 20230206092938.png]]
jikta firewall is not running pada port yang 80 maka atasi dengan:
```centos7
systemctl status firewalld
```
```centos7
systemctl start firewalld
```
kemudian ulangi langkah dengan port 80.

![[Pasted image 20230206094846.png]]


