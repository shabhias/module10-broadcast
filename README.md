# REFLECTION

## 2.1 Original code of broadcast chat.

- <a href="https://ibb.co/t4TsDFg"><img src="https://i.ibb.co/379NcQ2/Screenshot-2024-05-05-184537.png" alt="Screenshot-2024-05-05-184537" border="0"></a>

Setelah menjalankan server dengan menggunakan cargo run --bin server dan juga menjalankan klien dengan cargo run --bin client, Setiap klien dan server menerima pesan yang dikirimkan oleh setiap klien lainnya. Ketika seorang klien mengirimkan pesan, server akan meneruskannya kepada semua klien yang terhubung. Dengan demikian, setiap klien akan menerima pesan dari semua klien lainnya melalui server. Semua pesan dari klien akan disebarkan kepada semua klien yang terhubung ke server.


## 2.2 Modifying port

- <a href="https://ibb.co/SDg8R1k"><img src="https://i.ibb.co/mrKw6Yn/Screenshot-2024-05-05-191133.png" alt="Screenshot-2024-05-05-191133" border="0"></a>

Aplikasi akan berjalan baik seperti sebelumnya, seperti yang ditunjukkan pada gambar diatas ketika port yang digunakan oleh klien dan server adalah sama.


- <a href="https://ibb.co/D1mCp5S"><img src="https://i.ibb.co/x2wjHJR/Screenshot-2024-05-05-191319.png" alt="Screenshot-2024-05-05-191319" border="0"></a>

Apabila salah satu port diubah, misalkan port client. Maka, akan terjadi kesalahan pada sisi klien karena menurut klien, port tersebut tidak terhubung dan program akan mengalami kegagalan ketika perintah cargon run --bin client dijalankan sepertipada gambar di atas.


## 2.3 

- <a href="https://ibb.co/pbftHDK"><img src="https://i.ibb.co/8NrWy3x/Screenshot-2024-05-05-193307.png" alt="Screenshot-2024-05-05-193307" border="0"></a>
Saya merubah salah satu baris kode pada server.rs menjadi bcast_tx.send(format!("{addr} : {text}"))?;/ Perubahan dilakukan untuk memastikan bahwa ketika `bcast.tx` (yang bertindak sebagai *sender*) mengirimkan pesan kepada setiap klien, ia juga akan menyediakan alamat IP *sender* dari teks melalui variabel addr.