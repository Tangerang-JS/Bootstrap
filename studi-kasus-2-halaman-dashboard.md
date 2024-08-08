Halo temen-temen! Kali ini gue bakal ngajak kalian bikin halaman dashboard yang keren banget pakai Bootstrap 5. Dashboard ini akan punya layout yang rapi dengan Grid System, Card untuk statistik, Navbar dengan dropdown buat opsi admin, dan Progress Bars buat nunjukin proyek yang lagi dikerjain. Yuk kita mulai!

### Struktur Dasar HTML
Kita akan mulai dengan struktur HTML dasar berikut:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Dashboard</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Dashboard</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavDropdown">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link" href="#">Home</a>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                Admin
              </a>
              <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                <li><a class="dropdown-item" href="#">Settings</a></li>
                <li><a class="dropdown-item" href="#">Profile</a></li>
                <li><a class="dropdown-item" href="#">Logout</a></li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Container for Dashboard -->
    <div class="container mt-5">
      <div class="row">
        <!-- Statistik Card -->
        <div class="col-md-3">
          <div class="card text-white bg-primary mb-3">
            <div class="card-header">Users</div>
            <div class="card-body">
              <h5 class="card-title">150</h5>
              <p class="card-text">Total Users</p>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="card text-white bg-success mb-3">
            <div class="card-header">Sales</div>
            <div class="card-body">
              <h5 class="card-title">200</h5>
              <p class="card-text">Total Sales</p>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="card text-white bg-warning mb-3">
            <div class="card-header">Revenue</div>
            <div class="card-body">
              <h5 class="card-title">$3000</h5>
              <p class="card-text">Total Revenue</p>
            </div>
          </div>
        </div>
        <div class="col-md-3">
          <div class="card text-white bg-danger mb-3">
            <div class="card-header">Feedback</div>
            <div class="card-body">
              <h5 class="card-title">50</h5>
              <p class="card-text">Total Feedback</p>
            </div>
          </div>
        </div>
      </div>

      <!-- Progress Bars for Projects -->
      <h3 class="mt-5">Project Progress</h3>
      <div class="progress mb-3">
        <div class="progress-bar bg-success" role="progressbar" style="width: 75%" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100">Project 1 - 75%</div>
      </div>
      <div class="progress mb-3">
        <div class="progress-bar bg-info" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">Project 2 - 50%</div>
      </div>
      <div class="progress mb-3">
        <div class="progress-bar bg-warning" role="progressbar" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">Project 3 - 25%</div>
      </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
  </body>
</html>
```
![image](https://github.com/user-attachments/assets/373ef3bd-2a76-40fc-9334-4eaa08014d14)


### Penjelasan Kode
1. **Navbar**
   - **Navbar** di bagian atas halaman dengan opsi dropdown untuk admin. Ini berguna buat navigasi di dashboard.
   - `navbar-expand-lg` membuat navbar responsif sehingga berubah jadi ikon hamburger di layar kecil.
   - `navbar-brand` untuk judul dashboard dan `nav-link` untuk tautan navigasi.

2. **Grid System**
   - **Grid System** menggunakan `container`, `row`, dan `col-md-3` untuk membuat layout yang responsif.
   - `col-md-3` berarti setiap kolom akan mengambil 3 dari 12 kolom yang tersedia pada layar medium (tablet) ke atas.

3. **Card untuk Statistik**
   - **Card** untuk menampilkan statistik seperti jumlah pengguna, penjualan, pendapatan, dan umpan balik.
   - `card` dengan kelas `text-white bg-primary` atau `bg-success` untuk styling warna.
   - `card-header` untuk judul card dan `card-body` untuk konten utama.

4. **Progress Bars untuk Proyek**
   - **Progress Bars** untuk menampilkan progres proyek yang sedang berjalan.
   - `progress` sebagai container dan `progress-bar` untuk bar indikator progres.
   - `style="width: 75%"` menentukan panjang progres dalam persentase.

### Sumber Referensi
- [Bootstrap 5 Documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/)
- [W3Schools Bootstrap 5 Tutorial](https://www.w3schools.com/bootstrap5/index.php)

Dengan struktur dan penjelasan ini, temen-temen bisa bikin dashboard yang fungsional dan menarik dengan mudah. Selamat mencoba! 🚀
