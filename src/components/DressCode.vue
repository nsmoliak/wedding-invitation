<template>
  <section class="dresscode">
    <div class="dresscode-inside">
      <h2 class="title-text dresscode-title">Дресс-код</h2>

      <p class="descr-text dresscode-descr">
        Мы очень старались сделать праздник красивым и будем рады, если в своих нарядах вы поддержите цветовую гамму
        нашей свадьбы:
      </p>

      <!-- Palette swatches -->
      <div class="dresscode-colors">
        <div
          v-for="color in palette"
          :key="color.hex"
          class="dresscode-swatch"
          :style="{ background: color.hex }"
        ></div>
      </div>

      <p class="dresscode-hint">Соблюдение дресс-кода желательно, но не обязательно.</p>

    </div>
  </section>
</template>

<script setup>
const palette = [
  {hex: '#F0C8C8'},
  {hex: '#C7D5EF'},
  {hex: '#ADBEA4'},
  {hex: '#c8b8b0'},
  {hex: '#5B4633'},
  {hex: '#060503'},
]
</script>

<style scoped>
.dresscode {
  position: relative;
  z-index: 2;
  background: var(--bg);
  margin-top: -2px;
}

.dresscode-inside {
  width: 90%;
  max-width: 800px;
  margin: auto;
  padding: 70px 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  text-align: center;
}

.dresscode-title {
  color: var(--accent);
}

.dresscode-descr {
  color: var(--text);
}

.dresscode-colors {
  display: flex;
  justify-content: center;
  gap: 10px;
  padding-top: 30px;
}

.dresscode-swatch {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.dresscode-hint {
  font-size: 80%;
  color: var(--text);
  opacity: 0.7;
  padding-bottom: 10px;
}

.dresscode-img-wrap {
  width: 80%;
  max-width: 300px;
  margin: 10px auto;
}

.dresscode-img {
  width: 100%;
  border-radius: 4px;
}

.dresscode-cards {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  width: 100%;
  margin-top: 10px;
}

.dresscode-card {
  display: flex;
  flex-direction: column;
  gap: 12px;
  padding: 20px;
  text-align: left;
}

.dresscode-card-title {
  font-family: var(--font-beauty);
  font-size: 36px;
  font-weight: 400;
  color: var(--accent);
}

.dresscode-card-text {
  font-size: 80%;
  color: var(--text);
  line-height: 1.5;
}

.dresscode-details {
  width: 100%;
  margin-top: 20px;
  padding: 30px;
  border: 1px solid rgba(146, 26, 33, 0.2);
  border-radius: 4px;
}

.dresscode-details-text {
  font-size: 80%;
  text-align: left;
  line-height: 1.6;
}

@media (max-width: 500px) {
  .dresscode-cards {
    grid-template-columns: 1fr;
  }
}
</style>
