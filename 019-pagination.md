**Pagination** adalah cara untuk membagi konten menjadi beberapa halaman, membuat navigasi di antara halaman tersebut lebih mudah. Dalam Bootstrap 5, pagination memudahkan kita untuk membuat navigasi antar halaman dengan gaya yang sudah disediakan oleh framework ini.

#### 1. Membuat Pagination

Pagination di Bootstrap 5 menggunakan komponen `pagination`. Mari kita lihat bagaimana cara membuat pagination sederhana.

##### Kode Contoh:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagination Example</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <nav aria-label="Page navigation example">
            <ul class="pagination">
                <li class="page-item"><a class="page-link" href="#">Previous</a></li>
                <li class="page-item"><a class="page-link" href="#">1</a></li>
                <li class="page-item"><a class="page-link" href="#">2</a></li>
                <li class="page-item"><a class="page-link" href="#">3</a></li>
                <li class="page-item"><a class="page-link" href="#">Next</a></li>
            </ul>
        </nav>
    </div>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/d8c31dfb-b4d6-41e3-b1f3-a614ad6f2c4f)

##### Penjelasan Kode:

1. **Tag `<nav>`**: Digunakan untuk mendefinisikan navigasi, di sini kita menggunakan `aria-label` untuk meningkatkan aksesibilitas dengan memberi label "Page navigation example".
   
2. **Tag `<ul class="pagination">`**: Ini adalah elemen utama untuk membuat daftar pagination. Kelas `pagination` memberi gaya dasar pagination.

3. **Tag `<li class="page-item">`**: Setiap item dalam daftar pagination. Kelas `page-item` digunakan untuk styling setiap item pagination.

4. **Tag `<a class="page-link">`**: Ini adalah link dalam setiap item pagination. Kelas `page-link` memberi gaya pada link untuk menyesuaikan dengan desain pagination Bootstrap.

5. **Link "Previous" dan "Next"**: Digunakan untuk navigasi ke halaman sebelumnya atau berikutnya. Kamu bisa mengganti `href="#"` dengan URL halaman yang sesuai.

#### 2. Pagination dengan Variants

Bootstrap 5 juga menyediakan beberapa varian untuk pagination agar lebih sesuai dengan kebutuhan desain yang berbeda.

##### Kode Contoh untuk Pagination Variants:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pagination Variants Example</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container mt-5">
        <!-- Basic Pagination -->
        <nav aria-label="Basic pagination">
            <ul class="pagination">
                <li class="page-item"><a class="page-link" href="#">Previous</a></li>
                <li class="page-item"><a class="page-link" href="#">1</a></li>
                <li class="page-item"><a class="page-link" href="#">2</a></li>
                <li class="page-item"><a class="page-link" href="#">3</a></li>
                <li class="page-item"><a class="page-link" href="#">Next</a></li>
            </ul>
        </nav>

        <!-- Pagination with Numbers Only -->
        <nav aria-label="Pagination with numbers only">
            <ul class="pagination">
                <li class="page-item disabled"><span class="page-link">Previous</span></li>
                <li class="page-item active" aria-current="page"><span class="page-link">1</span></li>
                <li class="page-item"><a class="page-link" href="#">2</a></li>
                <li class="page-item"><a class="page-link" href="#">3</a></li>
                <li class="page-item"><a class="page-link" href="#">Next</a></li>
            </ul>
        </nav>

        <!-- Pagination with Icons -->
        <nav aria-label="Pagination with icons">
            <ul class="pagination">
                <li class="page-item">
                    <a class="page-link" href="#" aria-label="Previous">
                        <span aria-hidden="true">&laquo;</span>
                    </a>
                </li>
                <li class="page-item"><a class="page-link" href="#">1</a></li>
                <li class="page-item"><a class="page-link" href="#">2</a></li>
                <li class="page-item"><a class="page-link" href="#">3</a></li>
                <li class="page-item">
                    <a class="page-link" href="#" aria-label="Next">
                        <span aria-hidden="true">&raquo;</span>
                    </a>
                </li>
            </ul>
        </nav>
    </div>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/7a94214f-a711-4d4e-a677-a2f463b9f1d3)

##### Penjelasan Kode:

1. **Pagination dengan Angka Saja**:
   - Item dengan kelas `disabled` tidak dapat diklik, biasanya digunakan untuk menandakan bahwa halaman sebelumnya tidak ada.
   - Item dengan kelas `active` menunjukkan halaman saat ini.

2. **Pagination dengan Ikon**:
   - Menggunakan karakter HTML `&laquo;` dan `&raquo;` untuk ikon "Previous" dan "Next" yang lebih visual.

### Referensi
Untuk informasi lebih lanjut tentang pagination di Bootstrap 5, kalian bisa merujuk ke [dokumentasi resmi Bootstrap](https://getbootstrap.com/docs/5.3/components/pagination/). Di sana kalian akan menemukan panduan lengkap dan opsi tambahan untuk kustomisasi pagination.

Dengan memahami cara menggunakan pagination ini, kalian bisa membuat navigasi halaman yang lebih baik dan mudah digunakan dalam aplikasi web kalian. Semoga bermanfaat! 😄
