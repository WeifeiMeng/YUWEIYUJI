<template>
  <section class="story">
    <div class="section-header fade-in">
      <span class="sec-num">02</span>
      <span class="sec-tag">✦ 品牌故事</span>
      <h2 class="sec-title">关于屿尾与季</h2>
    </div>

    <div class="story-grid fade-in">
      <div class="story-text">
        <p>我们总在记录四季更替，却很少意识到——毛孩子的一生，也藏在这些季节里。</p>
        <p>第一次学会奔跑，第一次安静依偎，第一次一起搬家，第一次迎来春天。</p>
        <p class="story-highlight">屿尾与季希望用真实的食材、真诚的产品与长期的陪伴，守护毛孩子成长中的每一个四季。</p>
      </div>
      <div class="story-img-wrap">
        <img class="story-img" src="/品牌logo2.jpg" alt="屿尾与季品牌故事" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.story {
  padding: 4mm 12mm;
  position: relative;
  overflow: hidden;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.section-header { position: relative; z-index: 1; margin-bottom: 4mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 42px; font-weight: 900;
  color: rgba(217,185,145,0.07);
  position: absolute; top: -12px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 10px; letter-spacing: 5px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 2mm; }
.sec-title { font-family: "Noto Serif SC", serif; font-size: 24px; font-weight: 900; letter-spacing: 3px; color: var(--text); line-height: 1.2; }

.story-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 5mm;
  align-items: center;
  position: relative;
  z-index: 1;
}

.story-text p {
  font-size: 12px; color: var(--text-mid);
  line-height: 1.9; margin-bottom: 2mm;
}

.story-highlight {
  font-family: "Noto Serif SC", serif;
  font-size: 15px; font-weight: 700;
  color: var(--text);
  letter-spacing: 1px;
  margin-top: 3mm;
  line-height: 1.7;
  background: linear-gradient(180deg, transparent 58%, rgba(224,123,76,0.14) 58%);
  display: inline;
  padding: 0 2px;
}

.story-img-wrap {
  background: linear-gradient(145deg, #FFF5EE, #FFFDF8);
  padding: 2mm;
  border-radius: 8px;
  border: 2px solid rgba(224,123,76,0.10);
  box-shadow: var(--card-shadow);
  position: relative;
}

.story-img {
  width: 100%;
  border-radius: 5px;
  display: block;
  max-height: 55mm;
  object-fit: cover;
}

@media (max-width: 768px) {
  .story-grid { grid-template-columns: 1fr; }
  .story { padding: 4mm 6mm; }
}
</style>
