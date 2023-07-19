<template>
  <nav>
    <router-link to="/">Beranda</router-link> |
    <router-link to="/about">Donasi</router-link> |
    <router-link to="/profil">Profil</router-link>
  </nav>
  <router-view/>
  
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #598ddb;
}

body {
    background-color: #ffffff; /* Kode warna untuk biru muda */
  }
</style>
