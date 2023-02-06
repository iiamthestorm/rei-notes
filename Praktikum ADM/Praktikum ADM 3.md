# SETTING DNS
Setelah kita mendapatkan domain yang diinstruksi pada pertemuan sebelumnya, kita bisa mengikut langkah2 ini: 
![[Pasted image 20230206090008.png]]

## setting zona
```centos7
zone "admserver.top" IN {
-type master;
-file "/var/named/db.admserver.top";
-allow-update { none; };
};
```
![[Pasted image 20230206090348.png]]

## buat file db.admserver.top
![[Pasted image 20230206090643.png]]

## aktifkan service dns
```centos7
systemctl start named
systemctl enable named
```

test status dengan :
```centos7
systemctl status named 
```
 
jika terjadi balasan seperti "network unreachable resolving" maka cek dulu:
```centos7
vi /etc/named.conf
```
kita tutup ipv6 dengan mengetikkan tanda \\\\ pada "listen-on-v6 port 53".

kita cek zona, kemudian kita ganti 
```centos7
vi /etc/sysconfig/named
```

kita tambahkan dipaling bawah:
![[Pasted image 20230206092044.png]]

setelah itu kita restart dengan:
```centos7
systemctl restart named
```
cek status:
```centos7
systemctl status named
```
supaya dilocalhost juga kita masukkan sebagai name server :
```centos7
vi /etc/resolv.conf
```
![[Pasted image 20230206092307.png]]
kita masukkan name server yang paling atas sebagai localhost.

kita uji dns server dengan
```centos7
nslookup admserver.top
```
![[Pasted image 20230206092406.png]]


