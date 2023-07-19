<template>
  <div class="profile">
    <div class="profile-header">
      <h1>{{ username }}</h1>
      <p>{{ bio }}</p>
    </div>
    <div class="donation-stats">
      <div class="stat">
        <p class="stat-label">Total Donasi</p>
        <p class="stat-value">{{ totalDonations }}</p>
      </div>
      <div class="stat">
        <p class="stat-label">Total Pendukung</p>
        <p class="stat-value">{{ totalDonors }}</p>
      </div>
    </div>
    <div class="donation-history">
      <h2>Riwayat Donasi</h2>
      <ul>
        <li v-for="donation in donations" :key="donation.id">
          <p>{{ donation.amount }}</p>
          <p>{{ donation.date }}</p>
        </li>
        <li>
          <p>{{ totalDonations }} (Total donasi hingga {{ getLastDonationDate() }})</p>
        </li>
      </ul>
    </div>
  </div>
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
      username: 'Maria Teresia Elvara',
      bio: 'Passionate about making a difference',
      totalDonations: 9500000,
      totalDonors: 200,
      donations: [
        { id: 1, amount: 'Rp. 500.000', date: '2023-07-15' },
        { id: 2, amount: 'Rp. 3.000.000', date: '2023-07-12' },
        { id: 3, amount: 'Rp. 6.000.000', date: '2023-07-10' },
      ],
    };
  },
  methods: {
    getLastDonationDate() {
      if (this.donations.length > 0) {
        return this.donations[this.donations.length - 1].date;
      }
      return '';
    },
  },
};
</script>

<style>
.profile {
  background-image: linear-gradient(to bottom right, #007bff, #00c5a9);
  color: #fff;
  padding: 20px;
  border-radius: 10px;
}

.profile .profile-header {
  text-align: center;
  margin-bottom: 20px;
}

.profile .profile-picture {
  border-radius: 50%;
  width: 150px;
  height: 150px;
  display: block; /* Set display to block to ensure proper positioning */
  margin: 0 auto 10px; /* Center the image and add margin below it */
}


.profile .donation-stats {
  display: flex;
  justify-content: space-around;
  margin-bottom: 20px;
}

.profile .stat {
  text-align: center;
}

.profile .stat-label {
  font-size: 16px;
}

.profile .stat-value {
  font-size: 24px;
  font-weight: bold;
}

.profile .donation-history {
  text-align: center;
}

.profile .donation-history h2 {
  margin-bottom: 10px;
}

.profile .donation-history ul {
  list-style-type: none;
  padding: 0;
}

.profile .donation-history li {
  margin-bottom: 10px;
}

</style>
