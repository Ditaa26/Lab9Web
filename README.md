# Lab9Web
## Dita Tiara Putri
## 312310131
## TI 23 A1 

# 1. Buat file baru dengan nama header.php
![Screenshot 2024-11-26 065844](https://github.com/user-attachments/assets/0f93f184-3883-4e30-8b0b-2e26f32f2fa6) 
```sh
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Contoh Modularisasi</title>
<link href="style.css" rel="stylesheet" type="text/stylesheet"media="screen" />
</head>
<body>
    <div class="container">
    <header>
        <h1>Modularisasi Menggunakan Require</h1>
    </header>
    <nav>
        <a href="home.php">Home</a>
        <a href="about.php">Tentang</a>
        <a href="kontak.php">Kontak</a>
    </nav>
    </div>
```
![Screenshot 2024-11-26 070355](https://github.com/user-attachments/assets/5b6d06f2-1294-423c-a31b-aec5b783e9ff) 
File ini adalah kerangka dasar untuk halaman web yang menggunakan gaya modular.  
File PHP (``home.php``, ``about.php``, ``kontak.php``) akan berisi konten atau logika berbeda, sehingga konten dapat dikelola secara modular.  

# 2. Buat file baru dengan nama footer.php 
![Screenshot 2024-11-26 070804](https://github.com/user-attachments/assets/0be5a44a-e5f1-4bcf-8f05-7f677a8d2390) 
```sh
<footer>
        <p>&copy; 2021, Informatika, Universitas Pelita Bangsa</p>
    </footer>
</div>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/ec1f5e5a-ba9e-40cb-aded-1b26fdb2502f) 
``<footer>``: Tag HTML khusus yang digunakan untuk mendefinisikan area footer dalam sebuah dokumen atau bagian utama.  
Biasanya berisi informasi seperti hak cipta, tahun, atau tautan ke kebijakan privasi, syarat penggunaan, atau kontak.  

# 3. Buat file baru dengan nama home.php
![Screenshot 2024-11-26 072217](https://github.com/user-attachments/assets/b690ebde-97c0-432d-af4f-a8da26f1fe99) 
```sh
<?php require('header.php'); ?>
<div class="content">
    <h2>Ini Halaman Home</h2>
    <p>Ini adalah bagian content dari halaman.</p>
</div>
<?php require('footer.php'); ?>
```
![Screenshot 2024-11-26 072539](https://github.com/user-attachments/assets/6f08a305-c460-457d-96fb-ba81c42a3530) 
File ini berfungsi sebagai halaman utama situs, dengan menggunakan ``require()`` untuk memasukkan ``header.php`` di bagian atas dan ``footer.php`` di bagian bawah, sehingga file ini hanya berisi konten unik yang spesifik untuk halaman tersebut.  

# 4 Buat file baru dengan nama about.php
![Screenshot 2024-11-26 073511](https://github.com/user-attachments/assets/63e3c64a-f01c-485d-8edf-ec6ac4f87992) 
```sh
<?php require('header.php'); ?>
<div class="content">
    <h2>Ini Halaman About</h2>
    <p>Ini adalah bagian content dari halaman.</p>
</div>
<?php require('footer.php'); ?>
``` 
![Screenshot 2024-11-26 073645](https://github.com/user-attachments/assets/970e9d17-0a4a-47a4-8890-b58d63f1ce82)  
File ini adalah halaman "About" dari situs, menggunakan ``require()`` untuk menyisipkan ``header.php`` di bagian atas dan ``footer.php`` di bagian bawah, sehingga hanya konten khusus halaman ``"About"`` (judul dan paragraf) yang ditulis di file ini.  

# TUGAS 
Implementasikan konsep modularisasi pada kode program praktikum 8 tentang database, sehingga setiap halamannya memiliki template tampilan yang sama.  

# 1. Buat File tugas_header dan tugas_footer.php 
## tugas_header 
```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modularisasi - Praktikum 8</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
</head>
<body>
    <div class="container">
        <header>
            <h1>Sistem Data Barang</h1>
        </header>
        <nav>
            <a href="index.php">Home</a>
            <a href="tambah.php">Tambah Barang</a>
        </nav>
```
![image](https://github.com/user-attachments/assets/c74ec9a0-6518-4241-9e2a-e2e4f47b75ad) 
Menyediakan bagian atas template untuk setiap halaman web, termasuk deklarasi HTML, elemen header, dan navigasi. 
Menyediakan menu dengan link ke halaman utama (index.php) dan halaman tambah barang (tambah.php).  

## tugas_footer 
```sh
<link href="style.css" rel="stylesheet" type="text/css" />
<footer>
            <p>&copy; 2024, Sistem Informasi, Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
<footer>
        <p>&copy; 2021, Informatika, Universitas Pelita Bangsa</p>
    </footer>
</div>
</body>
</html>
```  
![image](https://github.com/user-attachments/assets/e690ae71-5e9d-433f-8852-34b1bfd5cb86) 
Menyediakan bagian bawah template untuk setiap halaman web.


## CSS 
```sh 
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

.container {
    width: 80%;
    margin: auto;
    overflow: hidden;
}

header {
    background: #69062a;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

nav {
    margin: 10px 0;
    text-align: center;
}

nav a {
    margin: 0 15px;
    text-decoration: underline;
    color: #000ce9;
    font-weight: bold;
}

footer {
    background: #69062a;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    margin-top: 20px;
}  
```
# 2. Membuat file index.php  
```sh
<?php
require('tugas_header.php'); 

$conn = new mysqli("localhost", "root", "", "latihan1");

if ($conn->connect_error) {
    die("Koneksi gagal: " . $conn->connect_error);
}
?>

<div class="content">
    <h2>Data Barang</h2>
    <a href="tambah.php" style="margin-bottom: 10px; display: inline-block;">Tambah Data</a>
    <table border="1" cellspacing="0" cellpadding="10">
        <tr>
            <th>ID</th>
            <th>Kategori</th>
            <th>Nama</th>
            <th>Gambar</th>
            <th>Harga Beli</th>
            <th>Harga Jual</th>
            <th>Stok</th>
            <th>Aksi</th>
        </tr>
        <?php
     
        $sql = "SELECT * FROM data_barang";
        $result = $conn->query($sql);

      
        if ($result->num_rows > 0) {
            while ($row = $result->fetch_assoc()) {
                echo "<tr>
                    <td>{$row['id_barang']}</td>
                    <td>{$row['kategori']}</td>
                    <td>{$row['nama']}</td>
                    <td><img src='{$row['gambar']}' alt='{$row['nama']}' width='50'></td>
                    <td>{$row['harga_beli']}</td>
                    <td>{$row['harga_jual']}</td>
                    <td>{$row['stok']}</td>
                    <td>
                        <a href='ubah.php?id={$row['id_barang']}'>Ubah</a> |
                        <a href='hapus.php?id={$row['id_barang']}' onclick='return confirm(\"Yakin ingin menghapus data ini?\")'>Hapus</a>
                    </td>
                </tr>";
            }
        } else {
            echo "<tr><td colspan='8'>Tidak ada data</td></tr>";
        }

        $conn->close();
        ?>
    </table>
</div>

<?php
require('footer.php'); 
?>
```
![image](https://github.com/user-attachments/assets/2751452c-1980-4368-beb9-1d9839b92197) 
Menghubungkan aplikasi ke database bernama latihan1.  
Menampilkan data barang dalam bentuk tabel HTML agar mudah dibaca oleh pengguna. 
Data diambil dari tabel database menggunakan perintah SQL  ``SELECT``.
Setiap baris data dari hasil query ditampilkan dalam elemen ``<table>``.  
Mengarahkan ke halaman edit (ubah.php).  
Mengarahkan ke halaman hapus (hapus.php).  

# 3 Membuat Tambah Barang  
```sh
<?php
require('tugas_header.php'); 

$conn = new mysqli("localhost", "root", "", "latihan1");

if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $kategori = $_POST['kategori'];
    $nama = $_POST['nama'];
    $gambar = $_POST['gambar'];
    $harga_beli = $_POST['harga_beli'];
    $harga_jual = $_POST['harga_jual'];
    $stok = $_POST['stok'];

    $sql = "INSERT INTO data_barang (kategori, nama, gambar, harga_beli, harga_jual, stok) 
            VALUES ('$kategori', '$nama', '$gambar', '$harga_beli', '$harga_jual', '$stok')";
    
    if ($conn->query($sql) === TRUE) {
        echo "<p>Data berhasil ditambahkan</p>";
    } else {
        echo "<p>Error: " . $conn->error . "</p>";
    }
}
?>

<div class="content">
    <h2>Tambah Data Barang</h2>
    <form method="post">
        <label>Kategori:</label><br>
        <input type="text" name="kategori" required><br>
        <label>Nama:</label><br>
        <input type="text" name="nama" required><br>
        <label>Gambar:</label><br>
        <input type="text" name="gambar" required><br>
        <label>Harga Beli:</label><br>
        <input type="number" name="harga_beli" required><br>
        <label>Harga Jual:</label><br>
        <input type="number" name="harga_jual" required><br>
        <label>Stok:</label><br>
        <input type="number" name="stok" required><br><br>
        <button type="submit">Simpan</button>
    </form>
</div>

<?php
require('footer.php'); 
?>
```
![image](https://github.com/user-attachments/assets/9f6c9204-08fe-4c1f-9bcd-4252abb8f67a) 
![image](https://github.com/user-attachments/assets/c7b91d26-215f-4cd9-ba84-8aad9e30575c) 
![image](https://github.com/user-attachments/assets/87cd67d3-bf94-4e05-80d3-27efc9040c7a) 
![image](https://github.com/user-attachments/assets/05924b5d-615e-4d0d-aa46-f4999f91f780)
![image](https://github.com/user-attachments/assets/64556152-ad87-4fe2-9d23-4292d2d32074)  
Menyimpan data ke dalam tabel data_barang di database menggunakan perintah ``INSERT``.  
Query dieksekusi melalui ``$conn->query($sql)``. Jika berhasil, data baru akan ditambahkan ke dalam tabel ``data_barang`` di database.  

# 4 Membuat Ubah Barang 
## saya mengubah stok pada laptop, yang awalnya 5 menjadi 4
```sh
<?php
require('tugas_header.php');

$conn = new mysqli("localhost", "root", "", "latihan1");

if ($conn->connect_error) {
    die("Koneksi gagal: " . $conn->connect_error);
}

$id_barang = $_GET['id'] ?? null;

if ($id_barang !== null && is_numeric($id_barang)) {
    $sql = "SELECT * FROM data_barang WHERE id_barang = $id_barang";
    $result = $conn->query($sql);

    if ($result->num_rows > 0) {
        $row = $result->fetch_assoc();
    } else {
        die("Data tidak ditemukan.");
    }
}

if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    $id_barang = $_POST['id_barang'];
    $nama = $_POST['nama'];
    $harga_beli = $_POST['harga_beli'];
    $harga_jual = $_POST['harga_jual'];
    $stok = $_POST['stok'];

    $sql = "UPDATE data_barang 
            SET nama = '$nama', harga_beli = '$harga_beli', harga_jual = '$harga_jual', stok = '$stok' 
            WHERE id_barang = $id_barang";

    if ($conn->query($sql) === TRUE) {
        echo "<p>Data berhasil diubah!</p>";
    } else {
        echo "<p>Error: " . $conn->error . "</p>";
    }
}

$conn->close();
?>

<div class="content">
    <h2>Ubah Barang</h2>
    <form method="post" action="">
        <input type="hidden" name="id_barang" value="<?php echo $row['id_barang']; ?>">
        <label for="nama">Nama Barang:</label><br>
        <input type="text" id="nama" name="nama" value="<?php echo $row['nama']; ?>" required><br><br>
        
        <label for="harga_beli">Harga Beli:</label><br>
        <input type="number" id="harga_beli" name="harga_beli" value="<?php echo $row['harga_beli']; ?>" required><br><br>
        
        <label for="harga_jual">Harga Jual:</label><br>
        <input type="number" id="harga_jual" name="harga_jual" value="<?php echo $row['harga_jual']; ?>" required><br><br>
        
        <label for="stok">Stok:</label><br>
        <input type="number" id="stok" name="stok" value="<?php echo $row['stok']; ?>" required><br><br>
        
        <button type="submit">Ubah</button>
    </form>
</div>

<?php
require('tugas_footer.php');
?>
```
![image](https://github.com/user-attachments/assets/f0ee6b05-0d0e-47a5-8fdc-5d003077d096) 
![image](https://github.com/user-attachments/assets/32cfd12e-022d-41f5-9dd9-4bda9f9e401a) 
![image](https://github.com/user-attachments/assets/27c1bd37-a8f4-4513-bbbd-76bf3942880d) 
![image](https://github.com/user-attachments/assets/11360772-7cc1-4c65-93a8-7971fb27063b) 
Kode ini memungkinkan untuk mengambil data barang berdasarkan ID yang diberikan melalui URL.  
Menampilkan form untuk mengubah data barang (seperti nama, harga beli, harga jual, dan stok).  
Setelah form di-submit, data yang diubah akan disimpan kembali ke database menggunakan query ``UPDATE``.  
Jika data berhasil diubah, sistem akan menampilkan pesan sukses, dan jika gagal, akan menampilkan pesan error.  

# 5 Hapus Barang
```sh
<?php
require('tugas_header.php'); 

$conn = new mysqli("localhost", "root", "", "latihan1");

if ($conn->connect_error) {
    die("Koneksi gagal: " . $conn->connect_error);
}

if (!isset($_GET['id']) || empty($_GET['id'])) {
    echo "<p>ID tidak ditemukan. <a href='index.php'>Kembali ke halaman utama</a></p>";
    exit;
}

$id = intval($_GET['id']); 

$sql_delete = "DELETE FROM data_barang WHERE id_barang = $id";

if ($conn->query($sql_delete) === TRUE) {
    echo "<p>Data berhasil dihapus. <a href='index.php'>Kembali ke halaman utama</a></p>";
} else {
    echo "<p>Terjadi kesalahan: " . $conn->error . "</p>";
}

$conn->close();
?>

<?php
require('footer.php'); 
?>
```
![image](https://github.com/user-attachments/assets/8f6cd4c9-3410-4a2d-af11-4277f6ddd5c4) 
![image](https://github.com/user-attachments/assets/d6fbd811-3013-40a1-89f2-6538f72d6400) 
Kode ini memungkinkan pengguna untuk menghapus data barang dari database berdasarkan ID yang diberikan melalui URL.  
Validasi dilakukan untuk memastikan ID yang diterima valid dan ada dalam URL.  
Setelah data berhasil dihapus atau terjadi kesalahan, pesan akan ditampilkan untuk memberi tahu status operasinya.  

## Note: id barang bisa berubah karena saya sebelumnya melakukan hapus dan menambah barang




























