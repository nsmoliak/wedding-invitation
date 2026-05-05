<template>
  <section class="dress-code">
    <div class="dress-code-inside">
      <h2 class="title-text dress-code-title" data-aos="fade-down" data-aos-once="true">Дресс-код</h2>

      <p class="descr-text dress-code-descr" data-aos="fade-right" data-aos-once="true">
        Мы очень старались сделать праздник красивым и будем рады, если в своих нарядах вы поддержите цветовую гамму
        нашей свадьбы:
      </p>

      <div class="dress-code-colors" data-aos="fade-left" data-aos-once="true">
        <div
          v-for="color in palette"
          :key="color.hex"
          class="dress-code-swatch"
          :style="{ background: color.hex }"
        ></div>
      </div>

      <p class="dress-code-hint" data-aos="fade-right" data-aos-once="true">Соблюдение дресс-кода желательно, но не обязательно.</p>
    </div>
  </section>
</template>

<script setup>
const palette = [
  {hex: '#E7D2CC'},
  {hex: '#A9BCC3'},
  {hex: '#B2B9A1'},
  {hex: '#BDB2BD'},
  {hex: '#DECDC3'},
  {hex: '#D4BDB5'},
  {hex: '#8E6D67'},
  {hex: '#060503'},
]
</script>

<style scoped>
.dress-code {
  position: relative;
  z-index: 2;
  background: var(--bg);
  margin-top: -2px;
}

.dress-code-inside {
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

.dress-code-title {
  color: var(--accent);
}

.dress-code-descr {
  color: var(--text);
}

.dress-code-colors {
  display: flex;
  justify-content: center;
  gap: 10px;
  padding-top: 30px;
}

.dress-code-swatch {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.dress-code-hint {
  font-size: 80%;
  color: var(--text);
  opacity: 0.7;
  padding-bottom: 10px;
}


@media (max-width: 600px) {
  .dress-code-swatch {
    width: 30px;
    height: 30px;
  }
}
</style>
