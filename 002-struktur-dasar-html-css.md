### Struktur Dasar HTML dan CSS dengan Bootstrap

Halo temen-temen! Kali ini gue bakal jelasin tentang cara bikin struktur dasar HTML dan CSS menggunakan Bootstrap. Jadi, buat temen-temen yang pengen mulai belajar Bootstrap, artikel ini cocok banget buat kalian!

#### Apa itu Bootstrap?
Bootstrap adalah framework CSS yang paling populer buat bikin website responsive dan modern. Dengan Bootstrap, kalian nggak perlu repot-repot nulis CSS dari nol karena udah disediain banyak komponen siap pakai. Asik banget, kan?

#### Cara Mengintegrasikan Bootstrap ke dalam Proyek
Langkah pertama, temen-temen harus nyertain file CSS dan JavaScript dari Bootstrap ke dalam proyek HTML kalian. Gampang kok, kita bisa pake CDN (Content Delivery Network).

#### Implementasi Kode Sederhana
Sekarang, gue bakal tunjukin gimana cara mengintegrasikan Bootstrap versi terbaru ke dalam proyek HTML kalian.

1. **Bikin File HTML Dasar**

   Pertama-tama, bikin file HTML baru. Misalnya, namanya `index.html`.

2. **Tambahin Bootstrap CDN**

   Supaya Bootstrap bisa dipake, kita perlu nyertain Bootstrap CDN ke dalam file HTML kita. Copy kode di bawah ini ke dalam `index.html` kalian:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Example</title>
    <!-- Bootstrap CSS -->
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <h1 class="text-center">Halo, Temen-temen!</h1>
    <div class="container">
        <div class="row">
            <div class="col-md-4">
                <div class="p-3 bg-primary text-white">Kolom 1</div>
            </div>
            <div class="col-md-4">
                <div class="p-3 bg-secondary text-white">Kolom 2</div>
            </div>
            <div class="col-md-4">
                <div class="p-3 bg-success text-white">Kolom 3</div>
            </div>
        </div>
    </div>
    <!-- Bootstrap JS and dependencies -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/js/bootstrap.min.js"></script>
</body>
</html>
```

![image](https://github.com/user-attachments/assets/c31f8b26-f4aa-4c8a-a6b7-cbe8a6cc8e68)


#### Penjelasan Kode

1. **Doctype dan HTML Basic Structure**
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Bootstrap Example</title>
   </head>
   <body>
   </body>
   </html>
   ```
   Kode di atas adalah struktur dasar HTML. Kita mulai dengan `<!DOCTYPE html>` yang ngasih tau browser kalau ini adalah dokumen HTML5. Lalu, kita bikin elemen `html`, `head`, dan `body` yang merupakan struktur dasar dari setiap dokumen HTML.

2. **Menghubungkan Bootstrap CSS**
   ```html
   <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/css/bootstrap.min.css" rel="stylesheet">
   ```
   Kode ini adalah link ke file CSS Bootstrap. Kita pake CDN supaya nggak perlu download dan nyimpen file Bootstrap di komputer kita.

3. **Menambahkan Konten**
   ```html
   <h1 class="text-center">Halo, Temen-temen!</h1>
   <div class="container">
       <div class="row">
           <div class="col-md-4">
               <div class="p-3 bg-primary text-white">Kolom 1</div>
           </div>
           <div class="col-md-4">
               <div class="p-3 bg-secondary text-white">Kolom 2</div>
           </div>
           <div class="col-md-4">
               <div class="p-3 bg-success text-white">Kolom 3</div>
           </div>
       </div>
   </div>
   ```
   Di sini kita bikin elemen `h1` dengan class `text-center` dari Bootstrap buat ngecenter teks. Terus kita bikin container (`<div class="container">`) yang di dalamnya ada row (`<div class="row">`) dan beberapa kolom (`<div class="col-md-4">`). Setiap kolom dikasih padding (`p-3`), background color, dan text color.

4. **Menghubungkan Bootstrap JS dan Dependencies**
   ```html
   <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
   <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"></script>
   <script src="https://stackpath.bootstrapcdn.com/bootstrap/5.3.0/js/bootstrap.min.js"></script>
   ```
   Bagian ini buat nyertain file JavaScript Bootstrap dan dependencies-nya (jQuery dan Popper.js) supaya komponen-komponen Bootstrap yang butuh JavaScript bisa berfungsi dengan baik.

#### Kesimpulan
Nah, itu dia penjelasan tentang cara bikin struktur dasar HTML dan CSS dengan Bootstrap. Gampang banget kan? Dengan Bootstrap, temen-temen bisa lebih cepat dan mudah buat bikin website yang responsive dan keren. Jadi, tunggu apa lagi? Ayo coba bikin proyek Bootstrap pertama kalian! 🎉

Semoga artikel ini bermanfaat buat temen-temen semua. Sampai jumpa di artikel selanjutnya! 👋
