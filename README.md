# KOWAR (Koneksi Warga)
Adalah solusi perangkat lunak router/repeater berbasis mikrokontroler yang mengubah jaringan WiFi menjadi portal hotspot sewa internet terintegrasi.

## Diagram
```txt
+-----------------------+    Koneksi WiFi (STA)     +--------------------------+
|  Router Utama / ISP   | ------------------------> | Wemos D1 Mini ESP8266    |
|  (Sumber Internet)    |                           | (KOWAR V1.0 Repeater)    |
+-----------------------+                           +--------------------------+
                                                                  |
                                                                  | Captive Portal / AP
                                                                  | (Tanpa Pass / Ber-Pass)
                                                                  v
                                                    +--------------------------+
                                                    |    Client / User         |
                                                    |    (HP / Laptop Warga)   |
                                                    +--------------------------+
```

Menggunakan Wemos D1 Mini ESP8266 sebagai otak utama perangkat keras, KOWAR V1.0 mengubah modul WiFi murah meriah ini menjadi router hotspot mandiri layaknya mikrokontroler profesional berfitur lengkap.

Keunggulan Perangkat Keras & Sistem:

- Optimasi Hardware ESP8266: Memanfaatkan memori dan fitur NAPT (Network Address Port Translation) secara efisien dengan arsitektur Global Session Timer, memastikan perangkat berjalan stabil tanpa crash atau lag.
- Manajemen Voucher Terpusat: Sistem sewa internet fleksibel (mulai dari 1 jam hingga 12 jam) yang dikelola langsung di dalam memori EEPROM internal.
- Captive Portal: Setiap perangkat yang terhubung ke WiFi dapat mengunjungi portal lokal (199.4.7.9) untuk memasukan kode voucher atau melihat countdown sisa waktu.
- Panel Admin Web-Based: Antarmuka modern bergaya sPanel ID style untuk membuat voucher, memantau client, scan jaringan sekitar, hingga melakukan factory reset langsung dari HP atau Laptop.

Platform Hardware: Wemos D1 Mini (ESP8266)

Pengembang: Suryo Dwijayanto
