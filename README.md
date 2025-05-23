## Tutorial 3: WebChat using Yew

Tutorial ini bertujuan untuk membangun aplikasi webchat menggunakan Yew sebagai frontend dan awalnya menggunakan server WebSocket berbasis JavaScript (Node.js) seperti yang direferensikan dari blog post [Let's Build a WebSockets Project with Rust and Yew](https://blog.devgenius.io/lets-build-a-websockets-project-with-rust-and-yew-0-19-60720367399f).

### 3.1. Original code

Proyek server WebSocket JavaScript (`SimpleWebsocketServer`) dan klien Yew (`webchat_yew`) di-clone dan dijalankan sesuai panduan.

**Cara Menjalankan:**
1.  **Server (JavaScript - `SimpleWebsocketServer`):**
    *   Masuk ke direktori `gatau/SimpleWebsocketServer`.
    *   Jalankan `npm install` untuk menginstal dependensi.
    *   Jalankan `npm start` (atau `node src/app.js` jika script start tidak ada/berbeda) untuk memulai server WebSocket. Server ini biasanya berjalan di port seperti `8000`, `9000`, atau `8080` (sesuai konfigurasi server JS tersebut).
2.  **Klien (Yew - `webchat_yew`):**
    *   Masuk ke direktori `gatau/webchat_yew`.
    *   Jalankan `npm install` untuk menginstal dependensi build (seperti webpack).
    *   Jalankan `npm start` untuk mengkompilasi kode Rust ke WebAssembly dan menjalankan development server untuk klien Yew. Ini biasanya akan membuka browser ke `http://localhost:8080` (atau port lain yang dikonfigurasi webpack).
    *   Pastikan alamat WebSocket URL di `webchat_yew/src/services/websocket.rs` (misalnya `ws://127.0.0.1:PORT_SERVER_JS`) sesuai dengan port tempat server JS berjalan.

**Hasil Eksekusi dan Interaksi:**
Aplikasi berhasil berjalan dengan baik. Saya bisa memasukkan username di halaman login, kemudian diarahkan ke halaman chat. Pesan yang dikirim muncul di area chat, dan jika membuka beberapa tab browser atau klien, pesan akan tersinkronisasi antar klien melalui server WebSocket JavaScript.

[alt text](ss1.png)