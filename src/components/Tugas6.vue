<template>
    <div class="iframe-container">
      <iframe src="https://tugas6p-pbk.vercel.app/" frameborder="0" width="100%" height="675px"></iframe>
    </div>
  </template>
  
  <style scoped>
  .iframe-container {
    width: 100%;
    display: flex;
    justify-content: center; /* Memposisikan konten ke tengah secara horizontal */
    align-items: center; /* Memposisikan konten ke tengah secara vertikal */
    overflow: hidden; /* Menghilangkan kemungkinan scrollbar */
    height: 100vh; /* Tinggi div sesuai tinggi layar (viewport) */
    background-color: #ffe4e1; /* Warna pink untuk latar belakang */
  }
  
  iframe {
    max-width: 100%; /* Lebar iframe 100% dari container */
    width: 1000px; /* Maksimum lebar iframe, bisa disesuaikan */
    height: 675px; /* Tinggi iframe sesuai yang diinginkan */
    border: none; /* Menghilangkan border iframe */
  }
  </style>
  