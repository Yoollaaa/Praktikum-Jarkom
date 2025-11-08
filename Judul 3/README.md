# Praktikum Jaringan Komputer – Judul 3  
## *Configure VLANs and Trunking (Physical Mode)*  
**Febby Yolanda Putri – 2315061003 – PJK-B**

---

## Video Demonstrasi  
[Klik di sini untuk menonton video praktikum di YouTube](https://youtu.be/GJ5-KQb2ZSY?si=M34mPMvZ-SnYG89j)

## Langkah Konfigurasi Singkat

### **1. Membuat VLAN**

```bash
vlan 10
 name Operations
vlan 20
 name Parking_Lot
vlan 99
 name Management
vlan 1000
 name Native
```

### **2. Mengatur Port ke VLAN**

```bash
interface fa0/6
 switchport mode access
 switchport access vlan 10
!
interface range fa0/11-24
 switchport mode access
 switchport access vlan 99
```

### **3. Mengonfigurasi IP Management**

```bash
interface vlan 99
 ip address 192.168.1.11 255.255.255.0
 no shutdown
```

### **4. Mengonfigurasi Trunk**

```bash
interface fa0/1
 switchport mode trunk
 switchport trunk native vlan 1000
 switchport trunk allowed vlan 10,20,99,1000
```

---

## 🧩 Topologi Jaringan

<img width="661" height="302" alt="image" src="https://github.com/user-attachments/assets/b7b90c06-5461-4544-bc88-f3deb5ae74d2" />



## 🧪 Hasil Pengujian

| Pengujian      | Hasil      | Keterangan                      |
| -------------- | ---------- | ------------------------------- |
| S1 ping S2     | ✅ Berhasil | Trunk aktif, VLAN 99 bisa lewat |
| PC-A ping PC-B | ✅ Berhasil | Keduanya di VLAN 10             |
| PC-A ping S1   | ❌ Gagal    | Berbeda VLAN (10 vs 99)         |
| PC-B ping S2   | ❌ Gagal    | Berbeda VLAN (10 vs 99)         |


## Kesimpulan

* VLAN memisahkan domain broadcast dan meningkatkan keamanan jaringan.
* Trunk memungkinkan banyak VLAN melewati satu link antar switch.
* Native VLAN sebaiknya tidak menggunakan VLAN 1 demi keamanan.
* DTP bersifat proprietary, jadi mode trunk manual lebih direkomendasikan.
* Komunikasi antar VLAN memerlukan perangkat Layer 3 untuk routing.

---
