<template>
  <section class="header" id="home">
    <div class="header-blocks">
      <div class="header-block text-dark" data-aos="fade-down" data-aos-once="true">Наконец-то!</div>
      <div class="header-block">
        <p class="header-sub">так сказали наши близкие и родные, когда узнали, эту</p>
        <p class="header-big text-dark">новость</p>
      </div>
      <div class="header-block-img">
        <img src="/arrow.svg" alt=""/>
      </div>
    </div>
  </section>
</template>

<style scoped>
.header {
  min-height: 100vh;
  background: var(--bg);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.header-blocks {
  height: 100vh;
  width: 100vw;
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
</style>
