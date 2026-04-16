<template>
  <section class="question" id="rsvp">
    <div class="scallop"></div>
    <div class="section-dark">
      <div class="section-dark-inside">
        <div class="question-inside">
          <h2 class="title-text question-title">Присутствие</h2>
          <p class="descr-text question-descr">
            Пожалуйста, подтвердите ваше присутствие на нашем празднике до 1 августа 2026 года любым удобным для вас способом.
          </p>

          <div class="rsvp-buttons">
            <div class="rsvp-approves">
              <span class="rsvp-member">Сторона жениха</span>
              <div class="rsvp-contacts">
                <a class="rsvp-phone" href="tel:+375293529638">
                  <img src="/phone.svg" width="24" height="24" alt="" />
                  +375 (29) 352-96-38
                </a>
              </div>
              <div class="rsvp-social">
                <a href="https://t.me/ChernickijD" target="_blank"><img src="/telegram.svg" width="24" height="24" alt="Telegram" /></a>
                <a href="viber://contact?number=+375293529638&text=Привет! Мы идём на свадьбу!"><img src="/viber.svg" width="24" height="24" alt="Viber" /></a>
              </div>
            </div>

            <div class="rsvp-approves">
              <span class="rsvp-member">Сторона невесты</span>
              <div class="rsvp-contacts">
                <a class="rsvp-phone" href="tel:+375336553207">
                  <img src="/phone.svg" width="24" height="24" alt="" />
                  +375 (33) 655-32-07
                </a>
              </div>
              <div class="rsvp-social">
                <a href="https://t.me/natallia_smoliak" target="_blank"><img src="/telegram.svg" width="24" height="24" alt="Telegram" /></a>
                <a href="viber://contact?number=+375336553207&text=Привет! Мы идём на свадьбу!"><img src="/viber.svg" width="24" height="24" alt="Viber" /></a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!--      <form v-if="!submitted" id="questions" @submit.prevent="handleSubmit">-->
      <!--        <div class="question-string">-->
      <!--          <label class="question-label">-->
      <!--            <span>Ваше имя</span>-->
      <!--          </label>-->
      <!--          <input-->
      <!--            v-model="form.name"-->
      <!--            type="text"-->
      <!--            placeholder="Имя и фамилия"-->
      <!--            required-->
      <!--          />-->
      <!--        </div>-->

      <!--        <div class="question-string">-->
      <!--          <label class="question-label">Количество гостей</label>-->
      <!--          <input-->
      <!--            v-model.number="form.guests"-->
      <!--            type="number"-->
      <!--            min="1"-->
      <!--            max="10"-->
      <!--            placeholder="1"-->
      <!--          />-->
      <!--          <p class="question-text-mini">*Количество должно быть целым числом, не более 10.</p>-->
      <!--        </div>-->

      <!--        <div class="question-string">-->
      <!--          <label class="question-label">Пожелания к меню</label>-->
      <!--          <input-->
      <!--            v-model="form.menu"-->
      <!--            type="text"-->
      <!--            placeholder="Аллергии, предпочтения..."-->
      <!--          />-->
      <!--        </div>-->

      <!--        <div class="button-container">-->
      <!--          <button type="submit" class="rsvp-btn">Подтвердить</button>-->
      <!--          <button type="button" class="rsvp-btn rsvp-btn-decline" @click="handleDecline">Отклонить</button>-->
      <!--        </div>-->
      <!--      </form>-->

      <!--      <div v-else class="rsvp-success">-->
      <!--        <template v-if="form.attendance === 'yes'">-->
      <!--          <h3 class="title-text rsvp-success-title">Спасибо, {{ form.name }}!</h3>-->
      <!--          <p class="descr-text">Мы очень рады, что вы будете с нами в этот день!</p>-->
      <!--        </template>-->
      <!--        <template v-else>-->
      <!--          <h3 class="title-text rsvp-success-title">Жаль, {{ form.name }}!</h3>-->
      <!--          <p class="descr-text">Мы будем скучать по вам в этот день.</p>-->
      <!--        </template>-->
      <!--      </div>-->
    </div>
    <div class="scallop-bottom"></div>
  </section>
</template>

<script setup>
import {ref, reactive} from 'vue'

const submitted = ref(false)

const form = reactive({
  name: '',
  attendance: 'yes',
  guests: 1,
  menu: '',
})

function handleSubmit() {
  form.attendance = 'yes'
  submitted.value = true
}

function handleDecline() {
  form.attendance = 'no'
  submitted.value = true
}
</script>

<style scoped>
.question {
  background: var(--bg);
  position: relative;
  z-index: 2;
  margin-top: -2px;
}

.question-inside {
  width: 100%;
  margin: auto;
  padding: 0 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  text-align: center;
}

.details-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  width: 120%;
  padding-top: 10px;
}

.question-title {
  color: var(--bg);
}

.rsvp-buttons {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 70px;
  padding-top: 20px;
  width: 100%;
}

.rsvp-approves {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.rsvp-member {
  font-family: var(--font-main);
  font-size: 18px;
  color: var(--bg);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.rsvp-contacts {
  display: flex;
  align-items: center;
}

.rsvp-phone {
  display: flex;
  align-items: center;
  gap: 8px;
  color: var(--bg);
  font-size: 18px;
  font-family: var(--font-main);
  text-decoration: none;
}

.rsvp-phone img {
  filter: brightness(0) invert(1);
}

.rsvp-social {
  display: flex;
  gap: 12px;
}

.rsvp-social img {
  filter: brightness(0) invert(1);
  transition: opacity 0.2s;
}

.rsvp-social a:hover img {
  opacity: 0.7;
}

.question-descr {
  color: var(--text);
}

#questions {
  padding: 30px 0;
  display: flex;
  flex-direction: column;
  gap: 0;
  width: 90%;
  margin: auto;
  text-align: left;
}

.question-string {
  margin-bottom: 10px;
}

.question-label {
  display: flex;
  align-items: center;
  gap: 5px;
  margin-bottom: 0;
  font-size: 80%;
  color: var(--text);
  text-transform: uppercase;
}

.question-string input[type="text"],
.question-string input[type="number"] {
  border: 0;
  background-color: var(--bg);
  border-bottom: 1px solid var(--text);
  border-radius: 0;
  font-size: 14px;
  text-transform: uppercase;
  padding: 5px 0;
  width: 100%;
  font-family: var(--font-main);
  color: var(--text);
  outline: none;
}

.question-text-mini {
  font-size: 80%;
  padding: 10px 0 20px;
  color: var(--text);
  opacity: 0.6;
}

.button-container {
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  padding-top: 20px;
}

.rsvp-btn {
  background: none;
  text-transform: uppercase;
  font-size: 18px;
  font-family: var(--font-main);
  padding: 15px 20px 10px;
  min-width: 200px;
  margin: 0;
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

.rsvp-btn-decline {
  border-color: var(--text);
  color: var(--text);
}

.rsvp-success {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  padding: 40px 0;
}

.rsvp-success-title {
  color: var(--accent);
}
</style>
