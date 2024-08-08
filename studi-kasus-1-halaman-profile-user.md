Hai temen-temen! Kali ini kita akan belajar membuat halaman profil pengguna menggunakan Bootstrap 5 versi terbaru. Kita akan menggunakan beberapa komponen Bootstrap seperti Grid System, Navbar, Card, dan Modal. Tujuannya adalah untuk membuat halaman profil yang simpel tapi fungsional, di mana pengguna bisa melihat informasi profil mereka dan mengeditnya melalui modal.

Berikut adalah langkah-langkahnya:

1. **Menggunakan Grid System untuk Layout**
2. **Navbar untuk Navigasi**
3. **Card untuk Menampilkan Informasi Pengguna**
4. **Modal untuk Edit Profil**

### Struktur Dasar HTML

Pertama-tama, kita mulai dengan struktur dasar HTML berikut:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Profil Pengguna</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Navbar</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Profile</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Settings</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="container mt-4">
      <div class="row">
        <div class="col-md-4">
          <div class="card">
            <img src="https://via.placeholder.com/150" class="card-img-top" alt="Profile Picture">
            <div class="card-body">
              <h5 class="card-title">Nama Pengguna</h5>
              <p class="card-text">Email: user@example.com</p>
              <p class="card-text">Telepon: +62 123 4567 890</p>
              <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#editProfileModal">
                Edit Profile
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Modal -->
    <div class="modal fade" id="editProfileModal" tabindex="-1" aria-labelledby="editProfileModalLabel" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="editProfileModalLabel">Edit Profil</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <form>
              <div class="mb-3">
                <label for="userName" class="form-label">Nama</label>
                <input type="text" class="form-control" id="userName" value="Nama Pengguna">
              </div>
              <div class="mb-3">
                <label for="userEmail" class="form-label">Email</label>
                <input type="email" class="form-control" id="userEmail" value="user@example.com">
              </div>
              <div class="mb-3">
                <label for="userPhone" class="form-label">Telepon</label>
                <input type="tel" class="form-control" id="userPhone" value="+62 123 4567 890">
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
            <button type="button" class="btn btn-primary">Save changes</button>
          </div>
        </div>
      </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
  </body>
</html>
```
![image](https://github.com/user-attachments/assets/666b67b1-aef3-4039-bfcc-847903b8d371)

![image](https://github.com/user-attachments/assets/504180a0-99b4-462d-89ff-2eda95a138cd)


### Penjelasan Kode

1. **Navbar untuk Navigasi**
    - Kita membuat navbar sederhana dengan beberapa item menu seperti Home, Profile, dan Settings. Navbar ini responsif dan akan berubah menjadi tombol hamburger pada layar kecil.

2. **Grid System untuk Layout**
    - Bootstrap menggunakan sistem grid 12 kolom untuk mengatur layout. Di sini, kita membuat container yang berisi satu row dengan satu kolom (col-md-4), yang berarti kolom ini akan mengambil 4 dari 12 kolom pada layar medium ke atas.

3. **Card untuk Menampilkan Informasi Pengguna**
    - Kita menggunakan komponen card untuk menampilkan informasi pengguna. Card ini berisi gambar profil, nama, email, dan telepon pengguna, serta tombol untuk mengedit profil.

4. **Modal untuk Edit Profil**
    - Modal ini akan muncul ketika tombol "Edit Profile" diklik. Di dalam modal, kita membuat form sederhana untuk mengedit nama, email, dan telepon pengguna.

### Referensi

Untuk lebih lanjut tentang penggunaan Bootstrap, temen-temen bisa cek dokumentasi resmi Bootstrap di [Bootstrap Documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/). Di sana temen-temen bisa menemukan berbagai contoh penggunaan dan komponen Bootstrap lainnya.

Dengan mengikuti langkah-langkah di atas, temen-temen bisa membuat halaman profil pengguna yang responsif dan fungsional. Jangan lupa untuk bereksperimen dengan komponen Bootstrap lainnya untuk membuat halaman yang lebih menarik!
