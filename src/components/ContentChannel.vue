<template>
  <section class="channel">
    <div class="section-header fade-in">
      <span class="sec-num">10</span>
      <span class="sec-tag">✦ 内容传播与展会</span>
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
        <span class="step" v-for="(s, i) in expoSteps" :key="i">
          <template v-if="i % 2 === 0">{{ s }}</template>
          <template v-else><span class="arrow">→</span> {{ s }} </template>
        </span>
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
const expoSteps = ['品牌故事', '→', '产品矩阵', '→', '试吃体验', '→', '品质背书']
</script>

<style scoped>
.channel {
  padding: 6mm 12mm;
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
  font-size: 50px; font-weight: 900;
  color: rgba(165,185,140,0.06);
  position: absolute; top: -14px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 10px; letter-spacing: 6px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 2mm; }

.channel-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 3mm;
  position: relative; z-index: 1;
}

.channel-card {
  padding: 4mm;
  border-radius: 10px;
  text-align: center;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
  transition: transform 0.3s;
}
.channel-card:hover { transform: translateY(-2px); }
.cc-1 { background: linear-gradient(180deg, #FFF5EE, #FFFDFA); border-color: rgba(224,123,76,0.16); }
.cc-2 { background: linear-gradient(180deg, #F5F8FB, #FFFDFA); border-color: rgba(150,190,210,0.18); }
.cc-3 { background: linear-gradient(180deg, #FFFDF8, #FFFBF5); border-color: rgba(217,185,145,0.20); }

.cc-name {
  font-family: "Noto Serif SC", serif;
  font-size: 17px; font-weight: 900;
  letter-spacing: 2px;
  color: var(--text);
  margin-bottom: 2mm;
}
.cc-content { font-size: 12px; color: var(--text-mid); line-height: 2; }

.expo-block {
  margin-top: 4mm;
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF8 100%);
  padding: 4mm;
  text-align: center;
  border-radius: 10px;
  border: 2px solid rgba(224,123,76,0.12);
  box-shadow: var(--card-shadow);
  position: relative; z-index: 1;
}

.expo-title {
  font-family: "Noto Serif SC", serif;
  font-size: 18px; font-weight: 900;
  letter-spacing: 3px;
  color: var(--text);
  margin-bottom: 2mm;
}
.expo-desc { font-size: 12px; color: var(--text-mid); letter-spacing: 1px; }

.expo-flow {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 2mm;
  margin-top: 3mm;
  font-size: 12px;
  color: var(--text-mid);
  flex-wrap: wrap;
  font-weight: 500;
}
.step {
  background: var(--white);
  padding: 2mm 4mm;
  border-radius: 16px;
  border: 2px solid rgba(224,123,76,0.15);
  font-weight: 700;
  box-shadow: 0 1px 4px rgba(60,30,10,0.03);
}
.arrow {
  color: var(--accent-warm);
  font-family: "Noto Serif SC", serif;
  font-size: 16px;
  font-weight: 700;
}

@media (max-width: 768px) {
  .channel-grid { grid-template-columns: 1fr; }
}
</style>
