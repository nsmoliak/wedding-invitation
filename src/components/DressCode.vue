<template>
  <section class="dresscode">
    <div class="dresscode-inside">
      <h2 class="title-text dresscode-title">Дресс-код</h2>

      <p class="descr-text dresscode-descr">
        Мы очень старались сделать праздник красивым и будем рады, если в своих нарядах вы поддержите цветовую гамму нашей свадьбы:
      </p>

      <!-- Palette swatches -->
      <div class="dresscode-colors">
        <div
          v-for="color in palette"
          :key="color.hex"
          class="dresscode-swatch"
          :style="{ background: color.hex }"
          :title="color.name"
        ></div>
      </div>

      <p class="dresscode-hint">Соблюдение дресс-кода желательно, но не обязательно.</p>

      <!-- Dress code image -->
      <div class="dresscode-img-wrap">
        <img src="/dresscode.png" alt="Дресс-код" class="dresscode-img" />
      </div>

      <div class="dresscode-cards">
        <div class="dresscode-card">
          <h3 class="dresscode-card-title text-dark">Девушки</h3>
          <p class="dresscode-card-text">
            Для нас главное — ваше присутствие. Но нам будет очень приятно, если вы учтёте наши пожелания при выборе нарядов. Коктейльные и вечерние платья в пастельных тонах. Просим избегать белого цвета.
          </p>
        </div>
        <div class="dresscode-card">
          <h3 class="dresscode-card-title text-dark">Мужчины</h3>
          <p class="dresscode-card-text">
            Для нас главное — ваше присутствие. Но нам будет очень приятно, если вы учтёте наши пожелания при выборе нарядов. Классический костюм или смокинг приветствуется.
          </p>
        </div>
      </div>

      <!-- Details block -->
<!--      <div class="dresscode-details">-->
<!--        <p class="descr-text dresscode-details-text">-->
<!--          <strong class="text-dark">Детали:</strong> Обратите внимание, что формат мероприятия не предполагает детской площадки и аниматоров. Пожалуйста, позаботьтесь о том, чтобы провести этот вечер без детей. Ваши подарки в конвертах помогут осуществить наши мечты.-->
<!--        </p>-->
<!--      </div>-->
    </div>
  </section>
</template>

<script setup>
const palette = [
  { hex: '#c8b8a2', name: 'Бежевый' },
  { hex: '#d4a5a5', name: 'Пыльная роза' },
  { hex: '#921A21', name: 'Бургундский' },
  { hex: '#8a9e8d', name: 'Шалфей' },
  { hex: '#e8e0d0', name: 'Кремовый' },
  { hex: '#b0a090', name: 'Тауп' },
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
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
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
