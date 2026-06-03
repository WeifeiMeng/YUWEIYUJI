<template>
  <section class="user">
    <div class="blob blob-gold"></div>
    <div class="section-header fade-in">
      <span class="sec-num">05</span>
      <span class="sec-tag">✦ 用户画像</span>
    </div>

    <div class="user-grid fade-in">
      <div>
        <p class="sub-label">核心用户</p>
        <div class="user-demographic">
          <div class="user-stat">25–40<span class="stat-unit">岁</span></div>
          <div class="stat-desc">养猫人群 · 城市女性占比约 70%</div>
          <ul class="user-traits">
            <li v-for="t in traits" :key="t">{{ t }}</li>
          </ul>
        </div>
      </div>
      <div>
        <p class="sub-label">他们购买的不仅是宠物食品</p>
        <div class="user-needs">
          <div class="user-need" v-for="(n, i) in needs" :key="i" :class="'un-' + (i + 1)">
            <span class="need-emoji">{{ n.emoji }}</span>
            {{ n.label }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const traits = ['把宠物当家人', '重视陪伴感', '喜欢高颜值产品', '愿意为品质买单', '喜欢记录养宠生活']
const needs = [
  { emoji: '🔒', label: '安全感' },
  { emoji: '✨', label: '仪式感' },
  { emoji: '💝', label: '陪伴感' },
  { emoji: '🎨', label: '品质感' },
]
</script>

<style scoped>
.user {
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
  width: 160px; height: 160px;
  background: radial-gradient(circle, rgba(217,185,145,0.11) 0%, transparent 70%);
  bottom: -40px; right: -40px;
  border-radius: 50%;
  pointer-events: none;
}

.section-header { position: relative; z-index: 1; margin-bottom: 5mm; }
.sec-num {
  font-family: "Noto Serif SC", serif;
  font-size: 50px; font-weight: 900;
  color: rgba(217,185,145,0.07);
  position: absolute; top: -14px; right: 0;
  line-height: 1;
}
.sec-tag { font-size: 11px; letter-spacing: 6px; color: var(--accent-warm); font-weight: 700; display: block; margin-bottom: 3mm; }

.user-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 5mm;
  position: relative;
  z-index: 1;
}

.sub-label { font-size: 13px; color: var(--text-mid); margin-bottom: 3mm; letter-spacing: 2px; }

.user-demographic {
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF9 100%);
  padding: 5mm;
  border-radius: 12px;
  border: 2px solid rgba(224,123,76,0.12);
  box-shadow: var(--card-shadow);
}

.user-stat {
  font-family: "Noto Serif SC", serif;
  font-size: 52px; font-weight: 900;
  color: var(--accent-warm);
  line-height: 1;
}
.stat-unit { font-size: 22px; }

.stat-desc { font-size: 12px; color: var(--text-mid); margin-top: 2mm; }

.user-traits {
  list-style: none;
  margin-top: 3mm;
}
.user-traits li {
  font-size: 12px; color: var(--text-mid);
  padding: 2mm 0;
  border-bottom: 2px dotted var(--border);
}
.user-traits li::before {
  content: "✦ ";
  color: var(--accent-warm);
  font-size: 10px;
}

.user-needs {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3mm;
}

.user-need {
  padding: 5mm 3mm;
  text-align: center;
  border-radius: 12px;
  font-family: "Noto Serif SC", serif;
  font-size: 17px;
  letter-spacing: 2px;
  color: var(--text);
  border: 2px solid transparent;
  box-shadow: var(--card-shadow);
  transition: transform 0.3s;
}
.user-need:hover { transform: translateY(-2px); }

.un-1 { background: #FFFDF9; border-color: rgba(224,123,76,0.22); }
.un-2 { background: #FFFDF9; border-color: rgba(217,185,145,0.25); }
.un-3 { background: #FFFDF9; border-color: rgba(180,150,120,0.22); }
.un-4 { background: #FFFDF9; border-color: rgba(200,170,140,0.22); }

.need-emoji { display: block; font-size: 28px; margin-bottom: 2mm; }

@media (max-width: 768px) {
  .user-grid { grid-template-columns: 1fr; }
}
</style>
