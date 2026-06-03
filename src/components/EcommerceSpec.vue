<template>
  <section class="section bg-neutral">
    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">电商详情页规范</div>
        <p class="section-subtitle">统一结构（13 步标准流程）</p>
      </div>

      <div class="ec-grid fade-in">
        <div class="ec-step" v-for="s in steps" :key="s.num">
          <div class="ec-num">{{ s.num }}</div>
          <strong>{{ s.title }}</strong>
          <span class="ec-sub">{{ s.sub }}</span>
        </div>
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
.ec-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
}

.ec-step {
  padding: 28px 16px;
  text-align: center;
  border-radius: var(--card-radius);
  border: 2px solid rgba(217,185,145,0.14);
  background: #FFFDF9;
  box-shadow: 0 2px 10px rgba(60,30,10,0.03);
  transition: transform 0.3s;
}
.ec-step:nth-child(odd) { background: #FFFBF6; }
.ec-step:hover { transform: translateY(-4px); }

.ec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 16px;
  color: var(--accent-warm);
  letter-spacing: 2px;
  font-weight: 700;
  margin-bottom: 8px;
}
.ec-step strong {
  display: block;
  font-size: 17px;
  color: var(--text);
  font-weight: 700;
  margin-bottom: 6px;
}
.ec-sub { font-size: 14px; color: var(--text-light); }

@media (max-width: 768px) {
  .ec-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 480px) {
  .ec-grid { grid-template-columns: 1fr; }
}
</style>
