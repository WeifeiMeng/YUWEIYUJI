<template>
  <section class="hero-section">
    <div class="blob blob-warm" style="width:600px;height:600px;top:-160px;right:-180px;"></div>
    <div class="blob blob-gold" style="width:420px;height:420px;bottom:-120px;left:-120px;"></div>
    <div class="blob blob-pink" style="width:320px;height:320px;top:45%;left:50%;transform:translate(-50%,-50%);"></div>

    <div class="hero-inner fade-in">
      <div class="hero-badge">PET GROWTH LIFESTYLE BRAND</div>
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
  background: linear-gradient(160deg, #FEFAF6 0%, #FCF4E7 25%, #F8EAD5 50%, #F5E2C8 75%, #F2DCC0 100%);
}

.blob {
  position: absolute;
  border-radius: 50%;
  pointer-events: none;
  z-index: 0;
}
.blob-warm { background: radial-gradient(circle, rgba(224,123,76,0.12) 0%, rgba(224,123,76,0.03) 50%, transparent 70%); }
.blob-gold { background: radial-gradient(circle, rgba(217,185,145,0.16) 0%, rgba(217,185,145,0.04) 50%, transparent 70%); }
.blob-pink { background: radial-gradient(circle, rgba(242,217,205,0.20) 0%, rgba(242,217,205,0.05) 50%, transparent 70%); }

.hero-inner {
  position: relative;
  z-index: 2;
  padding: 60px 32px;
}

.hero-badge {
  display: inline-block;
  background: var(--accent-warm);
  color: #fff;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 8px;
  padding: 10px 28px;
  border-radius: 30px;
  margin-bottom: 36px;
}

.hero-logo {
  width: 420px;
  max-width: 90%;
  margin-bottom: 32px;
  filter: drop-shadow(0 8px 28px rgba(60,25,5,0.12));
}

.hero-line {
  width: 140px;
  height: 3px;
  background: linear-gradient(90deg, transparent, var(--accent-warm), var(--rust), var(--accent-warm), transparent);
  margin: 0 auto 32px;
  border-radius: 2px;
}

.hero-name {
  font-family: "Noto Serif SC", serif;
  font-size: 64px;
  font-weight: 900;
  letter-spacing: 16px;
  color: var(--text);
  margin-bottom: 10px;
}

.hero-en {
  font-size: 20px;
  letter-spacing: 16px;
  color: var(--accent-deep);
  margin-bottom: 36px;
}

.hero-slogan {
  font-family: "Noto Serif SC", serif;
  font-size: 32px;
  color: var(--text-mid);
  letter-spacing: 6px;
  line-height: 1.8;
  font-weight: 600;
}

.hero-sub {
  font-size: 18px;
  color: var(--accent-warm);
  letter-spacing: 4px;
  font-weight: 500;
  margin-top: 12px;
}

.hero-sub i {
  display: inline-block;
  width: 5px; height: 5px;
  background: var(--accent-warm);
  border-radius: 50%;
  vertical-align: middle;
  margin: 0 8px;
}

@media (max-width: 768px) {
  .hero-name { font-size: 38px; letter-spacing: 8px; }
  .hero-slogan { font-size: 22px; letter-spacing: 3px; }
  .hero-logo { width: 280px; }
  .hero-en { font-size: 16px; letter-spacing: 10px; }
}
</style>
