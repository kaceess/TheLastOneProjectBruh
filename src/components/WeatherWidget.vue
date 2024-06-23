<template>
  <div class="weather-widget">
    <h2 class="widget-title">🍃☁️𝓦𝓮𝓪𝓽𝓱𝓮𝓻 𝓦𝓲𝓭𝓰𝓮𝓽☁️🍃</h2>
    <div class="search-bar">
      <input v-model="city" class="input-city" placeholder="Masukkan Nama Kota" @keyup.enter="getWeather" />
      <button @click="getWeather" class="btn-search">Search</button>
    </div>
    <div v-if="weather" class="weather-info">
      <p><strong class="info-label">Location:</strong> {{ weather.name }}</p>
      <p><strong class="info-label">Temperature:</strong> {{ weather.main.temp }}°C</p>
      <p><strong class="info-label">Weather:</strong> {{ weather.weather[0].description }}</p>
    </div>
    <div v-else>
      <p class="placeholder-text">Masukkan Nama Kota Untuk Melihat Cuaca</p>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

const city = ref('')
const weather = ref(null)

const getWeather = async () => {
  const apiKey = '23f0987b01236b80c30ceeb06f7c8c22'
  const url = `https://api.openweathermap.org/data/2.5/weather?q=${city.value}&units=metric&appid=${apiKey}`

  try {
    const response = await axios.get(url)
    weather.value = response.data
  } catch (error) {
    console.error(error)
    weather.value = null
  }
}

onMounted(() => {
  getWeather()
})
</script>

<style scoped>
.weather-widget {
  max-width: 400px; /* Ukuran maksimum widget */
  margin: auto; /* Menengahkan widget di layar */
  margin-top: 5rem;
  background-color: #ffe4e1; /* Warna pink untuk latar belakang */
  border: 2px solid #d6336c; /* Border pink di sekeliling widget */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  text-align: center;
  color: #d6336c;
  font-family: Arial, sans-serif; /* Menggunakan font Arial untuk semua teks */
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 20px; /* Padding tambahan di dalam widget */
  border-radius: 8px; /* Border radius untuk sudut */
}

.widget-title {
  color: #d6336c;
  margin-bottom: 20px;
  font-size: 24px; /* Ukuran font judul */
}

.search-bar {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.input-city {
  padding: 10px;
  border: 2px solid #d6336c;
  border-radius: 4px 0 0 4px;
  outline: none;
  width: 200px;
  color: #d6336c;
}

.btn-search {
  padding: 10px 20px;
  border: none;
  background-color: #d6336c;
  color: white;
  border-radius: 0 4px 4px 0;
  cursor: pointer;
}

.btn-search:hover {
  background-color: #e94e77;
}

.weather-info {
  background-color: #ffb6c1;
  padding: 15px;
  border-radius: 8px;
  color: #d6336c;
}

.weather-info p {
  margin: 5px 0;
}

.info-label {
  color: #d6336c;
  font-size: 14px; /* Ukuran font label di sini disesuaikan */
}

.placeholder-text {
  color: #d6336c;
  font-family: Arial, serif; /* Menggunakan font Arial serif */
}

</style>
