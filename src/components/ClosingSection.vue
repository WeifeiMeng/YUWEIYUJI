<template>
  <section class="closing print-page">
    <div class="blob blob-warm"></div>
    <div class="blob blob-pink"></div>
    <div class="blob blob-gold"></div>
    <div class="deco-dots">
      <span v-for="i in 12" :key="i"></span>
    </div>

    <div class="closing-content fade-in">
      <img class="closing-img" src="/品牌logo3.jpg" alt="屿尾与季" />
      <div class="closing-line"></div>
      <p class="closing-quote">屿尾与季不是一家只卖宠物食品的品牌。</p>
      <p class="closing-sub">
        我们希望用真实的食材、真诚的产品和长期的陪伴，<br />
        守护毛孩子成长中的每一个四季。
      </p>
      <div class="closing-footer">
        屿尾与季 <span class="dot"></span> YUWEIYUJI
      </div>
    </div>
  </section>
</template>

<style scoped>
.closing {
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
  width: 360px; height: 360px;
  background: radial-gradient(circle, rgba(224,123,76,0.09) 0%, transparent 70%);
  top: -80px; left: -100px;
}
.blob-pink {
  width: 300px; height: 300px;
  background: radial-gradient(circle, rgba(242,217,205,0.15) 0%, transparent 70%);
  bottom: -60px; right: -80px;
}
.blob-gold {
  width: 220px; height: 220px;
  background: radial-gradient(circle, rgba(217,185,145,0.10) 0%, transparent 70%);
  top: 50%; left: 50%; transform: translate(-50%, -50%);
}

.deco-dots {
  position: absolute;
  bottom: 50px; left: 40px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
  pointer-events: none;
}
.deco-dots span {
  width: 8px; height: 8px;
  border-radius: 50%;
  background: var(--accent);
  opacity: 0.22;
}

.closing-content {
  position: relative;
  z-index: 2;
  padding: 40px 30px;
}

.closing-img {
  width: 280px;
  max-width: 85%;
  margin-bottom: 28px;
}

.closing-line {
  width: 80px;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--accent-warm), var(--rust), var(--accent-warm), transparent);
  margin: 0 auto 28px;
  border-radius: 2px;
}

.closing-quote {
  font-family: "Noto Serif SC", serif;
  font-size: 26px;
  font-weight: 900;
  letter-spacing: 4px;
  color: var(--text);
  line-height: 2.1;
  max-width: 440px;
  margin: 0 auto;
}

.closing-sub {
  font-size: 17px;
  color: var(--text-mid);
  margin-top: 24px;
  letter-spacing: 2px;
  line-height: 2.2;
}

.closing-footer {
  margin-top: 36px;
  font-family: "Noto Serif SC", serif;
  font-size: 15px;
  letter-spacing: 5px;
  font-weight: 700;
  display: inline-block;
  padding: 6px 24px;
  border-radius: 24px;
  background: rgba(255,255,255,0.5);
  color: var(--accent-warm);
}

.dot {
  display: inline-block;
  width: 4px; height: 4px;
  background: var(--accent-warm);
  border-radius: 50%;
  vertical-align: middle;
  margin: 0 6px;
}
</style>
