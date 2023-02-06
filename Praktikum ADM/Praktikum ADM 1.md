## Cara cek ip address
Cara cek ip address dengan menggunakan command :
```centos7
ip addr
```

```ad-warning

ip addr hanya bekerja pada linux centos. ipconfig biasanya bisa dipakai untuk melihat ip address pada distro linux lainnya. tetapi tidak berjalan pada centos. Kalau di windows, biasanya pake ipconfig
```

## Cara melihat versi linux Centos nya
bisa dengan memakai perintah :
```centos7
cat /etc/redhat-release
```

## Cara mengupdate versi linux Centos nya
bisa dengan memakai perintah :
```centos7
yum -y update
```

## Syntax-Syntax Linux Centos
```centos7
su
```
 su itu adalah kepanjangan dari super user yang berfungsi untuk membuat user agar sama levelnya dengan root. Jadi bisa menerapkan berbagai macam command yang sama dengan root. su jarang dipakai pada praktikum ini karena cukup dengan menggunakan root saja.

```centos7
adduser
```
adduser adalah self explanatory, gunanya adalah untuk menambah user.
contoh: 
```centos7
adduser reihan
```

```centos7
passwd
```
untuk mengganti password. Contoh:
```centos7
passwd reihan
```

```centos7
cd
```
untuk change direktori. 

```centos7
pwd
```
untuk mengetahui saat ini berada di direktori mana.

```centos7
mkdir
```
untuk membuat direktori/folder.

```centos7
ls
```
untuk melihat apa apa saja isi dari folder/direktori. menampilkan list file dan folder.

```centos7
rmdir
```
untuk menghapus direktori.

```centos7
rm
```
untuk menghapus file

```centos7
cp
```
untuk copy file / folder

```centos7
mv
```
untuk move file/folder

```centos7
vi
```
perintah dasar untuk edit file
## SELinux pada Centos7
SELinux berguna sebagai pengaturan keamanan untuk membatasi aksesi ke modul kernel tertentu.

Fitur ini digunakan secara standar pada CENTOS untuk memberikan keamanan tambahan.

Agar kita bisa mensetting linux tanpa ada warning security, kita harus mengdisable SELinux.

Untuk memastikan SELinux Disable dengan command:
```centos7
sestatus
```

Cara untuk disable SELinux Centos7:
```centos7
vi /etc/sysconfig/selinux
```

