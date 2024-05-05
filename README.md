# REFLECTION

## 2.1 Original code of broadcast chat.

- <a href="https://ibb.co/t4TsDFg"><img src="https://i.ibb.co/379NcQ2/Screenshot-2024-05-05-184537.png" alt="Screenshot-2024-05-05-184537" border="0"></a>

Setelah menjalankan server dengan menggunakan cargo run --bin server dan juga menjalankan klien dengan cargo run --bin client, Setiap klien dan server menerima pesan yang dikirimkan oleh setiap klien lainnya. Ketika seorang klien mengirimkan pesan, server akan meneruskannya kepada semua klien yang terhubung. Dengan demikian, setiap klien akan menerima pesan dari semua klien lainnya melalui server. Semua pesan dari klien akan disebarkan kepada semua klien yang terhubung ke server.