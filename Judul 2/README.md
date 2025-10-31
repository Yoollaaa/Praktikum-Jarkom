# 🧩 Praktikum Jaringan Komputer – Judul 2  
## 🔧 *Build a Switch and Router Network*  
**Febby Yolanda Putri – 2315061003 – PJK-B**

---

## 🎥 Video Demonstrasi  
🎬 [Klik di sini untuk menonton video praktikum di YouTube](https://youtu.be/F0Ty90rI50Y?si=hD3PuRUjB7xxTO1d)

## 💾 File Cisco Packet Tracer  
📁 **Nama File:** `TA2.pkt`  
🔗 [Klik di sini untuk mengunduh file Cisco Packet Tracer](./TA2.pkt)


**Topologi Jaringan**
Berikut adalah tampilan topologi jaringan yang digunakan pada praktikum ini:
<img width="625" height="158" alt="image" src="https://github.com/user-attachments/assets/46994c88-d9ae-4687-b264-d5f2d6712091" />

## 🧪 Hasil Pengujian dan Verifikasi
### 1️⃣ Ping dari PC-A ke PC-B  
Pengujian ini dilakukan untuk memastikan komunikasi antar subnet melalui router berhasil.  
Hasil menunjukkan bahwa **ping berhasil**, menandakan routing antar jaringan berjalan dengan baik.
<img width="863" height="677" alt="ping PC A ke PC B" src="https://github.com/user-attachments/assets/943ce8dc-2549-44a0-958a-17e006c15a36" />

### 2️⃣ Ping dari Switch ke PC-B  
Pengujian ini dilakukan untuk menguji konektivitas dari switch ke perangkat di jaringan lain.  
Hasil menunjukkan bahwa **ping juga berhasil**, artinya switch dapat mengirimkan ICMP request melalui gateway (router) menuju jaringan lain.
<img width="846" height="150" alt="Ping Switch Ke PC B" src="https://github.com/user-attachments/assets/3467340a-89d3-409c-ae8b-f33a9eef6962" />

## ✅ Kesimpulan  
- Router berhasil menghubungkan dua subnet (`192.168.0.0/24` dan `192.168.1.0/24`).  
- PC-A dan Switch dapat berkomunikasi dengan PC-B melalui router.  
- Semua konektivitas antar perangkat berjalan normal.  
- Jaringan berfungsi sesuai konfigurasi yang telah dibuat di Packet Tracer.  

