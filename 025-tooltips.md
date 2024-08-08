Halo temen-temen! Pada kesempatan kali ini, kita bakal belajar tentang cara membuat dan menata **Tooltips** di Bootstrap 5. Tooltips ini adalah elemen kecil yang muncul ketika kita mengarahkan mouse ke sebuah elemen. Biasanya, tooltips ini digunakan untuk memberikan informasi tambahan tanpa mengacaukan tampilan utama.

### 1. Membuat Tooltips

Untuk membuat tooltips di Bootstrap 5, kita hanya perlu menggunakan atribut `data-bs-toggle="tooltip"` pada elemen yang ingin kita beri tooltip. Mari kita lihat contoh implementasinya:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap Tooltip Demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <div class="container mt-5">
      <button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-placement="top" title="Tooltip on top">
        Hover me
      </button>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
    <script>
      // Menginisialisasi semua tooltips di halaman
      var tooltipTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="tooltip"]'));
      tooltipTriggerList.map(function (tooltipTriggerEl) {
        return new bootstrap.Tooltip(tooltipTriggerEl);
      });
    </script>
  </body>
</html>
```
![image](https://github.com/user-attachments/assets/5ab7b2de-6627-419f-a2d1-1f0a4ba27785)

**Penjelasan Kode:**

- **HTML:**
  - Kita membuat sebuah tombol (`button`) dengan kelas `btn` dan `btn-primary` dari Bootstrap.
  - Kita menambahkan atribut `data-bs-toggle="tooltip"` untuk menunjukkan bahwa elemen ini akan memiliki tooltip.
  - Atribut `data-bs-placement` menentukan posisi tooltip. Dalam contoh ini, kita menggunakan `top`, tetapi kita bisa menggantinya dengan `bottom`, `left`, atau `right`.

- **JavaScript:**
  - Di akhir halaman, kita menggunakan JavaScript untuk menginisialisasi tooltip. Script ini mencari semua elemen yang memiliki atribut `data-bs-toggle="tooltip"` dan menginisialisasinya sebagai tooltip menggunakan `bootstrap.Tooltip`.

### 2. Tooltip Styling dan Penempatan

Untuk styling dan penempatan tooltip, kita bisa memanfaatkan beberapa opsi yang disediakan oleh Bootstrap.

- **Penempatan Tooltip:**
  - `top` - Tooltip muncul di atas elemen.
  - `bottom` - Tooltip muncul di bawah elemen.
  - `left` - Tooltip muncul di sebelah kiri elemen.
  - `right` - Tooltip muncul di sebelah kanan elemen.

- **Styling Tooltip:**
  - Bootstrap menggunakan styling default yang sudah cukup baik, tapi kita bisa menyesuaikan gaya tooltip dengan CSS tambahan jika diperlukan.

**Contoh Styling:**

```html
<style>
  .custom-tooltip .tooltip-inner {
    background-color: #ff6f61; /* Warna latar belakang */
    color: #fff; /* Warna teks */
  }
  .custom-tooltip .tooltip-arrow {
    border-top-color: #ff6f61; /* Warna panah tooltip */
  }
</style>
```

**Penerapan Styling dalam Kode:**

```html
<button type="button" class="btn btn-primary custom-tooltip" data-bs-toggle="tooltip" data-bs-placement="top" title="Custom Tooltip">
  Hover me
</button>
```

Dengan menggunakan class `custom-tooltip`, kita mengubah warna background, warna teks, dan warna panah tooltip sesuai dengan preferensi kita.

### Referensi

- [Bootstrap Tooltip Documentation](https://getbootstrap.com/docs/5.3/components/tooltips/)
- [Bootstrap 5 Documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

Dengan penjelasan ini, semoga temen-temen bisa dengan mudah memahami dan mengimplementasikan tooltips di proyek kalian. Selamat mencoba dan semoga bermanfaat! 😊
