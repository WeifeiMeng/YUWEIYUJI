<template>
  <section class="future">
    <div class="blob blob-gold"></div>
    <div class="section-header fade-in">
      <span class="sec-num">11</span>
      <span class="sec-tag">✦ 品牌未来三年规划</span>
    </div>

    <div class="timeline fade-in">
      <div class="t-phase" v-for="(p, i) in phases" :key="p.year" :class="'tp-' + (i + 1)">
        <span class="tp-year">{{ p.year }}</span>
        <h3 class="tp-title">{{ p.title }}</h3>
        <div class="tp-items">
          <span v-for="item in p.items" :key="item">{{ item }}<br /></span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const phases = [
  { year: '2025–2026', title: '品牌基础矩阵', items: ['餐盒', '主食冻干', '彩虹吊卡'] },
  { year: '2026–2027', title: '完善陪伴体系', items: ['猫条', '冻干桶', '节日礼盒'] },
  { year: '2027–2028', title: '建立守护体系', items: ['功能零食', '营养补充品', '四季成长系列'] },
]
</script>

<style scoped>
.future {
  padding: 7mm 12mm;
  position: relative;
  overflow: hidden;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.blob-gold {
  position: absolute;
  width: 180px; height: 180px;
  background: radial-gradient(circle, rgba(217,185,145,0.10) 0%, transparent 70%);
  top: -40px; right: -40px;
  border-radius: 50%;
  pointer-events: none;
}

.section-header { position: relative; z-index: 1; margin-bottom: 5mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 50px; font-weight: 900;
  color: rgba(224,123,76,0.06);
  position: absolute; top: -14px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 11px; letter-spacing: 6px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 3mm; }

.timeline {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 4mm;
  position: relative; z-index: 1;
}

.t-phase {
  padding: 5mm 4mm;
  border-radius: 12px;
  text-align: center;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
  transition: transform 0.3s;
}
.t-phase:hover { transform: translateY(-2px); }
.tp-1 { background: linear-gradient(180deg, #FFF5EE, #FFFDF9); border-color: rgba(224,123,76,0.18); }
.tp-2 { background: linear-gradient(180deg, #FFFDF8, #FFF9F2); border-color: rgba(217,185,145,0.22); }
.tp-3 { background: linear-gradient(180deg, #FFF8F2, #FFFDF9); border-color: rgba(194,104,58,0.18); }

.tp-year {
  font-family: "Noto Serif SC", serif;
  font-size: 14px; letter-spacing: 4px;
  font-weight: 700;
  display: inline-block;
  padding: 2mm 4mm;
  border-radius: 14px;
  margin-bottom: 3mm;
}
.tp-1 .tp-year { background: rgba(224,123,76,0.10); color: var(--accent-warm); }
.tp-2 .tp-year { background: rgba(217,185,145,0.15); color: var(--accent-deep); }
.tp-3 .tp-year { background: rgba(194,104,58,0.10); color: var(--accent-deep); }

.tp-title {
  font-family: "Noto Serif SC", serif;
  font-size: 19px; font-weight: 900;
  letter-spacing: 2px;
  color: var(--text);
  margin-bottom: 3mm;
}
.tp-items { font-size: 13px; color: var(--text-mid); line-height: 2.3; }

@media (max-width: 768px) {
  .timeline { grid-template-columns: 1fr; }
}
</style>
