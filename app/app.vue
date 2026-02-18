<template>
  <div :class="['container', darkMode ? 'dark' : 'light']">
    <div class="card">

      <!-- BOTÓN MODO -->
      <button class="toggle-btn" @click="toggleMode">
        {{ darkMode ? "🌙 Modo Noche" : "☀️ Modo Día" }}
      </button>

      <!-- IMAGEN -->
      <img src="/cass.jpg" class="cat" alt="Foto" />

      <h1>ING. ROWEENA ISADORA<br />SÁNCHEZ FLORES</h1>
      <h2>Ingeniería en Tecnologías de la Información y Comunicaciones</h2>

      <div class="divider"></div>

      <div class="skills">
        💡 <strong>Habilidades:</strong><br />
        Manualidades y creación de páginas web
      </div>

      <p class="info">📞 <strong>Teléfono:</strong> 5526747793</p>
      <p class="info">📧 <strong>Correo:</strong><br />ISAWOODSPINES@GMAIL.COM</p>
      <p class="info">
        💗 <strong>Gustos:</strong><br />
        AMO CAIFANES Y A ELVIS PRESLEY Y A LOS GATITOS ESPONJOSOS
      </p>

      <div class="divider"></div>

      <p class="footer">Ciudad de México, México 💜✨</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const darkMode = ref(false);

function toggleMode() {
  darkMode.value = !darkMode.value;
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: background 0.5s ease;
}

/* MODO DÍA */
.light {
  background: linear-gradient(135deg, #f3e8ff, #d8b4fe);
}

/* MODO NOCHE */
.dark {
  background: linear-gradient(135deg, #1e1b4b, #312e81);
}

.card {
  width: 350px;
  padding: 30px;
  border-radius: 20px;
  text-align: center;
  background: white;
  transition: all 0.4s ease;
}

.dark .card {
  background: #1f2937;
  color: white;
}

.cat {
  width: 150px;
  border-radius: 50%;
  margin-bottom: 15px;
  border: 4px solid #a855f7;
}

.divider {
  height: 2px;
  background: #c084fc;
  margin: 20px 0;
}

.toggle-btn {
  margin-bottom: 20px;
  padding: 10px 20px;
  border: none;
  border-radius: 20px;
  background: #a855f7;
  color: white;
  cursor: pointer;
  font-weight: bold;
  transition: all 0.3s ease;
}

.toggle-btn:hover {
  background: #9333ea;
  transform: scale(1.05);
}

.footer {
  margin-top: 15px;
  font-size: 14px;
}
</style>
