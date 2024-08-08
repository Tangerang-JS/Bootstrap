Halo temen-temen! Kali ini gue bakal ngajak lo untuk bikin sebuah form pendaftaran sederhana menggunakan Bootstrap 5. Kita bakal ngebahas mulai dari pembuatan form, menambahkan alert untuk menampilkan pesan, hingga memberikan validation feedback. Yuk kita mulai!

## Struktur Dasar HTML

Berikut adalah struktur dasar HTML yang akan kita gunakan. Gue udah siapin link CDN Bootstrap 5 versi terbaru dari jsDelivr.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Form Pendaftaran</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <div class="container mt-5">
      <h1 class="mb-4">Form Pendaftaran</h1>
      <form id="registrationForm">
        <!-- Form Controls akan ditambahkan di sini -->
      </form>
      <div id="alertPlaceholder"></div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
    <script>
      // JavaScript untuk menangani form submission akan ditambahkan di sini
    </script>
  </body>
</html>
```

## Membuat Form dengan Form Controls

Sekarang, kita tambahkan beberapa form controls ke dalam form kita. Gue akan menambahkan input untuk nama lengkap, email, dan password.

```html
<form id="registrationForm">
  <div class="mb-3">
    <label for="fullName" class="form-label">Nama Lengkap</label>
    <input type="text" class="form-control" id="fullName" required>
  </div>
  <div class="mb-3">
    <label for="email" class="form-label">Email</label>
    <input type="email" class="form-control" id="email" required>
  </div>
  <div class="mb-3">
    <label for="password" class="form-label">Password</label>
    <input type="password" class="form-control" id="password" required>
  </div>
  <button type="submit" class="btn btn-primary">Daftar</button>
</form>
```

## Menggunakan Alerts untuk Menampilkan Pesan

Untuk menampilkan pesan setelah form dikirim, kita bakal menggunakan alert dari Bootstrap. Kita akan menambahkan div dengan id `alertPlaceholder` untuk menampilkan pesan ini.

```html
<div id="alertPlaceholder"></div>
```

## Menambahkan Button dan Validation Feedback

Kita juga butuh menambahkan JavaScript untuk menangani form submission dan menampilkan alert jika form berhasil dikirim.

```html
<script>
  document.getElementById('registrationForm').addEventListener('submit', function(event) {
    event.preventDefault();
    var fullName = document.getElementById('fullName').value;
    var email = document.getElementById('email').value;
    var password = document.getElementById('password').value;

    // Validasi sederhana
    if (fullName && email && password) {
      showAlert('Pendaftaran berhasil!', 'success');
    } else {
      showAlert('Harap lengkapi semua field!', 'danger');
    }
  });

  function showAlert(message, type) {
    var alertPlaceholder = document.getElementById('alertPlaceholder');
    var alert = document.createElement('div');
    alert.className = `alert alert-${type} alert-dismissible fade show`;
    alert.role = 'alert';
    alert.innerHTML = `
      ${message}
      <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
    `;
    alertPlaceholder.append(alert);
  }
</script>
```

![image](https://github.com/user-attachments/assets/5c841280-19c8-43c7-b3cb-9b13bdf56859)

![image](https://github.com/user-attachments/assets/e35f20df-96dc-4e27-b979-fc9a35076bc4)


## Penjelasan Kode

1. **HTML Dasar**: Ini adalah struktur HTML dasar dengan link ke CSS dan JS Bootstrap.
2. **Form Controls**: Kita menambahkan input untuk nama lengkap, email, dan password. Semua input ini diatur sebagai required untuk validasi.
3. **JavaScript untuk Form Submission**: Kita menambahkan event listener untuk menangani submit event dari form. Saat form disubmit, kita mencegah default behavior dari form (yang biasanya mengirim data ke server dan merefresh halaman).
4. **Validasi Sederhana**: Jika semua field terisi, kita menampilkan alert sukses. Jika ada field yang kosong, kita menampilkan alert error.
5. **Fungsi showAlert**: Fungsi ini digunakan untuk membuat dan menampilkan alert dengan pesan dan tipe yang sesuai.

Dengan begitu, temen-temen sekarang punya form pendaftaran yang bisa menampilkan pesan sukses atau error berdasarkan validasi input. Mudah kan?

### Referensi
- [Bootstrap 5 Documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

Selamat mencoba dan semoga berhasil! Jika ada pertanyaan atau masukan, jangan ragu untuk share di kolom komentar. Happy coding, temen-temen!
