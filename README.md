###### Nama      : Irdiansyah Nur R.
###### Kelas     : XII RPL 1
###### No. Absen : 29

## Modul 4
#### View Blade Template
>Tugas 1 Membuat View

1) Membuat folder dan file yang mau diisi

### Nama folder yang harus dibuat 
- barang
- kategori
- layout

### Nama file yang harus dibuat
- home.blade.php
- index.blade.php
- app.blade.php

Folder dan file-file nya menjadi satu seperti 
contoh gambar yang terlihat seperti dibawah ini:
![image](https://user-images.githubusercontent.com/110436827/183369308-3c30aaf2-6dda-483b-8158-22e21474d23d.png)

>Tugas 2 membuat layout dengan master template blade

2) Pada folder layout `file app.blade.php` dan kita mengambil **css dan js di bootstrap** link di bawah ini:
https://getbootstrap.com/docs/5.2/getting-started/introduction/
![image](https://user-images.githubusercontent.com/110436827/183370642-e62fee14-acdc-4c0a-a6a6-8a081847f1e1.png)

Gambar yang diatas bagian bootstrap yang kita pakai sebagai css dengan menambahkan syntax sebagai berikut.
```
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
```

Berikutnya bagian jss dengan menambahkan syntax sebagai berikut
```
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>
```

Isilah file `app.blade.php` dengan all codenya!!
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>@yield('title')</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">

</head>
<body>
    <!-- untuk navbar -->
    <div class="container">
    <nav class="navbar navbar-expand-lg bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Penjualan</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/kategori">Kategori</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/barang">barang</a>
        </li>
        
    </div>
  </div>
</nav>
    </div>
    <!-- content -->
    <div class="container">
    @yield('content')
    </div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-A3rJD856KowSb7dwlZdYEkO39Gagi7vIsF0jrRAoQmDKKtQBHUuLZ9AsSv4jD4Xa" crossorigin="anonymous"></script>
</body>
</html>
```

Saya tidak menggunakan cara, yang saya jelaskan karena di bootstrap sudah ada jadi saya tinggal copy dan paste saja

Berikutnya folder **barang** yang berisi file `home.blade.php`

all codenya akan terlihat seperti dibawah ini karena kurang lebih saya memahami isi code dibawah:
```
@extends('layout.app')

@section('title')
    Barang
@endsection

@section('content')
<div class="mt-3">
<table class="table table-striped">
    <thead>
        <tr>
            <th width=5%>No</th>
            <th>Nama</th>
            <th width=15%>Kategori</th>
            <th width=10%>QTY</th>
            <th width=15%>Harga Beli</th>
            <th width=15%>Harga Jual</th>
            <th width=15%>Aksi</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <td>1.</td>
            <td>meja</td>
            <td>barang</td>
            <td>12</td>
            <td>Rp.50000</td>
            <td>Rp.55000</td>
            <td>Hapus | Edit</td>
        </tr>
        <tr>
            <td>2.</td>
            <td>kursi</td>
            <td>barang</td>
            <td>12</td>
            <td>Rp.40000</td>
            <td>Rp.45000</td>
            <td>Hapus | Edit</td>
        </tr>
    </tbody>
</div>
</table>
@endsection
```

Berikutnya pada folder **kategori** file `index.blade.php` 

all codenya akan ditampilkan di bawah ini:
```
@extends('layout.app')

@section('title')
    Kategori
@endsection

@section('content')
<div class="mt-3">
    <table class="table table-striped">
    <thead>
        <tr>
            <th width=5%>No</th>
            <th>Nama</th>
            <th width=15%>Kategori</th>
            <th width=10%>QTY</th>
            <th width=15%>Harga Beli</th>
            <th width=15%>Harga Jual</th>
            <th width=15%>Aksi</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <td>1.</td>
            <td>ATK</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td>Hapus | Edit</td>
        </tr>
        <tr>
            <td>2.</td>
            <td>Komputer</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td>Hapus | Edit</td>
        </tr><tr>
            <td>3.</td>
            <td>Accessoris</td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td>Hapus | Edit</td>
        </tr>
    </tbody>
</div>
</table>
@endsection
```

<!-- @extends('layout.app') yang beratri mewariskan ke (folder.file) -->

<!-- @section('title') barang @endsection berarti mengelompokkan agar bisa dipanggil ke berbagai file seperti pewarisan -->

hasil dari code yang kita kerjakan akan terlihat seperti dibawah ini

code yang ditampilkan ini dari folder **barang** file `home.blade.php`

![image](https://user-images.githubusercontent.com/110436827/183373473-9eccae9a-f562-4ba3-89d1-d21250c4963f.png)

![image](https://user-images.githubusercontent.com/110436827/183373658-cc97c05e-850f-4cef-8233-91ff7905beda.png)

Gambar diatas adalah jawabannya, Sekian terimakasih
