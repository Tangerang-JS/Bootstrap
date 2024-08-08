**Toasts** adalah komponen Bootstrap yang berguna untuk menampilkan pesan singkat kepada pengguna dalam bentuk notifikasi di sudut layar. Bayangkan temen-temen lagi nulis pesan di aplikasi, dan tiba-tiba muncul notifikasi kecil di sudut layar bilang "Pesan terkirim!" atau "Data berhasil disimpan." Itulah fungsi dari Toasts! 

Mari kita bahas cara membuat dan menggunakan Toasts dengan Bootstrap 5 versi terbaru. 

#### 1. Membuat Toast

Toasts sangat mudah dibuat dengan Bootstrap. Berikut adalah langkah-langkah dan contoh kode sederhana untuk membuat Toast:

##### **Kode HTML:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contoh Toasts Bootstrap 5</title>
  <!-- CSS Bootstrap CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  
  <!-- Button untuk menampilkan Toast -->
  <button type="button" class="btn btn-primary" id="showToastButton">Tampilkan Toast</button>

  <!-- Toast container -->
  <div class="toast-container position-fixed bottom-0 end-0 p-3">
    <div id="myToast" class="toast" role="alert" aria-live="assertive" aria-atomic="true">
      <div class="toast-header">
        <strong class="me-auto">Notifikasi</strong>
        <small>baru saja</small>
        <button type="button" class="btn-close" data-bs-dismiss="toast" aria-label="Close"></button>
      </div>
      <div class="toast-body">
        Ini adalah pesan Toast sederhana.
      </div>
    </div>
  </div>

  <!-- JS Bootstrap CDN -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    // Script untuk menampilkan Toast
    document.getElementById('showToastButton').addEventListener('click', function () {
      var toast = new bootstrap.Toast(document.getElementById('myToast'));
      toast.show();
    });
  </script>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/863976aa-705c-4294-8a55-6526f2109f65)

##### **Penjelasan Kode:**

1. **Link CSS Bootstrap:** 
   - Menggunakan CDN dari jsDelivr untuk memuat Bootstrap 5.3.0 CSS ke dalam halaman.

2. **Button untuk Menampilkan Toast:**
   - Tombol dengan id `showToastButton` yang saat diklik akan memicu munculnya Toast.

3. **Toast Container:**
   - Tempat untuk menampilkan Toast yang berada di sudut kanan bawah layar.
   - `position-fixed` menjaga Toast tetap berada di tempat tersebut meskipun halaman di-scroll.
   - `toast` adalah kelas yang menentukan bahwa elemen ini adalah Toast.

4. **Toast Header dan Body:**
   - `toast-header` berisi informasi seperti judul dan tombol tutup.
   - `toast-body` berisi teks pesan Toast.

5. **Script untuk Menampilkan Toast:**
   - Menggunakan JavaScript untuk menangani klik tombol dan menampilkan Toast.
   - `new bootstrap.Toast()` membuat instance Toast dari elemen dengan id `myToast`.
   - `toast.show()` menampilkan Toast di layar.

#### 2. Toast dengan Auto-Dismiss

Toasts secara default tidak hilang dengan sendirinya, tetapi bisa dikonfigurasi untuk menghilang otomatis setelah beberapa detik. Mari kita tambahkan fitur ini.

##### **Kode HTML dan JavaScript yang Diperbarui:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contoh Toasts Bootstrap 5 dengan Auto-Dismiss</title>
  <!-- CSS Bootstrap CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  
  <!-- Button untuk menampilkan Toast -->
  <button type="button" class="btn btn-primary" id="showToastButton">Tampilkan Toast</button>

  <!-- Toast container -->
  <div class="toast-container position-fixed bottom-0 end-0 p-3">
    <div id="myToast" class="toast align-items-center text-bg-primary border-0" role="alert" aria-live="assertive" aria-atomic="true">
      <div class="d-flex">
        <div class="toast-body">
          Ini adalah pesan Toast otomatis menghilang setelah beberapa detik.
        </div>
        <button type="button" class="btn-close btn-close-white me-2 m-auto" data-bs-dismiss="toast" aria-label="Close"></button>
      </div>
    </div>
  </div>

  <!-- JS Bootstrap CDN -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    // Script untuk menampilkan Toast dengan auto-dismiss
    document.getElementById('showToastButton').addEventListener('click', function () {
      var toast = new bootstrap.Toast(document.getElementById('myToast'), {
        autohide: true,  // Mengaktifkan auto-dismiss
        delay: 3000      // Waktu dalam milidetik (3 detik)
      });
      toast.show();
    });
  </script>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/7b4fdde7-4c1a-4b73-bfa7-ae35f1513818)

##### **Penjelasan Kode yang Diperbarui:**

1. **`autohide: true`:**
   - Menyeting Toast untuk secara otomatis menghilang setelah periode tertentu.

2. **`delay: 3000`:**
   - Mengatur durasi Toast tampil di layar selama 3 detik (3000 milidetik).

3. **Tampilan dan Styling:**
   - `text-bg-primary` untuk memberikan background biru pada Toast.
   - `btn-close-white` untuk warna tombol close yang kontras dengan background.

Dengan menggunakan kode ini, Toast akan muncul di layar saat tombol diklik dan menghilang secara otomatis setelah beberapa detik.

#### Referensi

- [Dokumentasi Bootstrap 5 Toasts](https://getbootstrap.com/docs/5.3/components/toasts/)
- [Bootstrap 5 CDN dari jsDelivr](https://www.jsdelivr.com/package/npm/bootstrap)

Semoga penjelasan ini memudahkan temen-temen dalam memahami dan menggunakan Toasts di proyek Bootstrap!
