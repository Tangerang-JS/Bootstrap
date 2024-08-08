Hai temen-temen! 🌟 Kali ini gue mau bahas tentang **Progress Bars** di Bootstrap 5, termasuk cara membuatnya, variannya, dan animasi yang bisa kita gunakan. Yuk, simak penjelasan dan contohnya!

### Apa Itu Progress Bar?

Progress Bar adalah komponen yang menunjukkan kemajuan dari sebuah proses atau tugas. Misalnya, saat mengupload file, progress bar menunjukkan seberapa banyak file yang sudah terupload. Di Bootstrap 5, membuat progress bar itu gampang banget dan bisa disesuaikan sesuai kebutuhan.

### Membuat Progress Bar

Bootstrap menyediakan class khusus untuk membuat progress bar dengan cepat dan mudah. Berikut adalah contoh sederhana tentang cara membuat progress bar:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Bootstrap Progress Bar</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <div class="container mt-4">
      <h1>Progress Bar Demo</h1>
      <div class="progress mt-4">
        <div class="progress-bar" role="progressbar" style="width: 25%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">25%</div>
      </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
  </body>
</html>
```
![image](https://github.com/user-attachments/assets/ea2d82d4-6348-4172-bac3-501ad38ca365)

#### Penjelasan Kode:

- **`<div class="progress">`**: Ini adalah kontainer untuk progress bar.
- **`<div class="progress-bar">`**: Ini adalah elemen yang menunjukkan kemajuan. Kita bisa mengatur lebar progress bar dengan properti `width`.
- **`style="width: 25%;"`**: Menentukan lebar progress bar. Dalam contoh ini, lebar bar-nya adalah 25% dari kontainer.
- **`aria-valuenow="25"`**: Menunjukkan nilai saat ini dari progress bar untuk aksesibilitas.
- **`aria-valuemin="0"`** dan **`aria-valuemax="100"`**: Menentukan nilai minimum dan maksimum dari progress bar.

### Variants dan Animasi

Bootstrap juga memungkinkan kita untuk menambahkan variasi dan animasi pada progress bar. Berikut beberapa opsi yang bisa digunakan:

1. **Variasi Warna**: Kita bisa menggunakan kelas tambahan untuk mengubah warna progress bar. Contohnya, untuk warna success, info, warning, dan danger.

```html
<div class="progress mt-4">
  <div class="progress-bar bg-success" role="progressbar" style="width: 75%;" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100">75%</div>
</div>
```

- **`bg-success`**: Menambahkan warna hijau pada progress bar.

2. **Animasi**: Untuk membuat progress bar bergerak secara terus-menerus, kita bisa menggunakan kelas `progress-bar-animated`.

```html
<div class="progress mt-4">
  <div class="progress-bar progress-bar-animated bg-primary" role="progressbar" style="width: 50%;" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">50%</div>
</div>
```

- **`progress-bar-animated`**: Menambahkan animasi bergerak pada progress bar.

### Studi Kasus Sederhana

**Studi Kasus 1: Menggunakan Progress Bar dalam Formulir Upload**

Misalnya, kita mau menampilkan progress bar saat meng-upload file.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>File Upload Progress</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  </head>
  <body>
    <div class="container mt-4">
      <h1>File Upload</h1>
      <form>
        <div class="mb-3">
          <input type="file" class="form-control" id="fileInput">
        </div>
        <button type="button" class="btn btn-primary" onclick="startUpload()">Upload</button>
      </form>
      <div class="progress mt-4" id="progressContainer" style="display: none;">
        <div class="progress-bar progress-bar-animated bg-info" role="progressbar" style="width: 0%;" id="progressBar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100">0%</div>
      </div>
    </div>

    <script>
      function startUpload() {
        const progressBar = document.getElementById('progressBar');
        const progressContainer = document.getElementById('progressContainer');
        
        // Show progress bar
        progressContainer.style.display = 'block';
        
        let width = 0;
        const interval = setInterval(() => {
          if (width >= 100) {
            clearInterval(interval);
          } else {
            width++;
            progressBar.style.width = width + '%';
            progressBar.setAttribute('aria-valuenow', width);
            progressBar.innerText = width + '%';
          }
        }, 100);
      }
    </script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
  </body>
</html>
```
![image](https://github.com/user-attachments/assets/88117690-b88e-4c44-8430-69fbd9a2ee7b)

#### Penjelasan Kode:

- **`startUpload()`**: Fungsi JavaScript yang memulai animasi progress bar.
- **`setInterval`**: Digunakan untuk memperbarui lebar progress bar setiap 100ms.

Dengan kode di atas, kamu bisa mendapatkan gambaran bagaimana progress bar bekerja dan bagaimana menambahkannya dengan animasi. Semoga penjelasan ini membantu temen-temen dalam memahami dan menggunakan progress bar di Bootstrap 5! Jika ada yang mau ditanya lebih lanjut, jangan ragu untuk bertanya ya. 🌟

### Referensi
- [Bootstrap Progress Bars Documentation](https://getbootstrap.com/docs/5.3/components/progress/)
