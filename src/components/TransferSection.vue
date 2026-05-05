<template>
  <!-- Dark invitation block -->


  <!-- Light transfert block -->
  <section class="transfert" id="transfert">
    <div class="transfert-inside">
      <div class="transfert-item">
        <h2 class="transfert-title title-text">Трансфер</h2>
        <p class="descr-text">Для вашего удобства будет организован трансфер</p>
        <p class="descr-text">ул. Горновых 17, г. Гродно </p>
        <p class="transfert-time text-dark">15:30</p>
        <a class="rsvp-btn" href="https://yandex.com/maps/-/CPvSq0jb" target="_blank" rel="noopener">Маршрут</a>
      </div>
<!--      <div class="transfert-item">-->
<!--        <h2 class="transfert-title title-text">Ждем вас</h2>-->
<!--        <p class="descr-text">Банкетный Зал "Event Hall Olshevski"</p>-->
<!--        <p class="descr-text">Старая Весь 19А, д. Василевичи</p>-->
<!--        <p class="transfert-time text-dark">16:00</p>-->
<!--        <a class="rsvp-btn" href="https://yandex.com/maps/-/CPvSqT2m" target="_blank" rel="noopener">Маршрут</a>-->
<!--      </div>-->

<!--      <div class="foto-bottom" data-aos="zoom-in" data-aos-once="true">-->
<!--        <img src="/foto.png" loading="lazy" alt=""/>-->
<!--      </div>-->

    </div>
  </section>
</template>

<style scoped>
.transfert {
  position: relative;
  z-index: 0;
  margin-top: 30px;
}

.info-invitation {
  display: flex;
  gap: 30px;
  flex-direction: column;
  align-items: center;
}

.welcome-title {
  font-size: 64px;
  line-height: 1;
  color: var(--bg);
}

.welcome-date {
  font-size: 72px;
  line-height: 1;
  padding-top: 20px;
  color: var(--bg);
}

.img-bottom {
  max-width: 18%;
  margin: 0 auto;
  padding-top: 50px;

  img {
    display: block;
    height: auto;
  }
}

.foto-bottom {
  max-width: 22%;
  margin: 0 auto;
  padding-top: 20px;

  img {
    display: block;
    height: auto;
  }
}

.transfert {
  position: relative;
  z-index: 2;
  background: var(--bg);
  margin-top: -4px;
}

.transfert-inside {
  width: 90%;
  max-width: 800px;
  margin: auto;
  padding: 30px 5%;
}

.transfert-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 8px;
  padding: 30px 0;
}

.transfert-item--two {
  padding-top: 50px;
}

.transfert-title {
  font-size: 42px;
  line-height: 0.8;
  padding-bottom: 15px;
  color: var(--accent);
}

.separator-img {
  width: 30px;
  padding: 20px 0;
  margin: 0 auto;
}

.transfert-time {
  color: var(--accent);
  font-size: 120%;
  padding-top: 15px;
}

.rsvp-btn {
  display: inline-block;
  margin-top: 20px;
  background: none;
  text-transform: uppercase;
  font-size: 18px;
  font-family: var(--font-main);
  padding: 15px 20px 10px;
  min-width: 200px;
  border: 1px dashed var(--accent);
  color: var(--accent);
  border-radius: 20px;
  line-height: 1;
  cursor: pointer;
  transition: opacity 0.2s;
}

.rsvp-btn:hover {
  opacity: 0.7;
}

@media (max-width: 800px) {
  .welcome-title {
    font-size: 54px;
  }

  .welcome-date {
    font-size: 56px;
  }

  .transfert-title {
    font-size: 36px;
  }
}
</style>
<script setup lang="ts">
</script>
