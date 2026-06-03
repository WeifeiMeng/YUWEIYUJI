<template>
  <section class="values">
    <div class="section-header fade-in">
      <span class="sec-num">03</span>
      <span class="sec-tag">✦ 品牌价值观</span>
    </div>

    <div class="values-grid fade-in">
      <div class="value-card" v-for="(v, i) in values" :key="i" :class="'v-' + (i + 1)">
        <span class="value-icon">{{ v.icon }}</span>
        <div class="value-name">{{ v.name }}</div>
        <div class="value-desc">{{ v.desc }}</div>
      </div>
    </div>
  </section>
</template>

<script setup>
const values = [
  { icon: '🤲', name: '真诚', desc: '认真做好每一份产品' },
  { icon: '🌿', name: '自然', desc: '尊重食材本来的样子' },
  { icon: '💛', name: '陪伴', desc: '珍惜成长中的每一天' },
  { icon: '🛡️', name: '安心', desc: '让每一次投喂都值得信赖' },
]
</script>

<style scoped>
.values {
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
  color: rgba(165,185,140,0.05);
  position: absolute; top: -12px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 10px; letter-spacing: 5px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 2mm; }

.values-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 3mm;
  position: relative;
  z-index: 1;
}

.value-card {
  text-align: center;
  padding: 4mm 3mm;
  border-radius: 10px;
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
}

.v-1 { background: linear-gradient(180deg, #FFF5EE 0%, #FFFDFA 100%); border-color: rgba(224,123,76,0.16); }
.v-2 { background: linear-gradient(180deg, #F7FAF3 0%, #FFFDFA 100%); border-color: rgba(165,185,140,0.20); }
.v-3 { background: linear-gradient(180deg, #FFFBF3 0%, #FFFDFA 100%); border-color: rgba(217,185,145,0.20); }
.v-4 { background: linear-gradient(180deg, #FFF7F5 0%, #FFFDFA 100%); border-color: rgba(200,160,140,0.18); }

.value-icon { font-size: 24px; display: block; margin-bottom: 2mm; }
.value-name {
  font-family: "Noto Serif SC", serif;
  font-size: 19px; font-weight: 900;
  letter-spacing: 2px;
  color: var(--text);
  margin-bottom: 1.5mm;
}
.value-desc { font-size: 11px; color: var(--text-mid); }

@media (max-width: 768px) {
  .values-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 480px) {
  .values-grid { grid-template-columns: 1fr; }
}
</style>
