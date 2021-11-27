# Jarkom-Modul-4-B10-2021
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