# Praktikum 04
Nama : Muhammad Aulia Rahman

NIM : 10221055

Pada praktikum kali ini akan mempelajari cara memanggil API Flask dari React. Tujuannya adalah agar frontend dapat menampilkan data yang didapat dari backend.
## Endpoint Flask Berfungsi
![alt text](image.png)

Pada proses ini Endpoint Flask berhasil ditampilkan di browser karena server Flask berjalan dengan benar tanpa error, dengan route yang telah didefinisikan secara tepat.
## Error Handling
![alt text](image-7.png)

Pada proses ini terjadi error, yang harusnya dapat menampilkan "Hello from Flask API", bukannya "Loading data...".

Maka dari itu harus ada code yang ditambahkan yaitu :
![alt text](image-8.png)

"from flask_cors import CORS"
"CORS(app)"

Lalu mengimport module flask nya :
![alt text](image-9.png)

Setelah itu maka tampilan akan berubah menjadi seperti berikut

## Integrasi React & Flask
![alt text](image-1.png)

"Hello from Flask API" berhasil ditampilkan menandakan berhasil menjalankan React & Flask Integration berikut code nya.
## Code "Hello from Flask API"
![alt text](image-2.png)

Kode ini merupakan aplikasi Flask sederhana dengan dukungan CORS (Cross-Origin Resource Sharing) menggunakan `Flask-CORS`, memungkinkan akses dari domain lain. Aplikasi ini mendefinisikan dua endpoint: `"/"` yang mengembalikan respons JSON dengan pesan `"Hello from Flask!"` dan `"/api/data"` yang mengembalikan data dalam format JSON. Server berjalan pada `host='0.0.0.0'` agar dapat diakses dari jaringan lain, menggunakan port `5000`, serta mode `debug=True` untuk memudahkan debugging dengan fitur hot-reloading.

## Terminal Flask
![alt text](image-5.png)

Jika python app.py dijalankan pada terminal, maka akan terlihat tampilan seperti ini, server berjalan dalam mode debug dan dapat diakses melalui http://127.0.0.1:5000 serta http://10.160.65.38:5000. Log menunjukkan beberapa permintaan GET ke endpoint "/api/data", yang berhasil dikembalikan dengan status 200.

Pada terminal flask sebelum menjalankan python app.py sudah masuk ke dalam virtual environment

## Terminal React
![alt text](image-6.png)

Jika npm run dev dijalankan memulai server pengembangan dengan cepat dalam 351 ms. Aplikasi React dapat diakses secara lokal melalui http://localhost:5173/. Selain itu, terdapat opsi untuk mengekspose ke jaringan menggunakan --host.

