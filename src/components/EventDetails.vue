<template>
  <!-- Dark invitation block -->
  <section class="info-date">
    <div class="scallop"></div>
    <div class="section-dark">
      <div class="section-dark-inside">
        <div class="info-invitation" data-aos="fade-up" data-aos-once="true">
          <h2 class="welcome-title title-text">Мы женимся!</h2>
          <p class="descr-text" data-aos="fade-up" data-aos-once="true" data-aos-delay="200">
            Один день в этом году будет для нас особенным и мы хотим провести его в кругу близких и друзей.
            <br><br>
            С большим удовольствием приглашаем вас на знаменательный праздник - <br> нашу свадьбу!
          </p>
          <div class="welcome-date title-text" data-aos="fade-up" data-aos-once="true" data-aos-delay="400">29 - 09 - 26</div>
        </div>
        <div class="img-bottom" data-aos="zoom-in" data-aos-once="true">
          <img src="/target.png" loading="lazy" alt="" />
        </div>
      </div>
    </div>
    <div class="scallop-bottom"></div>
  </section>

  <!-- Light place block -->
  <section class="place" id="place">
    <div class="place-inside">
      <div class="place-item">
        <h2 class="place-title title-text">Точка сбора</h2>
        <p class="descr-text">Для вашего удобства будет организован трансфер</p>
        <p class="descr-text">ул. Горновых 17, г. Гродно </p>
        <p class="place-time text-dark">15:30</p>
        <a class="rsvp-btn" href="https://yandex.com/maps/-/CPvSq0jb" target="_blank" rel="noopener">Маршрут</a>
      </div>
      <div class="place-item">
        <h2 class="place-title title-text">Торжественная регистрация</h2>
        <p class="descr-text">Банкетный Зал "Event Hall Olshevski"</p>
        <p class="descr-text">Старая Весь 19А, д. Василевичи</p>
        <p class="place-time text-dark">16:00</p>
        <a class="rsvp-btn" href="https://yandex.com/maps/-/CPvSqT2m" target="_blank" rel="noopener">Маршрут</a>
      </div>

      <div class="foto-bottom" data-aos="zoom-in" data-aos-once="true">
        <img src="/foto.png" loading="lazy" alt="" />
      </div>

    </div>
  </section>
</template>

<style scoped>
.info-date {
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
.place {
  position: relative;
  z-index: 2;
  background: var(--bg);
  margin-top: -4px;
}

.place-inside {
  width: 90%;
  max-width: 800px;
  margin: auto;
  padding: 30px 5%;
}

.place-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 8px;
  padding: 30px 0;
}

.place-item--two {
  padding-top: 50px;
}

.place-title {
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

.place-time {
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
  .welcome-title { font-size: 54px; }
  .welcome-date { font-size: 56px; }
  .place-title { font-size: 36px; }
}
</style>
<script setup lang="ts">
</script>
