<template>
  <div class="container">
    <header>
      <div class="logo">Buka Donasi</div>
      <nav>
        <ul>
          <li><a href="#">Tentang Kami</a></li>
          <li><a href="#">Kontak</a></li>
        </ul>
      </nav>
    </header>
  
    <main>
      <section class="hero">
        <div class="hero-content">
          <h1>Donasi untuk Masa Depan Lebih Baik</h1>
          <p>Bergabunglah dengan kami dalam upaya membantu mereka yang membutuhkan.</p>
          <a href="#" class="donate-button">Donasi Sekarang</a>
        </div>
      </section>
      <section class="donation-info">
        <h2>Apa yang Kami Lakukan?</h2>
        <p class="penjelasan">
          Buka Donasi adalah organisasi nirlaba yang berfokus pada membantu masyarakat yang membutuhkan,
          seperti anak-anak penderita kelaparan, keluarga yang kurang mampu, dan orang-orang yang terkena bencana alam.
          Kami berkomitmen untuk mengumpulkan dan mendistribusikan donasi dengan efisien dan transparan.
        </p>
      </section>

      <section class="how-to-donate">
        <h2>Cara Berdonasi</h2>
        <ol>
          <li>Pilih jenis donasi yang ingin Anda berikan.</li>
          <li>Kunjungi halaman donasi kami dan pilih jumlah yang Anda ingin berikan.</li>
          <li>Isi informasi yang diperlukan dan pilih metode pembayaran.</li>
          <li>Verifikasi dan selesaikan proses donasi.</li>
        </ol>
      </section>
    </main>

    <footer>
      <p>&copy; 2023 Buka Donasi. All rights reserved.</p>
    </footer>
  </div>
</template>

<style>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-image: linear-gradient(to right, #007bff, #00c5a9);
  color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

nav ul {
  list-style: none;
  display: flex;
}

nav li {
  margin-left: 20px;
}

nav li a {
  color: #fff;
  text-decoration: none;
  font-size: 16px;
  transition: color 0.3s ease;
}

nav li a:hover {
  color: #f2f2f2;
}
.hero {
  position: relative;
  background-image: url('../images/hero1.jpg');

  /* background-color: #007bff; */
  background-size: cover;
  background-position: center;
  color: #fff;
  text-align: center;
  padding: 120px 0;
  overflow: hidden;
}

.hero:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.6);
}

.hero-content {
  max-width: 600px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.hero h1 {
  font-size: 35px;
  font-weight: bold;
  margin-bottom: 20px;
  color: #fff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.hero p {
  font-size: 15px;
  line-height: 1.6;
  color: #fff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.donate-button {
  display: inline-block;
  padding: 15px 30px;
  background-image: linear-gradient(to right, #007bff, #00c5a9);
  color: #fff;
  text-decoration: none;
  font-size: 18px;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

.donate-button:hover {
  background-color: #007bff;
}
/* Additional styles for the donation-info section */
.donation-info {
  text-align: center;
  padding: 60px 0;
}

.donation-info h2 {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 30px;
}

.donation-info p {
  font-size: 18px;
  line-height: 1.6;
}

/* Additional styles for the how-to-donate section */
.how-to-donate {
  text-align: center;
  background-color: #f2f2f2;
  padding: 60px 0;
}

.how-to-donate h2 {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 30px;
}

.how-to-donate ol {
  font-size: 18px;
  line-height: 1.6;
  text-align: left;
}

/* Additional styles for the footer */
footer {
  text-align: center;
  background-color: #333;
  color: #fff;
  padding: 20px;
}

footer p {
  margin: 0;
}
.penjelasan {
  padding: 40px;
  background-color: #f9f9f9; /* Light gray background */
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle box shadow */
  margin: 100px;
}

.penjelasan h2 {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 20px;
  color: #333; /* Dark text color */
}

.penjelasan p {
  font-size: 16px;
  line-height: 1.6;
  color: #555; /* Slightly darker text color */
}


</style>
