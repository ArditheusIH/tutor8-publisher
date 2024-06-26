1. Jumlah data (pesan) yang dikirimkan oleh program publisher ke broker pesan dalam satu proses tergantung pada logika dan persyaratan dari program publisher tersebut. Program tersebut bisa dirancang untuk mengirimkan satu pesan, beberapa pesan, atau bahkan tidak mengirimkan pesan sama sekali, tergantung pada faktor-faktor seperti input pengguna, peristiwa, atau tugas-tugas terjadwal.

2. Ketika kedua program publisher dan subscriber  menggunakan URL yang sama "amqp://guest:guest@localhost:5672", itu berarti keduanya dikonfigurasi untuk terhubung ke instansi server RabbitMQ yang sama menggunakan kredensial default ("guest" sebagai username dan password) serta host default ("localhost") dan port default ("5672"). Konfigurasi ini menandakan bahwa kedua program tersebut berinteraksi dengan sistem pesan RabbitMQ yang sama, memungkinkan pertukaran pesan antara keduanya dengan efektif. 


![alt text](/rabbitmq.png)

![alt text](/cmd.png)

![alt text](/spike1.png)

Spike diatas muncul karena mengirim data berkali-kali dengan cepat kepada Subscriber. Setiap kita menjalankan cargo run pada Publisher, ia akan membuat koneksi baru dan mengirim message ke Subscriber. Jika dalam waktu yang singkat kita terus mengirimkan data ke Subscriber, maka akan muncul spike akibat adanya koneksi dan pengiriman data yang tinggi ke Subscriber