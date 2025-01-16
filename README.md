# Proposal Penggunaan LoRa untuk Penentuan Posisi Drone pada Drone Show

---

## Latar Belakang
Drone show menjadi salah satu bentuk hiburan modern yang memanfaatkan teknologi drone untuk menciptakan formasi visual yang indah dan sinkron. Agar drone dapat bergerak dengan presisi dalam formasi tertentu, diperlukan sistem penentuan posisi yang andal. Saat ini, penggunaan GPS sering menjadi pilihan utama. Namun, GPS memiliki keterbatasan, terutama dalam lingkungan dalam ruangan atau area yang terhalang. Oleh karena itu, kami mengusulkan penggunaan teknologi **LoRa (Long Range)** untuk sistem komunikasi dan penentuan posisi alternatif dalam drone show.

---

## Tujuan
1. Mengembangkan sistem penentuan posisi drone berbasis LoRa.
2. Memastikan sinkronisasi antar drone dengan akurasi hingga beberapa meter.
3. Mengoptimalkan efisiensi biaya dengan menggunakan perangkat LoRa yang hemat energi dan memiliki jangkauan luas.

---

## Teknologi LoRa
LoRa adalah teknologi komunikasi nirkabel yang menggunakan modulasi chirp spread spectrum (CSS). Beberapa keunggulan LoRa yang relevan untuk drone show adalah:
- **Jangkauan Luas:** Hingga 15 km di area terbuka.
- **Efisiensi Energi:** Konsumsi daya rendah, cocok untuk perangkat drone yang membutuhkan waktu operasional panjang.
- **Biaya Terjangkau:** Modul LoRa tersedia dengan harga relatif murah.
- **Resistensi terhadap Interferensi:** Ideal untuk lingkungan dengan banyak sinyal radio lainnya.

---

## Metode Implementasi

### 1. Penempatan Beacon LoRa
Beacon LoRa akan dipasang pada beberapa titik tetap di lokasi drone show. Setiap beacon akan memancarkan sinyal RF dengan informasi posisinya.

### 2. Trilaterasi Berbasis RSSI
Drone akan menggunakan metode **Received Signal Strength Indicator (RSSI)** untuk mengukur jarak ke setiap beacon. Dengan data jarak dari setidaknya tiga beacon, posisi drone dapat dihitung menggunakan algoritma trilaterasi.

### 3. Sinkronisasi Data
Untuk memastikan sinkronisasi antar drone, data posisi dari beacon akan dikirimkan melalui jaringan LoRaWAN ke server pusat. Server ini akan mengolah data dan mengirimkan perintah koreksi ke drone jika diperlukan.

### 4. Kontrol Formasi Drone
Sistem kontrol pada drone akan menerima data posisi dan perintah dari server pusat untuk menyesuaikan pergerakan sesuai formasi yang telah diprogram.

---

## Kebutuhan Perangkat Keras
1. **Modul LoRa:**
   - Contoh: Semtech SX1276 atau RFM95W.
2. **Microcontroller:**
   - Contoh: STM32 atau ESP32 dengan dukungan LoRa.
3. **Beacon Tetap:**
   - Modul LoRa dengan antena terkalibrasi.
4. **Ground Control System:**
   - Server untuk memproses data posisi dan mengontrol formasi drone.

---

## Keuntungan Penggunaan LoRa
1. **Biaya Rendah:** Teknologi LoRa lebih murah dibandingkan GPS RTK atau UWB.
2. **Sederhana:** Mudah diimplementasikan dengan perangkat keras yang tersedia secara luas.
3. **Fleksibilitas:** Dapat digunakan di area dalam ruangan maupun luar ruangan.
4. **Hemat Energi:** Memperpanjang waktu operasional drone.

---

## Studi Kasus
### Simulasi Drone Show (10 Drone):
1. Lokasi: Lapangan terbuka dengan ukuran 100 x 100 meter.
2. Penempatan beacon: 4 titik di setiap sudut area.
3. Resolusi posisi: Akurasi diestimasi 2-5 meter dengan koreksi real-time.
4. Hasil: Sistem berbasis LoRa berhasil menjaga formasi drone dengan kesalahan posisi minimal.

---

## Tantangan
1. **Akurasi RSSI:** Ketepatan pengukuran jarak menggunakan RSSI dapat dipengaruhi oleh multipath dan interferensi.
2. **Latency:** Pengiriman data LoRa memiliki latensi yang perlu diminimalkan untuk aplikasi real-time.
3. **Kapasitas Jaringan:** Pengaturan alokasi bandwidth agar semua drone dapat berkomunikasi tanpa tabrakan sinyal.

---

## Kesimpulan
Penggunaan teknologi LoRa dalam sistem penentuan posisi drone menawarkan solusi yang efisien, hemat biaya, dan fleksibel untuk aplikasi drone show. Dengan penempatan beacon yang tepat dan algoritma pengolahan data yang baik, LoRa dapat menggantikan atau melengkapi sistem GPS, terutama di area yang sulit dijangkau GPS.

---

## Rencana Tindak Lanjut
1. Pengembangan prototipe sistem LoRa untuk pengujian awal.
2. Simulasi drone show dengan 5-10 drone.
3. Optimasi algoritma trilaterasi untuk meningkatkan akurasi.
4. Evaluasi performa di lingkungan nyata.

---

**Disusun oleh:**
[Nama Tim / Perusahaan]  
[Kontak / Email]

---

