Kali ini kita bakal bahas tentang **Tables** di Bootstrap—sebuah fitur yang penting banget buat menampilkan data dengan cara yang terstruktur dan menarik. Bootstrap versi terbaru yang kita pakai adalah Bootstrap 5, jadi kita bakal fokus pada fitur-fitur dan cara implementasi yang ada di versi ini.

### Apa Itu Tabel di Bootstrap?

Di Bootstrap, tabel digunakan untuk menampilkan data dalam format grid, yang memudahkan kita untuk menyajikan informasi dengan cara yang rapi dan terstruktur. Bootstrap menyediakan beberapa fitur canggih untuk mempercantik dan memperbaiki tabel, seperti styling, responsivitas, dan pengaturan berbagai elemen dalam tabel.

### Fitur Utama Tabel di Bootstrap

1. **Tabel Dasar**
2. **Tabel Responsif**
3. **Tabel dengan Styling**
4. **Tabel Hover dan Striped**
5. **Tabel dengan Border**

### 1. Tabel Dasar

Tabel dasar adalah tabel yang paling sederhana dengan baris dan kolom yang diatur dalam format grid. 

#### Contoh Kode

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bootstrap Table Basic</title>
  <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.3.3/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <div class="container mt-4">
    <h2>Basic Table</h2>
    <table class="table">
      <thead>
        <tr>
          <th>#</th>
          <th>Name</th>
          <th>Age</th>
          <th>Location</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>1</td>
          <td>John Doe</td>
          <td>30</td>
          <td>New York</td>
        </tr>
        <tr>
          <td>2</td>
          <td>Jane Smith</td>
          <td>25</td>
          <td>Los Angeles</td>
        </tr>
      </tbody>
    </table>
  </div>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/2e0791c7-f236-4561-9441-0f4da0505908)

#### Penjelasan Kode

- `<table class="table">` adalah elemen tabel dasar dari Bootstrap.
- `<thead>` mendefinisikan bagian header tabel yang berisi judul kolom.
- `<tbody>` berisi baris-baris data tabel.
- Di dalam `<tr>`, kita mendefinisikan baris tabel, dan `<th>` untuk header kolom, sedangkan `<td>` untuk sel data.

### 2. Tabel Responsif

Tabel responsif memungkinkan tabel menyesuaikan lebar layar perangkat yang digunakan, sehingga tabel tetap dapat dibaca dengan baik di berbagai ukuran layar.

#### Contoh Kode

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bootstrap Responsive Table</title>
  <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.3.3/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <div class="container mt-4">
    <h2>Responsive Table</h2>
    <div class="table-responsive">
      <table class="table">
        <thead>
          <tr>
            <th>#</th>
            <th>Name</th>
            <th>Age</th>
            <th>Location</th>
            <th>Occupation</th>
            <th>Email</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>John Doe</td>
            <td>30</td>
            <td>New York</td>
            <td>Engineer</td>
            <td>john@example.com</td>
          </tr>
          <tr>
            <td>2</td>
            <td>Jane Smith</td>
            <td>25</td>
            <td>Los Angeles</td>
            <td>Designer</td>
            <td>jane@example.com</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/f5796b52-9468-40b8-8d4d-135473d49198)

![image](https://github.com/user-attachments/assets/205787d9-6065-49bb-87f9-210ccf0853ff)


#### Penjelasan Kode

- `<div class="table-responsive">` membungkus tabel untuk membuatnya responsif.
- Tabel akan secara otomatis menyesuaikan lebar layar perangkat, memungkinkan scroll horizontal jika tabel terlalu lebar.

### 3. Tabel dengan Styling

Bootstrap memungkinkan kita menambahkan berbagai gaya ke tabel, seperti tabel striping, hover efek, dan border.

#### Contoh Kode

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Styled Bootstrap Table</title>
  <link href="https://stackpath.bootstrapcdn.com/bootstrap/5.3.3/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
  <div class="container mt-4">
    <h2>Styled Table</h2>
    <table class="table table-striped table-hover table-bordered">
      <thead>
        <tr>
          <th>#</th>
          <th>Name</th>
          <th>Age</th>
          <th>Location</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>1</td>
          <td>John Doe</td>
          <td>30</td>
          <td>New York</td>
        </tr>
        <tr>
          <td>2</td>
          <td>Jane Smith</td>
          <td>25</td>
          <td>Los Angeles</td>
        </tr>
      </tbody>
    </table>
  </div>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/d3ffd31c-41c9-4663-9dd9-e4eb32bbadec)


#### Penjelasan Kode

- `table-striped` menambahkan garis-garis latar belakang bergantian pada baris tabel untuk meningkatkan keterbacaan.
- `table-hover` menambahkan efek hover pada baris tabel.
- `table-bordered` menambahkan border pada tabel dan sel.

### Referensi dan Sumber Belajar

Untuk informasi lebih lanjut tentang penggunaan tabel di Bootstrap, temen-temen bisa cek dokumentasi resmi Bootstrap:
- [Bootstrap Tables Documentation](https://getbootstrap.com/docs/5.3/content/tables/)

Dengan memahami dan menerapkan berbagai fitur tabel di Bootstrap, temen-temen bisa membuat tampilan data yang tidak hanya informatif tetapi juga menarik dan mudah digunakan di berbagai perangkat. Semoga penjelasan ini membantu, dan jangan ragu untuk bereksperimen dengan berbagai opsi styling yang ada!
