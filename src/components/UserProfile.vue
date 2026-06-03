<template>
  <section class="section bg-neutral">
    <div class="blob blob-gold" style="width:380px;height:380px;bottom:-100px;right:-100px;"></div>

    <div class="section-inner">
      <div class="fade-in" style="margin-bottom:48px;">
        <div class="section-tag">用户画像</div>
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
.user-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 56px;
}

.sub-label { font-size: 18px; color: var(--text-mid); margin-bottom: 20px; letter-spacing: 2px; }

.user-demographic {
  background: linear-gradient(145deg, #FFF5EE 0%, #FFFDF9 100%);
  padding: 36px 32px;
  border-radius: var(--card-radius);
  border: 2px solid rgba(224,123,76,0.14);
  box-shadow: var(--card-shadow);
}

.user-stat {
  font-family: "Noto Serif SC", serif;
  font-size: 80px;
  font-weight: 900;
  color: var(--accent-warm);
  line-height: 1;
}
.stat-unit { font-size: 32px; }

.stat-desc { font-size: 16px; color: var(--text-mid); margin-top: 8px; }

.user-traits {
  list-style: none;
  margin-top: 24px;
}
.user-traits li {
  font-size: 17px;
  color: var(--text-mid);
  padding: 12px 0;
  border-bottom: 2px dotted var(--border);
}
.user-traits li::before {
  content: "✦ ";
  color: var(--accent-warm);
  font-size: 12px;
}

.user-needs {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}

.user-need {
  padding: 36px 20px;
  text-align: center;
  border-radius: var(--card-radius);
  font-family: "Noto Serif SC", serif;
  font-size: 22px;
  letter-spacing: 3px;
  color: var(--text);
  border: 2px solid transparent;
  box-shadow: var(--card-shadow);
  transition: transform 0.3s;
}
.user-need:hover { transform: translateY(-4px); }

.un-1 { background: #FFFDF9; border-color: rgba(224,123,76,0.22); }
.un-2 { background: #FFFDF9; border-color: rgba(217,185,145,0.25); }
.un-3 { background: #FFFDF9; border-color: rgba(180,150,120,0.22); }
.un-4 { background: #FFFDF9; border-color: rgba(200,170,140,0.22); }

.need-emoji { display: block; font-size: 40px; margin-bottom: 12px; }

@media (max-width: 768px) {
  .user-grid { grid-template-columns: 1fr; }
  .user-stat { font-size: 56px; }
}
</style>
