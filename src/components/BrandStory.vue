<template>
  <section class="section bg-neutral">
    <div class="blob blob-gold" style="width:360px;height:360px;top:-80px;right:-100px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">品牌故事</div>
        <h2 class="section-title">关于屿尾与季</h2>
      </div>

      <div class="story-grid fade-in">
        <div class="story-text">
          <p>我们总在记录四季更替，却很少意识到——毛孩子的一生，也藏在这些季节里。</p>
          <p>第一次学会奔跑，第一次安静依偎，第一次一起搬家，第一次迎来春天。</p>
          <p>那些看似平凡的日常，其实都值得被认真珍藏。</p>
          <p class="story-highlight">屿尾与季希望用真实的食材、真诚的产品与长期的陪伴，守护毛孩子成长中的每一个四季。</p>
        </div>
        <div class="story-img-wrap">
          <img class="story-img" src="/品牌logo2.jpg" alt="屿尾与季品牌故事" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.story-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 64px;
  align-items: center;
}

.story-text p {
  font-size: 17px;
  color: var(--text-mid);
  line-height: 2.3;
  margin-bottom: 16px;
}

.story-highlight {
  font-family: "Noto Serif SC", serif;
  font-size: 24px;
  font-weight: 700;
  color: var(--text);
  letter-spacing: 2px;
  margin-top: 32px;
  line-height: 1.9;
  background: linear-gradient(180deg, transparent 58%, rgba(224,123,76,0.18) 58%);
  display: inline;
  padding: 0 4px;
}

.story-img-wrap {
  background: linear-gradient(145deg, #FFF5EE, #FFFDF8);
  padding: 20px;
  border-radius: var(--card-radius);
  border: 2px solid rgba(224,123,76,0.12);
  box-shadow: var(--card-shadow-lg);
  position: relative;
}

.story-img {
  width: 100%;
  border-radius: 10px;
  display: block;
}

@media (max-width: 768px) {
  .story-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  .story-text p { font-size: 15px; }
  .story-highlight { font-size: 20px; }
}
</style>
