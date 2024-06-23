<template>
    <div class="iframe-container">
      <iframe src="https://cv-shibal.vercel.app/" frameborder="0" width="500%" height="1000px"></iframe>
    </div>
  </template>
  
  <style scoped>
  .iframe-container {
    width: 100%;
    display: flex;
    justify-content: center;
    overflow-x: hidden; /* Menyembunyikan scrollbar horizontal */
  }
  
  iframe {
    max-width: 100%;
    width: 1000px; /* Atur lebar sesuai kebutuhan, atau biarkan 1000px */
    height: 1000px; /* Sesuaikan tinggi jika diperlukan */
  }
  </style>
  