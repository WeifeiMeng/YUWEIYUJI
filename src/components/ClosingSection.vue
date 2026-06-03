<template>
  <section class="closing-section">
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
  background: #fff;
}

.closing-inner {
  position: relative;
  z-index: 2;
  padding: 60px 32px;
}

.closing-img {
  width: 280px;
  max-width: 85%;
  margin-bottom: 36px;
}

.closing-line {
  width: 80px;
  height: 2px;
  background: var(--accent-warm);
  margin: 0 auto 36px;
  border-radius: 1px;
}

.closing-quote {
  font-family: "Noto Serif SC", serif;
  font-size: 30px;
  font-weight: 900;
  letter-spacing: 4px;
  color: var(--text);
  line-height: 2.1;
  max-width: 500px;
  margin: 0 auto;
}

.closing-sub {
  font-size: 18px;
  color: var(--text-mid);
  margin-top: 24px;
  letter-spacing: 2px;
  line-height: 2.2;
}

.closing-footer {
  margin-top: 44px;
  font-family: "Noto Serif SC", serif;
  font-size: 16px;
  letter-spacing: 5px;
  font-weight: 700;
  display: inline-block;
  padding: 8px 28px;
  border: 2px solid var(--accent-warm);
  border-radius: 30px;
  color: var(--accent-warm);
}

.closing-footer i {
  display: inline-block;
  width: 4px; height: 4px;
  background: var(--accent-warm);
  border-radius: 50%;
  vertical-align: middle;
  margin: 0 8px;
}

@media (max-width: 768px) {
  .closing-quote { font-size: 24px; }
  .closing-sub { font-size: 15px; }
}
</style>
