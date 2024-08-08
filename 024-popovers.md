Di kesempatan kali ini, kita bakal ngulik tentang **Popovers** di Bootstrap 5. Popovers itu mirip kayak tooltip, tapi bisa menampilkan lebih banyak konten, termasuk HTML. Yuk, kita bahas cara bikin popovers dan cara bikin popovers dengan konten dinamis.

### **Apa Itu Popovers?**

Popover itu adalah elemen UI yang muncul ketika kamu klik atau hover pada suatu elemen, dan menampilkan konten tambahan dalam bentuk overlay. Misalnya, kalau kamu pernah liat pop-up yang muncul ketika kamu klik tombol di aplikasi, nah itu mirip dengan popover.

### **Cara Membuat Popovers**

**1. Menyertakan Bootstrap**

Pertama-tama, kita perlu menyertakan Bootstrap di halaman HTML kita. Kita bakal pakai CDN dari jsDelivr untuk ini.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap Popovers Demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- Popover Trigger -->
    <button type="button" class="btn btn-primary" data-bs-toggle="popover" data-bs-content="This is a popover!">Click me</button>

    <!-- Bootstrap JavaScript Bundle -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>

    <script>
      // Initialize all popovers
      document.querySelectorAll('[data-bs-toggle="popover"]').forEach(popoverTrigger => {
        new bootstrap.Popover(popoverTrigger);
      });
    </script>
  </body>
</html>
```

![image](https://github.com/user-attachments/assets/df08060e-3142-4ff0-b795-af0404777b34)

**Penjelasan Kode:**

- **HTML**: 
  - Kita bikin tombol dengan kelas `btn btn-primary` dan atribut `data-bs-toggle="popover"`. Atribut `data-bs-content` digunakan untuk menentukan konten yang akan ditampilkan di popover.
  
- **JavaScript**: 
  - Kita inisialisasi popovers dengan script JavaScript di akhir body. Script ini mencari semua elemen dengan atribut `data-bs-toggle="popover"` dan membuat instance dari `bootstrap.Popover` untuk masing-masing.

### **Popover dengan Konten Dinamis**

Kadang-kadang kita ingin konten di popover berubah sesuai dengan interaksi pengguna. Misalnya, menampilkan informasi yang berbeda saat pengguna mengklik tombol yang berbeda.

**1. HTML dan Bootstrap Setup**

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Dynamic Popovers Demo</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- Buttons to trigger dynamic popovers -->
    <button type="button" class="btn btn-primary" data-bs-toggle="popover" data-bs-trigger="click" data-bs-html="true" data-bs-content="Loading...">Load Content 1</button>
    <button type="button" class="btn btn-secondary" data-bs-toggle="popover" data-bs-trigger="click" data-bs-html="true" data-bs-content="Loading...">Load Content 2</button>

    <!-- Bootstrap JavaScript Bundle -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>

    <script>
      document.querySelectorAll('[data-bs-toggle="popover"]').forEach(popoverTrigger => {
        new bootstrap.Popover(popoverTrigger, {
          customClass: 'popover-dynamic',
          sanitize: false, // Allow HTML content
          content: function() {
            // Fetch dynamic content based on button ID
            let button = this;
            if (button.getAttribute('data-bs-content') === 'Loading...') {
              return fetchContent(button);
            }
            return button.getAttribute('data-bs-content');
          }
        });
      });

      function fetchContent(button) {
        // Simulate an API call
        return new Promise((resolve) => {
          setTimeout(() => {
            if (button.classList.contains('btn-primary')) {
              resolve('Dynamic Content for Button 1');
            } else {
              resolve('Dynamic Content for Button 2');
            }
          }, 1000); // Simulate delay
        });
      }
    </script>
  </body>
</html>
```
![image](https://github.com/user-attachments/assets/d2b4af1c-1ba7-483c-9130-fa1a8585af45)

**Penjelasan Kode:**

- **HTML**:
  - Sama seperti sebelumnya, tetapi `data-bs-content` diatur ke "Loading..." untuk menandakan bahwa konten akan diambil secara dinamis.

- **JavaScript**:
  - Kita menggunakan `content` function untuk mengambil konten dinamis. Fungsi ini memeriksa apakah `data-bs-content` saat ini adalah "Loading...". Jika iya, maka konten dinamis diambil menggunakan `fetchContent`.
  - `fetchContent` berfungsi untuk mensimulasikan pengambilan data dari server dengan `setTimeout`. Dalam praktik nyata, ini bisa diganti dengan panggilan API yang sesungguhnya.

### **Referensi**

- [Bootstrap Documentation on Popovers](https://getbootstrap.com/docs/5.3/components/popovers/)
- [Bootstrap Popovers API](https://getbootstrap.com/docs/5.3/components/popovers/#api)

Nah, itu dia temen-temen, cara bikin popovers dan popovers dengan konten dinamis menggunakan Bootstrap 5. Semoga penjelasan ini membantu kalian membuat antarmuka yang lebih interaktif dan menarik!
