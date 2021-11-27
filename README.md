# Jarkom-Modul-4-B10-2021

## Anggota B10
Nama | NRP | Pembagian
------------ | ------------- | -------------
Pramudya Tiandana Wisnu Gautama | 05111940000018 | CIDR CPT
Jason Andrew Gunawan | 05111940000085 | VLSM GNS3
Frans Wijaya | 05111940000098 | VLSM GNS3

## Daftar Isi
- [Jarkom-Modul-4-B10-2021](#jarkom-modul-4-b10-2021)
  * [Anggota B10](#anggota-b10)
  * [Daftar Isi](#daftar-isi)
  * [Topologi](#topologi)
  * [VLSM pada GNS3](#vlsm-pada-gns3)
    + [Langkah 1](#langkah-1)
    + [Langkah 2](#langkah-2)
  * [CIDR pada CPT](#cidr-pada-cpt)
    + [Langkah 1](#langkah-1-1)
    + [Langkah 2](#langkah-2-1)
    + [Langkah 3](#langkah-3)
    + [Langkah 4](#langkah-4)
    + [Langkah 5](#langkah-5)
  * [Kendala](#kendala)


## Topologi
![Topologi](/assets/topologi.png)

## VLSM pada GNS3
Berikut pembagian subnet yang kami berikan untuk topologi tersebut
![Topologi VLSM](/assets/vlsm/vlsm.png)

### Langkah 1
Menentukan jumlah alamat yang dibutuhkan oleh tiap subnet dan melakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan.
Subnet | A1 | A2 | A3 | A4 | A5 | A6 | A7 | A8 | A9 | A10 | A11 | A12 | A13 | Total
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |--- | --- | --- | --- |
Jumlah IP | 1001 | 2 | 701 | 2 | 2021 | 101 | 2 | 521 | 502 | 13 | 2 | 252 | 721 | 5841
Netmask | /22 | /30 | /22 | /30 | /21 | /25 | /30 | /22 | /23 | /28 | /30 | /24 | /22 | /19

### Langkah 2
Membuat VLSM Tree.
![VLSM Tree](/assets/vlsm/VLSM_Tree.png)
Berikut pembagian IP dan Netmask untuk setiap subnet.

| Subnet | Network IP | Netmask |
| --- | --- | --- |
| A1 | 10.12.8.0 | 255.255.252.0 |
| A2 | 10.12.31.240 | 255.255.255.252 |
| A3 | 10.12.12.0 | 255.255.252.0 |
| A4 | 10.12.31.244 | 255.255.255.252 |
| A5 | 10.12.0.0 | 255.255.248.0 |
| A6 | 10.12.31.0 | 255.255.255.128 |
| A7 | 10.12.31.248 | 255.255.255.252 |
| A8 | 10.12.16.0 | 255.255.252.0 |
| A9 | 10.12.28.0 | 255.255.254.0 |
| A10 | 10.12.31.224 | 255.255.255.240 |
| A11 | 10.12.31.252 | 255.255.255.252 |
| A12 | 10.12.30.0 | 255.255.255.0 |
| A13 | 10.12.20.0 | 255.255.252.0 |

## CIDR pada CPT
Berikut langkah kami dalam menyusun susunan netmask dalam CIDR:

### Langkah 1
Menentukan subnet yang ada dalam topologi dan labelling netmask.
![Topologi CIDR](/assets/cidr/topologi.png)

### Langkah 2
Menggabungkan subnet paling bawah dan jauh dari internet dengan subnet terdekatnya. Lantas, dibentuklah subnet terbesar dari subnet yang kecil.

Untuk subnet BX disusun sebagai berikut.
![Subnet BX](/assets/cidr/subnet-b.png)

Untuk subnet CX disusun sebagai berikut.
![Subnet CX](/assets/cidr/subnet-c.png)

Untuk subnet DX disusun sebagai berikut.
![Subnet DX](/assets/cidr/subnet-d.png)

Untuk subnet EX disusun sebagai berikut.
![Subnet EX](/assets/cidr/subnet-e.png)

Untuk subnet FX disusun sebagai berikut.
![Subnet FX](/assets/cidr/subnet-f.png)

Untuk subnet GX disusun sebagai berikut.
![Subnet GX](/assets/cidr/subnet-g.png)

### Langkah 3
Dari proses tersebut, didapatkan netmask **/15**. Kali ini didapatkan NID 10.12.0.0 dengan netmask 255.254.0.0.

### Langkah 4
Maka, pembagian IP dengan pohon penggabungan subnet menjadi sebagai berikut.
![Pohon IP](/assets/cidr/pembagian-ip.jpg)

### Langkah 5
Sehingga, pembagian IP menjadi sebagai berikut.
![Tabel IP](/assets/cidr/tabel-ip.jpg)

Oleh karena itu, didapatkan bentuk topologi dalam CIDR sebagai berikut.
![Hasil CIDR](/assets/cidr/result-cidr.png)

## Kendala
- Pengaturan router harus dilakukan satu persatu.
- Mendadaknya perubahan jadwal, sehingga bertabrakan dengan beberapa deadline.