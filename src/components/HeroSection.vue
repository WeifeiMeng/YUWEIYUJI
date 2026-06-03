<template>
  <section class="hero-section">
    <div class="hero-inner fade-in">
      <img class="hero-logo" src="/品牌logo.jpg" alt="屿尾与季" />
      <div class="hero-line"></div>
      <h1 class="hero-name">屿尾与季</h1>
      <p class="hero-en">YUWEIYUJI</p>
      <p class="hero-slogan">陪伴毛孩子的每一个四季</p>
      <p class="hero-sub">伴成长朝夕 <i></i> 守健康四季</p>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
  background: #fff;
}

.hero-inner {
  position: relative;
  z-index: 2;
  padding: 60px 32px;
}

.hero-logo {
  width: 380px;
  max-width: 90%;
  margin-bottom: 40px;
}

.hero-line {
  width: 100px;
  height: 2px;
  background: var(--accent-warm);
  margin: 0 auto 40px;
  border-radius: 1px;
}

.hero-name {
  font-family: "Noto Serif SC", serif;
  font-size: 56px;
  font-weight: 900;
  letter-spacing: 14px;
  color: var(--text);
  margin-bottom: 8px;
}

.hero-en {
  font-size: 18px;
  letter-spacing: 14px;
  color: var(--accent-deep);
  margin-bottom: 32px;
}

.hero-slogan {
  font-family: "Noto Serif SC", serif;
  font-size: 28px;
  color: var(--text-mid);
  letter-spacing: 4px;
  line-height: 1.8;
  font-weight: 600;
}

.hero-sub {
  font-size: 16px;
  color: var(--accent-warm);
  letter-spacing: 3px;
  font-weight: 500;
  margin-top: 10px;
}

.hero-sub i {
  display: inline-block;
  width: 4px; height: 4px;
  background: var(--accent-warm);
  border-radius: 50%;
  vertical-align: middle;
  margin: 0 8px;
}

@media (max-width: 768px) {
  .hero-name { font-size: 36px; letter-spacing: 8px; }
  .hero-slogan { font-size: 20px; letter-spacing: 2px; }
  .hero-logo { width: 260px; }
  .hero-en { font-size: 14px; letter-spacing: 10px; }
}
</style>
