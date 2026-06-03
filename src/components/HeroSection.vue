<template>
  <section class="hero print-page">
    <div class="blob blob-warm"></div>
    <div class="blob blob-gold"></div>
    <div class="blob blob-pink"></div>
    <div class="deco-dots">
      <span v-for="i in 12" :key="i"></span>
    </div>

    <div class="hero-content fade-in">
      <div class="hero-badge">PET GROWTH LIFESTYLE BRAND</div>
      <img class="hero-logo" src="/品牌logo.jpg" alt="屿尾与季" />
      <div class="hero-line"></div>
      <h1 class="hero-name">屿尾与季</h1>
      <p class="hero-en">YUWEIYUJI</p>
      <p class="hero-slogan">陪伴毛孩子的每一个四季</p>
      <p class="hero-sub">伴成长朝夕 <span class="dot"></span> 守健康四季</p>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 297mm;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
  background: linear-gradient(160deg, #FEFAF6 0%, #FCF4E7 25%, #F8EAD5 50%, #F5E2C8 75%, #F2DCC0 100%);
}

.blob { position: absolute; border-radius: 50%; pointer-events: none; }
.blob-warm {
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(224,123,76,0.12) 0%, rgba(224,123,76,0.03) 50%, transparent 70%);
  top: -100px; right: -120px;
}
.blob-gold {
  width: 300px; height: 300px;
  background: radial-gradient(circle, rgba(217,185,145,0.16) 0%, rgba(217,185,145,0.04) 50%, transparent 70%);
  bottom: -80px; left: -80px;
}
.blob-pink {
  width: 220px; height: 220px;
  background: radial-gradient(circle, rgba(242,217,205,0.20) 0%, rgba(242,217,205,0.05) 50%, transparent 70%);
  top: 50%; left: 50%; transform: translate(-50%, -50%);
}

.deco-dots {
  position: absolute;
  top: 60px; right: 50px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 8px;
  z-index: 1;
}
.deco-dots span {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--accent);
  opacity: 0.20;
}

.hero-content {
  position: relative;
  z-index: 2;
  padding: 40px 30px;
}

.hero-badge {
  display: inline-block;
  background: var(--accent-warm);
  color: #fff;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 6px;
  padding: 5px 18px;
  border-radius: 24px;
  margin-bottom: 24px;
}

.hero-logo {
  width: 340px;
  max-width: 88%;
  margin-bottom: 24px;
  filter: drop-shadow(0 6px 20px rgba(60,25,5,0.10));
}

.hero-line {
  width: 120px;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--accent-warm), var(--rust), var(--accent-warm), transparent);
  margin: 0 auto 24px;
  border-radius: 2px;
}

.hero-name {
  font-family: "Noto Serif SC", serif;
  font-size: 52px;
  font-weight: 900;
  letter-spacing: 12px;
  color: var(--text);
  margin-bottom: 6px;
}

.hero-en {
  font-size: 17px;
  letter-spacing: 12px;
  color: var(--accent-deep);
  margin-bottom: 24px;
  font-weight: 400;
}

.hero-slogan {
  font-family: "Noto Serif SC", serif;
  font-size: 26px;
  color: var(--text-mid);
  letter-spacing: 5px;
  line-height: 1.8;
  font-weight: 600;
}

.hero-sub {
  font-size: 15px;
  color: var(--accent-warm);
  letter-spacing: 3px;
  font-weight: 500;
  margin-top: 8px;
}

.dot {
  display: inline-block;
  width: 4px; height: 4px;
  background: var(--accent-warm);
  border-radius: 50%;
  vertical-align: middle;
  margin: 0 5px;
}

@media (max-width: 768px) {
  .hero-name { font-size: 34px; letter-spacing: 6px; }
  .hero-slogan { font-size: 18px; letter-spacing: 3px; }
  .hero-logo { width: 260px; }
}
</style>
