<template>
  <div class="donation-form">
    <h2>Donasi Sekarang</h2>
    <form @submit.prevent="submitForm">
      <div>
        <label for="donation-type">Pilih Jenis Donasi:</label>
        <select id="donation-type" v-model="formData.donationType" required>
          <option value="" disabled>-- Pilih Jenis Donasi --</option>
          <option value="donation1">Donasi 1</option>
          <option value="donation2">Donasi 2</option>
          <!-- Tambahkan jenis donasi lainnya di sini jika diperlukan -->
        </select>
      </div>
      <div>
        <label for="name">Nama:</label>
        <input type="text" id="name" v-model="formData.name" required />
      </div>
      <div>
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="formData.email" required />
      </div>
      <div>
        <label for="amount">Jumlah Donasi:</label>
        <input
          type="number"
          id="amount"
          v-model="formData.amount"
          required
          min="1"
        />
      </div>
      <div>
        <label for="verification">Verifikasi:</label>
        <input
          type="text"
          id="verification"
          v-model="formData.verification"
          required
        />
      </div>
      <div>
        <button type="submit">Donasi Sekarang</button>
      </div>
    </form>
  </div>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <footer>
      <p>&copy; 2023 Buka Donasi. All rights reserved.</p>
    </footer>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        donationType: "", // Menambahkan properti untuk jenis donasi
        name: "",
        email: "",
        amount: 0,
        verification: "", // Menambahkan properti untuk verifikasi
      },
    };
  },
  methods: {
    submitForm() {
      // Di sini Anda dapat menambahkan logika untuk mengirim data donasi ke server
      console.log(this.formData);
      alert("Terima kasih atas donasi Anda!");
      this.formData.donationType = "";
      this.formData.name = "";
      this.formData.email = "";
      this.formData.amount = 0;
      this.formData.verification = "";
    },
  },
};
</script>

<style>
.donation-form {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
  border-radius: 15px; /* Membuat container lebih bulat */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Menambahkan efek bayangan */
  background-color: rgba(242, 242, 242, 0.8); /* Menambahkan transparansi pada latar belakang */
}

.donation-form h2 {
  text-align: center;
  margin-bottom: 20px; /* Memberikan sedikit ruang antara judul dan form */
}

.donation-form form div {
  margin-bottom: 15px; /* Memberikan sedikit ruang antara elemen form */
}

.donation-form label {
  display: block;
}

.donation-form input[type="text"],
.donation-form input[type="email"],
.donation-form input[type="number"],
.donation-form select {
  width: 80%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

/* Style untuk select dropdown */
.donation-form select {
  background: linear-gradient(to right, #007bff, #00c5a9);
  color: white;
}

/* Style untuk tombol submit */
.donation-form button {
  background: linear-gradient(to right, #007bff, #00c5a9);
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s;
}

.donation-form button:hover {
  background: linear-gradient(to right, #2196f3, #4fc3f7);
}
footer {
  text-align: center;
  background-color: #333;
  color: #fff;
  padding: 20px;
}

footer p {
  margin: 0;
}
</style>
