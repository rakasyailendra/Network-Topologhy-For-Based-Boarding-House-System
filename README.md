# Final Project Jaringan Komputer - Kelompok 1

## Materi Pilihan
- VLAN
- Hotspot
- Routing Dinamis (Statis)
- QoS (disinggung)

## Anggota Kelompok
- Achmad Fathoni – BB08101002E
- M Rakha Syailendra – BB08101001E  
- Heraldi Rizky Anggriawan – BB081010183E 
- Thareeq Ziad Ramadhan – BB08101014E  
- Rico Satyadharma Putra S – BB081010255E 

---

## BAB I – Pendahuluan

### 1.1 Latar Belakang
Perancangan jaringan kos-kosan satu lantai menggunakan VLAN, DHCP, Firewall, dan Hotspot untuk memisahkan pengguna dan menjaga keamanan jaringan.

### 1.2 Rumusan Masalah
- Bagaimana memisahkan jaringan berdasarkan jenis pengguna?
- Bagaimana konfigurasi DHCP, VLAN, firewall dan hotspot?
- Bagaimana membatasi akses tidak sah antar pengguna?

### 1.3 Tujuan
- Mengatur segmentasi jaringan (VLAN)
- Otomatisasi IP dengan DHCP Server
- Menjaga keamanan antar penghuni dengan Firewall
- Memberikan akses terbatas pada tamu (Hotspot)

---

## BAB II – Perancangan Jaringan

### 2.1 Topologi Jaringan
- VLAN 10: Area Depan
- VLAN 20: Area Kiri
- VLAN 30: Area Kanan
- VLAN 40: Area Tamu

### 2.2 Alat & Bahan
- GNS3
- Winbox
- Mikrotik CHR
- Ethernet Switch
- PC Virtual

### 2.3 Spesifikasi Jaringan
- DHCP aktif di setiap VLAN
- Firewall antar VLAN
- Hotspot di VLAN 40

---

## BAB III – Implementasi

### 3.1 Konfigurasi DHCP
- Konfigurasi DHCP dilakukan di router pusat, depan, kiri, kanan, dan tamu.

### 3.2 Konfigurasi Firewall
- Blokir akses antar PC (ping, komunikasi)
- Hanya Mikrotik Pusat yang dapat login ke Winbox

### 3.3 Routing Statis
- Routing antar VLAN diatur dari masing-masing router ke Router Pusat
- Jalur data antar area terkoneksi dengan gateway statis

### 3.4 Konfigurasi VLAN
- VLAN ID dikonfigurasi via Interface & DHCP
- Switch Port disesuaikan agar tiap kamar masuk VLAN tertentu

### 3.5 Konfigurasi Hotspot
- NAT + DHCP khusus VLAN 40
- Login page muncul saat tamu browsing

---

## BAB IV – Hasil dan Pembahasan

### 4.1 Hasil Simulasi
- DHCP dan IP berjalan dengan baik
- Firewall bekerja efektif
- Routing antar VLAN sukses
- Hotspot aktif dan mengarahkan ke login page

### 4.2 Kendala dan Solusi
- VLAN tidak terhubung pada perangkat → Solusi: Cek tagging port di switch

---

## BAB V – Penutup

### 5.1 Kesimpulan
- Segmentasi jaringan via VLAN berhasil
- Keamanan jaringan terjaga dengan firewall
- Akses terbatas diberikan melalui Hotspot
- Jaringan kos menjadi lebih aman dan efisien

---

> **Catatan:** File ini adalah ringkasan laporan. Untuk konfigurasi teknis dan detail topologi, silakan lihat file `.pdf` asli atau simulasi GNS3.

---

Kalau kamu mau, saya juga bisa bantu:
- Bikin template presentasi dari ini (Google Slides / PPTX)
- Export file ini jadi `.html` statis siap hosting
- Compress jadi ZIP untuk keperluan upload

Mau dilanjut ke salah satu itu?
