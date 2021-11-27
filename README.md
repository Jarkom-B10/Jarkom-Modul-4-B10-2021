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