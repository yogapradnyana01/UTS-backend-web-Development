Project ini terdiri dari beberapa folder utama: config, public, src, dengan masing-masing memiliki sub-folder atau file, berikut penjelasannya:
1. config (Konfigurasi Sistem)
=> Koneksi Database (`config/database.php`)

  File ini berfungsi:

 - Menggunakan PDO untuk koneksi ke database MySQL.
 
 - Konfigurasi host, nama database, username, dan password disimpan dalam konstanta.
 
 - Jika koneksi gagal, ditampilkan pesan error dan program dihentikan.
2. public (File Utama PHP)
=>  index.php

  File ini berfungsi sebagai halaman utama yang pertama kali diakses oleh pengguna saat membuka aplikasi. Digunakan untuk mengatur tampilan awal, seperti halaman beranda atau dashboard. Untuk saat ini berisi header yang bertuliskan “XYZ Sales API End Point”.
3. src
3.1. Controller (Kelas-Kelas Utama)

=>  CustomerController (`Controller/CustomerController.php`)

  File ini berfungsi:

 - Mengontrol data pelanggan.
 
 - Konstruktor menerima objek PDO untuk koneksi ke database.
 
 - Metode `getAllCustomers()`: Mengambil semua data pelanggan dari database.
 
 - Metode `getCustomerById($customerId)`: Mengambil data pelanggan berdasarkan ID.
 
 - Metode `addCustomer($customerData)`: Menambah data pelanggan baru.
 
 - Metode `updateCustomer($customerId, $customerData)`: Memperbarui data pelanggan berdasarkan ID.
 
 - Metode `deleteCustomer($customerId)`: Menghapus data pelanggan berdasarkan ID.

=>  PurchaseController (`Controller/PurchaseController.php`)

  File ini berfungsi:
 
 - Mengontrol data pembelian.
 
 - Metode serupa dengan `CustomerController` untuk pengelolaan data pembelian.

=>  SalesController (`Controller/SalesController.php`)

  File ini berfungsi:

 - Mengontrol data penjualan.
 
 - Metode serupa dengan `CustomerController` untuk pengelolaan data penjualan.

3.2. Kelas Model

=>  Customers (`Model/Customers.php`)

  File ini berfungsi:
  
 - Berinteraksi dengan tabel `customers` dalam database.
 
 - Metode `getAllCustomers()`: Mengambil semua data pelanggan dari tabel.

 - Metode `getCustomerById($customerId)`: Mengambil data pelanggan berdasarkan ID.
 
 - Metode `addCustomer($customerData)`: Menambah data pelanggan baru.
 
 - Metode `updateCustomer($customerId, $customerData)`: Memperbarui data pelanggan berdasarkan ID.
 
 - Metode `deleteCustomer($customerId)`: Menghapus data pelanggan berdasarkan ID.


=>  Purchases (`Model/Purchases.php`)

  File ini berfungsi:

 - Berinteraksi dengan tabel `purchases` dalam database.
 
 - Metode serupa dengan `Customers` untuk pengelolaan data pembelian.

=>  Sales (`Model/Sales.php`)

  File ini berfungsi:

 - Berinteraksi dengan tabel `sales` dalam database.

 - Metode serupa dengan `Customers` untuk pengelolaan data penjualan.


refleksi

Tantangan:
Menjamin bahwa setiap fungsi di setiap kelas dan metode beroperasi sesuai dengan ekspektasi yang telah ditetapkan.

Mengembangkan pemahaman yang mendalam tentang konsep MVC dan mengaplikasikannya dengan cermat dalam pengembangan proyek.

Menangani masalah keamanan dan mengimplementasikan validasi data input dengan teliti untuk mencegah risiko keamanan.

Solusi:
Melakukan serangkaian pengujian menyeluruh pada setiap bagian kelas dan metode untuk memastikan konsistensi fungsionalitasnya.

Menerapkan prinsip-prinsip OOP dengan bijaksana untuk memisahkan tanggung jawab dan tugas-tugas yang terkait.

Menggunakan PDO untuk operasi database guna meningkatkan keamanan dan efisiensi aplikasi.

Melakukan verifikasi dan validasi data secara ketat untuk menjaga keandalan dan keamanan data.

Semoga proyek back-end yang sedang dikembangkan menjadi landasan yang kuat untuk mengelola data pelanggan, pembelian, dan penjualan dengan efisiensi tinggi. Teruslah menantang diri sendiri dan mengatasi hambatan-hambatan, karena setiap langkah membawa pelajaran berharga bagi kemajuan di masa depan. Teruslah berinovasi dan berkontribusi positif dalam dunia teknologi!





