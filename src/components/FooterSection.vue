<template>
  <section class="footer">
    <div class="scallop"></div>
    <div class="section-dark">
      <div class="section-dark-inside">
        <div class="footer-container">
          <div class="names-footer-block">
            <div class="header-name" style="text-align: left;">
              <h2 class="welcome-title title-text">Даниил и</h2>
            </div>
            <div class="header-name" style="text-align: right;">
              <h2 class="welcome-title title-text">Наталья</h2>
            </div>
          </div>
          <div class="footer-img">
            <img src="/car.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.footer {
  position: relative;
  z-index: 0;
  margin-top: -4px;
}

.footer-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}

.names-footer-block {
  max-width: 400px;
  width: 80%;
  display: flex;
  flex-direction: column;
  margin: auto;
}

.welcome-title {
  color: var(--bg);
  font-size: 64px;
  line-height: 1;
  font-weight: 500;
}

.header-name {
  width: 100%;
}

.footer-img {
  width: 60%;
  max-width: 300px;
  margin: auto;
}

.footer-img img {
  width: 100%;
}

.section-dark {
  box-shadow: 0 100px 0 0 var(--accent);
}
</style>
