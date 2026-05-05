<template>
  <section class="details" id="details">
    <div class="scallop"></div>
    <div class="section-dark">
      <div class="section-dark-inside">
        <div class="details-info">
          <h2 class="title-text details-title" data-aos="fade-up" data-aos-once="true">Детали</h2>
          <p class="descr-text" data-aos="fade-right" data-aos-once="true" data-aos-delay="200">
            Если вы ищете альтернативу традиционному букету, мы будем рады бутылочке вашего любимого напитка. Ваш
            подарок точно не завянет, а со временем станет только лучше.
          </p>
          <div class="details-block-img" data-aos="fade-left" data-aos-once="true" data-aos-delay="200">
            <img src="/stars.png" alt=""/>
          </div>
          <p class="descr-text" data-aos="fade-right" data-aos-once="true" data-aos-delay="200">
            Пожалуйста, обратите внимание на время сбора гостей и заранее сообщите нам, если у вас возникнут вопросы.
          </p>
        </div>
      </div>
    </div>
    <div class="scallop-bottom"></div>
  </section>
</template>
<script setup lang="ts">

</script>
<style scoped>
.details {
  position: relative;
  z-index: 2;
  margin-top: -2px;
}

.details-info {
  width: 100%;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  text-align: center;
}

.details-title {
  color: var(--bg);
}

.details-block-img {
  width: 30px;
  margin: 10px;
  flex-shrink: 0;
}

.details-block-img img {
  width: 100%;
  filter: brightness(0) invert(1);
}

@media (max-width: 600px) {
  .details-block-img {
    width: 24px;
  }
}

</style>
