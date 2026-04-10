<template>
  <!-- Dark invitation block -->
  <section class="info-date">
    <div class="scallop"></div>
    <div class="section-dark">
      <div class="section-dark-inside">
        <div class="info-invitation">
          <h2 class="welcome-title title-text">Мы женимся!</h2>
          <p class="descr-text">
            Один день в этом году будет для нас особенным и мы хотим провести его в кругу близких и друзей.
            С большим удовольствием приглашаем вас на знаменательный праздник — нашу свадьбу!
          </p>
          <div class="welcome-date title-text">28 · 09 · 2026</div>
        </div>
      </div>
    </div>
    <div class="scallop-bottom"></div>
  </section>

  <!-- Light place block -->
  <section class="place" id="place">
    <div class="place-inside">
      <div class="place-item">
        <h2 class="place-title title-text">Торжественная регистрация</h2>
        <img class="separator-img" src="/stars.png" alt="" />
        <p class="descr-text">Event Hall Ольшевский</p>
        <p class="descr-text">Старая Весь 19А, Гродно</p>
        <p class="place-time text-dark">16:00</p>
        <a class="rsvp-btn" href="https://yandex.com/maps/org/event_hall_olshevski/219124670247/?ll=23.711256%2C53.804266&z=16" target="_blank" rel="noopener">Маршрут →</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.info-date {
  position: relative;
  z-index: 0;
  margin-top: -4px;
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

.place {
  position: relative;
  z-index: 2;
  background: var(--bg);
  margin-top: -4px;
  padding-top: 60px;
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
