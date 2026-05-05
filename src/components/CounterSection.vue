<template>
  <section class="counter" id="counter">
    <div class="counter-inside">
      <p class="timer-title title-text" data-aos="fade-up" data-aos-once="true" data-aos-delay="200">Увидимся через:</p>

      <div id="clockdiv" class="timer-blocks" data-aos="fade-up" data-aos-once="true" data-aos-delay="200">
        <div class="timer-block-info">
          <div class="timer-block-inside">
            <div class="timer-number">
              <span>{{ time.days }}</span>
            </div>
            <div class="timer-text">{{ declension(time.days, ['день', 'дня', 'дней']) }}</div>
          </div>
        </div>
        <div class="timer-block-info">
          <div class="timer-block-inside">
            <div class="timer-number">
              <span>{{ time.hours }}</span>
            </div>
            <div class="timer-text">{{ declension(time.hours, ['час', 'часа', 'часов']) }}</div>
          </div>
        </div>
        <div class="timer-block-info">
          <div class="timer-block-inside">
            <div class="timer-number">
              <span>{{ time.minutes }}</span>
            </div>
            <div class="timer-text">{{ declension(time.minutes, ['минута', 'минуты', 'минут']) }}</div>
          </div>
        </div>
        <div class="timer-block-info">
          <div class="timer-block-inside">
            <div class="timer-number">
              <span>{{ time.seconds }}</span>
            </div>
            <div class="timer-text">{{ declension(time.seconds, ['секунда', 'секунды', 'секунд']) }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const weddingDate = new Date('2026-08-29T14:00:00')

const time = ref({ days: 0, hours: 0, minutes: 0, seconds: 0 })

function update() {
  const now = new Date()
  const diff = weddingDate - now
  if (diff <= 0) {
    time.value = { days: 0, hours: 0, minutes: 0, seconds: 0 }
    return
  }
  const totalSeconds = Math.floor(diff / 1000)
  time.value = {
    days: Math.floor(totalSeconds / 86400),
    hours: Math.floor((totalSeconds % 86400) / 3600),
    minutes: Math.floor((totalSeconds % 3600) / 60),
    seconds: totalSeconds % 60,
  }
}

function declension(n, forms) {
  const abs = Math.abs(n) % 100
  const mod = abs % 10
  if (abs > 10 && abs < 20) return forms[2]
  if (mod > 1 && mod < 5) return forms[1]
  if (mod === 1) return forms[0]
  return forms[2]
}

let timer
onMounted(() => {
  update()
  timer = setInterval(update, 1000)
})
onUnmounted(() => clearInterval(timer))
</script>

<style scoped>
.counter {
  background: var(--bg);
  position: relative;
  z-index: 2;
  display: block;
}

.counter-inside {
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

.timer-title {
  font-family: var(--font-main);
  font-size: 28px;
  text-transform: uppercase;
  padding-bottom: 20px;
  color: var(--accent);
}

.timer-blocks {
  display: flex;
  width: 90%;
  margin: auto;
  align-items: center;
  justify-content: center;
  gap: 5px;
}

.timer-block-info {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.timer-block-inside {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}

.timer-number {
  height: 90px;
  width: 90px;
  background: var(--accent);
  border-radius: 50%;
  border: 20px solid #b7585d;
  display: flex;
  align-items: center;
  justify-content: center;
}

.timer-number span {
  line-height: 50px;
  color: var(--bg);
  font-size: 20px;
  font-family: var(--font-main);
}

.timer-text {
  font-size: 14px;
  color: var(--text);
}

@media (max-width: 500px) {
  .timer-number {
    height: 70px;
    width: 70px;
    border-width: 14px;
  }
  .timer-number span {
    font-size: 16px;
  }
}
</style>
