Pada praktikum kali ini akan mempelajari cara memanggil API Flask dari React. Tujuannya adalah agar frontend dapat menampilkan data yang didapat dari backend.
## Endpoint Flask Berfungsi
![Screenshot 2025-03-04 105755](https://github.com/user-attachments/assets/177ffe47-b396-4f13-9f3d-1eae86e00a4b)

Pada proses ini Endpoint Flask berhasil ditampilkan di browser karena server Flask berjalan dengan benar tanpa error, dengan route yang telah didefinisikan secara tepat.
## Error Handling
![Screenshot 2025-03-04 112125](https://github.com/user-attachments/assets/81d4f4d6-6059-45ec-a1fa-725b5d8acde5)

Pada proses ini terjadi error, yang harusnya dapat menampilkan "Hello from Flask API", bukannya "Loading data...".

Maka dari itu harus ada code yang ditambahkan yaitu :
![Screenshot 2025-03-04 112454](https://github.com/user-attachments/assets/53b5ed4d-42bf-4be7-a523-fbd935740a31)

"from flask_cors import CORS"
"CORS(app)"

Lalu mengimport module flask nya :
![Screenshot 2025-03-04 112613](https://github.com/user-attachments/assets/324788b8-36ae-4b9f-8b7d-12cfa29115b1)

Setelah itu maka tampilan akan berubah menjadi seperti berikut

## Integrasi React & Flask
![Screenshot 2025-03-04 110308](https://github.com/user-attachments/assets/766ddd27-40c0-4d66-87fe-6171dbb1f809)


"Hello from Flask API" berhasil ditampilkan menandakan berhasil menjalankan React & Flask Integration berikut code nya.
## Code "Hello from Flask API"
![Screenshot 2025-03-04 110511](https://github.com/user-attachments/assets/a27e1e01-3c00-43b4-b4d7-36d5dc4b07b2)

Kode ini merupakan aplikasi Flask sederhana dengan dukungan CORS (Cross-Origin Resource Sharing) menggunakan `Flask-CORS`, memungkinkan akses dari domain lain. Aplikasi ini mendefinisikan dua endpoint: `"/"` yang mengembalikan respons JSON dengan pesan `"Hello from Flask!"` dan `"/api/data"` yang mengembalikan data dalam format JSON. Server berjalan pada `host='0.0.0.0'` agar dapat diakses dari jaringan lain, menggunakan port `5000`, serta mode `debug=True` untuk memudahkan debugging dengan fitur hot-reloading.

## Terminal Flask
![Screenshot 2025-03-04 111241](https://github.com/user-attachments/assets/175d22ec-8893-481b-bf78-887f3b77f475)

Jika python app.py dijalankan pada terminal, maka akan terlihat tampilan seperti ini, server berjalan dalam mode debug dan dapat diakses melalui http://127.0.0.1:5000 serta http://10.160.65.38:5000. Log menunjukkan beberapa permintaan GET ke endpoint "/api/data", yang berhasil dikembalikan dengan status 200.

Pada terminal flask sebelum menjalankan python app.py sudah masuk ke dalam virtual environment

## Terminal React
![Screenshot 2025-03-04 111604](https://github.com/user-attachments/assets/ccb68651-655b-464e-9c6f-3cf64b330d4b)

Jika npm run dev dijalankan memulai server pengembangan dengan cepat dalam 351 ms. Aplikasi React dapat diakses secara lokal melalui http://localhost:5173/. Selain itu, terdapat opsi untuk mengekspose ke jaringan menggunakan --host.

