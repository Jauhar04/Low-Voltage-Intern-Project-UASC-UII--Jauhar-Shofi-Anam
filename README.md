# Low-Voltage-Intern-Project-UASC-UII--Jauhar-Shofi-Anam

#Project 1 (simulasi ESP 32 dengan sensor DHT22)
Project disimulasikan menggunakan Wokwi.
Project bisa diakses pada link berikut : https://wokwi.com/projects/399907289249282049
Program yang digunakan bisa diakses pada file word berikut : [Program Project 1.docx](https://github.com/user-attachments/files/15752541/Program.Project.1.docx)
Keterangan rangkaian dan program pada project 1:
RANGKAIAN
-DHT22 Sensor: Mengukur suhu dan kelembaban, dihubungkan ke pin 15 ESP32.
-Buzzer: Memberikan alarm suara jika suhu atau kelembaban berada di luar rentang yang ditentukan, dihubungkan ke pin 33 ESP32.
-LED: Memberikan indikasi visual jika suhu atau kelembaban berada di luar rentang yang ditentukan, dihubungkan ke pin 14 ESP32.
PROGRAM
-Inisialisasi:
Mengimpor pustaka Adafruit untuk sensor DHT.
Mendefinisikan pin untuk DHT22, buzzer, dan LED.
Mengatur ambang batas suhu dan kelembaban.
-Setup:
Memulai komunikasi serial untuk debug.
Menginisialisasi sensor DHT.
Mengatur mode pin untuk buzzer dan LED sebagai OUTPUT.
Memastikan buzzer dan LED dalam kondisi off saat memulai.
-Loop:
Membaca nilai suhu dan kelembaban dari DHT22.
Mengecek apakah pembacaan berhasil, jika gagal, mencetak pesan kesalahan.
Mencetak nilai suhu dan kelembaban ke serial monitor.
Mengecek apakah suhu atau kelembaban di luar rentang yang telah ditentukan:
Jika iya, menyalakan buzzer (1000 Hz selama 1 detik) dan LED.
Jika tidak, mematikan buzzer dan LED.
Menunggu 2 detik sebelum mengulangi pengukuran.





#Project 2 (Simulasi ESP 32 dengan sensor HC-SR04)
Project disimulasikan menggunakan Wokwi.
Project bisa diakses pada link berikut: https://wokwi.com/projects/399916031543209985
Program yang digunakan bisa diakses pada file word berikut: [Program project 2.docx](https://github.com/user-attachments/files/15752556/Program.project.2.docx)
Keterangan rangkaian dan program pada project 2:
RANGKAIAN
HC-SR04 Ultrasonic Sensor: Mengukur jarak dengan menggunakan gelombang ultrasonik.
Trig Pin: Mengirimkan sinyal ultrasonik, dihubungkan ke pin 5 ESP32.
Echo Pin: Menerima sinyal pantul, dihubungkan ke pin 18 ESP32.
OLED Display: Menampilkan hasil pengukuran jarak. Dioperasikan melalui komunikasi I2C yang terhubung ke pin SDA dan SCL pada ESP32.
PROGRAM
-Inisialisasi:
Mengimpor pustaka yang diperlukan untuk layar OLED dan komunikasi I2C.
Mendefinisikan pin untuk Trig dan Echo pada sensor HC-SR04.
Mendefinisikan ukuran layar OLED.
-Setup:
Memulai komunikasi serial untuk debugging.
Mengatur mode pin untuk Trig sebagai OUTPUT dan Echo sebagai INPUT.
Inisialisasi layar OLED dan cek apakah inisialisasi berhasil. Jika gagal, cetak pesan error dan hentikan program.
-Loop:
Mengirimkan sinyal ultrasonik:
Set Trig pin ke LOW selama 2 mikrodetik.
Set Trig pin ke HIGH selama 10 mikrodetik.
Kembali ke LOW.
Mengukur durasi sinyal pantul yang diterima oleh Echo pin.
Menghitung jarak berdasarkan durasi sinyal (dalam cm).
Menampilkan jarak pada serial monitor.
Menampilkan jarak pada layar OLED dengan mengatur teks, ukuran, dan warna.
Menghapus layar OLED sebelum pengukuran berikutnya.
Menunggu 1 detik sebelum pengukuran berikutnya.





#Project 3 (Simulasi Kontrol LED menggunakan Web Server)
Project disimulasikan menggunakan Wokwi dan dikontrol menggunakan web server Blynk.
Project wokwi bisa diakses pada link berikut:https://wokwi.com/projects/400216280641604609 
Tampilan kontrol web server bisa dilihat pada gambar berikut:
![Cuplikan layar 2024-06-09 195327](https://github.com/Jauhar04/Low-Voltage-Intern-Project-UASC-UII--Jauhar-Shofi-Anam/assets/171679877/d8768cb1-cd95-4052-9c3e-931994f396c0)
Program yang digunakan bisa diakses pada filer word berikut: [Program project 3.docx](https://github.com/user-attachments/files/15752594/Program.project.3.docx)
Keterangan rangkaian dan program pada project 3:
RANGKAIAN
-ESP32: Mikrocontroller yang digunakan untuk mengendalikan LED melalui koneksi WiFi.
-LED Kuning dan Hijau: Dihubungkan ke pin 25 dan 27 pada ESP32, masing-masing dilengkapi dengan resistor untuk membatasi arus.
PROGRAM
-Inisialisasi:
Mendefinisikan ID template, nama template, dan token autentikasi untuk Blynk.
Mengimpor pustaka yang diperlukan untuk koneksi WiFi dan Blynk.
Mendefinisikan kredensial WiFi yang digunakan untuk menghubungkan ESP32 ke jaringan.
-Fungsi BLYNK_WRITE(V0) dan BLYNK_WRITE(V1):
Fungsi ini dipanggil ketika ada perubahan nilai pada virtual pin V0 dan V1 dari aplikasi Blynk.
Nilai yang diterima digunakan untuk mengendalikan LED yang terhubung ke pin 25 dan 27 pada ESP32.
-Setup:
Memulai komunikasi serial untuk debugging.
Mengatur mode pin 25 dan 27 sebagai OUTPUT.
Memulai koneksi Blynk dengan autentikasi token dan kredensial WiFi.
-Loop:
Fungsi Blynk.run() dipanggil terus menerus untuk menjaga koneksi dengan server Blynk dan menangani komunikasi data.
CARA KERJA SIMULASI
Mengontrol LED melalui Aplikasi Blynk:
Pengguna dapat menekan tombol virtual pada aplikasi Blynk yang terhubung ke virtual pin V0 dan V1.
Jika tombol pada V0 ditekan, LED HIJAU pada pin 25 akan menyala atau mati sesuai status tombol.
Jika tombol pada V1 ditekan, LED KUNING pada pin 27 akan menyala atau mati sesuai status tombol.





Project 4 (Wiring Mobil Listrik UASC bagian LOw Voltage)
Wiring mobil dibuat menggunakan software proteus
Tampilan wiring bisa dilihat pada file berikut :![Cuplikan layar 2024-06-09 203556](https://github.com/Jauhar04/Low-Voltage-Intern-Project-UASC-UII--Jauhar-Shofi-Anam/assets/171679877/6c36bff0-0e8b-4054-9fce-1fc775901fbf)
Penjelasan Wiring:
Rangkaian tersebut menggunakan berbagai komponen seperti baterai, diode charger, konverter DC, dan kontroler motor. Sumber utama tenaga berasal dari baterai bertegangan 72V (BAT1). Arus dari baterai pertama-tama melewati Miniature Circuit Breaker (MCB) yang berfungsi sebagai pengaman untuk mencegah arus lebih. Kemudian, arus dialirkan melalui kontak yang bertindak sebagai saklar utama sistem. Diode charger (D1) ditempatkan di jalur pengisian baterai untuk mencegah arus balik selama pengisian melalui port charger battery. Selain itu, terdapat tombol high break untuk penghentian darurat.
Konverter DC 12V mengubah tegangan 27V menjadi 12V dan menyediakan tegangan 5V jika diperlukan. Konverter ini memiliki beberapa keluaran: 12V+ untuk keluaran positif 12V, GND sebagai ground, dan 5V OUT yang tidak digunakan dalam diagram ini. Starter adalah saklar yang mengaktifkan konverter DC dan menghubungkan arus ke kontroler motor.
Kontroler Votol EM-100 menerima tegangan dari baterai dan mengontrol motor melalui terminal B+ (positif baterai), B- (negatif baterai), serta terminal U, V, dan W untuk keluaran fase yang menggerakkan motor listrik. Motor terhubung ke terminal U, V, dan W dari kontroler. Seluruh rangkaian ini dirancang untuk memastikan pengoperasian motor listrik yang aman dan terkontrol dengan baik, menggunakan relay (kontaktor) untuk menghubungkan atau memutuskan arus dari baterai ke sistem berdasarkan arus kecil yang diaktifkan oleh konverter DC.

