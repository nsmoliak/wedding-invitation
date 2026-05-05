<template>
  <section id="plan" class="timetable">
    <div class="scallop"></div>
    <div class="section-dark">
      <div class="section-dark-inside">
        <div class="plan-place">
          <h2 class="title-text timetable-title" data-aos="fade-down" data-aos-once="true">План дня</h2>
          <div class="timetable-block">
            <div
              v-for="(item, i) in schedule"
              :key="i"
              class="timetable-block-stroke"
              :class="{ 'timetable-block-stroke--right': i % 2 === 1 }"
              :data-aos="i % 2 === 1 ? 'fade-left' : 'fade-right'"
              data-aos-once="true"
            >
              <div class="timetable-text">
                <div class="timetable-time">{{ item.time }}</div>
                <div class="timetable-name">{{ item.name }}</div>
                <div class="timetable-descr">{{ item.descr }}</div>
              </div>
              <div class="timetable-block-img" v-if="i < schedule.length - 1">
                <img src="/arrow-plan.png" alt="" />
              </div>
              <div class="timetable-block-img" v-else></div>
              <div class="timetable-block-empty"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="scallop-bottom"></div>
  </section>
</template>

<script setup>
const schedule = [
  { time: '16:00', name: 'Сбор гостей', descr: 'Бокал шампанского и закуски, пока праздник набирает силу' },
  { time: '16:30', name: 'Церемония', descr: 'Не исключено, что вам потребуются платочки для этого трогательного момента' },
  { time: '17:00', name: 'Праздничный ужин', descr: 'Вкусная еда, тёплые тосты и много любви за одним столом' },
  { time: '22:30', name: 'Свадебный торт', descr: 'Время загадать желание и отведать главный десерт вечера' },
  { time: '00:00', name: 'Окончание праздника', descr: 'Даже такая вечеринка может закончиться, но мы придумаем ещё поводы собраться вместе' },
]
</script>

<style scoped>
.timetable {
  position: relative;
  z-index: 0;
  margin-top: -4px;
}

.plan-place {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.timetable-title {
  color: var(--bg);
  margin-bottom: 10px;
}

.timetable-block {
  display: flex;
  gap: 30px;
  flex-direction: column;
}

.timetable-block-stroke {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
}

.timetable-text {
  width: 60%;
  text-align: left;
  display: flex;
  gap: 10px;
  flex-direction: column;
}

.timetable-time {
  font-size: 180%;
  line-height: 1;
  color: var(--bg);
}

.timetable-name {
  text-transform: uppercase;
  color: var(--bg);
}

.timetable-descr {
  font-size: 80%;
  line-height: 1;
  padding-bottom: 30px;
  color: rgba(239, 236, 224, 0.75);
}

.timetable-block-img {
  width: 100px;
  transform: scaleX(-1);
  flex-shrink: 0;
}

.timetable-block-img img {
  width: 100%;
  filter: brightness(0) invert(1);
  opacity: 0.6;
}

.timetable-block-empty {
  width: calc(40% - 102px);
  flex-shrink: 0;
}

.timetable-block-stroke--right {
  flex-direction: row-reverse;
}

.timetable-block-stroke--right .timetable-text {
  text-align: right;
}

.timetable-block-stroke--right .timetable-block-img {
  transform: scaleX(1);
}

@media (max-width: 600px) {
  .timetable-block-img { width: 60px; }
  .timetable-block-empty { width: calc(40% - 62px); }
}
</style>
