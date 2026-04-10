<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Hiker Best</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
<div class="container">

    <!-- SIDEBAR -->
    <aside class="sidebar" id="sidebar">
        <div class="sidebar-header">
            <h2>Hiker Best</h2>
            <button class="toggle-btn" onclick="toggleSidebar()">☰</button>
        </div>

       <ul class="menu">
    <li><a href="#">Gunung Favorit</a></li>
    <li><a href="peralatancrud.html">Peralatan</a></li>
    <li><a href="crudcuaca.html">Cuaca</a></li>
    <li><a href="#" onclick="openModal('modalGunung')">Tambah Gunung</a></li>
 
</ul>

<div id="modalGunung" class="modal" style="display:none; position:fixed; z-index:9999; left:0; top:0; width:100%; height:100%; background:rgba(0,0,0,0.7);">
    <div style="background:#fff; margin:10% auto; padding:20px; width:300px; border-radius:10px; color:#333;">
        <h3>Tambah Data Gunung</h3>
        <input type="text" id="newNama" placeholder="Nama Gunung" style="width:100%; margin-bottom:10px; padding:8px;">
        <input type="text" id="newLokasi" placeholder="Lokasi" style="width:100%; margin-bottom:10px; padding:8px;">
        <input type="text" id="newTinggi" placeholder="Tinggi (mdpl)" style="width:100%; margin-bottom:10px; padding:8px;">
        <textarea id="newDeskripsi" placeholder="Deskripsi Singkat" style="width:100%; margin-bottom:10px; padding:8px;"></textarea>
        <button onclick="simpanGunung()" style="background:#2f8f4a; color:white; border:none; padding:10px; width:100%; cursor:pointer;">Simpan Data</button>
        <button onclick="closeModal('modalGunung')" style="background:#ccc; border:none; padding:5px; width:100%; margin-top:5px; cursor:pointer;">Batal</button>
    </div>
</div>

<div id="modalGaleri" class="modal" style="display:none; position:fixed; z-index:9999; left:0; top:0; width:100%; height:100%; background:rgba(0,0,0,0.7);">
    <div style="background:#fff; margin:10% auto; padding:20px; width:300px; border-radius:10px; color:#333;">
        <h3>Tambah Foto Galeri</h3>
        <input type="file" id="galeriFile" style="width:100%; margin-bottom:10px; padding:8px;">
        <input type="text" id="galeriCaption" placeholder="Judul/Caption Foto" style="width:100%; margin-bottom:10px; padding:8px;">
        <button onclick="alert('Fitur upload galeri siap dikembangkan!')" style="background:#2f8f4a; color:white; border:none; padding:10px; width:100%; cursor:pointer;">Unggah Foto</button>
        <button onclick="closeModal('modalGaleri')" style="background:#ccc; border:none; padding:5px; width:100%; margin-top:5px; cursor:pointer;">Batal</button>
    </div>
</div>



<div id="modalGunung" class="modal" style="display:none; position:fixed; z-index:9999; left:0; top:0; width:100%; height:100%; background:rgba(0,0,0,0.7);">
    <div style="background:#fff; margin:10% auto; padding:20px; width:300px; border-radius:10px; color:#333;">
        <h3>Tambah Data Gunung</h3>
        <input type="text" id="newNama" placeholder="Nama Gunung" style="width:100%; margin-bottom:10px; padding:8px;">
        <input type="text" id="newLokasi" placeholder="Lokasi" style="width:100%; margin-bottom:10px; padding:8px;">
        <input type="text" id="newTinggi" placeholder="Tinggi (mdpl)" style="width:100%; margin-bottom:10px; padding:8px;">
        <textarea id="newDeskripsi" placeholder="Deskripsi Singkat" style="width:100%; margin-bottom:10px; padding:8px;"></textarea>
        <button onclick="simpanGunung()" style="background:#2f8f4a; color:white; border:none; padding:10px; width:100%; cursor:pointer;">Simpan Data</button>
        <button onclick="closeModal()" style="background:#ccc; border:none; padding:5px; width:100%; margin-top:5px; cursor:pointer;">Batal</button>
    </div>
</div>
        </ul>

        <div class="sidebar-footer">
            © 2025 Hiker Best
        </div>
    </aside>

    <!-- MAIN CONTENT -->
    <main class="main">
        <h1>Data Gunung Favorit</h1>
        <div class="card-container" id="cardContainer"></div>
    </main>

</div>

<script src="script.js"></script>
</body>
</html>
