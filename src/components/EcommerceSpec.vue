<template>
  <section class="ecommerce">
    <div class="section-header fade-in">
      <span class="sec-num">12</span>
      <span class="sec-tag">✦ 电商详情页规范</span>
      <p class="sec-desc">统一结构（13 步标准流程）</p>
    </div>

    <div class="ec-grid fade-in">
      <div class="ec-step" v-for="s in steps" :key="s.num">
        <div class="ec-num">{{ s.num }}</div>
        <strong>{{ s.title }}</strong>
        <span class="ec-sub">{{ s.sub }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  { num: '01', title: '品牌印象', sub: 'KV 主视觉' },
  { num: '02', title: '品牌理念', sub: '为什么做' },
  { num: '03', title: '产品矩阵', sub: '系列介绍' },
  { num: '04–08', title: '产品展示', sub: '逐个介绍' },
  { num: '09', title: '原料页', sub: '真实食材' },
  { num: '10–11', title: '产品信息', sub: '详细参数' },
  { num: '12', title: '工艺品质', sub: '信任背书' },
  { num: '13', title: '品牌收尾', sub: '价值输出' },
]
</script>

<style scoped>
.ecommerce {
  padding: 7mm 12mm;
  position: relative;
  overflow: hidden;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.section-header { position: relative; z-index: 1; margin-bottom: 5mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 50px; font-weight: 900;
  color: rgba(217,185,145,0.07);
  position: absolute; top: -14px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 11px; letter-spacing: 6px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 2mm; }
.sec-desc { font-size: 13px; color: var(--text-mid); letter-spacing: 2px; }

.ec-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 3mm;
  position: relative; z-index: 1;
}

.ec-step {
  padding: 4mm 3mm;
  text-align: center;
  border-radius: 10px;
  border: 2px solid rgba(217,185,145,0.13);
  background: #FFFDF9;
  box-shadow: 0 1px 6px rgba(60,30,10,0.03);
  transition: transform 0.3s;
}
.ec-step:nth-child(odd) { background: #FFFBF6; }
.ec-step:hover { transform: translateY(-2px); }

.ec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 12px;
  color: var(--accent-warm);
  letter-spacing: 2px;
  font-weight: 700;
  margin-bottom: 2mm;
}
.ec-step strong {
  display: block;
  font-size: 13px;
  color: var(--text);
  font-weight: 700;
  margin-bottom: 1mm;
}
.ec-sub { font-size: 11px; color: var(--text-light); }

@media (max-width: 768px) {
  .ec-grid { grid-template-columns: repeat(2, 1fr); }
}
</style>
