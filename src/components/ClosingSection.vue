<template>
  <section class="closing-section">
    <div class="blob blob-warm" style="width:500px;height:500px;top:-120px;left:-140px;"></div>
    <div class="blob blob-pink" style="width:400px;height:400px;bottom:-100px;right:-120px;"></div>
    <div class="blob blob-gold" style="width:280px;height:280px;top:50%;left:50%;transform:translate(-50%,-50%);"></div>

    <div class="closing-inner fade-in">
      <img class="closing-img" src="/品牌logo3.jpg" alt="屿尾与季" />
      <div class="closing-line"></div>
      <p class="closing-quote">屿尾与季不是一家只卖宠物食品的品牌。</p>
      <p class="closing-sub">
        我们希望用真实的食材、真诚的产品和长期的陪伴，<br />
        守护毛孩子成长中的每一个四季。
      </p>
      <div class="closing-footer">
        屿尾与季 <i></i> YUWEIYUJI
      </div>
    </div>
  </section>
</template>

<style scoped>
.closing-section {
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
.blob-warm { background: radial-gradient(circle, rgba(224,123,76,0.10) 0%, transparent 70%); }
.blob-pink { background: radial-gradient(circle, rgba(242,217,205,0.16) 0%, transparent 70%); }
.blob-gold { background: radial-gradient(circle, rgba(217,185,145,0.11) 0%, transparent 70%); }

.closing-inner {
  position: relative;
  z-index: 2;
  padding: 60px 32px;
}

.closing-img {
  width: 320px;
  max-width: 85%;
  margin-bottom: 36px;
}

.closing-line {
  width: 100px;
  height: 3px;
  background: linear-gradient(90deg, transparent, var(--accent-warm), var(--rust), var(--accent-warm), transparent);
  margin: 0 auto 36px;
  border-radius: 2px;
}

.closing-quote {
  font-family: "Noto Serif SC", serif;
  font-size: 32px;
  font-weight: 900;
  letter-spacing: 5px;
  color: var(--text);
  line-height: 2.1;
  max-width: 500px;
  margin: 0 auto;
}

.closing-sub {
  font-size: 20px;
  color: var(--text-mid);
  margin-top: 28px;
  letter-spacing: 3px;
  line-height: 2.2;
}

.closing-footer {
  margin-top: 48px;
  font-family: "Noto Serif SC", serif;
  font-size: 17px;
  letter-spacing: 6px;
  font-weight: 700;
  display: inline-block;
  padding: 10px 32px;
  border-radius: 30px;
  background: rgba(255,255,255,0.5);
  color: var(--accent-warm);
}

.closing-footer i {
  display: inline-block;
  width: 5px; height: 5px;
  background: var(--accent-warm);
  border-radius: 50%;
  vertical-align: middle;
  margin: 0 8px;
}

@media (max-width: 768px) {
  .closing-quote { font-size: 24px; }
  .closing-sub { font-size: 16px; }
}
</style>
