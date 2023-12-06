# Jarkom-Modul-4-A03-2023

### Kelompok A03

#### Kalyana Putri Al Kanza / 5025211137

## Topologi soal

![image](https://cdn.discordapp.com/attachments/1181618299046477984/1181618370915881040/topologi_soal.png?ex=6581b6dd&is=656f41dd&hm=170be8140c2f51787080a4ae0dd4df2ab62ad22512f50519a29b097f32f8776f&)

## Pembagian Subnet             

<img width="556" alt="subnet" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/4a40af2b-ff1a-4ca0-aaa9-138b740f5885">

# CIDR

## Langkah 1

Tentukan subnet yang ada dalam topologi dan lakukan labelling netmask terhadap masing-masing subnet. 

![image](https://cdn.discordapp.com/attachments/1181618299046477984/1181624830328586342/image.png?ex=6581bce1&is=656f47e1&hm=6d6ac4917500623078b6950472bbd403a2dedfd05ceff42fdccd814eeca25dd2&)

## Langkah 2

Lakukan penggabungan subnet dari subnet yang paling jauh dari internet. Subnet yang digabung tersebut akan membentuk sebuah subnet lebih besar dari subnet-subnet kecil yang ada di dalamnya. Lalu ulangi langkah tersebut sampai menjadi sebuah subnet besar yang mencakup 1 topologi yang kita milik

### Iterasi 1

<img alt="1" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/3188428f-e40c-409d-9a51-b7ea12f19833">

### Iterasi 2

<img alt="2" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/01a6c729-73a7-4ca1-9037-093494ffe9a3">

### Iterasi 3

<img alt="3" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/e44bed49-dbb4-47ae-8431-a927ed86a0c9">

### Iterasi 4

<img alt="4" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/14a4aada-cbbf-4046-874b-1b17e6e0d40e">

### Iterasi 5

<img alt="5" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/dd71aa1a-3c45-412e-b047-700f6a5e5422">

### Iterasi 6

<img alt="6" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/a8ffdf17-ab9e-4ad4-b96f-78b46806cdc7">

### Iterasi 7

<img alt="7" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/058911de-06ed-498c-975d-d9cb03da90b6">

### Iterasi 8

<img alt="8" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/01a0d756-a099-4517-ad60-69505f03236a">

### Iterasi 9

<img alt="9" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/c1d35f22-b74f-4e49-b3d7-ea929976db5f">

### Iterasi 10

<img alt="10" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/eb47ac45-5ad6-401b-8bf7-1d4887960321">

### Iterasi 11

<img alt="11" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/80da24bf-9f70-48e2-8b15-8274089ea03f">

## Langkah 3 

Dari proses penggabungan yang telah dilakukan, didapatkan sebuah subnet besar dengan netmask /21. Kali ini dapat menggunakan NID 192.170.0.0, netmask 255.255.248.0.

## Langkah 4 

Hitung pembagian IP dengan pohon berdasarkan penggabungan subnet yang telah dilakukan.

![image](https://cdn.discordapp.com/attachments/1181618299046477984/1181618371196878908/tree_cidr.jpg?ex=6581b6dd&is=656f41dd&hm=569dde914893c49fdddb0b693ec8a54f460a899ec94085eefe8e63ca28ea13b2&)

## Langkah 5

Berdasarkan penghitungan, maka didapatkan pembagian IP sebagai berikut:

![image](https://media.discordapp.net/attachments/1181618299046477984/1181628924367732846/image.png?ex=6581c0b1&is=656f4bb1&hm=29f22fad21d96b4edda1c1755efc0d86c583614146e238110e4acdd9800bf159&=&format=webp&quality=lossless&width=867&height=663)

## Langkah 6

Di Cisco Packet Tracer, buat topologi sebagai berikut.

<img alt="image" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/5617b33b-0299-40c9-b3d7-074e8d70d1c4">

Untuk subnetting, lakukan konfigurasi IP dan subnet pada router, client, dan server dengan subnet sesuai tabel di langkah 4 dan IP sesuai gambar berikut:

![image](https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/9b98aa85-b771-499f-9336-a995ddba73b1)

## Langkah 7

Lakukan konfigurasi pada masing-masing router sebagai berikut untuk routing:

### Aura

```
192.170.64.0/27 via 192.170.128.2
192.170.0.0/21 via 192.170.128.2
192.170.8.0/30 via 192.170.128.2
192.170.32.0/30 via 192.170.128.2
192.170.20.8/30 via 192.170.128.2
192.170.20.8/30 via 192.170.128.2
192.170.20.0/29 via 192.170.128.2
192.172.80.0/29 via 192.172.128.2
192.172.80.8/30 via 192.172.128.2
192.172.72.0/30 via 192.172.128.2
192.172.32.0/30 via 192.172.128.2
192.172.8.0/30 via 192.172.128.2
192.172.64.0/22 via 192.172.128.2
192.172.68.0/24 via 192.172.128.2
192.172.16.0/23 via 192.172.128.2
192.172.4.0/26 via 192.172.128.2
192.172.0.0/22 via 192.172.128.2
192.171.0.0/24 via 192.171.1.2
```

### Eisen

```
0.0.0.0/0 via 192.172.128.1
192.172.64.0/22 via 192.172.72.2
192.172.68.0/24 via 192.172.72.2
192.172.16.0/23 via 192.172.32.2
192.172.8.0/30 via 192.172.32.2
192.172.4.0/26 via 192.172.32.2
192.172.0.0/22 via 192.172.32.2
```

### Linie

```
192.172.4.0/26 via 192.172.8.2
192.172.0.0/22 via 192.172.8.2
0.0.0.0/0 via 192.172.32.1
```

### Lawine

```
192.172.0.0/22 via 192.172.4.2
0.0.0.0/0 via 192.172.8.1
```

### Frieren

```
192.170.8.0/30 via 192.170.32.2
192.170.0.0/21 via 192.170.32.2
192.170.16.0/22 via 192.170.32.2
192.170.20.8/30 via 192.170.32.2
192.170.20.0/29 via 192.170.32.2
0.0.0.0/0 via 192.170.128.1
```

### Flamme

```
192.170.0.0/21 via 192.170.8.2
192.170.20.0/29 via 192.170.20.10
0.0.0.0/0 via 192.170.32.1
```

### Fern

```
0.0.0.0/0 via 192.170.8.1
```

### Himmel

```
0.0.0.0/0 via 192.170.20.9
```

### Heiter

```
0.0.0.0/0 via 192.172.4.1
```

### Lugner

```
0.0.0.0/0 via 192.172.72.1
```

### Denken

```
0.0.0.0/0 via 192.171.1.1
```

## Testing

### Dari router

<img alt="router" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/50a9f12f-4cea-4ba9-8884-e93ef54417a7">

### Dari server

<img alt="server" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/aa0573c5-1039-4acb-89de-83d36cf68c9d">

### Dari client

<img alt="client" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/089ae8d3-f537-4a70-b55e-ae72fa30ce7f">


# VLSM

## Langkah 1

Tentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan lakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan.

![image](https://cdn.discordapp.com/attachments/1181618299046477984/1181624830328586342/image.png?ex=6581bce1&is=656f47e1&hm=6d6ac4917500623078b6950472bbd403a2dedfd05ceff42fdccd814eeca25dd2&)

## Langkah 2

Subnet besar yang dibentuk memiliki NID 192.168.1.0 dengan netmask /24. Perhitungan pembagian IP dilakukan berdasarkan NID dan netmask tersebut menggunakan pohon seperti gambar di bawah.

![image](https://cdn.discordapp.com/attachments/1181618299046477984/1181618371511464018/tree_vlsm.jpg?ex=6581b6dd&is=656f41dd&hm=43bb0f504c2ffa6a8c0829fb56fb716a0f0571e49eb656a68d1558c8229243f7&)

## Langkah 3

Lakukan subnetting dengan menggunakan pohon tersebut untuk pembagian IP sesuai dengan kebutuhan masing-masing subnet yang ada.

![image](https://cdn.discordapp.com/attachments/1181618299046477984/1181885106948935740/Untitled_-_tree_vlsm_1.jpg?ex=6582af47&is=65703a47&hm=99432c96fee071c8f08f0908f312a7cab413842df2c33bf8f16adae1508ec85d&)

Dari pohon dari pohon tersebut akan mendapat pembagian IP sebagai berikut.

![image](https://cdn.discordapp.com/attachments/1181618299046477984/1181629727014916186/image.png?ex=6581c170&is=656f4c70&hm=4168bade9f7be15e7936adeaa3749f96a47d866d0f25f2300d92a2460b97a6cb&)

## Langkah 4

Di GNS3, lakukan konfigurasi pada masing-masing router, client, dan server, sebagai berikut untuk subnetting:

### Aura

```
auto eth0
iface eth0 inet dhcp
up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.170.0.0/16

auto eth1
iface eth1 inet static
	address 192.170.0.5
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.170.0.37
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 192.170.0.33
	netmask 255.255.255.252
```

### Denken

```
auto eth0
iface eth0 inet static
	address 192.170.0.38
	netmask 255.255.255.252
	gateway 192.170.0.37
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.1.1
	netmask 255.255.255.0
```

### Eisen

```
auto eth0
iface eth0 inet static
	address 192.170.0.6
	netmask 255.255.255.252
	gateway 192.170.0.5
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.0.9
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.170.0.13
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 192.170.0.41
	netmask 255.255.255.248

auto eth4
iface eth4 inet static
	address 192.170.0.1
	netmask 255.255.255.252
```

### Lugner

```
auto eth0
iface eth0 inet static
	address 192.170.0.10
	netmask 255.255.255.252
	gateway 192.170.0.9
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.16.1
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.170.2.1
	netmask 255.255.252.0

```

### Linie

```
auto eth0
iface eth0 inet static
	address 192.170.0.14
	netmask 255.255.255.252
	gateway 192.170.0.13
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.0.17
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.170.4.1
	netmask 255.255.254.0

```

### Lawine

```
auto eth0
iface eth0 inet static
	address 192.170.0.18
	netmask 255.255.255.252
	gateway 192.170.0.17
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.0.129
	netmask 255.255.255.192
```

### Heiter

```
auto eth0
iface eth0 inet static
	address 192.170.0.130
	netmask 255.255.255.192
	gateway 192.170.0.129
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.12.1
	netmask 255.255.252.0
```

### Frieren

```
auto eth0
iface eth0 inet static
	address 192.170.0.34
	netmask 255.255.255.252
	gateway 192.170.0.33
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.0.65
	netmask 255.255.255.192

auto eth2
iface eth2 inet static
	address 192.170.0.29
	netmask 255.255.255.252
```

### Flamme

```
auto eth0
iface eth0 inet static
	address 192.170.0.30
	netmask 255.255.255.252
	gateway 192.170.0.29
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.0.25
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.170.8.1
	netmask 255.255.252.0

auto eth3
iface eth3 inet static
	address 192.170.0.21
	netmask 255.255.255.252
```

### Fern

```
auto eth0
iface eth0 inet static
	address 192.170.0.26
	netmask 255.255.255.252
	gateway 192.170.0.30
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.24.1
	netmask 255.255.248.0
```

### Himmel

```
auto eth0
iface eth0 inet static
	address 192.170.0.22
	netmask 255.255.255.252
	gateway 192.170.0.21
	up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.170.0.49
	netmask 255.255.255.248
```

### RoyalCapital

```
auto eth0
iface eth0 inet static
	address 192.170.1.65
	netmask 255.255.255.0
	gateway 192.170.1.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### WilleRegion

```
auto eth0
iface eth0 inet static
	address 192.170.1.2
	netmask 255.255.255.0
	gateway 192.170.1.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### TurkRegion

```
auto eth0
iface eth0 inet static
	address 192.170.16.2
	netmask 255.255.252.0
	gateway 192.170.16.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### GrobeForest

```
auto eth0
iface eth0 inet static
	address 192.170.2.2
	netmask 255.255.255.0
	gateway 192.170.2.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### GranzChannel

```
auto eth0
iface eth0 inet static
	address 192.170.4.2
	netmask 255.255.254.0
	gateway 192.170.4.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### BredtRegion
```
auto eth0
iface eth0 inet static
	address 192.170.0.131
	netmask 255.255.255.192
	gateway 192.170.0.129
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### RiegelCanyon

```
auto eth0
iface eth0 inet static
	address 192.170.12.3
	netmask 255.255.252.0
	gateway 192.170.12.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### LakeKorridor

```
auto eth0
iface eth0 inet static
	address 192.170.0.66
	netmask 255.255.255.224
	gateway 192.170.0.65
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### LaubHills

```
auto eth0
iface eth0 inet static
	address 192.170.0.2
	netmask 255.255.248.0
	gateway 192.170.0.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### AppetitRegion

```
auto eth0
iface eth0 inet static
	address 192.170.1.143
	netmask 255.255.248.0
	gateway 192.170.0.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### RohrRoad

```
auto eth0
iface eth0 inet static
	address 192.170.8.2
	netmask 255.255.252.0
	gateway 192.170.8.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### SchwerMountains

```
auto eth0
iface eth0 inet static
	address 192.170.0.50
	netmask 255.255.255.248
	gateway 192.170.0.49
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Stark

```
auto eth0
iface eth0 inet static
	address 192.170.0.2
	netmask 255.255.255.252
	gateway 192.170.0.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Richter

```
auto eth0
iface eth0 inet static
	address 192.170.0.42
	netmask 255.255.255.248
	gateway 192.170.0.41
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Revolte

```
auto eth0
iface eth0 inet static
	address 192.170.0.43
	netmask 255.255.255.248
	gateway 192.170.0.41
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Sein

```
auto eth0
iface eth0 inet static
	address 192.170.12.2
	netmask 255.255.252.0
	gateway 192.170.12.1
	up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

## Langkah 5

Lakukan konfigurasi pada masing-masing router sebagai berikut untuk routing:

### Aura
```
route add -net 192.170.0.0 netmask 255.255.255.252 gw 192.170.0.6
route add -net 192.170.0.40 netmask 255.255.255.248 gw 192.170.0.6
route add -net 192.170.1.0 netmask 255.255.255.0 gw 192.170.0.38
route add -net 192.170.0.64 netmask 255.255.255.224 gw 192.170.0.34
route add -net 192.170.24.0 netmask 255.255.248.0 gw 192.170.0.34
route add -net 192.170.8.0 netmask 255.255.252.0 gw 192.170.0.34
route add -net 192.170.0.48 netmask 255.255.255.248 gw 192.170.0.34
route add -net 192.170.0.128 netmask 255.255.255.192 gw 192.170.0.6
route add -net 192.170.12.0 netmask 255.255.252.0 gw 192.170.0.6
route add -net 192.170.2.0 netmask 255.255.255.0 gw 192.170.0.6
route add -net 192.170.16.0 netmask 255.255.252.0 gw 192.170.0.6
route add -net 192.170.4.0 netmask 255.255.254.0 gw 192.170.0.6
route add -net 192.170.0.8 netmask 255.255.255.252 gw 192.170.0.6
route add -net 192.170.0.12 netmask 255.255.255.252 gw 192.170.0.6
route add -net 192.170.0.16 netmask 255.255.255.252 gw 192.170.0.6
route add -net 192.170.0.20 netmask 255.255.255.252 gw 192.170.0.34
route add -net 192.170.0.24 netmask 255.255.255.252 gw 192.170.0.34
route add -net 192.170.0.28 netmask 255.255.255.252 gw 192.170.0.34
```

### Eisen
```
route add -net 192.170.16.0 netmask 255.255.252.0 gw 192.170.0.10
route add -net 192.170.2.0 netmask 255.255.255.0 gw 192.170.0.10
route add -net 192.170.4.0 netmask 255.255.254.0 gw 192.170.0.14
route add -net 192.170.0.16 netmask 255.255.255.252 gw 192.170.0.14
route add -net 192.170.0.128 netmask 255.255.255.192 gw 192.170.0.14
route add -net 192.170.12.0 netmask 255.255.252.0 gw 192.170.0.14
```

### Linie 
```
route add -net 192.170.0.128 netmask 255.255.255.192 gw 192.170.0.18
route add -net 192.170.12.0 netmask 255.255.252.0 gw 192.170.0.18
```

### Lawine
```
route add -net 192.170.12.0 netmask 255.255.252.0 gw 192.170.0.130
```

### Frieren
```
route add -net 192.170.24.0 netmask 255.255.248.0 gw 192.170.0.30
route add -net 192.170.0.24 netmask 255.255.255.252 gw 192.170.0.30
route add -net 192.170.8.0 netmask 255.255.252.0 gw 192.170.0.30
route add -net 192.170.0.20 netmask 255.255.255.252 gw 192.170.0.30
route add -net 192.170.0.48 netmask 255.255.255.248 gw 192.170.0.30
```

### Flamme
```route add -net 192.170.24.0 netmask 255.255.248.0 gw 192.170.0.26
route add -net 192.170.0.48 netmask 255.255.255.248 gw 192.170.0.22
```

## Testing

### Client ke client

<img alt="client client" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/137da725-b663-4a75-9afa-69c2e2519fba">

### Ping google dari client

<img alt="client google" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/ba018fcf-63d2-4d35-8eca-f7e4171cbac7">

### Client ke router

<img width="360" alt="client router" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/51a14610-20cd-425e-8094-8aa5029876e0">

### Client ke server

<img alt="client server" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/d6891baf-da85-47f0-a26f-cb0b4ab873b7">

### Ping google dari router

<img alt="router google" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/d07612a5-8ba0-4a9a-a147-53cffd73c271">

### Router ke router

<img alt="router router" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/7f47c878-b218-4c87-ad09-b51abee88a5a">

### Ping google dari server

<img alt="server google" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/e642e3c0-b300-4487-921d-e3e06ed0ee4d">

### Server ke router

<img alt="server router" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/23c788a8-f4f2-4f71-8911-91dc9c7de138">

### Server ke server

<img alt="server server" src="https://github.com/kalyanaalk/Jarkom-Modul-4-A03-2023/assets/107338432/bcffd34a-7ccb-43fc-a90a-7abf00eecf9f">


