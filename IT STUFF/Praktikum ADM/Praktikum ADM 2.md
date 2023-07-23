Disini kita akan setting dns server. tapi sebelum itu kita cobakkan dulu vps kita sebagai client dns.

## Install dig, host dan nslookup
sebelum menggunakan perintah tersebut kita harus terlebih dahulu install library nya dengan syntax:
```centos7
yum install bind-utils
```

## Check DNS Server 
Setelah kita menginstall library tadi, kita bisa mencoba linux sebagai client untuk check DNS Server. Dengan perintah:
```centos7
nslookup google.com
```

```centos7
nslookup -type=ns google.com
```
untuk mencari name server google. ns=name server.

```centos7
nslookup -type=mx google.com
```
mx = mail exchanger. untuk mencari tau mail server nya make apa di google.com.

Pastikan DNS client berjalan pada VPS Masing2 dengan menggunakan perintah:

```centos7
ping yahoo.com
```
kalau ada reply dari ping. berarti name server di vps kita berjalan dengan normal. Kalaut tidak berjalan maka tidak ada reply.

Untuk melihat name server yang kita gunakan:

```centos7
cat /etc/resolv.conf
```

untuk menghapus "seach invalid" kita bisa mengetikkan:

```centos7
vi /etc/resolv.conf
```

## Perintah dig

Perintah DIG (Domain Information Groper) adalah permintaan untuk meminta informasi tentang DNS name server. Perintah ini akan menampilkan lebih lengkap dibandingkan perintah nslookup. kita bisa menggunakan perintah :

```centos7
dig yahoo.com
```

informasi yang diberikan lebih lengkap ketimbang nslookup

## Perintah host

Perintah host adalah tool sederhana untuk DNS lookup utility.  dengan command:

```centos7
host google.com
```

uir masi menggunakan ipv4 belum ipv6.

Untuk mengetahui ip vps kita:

```centos7
hostname -i
```

Untuk mengetahui nameserver vps kita:

```centos7
cat /etc/resolv.conf
```

Setelah mencobakan vps kita sebagai client dns, langkah selanjutnya adalah setting/install dns server di vps kita.

## Install BIND:

```centos7
yum install bind-y
```

## Konfigurasi DNS Server

```centos7
-cd /etc
-cp named.conf named.conf.backup
```

## Konfig file named.conf

```centos7
vi /etc/named.conf
```

setelah kita konfigurasi, kita persiapkan domain. Boleh membeli domain atau provider domain yang memberikan secara gratis. 