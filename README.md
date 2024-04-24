1. Jumlah data (pesan) yang dikirimkan oleh program publisher ke broker pesan dalam satu proses tergantung pada logika dan persyaratan dari program publisher tersebut. Program tersebut bisa dirancang untuk mengirimkan satu pesan, beberapa pesan, atau bahkan tidak mengirimkan pesan sama sekali, tergantung pada faktor-faktor seperti input pengguna, peristiwa, atau tugas-tugas terjadwal.

2. Ketika kedua program publisher dan subscriber  menggunakan URL yang sama "amqp://guest:guest@localhost:5672", itu berarti keduanya dikonfigurasi untuk terhubung ke instansi server RabbitMQ yang sama menggunakan kredensial default ("guest" sebagai username dan password) serta host default ("localhost") dan port default ("5672"). Konfigurasi ini menandakan bahwa kedua program tersebut berinteraksi dengan sistem pesan RabbitMQ yang sama, memungkinkan pertukaran pesan antara keduanya dengan efektif. 


![alt text](/rabbitmq.png)