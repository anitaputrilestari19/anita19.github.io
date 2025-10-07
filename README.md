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
  <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Class Schedule A.Y. 2024–2025</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Raleway:wght@400;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --mauve:#9c6b6e;     /* header & cells */
      --mauve-dark:#845459; /* darker stroke */
      --cream:#efe0cd;     /* body cells */
      --paper:#f8f5ef;     /* canvas */
      --grid:#d9d5cf;      /* background grid lines */
      --shadow: 0 18px 35px rgba(0,0,0,.12);
    }

    *{box-sizing:border-box}
    body{
      margin:0;
      min-height:100vh;
      display:grid;
      place-items:center;
      background:
        /* subtle notebook grid */
        linear-gradient(transparent 31px, var(--grid) 32px),
        linear-gradient(90deg, transparent 31px, var(--grid) 32px);
      background-size:32px 32px, 32px 32px;
      background-color:#fffdf9;
      font-family:"Raleway", system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji";
      color:#3f2f30;
      padding:40px 16px;
    }

    .sheet{
      width:min(1100px, 96vw);
      background:var(--paper);
      border-radius:18px;
      box-shadow:var(--shadow);
      position:relative;
      padding:44px 28px 36px;
      overflow:hidden;
    }

    /* decorative masking tape */
    .tape{
      position:absolute; inset:auto auto calc(100% - 46px) calc(-14px);
      width:110px; height:34px; rotate:-15deg;
      background:
        repeating-linear-gradient(45deg, rgba(255,135,154,.75) 0 10px, rgba(255,135,154,.75) 10px 20px),
        radial-gradient(circle at 8px 8px, #ffd7de 0 6px, transparent 7px);
      background-blend-mode:multiply; filter:drop-shadow(0 6px 8px rgba(0,0,0,.12));
      border-radius:6px; opacity:.85;
      mask:linear-gradient(#000, #000) content-box, linear-gradient(#000, #000);
      -webkit-mask-composite: xor; mask-composite: exclude;
      padding:6px;
    }
    .tape.bottom{ inset: auto calc(-14px) -18px auto; rotate:18deg; }

    header{
      text-align:center; margin-bottom:10px; position:relative;
    }
    .title{
      font-family:"Playfair Display", serif; font-weight:900; letter-spacing:.5px;
      font-size: clamp(38px, 6vw, 84px);
      line-height:1; margin:0; color:#b7888b;
      text-shadow: 0 6px 0 rgba(151,106,110,.25), 0 10px 18px rgba(0,0,0,.1);
    }
    .subtitle{ margin:10px 0 14px; font-weight:600; letter-spacing:.28em; text-transform:uppercase; }

    /* cute corner doodles */
    .doodles{ position:absolute; right:26px; top:22px; font-size:0; }
    .heart{ width:30px; height:24px; border:6px solid #f0b; border-top-color:transparent; border-right-color:transparent; border-radius:12px 0 12px 0; display:inline-block; transform:rotate(-45deg); margin:0 4px; opacity:.6; }
    .heart:nth-child(2){ border-color:#7cc4ff; border-top-color:transparent; border-right-color:transparent; }
    .heart:nth-child(3){ border-color:#ffd966; border-top-color:transparent; border-right-color:transparent; }

    .schedule{
      width:100%; border-collapse:separate; border-spacing:0; table-layout:fixed;
      background:transparent; border-radius:14px; overflow:hidden; box-shadow: inset 0 0 0 2px rgba(0,0,0,.06);
    }

    .schedule th, .schedule td{
      border: 2px solid #2d1d1e22;
      padding: 16px 14px; text-align:center;
    }

    .schedule thead th{
      background:var(--mauve);
      color:#f1e8e6; font-weight:700; font-size: clamp(14px, 2vw, 22px);
      font-family:"Playfair Display", serif; letter-spacing:.02em;
    }

    .schedule tbody td{ background: var(--cream); font-weight:600; min-height:48px; }
    .schedule tbody td.time{ background:#b98b8f; color:#fff8f7; font-weight:700; font-family:"Playfair Display", serif; }

    .schedule thead th:first-child,
    .schedule tbody td:first-child{ position:sticky; left:0; z-index:2; }

    .grid-wrap{ overflow:auto; border-radius:14px; box-shadow:inset 0 0 0 3px #00000012; }

    /* Responsive tweaks */
    @media (max-width: 720px){
      .subtitle{ letter-spacing:.18em; font-size:12px; }
      .schedule th, .schedule td{ padding:12px 10px; font-size:12px; }
    }
  </style>
</head>
<body>

  <main class="sheet" aria-labelledby="title">
    <div class="tape"></div>
    <div class="tape bottom"></div>

    <header>
      <h1 id="title" class="title">Jadwal Pelajaran</h1>
      <div class="subtitle">XII DKV 2 2025–2026</div>
      <div class="doodles" aria-hidden="true">
        <span class="heart"></span>
        <span class="heart"></span>
        <span class="heart"></span>
      </div>
    </header>

    <div class="grid-wrap">
      <table class="schedule" role="table" aria-label="Class Schedule">
        <thead>
          <tr>
            <th scope="col">Time</th>
            <th scope="col">Monday</th>
            <th scope="col">Tuesday</th>
            <th scope="col">Wednesday</th>
            <th scope="col">Thursday</th>
            <th scope="col">Friday</th>
          </tr>
        </thead>
        <tbody>
          <!-- Row 1 -->
          <tr>
            <td class="time">07:00–07:40</td>
            <td>Upacara</td><td>PPKN</td><td>Bahasa Inggris</td><td>Kejuruan 3</td><td>Pengajian</td>
          </tr>
          <!-- Row 2 -->
          <tr>
            <td class="time">07:40–08:20</td>
            <td>Kejuruan 1</td><td>PPKN</td><td>Bahasa Inggris</td><td>Kejuruan 3</td><td>PKWH</td>
          </tr>
          <!-- Row 3 -->
          <tr>
            <td class="time">08:20–09:00</td>
            <td>Kejuruan 1</td><td>Kejuruan 2</td><td>Bahasa Inggris</td><td>Kejuruan 3</td><td>PKWH</td>
          </tr>
          <!-- Row 4 -->
          <tr>
            <td class="time">09:00–9:40</td>
            <td>Kejuruan 1</td><td>Kejuruan 2</td><td>Bahasa Inggris</td><td>Bahasa Indonesia</td><td>PKWH</td>
          </tr>
          <!-- Row 5 -->
          <tr>
            <td class="time">9:40–10:00</td>
            <td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td>
          </tr>
          <!-- Row 6 -->
          <tr>
            <td class="time">10:00–10:40</td>
            <td>Kejuruan 1</td><td>Matematika</td><td>Kejuruan 3</td><td>Agama Islam</td><td>Bahasa Indonesia</td>
          </tr>
            <td class="time">10:40–11:20</td>
            <td>Kejuruan 2</td><td>Matematika</td><td>Kejuruan 3</td><td>Agama Islam</td><td>Bahasa Indonesia</td>
          </tr>
            <td class="time">11:20–12:00</td>
            <td>Kejuruan 2</td><td>Matematika</td><td>Kejuruan 3</td><td>Agama Islam</td><td>Istirahat</td>
          </tr>
            <td class="time">12:00–12:45</td>
            <td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td><td>Istirahat</td>
          </tr>
            <td class="time">12:45–13:25</td>
            <td>Kejuruan 2</td><td>Mapel Pilihan DKV</td><td>Kejuruan 1</td><td>Kejuruan 1</td><td>Sholat Jum'at</td>
          </tr>
            <td class="time">13:25–14:05</td>
            <td>Kejuruan 2</td><td>Mapel Pilihan DKV</td><td>Kejuruan 1</td><td>Kejuruan 1</td><td>Jum'at Bersih</td>
          </tr>
            <td class="time">14:05–14:45</td>
            <td>Kejuruan 2</td><td>Mapel Pilihan DKV</td><td>PKWH</td><td>Bahasa Korea</td><td>Ekstrakurikuler</td>
          </tr>
            <td class="time">14:45–15:25</td>
            <td>Kejuruan 1</td><td>Mapel Pilihan DKV</td><td>PKWH</td><td>Bahasa Korea</td><td>Ekstrakurikuler</td>
          </tr>

        </tbody>
      </table>
    </div>
  </main>
</body>
</html>
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Pilihanku - Maliq & D'Essentials (Lirik & Chord)</title>
  <style>
    body { font-family: Arial, sans-serif; background:#fafafa; padding:20px; }
    .song { max-width:800px; margin:auto; background:#e4f2f8; padding:20px; border-radius:12px; box-shadow:5 2px 8px rgba(0,0,0,0.1); }
    h1 { font-size:22px; margin-top:0; }
    pre { white-space:pre-wrap; font-size:16px; line-height:1.8; }
    .chord { font-weight:bold; color:#2a5; }
  </style>
</head>
<body>
  <div class="song">
    <h1>Pilihanku - Maliq &amp; D'Essentials</h1>
    <pre>
<span class="chord">C</span>                     <span class="chord">G</span>
Maukah kau tuk menjadi pilihanku
<span class="chord">Am</span>                    <span class="chord">F</span>
Menjadi yang terakhir dalam hidupku
<span class="chord">C</span>                        <span class="chord">G</span>
Maukah kau tuk menjadi yang pertama
<span class="chord">Am</span>                          <span class="chord">F</span>
Yang slalu ada di saat pagi ku membuka mata

<span class="chord">F</span>           <span class="chord">G</span> 
Jadilah yang terakhir
<span class="chord">C</span>         <span class="chord">Am</span>
Tuk jadi yang pertama
<span class="chord">F</span>          <span class="chord">G</span> 
Tuk jadi selamanya...

<span class="chord">C</span>                     <span class="chord">G</span>
Maukah kau tuk menjadi pilihanku
<span class="chord">Am</span>                    <span class="chord">F</span>
Menjadi yang terakhir dalam hidupku
<span class="chord">C</span>                        <span class="chord">G</span>
Maukah kau tuk menjadi yang pertama
<span class="chord">Am</span>                          <span class="chord">F</span>
Yang selalu ada di saat pagi ku

<span class="chord">C</span>                     <span class="chord">G</span>
Maukah kau tuk menjadi pilihanku
<span class="chord">Am</span>                    <span class="chord">F</span>
Menjadi yang terakhir dalam hidupku
<span class="chord">C</span>                        <span class="chord">G</span>
Maukah kau tuk menjadi yang pertama
<span class="chord">Am</span>                          <span class="chord">F</span>
Yang selalu ada di saat pagi ku membuka mata

<span class="chord">F</span>           <span class="chord">G</span> 
Jadilah yang terakhir
<span class="chord">C</span>         <span class="chord">Am</span>
Tuk jadi yang pertama
<span class="chord">F</span>          <span class="chord">G</span> 
Tuk jadi selamanya....
    </pre>
  </div>
</body>
</html>


  <footer>
    &copy; 2025 Anita Putri Lestari - SMKN 1 Tangerang 
  </footer>

</body>
</html>
