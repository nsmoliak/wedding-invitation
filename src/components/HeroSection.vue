<template>
  <section class="header" id="home">
    <div class="header-blocks">
      <div class="header-block text-dark" data-aos="fade-down" >Наконец-то!</div>
      <div class="header-block" data-aos="zoom-in" data-aos-once="true">
        <p class="header-sub"> так сказали наши близкие и родные, когда узнали, эту</p>
        <p class="header-big text-dark">новость</p>
      </div>
      <div class="header-block-img" data-aos="fade-up" data-aos-delay="200">
        <img src="/arrow.svg" alt=""/>
      </div>
    </div>

    <div class="header-block-small-heart" id="music-block" data-aos="zoom-in" data-aos-once="true">
      <audio id="backgroundAudio" loop preload="auto" ref="audio">
        <source src="/song.mp3" type="audio/mpeg">
      </audio>
      <img v-if="playing" src="/music-on.png" alt=""  @click="toggleMusic"/>
      <img v-else src="/music-off.png" alt=""  @click="toggleMusic"/>
       <p id="music-text" class="header-text-small">{{ playing ? 'Выключить музыку' : 'Включить музыку' }}</p>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const audio = ref(null)
const playing = ref(false)

function toggleMusic() {
  if (playing.value) {
    audio.value.pause()
    playing.value = false
  } else {
    audio.value.play()
    playing.value = true
  }
}
</script>

<style scoped>
.header {
  min-height: 100vh;
  background-color: var(--bg);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.header-blocks {
  flex: 1;
  min-height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 50px 5%;
  gap: 70px;
  text-align: center;
}

.header-block {
  font-family: var(--font-main), sans-serif;
  font-size: 20px;
  max-width: 300px;
}

.header-block.text-dark {
  font-size: 62px;
  font-family: var(--font-beauty), sans-serif;
  color: var(--accent);
}

.header-sub {
  font-size: 20px;
  color: var(--text);
}

.header-big {
  font-size: 20px;
  text-transform: uppercase;
  padding-top: 20px;
  font-family: var(--font-main), sans-serif;
  color: var(--accent);
}

.header-block-img {
  width: 15%;
  max-width: 60px;
  margin: 0 auto;
}

.header-block-img img {
  width: 100%;
  display: block;
  height: auto;
}

.header-block-small-heart {
  text-align: center;
  font-size: 78.8px;
}

.header-block-small-heart img {
  width: 14%;
  height: auto;
  cursor: pointer;
  transition: opacity 0.2s;
}

.header-block-small-heart img:hover {
  opacity: 0.7;
}

.header-text-small {
  font-family: var(--font-main),sans-serif;
  font-size: 24px;
  line-height: 120%;
  color: var(--text);
  cursor: pointer;
}


@media (max-width: 800px) {
  .header-text-small {
    font-size: 20px;
  }
}

</style>
