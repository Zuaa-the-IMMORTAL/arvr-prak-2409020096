# Praktikum AR/VR - Pertemuan 1
- Nama : zahrani nazwa
- NIM : 2409020096
- Link demo : https://Zuaa-the-IMMORTAL.github.io/arvr-prak-2409020096/
Project ini berisi scene WebXR pertama menggunakan A-Frame 1.7.1.

1 Mengapa posisi objek yang terlihat pertama kali oleh pengguna memakai nilai z negatif?
2 Mengapa WebXR hanya aktif pada HTTPS atau localhost?
3 Jelaskan perbedaan peran WebXR Device API, three.js, dan A-Frame dengan bahasa Anda sendiri.

### 1. Mengapa posisi objek yang terlihat pertama kali oleh pengguna memakai nilai z negatif?

Dalam sistem koordinat standar WebGL/WebXR (menggunakan sistem koordinat tangan kanan/*right-handed*), kamera secara default menghadap ke arah sumbu **Z negatif** ($-\text{Z}$). Artinya, area yang berada tepat di depan layar atau di depan mata pengguna bernilai negatif. Oleh karena itu, agar objek muncul langsung di hadapan pandangan pengguna, koordinat Z-nya harus diatur ke angka negatif.

### 2. Mengapa WebXR hanya aktif pada HTTPS atau localhost?

Karena WebXR mengakses perangkat keras yang sangat sensitif—seperti sensor gerak, kamera, dan data spasial—yang berpotensi disalahgunakan untuk melacak privasi pengguna. Peramban (*browser*) mewajibkan **Secure Context** (HTTPS atau localhost) sebagai standar keamanan untuk mencegah serangan siber dan melindungi data pribadi pengguna dari situs web berbahaya.

### 3. Perbedaan peran WebXR Device API, Three.js, dan A-Frame

* **WebXR Device API:** API tingkat rendah (*low-level*) bawaan *browser* yang berfungsi sebagai jembatan utama untuk berkomunikasi langsung dengan perangkat keras VR/AR (seperti mengambil data posisi *headset* atau *controller*).
* **Three.js:** Pustaka (*library*) JavaScript grafis 3D yang menyederhanakan pembuatan objek, pencahayaan, material, dan animasi 3D tanpa harus menulis kode WebGL yang rumit.
* **A-Frame:** Kerangka kerja (*framework*) berbasis HTML tingkat tinggi yang dibangun di atas Three.js, memungkinkan Anda membuat dunia VR/AR dengan mudah menggunakan tag-tag HTML yang sederhana.