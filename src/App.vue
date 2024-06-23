<template>
  <div class="app-container">
    <div class="dropdown-container">
      <q-btn-dropdown
        label="List Tugas Eca Kiyowo"
        class="dropdown-button"
        menu-anchor="top right"
        offset="[0, 5]"
      >
        <q-list class="nav-list">
          <q-item clickable v-close-popup>
            <router-link to="/">
              <q-item-section>
                <q-item-label>Weather</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>

          <q-item clickable v-close-popup>
            <router-link to="/tugas1">
              <q-item-section>
                <q-item-label>Tugas 1</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>

          <q-item clickable v-close-popup>
            <router-link to="/tugas2">
              <q-item-section>
                <q-item-label>Tugas 2</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>

          <q-item clickable v-close-popup>
            <router-link to="/tugas3">
              <q-item-section>
                <q-item-label>Tugas 3</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>

          <q-item clickable v-close-popup>
            <router-link to="/tugas4">
              <q-item-section>
                <q-item-label>Tugas 4</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>

          <q-item clickable v-close-popup>
            <router-link to="/tugas5">
              <q-item-section>
                <q-item-label>Tugas 5</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>

          <q-item clickable v-close-popup>
            <router-link to="/tugas6">
              <q-item-section>
                <q-item-label>Tugas 6</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>

          <q-item clickable v-close-popup>
            <router-link to="/tugas7">
              <q-item-section>
                <q-item-label>Tugas 7</q-item-label>
              </q-item-section>
            </router-link>
          </q-item>
        </q-list>
      </q-btn-dropdown>
    </div>

    <router-view></router-view>
  </div>
</template>

<script>
export default {
  setup() {}
};
</script>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 16px;
  background-color: #ffe4e1; /* Warna pink untuk latar belakang */
  min-height: 100vh; /* Memastikan halaman selalu penuh tinggi */
}

.dropdown-container {
  position: absolute;
  top: 10px;
  right: 10px;
}

.dropdown-button {
  background-color: #d6336c;
  color: white;
}

.q-btn-dropdown .q-list {
  background-color: #ffb6c1;
  color: #d6336c;
}

.q-item-label {
  color: #d6336c;
}

.q-item:hover {
  background-color: #ffe4e1;
}

.router-link-active .q-item-label {
  font-weight: bold;
}

.q-item-section {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
