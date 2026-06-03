<template>
  <section class="section bg-warm">
    <div class="blob blob-gold" style="width:360px;height:360px;top:-80px;right:-80px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">品牌未来三年规划</div>
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
.timeline {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.t-phase {
  padding: 44px 28px;
  border-radius: var(--card-radius);
  text-align: center;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
  transition: transform 0.3s;
}
.t-phase:hover { transform: translateY(-6px); }
.tp-1 { background: linear-gradient(180deg, #FFF5EE, #FFFDF9); border-color: rgba(224,123,76,0.20); }
.tp-2 { background: linear-gradient(180deg, #FFFDF8, #FFF9F2); border-color: rgba(217,185,145,0.25); }
.tp-3 { background: linear-gradient(180deg, #FFF8F2, #FFFDF9); border-color: rgba(194,104,58,0.20); }

.tp-year {
  font-family: "Noto Serif SC", serif;
  font-size: 18px;
  letter-spacing: 6px;
  font-weight: 700;
  display: inline-block;
  padding: 8px 20px;
  border-radius: 20px;
  margin-bottom: 20px;
}
.tp-1 .tp-year { background: rgba(224,123,76,0.10); color: var(--accent-warm); }
.tp-2 .tp-year { background: rgba(217,185,145,0.15); color: var(--accent-deep); }
.tp-3 .tp-year { background: rgba(194,104,58,0.10); color: var(--accent-deep); }

.tp-title {
  font-family: "Noto Serif SC", serif;
  font-size: 26px;
  font-weight: 900;
  letter-spacing: 3px;
  color: var(--text);
  margin-bottom: 20px;
}
.tp-items { font-size: 17px; color: var(--text-mid); line-height: 2.5; }

@media (max-width: 768px) {
  .timeline { grid-template-columns: 1fr; }
}
</style>
