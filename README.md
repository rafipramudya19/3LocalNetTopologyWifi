#3LocalNetTopologyWifi

#### I. Teori Dasar
Wireless Fidelity atau yang lebih awam kita sebut wifi adalah suatu teknologi yang menggunakan gelombang radio dalam rentang 2,4GHz sampai dengan 5GHz untuk menghubungkan perangkat seperti PC/laptop, smartphone, dan perangkat microcontroller seperti ESP32 dan ESP8266 ke jaringan lokal wireless untuk bisa mengakses internet. Untuk dapat melakukan akses internet tersebut,maka perangkat elektronik diatas perlu berada dalam satu titik akses atau hotspot jaringan nirkabel sehingga terhubung dengan wifi. Pada umumnya jaringan wifi dapat menjangkau hingga 20 meter didalam ruangan dan lebih dari 20 meter untuk di luar ruangan. Pada awal kemunculannya, wifi hanya digunakan sebagai perangkat nirkabel pada jaringan LAN (Local Area Network) akan tetapi karena pesatnya teknologi di zaman sekarang wifi menjadi kebutuhan sehari-hari untuk akses jaringan internet dan IoT. Berbagai data yang kita minta atau kirimkan melalui wifi didistribusikan melalui gelombang radio di udara. Supaya data tersebut bisa terbaca maka harus ada yang namanya wireless adaptor yang menghubungkan ke wifi. Gelombang radio yang berwujud sinyal ini lalu dikirim menuju router yang fungsinya untuk memecahkan kode. Setelah terbaca maka data dikirim ke jaringan internet yang memanfaatkan koneksi ethernet. Karena jaringan wifi ini bekerja dua arah maka tiap data yang diterima dalam waktu yang sama menjadi kode pada tiap paket data lalu dikirim kembali dalam bentuk sinyal radio yang diterima adaptor komputer nirkabel.

#### II. Alat dan Bahan
1) ESP32
2) Breadboard
3) Kabel jumper
4) Sensor DHT 11, RFID
5) LED (5) dan Push Button (3)
6) Servo
7) Resistor 330,1K, 10K Ohm (@ 3)

#### III. Langkah Percobaan
A. ESP32 Wi-Fi Modes dan Wifi-Scan
1. Pada ESP32, terdapat 3 mode akses untuk Wifi, yaitu WIFI_STA (station mode : ESP32 sebagai client yang terkoneksi ke access point), WIFI_AP (access point mode : ESP32 berperan sebagai access point), WIFI_STA_AP (access point and station : ESP32 dapat terkoneksi dengan access point yang lain).

![1](https://user-images.githubusercontent.com/121251478/210208191-d7c361d8-3839-4489-a354-da88ccf101db.jpeg)


2. Buka Arduino IDE dan upload script program berikut ke ESP32 untuk melakukan scan jaringan Wi-Fi.
3. Buka serial monitor dan dokumentasikan outputnya.

![doc1](https://user-images.githubusercontent.com/121251478/210208203-d503211f-4fe4-410d-bb8d-2d9e1d5f6cd0.png)


4. Buatlah flow chart program diatas.

B. Menghubungkan ESP32 dengan Jaringan Wi-Fi
1. Buatlah program seperti script dibawah ini, kemudian upload program tersebut ke ESP32.
2. Buka serial monitor, kemudian dokumentasikan outputnya.

![doc2](https://user-images.githubusercontent.com/121251478/210208223-75967f38-367e-4d8a-bd27-98bc21cd38cf.png)


3. Buatlah flow chart program diatas

C. Menghubungkan Kembali (Re-connect) ESP32 dengan Jaringan Wi-Fi
1. Buatlah program seperti script dibawah ini, kemudian upload program tersebut ke ESP32.
2. Buka serial monitor, kemudian matikan paket data sebentar hingga koneksi ESP32 dengan jaringna Wi-Fi terputus. Setelah itu, nyalakan lagi paket data. Dokumentasikan proses yang terjadi.

![doc3](https://user-images.githubusercontent.com/121251478/210208236-89263869-5041-4736-95cb-7287f41d373c.png)


3. Buatlah flow chart program diatas.

D. Mengganti Hostname ESP32
1. Buatlah program seperti script dibawah ini, kemudian upload program tersebut ke ESP32.
2. Buka serial monitor, kemudian aktifkan mode koneksi Wi-Fi pada SmartPhone atau Laptop. Lakukan scan dan lihat daftar jaringan Wi-Fi yang tersedia. Dokumentasikan hasil keluarannya.

![doc4](https://user-images.githubusercontent.com/121251478/210208245-bc39f930-b082-449d-a614-ccbb7861a0af.png)



3. Buatlah flow chart program diatas.

E. Mengirim Data Sensor ke Database
1. Buatlah rangkaian seperti Gambar di bawah ini.
1. Install library Asynch Web Server dan Asycnh TCP untuk ESP 32 dengan cara download dari link berikut ini.
a. https://github.com/me-no-dev/ESPAsyncWebServer
b. https://github.com/me-no-dev/AsyncTCP/archive/master.zip
Install library tersebut secara manual dengan cara menyalin folder hasil ekstraksi file.zip ke direktori libarary Arduino di folder Document.
2. Buatlah script program seperti berikut ini.
3. Upload program di atas. Kemudian buka serial monitor untuk mengetahui IP Address ESP32.
4. Akses IP Address ESP32 pada browser laptop. Dokumentasikan hasilnya dan buatlah flow chart dari program tersebut.

![doc5](https://user-images.githubusercontent.com/121251478/210208268-b72f12a1-ef56-4396-8132-51f46347cae3.png)


Hasil yang muncul pada web seperti gambar dibawah, dikarenakan sensor rusak maka suhu tidak muncul atau terdeteksi.
![doc6](https://user-images.githubusercontent.com/121251478/210208294-8a846d16-847a-4624-8da7-c35a59aa0cc4.png)
