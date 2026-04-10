<template>
  <section class="question" id="rsvp">
    <div class="question-inside">
      <h2 class="title-text question-title">Присутствие</h2>
      <p class="descr-text question-descr">
        Пожалуйста, подтвердите ваше присутствие на нашем празднике до
        <strong class="text-dark">1 июня 2026 года</strong>
        любым удобным для вас способом или заполните форму ниже:
      </p>

      <form v-if="!submitted" id="questions" @submit.prevent="handleSubmit">
        <div class="question-string">
          <label class="question-label">
            <span>Ваше имя</span>
          </label>
          <input
            v-model="form.name"
            type="text"
            placeholder="Имя и фамилия"
            required
          />
        </div>

        <div class="question-string">
          <label class="question-label">Количество гостей</label>
          <input
            v-model.number="form.guests"
            type="number"
            min="1"
            max="10"
            placeholder="1"
          />
          <p class="question-text-mini">*Количество должно быть целым числом, не более 10.</p>
        </div>

        <div class="question-string">
          <label class="question-label">Пожелания к меню</label>
          <input
            v-model="form.menu"
            type="text"
            placeholder="Аллергии, предпочтения..."
          />
        </div>

        <div class="button-container">
          <button type="submit" class="rsvp-btn">Подтвердить</button>
          <button type="button" class="rsvp-btn rsvp-btn-decline" @click="handleDecline">Отклонить</button>
        </div>
      </form>

      <div v-else class="rsvp-success">
        <template v-if="form.attendance === 'yes'">
          <h3 class="title-text rsvp-success-title">Спасибо, {{ form.name }}!</h3>
          <p class="descr-text">Мы очень рады, что вы будете с нами в этот день!</p>
        </template>
        <template v-else>
          <h3 class="title-text rsvp-success-title">Жаль, {{ form.name }}!</h3>
          <p class="descr-text">Мы будем скучать по вам в этот день.</p>
        </template>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, reactive } from 'vue'

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

.question-title {
  color: var(--accent);
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
