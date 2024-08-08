Halo temen-temen! 😄 Kali ini kita bakal bahas tentang fitur keren di Bootstrap 5 yang bernama **Collapse**. Fitur ini sangat berguna untuk membuat konten yang bisa disembunyikan atau ditampilkan sesuai kebutuhan, seperti pada menu yang bisa dibuka-tutup atau informasi tambahan yang hanya muncul saat dibutuhkan. Yuk, kita eksplor lebih dalam tentang fitur ini dengan beberapa contoh implementasi sederhana!

---

### Apa Itu Collapse?

Bayangkan temen-temen punya sebuah kotak yang bisa diisi dengan informasi atau konten. Kotak ini punya tombol yang bisa dibuka dan ditutup. Ketika tombol diklik, kotak ini akan terbuka untuk menunjukkan isinya atau menutup untuk menyembunyikan isinya. Nah, fitur Collapse di Bootstrap berfungsi seperti itu!

Fitur ini memungkinkan kita untuk menyembunyikan atau menampilkan elemen dengan transisi animasi yang halus. Biasanya, ini digunakan dalam menu, panel, atau elemen lainnya yang mungkin memerlukan lebih banyak ruang di halaman web.

---

### Cara Kerja Collapse

Bootstrap Collapse menggunakan **JavaScript** untuk menangani proses buka-tutup konten. Bootstrap menyediakan kelas dan atribut HTML yang memudahkan kita dalam mengatur konten yang bisa di-collapse.

#### 1. Menyembunyikan dan Menampilkan Konten

Untuk menyembunyikan dan menampilkan konten, kita bisa menggunakan kelas `collapse` dari Bootstrap. Kelas ini digunakan pada elemen yang ingin kita sembunyikan atau tampilkan.

##### Contoh Kode:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Collapse Example</title>
  <!-- Bootstrap CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<div class="container mt-5">
  <h1>Contoh Collapse di Bootstrap</h1>

  <!-- Tombol untuk Mengaktifkan Collapse -->
  <button class="btn btn-primary" type="button" data-bs-toggle="collapse" data-bs-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
    Toggle Collapse
  </button>

  <!-- Konten yang Bisa di-Collapse -->
  <div class="collapse" id="collapseExample">
    <div class="card card-body mt-3">
      Ini adalah konten yang disembunyikan atau ditampilkan menggunakan Collapse. 
      Klik tombol di atas untuk melihatnya!
    </div>
  </div>
</div>

<!-- Bootstrap JS dan Popper.js CDN -->
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.min.js"></script>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/104c52ea-a41e-4e60-9883-656f6f899594)

##### Penjelasan Kode:

1. **Tombol Toggle:**
   - Kelas `btn btn-primary` memberikan styling pada tombol.
   - `data-bs-toggle="collapse"` memberi tahu tombol ini untuk mengendalikan elemen collapse.
   - `data-bs-target="#collapseExample"` menunjuk ke elemen dengan ID `collapseExample`, yang merupakan konten yang akan disembunyikan atau ditampilkan.
   - `aria-expanded="false"` menunjukkan bahwa konten awalnya tersembunyi.

2. **Konten Collapse:**
   - Kelas `collapse` pada elemen ini membuatnya tersembunyi secara default.
   - ID `collapseExample` digunakan untuk mengaitkan elemen ini dengan tombol.

3. **Bootstrap JS dan Popper.js:**
   - Script ini diperlukan untuk menjalankan fungsionalitas JavaScript dari Bootstrap.

---

#### 2. Collapse dengan Accordion

Sekarang, kita akan bahas tentang **Accordion** yang merupakan salah satu cara khusus menggunakan fitur Collapse. Accordion memungkinkan kita untuk membuat grup konten di mana hanya satu panel yang bisa dibuka pada satu waktu. Ini sering digunakan untuk menu atau FAQ.

##### Contoh Kode:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Accordion Example</title>
  <!-- Bootstrap CSS CDN -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<div class="container mt-5">
  <h1>Contoh Accordion di Bootstrap</h1>

  <div class="accordion" id="accordionExample">
    <div class="accordion-item">
      <h2 class="accordion-header" id="headingOne">
        <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
          Item #1
        </button>
      </h2>
      <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne" data-bs-parent="#accordionExample">
        <div class="accordion-body">
          Konten dari item pertama. Hanya satu item yang bisa dibuka pada satu waktu.
        </div>
      </div>
    </div>
    <div class="accordion-item">
      <h2 class="accordion-header" id="headingTwo">
        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
          Item #2
        </button>
      </h2>
      <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#accordionExample">
        <div class="accordion-body">
          Konten dari item kedua. Klik untuk membuka atau menutup konten ini.
        </div>
      </div>
    </div>
  </div>

</div>

<!-- Bootstrap JS dan Popper.js CDN -->
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.min.js"></script>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/eb1ed40d-7eb2-419c-a032-ff2a9a00835e)

##### Penjelasan Kode:

1. **Accordion Container:**
   - Kelas `accordion` pada elemen pembungkus untuk menandakan bahwa ini adalah komponen Accordion.
   - `data-bs-parent="#accordionExample"` memastikan bahwa hanya satu item yang dapat dibuka pada satu waktu.

2. **Accordion Item:**
   - Kelas `accordion-item` untuk setiap elemen item.
   - Kelas `accordion-button` untuk tombol yang akan mengontrol collapse.

3. **Accordion Content:**
   - Konten yang akan ditampilkan atau disembunyikan menggunakan kelas `accordion-collapse`.

---

### Referensi

Temen-temen bisa memeriksa dokumentasi resmi Bootstrap 5 untuk informasi lebih lanjut:

- [Bootstrap Collapse Documentation](https://getbootstrap.com/docs/5.3/components/collapse/)
- [Bootstrap Accordion Documentation](https://getbootstrap.com/docs/5.3/components/accordion/)

Semoga penjelasan ini membantu temen-temen dalam memahami dan menerapkan fitur Collapse dan Accordion di Bootstrap 5! Jika ada yang ingin ditanyakan, jangan ragu untuk bertanya ya! 😊
