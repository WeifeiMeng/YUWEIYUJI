<template>
  <section class="section bg-cool">
    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">内容传播与展会</div>
      </div>

      <div class="channel-grid fade-in">
        <div class="channel-card" v-for="(c, i) in channels" :key="c.name" :class="'cc-' + (i + 1)">
          <div class="cc-name">{{ c.name }}</div>
          <div class="cc-content">
            <span v-for="item in c.items" :key="item">{{ item }}<br /></span>
          </div>
        </div>
      </div>

      <div class="expo-block fade-in">
        <h3 class="expo-title">一座属于毛孩子的小岛</h3>
        <p class="expo-desc">展会视觉：自然 · 木质 · 留白 · 奶油色 · 生活场景</p>
        <div class="expo-flow">
          <span class="step">品牌故事</span>
          <span class="arrow">→</span>
          <span class="step">产品矩阵</span>
          <span class="arrow">→</span>
          <span class="step">试吃体验</span>
          <span class="arrow">→</span>
          <span class="step">品质背书</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const channels = [
  { name: '小红书', items: ['成长记录', '养宠日记', '产品摆拍', '陪伴故事'] },
  { name: '抖音', items: ['吃播', '互动奖励', '成长过程', '真实反馈'] },
  { name: '淘宝', items: ['品牌感', '产品感', '品质感'] },
]
</script>

<style scoped>
.channel-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-bottom: 40px;
}

.channel-card {
  padding: 40px 24px;
  border-radius: var(--card-radius);
  text-align: center;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
  transition: transform 0.3s;
}
.channel-card:hover { transform: translateY(-6px); }
.cc-1 { background: linear-gradient(180deg, #FFF5EE, #FFFDFA); border-color: rgba(224,123,76,0.18); }
.cc-2 { background: linear-gradient(180deg, #F5F8FB, #FFFDFA); border-color: rgba(150,190,210,0.20); }
.cc-3 { background: linear-gradient(180deg, #FFFDF8, #FFFBF5); border-color: rgba(217,185,145,0.22); }

.cc-name {
  font-family: "Noto Serif SC", serif;
  font-size: 28px;
  font-weight: 900;
  letter-spacing: 4px;
  color: var(--text);
  margin-bottom: 16px;
}
.cc-content { font-size: 16px; color: var(--text-mid); line-height: 2.3; }

.expo-block {
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF8 100%);
  padding: 44px 32px;
  text-align: center;
  border-radius: var(--card-radius);
  border: 2px solid rgba(224,123,76,0.14);
  box-shadow: var(--card-shadow);
}

.expo-title {
  font-family: "Noto Serif SC", serif;
  font-size: 32px;
  font-weight: 900;
  letter-spacing: 5px;
  color: var(--text);
  margin-bottom: 12px;
}
.expo-desc {
  font-size: 16px;
  color: var(--text-mid);
  letter-spacing: 2px;
  margin-bottom: 24px;
}

.expo-flow {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 12px;
  font-size: 16px;
  color: var(--text-mid);
  flex-wrap: wrap;
  font-weight: 500;
}
.step {
  background: var(--white);
  padding: 8px 22px;
  border-radius: 30px;
  border: 2px solid rgba(224,123,76,0.18);
  font-weight: 700;
  box-shadow: 0 2px 8px rgba(60,30,10,0.04);
}
.arrow {
  color: var(--accent-warm);
  font-family: "Noto Serif SC", serif;
  font-size: 24px;
  font-weight: 700;
}

@media (max-width: 768px) {
  .channel-grid { grid-template-columns: 1fr; }
}
</style>
