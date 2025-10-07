<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Saya</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0; padding: 0;
      background-color: #f5f3f0; /* warna latar belakang soft */
    }

    header {
      background-color: #110586; /* coklat susu gelap */
      color: white;
      padding: 30px 0;
      text-align: center;
    }

    nav {
      background-color: #87cefa; /* biru medium */
      display: flex;
      justify-content: center;
    }

    nav a, .dropbtn {
      color: white;
      text-decoration: none;
      padding: 14px 20px;
      font-weight: bold;
      display: inline-block;
    }

    nav a:hover, .dropdown:hover .dropbtn {
      background-color: #110586;
      border-radius: 5px;
    }

    /* Dropdown */
    .dropdown {
      position: relative;
      display: inline-block;
    }
    .dropdown-content {
      display: none;
      position: absolute;
      background: #fff;
      min-width: 160px;
      box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
      z-index: 1;
      border-radius: 5px;
    }
    .dropdown-content a {
      color: #333;
      padding: 10px 14px;
      display: block;
      text-decoration: none;
    }
    .dropdown-content a:hover {
      background: #f2e6da;
    }
    .dropdown:hover .dropdown-content {
      display: block;
    }

    section {
      display: none;
      padding: 40px;
      text-align: center;
    }
    section.active {
      display: block;
    }

    .card {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      display: inline-block;
    }

    button {
      background: #110586;
      color: white;
      padding: 8px 14px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 10px;
    }
    button:hover {
      background: #8c5e47;
    }

    input {
      padding: 5px;
      margin: 5px;
      border-radius: 4px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>

  <header>
    <h1>⋆˚✿˖° Website Anita Putri Lestari 🧸༄.°</h1>
    <p>Blog Website Saya</p>
  </header>

  <nav>
    <a href="#" onclick="showPage('beranda')">Beranda</a>
    <a href="tentang anita.html" onclicke="showPage('tentang')">Tentang Saya</a>
    <a href="Jadwal Pelajaran.html" onclicke="showPage('jadwal')">Jadwal Pelajaran</a>
    <a href="lirik lago.html" onclicke="showPage('syair')">Syair Lagu</a>
    <div class="dropdown">
      <a href="#" class="dropbtn">Menghitung ▼</a>
      <div class="dropdown-content">
        <a href="#" onclick="showPage('luas')">Luas Persegi</a>
        <a href="#" onclick="showPage('volume')">Volume Kotak</a>
      </div>
    </div>
  </nav>

  <!-- Halaman -->
  <section id="beranda" class="active">
    <div class="card">
      <h2>Haiii Selamat Datang!~</h2>
      <p>Blog ini merupakan beranda Anita Putri Lestari siswi SMKN 1 Kota Tangerang.</p>
    </div>
  </section>

  <section id="tentang">
    <div class="card">
      <h2>Tentang Saya</h2>
      <p>Halo, kenalin nama aku Anita dan ini adalah web pribadi tentang diri aku.</p>
    </div>
  </section>

  <section id="jadwal">
    <div class="card">
      <h2>Jadwal Pelajaran</h2>
          <p>Berikut jadwal mingguan aku di kelas XII DKV 2.</p>
 </div>
  </section>

  <section id="syair">
    <div class="card">
      <h2>Syair Lagu</h2>
      <p>Berisikan syair lagu favoriteku!!!</p>
    </div>
  </section>

  <section id="luas">
    <div class="card">
      <h2>Menghitung Luas Persegi</h2>
      <p>Masukkan panjang sisi:</p>
      <input type="number" id="sisi" placeholder="Sisi">
      <button onclick="hitungLuas()">Hitung</button>
      <p id="hasilLuas"></p>
    </div>
  </section>

  <section id="volume">
    <div class="card">
      <h2>Menghitung Volume Kotak</h2>
      <p>Masukkan panjang, lebar, tinggi:</p>
      <input type="number" id="panjang" placeholder="Panjang">
      <input type="number" id="lebar" placeholder="Lebar">
      <input type="number" id="tinggi" placeholder="Tinggi">
      <button onclick="hitungVolume()">Hitung</button>
      <p id="hasilVolume"></p>
    </div>
  </section>

  <script>
    function showPage(pageId) {
      let pages = document.querySelectorAll("section");
      pages.forEach(p => p.classList.remove("active"));
      document.getElementById(pageId).classList.add("active");
    }

    function hitungLuas() {
      let sisi = document.getElementById("sisi").value;
      let hasil = sisi * sisi;
      document.getElementById("hasilLuas").innerText = "Luas = " + hasil;
    }

    function hitungVolume() {
      let p = document.getElementById("panjang").value;
      let l = document.getElementById("lebar").value;
      let t = document.getElementById("tinggi").value;
      let hasil = p * l * t;
      document.getElementById("hasilVolume").innerText = "Volume = " + hasil;
    }
  </script>

</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tentang Saya</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: #f0f8ff;
      color: #444;
    }

    header {
      background: linear-gradient(135deg, #aee1f9, #d6ecfa);
      color: #2b4c6f;
      text-align: center;
      padding: 40px 20px;
      border-bottom: 4px dotted #90caf9;
    }

    header h1 {
      margin: 0;
      font-size: 2.5em;
    }

    .container {
      max-width: 960px;
      margin: 30px auto;
      background-color: #ffffff;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    }

    .profile-photo {
      width: 180px;
      height: 180px;
      object-fit: cover;
      border-radius: 50%;
      border: 6px dashed #90caf9;
      display: block;
      margin: 0 auto 20px;
      background-color: #fff;
    }

    h2 {
      color: #1976d2;
      border-bottom: 2px dashed #90caf9;
      padding-bottom: 5px;
      margin-top: 40px;
    }

    section {
      margin-bottom: 40px;
    }

    ul {
      padding-left: 25px;
      line-height: 1.8;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      justify-content: center;
    }

    .gallery img {
      width: 200px;
      height: 140px;
      object-fit: cover;
      border-radius: 10px;
      border: 3px solid #90caf9;
      background-color: #e3f2fd;
    }

    footer {
      background: linear-gradient(135deg, #aee1f9, #d6ecfa);
      color: #2b4c6f;
      text-align: center;
      padding: 20px;
      margin-top: 60px;
      border-top: 4px dotted #90caf9;
    }

    /* Elemen lucu */
    .emoji {
      font-size: 1.3em;
      margin-right: 6px;
    }
  </style>
</head>
<body>

  <header>
    <h1>⋆. 𐙚 ˚ Anita Putri Lestari 𝜗𝜚˚⋆ </h1>
  </header>

  <div class="container">

    <!-- FOTO DIRI -->
    <img src="C:\Users\anita\Downloads\anita.jpeg" alt="Foto Diri" class="profile-photo" />

    <!-- PENJELASAN DIRI -->
    <section>
      <h2><span class="emoji">🕊</span> Yukk Kenalan!!</h2>
      <p>Haloo!! Perkenakan Aku <strong>Anita Putri Lestari</strong>, seseorang pelajar di salah satu SMKN 1 Tangerang, aku adalah siswi di jurusan DKV yang sekarang menduduki kelas 12. Aku memiliki semangat penuh yang suka belajar tentang hal-hal yang baru, membuat design kreatif. Menciptakan sesuatu yang bisa membuat orang lain senang dan terinspirasi adalah suatu keinginanku!</p>
    </section>

    <!-- HOBI -->
    <section>
      <h2><span class="emoji">🎨</span> Hobi</h2>
      <ul>
        <li>Menggambar dan desain ilustrasi lucu</li>
        <li>Desain Busana </li>
        <li>Mendengarkan lagu</li>
        <li>Menonton drama</li>
        <li>Bermain Badmintoon</li>
      </ul>
    </section>

    <!-- AKTIVITAS KESUKAAN -->
    <section>
      <h2><span class="emoji">💥</span> Aktivitas Kesukaan</h2>
      <p>Aku aktif di bidang <strong>melukis, Membuat makanan</strong>. Aku juga sering scroll tiktok untuk hiburan maupun untuk menemukan inspirasi, merangkai lego.</p>
    </section>

    <!-- BERBAGAI KEGIATANKU -->
    <section>
      <h2><span class="emoji">🪼</span> Berbagai Kegiatanku</h2>
      <div class="gallery">
        <img src="C:\Users\anita\Downloads\desain.jpeg?text=Desain" alt="Desain" />
        <img src="C:\Users\anita\Downloads\osis.jpeg?text=Workshop" alt="Workshop" />
        <img src="C:\Users\anita\Downloads\bunga.jpeg?text=Ilustrasi" alt="Ilustrasi" />
        <img src="C:\Users\anita\Downloads\melukis.jpeg?text=Organisasi" alt="Organisasi" />
      </div>
    </section>

    <!-- MAKANAN KESUKAAN -->
    <section>
      <h2><span class="emoji">🍬</span> Makanan Favorit</h2>
      <ul>
        <li>Mie ayam🍝</li>
        <li>Ramen🍜</li>
        <li>Soto betawi🥗</li>
        <li>Buah strawberi🍓</li>
        <li>Ice cream🍨</li>
      </ul>
    </section>

    <!-- CITA-CITA -->
    <section>
      <h2><span class="emoji">🌟</span> Cita-Cita</h2>
      <p>Aku ingin menjadi seorang <strong>Designer Busana</strong> yang bisa membuat busana gaun yang cantik untuk acara berharga bagi seseorang serta membahagiakan orang dengan hasil gaun ku yang indah, mempunyai butik terkenal dan menjadi model hasil gaun ku sendiri!</p>
    </section>

  </div>

  <footer>
    &copy; 2025 Anita Putri Lestari - SMKN 1 Tangerang 
  </footer>

</body>
</html>
