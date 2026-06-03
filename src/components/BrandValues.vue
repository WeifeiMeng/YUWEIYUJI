<template>
  <section class="section bg-cool">
    <div class="blob blob-green" style="width:320px;height:320px;bottom:-100px;left:-100px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;text-align:center;">
        <div class="section-tag">品牌价值观</div>
      </div>

      <div class="values-grid fade-in">
        <div class="value-card" v-for="(v, i) in values" :key="i" :class="'v-' + (i + 1)">
          <span class="value-icon">{{ v.icon }}</span>
          <div class="value-name">{{ v.name }}</div>
          <div class="value-desc">{{ v.desc }}</div>
        </div>
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
.values-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}

.value-card {
  text-align: center;
  padding: 44px 20px;
  border-radius: var(--card-radius);
  box-shadow: var(--card-shadow);
  border: 2px solid transparent;
  transition: transform 0.3s, box-shadow 0.3s;
}
.value-card:hover { transform: translateY(-6px); box-shadow: var(--card-shadow-lg); }

.v-1 { background: linear-gradient(180deg, #FFF5EE, #FFFDFA); border-color: rgba(224,123,76,0.18); }
.v-2 { background: linear-gradient(180deg, #F7FAF3, #FFFDFA); border-color: rgba(165,185,140,0.22); }
.v-3 { background: linear-gradient(180deg, #FFFBF3, #FFFDFA); border-color: rgba(217,185,145,0.22); }
.v-4 { background: linear-gradient(180deg, #FFF7F5, #FFFDFA); border-color: rgba(200,160,140,0.20); }

.value-icon { font-size: 48px; display: block; margin-bottom: 16px; }
.value-name {
  font-family: "Noto Serif SC", serif;
  font-size: 28px;
  font-weight: 900;
  letter-spacing: 4px;
  color: var(--text);
  margin-bottom: 10px;
}
.value-desc { font-size: 15px; color: var(--text-mid); }

@media (max-width: 768px) {
  .values-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 480px) {
  .values-grid { grid-template-columns: 1fr; }
}
</style>
